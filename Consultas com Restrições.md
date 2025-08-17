**04/08/2025**

**FILTRANDO E CLASSIFICANDO OS RESULTADOS DA CONSULTA (DISTINCT)**



Apesar de os dados de uma tabela ser exclusivos, ainda assim, uma consulta pode dar valores dispensáveis, vários filmes ou carros podem lançados no mesmo ano e tu so quereres os dados de um único filme. Para fazer essa filtragem  e selecionar uma consulta com dados exclusivos, e remover todas as outras linhas duplicadas usamos o ***DISTINCT***.

SELECT DISTINCT column, another\_column, …

FROM mytable

WHERE condition(s);



**ORDENAÇÃO DE RESULTADOS (ORDER BY)**



A adição de dados em bancos de dados reais, normalmente não ocorre em nenhuma ordem de coluna específica, então, pode ser difícil com o tempo ler e entender os resultados de uma consulta com milhares de linhas, para isso, o SQL usa a cláusula ***ORDER BY ASC/DESC***

SELECT column, another\_column, …

FROM mytable

WHERE condition(s)

ORDER BY column ASC/DESC;



**LIMITANDO OS RESULTADOS A UM SUBCONJUNTO (LIMIT \& OFFSET)**



LIMIT especifica o numero máximo de registros a serem retornados pela consulta. Exemplos, SELECT \* FROM produtos LIMIT 10 ( retorna os 10 primeiros produtos)

OFFSET especifica quanto registros devem ser ignorados antes de exibir os resultados

SELECT \* FROM produtos LIMIT 10 OFFSET 10 ( igonra os 10 primeiros produtos e retorna 10 produtos começano do 11º)

SELECT column, another\_column, …

FROM mytable

WHERE condition(s)

ORDER BY column ASC/DESC

LIMIT num\_limit OFFSET num\_offset;

