## SQL -  Exemplos de consultas  do ban Fly By Night

O comando `SELECT` é usado para **consultar dados armazenados nas tabela do banco de dados**.

## SELECT básico: Consultar todos os dados de uma tabela:

```sql
SELECT * FROM produtos;
```
## SELECT para apenas determinadas colunas 

```sql
SELECT nome, preco FROM produtos;
```
## Alterando o nome de exibição das colunas

Usamos o comando  `AS` para criar um **apelido (alias)**.

```sql
SELECT
 nome AS produto,
 preco AS valor
FROM produtos;
```

## FILTRANDO registro com WHERE

o `WHERE` permite determinar **quando registro devem aparecer** no resultado. Na prática, são condições para execulsão para execução do `SELECT`.
 
 ```sql
 SELECT * FROM  produtos WHERE quantidade = 0;
 ```

 ### Comparação de maios/menor

 ```sql
 SELECT nome, preco FROM produtos WHERE preco > 1000;
 ```

 ### Comparação de menor e igual 

```sql
SELECT nome, preco FROM produtos WHERE preco <= 100;
```

### Comparação de diferença

Normalmente se usa o operador `<>` em vez do ``!=``.

```sql
SELECT * FROM produtos WHERE fornecedor_id <> 1;
```

## Combinando condições 

Usamos o `WHERE` e operadores lógicos e relacionais.

### Operador  AND (E)

Exibir os produtos que custem menos de 500 e quantidade acima de 20.

```sql
SELECT nome, preco, quantidade FROM produtos WHERE preco < 500 AND quantidade > 20;
```

### Operador OR (OU)

Exibir  os produtos  que custem mais de 3000 ou com quantidade zerarada.

```sql
SELECT nome, preco, quantidade FROM produtos WHERE preco > 3000 OR quantidade = 0;
```

### Operador NOT(NÃO)

Exibir os produtos que **não possuem preço acima de 1000**.

```sql
SELECT nome, preco FROM produtos WHERE NOT preco > 1000;
```

**Obs.:** o uso do `NOT` não é obrigatório, desde que você consiga o mesmo resultado usando uma lógica diferente, como por exemplo:
`SELECT nome, preco FROM produtos WHERE  preco <= 1000;`

### BETWEEN

EXIBIR produtos com preço **entre 100 e 500**.

```sql
SELECT nome, preco FROM produtos WHERE preco BETWEEN 100 AND 500;
```

### IN

Exibir produtos  que tem fornecedor ID 1, 4 ou 8.

```sql
SELECT * FROM produtos WHERE fornecedor_id IN (1, 4, 8);
```