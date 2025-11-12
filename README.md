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

Testar conexão:

> docker exec -it meu_postgres psql -U postgres

saída: **psql (18.0 (Debian 18.0-1.pgdg13+3))**

# Criar tabela usuario:
> postgres=#
CREATE TABLE public.usuarios (
    id SERIAL PRIMARY KEY,
    nome VARCHAR(100) NOT NULL
);

Listar as tabelas existentes no banco:
> postgres=# \dt

Após essas estapas verificar a conexão local com o DBeaver e replicação do banco no mesmo.

