## Banco de Dados

🚀  CRUD - CREATE, READ, UPDATE, DELETE

- NOT NULL => Obriga que o atributo tenha algum dado,
- UNSIGNED => É um valor sem sinal,
- UNIQUE => Não aceita duplicidade,
- ENUM => Valores já pré-definidos,

# CREATE

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

---------------------------------------------------------------------------------------
# UPDATE

UPDATE estados SET nome = 'Maranhão' WHERE sigla = 'MA';
---------------------------------------------------------------------------------------
# DELETE

DELETE FROM estados WHERE sigla = 'AC'
---------------------------------------------------------------------------------------
# READ
- Quero dar um apelido para a coluna nome.

- Quero que seja exibido os estados da regiao Sul e a sua sigla.
nome = > Nome do Estado.
SELECT sigla, nome AS 'Nome do Estado' FROM estados WHERE regiao = 'Sul';

* Selecionar os estados da tabela estados onde a população é igual ou superior a 10 milhões.
SELECT nome FROM estados WHERE populacao >= 10.00;

* Selecionar os estados da tabela estados onde a população é igual ou superior a 10 milhões por ordem DESCENDENTE

ORDER BY - Ordenador por
ASC => menor para o maior
DESC => maior para o menor

1. Consulta agregada
Total de habitantes do pais Brasil - POPULAÇÃO DO BRASIL.

SUM() => SELECT SUM(populacao) AS 'POPULAÇÃO DO BRASIL' FROM estados;

A media de população por estado;
AVG() => 
207.67
----------------------------------------------------------------------
# DROP X TRUNCATE

TRUNCATE TABLE estados;
----------------------------------------------------------------------
# APELIDOS PARA AS TABELAS E COLUNAS
- COLOCANDO AS DEPOIS DO NOME DA TABELA/COLUNA.
- APENAS COLOCANDO O APAELIDO APÓS O NOME DA TABLE/COLUNA.

----------------------------------------------------------------------
# FILTRAGEM MÚLTIPLA
SELECT
FROM
WHERE

-- id = 3 e id = 7.
SELECT nome FROM estados WHERE id = 3 AND id =
----------------------------------------------------------------------
# FILTRAGEM MÚLTIPLA 2
AND - E.
OR - OU.

SELECT nome FROM estados WHERE regiao = 'Norte' AND populacao < 8.00;
----------------------------------------------------------------------
# OPERADOR NOT

- Consulta devolve qualquer dado que não tenha a negação
SELECT nome AS 'ESTADOS NÃO SUDESTE' FROM estados WHERE NOT regiao = 'Sudeste';
----------------------------------------------------------------------
# BETWEEN - ENTRE
=> NOS FORNECE A CAPACIDADE DE FILTRAR BUSCANDO PADROES EM INTERVALOS.

SELECT nome 'ESTADOS ABAIXO DE 3.00' FROM estados WHERE populacao BETWEEN 0.50 AND 3.00; 
----------------------------------------------------------------------
# DIFERENTE <>
=> É utilizado quando queremos valores diferentes

SELECT nome AS 'ESTADOS NÃO SUDESTE' FROM estados WHERE regiao <> 'Sudeste'
----------------------------------------------------------------------
# OPERADOR IN
=> Promove a comparação com uma dada lista de valores.

SELECT * FROM actor WHERE first_name IN('Penelope', 'Nick', 'ED');
----------------------------------------------------------------------
# OPERADOR LIKE
=> Promove a comparação com a capacidade de utilizar caracteres curingas.

1. _ => substituir apenas um caracter
-- Imprimir na tela todos os dados da tabela actor onde o first_name seja parecido '_enelope'.

SELECT * FROM actor WHERE first_name LIKE '_enelope.'

2. % => substituir qualquer quantidade de caracteres.
-- NICK - %CK

SELECT * FROM actor WHERE first_name LIKE '%CK'
----------------------------------------------------------------------
# DISTINCT - DIFERENTES REGISTROS
=> Para saber quais são as entradas únicas em um banco de dados.
SELECT DISTINCT first_name FROM actor
----------------------------------------------------------------------
# ORDER BY 
=> Para ordenar os resultados de uma coluna.

ASC => menor para o maior
DESC => maior para o menor

* EXIBIDO OS PRIMEIROS NOMES DOS ATORES/ATRIZES EM ORDEM, DESC

SELECT first_name FROM actor ORDER BY first_name DES
----------------------------------------------------------------------
# MÍNIMO E MÁXIMO
=> MÁXIMO - Retornar um valor máximo em uma tabela.
-SELECT MAX(amount) FROM payment;
=> MÍNIMO - Retornar um valor mínimo em uma tabela.
SELECT MIN(amount) FROM payment;
----------------------------------------------------------------------

01 - SELECT * FROM customer WHERE first_name LIKE 'P%'.
=> 
02 - Quais clientes se chamam Penelope, John, Maria ou Barbara
=> 
SELECT * FROM customer WHERE first_name IN ('PENELOPE', 'JOHN', 'MARIA', 'BARBARA');






















