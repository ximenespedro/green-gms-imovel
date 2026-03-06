# Especificacao Frontend — Apartamento Itaim Bibi

## Visao Geral

HTML unico, self-contained (CSS + JS inline), estilo Apple scroll narrativo.
Cinematografico, premium, muito espaco em branco, animacoes lentas.
NAO deve parecer anuncio imobiliario comum. E uma apresentacao curada.

## Dados do Imovel

- **Endereco:** Rua Iaia 112, Itaim Bibi, Sao Paulo
- **Area:** 107 m2
- **Quartos:** 3 (sendo 1 home office reversivel)
- **Vaga:** 1 fixa ao lado do elevador
- **Valor:** R$ 1.850.000
- **Condominio:** R$ 1.990/mes
- **IPTU:** 10x de R$ 510

## Contatos CTA

- **Cristiano** (Proprietario): +1 512 788 2841
- **Luciana** (Corretora SP): +55 11 99739 4095

---

## Design Tokens

### Cores (derivadas do branding Green GMS)

| Token | Hex | Uso |
|-------|-----|-----|
| --green-primary | #05AB41 | Botoes CTA WhatsApp, icones ativos |
| --green-dark | #019C39 | Hover de botoes |
| --blue-dark | #053087 | Titulos de secao, header |
| --blue-deeper | #012877 | Hover titulos |
| --yellow-accent | #FDD216 | Badges destaque, icones features |
| --white | #FFFFFF | Background principal |
| --off-white | #F8F8F8 | Background secoes alternadas |
| --gray-light | #F0F0F0 | Background cards |
| --gray-medium | #8A8A8A | Texto secundario, labels |
| --gray-dark | #32373c | Texto corpo |
| --black | #1A1A1A | Texto headline hero |
| --overlay | rgba(0,0,0,0.35) | Overlay sobre fotos com texto |

### Tipografia

| Elemento | Font | Weight | Size (mobile) | Size (desktop) |
|----------|------|--------|---------------|----------------|
| Hero headline | Inter ou Playfair Display | 700 | 28px | 48px |
| Secao titulo | Inter | 600 | 22px | 36px |
| Corpo | Inter | 400 | 16px | 18px |
| Label/apoio | Inter | 400 | 13px | 14px |
| CTA botao | Inter | 600 | 16px | 18px |
| Numeros destaque | Inter | 700 | 32px | 56px |

Carregar via Google Fonts (CDN externo permitido).

### Espacamento

- Padding horizontal mobile: 24px
- Padding horizontal desktop: max-width 1200px, centrado
- Gap entre secoes: 80px mobile / 120px desktop
- Cada secao ocupa ~100vh ou proximo disso

---

## Estrutura de Secoes (15 telas)

### SECAO 1 — Hero / Abertura

- **Layout:** Fullscreen (100vh), foto background cover, overlay escuro
- **Headline:** "Amplo, elegante e a poucos passos da Faria Lima"
- **Subheadline:** "Um apartamento raro no Itaim Bibi"
- **Info:** "107 m2 | 3 quartos | 1 vaga fixa | Rua Iaia 112"
- **Apoio:** "A poucos passos da Faria Lima, Infinity Tower e dos principais escritorios e restaurantes do bairro."
- **Foto:** sala-living-janela.jpg (foto da sala com janelao — arquivo `19.34.40.jpeg`)
- **Animacao:** Fade-in lento do titulo (1.5s), zoom muito sutil na imagem (scale 1.0 -> 1.05 em 10s)
- **Elemento:** Seta discreta "scroll" no bottom center, pulsando

### SECAO 2 — Proposta de Valor

- **Layout:** Texto centralizado sobre fundo off-white
- **Titulo:** "Espaco, localizacao e versatilidade"
- **Texto:** "Um apartamento com planta generosa, ambientes bem distribuidos e excelente iluminacao natural, em uma das localizacoes mais desejadas de Sao Paulo."
- **Foto:** sala-ampla-arte.jpg (sala panoramica com quadro — arquivo `19.34.40 (1).jpeg`)
- **Animacao:** Texto entra primeiro (fade-up), imagem sobe suavemente depois

### SECAO 3 — Sala

