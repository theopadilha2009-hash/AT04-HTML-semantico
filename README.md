# [AT04] HTML semântico — Mundo Startup

- **Estudante:** Theo Lorentz Padilha
- **Turma:** DSM3-2025
- **Unidade curricular:** Programação de Aplicativos
- **Tema escolhido:** Startups

## Sobre o site

O Mundo Startup é um site de cinco páginas que explica o que são startups, como uma ideia vira empresa e como participar de um Demo Day escolar, evento em que os alunos apresentam ideias de startup. O site não tem CSS nem JavaScript de propósito, porque o foco da atividade é a estrutura HTML, a semântica e a acessibilidade.

> O projeto começou com o tema Roblox e mudou para startups. A troca aparece no histórico de commits (PRs #10 a #14).

## Como abrir o projeto

1. Baixe ou clone o repositório.
2. Abra o arquivo `index.html` no navegador (duplo clique ou "Abrir com").
3. Use o menu no topo para navegar entre as páginas.

## Páginas

| Arquivo | O que tem |
|---|---|
| `index.html` | Início: apresenta o tema, listas, imagens e convida a navegar |
| `sobre.html` | Sobre: sumário, artigos, curiosidade, glossário e fontes externas |
| `dados.html` | Dados: tabela de startups fictícias com total e média no rodapé |
| `cadastro.html` | Cadastro: formulário de inscrição no Demo Day com validação nativa |
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
- **Teste de teclado (só com a tecla Tab):** executado de forma automatizada, simulando a tecla Tab no Chrome. Em todas as páginas o primeiro foco vai para "Pular para o conteúdo", depois passa pelo menu na ordem Início, Sobre, Dados, Cadastro e Contato, e segue pelos links e campos do conteúdo, sem armadilha de foco. No Cadastro, a ordem é nome, e-mail, telefone, data, área da ideia, estágio, horas, nota de confiança, ajuda que preciso, descrição da ideia, aceite e os botões de enviar e limpar. Todos os campos são alcançáveis pelo teclado.

## Decisões de semântica

- `<section>` para cada bloco temático com título próprio (por exemplo, "Como uma startup funciona" e "Glossário").
- `<article>` para os dois textos "Testando a ideia" e "Conseguindo dinheiro" da página Sobre, porque cada um faz sentido sozinho.
- `<aside>` para o "Você sabia?", que é um complemento ao texto principal.
- `<dl>` para o glossário e para o horário de atendimento, porque são pares termo/descrição.
- `<address>` para as informações de contato do responsável pelo site.

## Dificuldades encontradas e como foram resolvidas

- **Troca de tema:** o site começou sobre Roblox e foi trocado por startups. Como a estrutura já estava validada, só os textos, as imagens e a tabela foram reescritos, uma página por vez, mantendo todos os requisitos de cada etapa.
- **Dados da tabela:** não foi possível confirmar datas de fundação de empresas reais em uma fonte confiável, então a tabela usa startups fictícias, avisadas na própria página, com total e média conferidos por cálculo.
- **`<br>` no endereço:** a regra proíbe `<br>` para criar espaço. Mesmo sendo um uso válido no endereço, cada linha virou um parágrafo dentro do `<address>` para não deixar dúvida.
- **Link do menu pequeno no Lighthouse:** o item `target-size` só se resolve com CSS, que a atividade proíbe. Ficou registrado como pendência para a fase de estilo.
- **Validação do formulário vazio:** o balão de erro do navegador não aparece em captura de tela automática comum, então a evidência foi feita com o Chrome aberto de verdade.

## Fontes consultadas

- Referência de HTML: [MDN Web Docs](https://developer.mozilla.org/pt-BR/), [W3Schools](https://www.w3schools.com/html/) e [HTML Standard (WHATWG)](https://html.spec.whatwg.org/).
- Validação: [Nu Html Checker](https://validator.w3.org/nu/).
- Conteúdo sobre o tema: [Startup na Wikipédia](https://pt.wikipedia.org/wiki/Startup) e [Lista dos unicórnios brasileiros, do Distrito](https://www.distrito.me/blog/lista-dos-unicornios-brasileiros).

## Imagens

| Arquivo | Fonte e licença |
|---|---|
| `img/equipe-startup.svg` | Autoria própria (desenhada em SVG) |
| `img/grafico-crescimento.svg` | Autoria própria (desenhada em SVG) |
| `img/divisor-foguete.svg` | Autoria própria (desenhada em SVG) |

Todas pesam bem menos de 300 KB. Os nomes das startups, os números da tabela, o endereço, o e-mail e o telefone são fictícios.
