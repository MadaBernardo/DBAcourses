17/08/2025

**(QUERIES) CONSULTAS COM EXPRESSÕES**



Usamos expressões em consultas para escrever uma lógica mais complexa em valores de coluna. Essas expressões podem usar matemática e funções de string junto com aritmética básica para transformar valores quandoa consulta é executada. Exemplo:

SELECT particle\_speed / 2.0 AS half\_particle\_speed

FROM physics\_data

WHERE ABS(particle\_position) \* 10.0 > 500;



O uso dessas expressões podem economizar tempo e pós-processamento extra de dados , mas também pode tornar a consulta mais difícil de ker. Por isso, aconselha-se o uso de **ALIAS**, usando a palavra-chave **SELECT AS**. Exemplo:

SELECT col\_expression AS expr\_description, …

FROM mytable;



Colunas muito usadas e até tabelas também podem ter ALIASES para tornar mais fácil para referenciar e simplificar as consultas mais complexas.

SELECT column AS better\_column\_name, …

FROM a\_long\_widgets\_table\_name AS mywidgets

INNER JOIN widget\_sales

&nbsp; ON mywidgets.id = widget\_sales.widget\_id;

