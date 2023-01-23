## AULA 01 - Suas consultas

# BETWEEN
=> Nos fornece a capacidade de filtrar buscando padrões em intervalos. 
EX: 
SELECT
  *
FROM
  actor
WHERE
  actor_id BETWEEN 13 AND 115;

# DIFERENTE DE <>
=> Utilizado quando queremos valores diferentes de.
EX:
FROM  
  actor
WHERE
  first_name <> 'Penelope';

# OPERADOR IN
=> Promove a comparação com uma dada lista de valores.
EX:
SELECT
  *
FROM
  actor
WHERE
  first_name IN ('Penelope', 'Nick', 'ED');

# OPERADOR LIKE
* Promove a comparação com a capacidade de utilizar caracteres curingas.
* _: Substitui apenas um caracter
* %: Substitui qualquer quantidade de caracteres
EX:
SELECT
  *
FROM
  actor
WHERE
  first_name LIKE '_enelope'
  OR first_name LIKE '%ck';

# DISTINCT - DIFERENTES REGISTROS
* Para saber quais são as entradas únicas em um banco de dados.
EX:
SELECT
  DISTINCT first_name
FROM
  actor;

# ORDENANDO RESULTADOS - ORDER BY
* Para ordenar os resultados de uma query utilizamos ORDER BY.
EX:
SELECT
  first_name
FROM
  actor
ORDER BY
  first_name DESC;

# MÍNIMO E MÁXIMO
* Retorna um valor máximo em uma tabela MAX()
EX:
SELECT
  MAX(valor)
FROM
  vendas;
-
EX: 
SELECT
  MIN(amount)
FROM
  payment;
