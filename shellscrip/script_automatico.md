#AGENDANDO O SCRIP PARA EXECUÇÃO AUTOMATICA

- Executar no terminar o comando: crontab -e
- Adicionar na ultima linha para o scrip executar a cada minuto e todos os dias: 
```Bash
* * * * * /home/atalia/monitoramento.sh >>> /homem/atalia/saida_monitoramento.txt
```
- Salve o arquivo
- Depois execute o arquivo:
