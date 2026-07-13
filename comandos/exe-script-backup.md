# EXECUTANDO SCRIPT DE BACKUP

## Chamando o script

```Bash
cmd@usuario: ./compactador
```
SAIDA: O programa ./compactador requer nome do diretorio e o dos arquivos que requer sermpactados


## Passando os parametros (Nome para o arquivo + diretorios e arquivos)

```Bash
cmd@usuario: ./compactador testebackup.tar.gz /home/lia/saudacao.txt /home/lia/novo.txt
```

SAIDA: tar: Removing leading `/' from member names
       tar: Removing leading `/' from hard link targets
       Compactado com sucesso em testebackup.tar.gz


## Listando os arquivos para visualizar o arquivo de backup criado
```Bash
cmd@usuario: ls
```

SAIDA: testebackup.tar.gz

## Abrindo o arquivo tar para verificar os arquivos existente dentro dele.

```Bash
cmd@usuario: tar -tf testebackup.tar.gz
```

SAIDA: home/usuario/saudacao.txt
       home/usuario/novo.txt
