**Introdução ao SQL- 03/08/2025**



SQL é uma linguagem que permite o usuário consultar, manipular e transformar dados de um banco de dados relacional. ao aprender SQL, o objetivo é apender a responder a perguntas específicas para ajudar a tomar boas decisões no futuro.



Tabelas: Entidades(um modelo)

Colunas: Atributos (As caraterísticas da entidade)

Linhas: Instâncias (A verdadeira informação que está nos atributos, o dado real que preenche o modelo)



**Consultas SQL**



Uma Consulta é uma instrução que declara o que estamos a procura, onde procurar e possivelmente, como transformar essa informação antes de obtê-la. A sua sintaxe é ***SELECT***

Para selecionar toda informação de uma tabela usamos:

SELECT \*          ou     SELECT nameColuna (para info. de colunas específicas)

FROM nametable           FROM nameTable



**Consultas com Restrições 1**



Se não quisermos ter acesso a todas as informações de uma coluna de uma vez, devemos usar uma cláusula na consulta. Essa é aplicada a cada linha de dados verificando os valores na coluna escolhida para saber se aquela linha deve ser incluída na consulta ou não, permite que a  consulta seja mais rápida devido a redução de dados desnecessários. A sintaxe é ***WHERE***

SELECT coluna, outraColuna

FROM nameTable

WHERE condição

AND/OR outra condição

AND/OR …



**OPERADORES PARA CONDIÇÕES**



=, !=, <, <=, >, >=	Standard numerical operators	col\_name != 4

BETWEEN … AND …	     Number is within range of two values (inclusive)	col\_name BETWEEN 1.5 AND 10.5



NOT BETWEEN … AND …	Number is not within range of two values (inclusive)	col\_name NOT BETWEEN 1 AND 10

IN (…)	Number exists in a list	col\_name IN (2, 4, 6)

NOT IN (…)	Number does not exist in a list	col\_name NOT IN (1, 3, 5)

