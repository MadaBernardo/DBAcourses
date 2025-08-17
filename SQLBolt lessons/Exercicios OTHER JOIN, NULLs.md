**OTHER JOIN**

1\. Find the list of all buildings that have employees



SELECT DISTINCT Building\_name

FROM Buildings

LEFT JOIN Employees

ON Buildings.Building\_name = Employees.Building

WHERE Employees.Building IS NOT NULL;



2\. Find the list of all buildings and their capacity



SELECT Building\_name, Capacity

FROM Buildings;



3\. List all buildings and the distinct employee roles in each building (including empty buildings)



SELECT DISTINCT Building\_name, Role

FROM Buildings

LEFT JOIN Employees

ON  Buildings.Building\_name = Employees.Building;



**DISTINCT garante que cada combinação de dados aperece só uma vez na consulta mesmo que estja repetido várias vezes na tabela.**



**NULLs**



1.Find the name and role of all employees who have not been assigned to a building

SELECT Name, Role

FROM Employees

LEFT JOIN Buildings

ON Employees.Building = Buildings.Building\_name

WHERE Employees.Building IS NULL;



2.Find the names of the buildings that hold no employees

SELECT Building\_name

FROM Buildings

LEFT JOIN Employees

ON Employees.Building = Buildings.Building\_name

WHERE Employees.Building IS NULL;

