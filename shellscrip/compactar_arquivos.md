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
tar -czf "$nome_arquivo_backup" "${arquivos[@]}"
echo "Compactado com sucesso em $nome_arquivo_backup"
```


## Verificando argumentos passados pelo usuario

- $# = argumento passado pelo usuario
- -lt = se o parametro passado pelo usuario for menor que 2, retornar uma mensagem
- echo = exibi na tela a mensagem entre aspas duplas
- $0 = é a possição do nome do arquivo desse bash
- exit 1 = finaliza com um erro

## Comando para receber os diretorios de backup e nome do arquivo

- nome_arquivo_backup = varivel responsavel por receber o nome do arquivo de backup
- $1 = posição do nome do arquivo de backup
- arquivos = variavel responsavel por receber os arquivos que seram compactados
- ("${@:2}") = pegue todos os argumentos apartir da posição 2
- tar = criar um arquivo compactado de acordo com os parametros
- -czf = Arquivo/gzip/criar
- $nome_arquivo_backup = vai receber o nome digitado pelo usuario para nomear o arquivo de backup.
- ${arquivos[@]} = vai receber o nome dos arquivos que deseja fazer backup
- echo = uma mensagem sera exibida para indicar que o script foi finalizado com sucesso



## TIPS

1. Na linha 07 a 10 = Executa uma condição IF que verificará se a confiçao é verdadeira, caso o usuario tenha digitado o nome do arquivo para executa-lo, a mensagem ECHO aparece informando o que ele precisa digitar mais argurmentos para executar o script de backup. A posiçao inicial do nome do script é 0.
2. Na linha 12 = Uma variavel vai receber o nome do arquivo de backup que foi digita pelo usuario no parametro/posiçao 1.
3. Na linha 13 = Uma variavel vai receber um array para armazenar os outros parametros que serão, o nome do arquivo de backup e o diretorio que ele estar. 
