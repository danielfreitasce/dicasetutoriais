# Como instalar o PostgreSQL no Manjaro 21 (Pahvo)

Recentemente tive dificuldades em instalar o Postgresql no Manjaro 21. 
Então eu deixo aqui um "ligtning tutorial" :zap: pra quem está passando esse novo desafio e que por acaso conseguiu encontrar essa página. 

## Instale o PostgresSQL

Instale o postgreSQL:  

`sudo pacman -S postgresql`  

A instalação cria um usuário do sistema chamado postgres. Mude para este usuário e inicialize o banco de dados:  

`sudo -u postgres –i`  

`initdb --locale $LANG -E UTF8 -D '/var/lib/postgres/data'`  

Saia do usuário:  

`exit`  

Ative o PostgreSQL:  

`sudo systemctl enable postgresql`

E inicie o serviço:  

`sudo systemctl start postgresql`

## Configurar o PostgreSQL

Volte para o usuário postgres e execute o comando `psql` para logar no banco de dados:  

`sudo -u postgres psql`  

Crie uma senha para o usuário: 

`\password postgres`  

Digite uma nova senha e confirme.  

Saia do banco de dados:  

`\q`  

Se você deseja aprender PostgreSQL de graça, te indico estes cursos:  
Faz esse primeiro: [Modelagem de Bancos de Dados](https://www.youtube.com/playlist?list=PLucm8g_ezqNoNHU8tjVeHmRGBFnjDIlxD);  
Depois esse: [Curso de PostgreSQL - Bancos de Dados](https://www.youtube.com/playlist?list=PLucm8g_ezqNoAkYKXN_zWupyH6hQCAwxY).

Fontes?  
[How to Install, Configure, and Upgrade PostgreSQL on Arch Linux](https://www.vultr.com/docs/how-to-install-configure-and-upgrade-postgresql-on-arch-linux)  
[How To Install PostgreSQL on Manjaro 20](https://idroot.us/install-postgresql-manjaro-20/)




