Comandos Git
===========================

Principais comandos para o dia-a-dia com o Git
-------------------------
https://git-scm.com/book/pt-br/v1

```
git init
```

```
git status
```

```
git log 
```

Adicionando um aquivo para ser "committed"
```
git add <filename>
```

Adicionando todos aquivos para serem "committed"
```
git add .
```


Commit 
```
git commit -m "mensagem"
```

Commit adicionando todos os arquivos 'Untrackeds'
```
git commit -a -m "mensagem"
```

Voltar um arquivo para "Untracked"
```
git reset HEAD <filename>
```

Voltando para uma Versão específica
```
git checkout <hashcode>
```

Volta a 'n' versões anteriores, mas deixa os arquivos em utilização
```
git reset HEAD~n <--soft> 
```

Volta a 'n' versões anteriores, inclusive, arquivos em utilização
```
git reset HEAD~2 <--hard> 
```

Branches (ramificações)
-------------------------

Para criar um branch e mudar para ele ao mesmo tempo
```sh
git checkout -b iss53
```
OU
```sh
$ git branch iss53
$ git checkout iss53
```

Merge básico
```sh
$ git checkout master
$ git merge iss53
```


- Hooks (https://git-scm.com/book/pt-br/v1/Customizando-o-Git-Hooks-do-Git)
```
.git/hooks/post-receive
```

Conteúdo do arquivo post-receive (exceto pasta .git)
```
#!/bin/sh
GIT_WORK_TREE=/Caminho/do/site/para/publicacao git checkout -f
```

Permissão de execução no arquivo
```
chmod +x  ~/.git/hooks/post-receive
```

Push ()
-------------------------
Remoto
```
git push -u origin master
```

Local
```
git push local master
```

Merge e Rebase
-------------------------

-- listar os branchs 
git branch

git merge <branch>

-- organiza os branchs, fazendo um merge com o master
git rebase <branch>
