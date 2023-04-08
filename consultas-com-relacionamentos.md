# Consultas com relacionamentos

### Relacionando tabela aluno com tabela aluno_curso

```sql
SELECT *
FROM aluno
JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id;
```

### Relacionando tabela aluno com tabela curso

```sql
SELECT *
FROM aluno
JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
JOIN curso ON curso.id = aluno_curso.curso_id;
```

### Relacionando tabela aluno com tabela curso, obtendo nome do aluno e do curso

```sql
SELECT
    aluno.nome as "Nome do Aluno",
    curso.nome as "Nome do Curso"
FROM aluno
JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
JOIN curso ON curso.id = aluno_curso.curso_id;
```