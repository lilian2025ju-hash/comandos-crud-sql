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