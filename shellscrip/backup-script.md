# CRIANDO UM BACKUP USANDO A LINGUAGEM BASH

## Ferramenta:
- [x] Nano

### 1: Abrindo a ferramenta de editor

```Bash
nano
```

### 2: Script de backup

```Bash
#! /bin/bash

diretorio_backup="/home/usuario/devops
nome_arquivo_backup="backup_$(date +%Y%m%d_%H&M%S).tar.gz"
tar -czf "nome_arquivo_backup" "diretorio_backup"
echo "Backup realizado com sucesso em %nome_arquivo_backup"

# primeira linha: representa o interpretador desse script
# segunda linha: é a variavel reponsavel por armazenar o diretorio que sera feito o backup
# terceira linha: é a variavel responsavel por armazenar o nome do arquivo do backup
# terceira linha: ainda na segunda linha o comando $(date +%Y%m%d_%H&M%S).tar.gz, vai exibir a data, mes, ano, dia e horario que ocorreu o backup
# quarta linda: comando para compactar esse arquivo de backup e enviar para o diretorio de backup
# quinta linha: exibe a mensagem de backup concluido com sucesso e o nome do arquivo que foi salvo.
# Salve o arquivo com a extensão sh, exemplo: backup.sh
```

### 3: Mudando as permissões do arquivo para executa-lo

```Bash
chmod +x backup.sh
```

### 4: Executando o script

```Bash
bash backup.sh
```
