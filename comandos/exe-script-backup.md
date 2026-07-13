cmd@usuario: ./compactador
SAIDA: O programa ./compactador requer nome do diretorio e o dos arquivos que requer sermpactados

cmd@usuario: ./compactador testebackup.tar.gz /home/lia/saudacao.txt /home/lia/novo.txt
SAIDA: tar: Removing leading `/' from member names
tar: Removing leading `/' from hard link targets
Compactado com sucesso em testebackup.tar.gz

cmd@usuario: ls
SAIDA: Docs                           backup_20260627_001544.tar.gz  compactador  dir1  dir3      saudacao.txt
backup_20260627_000831.tar.gz  backup_server.sh               devops       dir2  novo.txt  testebackup.tar.gz

cmd@usuario: tar -tf testebackup.tar.gz
SAIDA: home/usuario/saudacao.txt
home/usuario/novo.txt