- **Layout:** Foto dominante (~70% tela) + texto lateral (desktop) ou abaixo (mobile)
- **Titulo:** "Sala ampla e iluminada"
- **Texto:** "Area de convivencia com janelas amplas, piso de madeira em excelente estado e ar condicionado instalado. Layout ideal para estar, jantar e receber com conforto."
- **Fotos (carousel):**
  1. sala-janela.jpg — `19.34.40.jpeg` (sala com janelao e ar-condicionado)
  2. sala-arte-pb.jpg — `19.34.39 (2).jpeg` (sala com quadro P&B)
  3. sala-panoramica.jpg — `19.34.40 (1).jpeg` (vista ampla com corredor)
  4. sala-arte-colorida.jpg — `19.34.40 (2).jpeg` (sala com quadro colorido e estante)
- **Animacao:** Parallax leve, fade between fotos

### SECAO 4 — Home Office Reversivel

- **Layout:** Foto dominante + texto
- **Titulo:** "Home office completo, reversivel para quarto"
- **Texto:** "Hoje configurado com duas estacoes de trabalho prontas, armarios embutidos e excelente aproveitamento de espaco. Pode voltar a ser quarto com facilidade, sem reforma."
- **Fotos (carousel):**
  1. escritorio.jpg — `19.34.39.jpeg` (estantes em L + armario)
- **Animacao:** Fade-in ao entrar na viewport

### SECAO 5 — Corredor / Area Intima

- **Layout:** Foto full-width + texto overlay ou abaixo
- **Titulo:** "Privacidade na area intima"
- **Texto:** "A area intima e separada da sala por porta de correr, trazendo mais privacidade ao dia a dia. O corredor conta ainda com armario roupeiro, excelente para organizacao."
- **Fotos:**
  1. corredor.jpg — `19.34.40 (10).jpeg` (corredor com armarios)
- **Animacao:** Fade suave

### SECAO 6 — Suite Principal

- **Layout:** Carousel de fotos + texto
- **Titulo:** "Suite principal com excelente capacidade de armarios"
- **Texto:** "Suite confortavel, silenciosa e bem iluminada, com armarios estilo walk-in, sapateira e 10 portas de armario no total."
- **Fotos (carousel):**
  1. suite-quarto.jpg — `19.34.40 (8).jpeg` (suite ampla com armario)
  2. suite-closet.jpg — `19.34.39 (3).jpeg` (closet com prateleiras)
  3. suite-banheiro.jpg — `19.34.39 (4).jpeg` (banheiro suite com box)
- **Animacao:** Parallax leve, swipe no carousel

### SECAO 7 — Segundo Quarto

- **Layout:** Foto + texto
- **Titulo:** "Segundo quarto espacoso"
- **Texto:** "Ambiente versatil, com armarios embutidos, ideal para quarto, hospedes ou apoio familiar."
- **Fotos (carousel):**
  1. quarto2.jpg — `19.34.40 (9).jpeg` (quarto armario, parede azul)
  2. quarto2-b.jpg — `19.34.39 (1).jpeg` (quarto vazio parede cinza)
- **Animacao:** Fade-in

### SECAO 8 — Banheiros

- **Layout:** Grid 2 colunas (desktop) ou carousel (mobile)
- **Titulo:** "Banheiros reformados"
- **Texto:** "Acabamento moderno, box em vidro, marcenaria planejada e ducha Deca de altissima pressao."
- **Fotos:**
  1. banheiro-suite.jpg — `19.34.39 (4).jpeg` (banheiro com box vidro)
  2. banheiro-social.jpg — `19.34.40 (7).jpeg` (banheiro espelho grande)
- **Animacao:** Fade-in escalonado

### SECAO 9 — Cozinha

- **Layout:** Carousel de fotos grande + texto
- **Titulo:** "Cozinha moderna e funcional"
- **Texto:** "Marcenaria planejada, excelente circulacao e bancada de apoio. Os azulejos em estilo portugues trazem identidade e personalidade ao ambiente."
- **Fotos (carousel):**
  1. cozinha-geral.jpg — `19.34.39 (6).jpeg` (vista completa com mesa)
  2. cozinha-bancada.jpg — `19.34.40 (4).jpeg` (bancada e azulejos)
  3. cozinha-copa.jpg — `19.34.40 (5).jpeg` (area refeicao com adega)
  4. cozinha-completa.jpg — `19.34.40 (6).jpeg` (vista com TV e area servico)
