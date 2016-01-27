[Drops CWI](http://cwisoftware.github.io/drops/)
--------

[![Build Status](https://api.travis-ci.org/CWISoftware/blog.svg?branch=gh-pages)](https://travis-ci.org/CWISoftware/blog)

# Work in progress


## Ambiente

- [Instalação](/docs/installation.md)


## Criar autor

Todos colaboradores da CWI podem escrever no blog! Você só precisa de um nome de usuário e gerar alguns arquivos com suas informações.

```sh
rake author <usuario>
```

Ou manualmente, criar os arquivos `autores/<usuario>.md` e `_data/authors/<usuario>.yml` e preencher conforme os demais.


## Criar post

```sh
octopress new post 'Nome do post'
```
