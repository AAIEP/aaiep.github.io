---
title: Criar uma publicação
subtitle: Como criar um post que apareça na página de notícias?
---

# Porquê publicações?

Uma publicação, ou *post* para ser consistente na terminologia do Jekyll, é o tipo de páginas que vão criar mais vezes. Para os vários propósitos da vossa atividade, um post é o ideal:

- Querem lançar os resultados das eleições? Post.
- Querem anunciar uma nova parceria? Post.
- Querem informar os associados de uma sessão de cinema? Post.
- Querem convocar uma AGA? Post.

A ideia é ter o site a funcionar de mãos dadas com as redes sociais. Sejamos honestos, o bom aluno iepiano não irá acordar a uma segunda-feira e, no seu primeiro instinto matinal, abrir o site da AAIEP para ver as notícias. No entanto... ele muito provavelmente vai abrir o Facebook, Twitter, ou Instagram e aí poderá encontrar uma publicação da AAIEP que tem o link para esse artigo. Ninguém lê posts de redes sociais longos, portanto a ideia é a vossa equipa de comunicação criar um post no site, e partilhar o link desse post com um resumo sobre o que se trata nas redes sociais.

**Exemplo:** Anunciar os resultados de eleições.

1. Cria-se um post no site com os resultados completos e um anexo com o documento pdf oficial que a Comissão eleitoral disponibiliza.
2. Cria-se uma publicação para as redes sociais com uma mensagem curta a informar os vencedores, mete-se o link para o post do site no fim, e dá-se o trabalho por terminado. (notem que deixa de ser necessário criar imagens para cada publicação no Facebook e Twitter, visto que passam a aparecer aqueles "cartões" que vocês vêm em publicações com links).

---

# Como criar uma publicação?

Uma publicação, tal como qualquer outra página do site, consiste em **conteúdo** e **metadados**. Enquanto que o conteúdo pode ser livremente escolhido por vocês, e é o que quiserem escrito em Markdown, os metadados são o que informa o Jekyll (lembrar, este é o programa que *constrói* o site) sobre como formatar a página: título, subtítulo, autor, categoria, tópico, imagem de fundo, se a imagem de fundo é azulada (termo correto seria "escurecido conforme as normas gráficas") ou não, etc...

Devem criar um ficheiro na pasta ``_posts`` com um nome no seguinte formato: ``YYYY-MM-DD-titulo-curto-do-post.md``onde:

- ``YYYY``: ano
- ``MM``: mês
- ``DD``: dia
- ``titulo-curto-do-post``: título curto para o post (não afeta o que aparece no ecrã, mas define o link)
- ``.md``: o ficheiro deve terminar sempre com isto, para informar que é um ficheiro Markdown

Depois de criado o ficheiro, o seu conteúdo deve seguir este template:

``` yml
    ---
    layout: post

    title: "O título do post"
    subtitle: "O subtítulo do post, que aparece mais pequeno abaixo do título"
    author: "autor do artigo" (pode estar vazio, reverte automaticamente para "AAIEP")

    hero_image: link local ou URL para uma imagem que aparece no banner (se estiver vazio, reverte para a imagem pré-definida da AAIEP)
    hero_darken: true / false ("true" se quiserem a imagem azulada conforme as normas gráficas, ou "false" para a imagem não adulterada, reverte para "true" quando vazio, de modo a que a imagem de base esteja conforme as normas)
    hero_link: utilizado apenas se quiserem que o utilizador carregue num botão que o direcione para, por exemplo, um formulário
    hero_link_text: se, no anterior, colocaram algo, o botão tem que dizer algo, e é para isto que esta variável serve
    ---
```

**Exemplo prático:** Resultados eleitorais

``` yml
    ---
    layout: post

    title: "Resultados eleitorais: mandato 2024/2025"
    subtitle: "Confere aqui os resultados eleitorais da eleição de 4 de maio de 2024"
    author: "Comissão Eleitoral"

    hero_image:
    hero_darken: true
    hero_link: https://github.com/aaiep/documentos/eleicoes/2024.pdf (link inventado, mas seria assim)
    hero_link_text: "Comunicado da Comissão Eleitoral"
    ---
```

**Exemplo prático:** Sessão de cinema

``` yml
    ---
    layout: post

    title: "Sessão de Cinema, 5 de dezembro"
    subtitle: "Junta-te à AAIEP numa visualização do filme Velocidade Furiosa 43: How is this not over yet?"
    author: "Pessoa ou departamento que organizou"

    hero_image: https://image.tmdb.org/t/p/original/95MVDO5VyjbzqInMFx6P576Ds0x.jpg
    hero_darken: true
    hero_link: https://forms.google.com/inscrever-aaiep-cinema/ (link inventado, mas seria assim)
    hero_link_text: "Pré-inscrição para evento"
    ---
```

---

# Séries de posts

Apesar de não terem grande necessidade de utilizar esta função, poderá ser útil terem à mão a possibilidade de criarem "séries" de posts. Um uso futuro que vejo como possibilidade, é se quiserem criar algo como um guia de caloiro. O criador do tema deixou um [exemplo prático de como isso ficaria](http://www.csrhymes.com/bulma-clean-theme/2021/10/30/creating-a-post-series/). Esta página ensina como implementar uma "série" e é, ela própria parte de uma série que implementa as suas funcionalidades, com um menu no topo que dá link para isso mesmo.

Verão numa página do guia futura que isto é muito semelhante a "coleções" do Jekyll. A diferença é que está incluído no sistema específico dos "posts", permitindo assim que o utilizador tenha acesso rápido, à sua direita, dos posts recentes do site e, ao mesmo tempo, um menu de navegação exclusivo à série.