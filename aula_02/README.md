## AULA 02 - Abrindo portas

# Chaves
- Chaves => São identificados e índices.
- Chave primária (PK) => É a chave principal de uma tabela, é um identificador único de cada entidade.
- Chave estrangeira => É uma chave que armazena uma referência a uma outra  tabela. Assim, não temos tabelas
com dados redundantes e conseguimos ligar diferentes tabelas.

# Cardinalidade de Relacionamentos
Cardinalidade => Diz respeito ao tipo de relacionamento desempenhado pelas entidades(tabelas).

- Cardinalidade - 1:1 => Ocorre quando uma entidade é referenciada apenas uma vez por outra. 
Ex: Quarto particular de hospital e paciente.

- Cardinalidade - 1:N => Ocorre quando 1 entidade é referenciada N vezes por outra.
EX: Médicos e departamento.

- Cardinalidade- N:N => Ocorre quando duas entidades possuem um relacionamento no qual elas se referenciam diversas vezes.
EX: Médicos e pacientes: Um médico atende mais de um paciente e um paciente pode ser atendido por mais de um médico.

# Tipos de Dados

* Inteiros
- tinyint
- smallint
- mediumint
˜ INT*
- bigint

* Decimais
- ponto fixo (numeric,DECIMAL*)
- ponto flutuante(FLOAT*, DOUBLE*)

* Strings
- CHAR*
- VARCHAR*
- text

* Datas
- DATE*
- datetime
- timestamp

# Material complementar:

* Documentação MySQL
  => https://dev.mysql.com/doc/refman/8.0/en/data-types.html