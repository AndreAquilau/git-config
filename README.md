### Documentação de como configrurar o git em seus projetos.

#### CLI básico git.
Iniciando repositório com git.
~~~bash
git init
~~~
Adicionar arquivos que seram manitorados.
~~~bash
git add --all -> add all files.

git add name-file -> add single file.
~~~
Adicionar alteração feita nos arquivos.
~~~bash
git commit -m 'commentary'
~~~

#### CLI logs and Status
logs dos commits feitos.
~~~bash
git log

git log --oneline -> mostra apenas uma linha.

or

git log -a
~~~
Mostra as alterações nos arquivos.
~~~bash
git status

git status -s ->mostra de forma resumida
~~~

#### CLI git config
Verificar configurações do git.
~~~bash
git config --list -> lista todas configurações do git
~~~

#### Nível de configuração do git
O git possui três níveis de configurações, primeiro nível "--system" que é a configuração para qualquer usuário na quele computador, o segundo nível "--global" que é a configuração do seu usuário para qualquer projeto, é o terceiro nível "--local" que são as configurações apenas do projeto que está sendo feito.
~~~bash
git config --system -> todos usuários.

git config --global -> apenas o usuário que esá logado.

git config --local -> apenas para o projeto.
~~~

#### Editando configurações do git
Para alteramos algum nível de configuração do git devemos utilizar a flag "--edit".
~~~
git config --global --edit
~~~
.gitconfig
~~~
[core]
	editor = \"C:\\Users\\Andre\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" --wait
[user]
	name = Andre Aquilau
	email = Andre.Aquilau@outlook.com
[filter "lfs"]
	clean = git-lfs clean -- %f
	smudge = git-lfs smudge -- %f
	process = git-lfs filter-process
	required = true
[code]
	editor = code --wait //add --wait faz com que o vscode espera carregar os comondos do git.
~~~
#### Criando apelidos -> alias
alias = !commond
~~~
[alias]
	s = !git status -s
	c = !git add --all && git commit -m
	l = !git log --oneline -> mostras as informações em apenas uma linha
	lp = !git log --pretty=format:'%C(blue)%h %C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
~~~

#### Formatando CLI git log.
Pra formatarmos o CLI do git temos que usar o --pretty=format:'' utilizamos no final da linha.
##### flags
~~~
%C(color) -> definimos a cor da linha inteira.

%C(blue)%h -> definimos a cor da coluna.

%cn -> commit name, variável que retorna o nome da pessoa que fez o commit.

%cr -> commit relative date, retorna a data relativa do commit.

%H -> mosta a hash do commit.

%h -> mostra a hash reduzida do commit.

%d -> mostra a branch que está sendo usada.

%s -> subject, mostra a mensagem do commit.
~~~

[PRETTY FORMATS](https://git-scm.com/docs/pretty-formats)


