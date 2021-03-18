# Trabalhando com tags

## O que é uma tag?

Um elemento que marca um commit no histórico do seu repositório.

## Para que serve?

Serve para identificar versões relevantes do seu projeto, como por exemplo versões estáveis do seu software.

## Criando uma tag no repositório local

```shell
git tag v1.0.0 -m "First stable version"
```

## Enviando tags para repositório remoto

```shell
git push origin --tags
```

Por padrão(sem a flag --tags) esse comando não envia tags para o reposiório remoto.

## Deletando uma tag do repositório local

```shell
git tag -d v1.0.0
```

## Deletando uma tag do repositório remoto

```shell
git push origin :v1.0.0
```
