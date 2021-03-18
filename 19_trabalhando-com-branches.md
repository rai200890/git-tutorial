# Trabalhando com branches

Com o objetivo de isolar trabalho em repositórios com mais de um desenvolvedor, podemos criar **branches**.

Uma **branch** é um atalho móvel para um **commit**.

Esse isolamento permite que várias pessoas sigam o desenvolvimento de features isolamente, sem conflitos entre si.

Isso pode ajudar a garantir que a versão na master é a mais estável por exemplo.

Exemplo:

```
                    A---B---C branch_a
                    /
               D---E  master
                    \                  
                     H---------I branch_b 
```


## Criando uma branch

```shell
git branch branch_a
```
## Acessando uma branch

```shell
git checkout branch_a
```

É possível fazer checkout de **branches**, **tags** e até mesmo **commits** específicos.

## Criando e acessando uma branch

```shell
git checkout -b branch_a
```

## Visualizando branches

```shell
git branch
```

A branch corrente começa com um (*)

## Removendo uma branch que ainda já foi integrada ao repositório remoto

```shell
git branch -d branch_a
```

## Removendo uma branch que ainda não integrada ao repositório remoto

```shell
git branch -D branch_a
```

## Removendo uma branch do repositório remoto

```shell
git branch --delete origin :branch_a
```

Cuidado pois ela não estará mais acessível no repositório remoto. Alguma outra pessoa pode querer fazer checkout dessa branch.

## Integra a branch master com na branch corrente

```shell
git merge master
```

## Integrando uma branch na outra

Integra a branch_a na branch corrente

```shell
git merge branch_a
```

### Integrando branches

1. Projeto com 3 branches:

- branch_a 
- branch_b
- master(branch padrão)

```
                    A---B---C branch_a
                    /
               D---E  master
                    \                  
                     H---------I branch_b 
```

2. Projeto após a o merge da branch_a na master:

```
                    A---B---C 
                    /        \
               D---E --------J master 
                    \                  
                     H---------I branch_b 
```


3. Projeto após o merge da branch_b na master:

```
                    A---B---C 
                    /        \
               D---E --------J---K master
                    \           /                
                     H---------I
```
