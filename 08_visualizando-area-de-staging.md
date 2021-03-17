# Visualizando área de staging

## Visualiza diferença entre área de staging e área de trabalho

```shell
git status
```

- Comando usado para obter um resumo dos arquivos que foram modificados e que já estão na área de staging, prontos para serem inclusos no próximo **commit**.

### Exemplo

```
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   11_desfazendo_mudancas.md
	renamed:    11_registrando-mudancas.md -> 12_registrando-mudancas.md
	renamed:    12_visualizando-mudancas.md -> 18_visualizando-mudancas.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   08_visualizando-area-de-staging.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	hello.txt
```

## Visualiza diferença de conteúdo entre arquivos

```shell
git diff
```

- Comando usado para visualizar mudanças de arquivos entre commits e/ou área de staging 

```

```