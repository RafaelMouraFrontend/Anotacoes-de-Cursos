# Lista de comnandos Git

Este é o arquivo com comandos, do curso básico de git e github do Willian Justen

**São apenas anotações como forma de lembrete:**

git init

git status

git log

git log --graph --mostra o gráfico de commits

git diff

git add (nome do arquivo)

git checkout (nome do arquivo)--- pra voltar o arquivo quando ele ainda não está em staged

git reset HEAD (nome do arquivo) --- volta com o arquivo que já está em staged

git reset --soft --volta o arquivo commitado pra staged

git reset --mixed -- volta o arquivo antes do staged apenas modify

git reset --hard -- ignora totalmente a  existencia do commit

git commit -m 'mensagem que fala sobre o commit'

git am "add com o commit"

g clone (endereço repositório) (nome da pasta)


**Depois de criar o repositório no github**

git remote add origin https://github.com/RafaelMouraFrontend/courseWllianGit.git

git push -u origin master ----> primeiro envio

git push origin master ---> enviando para o gitgub

**O fork serve para fazer colaboração em outros projetos**

Você vai estar fazendo uma copia do repositorio e depois vai subir as alterações

**Branch**

git checkout -b 'testing' -- cria

git checkout -- muda de branch

git branch -- existentes e qual Você está

git -D testing -- apaga a branch

git merge <nome da branch>  -- mescla as camadas criando um novo commit

git rebase <nome da branch> -- joga a branch pra frente

.gitignore -- se trata do arquivo com oq vai ser ignorado quando subir par ao github

git stash -- guarda sem dar o commits

git tag -a 1.0.0  -m "mensagem da tag" -- cria a staged

git push origin master --tags -- sobe as tags

git push origin: (nome da branch)-- apaga branch remota
