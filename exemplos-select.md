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
SELECT * FROM produtos WHERE fornrcedor_id <> 1;
```