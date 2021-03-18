# Gerando chave SSH

Esse tutorial ensinará a gerar uma chave ssh e cadastrá-la no [Github](http://github.com)

1. Crie uma conta do [Github](https://github.com/join)
2. Na sua máquina local verifique se alguma chave ssh já existe com o seguinte comando:

```shell
ls -al ~/.ssh
```

3. Gere uma nova chave com o seguinte comando usando o email cadastrado do Github:

```shell
ssh-keygen -t ed25519 -C "email@email.com"
```

ou se o comando anterior não funcionar:

```shell
ssh-keygen -t rsa -b 4096 -C "email@email.com"
```

4. Adicione uma senha para a sua chave,

5.  Inicie o ssh-agent

```shell
eval "$(ssh-agent -s)"
```

6. Adicione a sua chave **privada** ao ssh agent:

```shell
ssh-add ~/.ssh/id_ed25519
```

7. Copie a sua chave **pública**: 

```shell
sudo apt-get install xclip # instala o xclip para copiar via linha de comando

xclip -selection clipboard < ~/.ssh/id_ed25519.pub # copia chave pública
```

8. Acesse as [configurações de chave SSH do Github](https://github.com/settings/keys)

9. Crie uma [nova entrada usando a chave copiada](https://github.com/settings/ssh/new)