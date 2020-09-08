### Documentação de como implementar o git dá forma correta em projetos.

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

or

git log -a
~~~
Mostra as alterações nos arquivos.
~~~bash
git status
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

