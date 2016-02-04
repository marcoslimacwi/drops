# Criar post

Um post é um arquivo dentro da pasta _posts. Os arquivos tem um trecho inicial semelhante a esse:

```yml
---
layout: post
title:  "Nome do meu post"
date:   2016-01-15 09:16:35 -0200
abstract: >
  Um resumo de umas 2 ou 3 linhas do meu post.
---
```

Esse trecho se chama *front matter*. Não apague o *front matter*, apenas altere com os dados do seu post.

Cada post deve resultar em um **pull request** no repositório do Drops no GitHub, para que seja revisado e aprovado pela equipe do Drops. **Não faça commit do seu post diretamente na branch master**.

Existem 2 formas de criar o post:

1. usando um gerador (**recomendado**)
1. manualmente


## Com gerador (`octopress`)

```sh
octopress new post 'Nome do post'
```


## Manualmente

Criar o arquivo na pasta _posts, seguindo **rigorosamente** o padrão de nome e data dos demais posts.
