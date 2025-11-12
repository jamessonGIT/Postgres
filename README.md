# Postgres com Docker

Após instalação do Docker, testar a versão do mesmo.

> docker -v

# Instalando & Executando o Postgres


Executar um dos 2 comandos abaixo:

> docker run --name meupostgres -e POSTGRESPASSWORD=minhasenha -p 5432:5432 -d postgres

> docker run --name meu_postgres -e POSTGRES_PASSWORD=minhasenha -p 5432:5432 -d postgres

Persistência de dados (opcional)
Para manter os dados mesmo após reiniciar o container:

> -v pgdata:/var/lib/postgresql/data  -d postgres
