# Limitando as consultas

### Buscando os 5 primeiros funcionários

```sql
SELECT * FROM funcionarios LIMIT 5;
```

### Buscando os 5 primeiros funcionários ordenando pelo nome

```sql
SELECT *
FROM funcionarios
ORDER BY nome
LIMIT 5;
```

### Buscando os 5 primeiros funcionários ordenando pelo id

```sql
SELECT *
FROM funcionarios
ORDER BY id
LIMIT 5;
```

### Obtendo do segundo ao sexto funcionário (OFFSET 1)

```sql
SELECT *
FROM funcionarios
ORDER BY id
LIMIT 5
OFFSET 1;
```

### Obtendo do primeiro ao quinto funcionário (OFFSET 0)

```sql
SELECT *
FROM funcionarios
ORDER BY id
LIMIT 5
OFFSET 0;
```

### Obtendo do terceiro ao sétimo funcionário (OFFSET 2)

```sql
SELECT *
FROM funcionarios
ORDER BY id
LIMIT 5
OFFSET 2;
```

### Obtendo do quarto ao sétimo funcionário (OFFSET 3) mesmo limitando a 5 funcionários, irá trazer apenas 4 funcionários

```sql
SELECT *
FROM funcionarios
ORDER BY id
LIMIT 5
OFFSET 3;
```