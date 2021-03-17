# Enviando mudanças para repositório remoto

## Envia commits na sua área de trabalho para o repositório remoto

```shell
git push 
```

## Envia mudanças para o repositório remoto para um branch de mesmo nome do que localmente

```shell
git push origin master
```

## Envia mudanças para o repositório remoto para um branch de mesmo nome do que localmente, configurando o **upstream**

**Upstream** é o branch no repositório remoto que vai estar sincronizado com o branch no repositório local.

```shell
git push -u origin master
```

## Envia e sobrescreve obrigatoriamente mudanças no seu repositório remoto

Use esse comando com cautela pois você pode perder mudanças no repositório remoto  

```shell
git push -f 
```

#### Fluxo de trabalho

```

[Área de trabalho] -> [Index - Área de staging] -> [Repositório Local] -> [Repositório remoto] 

```

1. Modificamos arquivos na nossa área de trabalho.
2. Adicionamos todos o conteúdo passado como parâmetro do comando `git add` a área de staging, preparando-os para o próximo **commit**.
3. Faz um **commit** com as mudanças adicionadas a área de staging com o comando `git commit`
4. Envia **commits** no repositório local para o repositório remoto com o comando `git push`