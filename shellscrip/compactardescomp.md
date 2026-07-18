# COMPACTAR E DESCOMPACTAR ARQUIVO DE ACORDO COM A FUNCAO DIGITADA PELO USUARIO

## Nesse script sera solicitado ao usuario qual das funcoes ele deseja executar, seja ela Compactar um determinado arquivo ou Descompactar o mesmo.

```Bash
#! /bin/bash

read -p "Digite qual funcao voce deseja executar: 'compactar' ou 'descompactar' = " funcao

case "$funcao" in
        "compactar")
                read -p "Digite o nome do arquivo final com a extensao (.tar.gz): " nomec_arquivo
                read -p "Digite o diretorio/arquivo a ser compactado: " diretorioc_arquivo
                tar -czf "$nomec_arquivo" "$diretorioc_arquivo"
                echo "Arquivo compactado com sucesso!"
        ;;
        "descompactar")
                read -p "Digite o nome do arquivo a ser descompactado com a extensao (.tar.gz): " nom>
                read -p "Digite o diretorio que deseja salvar o arquivo descompactado: " diretoriod_a>
                tar xzf "$nomed_arquivo" -C "$diretoriod_arquivo"
                echo "Arquivo descompactado com sucesso!"
        ;;
        *)
        echo "Operacao invalida!"
        echo "Digite as palavras de acordo com a funcao desejada: compactar ou descompactar"
        exit 1
        ;;
esac
```


