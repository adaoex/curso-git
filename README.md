Comandos Git
===========================

Principais comandos para o dia-a-dia com o Git
-------------------------
https://git-scm.com/book/pt-br/v1

```console
git init
```

```console
git status
```

```console
git log 
```

Adicionando um aquivo para ser "committed"
```console
git add <filename>
```

Adicionando todos aquivos para serem "committed"
```console
git add .
```


Commit 
```console
git commit -m "mensagem"
```

Commit adicionando todos os arquivos 'Untrackeds'
```console
git commit -a -m "mensagem"
```

Voltar um arquivo para "Untracked"
```console
git reset HEAD <filename>
```

Voltando para uma Versão específica
```console
git checkout <hashcode>
```

Volta a 'n' versões anteriores, mas deixa os arquivos em utilização
```console
git reset HEAD~n <--soft> 
```

Volta a 'n' versões anteriores, inclusive, arquivos em utilização
```console
git reset HEAD~2 <--hard> 
```

Branches (ramificações)
-------------------------

Para criar um branch e mudar para ele ao mesmo tempo
```console
git checkout -b iss53
```
OU
```console
$ git branch iss53
$ git checkout iss53
```

Merge básico
```console
$ git checkout master
$ git merge iss53
```

Remover um branch
```console
git branch -D nome-do-branch
```

Remover um branch
```console
git push origin :nome-do-branch
```

- Hooks (https://git-scm.com/book/pt-br/v1/Customizando-o-Git-Hooks-do-Git)
```console
.git/hooks/post-receive
```

Conteúdo do arquivo post-receive (exceto pasta .git)
```console
#!/bin/sh
GIT_WORK_TREE=/Caminho/do/site/para/publicacao git checkout -f
```

Permissão de execução no arquivo
```console
chmod +x  ~/.git/hooks/post-receive
```

Push e Pull
-------------------------
Enviando para servidor Remoto
```console
git push -u origin master
```

Local
```console
git push local master
```

Baixando do servidor Remoto
```console
git pull origin master
```

Merge e Rebase
-------------------------

Listar os branchs 
```console
git branch
```

```console
git merge <branch>
```

Organiza os branchs, fazendo um merge com o master
```console
git rebase <branch>
```

Pull Requests (PR) Colaborando com outros projetos
-------------------------

1. Fazer um fork do projeto (github.com)

2. Pull Requests
