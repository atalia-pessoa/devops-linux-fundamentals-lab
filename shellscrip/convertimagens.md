
```Bash
#! /bin/bash

read -p "Digite o caminho onde as imagens estao armazenadas: " n_diretorio

if [ -d "$n_diretorio" ]; then
        read -p "Digite o nome da imagem a ser convertida (.jpg): " imagem
        convert "$n_diretorio/$imagem" "$n_diretorio/${imagem%.jpg}.png"
        echo "Imagem convertida!"
else
        echo "Diretorio nao existe!"
fi
```

## Recebendo diretorio onde estao armazenado a imagem
- read -p: exibi uma mensagem para o usuario e chamado o promt para receber um valor digitado
- n_diretorio: variavel responsavel por armazenar o valor digitado pelo usuario
- -d "$n_diretorio": identifica se o diretorio existe ou nao
- read -p ... imagem: solicita ao usuario o nome da imagem com extesao .jpg e armazena na variavel imagem
- convert: funcao usada para converter uma imagem com um formato para outro formado desejado
- "$n_diretorio/$imagem": acessar o diretorio que o usario digitou e recebe o nome da imagem digitada
- $n_diretorio/${imagem%.jpg}.png: acessa novamente o diretorio e remove a extensao jpg usando o %, alegando que sera retirado a extensao jpg depois do nome.
- echo "Imagem convertida!": mensagem de sucesso
- else echo "Imagem nao existe!": mensagem de erro caso o diretorio nao exista.
