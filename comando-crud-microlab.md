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

 ('Tecnologia e inovação','Novas ferramentas estão surgindo','Atividades do dia mais praticos','Inovação.jpg', 'nao',1,1);

    


```






```