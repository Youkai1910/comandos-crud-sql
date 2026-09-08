# Exercícios Microblog CRUD 

## usuarios
```sql
INSERT INTO usuarios(nome, email, senha, tipo) VALUES 
    ('Ana Silva','ana@email.com','123abc','editor'),
    ('Bruno Souza','bruno@email.com','abc456','admin'),
    ('Carla Mendes','carla@email.com','789xyz','editor');
```
## categorias
```sql
INSERT INTO categorias(nome) VALUES 
('Tecnologia'),
('Educação'),
('Entretenimeto');
```
## noticias
```sql
INSERT INTO noticias(titulo, resumo, texto, destaque, imagem, usuario_id, categoria_id) VALUES
('Novas Tecnologia mudam o dia a dia',
'As novas tecnologias estão redefinindo profundamente o nosso cotidiano', 'transformando radicalmente a forma como trabalhamos, nos comunicamos, aprendemos e cuidamos da saúde. O avanço da inteligência artificial (IA), da automação e da conectividade global acelerou essa transição, tornando tarefas complexas mais acessíveis e integradas à nossa rotina diária.',
'sim',
'tecnologia.jpg',
1,
1),

('A Educação Salva o Futuro',
'A educação de qualidade é o pilar central para transformar a sociedade', 'salvar o futuro e moldar as próximas gerações frente às rápidas mudanças globais. Em um mundo cada vez mais digital, o papel do ensino vai muito além da memorização: ele desenvolve o pensamento crítico, a empatia e a capacidade de adaptação necessárias para os desafios que vêm pela frente.',
'nao',
'educacao.jpg',
3,
2),
('O Entretenimento Pra Saúde',
'O entretenimento exerce um papel terapêutico fundamental na saúde', 'atuando diretamente no bem-estar físico, mental e emocional das pessoas. Longe de ser apenas uma distração ou perda de tempo, o lazer e as atividades recreativas ajudam a regular o sistema nervoso, reduzem o estresse e estimulam funções cognitivas vitais.',
'nao',
'entretenimento.jpg',
2,
3),
('Senac 2027',
'Senac tem novos cursos para 2027',
'Cursos do Senac são bons e tem em varias expecialidades',
'sim',
'senac.jpg',
3,
2);
```

----

## UPDATE na tabela usuarios
```sql
UPDATE usuarios 
SET nome = 'Ana Silva Souza' 
WHERE id = 1;
```
```sql
UPDATE usuarios 
SET tipo = 'admin' 
WHERE id = 3;
```
## UPDATE na tabela categorias
```sql
UPDATE categorias 
SET nome = 'Entretenimento e Lazer' 
WHERE id = 3;
```
## UPDATE na tabela noticias
```sql
UPDATE noticias 
SET titulo = 'Novas Tecnologias mudam o dia a dia de todos' 
WHERE id = 1;
```
```sql
UPDATE noticias 
SET destaque = 'sim' WHERE id = 2;
```
```sql
UPDATE noticias 
SET categoria_id = 1 WHERE id = 4;
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
DELETE FROM usuarios WHERE id = 2;
```


