# Funções de agregação

## COUNT

Retorna a quantidade registros

### Obtendo a quantidade de funcionários

```sql
SELECT COUNT(id)
FROM funcionarios;
```

## SUM

Retorna a soma dos registros

### Obtendo a soma dos ids do 1 ao 7 (1 + 2 + 3 + 4 + 5 + 6 + 7 = 28)

```sql
SELECT
    COUNT(id),
    SUM(id)
FROM funcionarios;
```

## MAX

Retorna o maior valor dos registros

### Obtém o maior id de 1 a 7 (7)

```sql
SELECT
    COUNT(id),
    SUM(id),
    MAX(id)
FROM funcionarios;
```

## MIN

Retorna o menor valor dos registros

### Obtém o menor id de 1 a 7 (1)

```sql
SELECT
    COUNT(id),
    SUM(id),
    MAX(id),
    MIN(id)
FROM funcionarios;
```

## AVG

Retorna a média dos registros

### Obtém a média dos ids (1 + 2 + 3 + 4 + 5 + 6 + 7) / 7 = 4.0000000000000000

```sql
SELECT
    COUNT(id),
    SUM(id),
    MAX(id),
    MIN(id),
    AVG(id)
FROM funcionarios;
```

### Obtém a média dos ids e arredonda para 2 casas decimais = 4.00

```sql
SELECT
    COUNT(id),
    SUM(id),
    MAX(id),
    MIN(id),
    ROUND(AVG(id), 2)
FROM funcionarios;
```

### Obtém a média dos ids sem casas decimais = 4

```sql
SELECT
    COUNT(id),
    SUM(id),
    MAX(id),
    MIN(id),
    ROUND(AVG(id), 0)
FROM funcionarios;
```