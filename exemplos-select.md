# SQL SELECT - EXEMPLOS DE CONSULTAS AO BANCO FLY BY NIGTH


O Comando `SELECT` é usado para **consultar dados armazenados nas tabelas do banco de dados**.

## SELECT básico

Consultar todos os dados de uma tabela:




```sql

SELECT * FROM produtos;

```

## SELECT para determinadas colunas


```sql

SELECT nome, preco FROM produtos;

```

## Alterando o nome de exibição das colunas

Usamos o comando `As` para criar um **apelido( alias)**.

```sql
SELECT
nome AS produto,
preco AS valor 
from produtos;

```

## Filtrando registros com Where
O `WHERE` permite determinar **quais registros devem aparecer** no resultado, Na prática, são condições para execução do `SELECT`.


```sql
SELECT * FROM produtos WHERE quantidade = 0;
```


## COMPARAÇÃO DE MAIOR
```sql

SELECT nome, preco FROM produtos WHERE preco > 1000;

```
## COMPARAÇÃO DE MENOR OU IGUAL
```sql

SELECT nome, preco FROM produtos WHERE preco <= 100;

```

### COMPARAÇÃO DE DIFERENÇA

Normalmente se usa o operador `<>` em vez do `!=`.

```sql

SELECT * FROM produtos WHERE fornecedor_id <> 1;

```

---

## Combinando condições
 
Usamos o `WHERE` e operadores lógicos e relacionais.
 
### Operador AND (E)
 
Exibir os produtos que custem menos de 500 e quantidade acima de 20.
 
```sql
SELECT nome, preco, quantidade FROM produtos
WHERE preco < 500 AND quantidade > 20;
```
 
### Operador OR (OU)
 
Exibir os produtos que custem mais de 3000 ou com quantidade zerada.
 
```sql
SELECT nome, preco, quantidade FROM produtos
WHERE preco > 3000 OR quantidade = 0;
```
 
```sql
SELECT nome, preco FROM produtos WHERE NOT preco > 1000;

```
 **Obs.:** o uso do `NOT` não é obrigatorio , desde que vocé consiga o mesmo resultado usando uma lógica diferente , como no exemplo:

 `SELECT nome, preco FROM produtos WHERE preco <= 1000;`

 ### BETWEEN
 Exibir produtos com preço **entre 100 e 500**.

 ```sql

SELECT nome, preco FROM produtos
WHERE preco BETWEEN 100 AND 500;
 
```

### IN

Exibir produtos que tenha o fornecedor ID 1, 4 ou 8.

```sql
SELECT * FROM produtos
WHERE fornecedor_id IN (1,4,8);

```