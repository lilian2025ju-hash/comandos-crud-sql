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

Sem usar o `IN`, teríamos que fazer a lógica com multiplos `OR`

```sql
 SELECT * FROM produtos
 WHERE
  fornecedor_id = 1 OR
  fornecedor_id = 4 OR
  fornecedor_id = 8;

```

### LIKE
 
`LIKE` é usado principalmente para realizar pesquisas em textos. Junto com o caractere `%` permite fazer buscas baseadas em partes de uma string.
 
Exemplo: procurar produtos que tenham a palavra **Gamer** em qualquer posição do nome.
 
```sql
SELECT nome, preco FROM produtos
WHERE nome LIKE '%GAMER%'

```
## DISTINCT
Elimina valores repetidos do resultado da consulta.

```sql
SELECT DISTINCT fornecedor_id FROM produtos;
```

## ORDENAÇÃO( OU CLASSIFICAÇÃO)

Usamos o `ORDER BY` para organizar os registros do resultado.

### ORDEM CRESCENTE (PADRÃO)
DO MENOR PARA O MAIOR, OU DE A-Z,DE MAIS ANTIGO PARA MAIS RECENTE.

```sql
SELECT nome, preco FROM produtos
ORDER BY preco ASC; --Nem precisa colocar o Asc, pois é padrão
```
```sql
SELECT nome, preco FROM produtos
ORDER BY preco DESC;
```

## ORDENANDO POR MAIS DE UMA CULUNA
```sql
SELECT nome, preco FROM produtos
ORDER BY preco DESC, nome ASC;

```
## FUNÇÕES DE AGREGAÇÃO

Funções de agregação realizam cálculos ou processos em registros de um resultado.

Entre as principais

- `COUNT ()`->conta registros
- `SUM ()` ->soma valores
- `AVG ()`->calcula a média de valores
- `MIN ()`->encontra o menor valor
- `MAX ()`->encontra o maior valor
- `ROUND ()`->arredonda valores e define casas decimais

## COUNT

Contando quantos registros existem na tabela produtos:

```sql

SELECT COUNT(*) AS total FROM produtos;

```

### SUM

Somar a quantidade de todos os produtos da tabela:

```sql
SELECT SUM(quantidade) AS "QUANTIDADE TOTAL" FROM produtos;

```
### AVG

Calcular a média dos preços dos produtos:

```sql

SELECT AVG(preco) AS "MÉDIA DOS PREÇOS" FROM produtos;

```

### MIN

Retornar o menor preço existente:

```sql
SELECT MAX(preco) AS maior_preco FROM produtos;

```

### COMBINANDO AGREGAÇÕES

```sql
SELECT
COUNT(*) AS quantidades_produtos,
MIN(preco) AS menor_preco,
MAX(preco)AS maior_preco,
ROUND(AVG(PRECO),2) AS preco_medio
FROM produtos;
```

**Atenção:** não coloque espaço entre o nome da função e os parênteses!!

## RECURSOS DE AGRUPAMENTO

`GROUP BY` Reúne Registros que possuem um determinado valor comum

Exemplo: descobrir quantos produtos existem em cada fornecedor.

```sql
SELECT fornecedor_id, COUNT(*) AS total_produto
FROM produtos GROUP BY fornecedor_id;

```

### DETERMINANDO A MÉDIA DE PREÇOS POR FORNECEDOR

