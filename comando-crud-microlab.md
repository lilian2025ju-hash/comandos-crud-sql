# Comandos CRUD para o banco de dados 

## INSERT Inserindo dados

```sql
INSERT INTO usuarios(nome , email, senha, tipo) VALUES
('Ana Silva','ana@email.com','123abc','editor');
('Bruno Souza', 'bruno@email.com','abc456','admim');
('Carla Mendes','carla@email.com','789xyz','editor
 ');


```

--Insert  tabelas categorias
```sql


INSERT INTO categorias (nome) VALUES
('Tecnologia'),
('Educação'),
('Entretenimento');

```
--Inserte tabelas de notícias
```sql
INSERT INTO noticias (nome) VALUES
('Tecnologia'),
('Educação'),
('Entretenimento');
```


```sql
INSERT INTO noticias
(titulo, resumo, texto, imagem, destaque, usuario_id, categoria_id) VALUES

(
    'Novas Tecnologia no dia a dia', 'A Tecnologias esta cada vez mais presentes na vida das pessoas',' As novas tecnologias ajudam a facilitar o cotidiano', 'tecnologia.jpg', 'sim',1,1),

( 'A importancia da educação','A educação é fundamental para o desenvolvimento da sociedade', 'Investir em educação é importante para criar varias oportunidades','noticias.jpg','sim',2,2),

 ('Novidades de Entretenimento' 'Filmes e series', 'O mundo do Entretedimento esta cada vez mais concorrido', 'entretedimento.jpg','nao',3,3),

 ('Tecnologia e inovação','Novas ferramentas estão surgindo','Atividades do dia mais praticos','Inovação.jpg', 'nao',3,3),

    (
    'Tecnologia nas escolas',
    'Tecnologia ajuda no aprendizado.',
    'O uso da tecnologia nas escolas pode auxiliar professores e alunos durante o processo de aprendizagem.',
    'escola-tecnologia.jpg',
    'nao',
    1,
    2
    );

```

## DELETE NA TABELA FORNECEDORES

```sql
## UPDATE na tabela usuarios
```sql
UPDATE usuarios SET nome = 'Ana Souza' WHERE id = 1;
```
```sql
UPDATE usuarios SET tipo = 'admin' WHERE id = 3;
```
## UPDATE na tabela categorias
```sql
UPDATE categorias SET nome = 'Diversão' WHERE id = 3;
```
## UPDATE na tabela noticias
```sql
UPDATE noticias SET titulo = 'Novas Tecnologias ' WHERE id = 1;
```
```sql
UPDATE noticias SET destaque = 'sim' WHERE id = 2;
```
```sql
UPDATE noticias SET categoria_id = 1 WHERE id = 4;
```
## DELETE na tabela de noticias
```sql
DELETE FROM noticias WHERE id = 4;
```
## DELETE na tabela de categorias
```sql
DELETE FROM categorias WHERE id = 3;
```
## DELETE na tabela de usuarios
```sql
DELETE FROM usuarios WHERE id = 3;

```






