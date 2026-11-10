# [AT04] HTML semântico — Meu Mundo Roblox

- **Estudante:** Theo Lorentz Padilha
- **Turma:** DSM3-2025
- **Unidade curricular:** Programação de Aplicativos
- **Tema escolhido:** Roblox

## Sobre o site

O Meu Mundo Roblox é um site de cinco páginas sobre a plataforma Roblox: como ela funciona, como criar experiências no Roblox Studio e como participar de um campeonato de construção. O site não tem CSS nem JavaScript de propósito, porque o foco da atividade é a estrutura HTML, a semântica e a acessibilidade.

## Como abrir o projeto

1. Baixe ou clone o repositório.
2. Abra o arquivo `index.html` no navegador (duplo clique ou "Abrir com").
3. Use o menu no topo para navegar entre as páginas.

## Páginas

| Arquivo | O que tem |
|---|---|
| `index.html` | Início: apresenta o tema, listas, imagens e convida a navegar |
| `sobre.html` | Sobre: sumário, artigos, curiosidades, glossário e fontes externas |
| `dados.html` | Dados: tabela de protótipos com total e média no rodapé |
| `cadastro.html` | Cadastro: formulário de inscrição no campeonato com validação nativa |
| `contato.html` | Contato: endereço fictício, horário e formulário de mensagem |

## Acessibilidade

Recursos aplicados:

- idioma `pt-BR` declarado e `alt` descritivo em todas as imagens informativas (a decorativa tem `alt` vazio);
- link "Pular para o conteúdo" como primeiro elemento do `<body>` de todas as páginas;
- `aria-current="page"` no menu e `aria-label` nos `<nav>`;
- títulos em ordem, sem pular nível;
- todos os campos de formulário com `<label for>` e `<fieldset>` com `<legend>` nos grupos;
- tabela com `<caption>` e células de cabeçalho com `scope`.

### Resultados das verificações

- **Validador do W3C (Nu Html Checker):** as cinco páginas com 0 erros e 0 avisos.
- **Lighthouse, categoria Acessibilidade:** `index` 95, `sobre` 95, `dados` 95, `cadastro` 95 e `contato` 96.
  - Único item apontado em todas as páginas: *Touch targets do not have sufficient size or spacing* (`target-size`), nos links do menu. Ele só pode ser resolvido com CSS (aumentar a área de clique dos links), e o enunciado proíbe CSS nesta atividade. Fica registrado como pendência para quando o estilo for aplicado.
- **Teste de teclado (só com a tecla Tab):** em todas as páginas o primeiro foco vai para "Pular para o conteúdo", depois passa pelo menu na ordem Início, Sobre, Dados, Cadastro e Contato, e segue pelos links e campos do conteúdo, sem armadilha de foco. No Cadastro, a ordem é nome, e-mail, telefone, data, categoria, nível, horas, nota, modos de jogo, mensagem, aceite e os botões de enviar e limpar. Todos os campos são alcançáveis e preenchíveis pelo teclado.

## Decisões de semântica

- `<section>` para cada bloco temático com título próprio (por exemplo, "Como a plataforma funciona" e "Glossário").
- `<article>` para os dois textos "Jogando" e "Criando" da página Sobre, porque cada um faz sentido sozinho.
- `<aside>` para o "Você sabia?", que é um complemento ao texto principal.
- `<dl>` para o glossário e para o horário de atendimento, porque são pares termo/descrição.
- `<address>` para as informações de contato do responsável pelo site.

## Fontes consultadas

- Referência de HTML: [MDN Web Docs](https://developer.mozilla.org/pt-BR/), [W3Schools](https://www.w3schools.com/html/) e [HTML Standard (WHATWG)](https://html.spec.whatwg.org/).
- Validação: [Nu Html Checker](https://validator.w3.org/nu/).
- Conteúdo sobre o tema: [Documentação do Roblox para criadores](https://create.roblox.com/docs) e [Roblox na Wikipédia](https://pt.wikipedia.org/wiki/Roblox).

## Imagens

| Arquivo | Fonte e licença |
|---|---|
| `img/blocos-construcao.svg` | Autoria própria (desenhada em SVG) |
| `img/mapa-obby.svg` | Autoria própria (desenhada em SVG) |
| `img/divisor-blocos.svg` | Autoria própria (desenhada em SVG) |

Todas pesam bem menos de 300 KB. Os dados da tabela, o endereço, o e-mail e o telefone são fictícios.
