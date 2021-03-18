# Incorporando mudanças

## Baixa commits do repositório remoto origin para o repositório local, incorporando no repositório local na branch padrão

```shell
git pull 
```

## Baixa commits do repositório remoto origin para o repositório local, incorporando no repositório local na branch **master**

```shell
git pull origin master 
```

equivalente a:

```shell
git fetch origin master
git merge origin/master
```

### Como funciona

Antes do pull:

```
                    A---B---C master on origin
                    /
               D---E---F---G master
                   ^
                   origin/master
```

Última versão no repositório local(head): G

Última versão no repositório remoto(head): C

Depois do pull:

```
                    A---B---C origin/master
                    /         \
               D---E---F---G---H master
```

O commit H é resultando do merge

Se existir mudanças não comitadas no repositório local, o merge é cancelado automaticamente.
Se um mesmo arquivo for modificado em ambos os repositórios, pode acontecer um **conflito**.
