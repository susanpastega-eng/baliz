# Site Balíz

Landing page única da Balíz — mentorias e workshops de liderança.

**No ar:** [baliz.co](https://baliz.co) · publicado via GitHub Pages a partir do `index.html` na raiz do repositório.

## Arquitetura

Página única com navegação por anchor links. Não há páginas internas.

| Seção | Anchor | Conteúdo |
|---|---|---|
| Hero | — | Título, grafismo do farol, CTA "Começar agora" |
| Para quem | `#para-quem` | Quatro perfis atendidos |
| Mentorias | `#mentorias` | Cais, Mar Aberto e Oceano em cards que giram 180° ao clique |
| Workshops | `#workshops` | Workshops em grupo |
| Direção | — | Tópicos do método |
| Sobre | `#sobre` | Bio da fundadora com foto |
| Contato / rodapé | `#contato` | Newsletter, links, logo |

Links externos: **Diário de Bordo** aponta para a newsletter no Substack; **Começar agora** e **Contato** abrem `mailto:susan@baliz.co`.

## Publicação

O arquivo servido é um bundle standalone: HTML, CSS, JS (React via Babel) e todas as imagens embutidas como data URIs num único arquivo. Isso evita dependência de caminhos relativos de assets no GitHub Pages.

Fluxo de atualização:

1. Editar o fonte em `ui_kits/site/index.html` (no projeto de design)
2. Gerar o bundle standalone
3. Subir no repositório como `index.html` na raiz — via **Add file → Upload files**, arrastando o arquivo (não colar conteúdo em editor de texto: linhas muito longas podem truncar)

O arquivo `.nojekyll` na raiz impede o GitHub Pages de processar o HTML pelo Jekyll.

## Domínio

`baliz.co` (GoDaddy) aponta para o GitHub Pages via 4 registros A (`185.199.108–111.153`) e CNAME `www` → `susanpastega-eng.github.io`. HTTPS via certificado do GitHub Pages.

## Responsivo

Breakpoints em `≤900px` (mobile) e `901–1300px` (laptop). No mobile o menu do cabeçalho é oculto, as logos do cabeçalho e do rodapé ficam centralizadas a 190px, e todas as grades colapsam para coluna única.
