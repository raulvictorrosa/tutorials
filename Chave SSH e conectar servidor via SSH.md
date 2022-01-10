Chave SSH e conectar servidor via SSH
---------------------------------------------

https://docs.gitlab.com/ee/ssh/


```sh
# visualiza sua chave
$ cat ~/.ssh/id_rsa.pub

# copia chave ssh para o clipboard
$ cat ~/.ssh/id_rsa.pub | xclip -sel clip

# gera a chave
$ ssh-keygen -t rsa -C "account@domain"

Alternatively, you can generate a new RSA key with the more secure encryption format with the following command:
$ ssh-keygen -o -f ~/.ssh/id_rsa -t rsa -b 4096 -C "account@domain"

# copia sua chave para as autorizadas no servidor
$ ssh-copy-id -i ~/.ssh/mykey user@host

# conecta ao servidor.
$ ssh username@server

# recebe no servidor a atual versão do repositório
$ git pull
```
