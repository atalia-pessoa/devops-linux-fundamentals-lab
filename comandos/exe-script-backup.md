lia@lia:~$ ./compactador
O programa ./compactador requer nome do diretorio e o dos arquivos que requer sermpactados
lia@lia:~$ nano compactador
lia@lia:~$ ./compactador
O programa ./compactador requer nome do diretorio e o dos arquivos que requer ser compactados
lia@lia:~$ ./compactador testebackup.tar.gz /home/lia/saudacao.txt /home/lia/novo.txt
tar: Removing leading `/' from member names
tar: Removing leading `/' from hard link targets
Compactado com sucesso em testebackup.tar.gz
lia@lia:~$ ls
Docs                           backup_20260627_001544.tar.gz  compactador  dir1  dir3      saudacao.txt
backup_20260627_000831.tar.gz  backup_server.sh               devops       dir2  novo.txt  testebackup.tar.gz
lia@lia:~$ tar -tf testebackup.tar.gz
home/lia/saudacao.txt
home/lia/novo.txt
lia@lia:~$
