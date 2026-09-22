# Checkpoint 1 — HTML semântico

**Frontend Design · Turma 2 · Prof. Fábio Alencar**
Data: **\_22/09/2026** · Janela: **100 minutos, em sala** · Individual

---

## O que é

Uma página institucional de uma organização fictícia, feita **só com HTML**. Nada de CSS, nada de JavaScript. O tema é **sorteado pelo seu RM** no início da aula: cada pessoa recebe um briefing diferente, com o nome da organização, o que ela faz e o conteúdo que a página precisa ter.

Sem CSS, a única coisa que dá forma à página é a marcação. É isso que está sendo avaliado: se você escolheu a tag certa para cada pedaço de conteúdo, se os títulos formam uma hierarquia, se um formulário pode ser preenchido só com o teclado, se um leitor de tela consegue navegar pelo que você escreveu. Uma página "feia" no navegador não perde ponto. Uma página feita de `<div>` e `<br>`, sim.

## Seu briefing

Está em `briefings/<número>-<nome>.md`. Ele traz os fatos: serviços, diferenciais, um passo a passo, horário, endereço, contato e os campos do formulário. **O texto é seu** — os parágrafos você escreve com as suas palavras. Os dados (endereço, telefone, e-mail) podem ir como estão.

O briefing vem com uma **imagem de referência**: a página montada, para você enxergar a hierarquia — o que é título de quê, o que é lista, como o formulário se agrupa. Ela não tem nenhuma tag escrita, e não é para copiar o visual (sua página não terá CSS). O briefing diz _o que_ vai na página e a imagem mostra _como se organiza_. Nenhum dos dois diz qual tag usar. Essa decisão é a prova.

---

## O que a página precisa ter

**1. `<head>` completo**
`lang="pt-BR"` no `<html>`, `<meta charset>`, `<meta name="viewport">`, `<meta name="description">` com uma frase sobre a organização, e um `<title>` com o nome dela.

**2. Comentário de identificação**, logo depois de `<body>`, exatamente neste formato:

```html
<!-- Nome: Maria da Silva · RM: 570000 · Tema: 07 · Roda Justa -->
```

**3. `<header>`** com o nome da organização como **único `<h1>`** da página, um slogan, e um `<nav>` com **5 links âncora** (`href="#..."`) que levam para as 5 seções do `<main>`.

**4. `<main>` com 5 `<section>`**, cada uma com `id` (para a âncora funcionar) e um `<h2>`:

| Seção                                                     | O que vai nela                                                                                                                                                   |
| --------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sobre                                                     | um ou dois parágrafos de apresentação                                                                                                                            |
| Serviços / produtos / atividades (o nome vem do briefing) | **3 `<article>`**, cada um com `<h3>`, um parágrafo e uma `<img>` com `alt` descritivo                                                                           |
| Diferenciais + passo a passo                              | uma lista **não ordenada** (`ul`) com os diferenciais e uma lista **ordenada** (`ol`) com o passo a passo — e a escolha de qual é qual tem que fazer sentido     |
| Onde e quando                                             | **quatro parágrafos** — horário, endereço, telefone e e-mail — cada um começando com o rótulo em `<strong>`: `<p><strong>Horário:</strong> Segunda a sexta…</p>` |
| Contato / agendamento / pedido (o nome vem do briefing)   | o **formulário** do item 5                                                                                                                                       |

**5. `<form>`** com os campos do briefing, seguindo estas regras:

- **Dois `<fieldset>`**, cada um com `<legend>` — um para os dados da pessoa, outro para o pedido/agendamento
- **Todo campo tem `<label>`** ligado por `for`/`id`. Sem exceção: input, textarea, cada radio, o checkbox
- **Pelo menos 5 `type` diferentes de `<input>`** — o briefing pede nome, e-mail, telefone, uma data ou número, duas escolhas únicas e uma marcação; escolha o `type` que o navegador entende, não `text` para tudo
- **Dois grupos de radio**: cada grupo com o mesmo `name` em todas as opções (é isso que faz o navegador deixar marcar só uma) e um `<label>` por opção
- Um **`<textarea>`** para o campo de texto longo
- **`required`** nos campos que não podem ficar vazios (você decide quais, mas pelo menos um)
- **`<button type="submit">`** no fim. O formulário não precisa enviar para lugar nenhum — simplesmente não coloque `action` (um `action=""` vazio é erro no validator)

