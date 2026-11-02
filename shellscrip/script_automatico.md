#AGENDANDO O SCRIP PARA EXECUÇÃO AUTOMATICA

- Executar no terminar o comando: crontab -e
- Adicionar na ultima linha para o scrip executar a cada minuto e todos os dias: 
```Bash
* * * * * /home/atalia/monitoramento.sh >>> /homem/atalia/saida_monitoramento.txt
```
- Salve o arquivo
- Depois execute o arquivo:
```Bash
cat saida_monitoramento.txt
```

##Sera exibido a mensagem com a data e horario da execução
