# Relatório de Técnicas Utilizadas — Projeto Allbirds

## 1. Visão geral

O projeto Allbirds é uma interface de e-commerce desenvolvida com HTML e CSS. A estrutura enviada contém duas páginas:

- `index.html`: página inicial, com navegação, banner principal (hero), área de destaques e rodapé.
- `modelos.html`: página de modelos, com quatro produtos apresentados em faixas alternadas de imagem e texto.

O projeto também utiliza arquivos CSS separados, imagens, ícones SVG e fontes locais.

## 2. HTML utilizado

### Estrutura do documento

- `<!DOCTYPE html>` para declarar o documento HTML5.
- `lang="pt-BR"` para indicar o idioma.
- `meta charset="UTF-8"` para suportar caracteres especiais.
- `meta name="viewport"` para controlar a apresentação em dispositivos móveis.
- `title` para definir o título de cada página.

### Elementos semânticos e organização

Foram utilizados elementos como:

- `header` para o cabeçalho.
- `nav` para a navegação.
- `main` na página de modelos para agrupar o conteúdo principal.
- `section` para agrupar áreas de conteúdo.
- `footer` para o rodapé.
- `ul` e `li` para listas de navegação, destaques e modelos.
- `h1`, `h2` e `h3` para títulos e hierarquia de conteúdo.
- `p` e `span` para textos e informações dos produtos.
- `a` para links e chamadas para ação.
- `label` e `input type="email"` para o campo de inscrição por e-mail.
- `img` com atributos `alt` para descrever imagens.

### Atributos de acessibilidade observados

- Textos alternativos (`alt`) nas imagens de produtos e redes sociais.
- `aria-label` nos links que contêm ícones, identificando sua finalidade.
- `alt=""` nos ícones decorativos acompanhados por um `aria-label` no link.

## 3. CSS utilizado

### Organização dos arquivos

Os estilos estão separados por responsabilidade:

| Arquivo | Responsabilidade |
|---|---|
| `style.css` | Configurações gerais, fontes, links e estilos globais |
| `header.css` | Cabeçalho, navegação e banner principal |
| `destaques.css` | Composição visual da seção de destaques |
| `modelos.css` | Apresentação dos quatro modelos de produtos |
| `footer.css` | Rodapé, inscrição, redes sociais e navegação inferior |

### Tipografia personalizada

O projeto utiliza `@font-face` para carregar arquivos locais da família Ubuntu em quatro pesos:

- 300 — Light
- 400 — Regular
- 500 — Medium
- 700 — Bold

A fonte é aplicada globalmente ao `body`.

### Reset e configurações globais

- Seletor universal `*` para aplicar `box-sizing: border-box` e zerar margens.
- Estilos globais para `body`, listas e links.
- Definição de cor de fundo, família tipográfica e comportamento padrão dos links.

## 4. Técnicas de layout

### Flexbox

Flexbox é utilizado em diferentes áreas:

- Alinhamento horizontal da navegação.
- Distribuição dos blocos do cabeçalho.
- Posicionamento do conteúdo do hero.
- Organização dos botões da seção de destaques.
- Composição vertical dos textos dos produtos.
- Alternância entre imagem e texto na página de modelos.
- Organização do conteúdo e das redes sociais no rodapé.
- Reorganização em coluna em telas menores.

Propriedades observadas incluem `display: flex`, `flex-direction`, `justify-content`, `align-items`, `flex-wrap`, `gap` e `flex-shrink`.

### CSS Grid

Grid é utilizado principalmente:

- Na composição das imagens da seção de destaques.
- Na distribuição das colunas de navegação do rodapé.
- Na reorganização das colunas do rodapé em telas menores.

Propriedades observadas incluem `display: grid`, `grid-template-columns`, `grid-template-rows`, `grid-column` e `grid-row`.

### Seletores e posicionamento de elementos

O projeto utiliza:

- Seletores de classe e de elemento.
- Pseudo-classes `:hover`, `:first-child`, `:nth-child()`, `:nth-child(odd)`, `:nth-child(even)` e `:not()`.
- `position: relative` em elementos da composição visual.
- `overflow: hidden` para controlar o conteúdo dentro de áreas delimitadas.

## 5. Imagens e proporções

- `object-fit: cover` para preencher áreas de imagem sem distorcer a proporção.
- `object-position` para ajustar o enquadramento.
- `aspect-ratio` para manter proporções dos blocos em layouts responsivos.
- `background-image`, `background-size`, `background-position` e `background-repeat` no banner principal.
- Uso de imagens em formatos JPG e ícones SVG.

## 6. Responsividade

Foram identificadas media queries para diferentes larguras:

- `max-width: 1390px` na seção de destaques.
- `max-width: 768px` no cabeçalho, destaques, modelos e rodapé.
- `max-width: 390px` na seção de destaques.

As adaptações incluem:

- Redimensionamento de áreas e imagens.
- Mudança de layouts horizontais para verticais.
- Uso de `flex-wrap` para permitir que os itens ocupem mais de uma linha.
- Mudança da quantidade de colunas no Grid.
- Ajuste de espaçamentos, fontes e proporções.
- Uso de `clamp()` para dimensionar um título de forma flexível.

## 7. Efeitos e interação visual em CSS

- `:hover` para alterar a aparência de links e botões.
- `transition` para suavizar a mudança de cor do botão Comprar.
- `transform: scale()` para pequenos efeitos de destaque em links e ícones.

Esses efeitos são visuais e foram implementados em CSS, sem necessidade de JavaScript.

## 8. Recursos e funcionalidades que ainda dependem de implementação

Na versão analisada, alguns links estão com `href="#"`, incluindo links de categorias, redes sociais, navegação e botões de compra. Eles funcionam como destinos provisórios e ainda precisam receber seus destinos reais.

O campo de e-mail está presente visualmente, mas não foi identificada integração de envio ou processamento de cadastro.

Não foi identificado JavaScript no projeto analisado. Portanto, o relatório não atribui ao projeto filtros funcionais, carrinho, autenticação, processamento de compras ou integração com back-end.

## 9. Relação com os estudos

Os conhecimentos de HTML, CSS, Flexbox e CSS Grid aparecem aplicados diretamente na estrutura e no layout do projeto.

O projeto também oferece prática com assuntos específicos de CSS, como:

- `@font-face`;
- media queries;
- pseudo-classes;
- `object-fit` e `aspect-ratio`;
- seletores estruturais como `:nth-child()`;
- efeitos com `transition` e `transform`;
- composição de layouts com Flexbox e Grid.

Este relatório registra técnicas encontradas nos arquivos enviados. Ele não afirma que todos esses recursos foram ensinados no curso; diferencia o que foi aplicado no projeto dos conteúdos cuja origem no curso ainda precisa ser confirmada.

## 10. Conclusão

O Allbirds reúne duas páginas construídas com HTML e CSS, utilizando estruturação de conteúdo, tipografia local, Flexbox, Grid, imagens, efeitos visuais e media queries. A organização dos estilos em arquivos separados permite localizar e manter cada parte da interface com mais clareza.

O projeto demonstra a aplicação prática de fundamentos de desenvolvimento front-end, mantendo JavaScript e integrações de e-commerce como etapas futuras.