- **Animacao:** Parallax leve

### SECAO 10 — Localizacao Corporativa

- **Layout:** Fundo claro, texto centralizado, lista com distancias
- **Titulo:** "A poucos passos da Faria Lima"
- **Subtitulo:** "Distancias medidas pelo Google Maps caminhando"
- **Lista animada (surge uma a uma no scroll):**
  - Infinity Tower — 160 m | 2 min
  - Google, BTG, Morgan Stanley e J.P. Morgan — 550 m | 7 min
  - Bank of America Merrill Lynch e Itau BBA — 650 m | 8 min
- **Visual:** Fundo off-white, sem foto. Icones minimalistas ou pontos no mapa
- **Animacao:** Itens surgem um a um conforme scroll (stagger 200ms)

### SECAO 11 — Ecossistema Juridico

- **Layout:** Texto centralizado sobre fundo branco
- **Titulo:** "No centro de uma das regioes mais estrategicas de Sao Paulo"
- **Texto:** "Entre 300 e 800 metros de grandes escritorios como Lefosse, TozziniFreire, Lobo de Rizzo, Machado Meyer, Araujo e Policastro, Mundie, Veirano e PLKC. Tambem proximo de bancas internacionais como White & Case, Linklaters, Hogan Lovells e A&O Shearman."
- **Visual:** Fundo branco, tipografia forte, sem foto
- **Animacao:** Fade-in suave

### SECAO 12 — Lifestyle

- **Layout:** Cards horizontais com scroll ou lista elegante
- **Titulo:** "O melhor do Itaim a pe"
- **Texto:** "Restaurantes, padarias e cafes entre 3 e 8 minutos caminhando."
- **Lista:** Nino Cucina, Due Cuochi, Barbacoa, Rubaiyat, Le Vin, Tatu Bola, Benjamin, Mani Manioca, Rascal e La Tambouille
- **Apoio:** "Uma regiao plana, agradavel e feita para caminhar."
- **Visual:** Cards com nome do restaurante em tipografia elegante, fundo off-white
- **Animacao:** Scroll horizontal dentro do vertical OU cascata

### SECAO 13 — Educacao e Investimento

- **Layout:** Blocos com fundo neutro, tipografia grande
- **Titulo:** "Excelente tambem para familias e estudantes"
- **Texto bloco 1:** "Uma opcao rara para familias de fora de Sao Paulo que buscam mais conforto do que as kitnets tao comuns hoje em dia."
- **Texto bloco 2:** "Quando a familia visita, o apartamento oferece estrutura real de moradia. Tambem permite receber colegas para estudos em grupo com conforto."
- **Dados:**
  - Insper — 7 min de carro
  - IBMEC — 11 min de carro
- **Fecho:** "Apos a graduacao, muitos profissionais passam a trabalhar justamente nas empresas da Faria Lima, a poucos minutos do imovel."
- **Animacao:** Blocos fade-in escalonado

### SECAO 14 — Numeros do Imovel

- **Layout:** Grid de numeros destacados, fundo off-white
- **Titulo:** "Detalhes"
- **Numeros (counter animation ou fade individual):**
  - 107 m2
  - 3 quartos
  - 1 vaga fixa ao lado do elevador
  - Predio muito bem mantido
- **Valores:**
  - Venda: R$ 1.850.000
  - Condominio: R$ 1.990/mes
  - IPTU: 10x de R$ 510
- **Animacao:** Counter animation nos numeros, fade nos textos

### SECAO 15 — CTA Final

- **Layout:** Tela limpa, centralizada, muito respiro
- **Titulo:** "Agende sua visita"
- **Contatos (2 botoes WhatsApp lado a lado ou empilhados mobile):**
  - Botao 1: "Cristiano (Proprietario)" -> wa.me/15127882841
  - Botao 2: "Luciana (Corretora SP)" -> wa.me/5511997394095
- **Apoio:** "Visitas com agendamento."
- **Footer:** Logo Green GMS pequeno
- **Animacao:** Entrada suave, sem excesso

---

## Mapeamento de Fotos -> Nomes para Hospedagem

Renomear antes de subir ao GitHub:

