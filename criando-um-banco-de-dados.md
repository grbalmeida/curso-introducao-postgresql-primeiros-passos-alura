# Criando um banco de dados

### Comando para criar um banco de dados na linha de comando

```sql
CREATE DATABASE alura;
```

### Comando gerado pelo wizard de criação de bancos do PGAdmin

```sql
CREATE DATABASE teste
    WITH
    OWNER = postgres
    ENCODING = 'UTF8'
    CONNECTION LIMIT = 1;
```

### Comando para listar os bancos de dados

```
\l
```

### Comando para excluir um banco de dados

```sql
DROP DATABASE teste;
```