# Guia de Configuração do Google Tag Manager (GTM) — Maufe Telas

Este documento explica como o Google Tag Manager (GTM) deve ser integrado ao novo site desenvolvido em Astro.

A tag configurada para o projeto é: **GTM-K97TQB9**.

---

## Como funciona no Astro vs. WordPress (Elementor)

No WordPress/Elementor, a injeção do código do GTM geralmente era feita por meio de plugins ou em campos de configuração globais. 

No Astro, não precisamos de plugins. O site utiliza um arquivo de layout base chamado `src/layouts/Layout.astro` que envolve todas as páginas do site (a Home, a Política de Privacidade e os Termos de Uso). 
Ao inserirmos o código do GTM nesse arquivo único, ele é replicado automaticamente para todas as páginas do site, garantindo o rastreamento completo de visualizações de páginas e conversões.

---

## Os Códigos a serem Inseridos

O GTM requer a inserção de dois blocos de código:

### 1. Bloco do `<head>` (Script Principal)
Deve ser posicionado o mais alto possível dentro da tag `<head>` do arquivo [Layout.astro](file:///d:/Projetos/Paginas/maufetelas/src/layouts/Layout.astro). Este código inicializa o rastreamento.

```html
<!-- Google Tag Manager -->
<script is:inline>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-K97TQB9');</script>
<!-- End Google Tag Manager -->
```

> **Nota de Desenvolvimento:** No Astro, adicionamos o atributo `is:inline` na tag `<script>` para garantir que o compilador não otimize nem mova esse script de lugar, mantendo-o exatamente no topo do `<head>` conforme exigido pelo Google.

### 2. Bloco do `<body>` (Noscript Fallback)
Deve ser posicionado imediatamente após a abertura da tag `<body>` no arquivo [Layout.astro](file:///d:/Projetos/Paginas/maufetelas/src/layouts/Layout.astro). Ele garante o rastreamento caso o usuário esteja navegando com JavaScript desativado.

```html
<!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-K97TQB9"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->
```

---

## Onde os códigos são inseridos na prática

No arquivo [Layout.astro](file:///d:/Projetos/Paginas/maufetelas/src/layouts/Layout.astro), a estrutura final fica exatamente assim:

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <!-- Google Tag Manager -->
    <script is:inline>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
    new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
    j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
    'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
    })(window,document,'script','dataLayer','GTM-K97TQB9');</script>
    <!-- End Google Tag Manager -->

    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    ...
  </head>
  <body class="...">
    <!-- Google Tag Manager (noscript) -->
    <noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-K97TQB9"
    height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
    <!-- End Google Tag Manager (noscript) -->

    <slot />
  </body>
</html>
```

---

## Verificação e Validação

Uma vez inserido o código:
1. Abra o site em ambiente de desenvolvimento (`npm run dev`) ou produção.
2. Utilize a extensão oficial **Tag Assistant Companion** do Chrome ou entre no modo Preview no painel do seu Google Tag Manager (GTM).
3. Verifique se o container `GTM-K97TQB9` está disparando corretamente.
