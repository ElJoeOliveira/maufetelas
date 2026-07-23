# Estrutura de Conteúdo e Copywriting — Maufe Telas

Este documento apresenta a estrutura completa de conteúdo para o novo site da **Maufe Telas**, elaborado sob a ótica de copywriting de alta conversão. Ele serve como especificação direta para o desenvolvimento do site em Astro + Tailwind CSS, mapeando todas as seções, textos, links e ativos de imagens disponíveis.

---

## 1. Meta Conteúdo (SEO)

*   **Page Title (SEO):** Maufe Telas | Redes de Proteção e Telas Mosquiteiras em Mato Grosso do Sul
*   **Meta Description:** Proteja sua família, seus pets e seu lar contra quedas e insetos. Redes de proteção certificadas e telas mosquiteiras sob medida em todo o Mato Grosso do Sul. Orçamento rápido via WhatsApp em até 12 minutos.
*   **Target Keywords:** redes de proteção Campo Grande MS, telas mosquiteiras, proteção para gatos, redes de proteção para sacadas, tela pet screen, proteção contra pombos.

---

## 2. Estrutura da Navbar (Navegação)

> [!NOTE]
> De acordo com as diretrizes do arquivo `specs/diretrizes_navbar.md`, a navbar deve usar âncoras de rolagem suave (`scroll-smooth`) para seções da própria página na página principal.

*   **Logo:** `referencias/imagens/C_Logo-Maufe-600px.png` (ou `referencias/imagens/C_Logo-Maufe-Quadrada-300x300.png.webp` para visual mobile/compacto).
*   **Links de Navegação:**
    1.  **Início** (`#home`)
    2.  **Soluções** (`#solucoes`)
    3.  **Depoimentos** (`#depoimentos`)
    4.  **Clientes** (`#clientes`)
    5.  **Dúvidas** (`#faq`)
*   **Botão de Ação (CTA na Navbar):**
    *   **Texto:** Projeto Personalizado
    *   **Link:** WhatsApp (`https://api.whatsapp.com/send?phone=5567991355250&text=%5BM0%5D%20Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20as%20Telas.`)
    *   **Anotação de Design:** Botão estilo *outline* que preenche no *hover*, destacando-se sutilmente.

---

## 3. Seção Hero (Acima da Dobra)

*   **Identificador HTML:** `id="home"`
*   **Imagem de Fundo:** `referencias/imagens/GatoTela.jpg` (com sobreposição escura/gradiente para garantir legibilidade do texto).
*   **Headline:** Proteção real para quem você mais ama.
*   **Subheadline:** Redes de proteção certificadas e telas mosquiteiras sob medida que protegem sua família e seus pets sem comprometer a estética do seu lar.
*   **CTA Principal (Botão Flutuante/Destaque):**
    *   **Texto:** SOLICITAR ORÇAMENTO VIA WHATSAPP
    *   **Link:** WhatsApp (`https://api.whatsapp.com/send?phone=5567991355250&text=%5BM1%5D%20Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20as%20Telas.`)
    *   **Ícone:** WhatsApp (`fab fa-whatsapp`)
    *   **Estilo:** Botão com cor de destaque viva e pulsante (Accent Color), de alta visibilidade.

---

## 4. Seção Destaque / Conceito

*   **Texto em Destaque:** Carinho e proteção
*   **Anotação de Copy:** Seção de transição curta e visualmente limpa para introduzir a divisão de soluções com apelo afetivo.

---

## 5. Seção de Soluções ("Proteção para quem?")

*   **Identificador HTML:** `id="solucoes"`
*   **Título Principal:** Proteção para quem?
*   **Subtítulo:** Conheça nossa linha completa de redes de proteção e telas mosquiteiras projetadas para atender às necessidades específicas da sua casa ou empresa.

### Bloco A: Redes de Proteção (Segurança contra Quedas e Acidentes)

*   **Descrição Geral do Bloco:** Redes de alta densidade confeccionadas com polietileno 100% virgem (PEAD) com tratamento UV, instaladas rigorosamente conforme as normas de segurança ABNT NBR 16046. Suportam até 150kg/m² de impacto.

#### 1. Proteção para Janelas
*   **Imagem:** `referencias/imagens/Gato500.jpg.webp`
*   **Título:** Proteção para Janelas
*   **Copy:** Segurança total para apartamentos e sobrados. Proteja a curiosidade das crianças e garanta a segurança de todas as 7 vidas dos seus gatos em janelas de qualquer tamanho.

