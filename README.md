# 🔵 LinkedIn Profile – 

Recriação do perfil do LinkedIn do professor **Carlos Eduardo Simões Pelegrin** utilizando **HTML5 semântico** e **CSS puro**, como projeto acadêmico da disciplina de desenvolvimento web.

---

## 👥 Integrantes do Grupo

> 

| Nome | RA |
|------|----|
|  Victor hugo de souza junqueira    | 60018315   |
|    João otavio cardoso vilela  |    | 60020628
|      |    |
|      |    |

---

## 📁 Estrutura do Projeto

```
linkedin-pelegrin/
├── index.html        → Estrutura HTML da página
├── estilo.css        → Todos os estilos CSS (classes em português)
├── foto-perfil.svg   → Imagem de perfil (placeholder SVG)
├── capa.svg          → Imagem de capa (placeholder SVG)
└── README.md         → Este arquivo
```

---

## 🚀 Como Executar

1. **Clone ou descompacte** o projeto em uma pasta local.
2. **Abra o arquivo `index.html`** diretamente no navegador (Google Chrome, Firefox, Edge etc.).
3. Não é necessário servidor web — é um projeto estático puro.

> **Dica:** Se quiser substituir as imagens de placeholder pelas fotos reais, basta renomear suas imagens para `foto-perfil.svg` (ou `.jpg`/`.png`) e `capa.svg` (ou `.jpg`/`.png`) e atualizar o atributo `src` nas tags `<img>` correspondentes no `index.html`.

---

## 🏗️ Tecnologias Utilizadas

| Tecnologia | Versão/Detalhe |
|------------|----------------|
| HTML5 | Semântico, com tags estruturais (`<header>`, `<main>`, `<section>`, `<nav>`, `<aside>`, `<ul>`, `<li>`, etc.) |
| CSS3 | Puro, sem frameworks — Grid, Flexbox, variáveis CSS, z-index, border-radius |
| SVG | Ícones e imagens placeholder inline/externos |

---

## 🎨 Decisões de Implementação

### Tags HTML utilizadas (referência W3Schools)

| Tag | Uso no projeto |
|-----|---------------|
| `<header>` | Cabeçalho de navegação fixo |
| `<nav>` | Barra de navegação principal e links do rodapé |
| `<main>` | Conteúdo principal da página |
| `<section>` | Cada card/seção do perfil (Sobre, Experiência, Formação) |
| `<aside>` | Colunas laterais esquerda e direita |
| `<h1>` – `<h3>` | Hierarquia de títulos (nome, cargo, empresa) |
| `<p>` | Parágrafos de texto descritivo |
| `<ul>` / `<li>` | Listas de experiências, formações, sugestões |
| `<a>` | Links de navegação e conexões |
| `<button>` | Botões de ação (conectar, editar, premium) |
| `<input>` | Campo de busca |
| `<img>` | Foto de perfil e imagem de capa |
| `<strong>` | Destaque em textos (nome de empresas) |
| `<svg>` | Ícones vetoriais (logo LinkedIn, ícones de menu) |

### Layout com CSS Grid e Flexbox

- A grade principal usa **CSS Grid** com 3 colunas (`grid-template-columns: 1fr 2fr 1fr`)
- Os cards internos usam **Flexbox** para alinhar foto, texto e botões
- O cabeçalho usa **`position: fixed`** com **`z-index: 100`** para ficar sempre visível

### Z-index e sobreposição

Um requisito do projeto era usar `z-index` para sobrepor elementos. Isso foi aplicado em:

```css
/* A capa fica na camada base */
.area-capa {
  position: relative;
  z-index: 1;
}

/* A foto sobe sobre a capa com z-index maior */
.area-foto-perfil {
  position: relative;
  z-index: 10;
  margin-top: -40px; /* Empurra para cima, sobre a capa */
}

/* O botão de edição flutua sobre o card inteiro */
.acoes-card-topo {
  position: absolute;
  top: 108px;
  right: 12px;
  z-index: 20;
}

/* O cabeçalho fixo fica acima de tudo */
.cabecalho-navegacao {
  position: fixed;
  z-index: 100;
}
```

### Foto arredondada

A foto de perfil é arredondada usando:

```css
.moldura-foto {
  border-radius: 50%;   /* torna o quadrado em círculo */
  overflow: hidden;     /* corta a imagem no formato circular */
  border: 3px solid #ffffff; /* borda branca ao redor */
}
```

### Classes em Português

Todas as classes CSS foram nomeadas em **português**, por exemplo:

- `.cabecalho-navegacao` — cabeçalho de navegação
- `.area-foto-perfil` — área da foto de perfil
- `.lista-experiencias` — lista de experiências
- `.item-formacao` — item de formação acadêmica
- `.botao-primario` / `.botao-secundario` — botões de ação

---

## 📐 Seções Replicadas

- [x] **Cabeçalho de Navegação** — Logo LinkedIn, busca, ícones, avatar, botão Premium
- [x] **Dados Pessoais** — Capa, foto circular, nome, título, localização, conexões, botões
- [x] **Sobre** — Texto de apresentação profissional
- [x] **Experiências Profissionais** — 5 experiências (Unipar, Senac, Smartgreen, Positivo, Freelancer)
- [x] **Formação Acadêmica** — Mestrado (UEM) e Bacharelado (Unipar)

---

## 📱 Responsividade

O layout se adapta a telas menores:

- **< 960px**: Remove a coluna direita, layout em 2 colunas
- **< 640px**: Layout em 1 coluna, oculta rótulos de navegação

---

## 📚 Referências

- [W3Schools – HTML Tags by Function](https://www.w3schools.com/tags/ref_byfunc.asp)
- [LinkedIn – Perfil original](https://www.linkedin.com/in/cpelegrin/)
- [MDN Web Docs – CSS z-index](https://developer.mozilla.org/pt-BR/docs/Web/CSS/z-index)
- [MDN Web Docs – CSS Grid Layout](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_grid_layout)
- [MDN Web Docs – border-radius](https://developer.mozilla.org/pt-BR/docs/Web/CSS/border-radius)