**6. `<footer>`** com o nome da organização, um link de e-mail (`href="mailto:..."`), um link de telefone (`href="tel:..."`) e um link externo (rede social ou mapa, pode ser inventado) que abre em nova aba.

**7. Ênfase com sentido.** Além dos rótulos da seção "Onde e quando", pelo menos um `<strong>` e um `<em>` no texto corrido, em lugares em que a ênfase muda o sentido da frase — não para "deixar em negrito".

**8. Texto coerente com o tema.** Nome, serviços e dados são os do briefing. Textos genéricos ou de outro tema valem nota de outro tema — ou seja, zero naquele critério.

### O que é proibido

- `<style>`, atributo `style=""`, `<link rel="stylesheet">` — **nenhum CSS**
- `<script>` — **nenhum JavaScript**
- `<br>` para criar espaço, `<div>` onde cabe uma tag semântica, `<b>` e `<i>` no lugar de `<strong>` e `<em>`
- Tabelas para layout
- `placeholder` no lugar de `<label>` — placeholder some quando a pessoa digita; label não
- Qualquer ferramenta de IA generativa (Copilot, ChatGPT, Claude, Gemini, IA do navegador). Desative o Copilot antes de começar.
- Comunicação entre colegas durante a janela

### O que é permitido

- VS Code com as extensões de HTML da aula 2
- MDN e o ebook das aulas
- [validator.w3.org](https://validator.w3.org/#validate_by_upload) — use, e mais de uma vez
- Imagens de placeholder (`https://picsum.photos/400/300`) ou qualquer foto livre

---

## Entrega

Um único arquivo, chamado **`index.html`**, enviado pelo **assignment do Teams** até o fim da janela. Depois disso o assignment fecha.

Não é pasta, não é zip, não é `Index.HTML`, não é `site.html`. É `index.html`.

Antes de enviar, passe pelo [`CHECKLIST.md`](CHECKLIST.md). Ele lista tudo o que o corretor confere de forma automática — os cinco itens do topo são os que mais tiraram ponto da turma passada.

---

## Avaliação

Nota de 0 a 10.

| Critério                  | O que conta                                                                                                                                                  | Pts |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | --: |
| **Estrutura semântica**   | `header`, `nav`, `main`, `section`, `article`, `footer` no lugar certo; nenhum `div` onde cabia tag semântica; aninhamento correto                           | 2,5 |
| **Formulário**            | `fieldset`/`legend`; `label` em 100% dos campos; `type` certo para cada informação; grupos de radio com `name` comum; `textarea`, `required`, botão de envio | 2,5 |
| **Hierarquia de títulos** | um único `h1`; `h2` em cada seção; `h3` nos artigos; nenhum nível pulado                                                                                     | 1,5 |
| **Conteúdo**              | `ul` e `ol` no contexto certo; dados em parágrafos rotulados; `strong`/`em` com sentido; `img` com `alt` útil; âncoras e links funcionando                   | 1,5 |
| **Head e validade**       | `lang`, charset, viewport, description, `title`; zero erros no validator                                                                                     | 1,0 |
| **Organização**           | comentário de identificação, indentação consistente, texto coerente com o tema                                                                               | 1,0 |

**Penalidades**

|                                                        |      |
| ------------------------------------------------------ | ---: |
| CSS ou JS no arquivo (o estilo é ignorado na correção) | −1,0 |
| Tema diferente do sorteado                             | −3,0 |
| Arquivo com outro nome ou dentro de pasta/zip          | −0,5 |
| Entrega fora da janela                                 |   -3 |
| Uso de IA ou cópia entre colegas                       |  -10 |

---

## O que entregar, em uma linha

Um `index.html` sem uma linha de CSS que, lido por uma pessoa cega ou por um robô de busca, conta a história inteira da organização do seu briefing e deixa qualquer um preencher o formulário só com o teclado — porque cada tag foi escolhida pelo que ela significa.
