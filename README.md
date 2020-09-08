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

