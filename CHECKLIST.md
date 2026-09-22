# Checklist antes de entregar

Passe por todos. Os cinco primeiros são os que mais tiraram ponto da turma passada.

## Os cinco clássicos

- [ ] A página tem **um** `<h1>`, e ele é o nome da organização
- [ ] `<html lang="pt-BR">` — não `en`, não vazio
- [ ] Tem `<meta name="description" content="...">` com uma frase de verdade
- [ ] O arquivo se chama exatamente `index.html`
- [ ] O comentário de identificação está logo depois de `<body>`, no formato do enunciado

## Head

- [ ] `<!DOCTYPE html>` na primeira linha
- [ ] `<meta charset="UTF-8">`
- [ ] `<meta name="viewport" content="width=device-width, initial-scale=1">`
- [ ] `<title>` com o nome da organização

## Estrutura

- [ ] `<header>` com `<h1>`, slogan e `<nav>`
- [ ] `<nav>` com 5 `<a href="#id">` — e cada `id` existe numa `<section>`
- [ ] `<main>` — só um
- [ ] 5 `<section>`, cada uma com `id` e `<h2>`
- [ ] 3 `<article>`, cada um com `<h3>`, `<p>` e `<img>`
- [ ] `<footer>` com `mailto:`, `tel:` e um link com `target="_blank"`
- [ ] Nenhuma `<div>` fazendo o papel de `section`, `article`, `header` ou `footer`

## Títulos

- [ ] `h1` → `h2` → `h3`, sem pular (nada de `h1` direto para `h3`)
- [ ] Nenhum título escolhido pelo tamanho — o nível vem da hierarquia, não da aparência

## Conteúdo

- [ ] `<ul>` para os diferenciais
- [ ] `<ol>` para o passo a passo
- [ ] Horário, endereço, telefone e e-mail em quatro `<p>`, cada um começando com o rótulo em `<strong>`
- [ ] Nenhum `<dl>`, nenhum `<select>` — não vimos em aula
- [ ] Todas as `<img>` têm `alt` que descreve a foto (não "imagem", não "foto1")
- [ ] Pelo menos um `<strong>` e um `<em>`, e a ênfase faz sentido lida em voz alta
- [ ] O texto é sobre o **seu** tema, escrito por você

## Formulário

- [ ] `<form>` dentro da quinta `<section>`, com `<h2>`
- [ ] 2 `<fieldset>`, cada um com `<legend>`
- [ ] Cliquei em **cada** `<label>` e o campo certo recebeu o foco — se não recebeu, o `for` não bate com o `id`
- [ ] Dois grupos de radio; em cada grupo, todas as opções têm o **mesmo** `name` — testei: marcar uma desmarca a outra
- [ ] Cada radio tem o seu próprio `<label>`, ligado pelo `for`
- [ ] Contei os `type` de `<input>`: são 5 ou mais diferentes (text, email, tel, date ou number, radio, checkbox…)
- [ ] `<textarea>` com `<label>`
- [ ] `required` em pelo menos um campo — e cliquei em enviar com ele vazio para ver o navegador reclamar
- [ ] `<button type="submit">` no fim
- [ ] Nenhum `placeholder` fazendo papel de label
- [ ] Naveguei o formulário inteiro só com Tab

## Proibidos

- [ ] Nenhum `<style>`, nenhum `style=""`, nenhum `<link rel="stylesheet">`
- [ ] Nenhum `<script>`
- [ ] Nenhum `<br>` para dar espaço, nenhum `<b>`/`<i>` no lugar de `<strong>`/`<em>`

## Validação

- [ ] Subi o arquivo em [validator.w3.org](https://validator.w3.org/#validate_by_upload) e deu **zero erros** (warnings podem ficar)
- [ ] Abri no navegador e cliquei nos 5 links do menu — todos rolam para a seção certa
- [ ] Indentação consistente: cada filho um nível para dentro do pai