#### 2. Proteção para Sacadas
*   **Imagem:** `referencias/imagens/sacadas.jpg.webp`
*   **Título:** Proteção para Sacadas
*   **Copy:** Rede de proteção integrada de forma elegante à sua varanda ou sacada. Segurança completa sem bloquear a sua vista ou interferir na arquitetura do ambiente.

#### 3. Proteção para Quintais e Áreas Abertas
*   **Imagem:** `referencias/imagens/quintais.jpg.webp`
*   **Título:** Proteção para Quintais
*   **Copy:** Instalação de redes de proteção para fechamento de quintais, vãos livres e coberturas. Liberdade e tranquilidade para crianças e pets brincarem no quintal com segurança máxima.

#### 4. Redes Esportivas para Quadras
*   **Imagem:** `referencias/imagens/Quadra.jpg.webp`
*   **Título:** Proteção para Quadras
*   **Copy:** Projetamos e executamos quadras poliesportivas completas. Desde a fundação, montagem de estruturas metálicas de sustentação até o fechamento com redes esportivas de alta durabilidade.

#### 5. Gatis e Canis Profissionais
*   **Imagem:** `referencias/imagens/Gatis_Canis.jpg.webp`
*   **Título:** Proteção para Gatis e Canis
*   **Copy:** Telas especiais projetadas para clínicas veterinárias, hotéis pet e centros de adestramento. Máxima contenção e segurança sem prejudicar a ventilação e a iluminação dos animais.

#### 6. Bloqueio Contra Pombos em Fachadas
*   **Imagem:** `referencias/imagens/Pombos_Fachadas.jpg.webp`
*   **Título:** Proteção Contra Pombos em Fachadas
*   **Copy:** Solução mecânica discreta e ecologicamente correta para afastar pombos e morcegos. Protege a saúde pública, a higiene e preserva a fachada do seu estabelecimento comercial ou condomínio.

---

### Bloco B: Telas Mosquiteiras (Proteção contra Insetos)

*   **Descrição Geral do Bloco:** Esquadrias em alumínio sob medida com tela em fibra de vidro revestida com PVC. Material antichama, super resistente, lavável e quase invisível, mantendo a ventilação natural fresca e impedindo a entrada de insetos e animais peçonhentos.

#### 7. Proteção contra Mosquitos
*   **Imagem:** `referencias/imagens/Mosquiteira.jpg.webp`
*   **Título:** Proteção c/ Mosquitos (Janelas)
*   **Copy:** Bloqueio definitivo contra mosquitos da dengue, pernilongos, moscas, baratas e escorpiões. A melhor alternativa ao ar-condicionado para desfrutar da brisa natural com tranquilidade absoluta.

#### 8. Telas Mosquiteiras para Portas Comuns
*   **Imagem:** `referencias/imagens/Mosquiteiras_Portas_Comuns.jpg.webp`
*   **Título:** Tela Mosquiteira para Porta Comum
*   **Copy:** Portas mosquiteiras sob medida com perfis de alumínio reforçados e dobradiças automáticas. Passagem livre para a ventilação mantendo os insetos totalmente do lado de fora da casa.

#### 9. Telas Mosquiteiras para Portas de Correr
*   **Imagem:** `referencias/imagens/Mosquiteiras_Portas_Correr.jpg.webp`
*   **Título:** Tela Mosquiteira para Porta de Correr
*   **Copy:** Solução deslizante com trilhos suaves e vedação magnética ou com escovas periféricas. Perfeita para portas balcão de varandas ou áreas de lazer de alto padrão.

---

*   **CTA de Fechamento da Seção de Serviços:**
    *   **Texto:** CLIQUE AQUI PARA ORÇAMENTO VIA WHATSAPP
    *   **Link:** WhatsApp (`https://api.whatsapp.com/send?phone=5567991355250&text=%5BM2%5D%20Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20as%20Telas.`)

---

## 6. Seção Prova Social (Coleção de Elogios)

*   **Título:** Coleção de elogios
*   **Subtítulo:** Todos os dias tem alguém elogiando nosso trabalho, nosso atendimento e nossa equipe.
*   **Descrição:** Carrossel horizontal dinâmico com capturas de tela reais de clientes satisfeitos nos enviando feedback.
*   **Ativos Utilizados:** Imagens localizadas na pasta `referencias/elogios/` (arquivos `1.jpg` a `23.jpg`).

---

