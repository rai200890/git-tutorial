## Desfazendo mudanças

## Removendo commits 

```shell
git reset --soft HEAD~2
```

Remove últimos 2 commits em relação ao HEAD e mantém mudanças na área de staging


```shell
git reset --hard HEAD~2
```

Remove últimos 2 commits em relação ao HEAD descartando as mudanças introduzidas pelos mesmos

## Revertendo commits 

```shell
git revert 9fd2832b3ef3f8e7468f2e5f968f191681e47c0b
```

Reverte as mudanças feitas no **commit** **9fd2832b3ef3f8e7468f2e5f968f191681e47c0b** adicionando um novo commit no repositório local

## Diferença enre reset, restore e revert
        
- `git revert` - cria um novo commit desfazendo mudanças feitas por outros commits

- `git restore` - restaura arquivos a partir da área de staging ou outro commit. Não atualiza o branch corrente.
       
- `git reset` - atualiza seu branch, move o **head** para adicionar ou remover commits, alterando seu histórico. Também é possível restaurar arquivos da sua área de staging, cumprindo a mesma função que o `git restore`