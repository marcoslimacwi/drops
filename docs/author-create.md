# Criar autor

Você só precisa de um nome de usuário e gerar alguns arquivos com suas informações.

O nome de usuario deve ser um nome de usuário como o que você usa normalmente em algum serviço: começando por letras, sem espaços, etc. De preferência use o mesmo nome de usuário da CWI ou do seu email pessoal (sem @ etc).

Existem 2 formas de criar o usuário:

1. usando um gerador (**recomendado**)
1. manualmente

## Com gerador (`rake`)

```sh
rake author <usuario>
```


## Manualmente

Criar os arquivos `autores/<usuario>.md` e `_data/authors/<usuario>.yml` e preencher, usando o arquivo de algum outro autor como modelo.
