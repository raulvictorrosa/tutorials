Chave SSH e conectar servidor via SSH
---------------------------------------------

```sh
# visualiza sua chave
$ cat ~/.ssh/id_rsa.pub

# copia chave ssh para o clipboard
$ cat ~/.ssh/id_rsa.pub | xclip -sel clip

# gera a chave
$ ssh-keygen -t rsa -C "account@domain"

# copia sua chave para as autorizadas no servidor
$ scp ~/.ssh/id_rsa.pub username@server:~/.ssh/authorized_keys

# conecta ao servidor.
$ ssh username@server

# recebe no servidor a atual versão do repositório
$ git pull
```
