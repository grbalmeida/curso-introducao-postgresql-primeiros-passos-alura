# Criando tabela com chave estrangeira

### Criando tabela de alunos simples

```sql
CREATE TABLE aluno (
    id SERIAL PRIMARY KEY,
    nome VARCHAR(255) NOT NULL
);
```

### Populando tabela de alunos

```sql
INSERT INTO aluno (nome) VALUES ('Diogo');
INSERT INTO aluno (nome) VALUES ('Vinícius');
```

### Criando tabela que relaciona alunos com os cursos (com chave composta)

```sql
CREATE TABLE aluno_curso (
    aluno_id INTEGER,
    curso_id INTEGER,
    PRIMARY KEY (aluno_id, curso_id)
);
```

### Populando a tabela aluno_curso

```sql
insert into aluno_curso (aluno_id, curso_id) values (1, 1);
insert into aluno_curso (aluno_id, curso_id) values (1, 2);
insert into aluno_curso (aluno_id, curso_id) values (1, 3);
insert into aluno_curso (aluno_id, curso_id) values (1, 4);

insert into aluno_curso (aluno_id, curso_id) values (2, 1);
insert into aluno_curso (aluno_id, curso_id) values (2, 2);
insert into aluno_curso (aluno_id, curso_id) values (2, 3);
insert into aluno_curso (aluno_id, curso_id) values (2, 4);
```

### Criando tabela que relaciona alunos com os cursos (com chave estrangeira)

```sql
CREATE TABLE aluno_curso (
    aluno_id INTEGER,
    curso_id INTEGER,
    PRIMARY KEY (aluno_id, curso_id),

    FOREIGN KEY (aluno_id)
        REFERENCES aluno (id),
    FOREIGN KEY (curso_id)
        REFERENCES curso (id)
);
```