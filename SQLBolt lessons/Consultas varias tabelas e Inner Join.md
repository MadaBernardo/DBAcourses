**15/08/2025**

**Consultas de várias tabelas com JOINs E Normalização**



**NORMALIZAÇÃO DE BANCO DE DADOS** é útil para evitar dados duplicados e permitir o crescimento dos dados independentes uns dos outros. Em compensação surgem problemas como consultas mais complexas, desempenho por ter que trabalhar com muitas tabelas grandes.



**INNER JOIN... ON** combinamos dados de linha em duas tabelas diferentes por meio da chave única. As linhas partilham as mesmas chaves. Essa cláusula é uma junção interna e funciona melhor em tabelas que têm asmesmas chaves. Retorna correspondência exatas.

**SELECT column, another\_table\_column, …**

**FROM mytable**

**INNER JOIN another\_table** 

    **ON mytable.id = another\_table.id**

**WHERE condition(s)**

**ORDER BY column, … ASC/DESC**

**LIMIT num\_limit OFFSET num\_offset;**



 **OUTER JOINs** a relação entre tabelas não depende de uma chave formal, mas sim de uma coluna relacionável que pode ser qualquer campo com valores correspondentes.

**1.LEFT JOIN** retorna todos os dados da tabela a esquerda, mesmo sem existência de primary ou foreigh key.

**2.RIGTH JOIN** retorna todos dados da tabela a esquerda, mesmo sem existência de primary ou foreigh key.

**1.FULL JOIN** retorna todos dados de ambas tabelas, mesmo sem existência de primary ou foreigh key.

SELECT column, another\_column, …

FROM mytable

INNER/LEFT/RIGHT/FULL JOIN another\_table 

&nbsp;   ON mytable.id = another\_table.matching\_id

WHERE condition(s)

ORDER BY column, … ASC/DESC

LIMIT num\_limit OFFSET num\_offset;



INNER JOIN: "Quero apenas o que existe em ambas"

LEFT JOIN: "Quero todos da primeira tabela, mesmo sem par, mostra tudo da tabela a esquerda"

RIGHT JOIN: "Quero todos da segunda tabela, mesmo sem par, mostra tudo da tabela a direita"

FULL JOIN: "Quero tudo de todos, com ou sem par"

