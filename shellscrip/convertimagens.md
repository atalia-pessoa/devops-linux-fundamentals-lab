# CONVERSAO DE IMAGENS JPG PARA PNG

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

- read -p: exibi uma mensagem para o usuario e chamado o promt para receber um valor digitado
- n_diretorio: variavel responsavel por armazenar o valor digitado pelo usuario
- -d "$n_diretorio": identifica se o diretorio existe ou nao
- read -p ... imagem: solicita ao usuario o nome da imagem com extesao .jpg e armazena na variavel imagem
- convert: funcao usada para converter uma imagem com um formato para outro formado desejado
- "$n_diretorio/$imagem": acessar o diretorio que o usario digitou e recebe o nome da imagem digitada
- $n_diretorio/${imagem%.jpg}.png: acessa novamente o diretorio e remove a extensao jpg usando o %, alegando que sera retirado a extensao jpg depois do nome.
- echo "Imagem convertida!": mensagem de sucesso
- else echo "Imagem nao existe!": mensagem de erro caso o diretorio nao exista.


## Existe outra manera de escrever esse script usando o laço FOR

```Bash
#! /bin/bash

read -p "Digite o caminho onde as imagens estao: " diretorio

if [ ! -d "$diretorio" ]; then
        echo "Diretorio nao existe"
        exit 1
fi

for imagens in "$diretorio"/*.jpg; do
        convert "$imagens" "${imagens%.jpg}.png" && echo "Imagens convertidas!" || echo "Falha na conversao"
done

echo "Conversao concluida!"
```

O unico ponto diferente é o uso do FOR que é usado para realizar a conversão de varios arquivos em um loop.
Abaixo eu explico quais os pontos diferentes.

- imagens: é a variavel responsavel por armazenar os resultados regarados a cada loop
- "${$diretorio": diretorio digitado pelo usuario
- /*jpg}: o barra separa o diretorio dos arquivos exitentes. O * indica que nao importa qual o nome o arquivo tenha, mas que terminei com .jpg
- .png: é a extensao definida para conversao
- &&: executa o proximo comando se o anterior for verdadeiro
- ||: é o else







