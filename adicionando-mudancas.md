# Adicionando mudanças

## Como funciona

Cada arquivo no sua área de trabalho pode estar em 2 estados

- **tracked**: arquivos que estavam na última versão salva ou que já foram selecionados para irem na próxima versão(staged), adicionando-os a área de staging. Em resumo aqueles que o git já sabe que existem e acompanha mudanças
- **untracked**: arquivos na sua área de trabalho que ainda não foram submetidos para a próxima versão, isto é, são arquivos que ainda não estão no index. 

## Sintaxe

- Adiciona arquivo na sua área de trabalho a área de staging(ou index), preparando-o para ser enviados na próxima versão.
- Arquivos ignorados não vão ser inclusos por esse comando por padrão.

### O que é a área de staging?

- Conhecida como **index**, armazena uma 'fotografia' do conteúdo do seu projeto. Essa 'fotografia' que vai ser usada como conteúdo do seu próximo **commit**.

```shell
git add <arquivo-ou-diretório>
```

### Adiciona arquivo na sua área de trabalho à área de staging

```shell
git add farofa.md 
```

### Adiciona todos os arquivos com extensão .md à área de staging

```shell
git add *.md 
```

### Adiciona todas os arquivos no diretório corrente à área de staging

```shell
git add . 
```

## Fluxo de trabalho

```

[Área de trabalho] -> [Index - Área de staging]

``` 