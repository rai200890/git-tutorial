# Registrando mudanças

## Comando

```shell
git commit [-m <mensagem-descrevendo-mudanças>]
```

- Armazena uma nova versão do seu projeto no histórico do git através de um **commit**.
- Esse **commit** representa o estado corrente da sua área de staging.
- Essa ação avança o ponteiro **HEAD** para esse novo **commit**.

## O que é o **HEAD**?

- É um atalho para o último **commit** no seu **branch** corrente. 

## O que é um **branch**?

## Cria uma nova versão, abrindo o editor configurado para que a mensagem seja editada

```shell
git commit
```

- Por padrão usa o **nano**.
- Se uma mensagem não for informada esse comando falha.

## Cria uma nova versão com o conteúdo na área de staging, com uma mensagem descrevendo o que foi alterado

```shell
git commit -m "feat: Add first commit" 
```

## Fluxo de trabalho

```

[Área de trabalho] -> [Index - Área de staging] -> [Repositório local]

```

1. Modificamos arquivos na nossa área de trabalho.
2. Adicionamos todos o conteúdo passado como parâmetro do comando `git add` a área de staging, preparando-os para o próximo **commit**.
3. Registramos mudanças inclusas na área de staging ao repositório git local com o comando `git commit`.