## AULA 03 - E nasceu!

# MySQK workbench
(Estamos utilizando o phpmyadmin)

# dbDiagram
=> É uma ferramente para auxiliar na criação de esquemas de banco de dados.

# CRUD - CREATE/CRIAÇÃO
* CRIANDO A DATABSE(BANCO DE DADOS)
=> CREATE DATABASE `NOME DO BANCO`

* CRIANDO A TABELA(ENTIDADE)
-- Criando a tabela Estados
create table estados (
    id INT PRIMARY KEY NOT NULL ,
    nome VARCHAR(45) NOT NULL,
    sigla VARCHAR(2) NOT NULL,
    regiao EVARCHAR(45) NOT NULL ,
    populacao DECIMAL(5,2) NOT NULL,
);

# CRUD - DELETE/DELEÇÃO
* DELETANO A DATABASE
=> DROP DATABASE `NOME DO BANCO`

* DELETANDO UMA TABLE
=> DROP TABLE `NOME DO BANCO`
