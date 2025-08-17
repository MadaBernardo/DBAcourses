**04/08/2025**

**QUERIES COM RESTIÇÕES parte 2**



Podemos usar alguns operadores em consultas com cláusula (WHERE), fazer comparações de dados  em colunas que contem dados como textos que não diferencia maiúsculas de minúsculas, strings não case-sensitive.



**OPERADORES CASE-SENSITIVE** 



* =	        coluna\_name = "abc"
* != or <>     coluna\_name != "abcd"



**OPERADORES CASE-INSENSITIVE**



* LIKE		coluna\_name LIKE "ABC"
* NOT LIKE	col\_name NOT LIKE "ABCD"
* **% (coringa)** usado como LIKE para apresentar padrões incluindo nenhum, todo que contém o carácter que buscas. Exemplo, %Jo%(joana, joão, feijoada, em qualquer posição)

&nbsp;  %jo, mostra tudo que termina com jo e jo% tudo que começa.

* \_ (**coringa**) usado com LIKE, procura um caráter especifico numa posição exata. Exemplo, \[\_jo termina com jo mas tem exatamente 1 caráter antes(Ajo, 1jo), jo\_ começa com jo mas tem exatamente 1 caráter depois(joa, joo, jo1)]
* IN verifica se o valor está em uma lista. Exemplo, WHERE Id IN (1, 5, 10), é o mesmo que Id= 1, Id= 5, Id= 10.
* NOT IN a mesma coisa que IN mas para valores que não existem nas listas citadas



Case sensitive distingue maiúsculas de minúsculas, texto != Texto != TEXTO, etc. Case insensitive não distingue, texto= Texto=TEXTO, mais usados em bancos de dados e pode ser reforçado com o Lower(). **Todas os caracteres devem ser posto em aspas para que o analisador de consultas possa fazer a distinção da string e das palavras chaves do SQL.**



**SELECT column, another\_column, …**

**FROM mytable**

**WHERE condition**

    **AND/OR another\_condition**

    **AND/OR …;**

