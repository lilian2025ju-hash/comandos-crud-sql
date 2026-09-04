# Comandos CRUD para o banco de dados FLY BY NIGTHT

## INSERT na Tabela de Fornecedores


```sql
--Insert de fornecedores
INSERT INTO fornecedores (nome) VALUES ('Eletrônicos Tabajara');

INSERT INTO fornecedores (nome) VALUES ('Games ABCD'),('Supermercado tem de tudo'),('Livraria Demais da conta');
```
 ## INSERT na tabela de Produtos

 ```sql

INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id)
values(
    'Smartphone Galaxy s23', 
    'Equipamento com sistema Android e câmera FULL HD e etc e tal',
    1599.49,
    20, 
    1 -- id do fornecedor Eletônicos Tabajara
);


INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id)
values(
    'Senhor dos Anéis: As Duas Torres', 
    'Volume 2 da série de livros criados autor j.R.R Tolkien',
    80.99,
    100, 
    4 -- id do fornecedor Eletônicos Tabajara
);


INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id)
values(
    'TV LED', 
    'Tela de 50 polegadas, resolução 4K, entradas HDMI e etc e tal',
    3420,
    12, 
    1 -- id do fornecedor Eletônicos Tabajara
);
 ```

 ## INSERT NA TABELA DE LOJAS
 ```sql
-- Insira sa lojas :Casas bahia, Shopping Zona Leste, Bazar das coisas, Americanas.
INSERT INTO lojas(nome) Values ('Casas bahia');
INSERT INTO lojas(nome) Values ('Shopping Zona Leste');
INSERT INTO lojas(nome) Values ('Bazar das coisas');
INSERT INTO lojas(nome) Values ('Americanas');

  ```


