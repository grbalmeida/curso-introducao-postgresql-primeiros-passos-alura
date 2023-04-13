# Filtrando consultas agrupadas

### Obtém os cursos sem alunos matriculados

```sql
SELECT curso.nome, COUNT(aluno.id)
FROM curso
LEFT JOIN aluno_curso ON aluno_curso.curso_id = curso.id
LEFT JOIN aluno ON aluno.id = aluno_curso.aluno_id
GROUP BY 1
HAVING COUNT(aluno.id) = 0;
```

| nome  | count |
| ----- | ----- |
| Java  |   0   |
| HTML  |   0   |

### Obtém os cursos com alunos matriculados

```sql
SELECT curso.nome, COUNT(aluno.id)
FROM curso
LEFT JOIN aluno_curso ON aluno_curso.curso_id = curso.id
LEFT JOIN aluno ON aluno.id = aluno_curso.aluno_id
GROUP BY 1
HAVING COUNT(aluno.id) > 0;
```

| nome       | count |
| ---------- | ----- |
| PostgreSQL |   4   |
| CSS        |   2   |

### Obtém os funcionários com nome duplicado

```sql
SELECT nome, COUNT(id)
FROM funcionarios
GROUP BY nome
HAVING COUNT(id) > 1;
```

| nome   | count |
| ------ | ----- |
| Diogo  |   3   |

### Obtém os funcionários que não tem o nome duplicado

```sql
SELECT nome, COUNT(id)
FROM funcionarios
GROUP BY nome
HAVING COUNT(id) = 1;
```

| nome     | count |
| -------- | ----- |
| Nico     |   1   |
| João     |   1   |
| Vinícius |   1   |
| Alberto  |   1   |