## 7. Seção de Agilidade (Orçamento Rápido)

*   **Título:** Orçamento Rápido
*   **Texto Principal:** Seu atendimento inicial pelo WhatsApp em até **12 minutinhos***. Você duvida? **CLIQUE E CONFIRA**.
*   **Nota de Rodapé:** *\*De segunda a sexta, em horário comercial, combinado?*
*   **CTA de Agilidade:**
    *   **Texto:** ORÇAMENTO RÁPIDO VIA WHATSAPP
    *   **Link:** WhatsApp (`https://api.whatsapp.com/send?phone=5567991355250&text=%5BM3%5D%20Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20as%20Telas.`)

---

## 8. Seção de Avaliação do Google ("E lá no Google?")

*   **Identificador HTML:** `id="depoimentos"`
*   **Título:** E LÁ NO GOOGLE?
*   **Selo de Destaque:** Imagem de 5 Estrelas.
*   **Texto de Apoio:** Somos 5 estrelas nas avaliações do Google. Nunca tivemos uma nota que não fosse 5 estrelas.
*   **Carrossel de Depoimentos:**
    *   > [!IMPORTANT]
    *   > As imagens de depoimentos do Google serão disponibilizadas posteriormente. Provisoriamente, o layout de desenvolvimento deve utilizar **placeholders visuais** representados por caixas estilizadas em Tailwind contendo o texto das avaliações simuladas.
    *   **Placeholder 1:** "Atendimento impecável! O instalador foi super profissional, deixou tudo limpinho e as telas ficaram ótimas. Recomendo muito!" — *Mariana S., Campo Grande*
    *   **Placeholder 2:** "Preço justo, agilidade incrível. Responderam no zap super rápido e no dia seguinte já estavam instalando. Minha gata agora está segura." — *Ricardo M., Dourados*
    *   **Placeholder 3:** "Trabalho de altíssima qualidade. Fizemos o fechamento da quadra do condomínio e as portas mosquiteiras do salão de festas. Ótimo acabamento." — *Síndico Cond. Alphaville*

---

## 9. Seção Clientes Corporativos ("Quem já se protegeu conosco")

*   **Identificador HTML:** `id="clientes"`
*   **Título:** quem já se protegeu conosco.
*   **Subtítulo:** Empresas, Instituições, órgãos governamentais, escolas, bares e restaurantes de Mato Grosso do Sul.
*   **Grid de Logos de Clientes:**
    *   `referencias/clientes/Funcional.jpg.webp` — Funcional
    *   `referencias/clientes/Estoril.jpg.webp` — Estoril
    *   `referencias/clientes/Eletrobras.jpg.webp` — Eletrobras
    *   `referencias/clientes/Delirio.jpg.webp` — Delírio
    *   `referencias/clientes/Cassems.jpg.webp` — Cassems
    *   `referencias/clientes/Elite.jpg.webp` — Elite
    *   `referencias/clientes/QuartaIgreja.jpg.webp` — Quarta Igreja
    *   `referencias/clientes/Paris6.jpg.webp` — Paris 6
    *   `referencias/clientes/NascenteAzul.jpg.webp` — Nascente Azul
    *   `referencias/clientes/IFMS.jpg.webp` — IFMS
    *   `referencias/clientes/Hook.jpg.webp` — Hook
    *   `referencias/clientes/Ponto-alto.jpg.webp` — Ponto Alto

---

## 10. Seção Construtoras e Condomínios ("Casas e Condomínios")

*   **Título:** Casas e Condomínios.
*   **Subtítulo:** Já protegemos mais de uma centena de condomínios das principais construtoras da cidade. Além de Casas, Chácaras e Fazendas.
*   **Grid de Logos de Construtoras/Condomínios:**
    *   `referencias/condominios/Damha.jpg.webp` — Damha
    *   `referencias/condominios/Alphaville2.jpg.webp` — Alphaville
    *   `referencias/condominios/Plaenge.jpg.webp` — Plaenge
    *   `referencias/condominios/Vanguard2.jpg.webp` — Vanguard
    *   `referencias/condominios/MRV.jpg.webp` — MRV
    *   `referencias/condominios/Tecol.jpg.webp` — Tecol

---

## 11. Seção FAQs / Dúvidas Frequentes

*   **Identificador HTML:** `id="faq"`
*   **Título:** PRINCIPAIS DÚVIDAS

### FAQ Parte 1: Redes de Proteção

