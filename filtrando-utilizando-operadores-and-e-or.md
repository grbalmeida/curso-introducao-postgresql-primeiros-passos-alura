# Filtrando utilizando operadores E e OU

## AND

### Filtrando todos os alunos que começam com a letra D e que possuem cpf

```sql
SELECT *
FROM aluno
WHERE nome LIKE 'D%'
AND cpf IS NOT NULL;
```

## OR

### Filtrando alunos com nome Diogo OU Rodrigo

```sql
SELECT *
FROM aluno
WHERE nome LIKE 'Diogo'
OR nome LIKE 'Rodrigo';
```

### Filtrando alunos com nome Diogo OU Rodrigo ou que começem com Nico

```sql
SELECT *
FROM aluno
WHERE nome LIKE 'Diogo'
OR nome LIKE 'Rodrigo'
OR nome LIKE 'Nico%';
```

### Filtrando alunos que terminem com Steppat e começem com Nico

```sql
SELECT *
FROM aluno
WHERE nome LIKE '%Steppat'
AND nome LIKE 'Nico%';
```

### Filtrando alunos que o nome seja Diogo ou que começem com Nico

```sql
SELECT *
FROM aluno
WHERE nome LIKE 'Diogo'
OR nome LIKE 'Nico%';
```