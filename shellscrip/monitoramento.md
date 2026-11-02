#MONITORAMENTO DE PROCESSOS OU SERVICOS

```Bash
#! /bin/bash

if pgrep ngnix &> /dev/null
then
  echo "Ngnix esta operando $( date +"%Y-%m-%d%H:%M:%S")"
else
  echo "Ngnix fora de operacao $( date +"%Y-%m-%d%H:%M:%S")"
fi
```

- pgrep ngnix: processos do ngnix
- &> /dev/null: esse comando vai direcionar o resultado valido e o erro para o descarte, sendo assim, nao sera exibido na tela para o usuario.
- then echo "Ngnix esta operando $( date +"%Y-%m-%d%H:%M:%S")" : exibira a mensagem que o processo esta sendo operado e informa a data e horario dessa execução.
- else echo "Ngnix fora de operacao $( date +"%Y-%m-%d%H:%M:%S")" : exibira a mensagem que o processo esta parado, informando a data e horario dessa execução.