1.  **A rede de proteção compromete a estética do ambiente?**
    *   *Resposta:* Não. Trabalhamos com redes discretas e fios finos, nas cores branca, cinza, preta e marrom, escolhidas para harmonizar com o ambiente, seja residencial, comercial ou corporativo. A escolha da cor não altera o valor do serviço. Nosso objetivo é manter a segurança sem prejudicar o visual elegante da fachada.
2.  **Quais são as especificações técnicas das redes de proteção da Maufe Telas?**
    *   *Resposta:* As nossas redes são fabricadas em polietileno de alta densidade (PEAD) com tratamento UV e antioxidante, fio 2 mm de altíssima resistência. Estão disponíveis nas malhas 5×5 cm (padrão residencial e comercial), malha 3×3 cm (indicada para proteção de gatos e pequenos pets) e malhas especiais para quadras esportivas.
3.  **As redes realmente aguentam o peso de uma criança ou de um animal?**
    *   *Resposta:* Sim. As redes suportam até 100 kg de peso constante e até 150 kg/m² de impacto, dependendo da resistência da alvenaria e fixação dos ganchos. Toda a instalação atende rigorosamente às normas da ABNT NBR 16046.
4.  **Qual é a durabilidade e quando devo substituir a rede?**
    *   *Resposta:* A durabilidade média é de 5 a 7 anos. No entanto, a recomendação da ABNT é que a substituição preventiva seja feita a partir de 3 anos de uso, principalmente em faces que recebem sol e chuva intensos.
5.  **As redes de proteção precisam de manutenção periódica?**
    *   *Resposta:* Sim. Recomendamos uma verificação visual anual para avaliar a tensão dos fios, o estado dos ganchos e das buchas. A Maufe Telas realiza visitas de manutenção periódica e revisão programada sob agendamento.
6.  **As redes são seguras mesmo em prédios muito altos?**
    *   *Resposta:* Sim, a altura não interfere na segurança. Nossos técnicos de instalação são plenamente qualificados e certificados para trabalho em altura (NR-35), utilizando ancoragens e fixações metálicas de alta resistência.
7.  **As redes podem ser instaladas em varandas de vidro, esquadrias ou estruturas personalizadas?**
    *   *Resposta:* Sim. Desenvolvemos projetos 100% sob medida. Adaptamos a fixação em varandas com fechamento de vidro, esquadrias de alumínio, madeira e estruturas especiais sem causar danos ou comprometer a integridade física dos caixilhos.
8.  **Tenho gatos. A rede resiste às unhas e ao peso deles ao escalar?**
    *   *Resposta:* Sim, é totalmente resistente. Para gatos, indicamos a malha de 3×3 cm, projetada com espaços menores para evitar que fiquem presos ou consigam passar as patas ou garras através da malha.
9.  **A instalação gera muita sujeira ou danifica a pintura das paredes?**
    *   *Resposta:* Não. Utilizamos brocas adequadas para reduzir poeira e isolamos os locais de furação quando necessário. Entregamos o espaço limpo e pronto para o uso imediato.
10. **Qual é o prazo médio de instalação?**
    *   *Resposta:* O prazo de instalação varia de 1 a 3 dias úteis a partir da medição do local e aceite do orçamento, a depender da quantidade de vãos.
11. **Vocês fazem redes para quadras esportivas?**
    *   *Resumo Técnico:* Sim. A Maufe Telas executa quadras completas, desde a fundação, montagem de estruturas metálicas e redes esportivas, até o acabamento final, atendendo escolas, clubes, condomínios e chácaras.
12. **Por que investir em uma rede de proteção premium?**
    *   *Resposta:* Segurança e durabilidade são investimentos em bem-estar. Redes de baixo custo frequentemente usam plástico reciclado sem proteção UV, enfraquecendo rapidamente. Na Maufe Telas, fornecemos materiais certificados que asseguram proteção real com durabilidade excepcional.

### Resumo Técnico (Exibido ao lado ou abaixo do FAQ de Redes):
*   **Fio:** 2 mm PEAD (Polietileno de Alta Densidade)
*   **Malhas:** 3×3 cm | 5×5 cm | Esportiva
*   **Cores:** Branco | Cinza | Preto | Marrom (sem custo adicional)
*   **Resistência:** até 100 kg peso constante | 150 kg/m²
*   **Normas:** ABNT NBR 16046
*   **Garantia:** 3 anos materiais | 1 ano mão de obra
*   **Atendimento:** Todo o Mato Grosso do Sul

