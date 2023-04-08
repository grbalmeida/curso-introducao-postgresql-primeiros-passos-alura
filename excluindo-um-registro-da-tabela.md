# Excluindo um registro da tabela

### Buscando o aluno que será excluído

```sql
SELECT *
    FROM aluno
WHERE nome = 'Nico';
```

### Comando para excluir o aluno com nome Nico

```sql
DELETE
    FROM aluno
WHERE nome = 'Nico';
```