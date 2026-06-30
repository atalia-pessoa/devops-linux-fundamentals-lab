### 1: Listar todos os diretorios

```Bash
ls
```

### 2: Listar arquivos ocultos

```Bash
ls -a
```
### 3: Criando diretorios

```Bash
makdir nome_pasta
```

### 4: Criando arquivos

```Bash
touch nome_arquivo.txt
```

### 5: Navegar em diretorio

```Bash
cd nome_pasta
```

### 6: Historico de todos o comandos utilizados

```Bash
history
```

### 7: Ler e Exibir arquivos

```Bash
cat arquivo.txt
```
### 8: Criar arquivos de formar pratica

```Bash
cat hello world > nome_pasta
```
O arquivo criado vai ter o conteudo hello world

### 9: Exibir mensagem na tela

```Bash
echo "hello world"
```

### 10: Compactar aquivos

```Bash
tar -czf nome_arquivo.tar.gz arquivo1.txt arquivo2.txt

#czf = parametro (criar e compactar arquivo)
#nome_aquivo.tar.gz = nome do arquivo que deseja e o tipo desse arquivo no formato tar
#arquivo1 e aquivo2 = sao os arquivos que eu desejo compactar
```

### 11: Mover arquivo

```Bash
mv nome_arquivo /home/usuario/nome_pasta

#movendo o arquivo para o diretorio destinado
```

### 12: Remover arquivo

```Bash
rm nome_arquivo
```

### 13: Criando varios diretorios

```Bash
mkdir -p app/diretorio1 app/diretorio2

#Sera criado o diretorio1 e diretorio2 no diretorio app
```

### 14: Listando os arquivos que começam com as letras music

```Bash
ls music*

#Sera exibido diretorios e arquivos que tem as iniciar: music.
```

