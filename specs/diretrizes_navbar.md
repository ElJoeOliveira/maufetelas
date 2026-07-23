# Diretrizes de Implementação de Navbar com Comportamento de Scroll

Este documento descreve o padrão arquitetural e as boas práticas para implementar uma navbar com comportamento visual dinâmico ao rolar a página (scroll), usando **Astro + Tailwind CSS**.

---

## 1. O Problema a Evitar

Abordagens ingênuas para animar a navbar no scroll frequentemente falham por conflito de especificidade CSS. Os erros mais comuns são:

- Tentar modificar `left`, `right` ou `width` via CSS (`.navbar-scrolled { left: Xrem }`) enquanto o elemento possui classes Tailwind como `left-0 right-0` — o Tailwind pode sobrescrever dependendo da ordem de carregamento.
- Tentar modificar `height` do elemento para criar o efeito de "destaque" — o usuário não percebe a mudança de altura de forma intuitiva.
- Usar `style is:global` para sobrescrever classes Tailwind — a ordem de injeção do CSS no Astro não é garantida e pode resultar em comportamento inconsistente.
- Usar `max-w-[XX%]` como largura do estado encolhido — em telas largas, uma porcentagem pode resultar em valor *maior* que o estado inicial fixo (`max-w-7xl` = 1280px), causando *expansão* em vez de encolhimento.

---

## 2. A Arquitetura Correta: Dois Elementos Aninhados

A solução robusta usa **dois elementos aninhados** com responsabilidades distintas:

```html
<!-- Elemento externo: âncora de posicionamento, sempre full-width -->
<header id="navbar-wrapper" class="fixed top-0 left-0 right-0 z-50 px-0 transition-all duration-500">

  <!-- Elemento interno: detém o visual (fundo, borda, sombra) e o max-width -->
  <div id="navbar" class="mx-auto w-full max-w-7xl bg-[...] border border-transparent transition-all duration-500">

    <!-- Conteúdo da navbar aqui -->

  </div>
</header>
```

### Por que funciona

- O `<header>` externo é sempre `left-0 right-0` — nunca é modificado. Sua única função é posicionar.
- O `<div>` interno (`#navbar`) é quem recebe o fundo, a borda e o `max-width`. Ao mudar o `max-width` dele via `classList`, o efeito visual de encolhimento é real e animável.
- O `transition-all duration-500` no `<div>` interno garante a animação suave de `max-width`.

---

## 3. Estado Inicial (Topo da Página)

O `<div>` interno deve iniciar com:

```html
<div
  id="navbar"
  class="mx-auto w-full max-w-7xl bg-[rgba(R,G,B,0.96)] border border-transparent transition-all duration-500"
>
```

- `max-w-7xl` (ou o mesmo `max-width` usado pelo container de conteúdo do site) — garante alinhamento visual com o restante da página.
- `bg-[rgba(R,G,B,0.96)]` — fundo quase sólido, visível desde o carregamento. Evita o problema de "navbar invisível" em modo mobile ou hero claro.
- `border border-transparent` — reserva o espaço da borda sem exibi-la, prevenindo saltos de layout ao adicioná-la no scroll.

---

## 4. Estado Scrolled (Após Rolagem)

Todo o comportamento de scroll deve ser controlado **exclusivamente via JavaScript com `classList`**, nunca via CSS puro ou inline style para propriedades que conflitem com Tailwind.

```js
const wrapper = document.getElementById('navbar-wrapper');
const navbar  = document.getElementById('navbar');

if (wrapper && navbar) {
  window.addEventListener('scroll', () => {
    if (window.scrollY > 20) {
      navbar.classList.remove('max-w-7xl', 'border-transparent', 'bg-[rgba(R,G,B,0.96)]');
      navbar.classList.add(
        'max-w-[VALOR_FIXO_EM_PX]',   // ex: 'max-w-[1200px]'
        'bg-[rgba(R,G,B,0.55)]',       // transparência leve
        'backdrop-blur-xl',
        'border-[rgba(R,G,B,0.45)]',   // borda colorida sutil
        'shadow-[0_4px_30px_rgba(0,0,0,0.6)]',
        'rounded-xl'                   // leve arredondamento
      );
      wrapper.classList.add('pt-3');    // descola levemente do topo
      wrapper.classList.remove('pt-0');
    } else {
      navbar.classList.add('max-w-7xl', 'border-transparent', 'bg-[rgba(R,G,B,0.96)]');
      navbar.classList.remove(
        'max-w-[VALOR_FIXO_EM_PX]',
        'bg-[rgba(R,G,B,0.55)]',
        'backdrop-blur-xl',
        'border-[rgba(R,G,B,0.45)]',
        'shadow-[0_4px_30px_rgba(0,0,0,0.6)]',
        'rounded-xl'
      );
      wrapper.classList.remove('pt-3');
      wrapper.classList.add('pt-0');
    }
  }, { passive: true });
}
```

---

## 5. Regra Crítica: Largura do Estado Scrolled em Pixels Fixos

> **Nunca use `max-w-[XX%]` para o estado encolhido.**

O estado scrolled deve usar um valor **fixo em pixels** (ex: `max-w-[1200px]`) que seja **sempre menor** que o estado inicial (`max-w-7xl` = 1280px).

| Estado | Classe | Valor |
|--------|--------|-------|
| Inicial | `max-w-7xl` | 1280px |
| Scrolled | `max-w-[1200px]` | 1200px ✅ |
| ❌ Errado | `max-w-[94%]` | ~1440px em telas largas ❌ |

**Motivo:** `max-w-[94%]` de um viewport de 1536px = 1443px — maior que 1280px, causando expansão em vez de encolhimento.

A redução recomendada é entre **60px e 120px** para que o encolhimento seja perceptível sem parecer excessivo.

---

## 6. Efeito Visual Desejado no Scroll

Ao rolar a página, o usuário deve perceber:

1. **Encolhimento lateral:** a barra fica visivelmente mais estreita, centralizada na tela.
2. **Descolamento do topo:** leve `padding-top` no wrapper cria a sensação de "flutuar".
3. **Fundo semitransparente:** `bg-[rgba(..., 0.55)]` + `backdrop-blur-xl` cria o efeito glass.
4. **Borda colorida:** use a cor de destaque (accent) da marca com opacidade entre `0.35` e `0.55`.
5. **Arredondamento:** `rounded-xl` ou `rounded-2xl` para suavizar o container encolhido.

---

## 7. O que NÃO fazer

| ❌ Não fazer | ✅ Fazer |
|---|---|
| Modificar `left`/`right` do `<header>` fixo | Modificar `max-width` do `<div>` interno |
| Usar `style is:global` para sobrescrever Tailwind | Usar `classList.add/remove` no JavaScript |
| Usar `max-w-[XX%]` para largura encolhida | Usar `max-w-[XXXpx]` com valor fixo menor que o inicial |
| Reduzir altura da navbar para sinalizar destaque | Reduzir largura — o usuário percebe, altura passa despercebida |
| Iniciar navbar com `bg-transparent` | Iniciar com fundo visível (`opacity > 0.9`) |
| Usar inline `style=` para animações de scroll | Usar `classList` — o `transition-all` do Tailwind cuida da animação |
