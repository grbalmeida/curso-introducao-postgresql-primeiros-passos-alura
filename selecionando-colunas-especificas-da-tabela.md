# Selecionando colunas específicas da tabela

### Selecionando apenas a coluna nome

```sql
SELECT nome FROM aluno;
```

### Selecionando coluna nome e idade

```sql
SELECT
    nome,
    idade
FROM aluno;
```

### Selecionando colunas nome, idade e matriculado_em

```sql
SELECT
    nome,
    idade,
    matriculado_em
FROM aluno;
```

### Selecionando colunas nome, idade e matriculado_em, utilizando o alias quando_se_matriculou para a coluna matriculado_em

```sql
SELECT
    nome,
    idade,
    matriculado_em AS quando_se_matriculou
FROM aluno;
```

### Selecionando colunas nome, idade e matriculado_em com alias com espaço

```sql
SELECT
    nome AS "Nome do Aluno",
    idade AS "Idade do Aluno",
    matriculado_em AS "Quando se matriculou"
FROM aluno;
```