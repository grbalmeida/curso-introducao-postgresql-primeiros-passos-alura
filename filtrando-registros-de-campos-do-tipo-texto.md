# Filtrando registros de campos do tipo texto

### Inserindo nomes para filtrar

```sql
INSERT INTO aluno (nome) VALUES ('Vinícius Dias');
INSERT INTO aluno (nome) VALUES ('Nico Steppat');
INSERT INTO aluno (nome) VALUES ('João Roberto');
INSERT INTO aluno (nome) VALUES ('Diego');
```

### Filtrando alunos com nome igual a Diogo

```sql
SELECT * FROM aluno WHERE nome = 'Diogo';
```

### Filtrando alunos com nome igual a Vinícius Dias

```sql
SELECT * FROM aluno WHERE nome = 'Vinícius Dias';
```

### Filtrando alunos com nome igual a Nico Steppat

```sql
SELECT * FROM aluno WHERE nome = 'Nico Steppat';
```

### Filtrando alunos com nome igual a João Roberto

```sql
SELECT * FROM aluno WHERE nome = 'João Roberto';
```

### Filtrando alunos com nome igual a Diego

```sql
SELECT * FROM aluno WHERE nome = 'Diego';
```

### Filtrando alunos com nome diferente de Diogo com <>

```sql
SELECT * FROM aluno WHERE nome <> 'Diogo';
```

### Filtrando alunos com nome diferente de Diogo com !=

```sql
SELECT * FROM aluno WHERE nome != 'Diogo';
```

### Filtrando alunos com nome terminando com iogo (Diogo)

```sql
SELECT * FROM aluno WHERE nome LIKE '_iogo';
```

### Filtrando alunos com nome que começa com Di e termina com go (Diego, Diogo)

```sql
SELECT * FROM aluno WHERE nome LIKE 'Di_go';
```

### Filtrando alunos com nome que NÃO começa com Di e NÃO termina com go

```sql
SELECT * FROM aluno WHERE nome NOT LIKE 'Di_go';
```

### Filtrando alunos que começam com a letra D

```sql
SELECT * FROM aluno WHERE nome LIKE 'D%';
```

### Filtrando alunos que terminam com a letra s

```sql
SELECT * FROM aluno WHERE nome LIKE '%s';
```

### Filtrando alunos que tenham espaço no nome

```sql
SELECT * FROM aluno WHERE nome LIKE '% %';
```

### Filtrando alunos que tenham primeiro a letra i e depois a letra a no nome (Vinícius Dias e Nico Steppat)

```sql
SELECT * FROM aluno WHERE nome LIKE '%i%a%';
```