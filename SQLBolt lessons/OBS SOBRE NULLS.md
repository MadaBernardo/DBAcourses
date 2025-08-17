**OBS SOBRE NULLS**



É sempre bom ter **valores padrão apropriados para o tipo de dados**, como 0 para dados numéricos srings vazias para dados de texto. Mas tem vezes que o banco de dados vai precisar armezenar dados imcompletos **NULL**



**NULL não é zero ou string vazia, é ausência de valor.** **NULL não é igual a nada, nem a ele mesmo**

WHERE column = NULL  ❌

WHERE column != NULL ❌



IS NULL / IS NOT NULL

WHERE column IS NULL     ✅

WHERE column IS NOT NULL ✅



**Qualquer coisa somado com NULL é igual**



10 + NULL = NULL

'Hello' + NULL = NULL

-- Qualquer operação com NULL resulta em NULL



SELECT column, another\_column, …

FROM mytable

WHERE column IS/IS NOT NULL

AND/OR another\_condition

AND/OR …;

