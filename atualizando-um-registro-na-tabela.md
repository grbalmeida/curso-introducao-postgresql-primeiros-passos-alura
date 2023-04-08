# Atualizando um registro na tabela

### Buscando o registro que será atualizado

```sql
SELECT *
    FROM aluno
WHERE id = 1;
```

### Comando para atualizar o registro do aluno com o id igual a 1

```sql
UPDATE aluno
    SET nome = 'Nico',
    cpf = '10987654321',
    observacao = 'Teste',
    idade = 38,
    dinheiro = 15.23,
    altura = 1.90,
    ativo = FALSE,
    data_nascimento = '1980-01-15',
    hora_aula = '13:00:00',
    matriculado_em = '2023-04-07 15:00:00'
WHERE id = 1;
```