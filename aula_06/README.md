## AULA 06 - Ih, pra onde foi?

# CRUD - DELETE/DELEÇÃO
* REMOVER REGISTROS DO BANCO DE DADOS
DELETE
FROM fornecedor
WHERE nome LIKE 'Mister lanches';

# DROP x TRUNCATE
* TRUNCANTE REMOVE TODOS OS DADOS DA TABELA
TRUNCATE TABLE fornecedor;

# CRUD - READ/LEITURA
SELECT
  endereco,
  nome
FROM
  fornecedor;

# APELIDOS PARA AS TABELAS E COLUNAS
* COLOANDO AS OU APENAS COLOCANDO O `APELIDO` APÓS A COLUNA OU TABELA.
SELECT
  endereco AS endereco_fornecedor
FROM
  fornecedor;
- OU
SELECT
  endereco endereco_fornecedor
FROM
  fornecedor;

# FILTRAGEM
* UTILIZAMDO O WHERE(ONDE)
SELECT
  *
FROM
  fornecedor
WHERE
  id = 1;

# FILTRAGEM MÚLTIPLA
* UTILIZAMDO O WHERE(ONDE)
SELECT
  *
FROM
  fornecedor
WHERE
  id = 1
  OR id = 3;

# OPERADOR NOT
* NEGAÇÃO DE UMA CONDIÇÃO
SELECT
  *
FROM
  actor
WHERE
  NOT first_name = 'Penelope'


# Material complementar:

* LEI GERAL DE PROTEÇÃO DE DADOS PESSOAIS - LGPD
  => https://pt.wikipedia.org/wiki/Lei_Geral_de_Prote%C3%A7%C3%A3o_de_Dados_Pessoais

