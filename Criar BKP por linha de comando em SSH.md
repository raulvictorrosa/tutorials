Criar BKP por linha de comando em SSH
-----------------------------------------------

```sh
# Lista arquivos da pasta onde você está
$ ls

# Acessa a pasta desejada
$ cd nomepasta

# Cria o .tar para backup
$ tar -cvf nomedoarquivo.tar nomedoarquivooroginal

# Move o arquivo
$ mv nomedoarquivo.tar pastadestino

# Descompacta o arquivo
$ tar -xf nomedoarquivo.tar -C pastadestino

# Remove o arquivo desejado
$ rm -rf nomedoarquivo.tar
```