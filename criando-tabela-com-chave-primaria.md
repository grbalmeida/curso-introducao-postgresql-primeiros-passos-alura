# Criando tabela com chave primária

### Criando a tabela de cursos

```sql
CREATE TABLE curso (
    id INTEGER,
    nome VARCHAR(255)
);
```

### Criando a tabela de cursos com id e nome sendo obrigatórios (permite id duplicado)

```sql
CREATE TABLE curso (
    id INTEGER NOT NULL,
    nome VARCHAR(255) NOT NULL
);
```

### Criando a tabela de cursos com id e nome sendo obrigatórios (NÃO permite id duplicado)

```sql
CREATE TABLE curso (
    id INTEGER NOT NULL UNIQUE,
    nome VARCHAR(255) NOT NULL
);
```

### Criando a tabela de cursos com chave primária

```sql
CREATE TABLE curso (
    id INTEGER PRIMARY KEY,
    nome VARCHAR(255) NOT NULL
);
```