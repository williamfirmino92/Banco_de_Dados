## AULA 08 - Mais informações

# AGREGAÇÃO SOMA E CONTAGEM
=> CONTAR,SOMAR,AGRUPAR os resultados.
* SOMA
SELECT
  customer_id,
  SUM(amount)
FROM payment
GROUP BY
  customer_id;

* CONTAGEM
SELECT
  customer_id,
  COUNT(customer_id)
FROM payment
GROUP BY
  customer_id;

# FILTROS EM AGREGAÇÃO - HAVING
=> Como o WHERE acontece antes do SELECT não podemos utilizá-lo!
EX:
SELECT
  customer_id,
  SUM(customer_id)
FROM payment
GROUP BY customer_id
HAVING SUM(amount) > 100;
-
SELECT
  customer_id,
  COUNT(customer_id)
FROM RENTAL
GROUP BY customer_id
HAVING
  count(customer_id) > 10;

# LIMITANDO RESULTADOS
* Utilizamos a palavra LIMITE.
* Podemos utilizar OFFSET para dizer a partir de qual registro a contagem do limite começa.
EX:
SELECT
  *
FROM
  film
LIMITE 30;

# CONDICÕES E CLASSIFICACÕES 
* Utilizamos a expressão CASE.

# Material complementar:
