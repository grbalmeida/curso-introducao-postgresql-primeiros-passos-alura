# Filtrando registros de campos do tipo numérico, data e booleano

## IS NULL

### Filtrando alunos que não possuem cpf

```sql
SELECT * FROM aluno WHERE cpf IS NULL;
```

### Filtrando alunos que não possuem observacao

```sql
SELECT * FROM aluno WHERE observacao IS NULL;
```

### Filtrando alunos que não possuem idade

```sql
SELECT * FROM aluno WHERE idade IS NULL;
```

## IS NOT NULL

### Filtrando alunos que possuem cpf

```sql
SELECT * FROM aluno WHERE cpf IS NOT NULL;
```

### Filtrando alunos que possuem observacao

```sql
SELECT * FROM aluno WHERE observacao IS NOT NULL;
```

### Filtrando alunos que possuem idade

```sql
SELECT * FROM aluno WHERE idade IS NOT NULL;
```

## IGUAL

### Filtrando alunos com 35 anos de idade

```sql
SELECT * FROM aluno WHERE idade = 35;
```

## DIFERENTE

### Filtrando alunos que não tem 36 anos de idade

```sql
SELECT * FROM aluno WHERE idade <> 36;
```

## MAIOR OU IGUAL

### Filtrando alunos que a idade é igual ou maior que 35

```sql
SELECT * FROM aluno WHERE idade >= 35;
```

## MENOR OU IGUAL

### Filtrando alunos que a idade é menor ou igual a 35

```sql
SELECT * FROM aluno WHERE idade <= 35;
```

## MAIOR

### Filtrando alunos que tenham mais de 35 anos

```sql
SELECT * FROM aluno WHERE idade > 35;
```

## MENOR

### Filtrando alunos que tenham menos de 35 anos

```sql
SELECT * FROM aluno WHERE idade < 35;
```

### Filtrando alunos com menos de 100 anos

```sql
SELECT * FROM aluno WHERE idade < 100;
```

## BETWEEN - ENTRE - INCLUSIVO

### Filtrando alunos que tenham de 10 a 20 anos

```sql
SELECT * FROM aluno WHERE idade BETWEEN 10 AND 20;
```

### Filtrando alunos que tenham de 35 a 40 anos (traz o Diogo que tem 35 anos)

```sql
SELECT * FROM aluno WHERE idade BETWEEN 35 AND 40;
```

### Filtrando alunos que tenham de 10 a 35 anos (traz o Diogo que tem 35 anos)

```sql
SELECT * FROM aluno WHERE idade BETWEEN 10 AND 35;
```

## BOOLEANO

### Filtrando alunos ativos

```sql
SELECT * FROM aluno WHERE ativo = TRUE;
```

### Filtrando alunos inativos

```sql
SELECT * FROM aluno WHERE ativo = FALSE;
```