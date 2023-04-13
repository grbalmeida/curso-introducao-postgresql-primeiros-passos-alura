# Agrupando consultas

### Obtém os nomes sem repetir

```sql
SELECT DISTINCT nome
FROM funcionarios
ORDER BY nome;
```

| nome     |
| -------- |
| Alberto  |
| Diogo    |
| João     |
| Nico     |
| Vinícius |

### Obtém o nome e o sobrenome sem repetir (Diogo Mascarenhas que está duplicado será exibido apenas uma vez)

```sql
SELECT DISTINCT nome, sobrenome
FROM funcionarios
ORDER BY nome;
```

| nome     | sobrenome   |
| -------- | ----------- |
| Alberto  | Martins     |
| Diogo    | Mascarenhas |
| João     | Roberto     |
| Nico     | Steppat     |
| Vinícius | Dias        |

### Obtém a quantidade de pessoas com o mesmo sobrenome

```sql
SELECT nome, sobrenome, COUNT(id)
FROM funcionarios
GROUP BY nome, sobrenome
ORDER BY nome;
```

| nome     | sobrenome   | count |
| -------- | ----------- | ----- |
| Alberto  | Martins     |   1   |
| Diogo    | Mascarenhas |   2   |
| Diogo    | Oliveira    |   1   |
| João     | Roberto     |   1   |
| Nico     | Steppat     |   1   |
| Vinícius | Dias        |   1   |

### Obtém a quantidade de pessoas com o mesmo sobrenome, agrupando pela posição da coluna

```sql
SELECT nome, sobrenome, COUNT(id)
FROM funcionarios
GROUP BY 1, 2
ORDER BY nome;

-- Agrupando pelo nome e sobrenome
```

| nome     | sobrenome   | count |
| -------- | ----------- | ----- |
| Alberto  | Martins     |   1   |
| Diogo    | Mascarenhas |   2   |
| Diogo    | Oliveira    |   1   |
| João     | Roberto     |   1   |
| Nico     | Steppat     |   1   |
| Vinícius | Dias        |   1   |

### Obtendo a quantidade de alunos em cada curso

```sql
SELECT curso.nome, COUNT(aluno.id)
FROM aluno
JOIN aluno_curso ON aluno.id = aluno_curso.aluno_id
JOIN curso ON curso.id = aluno_curso.curso_id
GROUP BY 1
ORDER BY 1;

-- Agrupa e ordena pelo nome do curso
```

| nome       | count |
| ---------- | ----- |
| CSS        |   2   |
| PostgreSQL |   4   |

### Obtém o aluno e em quantos cursos está matriculado

```sql
SELECT aluno.id, aluno.nome, COUNT(curso.id)
FROM aluno
JOIN aluno_curso ON aluno.id = aluno_curso.aluno_id
JOIN curso ON curso.id = aluno_curso.curso_id
GROUP BY aluno.id
ORDER BY aluno.nome;
```