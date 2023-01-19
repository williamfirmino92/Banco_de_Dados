# Banco_de_Dados

## CRUD - CREATE, READ, UPDATE, DELETE

- NOT NULL => Obriga que o atributo tenha algum dado,
- UNSIGNED => É um valor sem sinal,
- UNIQUE => Não aceita duplicidade,
- ENUM => Valores já pré-definidos,

* Criação da tabela estados
CREATE TABLE estados (
	id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    nome VARCHAR(45) NOT NULL,
    sigla VARCHAR(2) NOT NULL,
    regiao ENUM('Norte', 'Nordeste', 'Centro-Oeste', 'Sudeste', 'Sul') NOT NULL,
    populacao DECIMAL(5,2) NOT NULL,
    PRIMARY KEY(id),
    UNIQUE KEY (nome),
    UNIQUE KEY (sigla)
);
