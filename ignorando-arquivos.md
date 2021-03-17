# Ignorando arquivos

Arquivos são ignorados através da criação de um arquivo chamado `.gitignore`

## Arquivos que podem ser ignorados

- Arquivos que contém senhas
- Arquivos temporários

## Exemplo de arquivo

```
/.vscode
/_build
/cover
/deps
/doc
/.fetch
erl_crash.dump
*.ez
*.beam
/config/*.secret.exs
.elixir_ls
/**/node_modules
log/

/deploy/rendered/
/dist

/_dialyzer/
```

## Como usar

1. Crie um arquivo na raiz do seu repositório com o nome `.gitignore`
2. Edite o arquivo adicionando os arquivos e/ou diretórios ignorados
3. Adicione esse arquivo a área de staging com o comando `git add .gitignore`
4. Faça um novo **commit**  

A partir de agora todos os arquivos ou diretórios inclusos no `.gitignore` não podem mais ser adicionados à área de staging
```