
```Bash
#! /bin/bash

read -p "Digite o caminho onde as imagens estao armazenadas: " n_diretorio

if [ -d "$n_diretorio" ]; then
        read -p "Digite o nome da imagem a ser convertida (.jpg): " imagem
        convert "$n_diretorio/$imagem" "$n_diretorio/${imagem%.jpg}.png"
        echo "Imagem convertida!"
else
        echo "Imagem nao existe!"
fi
```