| Arquivo Original | Nome Limpo | Secao |
|-----------------|------------|-------|
| WhatsApp Image 2026-03-05 at 19.34.39.jpeg | escritorio.jpg | 4 |
| WhatsApp Image 2026-03-05 at 19.34.39 (1).jpeg | quarto2-b.jpg | 7 |
| WhatsApp Image 2026-03-05 at 19.34.39 (2).jpeg | sala-arte-pb.jpg | 3 |
| WhatsApp Image 2026-03-05 at 19.34.39 (3).jpeg | suite-closet.jpg | 6 |
| WhatsApp Image 2026-03-05 at 19.34.39 (4).jpeg | banheiro-suite.jpg | 6, 8 |
| WhatsApp Image 2026-03-05 at 19.34.39 (5).jpeg | quarto3-listrado.jpg | 7 (alternativa) |
| WhatsApp Image 2026-03-05 at 19.34.39 (6).jpeg | cozinha-geral.jpg | 9 |
| WhatsApp Image 2026-03-05 at 19.34.39 (7).jpeg | sala-janela.jpg | 1, 3 |
| WhatsApp Image 2026-03-05 at 19.34.40.jpeg | sala-living.jpg | 2, 3 |
| WhatsApp Image 2026-03-05 at 19.34.40 (1).jpeg | sala-panoramica.jpg | 3 |
| WhatsApp Image 2026-03-05 at 19.34.40 (2).jpeg | sala-arte-colorida.jpg | 3 |
| WhatsApp Image 2026-03-05 at 19.34.40 (3).jpeg | sala-corredor-arte.jpg | 3 (extra) |
| WhatsApp Image 2026-03-05 at 19.34.40 (4).jpeg | cozinha-bancada.jpg | 9 |
| WhatsApp Image 2026-03-05 at 19.34.40 (5).jpeg | cozinha-copa.jpg | 9 |
| WhatsApp Image 2026-03-05 at 19.34.40 (6).jpeg | cozinha-completa.jpg | 9 |
| WhatsApp Image 2026-03-05 at 19.34.40 (7).jpeg | banheiro-social.jpg | 8 |
| WhatsApp Image 2026-03-05 at 19.34.40 (8).jpeg | suite-quarto.jpg | 6 |
| WhatsApp Image 2026-03-05 at 19.34.40 (9).jpeg | quarto2.jpg | 7 |
| WhatsApp Image 2026-03-05 at 19.34.40 (10).jpeg | corredor.jpg | 5 |

## Hospedagem de Imagens

- Repositorio GitHub do usuario (public ou raw URLs)
- Base URL: `https://raw.githubusercontent.com/{user}/{repo}/main/fotos/`
- Formato: JPEG otimizado (comprimir para ~200KB cada antes de subir)
- Todas as imagens devem ter alt text descritivo para acessibilidade

---

## Comportamento Responsivo

| Breakpoint | Comportamento |
|-----------|---------------|
| < 768px (mobile) | Single column, fotos full-width, texto abaixo, carousels com swipe |
| 768-1024px (tablet) | Texto lateral em algumas secoes, 2 colunas nos banheiros |
| > 1024px (desktop) | Max-width 1200px centrado, texto lateral, parallax mais pronunciado |

## Animacoes (Intersection Observer)

- Fade-up: elementos entram de baixo (translateY 30px -> 0, opacity 0 -> 1)
- Stagger: itens de lista entram com delay de 150-200ms entre si
- Parallax: fotos movem mais lento que o scroll (translateY baseado no scroll)
- Counter: numeros contam de 0 ate o valor final em ~2s
- Carousel: swipe touch no mobile, setas no desktop, dots indicadores
- Transicao entre slides: fade ou slide horizontal (300ms ease)

## Performance

- Lazy loading em todas as imagens (loading="lazy")
- Imagens abaixo do fold nao carregam ate o scroll chegar perto
- CSS e JS inline (zero requests externos alem das imagens e fonte)
- Fonte: carregar Inter via Google Fonts com display=swap
- Target: < 3s de First Contentful Paint em 4G

## Acessibilidade

- Alt text em todas as imagens
- Contraste minimo AA nos textos sobre fotos (overlay adequado)
- Botoes CTA com area de toque minima 44x44px
- Navegacao por teclado funcional no carousel
- Semantica HTML5 (section, header, nav, main, footer)
