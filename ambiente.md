Criar ambiente de Trabalho
======================
Criar ambiente de trabalho no Ubuntu Linux e Windows.

----------

[TOC]


Webserver
-------------

Junto com **Apache** Webserver instalaremos o **PHP** e **MySQL**. Em Linux o pacote LAMP[^LAMP] e no Windows pacotes como [EasyPHP](http://www.easyphp.org/) e [WAMP](http://www.wampserver.com/en/).

> **Nota:**
>  No Windows os pacotes costumam conter o [phpMyAdmin](https://www.phpmyadmin.net/)[^phpMyAdmin].

### Linux (Ubuntu)

```sh
$ sudo apt-get install -y lamp-server^
```

#### Adicionar usuário no grupo www-data[^www-data]

```sh
$ sudo usermod -a -G www-data username
```

> **Nota:**
> Substitua ```username``` por seu nome do usuário.

#### phpMyAdmin

```sh
$ sudo apt-get install -y phpmyadmin
```

GIT
-------------

[Git](https://git-scm.com/) é um sistema de controle de versão distribuído, projetado para manipular de pequenos à grandes projetos com velocidade e eficiência.

Git é fácil de aprender e possui objetivo claro com performance rápida como um relâmpago. Ele supera ferramentas de SCM[^SCM] como Subversion, CVS, Perforce, and ClearCase com recursos como ramificação local curta, convenientes áreas de preparação, e vários fluxos de trabalho.

Aprenda Git em seu navegador gratuitamente com [Try Git](http://try.github.com/).

Gerar chave SSH
-------------------

Excute no terminar do Linux ou no Windows no bash[^bash] do Git.

```sh
$ ssh-keygen -t rsa

# OU com e-mail
$ ssh-keygen -t rsa -C "username@domain"
```
// TODO instruir processo prompt

> **Nota:**
> Substitua ```username@domain``` por seu nome e-mail.

Visualizar chave criada.

```sh
$ cat ~/.ssh/id_rsa.pub
```

> **Notas:**
>
>  * Adicione essa chave no repositório online de Git (como [Bitbucket](https://bitbucket.org/), [GitHub](https://github.com/), [Git](https://about.gitlab.com/)). Assim será possível comunicar-se (clonar, sincronizar, etc) com o repositório origem sem 'https' ou usuário e senha.
>  * Adicione essa chave no nas permitidas do servidor de hospedagem () para que não seja necessário nem usuário ou senha para conexões SSH.

Utilidades Linux (Ubuntu)
------------------------------

### Alterar permissões

Acesse no terminal a pasta.

**Exemplo:**
```sh
$ cd ~/git
```

#### Nível de acesso

```sh
# para diretórios

$ find -type d -print0 | xargs -0 chmod 755
## com permissão
$ find -type d -print0 | sudo xargs -0 chmod 755

# para arquivos

$ find -type f -print0 | xargs -0 chmod 644
## com permissão
$ find -type f -print0 | sudo xargs -0 chmod 644
```

#### Usuário e grupo proprietário

```sh
$ sudo chown www-data:www-data ~/git/*
```

// TODO Organizar comandos
### Outros
```sh
$ sudo apt-get install -y build-essential
$ sudo apt-get install -y freetds-bin php5-sybase php5-mssql
```
// TODO Node
```sh
$ curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
$ sudo apt-get install -y nodejs
$ sudo apt-get install -y npm
```
// TODO Grunt
```sh
$ sudo npm install -g grunt-cli
```
// TODO Bower
```sh
$ sudo npm install -g bower
```
// TODO Git
```sh
$ git config --global user.name "Nome Sobrenome"
```
```sh
$ git config --global user.email username@domain
```


[^LAMP]: LAMP são as inicias para Linux, Apache Server, MySQL e PHP.

[^phpMyAdmin]: Administrador de MySQL através do navegador.

[^www-data]: Grupo de usuário do Apache Webserver.

[^SCM]: Do inglês Source Control Management, algo como 'Gestor de controle de código fonte'

[^bash]: Bash é um porte (como uma cópia) para Windows de um terminal Linux. Como um 'cmd' que aceita o padrão de comandos do Linux.

**Navegadores**

1. [Google Chrome](https://www.google.com.br/chrome/browser/desktop/)

**Editor de código**

1. [Brackets](http://brackets.io/)

**Git**

[https://git-scm.com/download/win](https://git-scm.com/download/win)

**Node.js**

[https://nodejs.org/](https://nodejs.org/en/)

`
npm install grunt-cli -g

**Grunt**

[http://gruntjs.com/](http://gruntjs.com/)

`
npm install -g grunt-cli
`

**Bower**

[http://bower.io/](http://bower.io/)

`
npm install -g bower
`

**Ruby Sass**

[http://rubyinstaller.org/downloads/](http://rubyinstaller.org/downloads/)

`
set PATH=C:\Ruby22-x64\bin;%PATH%
`

`
gem install sass
`


[**Putty**](http://the.earth.li/~sgtatham/putty/latest/x86/putty.exe)

**Web Server**

[EasyPHP](http://www.easyphp.org/)

Instale o [Visual C++ Redistributable for Visual Studio 2012 Update 4](http://www.microsoft.com/en-us/download/details.aspx?id=30679) x32 antes de executar.

Edite a configuração do PHP, descomentando a linha a seguir

`
;extension=php_openssl.dll
`

Edite a configuração do MySQL, localize a linha abaixo e adicione logo abaixo as próximas duas

`
[mysqld]
`

`
collation-server = utf8mb4_unicode_ci
character-set-server = utf8mb4
`

**Composer**

[https://getcomposer.org/download/](https://getcomposer.org/download/)

**WP-CLI**

```text
mkdir composer
cd C:\composer\
```

```text
composer create-project wp-cli/wp-cli --no-dev
```

```text
set PATH=C:\composer\wp-cli\bin\wp.bat;%PATH%
```