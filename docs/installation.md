Instalação
----------

Existem 2 formas de instalar o ambiente de desenvolvimento:

1. usando Vagrant (recomendado, especialmente para Windows)
1. usando seu ambiente local


## Instalando com Vagrant

### Dependências

- Vagrant
- VirtualBox

### Instalação

```
git clone https://github.com/CWISoftware/blog.git && cd blog
vagrant up
```

### Rodando o projeto

```
vagrant ssh
cd /vagrant && ./scripts/run_guest.sh
```

Acesse http://0.0.0.0:4000/blog/


## Instalando no seu ambiente local

### Dependências

- Ruby 2.2.3 (preferencialmente instalado com [rbenv](https://github.com/rbenv/rbenv))
- Bundler (`gem install bundler`)

### Instalação

```
git clone https://github.com/CWISoftware/blog.git && cd blog
bundle install
```

### Rodando o projeto

```
./scripts/run_host.sh
```

ou

```
jekyll s
```

Acesse http://0.0.0.0:4000/blog/