---

### FAQ Parte 2: Telas Mosquiteiras

1.  **As telas mosquiteiras afetam a ventilação e a luminosidade dos cômodos?**
    *   *Resposta:* Não. A malha em fibra de vidro com revestimento de PVC é extremamente fina e possui excelente transparência, mantendo a passagem livre de ar e luz natural, sem alterar a estética dos ambientes.
2.  **É possível instalar sem danificar o caixilho ou o acabamento da janela?**
    *   *Resposta:* Sim. As telas são montadas em perfis de alumínio sob medida com encaixes e fixação por travas inteligentes ou ímãs, preservando esquadrias de alumínio, madeira, PVC e pintura original.
3.  **Qual o tempo de duração da tela mosquiteira?**
    *   *Resposta:* A vida útil média é de 5 a 8 anos, dependendo da incidência de sol e frequência de limpeza.
4.  **As telas impedem apenas mosquitos ou bloqueiam outros insetos e animais?**
    *   *Resposta:* Bloqueiam mosquitos (incluindo o Aedes aegypti), pernilongos, moscas, baratas, escorpiões, morcegos e pequenos pássaros.
5.  **É possível remover a tela para realizar a limpeza?**
    *   *Resposta:* Sim. Projetamos quadros removíveis e telas basculantes de fácil remoção e reposicionamento, facilitando a limpeza periódica tanto da tela quanto da janela.
6.  **Posso instalar em portas de correr, janelas com persianas integradas ou vidro temperado?**
    *   *Resposta:* Sim. Nossos sistemas são customizados e se integram perfeitamente a portas de correr, janelas integradas e vidros temperados (blindex), garantindo o correto fechamento de todas as frestas.
7.  **Como deve ser feita a limpeza das telas?**
    *   *Resposta:* Basta utilizar um espanador, aspirador de pó com bocal macio ou passar levemente um pano umedecido em água e sabão neutro. Evite produtos químicos abrasivos.
8.  **As telas alteram o visual externo da fachada do prédio ou casa?**
    *   *Resposta:* Praticamente não são notadas. Os perfis de alumínio da tela são pintados nas mesmas tonalidades das esquadrias da fachada (branco, preto, bronze, anodizado), atendendo às regras estéticas de condomínios exigentes.
9.  **Qual o prazo de instalação das telas mosquiteiras?**
    *   *Resposta:* O prazo médio de entrega e instalação é de 1 a 3 dias úteis após a medição e escolha das estruturas.
10. **É possível obter proteção contra mosquitos mantendo a visão limpa da paisagem?**
    *   *Resposta:* Sim. A fibra de vidro na cor cinza ou preta apresenta baixíssimo reflexo de luz, tornando-se praticamente invisível ao olhar de dentro para fora do imóvel.
11. **Existe garantia para telas mosquiteiras?**
    *   *Resposta:* Sim, fornecemos garantia contra defeitos de montagem, instalação e falhas de fabricação nos perfis e tecidos das telas.
12. **Posso instalar as telas mosquiteiras mesmo tendo cães ou gatos?**
    *   *Resposta:* Sim. Para lares com animais domésticos ativos, disponibilizamos a tela **Pet Screen**, uma malha de poliéster super reforçada e revestida com vinil que resiste a arranhões, mordidas e empurrões sem rasgar.
13. **Es possível integrar com automação ou esquadrias de altíssimo padrão?**
    *   *Resposta:* Sim. Desenvolvemos soluções integradas de telas mosquiteiras recolhíveis (tipo rolo) ou motorizadas que se adaptam a projetos arquitetônicos modernos e sistemas de automação residencial.
14. **Vale a pena investir em telas se eu já possuo ar-condicionado?**
    *   *Resposta:* Com certeza. Permite desligar o ar-condicionado em dias de temperatura amena para ventilar a casa naturalmente com ar fresco, gerando economia substancial de energia elétrica com total segurança contra insetos.
15. **A Maufe Telas atende empresas, restaurantes e indústrias?**
    *   *Resposta:* Sim. Instalamos telas mosquiteiras industriais e comerciais que atendem rigorosamente às normas da Vigilância Sanitária (ANVISA) para cozinhas industriais, restaurantes, hotéis e clínicas.

---

## 12. Seção de Fechamento / Impacto Emocional

