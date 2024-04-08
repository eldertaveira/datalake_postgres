# datalake_postgres
dllocal
Projeto contendo datalake de desenvolvimento. Três instâncias do postegres rodando em containers diferentes.

Instruções


Estando na pasta onde está o arquivo docker-compse.yml, no terminal digite: "docker-compose up"

Use a flag "-d" para liberar o terminal. Ex: "docker-compose up -d"
Use a flag "-f" para indicar o local do arquivo .yml, caso não esteja na mesma pasta em que o arquivo. Ex. "docker-compose up -d -f /opt/bi/dllocal/docker-compose.yml"



Modifique o arquivo hosts ( "/etc/hosts" ) e adicione os ips para cada container e seu respectivo alias.

127.0.0.1 dl1host
127.0.0.2 dl2host
127.0.0.3 dl3host



Tudo pronto para acesso.

Para acessar através de outras máquinas use o ip da máquina host e as portas 54321, 54322 e 54323. ( DL1, DL2 e DL3 respectivamente)
Ex. 10.16.00.100:54321 ( DL1 )
Ex. 10.16.00.100:54322 ( DL2 )
Ex. 10.16.00.100:54323 ( DL3 )



Para parar o serviço use "docker-compose down" ou "docker stop XXX"
