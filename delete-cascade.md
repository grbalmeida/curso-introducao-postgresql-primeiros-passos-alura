# DELETE CASCADE

Ao tentar excluir o aluno, com o comando abaixo é exibida a mensagem abaixo:

```sql
DELETE FROM aluno WHERE id = 1;
```

ERROR:  update or delete on table "aluno" violates foreign key constraint "aluno_curso_aluno_id_fkey" on table "aluno_curso"
DETAIL:  Key (id)=(1) is still referenced from table "aluno_curso".

O comportamento padrão é restringir a exclusão de um registro que já esteja vinculado a outra tabela.

### Comportamento padrão do create table para restringir exclusões

```sql
CREATE TABLE aluno_curso (
    aluno_id INTEGER,
    curso_id INTEGER,
    PRIMARY KEY (aluno_id, curso_id),

    FOREIGN KEY (aluno_id)
        REFERENCES aluno (id)
        ON DELETE RESTRICT,
    
    FOREIGN KEY (curso_id)
        REFERENCES curso (id)
        ON DELETE RESTRICT
);
```

### Recriando tabela aluno_curso, permitindo a exclusão do aluno, mesmo se ele tiver relacionamento com outra tabela

```sql
CREATE TABLE aluno_curso (
    aluno_id INTEGER,
    curso_id INTEGER,
    PRIMARY KEY (aluno_id, curso_id),

    FOREIGN KEY (aluno_id)
        REFERENCES aluno (id)
        ON DELETE CASCADE,

    FOREIGN KEY (curso_id)
        REFERENCES curso (id)
        ON DELETE CASCADE
);
```