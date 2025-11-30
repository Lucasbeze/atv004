📚 Projeto Lógico e Manipulação de Dados (DML) – Livraria Saber

Este repositório contém o Projeto Lógico (DDL) e os scripts de manipulação de dados (DML) desenvolvidos para o minimundo Livraria Saber.

O objetivo é criar um banco de dados relacional robusto, garantindo integridade, desempenho e consistência nas operações envolvendo clientes, vendedores, fornecedores, produtos (livros e papelaria) e transações de vendas.

🚀 Visão Geral do Projeto
1. Modelo Lógico e Normalização

O modelo foi elaborado seguindo rigorosamente os princípios da Terceira Forma Normal (3FN), eliminando redundâncias e dependências transitivas.

🔹 Estrutura Geral:

O banco possui 6 principais entidades: CLIENTE, VENDEDOR, FORNECEDOR, LIVRO, PAPELARIA, EDITORA.

Conta também com:

Uma tabela associativa LIVRO_AUTOR para resolver o relacionamento N:N.

A tabela ITEM_VENDA para armazenar os itens comprados em cada venda.

A tabela VENDA, que registra dados da transação.

🔹 Integridade Referencial:

Estruturado com chaves estrangeiras que impedem dados órfãos e mantêm o modelo sempre consistente.

🔹 Decisão de Denormalização Tática:

A tabela VENDA inclui o campo valor_total, reduzindo processamento em relatórios e evitando recálculos frequentes.

2. Diagrama Entidade‑Relacionamento (DER)

📌 Link diagrama:
➡️ https://dbdiagram.io/d/692c6a80d6676488baf6468f

O diagrama representa visualmente todas as entidades, atributos, relacionamentos e cardinalidades do sistema da Livraria Saber.

📦 Estrutura do Repositório

O projeto está organizado em três arquivos principais, correspondentes às etapas de desenvolvimento e manipulação:

Arquivo	Conteúdo	Etapa
01_ddl_criacao_tabelas.sql	CREATE TABLE, PRIMARY KEY, FOREIGN KEY	Projeto Lógico (DDL)
02_dml_insercao_consulta.sql	INSERT INTO (povoamento) + SELECT (consultas)	Manipulação Sprint 2
03_dml_manipulacao.sql	UPDATE, DELETE e testes de integridade	Manipulação Sprint 3
⚙️ Instruções para Execução

Para executar este projeto será necessário:

Pré‑requisitos

MySQL Server ou MariaDB

Cliente SQL como MySQL Workbench, DBeaver, HeidiSQL, etc.

Passo a Passo
1. Criar o Schema

No MySQL Workbench, execute:

CREATE DATABASE livraria_saber;
USE livraria_saber;
2. Executar o Script DDL

Rode o arquivo:

01_ddl_criacao_tabelas.sql

Isso criará todas as tabelas e relacionamentos.

3. Popular o Banco e Consultar Dados

Execute:

02_dml_insercao_consulta.sql

Aqui são inseridos clientes, produtos, autores, papelaria, fornecedores, editoras, vendas e itens.

4. Manipulação e Testes de Integridade

Execute:

03_dml_manipulacao.sql

Inclui UPDATE, DELETE, remoção segura com restrições e validações.

🧩 Modelo Conceitual – Entidades Principais

CLIENTE – Dados pessoais e contatos

VENDEDOR – Informações de funcionário e comissão

FORNECEDOR – Origem dos produtos

EDITORA – Ligada aos livros

LIVRO – Título, ISBN, preço, estoque, editora

PAPELARIA – Produtos gerais (marca, categoria, fornecedor)

LIVRO_AUTOR – Associação N:N entre livros e autores

ITEM_VENDA – Itens pertencentes à venda

VENDA – Registro completo da compra


👤 Autor

Lucas Bezerra da Silva
