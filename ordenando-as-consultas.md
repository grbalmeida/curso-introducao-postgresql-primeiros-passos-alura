# Ordenando as consultas

### Criação da tabela funcionarios

```sql
CREATE TABLE funcionarios (
    id SERIAL PRIMARY KEY,
    matricula VARCHAR(10),
    nome VARCHAR(255),
    sobrenome VARCHAR(255) 
);
```

### Inclusão dos funcionários

```sql
INSERT INTO funcionarios (matricula, nome, sobrenome) VALUES ('M001', 'Diogo', 'Mascarenhas');
INSERT INTO funcionarios (matricula, nome, sobrenome) VALUES ('M002', 'Vinícius', 'Dias');
INSERT INTO funcionarios (matricula, nome, sobrenome) VALUES ('M003', 'Nico', 'Steppat');
INSERT INTO funcionarios (matricula, nome, sobrenome) VALUES ('M004', 'João', 'Roberto');
INSERT INTO funcionarios (matricula, nome, sobrenome) VALUES ('M005', 'Diogo', 'Mascarenhas');
INSERT INTO funcionarios (matricula, nome, sobrenome) VALUES ('M006', 'Alberto', 'Martins');
INSERT INTO funcionarios (matricula, nome, sobrenome) VALUES ('M007', 'Diogo', 'Oliveira');
```

### Ordenando pelo nome


```sql
SELECT * FROM funcionarios ORDER BY nome;
```

### Ordenando pelo nome decrescente

```sql
SELECT * FROM funcionarios ORDER BY nome DESC;
```

### Ordenando pelo nome e por matricula

```sql
SELECT * FROM funcionarios ORDER BY nome, matricula;
```

### Ordenando pelo nome crescente e por matricula decrescente

```sql
SELECT * FROM funcionarios ORDER BY nome, matricula DESC;
```

### Ordenando pela sobrenome (1 - id, 2 - matricula, 3 - nome, 4 - sobrenome)

```sql
SELECT * FROM funcionarios ORDER BY 4;
-- Ordenando pelo sobrenome
```

### Ordenando pelo nome, sobrenome e matricula

```sql
SELECT * FROM funcionarios ORDER BY 3, 4, 2;
```

### Ordenando pelo sobrenome decrescente, nome decrescente e matricula crescente

```sql
SELECT * FROM funcionarios ORDER BY 4 DESC, nome DESC, 2 ASC;
```

### Ordenação utilizando a tabela

```sql
SELECT
	aluno.nome as "Nome do Aluno",
	curso.nome as "Nome do Curso"
FROM aluno
JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
JOIN curso ON curso.id = aluno_curso.curso_id
ORDER BY aluno.nome;
```