# Removendo mudanças

## Comando

```shell
git rm <arquivo-ou-diretorio>
```

- Remove arquivos da área de trabalho e da área de staging

## Remove arquivo da área de trabalho e da área de staging, e para de acompanhar mudanças no mesmo

```shell
git rm farofa
```

O arquivo farofa precisa existir no repositório local

equivalente a:

```shell
rm farofa
git add farofa
```

## Remove arquivo somente da área de staging, mantendo-o na sua área da trabalho

```shell
git rm farofa --staged 
```
