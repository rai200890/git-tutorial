# Resolvendo os conflitos

## Exemplo de arquivo em conflito

### Arquivo em conflito

### Arquivo no repositório local

```html
<html>
  <head>
  </head>
  <body>
    <h1>Hi!</h1>
  </body>
</html>
```

### Arquivo no repositório remoto

```html
<html>
  <head>
  </head>
  <body>
    <h1>Hello!</h1>
  </body>
</html>
```

```html
<html>
  <head>
  </head>
  <body>
<<<<<<< HEAD
    <h1>Hi!</h1>
=======
    <h1>Hello!</h1>
>>>>>>> master
  </body>
</html>
```

## Resolvendo conflito passo a passo

1. Para resolver essa situação armazene as suas mudanças localmente usando os seguintes comandos:

```shell
git add . # adiciona os arquivos desejados
git stash # armazene as mudanças na área de stash
```

Podemos ver o que está em nossa área de staging com o comando:

```shell
git status
```

2. Incorpora mudanças do repositório remoto no local

```shell
git pull # incorpora mudanças no branch no repositório local
git stash pop # aplica última mudanças armazenadas na área de stash no repositório local

3. Edite o arquivo resolvendo o conflto

```html
<html>
  <head>
  </head>
  <body>
    <h1>Hi!</h1>
  </body>
</html>
```

4. Registre mudança no repositório local

```shell
git add .
git commit
```

5. Envie mudança para o repositório remoto

```shell
git push origin master # envia commits para o repositório remoto
```