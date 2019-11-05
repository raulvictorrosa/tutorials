Criar BKP por linha de comando em SSH
-----------------------------------------------

```sh
# Lista arquivos da pasta onde você está
$ ls

# Acessa a pasta desejada
$ cd nomepasta

# Cria o .tar para backup
$ tar -czvf bkp-nomedoarquivo-$(date '+%Y%m%d-%H%M%S').tar.gz nomedoarquivooroginal

# Move o arquivo
$ mv nomedoarquivo.tar pastadestino

# Descompacta o arquivo
$ tar -xzvf nomedoarquivo.tar -C pastadestino

# Remove o arquivo desejado
$ rm -rf nomedoarquivo.tar
```
