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
git clone https://github.com/CWISoftware/drops.git && cd drops
vagrant up
```

### Rodando o projeto

```
vagrant ssh
cd /vagrant && ./scripts/run_guest.sh
```

Acesse http://localhost:4000/drops/


## Instalando no seu ambiente local

### Dependências

- Ruby 2.2.3 (preferencialmente instalado com [rbenv](https://github.com/rbenv/rbenv))
- Bundler (`gem install bundler`)

### Instalação

```
git clone https://github.com/CWISoftware/drops.git && cd drops
bundle install
```

### Rodando o projeto

```
jekyll s
```

Acesse http://localhost:4000/drops/
