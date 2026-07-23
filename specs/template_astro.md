# Diretrizes para Desenvolvimento de Novas Páginas (Landing Pages)

Este documento serve como um guia padrão estrutural, de design e de boas práticas para o desenvolvimento de novas páginas (Landing Pages e sites institucionais) para diferentes clientes e segmentos de negócio, utilizando a mesma base arquitetural.

## 1. Stack Tecnológica
- **Framework:** [Astro](https://astro.build/) - Focado em performance e entrega de conteúdo estático rápido.
- **Estilização:** [Tailwind CSS](https://tailwindcss.com/) - Para desenvolvimento rápido e estilização baseada em utilitários diretamente no HTML.

## 2. Arquitetura e Estrutura de Componentes

A arquitetura do projeto divide as páginas entre **Página Principal (Home)** e **Subpáginas (Especialidades/Serviços)**.

### Páginas como Orquestradores
- Os arquivos `.astro` dentro da pasta `src/pages/` atuam apenas como índices de montagem.
- Eles importam os componentes, estruturam o layout (tags principais, SEO, divisores) e não devem conter lógica de marcação HTML complexa.

### Princípio da Responsabilidade Única (SRP) e Diretórios
- **Componentes Globais (`src/components/`):** Elementos compartilhados entre diversas páginas (ex: `Footer.astro`, Navbars).
- **Componentes Utilitários (`src/components/ui/`):** Elementos reutilizáveis genéricos (ex: Divisores, botões, cards).
- **Componentes de Contexto (`src/components/[niche]/`):** Cada seção visual de uma página possui seu componente específico isolado para uma especialidade (ex: `Hero.astro`, `FAQ.astro` dentro de uma pasta específica).

### Componentes Compartilhados (Exemplos)
- Carrossel ou Grade de Depoimentos/Reviews.
- Botões de Chamada para Ação (CTAs).
- Rodapé (Footer) global e divisores geométricos elegantes.

## 3. Diretrizes de Design e Identidade Visual

O design deve manter uma estética "Premium" focada em alta conversão.

### Tipografia Adaptável
- **Títulos e Destaques (Fonte Primária):** A fonte primária deve ser selecionada de acordo com o tom de voz da marca (ex: fontes Serif para transmitir autoridade e confiança, ou fontes Sans-serif arredondadas para um aspecto mais lúdico e amigável).
- **Textos e Botões (Fonte Secundária):** Utilizar sempre uma fonte limpa e de altíssima legibilidade (sans-serif) para facilitar a leitura em blocos de texto e rótulos.

### Paleta de Cores e Identidade da Marca
- **Flexibilidade Temática:** A paleta de cores será definida no briefing inicial de cada cliente. Não há obrigação de usar um padrão escuro (Dark Mode). O design deve respirar a identidade do negócio — seja um tema suave para um SPA, lúdico para uma loja infantil, ou escuro/sóbrio para um escritório corporativo.
- **Ritmo Visual e Contraste:** Independentemente de a paleta ser clara ou escura, alterne levemente os tons de fundo entre as seções para criar ritmo e facilitar a leitura e separação dos conteúdos.
- **Cor de Destaque (Accent Color):** É obrigatório o uso de uma cor viva e contrastante para botões de conversão (CTAs), palavras-chave e elementos de interação, guiando o olhar do usuário.

### Espaçamento e Layout
- Utilizar muito "respiro" (whitespace) entre as seções para sensação de luxo (ex: `py-16` ou `py-24`).
- Containers centralizados com larguras máximas adequadas para leitura.

## 4. Navegação (Navbar) e Fluxo do Usuário

A navegação deve ser intuitiva e manter o usuário focado na conversão.

### Comportamento Visual da Navbar
- **Topo da Página:** Geralmente transparente, mesclando-se com a seção Hero.
- **Ao Rolar a Página (Scroll):** A Navbar deve **se destacar e ficar flutuante (sticky/fixed)**. Ela pode se desprender do topo, adotar formato de "pílula" e ganhar fundo semi-transparente (backdrop blur).

### Regras de Roteamento da Navbar
- **Navegação Interna (Âncoras):** Os itens da Navbar **sempre** devem conduzir a uma seção da página atual (via scroll suave usando IDs) e **nunca** abrir uma subpágina ou navegar para fora do escopo atual.
- **Navbar da Página Principal:**
  - Os links no menu navegam para as seções da Home que indicam cada uma das especialidades do negócio.
  - Dentro do conteúdo de cada seção específica (e não no menu), haverá botões/links conduzindo o usuário para a Subpágina detalhada daquela especialidade.
- **Navbar das Subpáginas:**
  - Os links no menu navegam **apenas** pelas seções internas da própria subpágina.
  - Não deve haver links na Navbar da subpágina para retornar à página principal ou para ir a outras subpáginas.
- **Rodapé (Footer) das Subpáginas:**
  - O rodapé das subpáginas deve conter um link simples e discreto para retornar à Página Principal.

## 5. Chamadas para Ação (CTAs) e Conversão

- **Estilo de Botões:** Botões secundários ou de contato com WhatsApp costumam usar estilo "Outline" (vazado), preenchendo com a cor de destaque no *hover*.
- **Seção Final de Conversão:** A última seção antes do rodapé deve ser de alto impacto, com tipografia gigante, fundos texturizados ou escuros e fortes chamadas para a ação (ex: botões flutuantes ou em destaque).

## 6. Requisitos para Iniciar um Novo Projeto

Para garantirmos agilidade e fidelidade na criação de uma nova página, o cliente (ou responsável) deverá fornecer previamente o seguinte checklist:

1. **Nome da Empresa / Marca.**
2. **Documento de Briefing:** Informações detalhadas sobre o que a empresa oferece (serviços, produtos, diferenciais).
3. **Ativos Visuais:** Imagens em alta qualidade, Logotipos (preferencialmente vetores SVG ou PNG transparente) e Favicons.
4. **Identidade Visual:** Paleta de cores da marca (códigos HEX/RGB).
5. **Tema / Estilo Visual:** Referências de design, tom de voz e estilo desejado.
6. **Conteúdo Textual (Copy):**
  - Textos para a página principal (Headlines, descrições, CTAs).
  - Especialidades do negócio: Conteúdo detalhado para cada uma das subpáginas.

## 7. Boas Práticas Adicionais
- Mantenha o design responsivo (Mobile First), garantindo que as quebras do Tailwind sejam aplicadas corretamente.
- Otimize todas as imagens fornecidas utilizando as integrações nativas do Astro para máxima velocidade de carregamento.
