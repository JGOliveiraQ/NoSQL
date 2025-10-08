# Os tipos de dados e regras na modelagem SQL <img src="https://cdn-icons-png.freepik.com/256/8263/8263251.png?semt=ais_white_label" alt="SQL" width="50"/>

Nesse artigo, vamos aprender como funciona os dados e as regras do SQL.

### O que seria o SQL?

O SQL é uma linguagem padrão que é utilizada para trabalhar com banco de dados relacionais, utilizada por muitos profissionais em diversas áreas, desde usuários de Excel até cientistas de dados. SQL 

## O que são tipos de dados SQL?

Em SQL, os tipos de dados são categorias que determinam o tipo de informação que cada coluna de uma tabela pode conter. Por exemplo, uma coluna pode armazenar números, textos, datas ou valores booleanos. Isso auxilia o banco de dados na organização e compreensão dos dados que você deseja armazenar.


<img width="579" height="482" alt="Captura de tela 2025-10-07 214020" src="https://github.com/user-attachments/assets/095c2327-bc6c-4850-8fb7-6e2010cf7865" />

## Como cada regra é aplicada:
Regra	Onde no modelo	O que garante
Integridade da Entidade	id_cliente INT PRIMARY KEY
id_pedido INT PRIMARY KEY	Garante que cada registro em clientes ou pedidos é identificado unicamente, e que a chave primária nunca será nula.
Integridade da Chave	email VARCHAR(150) UNIQUE	Evita duplicação de e-mail entre clientes — duas pessoas não podem ter o mesmo email.
Integridade Referencial	FOREIGN KEY (cliente_id) REFERENCES clientes(id_cliente)	Garante que cada pedido esteja associado a um cliente existente — não permite “pedido órfão”. O uso de ON DELETE CASCADE implica que, se um cliente for excluído, todos os seus pedidos sejam automaticamente excluídos, mantendo coerência.
