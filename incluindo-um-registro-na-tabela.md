# Incluindo um registro na tabela

### Comando para incluir um registro na tabela aluno

```sql
INSERT INTO aluno (
    nome,
    cpf,
    observacao,
    idade,
    dinheiro,
    altura,
    ativo,
    data_nascimento,
    hora_aula,
    matriculado_em
)
VALUES (
    'Diogo',
    '12345678901',
    'Proin non iaculis neque. Vivamus eros metus, fringilla eu risus semper, mattis consectetur lacus. Nunc et nisi felis. Sed sodales ligula vitae ante efficitur vulputate. Vivamus nec semper sem. Proin auctor consectetur nisl, quis molestie purus convallis sed. Vivamus maximus, eros id laoreet ornare, felis tellus dignissim lectus, vitae pharetra elit leo ut odio. In gravida tristique nisl sit amet ultricies. Aliquam mattis vulputate metus, non consequat eros scelerisque nec. Nam ut ligula arcu. Donec rutrum molestie tellus, lobortis facilisis neque suscipit in. Nullam varius efficitur molestie. Ut malesuada gravida lacus, sed sagittis arcu finibus eu. Integer augue massa, blandit laoreet finibus et, posuere vitae lacus. Sed ut dapibus felis.',
    35,
    100.50,
    1.81,
    TRUE,
    '1984-08-27',
    '17:30:00',
    '2023-04-08 16:28:45'
);
```