# LEFT, RIGHT, CROSS e FULL JOINS

### LEFT JOIN

```sql
SELECT
	aluno.nome as "Nome do Aluno",
	curso.nome as "Nome do Curso"
FROM aluno
LEFT JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
LEFT JOIN curso ON curso.id = aluno_curso.curso_id;
```

Traz os dados da tabela aluno, porém quando o aluno não é matriculado em um curso, a coluna nome do curso é NULL.

| Nome do Aluno | Nome do Curso |
|---------------|---------------|
| Diogo         | PostgreSQL    |
| Vinícius      | Java          |
| Nico          | NULL          |

### RIGHT JOIN

```sql
SELECT
    aluno.nome as "Nome do Aluno",
    curso.nome as "Nome do Curso"
FROM aluno
RIGHT JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
RIGHT JOIN curso ON curso.id = aluno_curso.curso_id;
```

Traz os dados da tabela curso, e na coluna do nome do aluno é NULL

| Nome do Aluno | Nome do Curso |
|---------------|---------------|
| Diogo         | PostgreSQL    |
| Vinícius      | Java          |
| NULL          | CSS           |

### FULL JOIN

```sql
SELECT
	aluno.nome as "Nome do Aluno",
	curso.nome as "Nome do Curso"
FROM aluno
FULL JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
FULL JOIN curso       ON curso.id = aluno_curso.curso_id;
```

Traz dados da tabela aluno e curso, e quando não houver o relacionamento, traz o valor NULL.

| Nome do Aluno | Nome do Curso |
|---------------|---------------|
| Diogo         | PostgreSQL    |
| Vinícius      | Java          |
| Nico          | NULL          |
| NULL          | CSS           |

### CROSS JOIN

```sql
SELECT
    aluno.nome as "Nome do Aluno",
    curso.nome as "Nome do Curso"
FROM aluno
CROSS JOIN curso;
```

Multiplica a quantidade de dados da tabela A, pela quantidade de dados da tabela B

| Nome do Aluno | Nome do Curso |
|---------------|---------------|
| Diogo         | PostgreSQL    |
| Diogo         | Java          |
| Diogo         | CSS           |
| Vinícius      | PostgreSQL    |
| Vinícius      | Java          |
| Vinícius      | CSS           |
| Nico          | PostgreSQL    |
| Nico          | Java          |
| Nico          | CSS           |