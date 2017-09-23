### Criando o Banco de dados

Faca login no terminal como usuário postgres

```console
$ su postgres
```

Crie o banco de dados

```console
$ createdb nome_banco
```

Para saber os bancos existentes

```console
$ psql -l
```

Para deletar um banco de dados

```console
$ dropdb nome_banco
```


### Restaurando o Banco de Dados

Crie o arquivo de scripts contendo os sqls que deseja executar.

```console
$ echo 'CREATE TABLE teste (id serial);' >> ./0.0.1.sql
```

Faca login no terminal como usuário postgres

```console
$ su postgres
```

Passe o arquivo de scripts como parametro

```console
$ psql -U postgres -d speedcob_beta -f ./0.0.1.sql
```


### Comandos úteis postgres

Comandos dentro do usuário postgres

| Comando | Descricao |
| --- | --- |
| **psql -l** |  lista os bancos de dados existentes |
| **psql -U postgres nome_do_banco** |  conecta ao banco desejado |
| **psql banco -E** |  Mostra um debug das consultas realizadas |
| **psql –version** |  mostra versão do PostgreSQL |
| **createdb** | Cria um banco de dados |
| **dropdb** | Delete um banco de dados existente |


Comandos dentro do console

| Comando | Descricao |
| --- | --- |
| **\q** | sair |
| **\c nomebanco nomeuser** | Conectar a outro banco |
| **\i /path/script.sql** | importar script.sql |
| **\timing** | iniciar/parar o cronômetro para atividades |
| **\dT+** | lista os tipos de dados do PG com detalhes |
| **\cd** | mudar para outro diretório |
| **\d** | lista tabelas, índices, sequências ou views |
| **\d nometabela** | mostra estrutura da tabela |
| **\dt** | lista tabelas |
| **\di** | lista indices |
| **\ds** | lista sequências |
| **\dv** | lista views |
| **\dS** | lista tabelas do sistema |
| **\dn** | lista esquemas |
| **\dp** | lista privilégios |
| **\du** | lista usuários |
| **\dg** | lista grupos |
| **\l** | lista todos os bancos do servidor, juntamente com seus donos e codificações |
| **\e** | abre o editor vi com a última consulta |
| **\o** | inicia/termina a criação de arquivo. Ex.: \o arquivo.sql |
| **\! comando_do_sistemaoperacional** | executa o arquivo do sistema operacional |
| **\?** | ajuda geral dos comandos do psql |
| **\h comandosql** | ajuda específica sobre o comando SQL, ex.: \h alter table |
| **\H** | ativa/desativa saída em HTML |
| **\encoding** | exibe codificação atual |
