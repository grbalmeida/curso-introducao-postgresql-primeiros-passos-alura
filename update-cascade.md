# UPDATE CASCADE

Mesmo com o ON DELETE CASCADE, ao tentar alterar o registro com o comando abaixo, é exibida a seguinte mensagem:

```sql
UPDATE aluno
SET id = 10
WHERE id = 1;
```

ERROR:  update or delete on table "aluno" violates foreign key constraint "aluno_curso_aluno_id_fkey" on table "aluno_curso"
DETAIL:  Key (id)=(1) is still referenced from table "aluno_curso".

### Alterando tabela para permitir o UPDATE CASCADE

```sql
CREATE TABLE aluno_curso (
    aluno_id INTEGER,
    curso_id INTEGER,
    PRIMARY KEY (aluno_id, curso_id),

    FOREIGN KEY (aluno_id)
        REFERENCES aluno (id)
        ON DELETE CASCADE
        ON UPDATE CASCADE,

    FOREIGN KEY (curso_id)
        REFERENCES curso (id)
        ON DELETE CASCADE
        ON UPDATE CASCADE
);
```