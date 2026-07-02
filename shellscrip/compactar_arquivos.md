# COMPACTANDO VARIOS ARQUIVOS

## Nesse bash sera compactado diferentes arquivos em diferentes diretorios e enviar para um diretorio de backup.

```Bash
#! /bin/bash
if [ "$#" -lt 2]; then
  echo "O programa $0 requer nome do diretorio e o nome dos arquivos que requer ser compactados"
    exit 1
fi
arquivo_backup="$1"
arquivos=("${@:2}")
tar -czf "arquivo_backup" "${arquivos[@]}"
echo "COmpactado com sucesso em $arquivo_backup"
```


- $# = parametro digitado pelo usuario
- -lt = se o parametro passado pelo usuario for menor que 2
 echo = exibi na tela a mensagem entre aspas duplas
- $0 = é a possição do nome do arquivo desse bash
- exit 1 = finaliza com um erro
- arquivo_backup = varivel responsavel por receber o nome do arquivo de backup
- $1 = posição do nome do arquivo de backup
- arquivos = variavel responsavel por receber os arquivos que seram compactados
- ("${@:2}") = pegue todos os argumentos apartir da posição 2
