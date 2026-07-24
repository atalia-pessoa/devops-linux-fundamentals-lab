```Bash
#! /bin/bash

read -p "Digite o diretorio a ser feito o backup: " origem

read -p "Digite o diretorio que deva armazenar: " destino


tar -czf "$destino/backup.tar.gz" "$origem"
echo "Backup realizado com sucesso!"
``` 