*   **Imagem de Fundo/Lateral:** `referencias/imagens/CriancaGato3.jpg.webp`
*   **Headline de Fechamento:** O que realmente importa!
*   **Subheadline:** Proteção para os pequenos mais importantes da nossa vida.
*   **CTA de Alto Impacto:**
    *   **Texto:** QUERO PROTEGER MINHA FAMÍLIA AGORA
    *   **Link:** WhatsApp (`https://api.whatsapp.com/send?phone=5567991355250&text=%5BM4%5D%20Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20as%20Telas.`)

---

## 13. Seção Escopo Regional

*   **Imagem/Marca:** `referencias/imagens/C_Logo-Maufe-Quadrada-300x300.png.webp`
*   **Texto:** Atendemos **toda a região do Mato Grosso do Sul**, tanto com **fornecimento de materiais** quanto com **instalação completa**. Nossa equipe realiza atendimento presencial e logística personalizada conforme o tamanho e a localização do projeto.

---

## 14. Rodapé (Footer)

*   **Telefone:** (67) 9 9135-5250
*   **E-mail:** contato@maufetelas.com.br
*   **CNPJ:** 44.776.352/0001-09
*   **Certificações/Selo:** Certificado de SSL Seguro (`referencias/imagens/C_SSLSeguro-300x50.png` ou `C_SSLSeguro.png`)
*   **Links de Rodapé:** Política de Privacidade | Termos de Uso
*   **Créditos de Desenvolvimento:** Desenvolvido por [AnuncieCerto](https://anunciecerto.com.br)
*   **Link Discreto:** Retornar ao Topo (Scroll suave para `#home`).

---

## 15. Anotações de Copywriting e Gatilhos Mentais Aplicados

1.  **Clareza acima de tudo:** As soluções foram segmentadas de forma explícita. O usuário que busca segurança contra quedas encontra facilmente as redes; o que busca proteção contra insetos encontra as telas mosquiteiras, evitando confusão de finalidade de produto.
2.  **Gatilho de Prova Social Reversa:** A exibição proeminente de logotipos de grandes construtoras (Plaenge, Vanguard, Damha, Alphaville) transfere autoridade corporativa instantaneamente para o cliente residencial ("se eles confiam suas grandes obras à Maufe Telas, eu também posso confiar meu lar").
3.  **Quebra Ativa de Objeções (FAQ):** A divisão do FAQ em duas partes específicas (Redes e Telas) responde diretamente aos medos latentes do comprador: durabilidade, comprometimento estético da fachada do condomínio, resistência a gatos ativos (com a introdução do termo *Pet Screen*) e facilidade de higienização.
4.  **Uso do Humor e Simplicidade:** O texto curto nas seções de transição ("Para você que odeia pernilongos. Não se preocupe. Nós também os odiamos.") cria conexão imediata e empatia com o leitor.
5.  **CTA Direta e Redução de Atrito:** Em vez de "Fale Conosco" ou "Enviar Formulário", os CTAs utilizam verbos de ação com benefício ("Solicitar Orçamento via WhatsApp", "Orçamento Rápido em 12 minutos"), gerando pressa positiva e facilidade de contato imediato.

---

## 16. Alternativas de Headlines e CTAs para Testes de Conversão (A/B)

### Headlines Principais (Hero Section)

*   **Opção A (Foco em Segurança/Emocional - Principal):**
    *   *Texto:* Proteção real para quem você mais ama.
    *   *Racional:* Apela para a emoção e o instinto protetor de pais e tutores de pets.
*   **Opção B (Foco em Benefício Funcional):**
    *   *Texto:* Sua casa segura contra quedas e livre de insetos.
    *   *Racional:* Comunica diretamente os dois benefícios práticos dos produtos oferecidos.
*   **Opção C (Foco em Autoridade/Certificação):**
    *   *Texto:* Redes de proteção certificadas pela ABNT com instalação sob medida.
    *   *Racional:* Constrói credibilidade e confiança técnica logo na chegada ao site.

### Chamadas para Ação (CTAs)

*   **Opção A (Foco em Velocidade - Principal):**
    *   *Texto:* ORÇAMENTO RÁPIDO VIA WHATSAPP (em até 12 minutos)
    *   *Racional:* Ataca a principal dor do cliente moderno, que é a demora no retorno de orçamentos.
*   **Opção B (Foco em Conveniência):**
    *   *Texto:* SOLICITAR PROJETO PERSONALIZADO GRÁTIS
    *   *Racional:* Reduz o atrito comercial ao usar a palavra "grátis" e evocar exclusividade ("projeto personalizado").
