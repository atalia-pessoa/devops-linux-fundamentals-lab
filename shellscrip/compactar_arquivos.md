# COMPACTANDO VARIOS ARQUIVOS

## Nesse bash sera compactado diferentes arquivos em diferentes diretorios e enviar para um diretorio de backup.

```Bash
#! /bin/bash
if [ "$#" -lt 2 ]; then
  echo "O programa $0 requer nome do diretorio e o nome dos arquivos que requer ser compactados"
    exit 1
fi

nome_arquivo_backup="$1"
arquivos=("${@:2}")
tar -czf "nome_arquivo_backup" "${arquivos[@]}"
echo "Compactado com sucesso em $nome_arquivo_backup"
```


- $# = nome do arquivo digitado pelo usuario
- -lt = se o parametro passado pelo usuario for menor que 2
- echo = exibi na tela a mensagem entre aspas duplas
- $0 = é a possição do nome do arquivo desse bash
- exit 1 = finaliza com um erro
- nome_arquivo_backup = varivel responsavel por receber o nome do arquivo de backup
- $1 = posição do nome do arquivo de backup
- arquivos = variavel responsavel por receber os arquivos que seram compactados
- ("${@:2}") = pegue todos os argumentos apartir da posição 2
- tar = criar um arquivo compactado de acordo com os parametros
- -czf = Arquivo/gzip/criar
- echo = saida com uma mensagem para indicar que o script foi finalizado com sucesso




- Na linha 07 a 10 = Executa uma condição IF que verificará se a confiçao é verdadeira, caso o usuario tenha digitado o nome do arquivo para executalo, a mensagem ECHO aparece informando o que ele precisa digitar para executar o script de backup. A posiçao inicial do nome do script é 0
- Na linha 12 = Uma variavel vai receber o nome do arquivo de backup que foi digita pelo usuario no parametro/posiçao 1.
- Na linha 13 = Uma variavel vai receber um array para armazenar os outros parametros que serão, o nome do arquivo de backup e o diretorio que ele estar. 
