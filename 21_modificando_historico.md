# Modificando histórico

- Uma commit no repositório local pode ser alterado  
- Uma commit já sincronizado no repositório remoto pode ser alterado.
- Esse tipo de mudança tem que ser feita com cuidado pois pode ocasionar perda de código.

## Modificando último commit

```shell
git commit --amend
```

É possível adicionar mudanças na área de staging ao **último** commit existente e editar sua mensage,.
O commit antigo desaparecerá e será subtituido por um novo **commit**, com uma nova referência.

## Modificando commits na branch corrente

```shell
git rebase -i HEAD~5
```

Permite remover(delete), juntar(squash) e renomear mensagens(reword) referentes aos últimos 5 commit antes do ponteiro HEAD.

### Exemplo:

```
pick 97268476 chore: bump newrelic and phoenix versions (#1013)
pick d7e4eade refactor: add request_id to kafka events (#1014)
pick a2f65ea8 chore: Bump version (#1015)
pick 8eb1529e feat: cache cip consults (#995)
pick 9fd2832b fix: hml config (#1016)

# Rebase bda5b6c0..9fd2832b onto 8eb1529e (5 commands)
#
# Commands:
# p, pick <commit> = use commit
# r, reword <commit> = use commit, but edit the commit message
# e, edit <commit> = use commit, but stop for amending
# s, squash <commit> = use commit, but meld into previous commit
# f, fixup <commit> = like "squash", but discard this commit's log message
# x, exec <command> = run command (the rest of the line) using shell
# b, break = stop here (continue rebase later with 'git rebase --continue')
# d, drop <commit> = remove commit
# l, label <label> = label current HEAD with a name
# t, reset <label> = reset HEAD to a label
# m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
# .       create a merge commit using the original merge commit's
# .       message (or the oneline, if no original merge commit was
# .       specified). Use -c <commit> to reword the commit message.
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out
```

Pode ser que exista um conflito derivado dessas alterações que pode ser revertido com `git rebase --abort` e depois de resolvido, aplicado com `git rebase --continue`