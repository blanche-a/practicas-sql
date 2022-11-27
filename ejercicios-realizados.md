1. Listar los nombres de los usuarios
``` sql
SELECT nombre FROM Usuarios;
```
2. Calcular el saldo máximo de los usuarios de sexo “Mujer”
``` sql
SELECT MAX(saldo) FROM Usuarios WHERE sexo='M';
```
3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY
``` sql
SELECT nombre,telefono FROM Usuarios WHERE marca IN('NOKIA','BLACKBERRY','SONY');
```
4. Contar los usuarios sin saldo o inactivos
``` sql
SELECT COUNT(usuario) FROM Usuarios WHERE saldo = 0 OR activo = 0;
```
5. Listar el login de los usuarios con nivel 1, 2 o 3
``` sql
SELECT usuario FROM Usuarios WHERE nivel BETWEEN 1 AND 3;
```
6. Listar los números de teléfono con saldo menor o igual a 300
``` sql
SELECT telefono FROM Usuarios WHERE saldo <= 300;
```
7. Calcular la suma de los saldos de los usuarios de la compañía telefónica NEXTEL
``` sql
SELECT SUM(saldo) FROM Usuarios WHERE compania = 'NEXTEL';
```
8. Contar el número de usuarios por compañía telefónica
``` sql
SELECT compania,COUNT(*) FROM Usuarios GROUP BY compania;
```
9. Contar el número de usuarios por nivel
``` sql
SELECT COUNT(usuario),nivel FROM Usuarios GROUP BY nivel;
```
10. Listar el login de los usuarios con nivel 2
``` sql
SELECT usuario FROM Usuarios WHERE nivel = 2;
```
11. Mostrar el email de los usuarios que usan gmail
``` sql
SELECT email FROM Usuarios WHERE email LIKE '%gmail.com';
```
12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA
``` sql
SELECT nombre,telefono FROM Usuarios WHERE marca IN('LG','MOTOROLA','SAMSUNG');
```
13. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG
``` sql
SELECT nombre,telefono FROM Usuarios WHERE marca NOT IN('LG','SAMSUNG');
```
14. Listar el login y teléfono de los usuarios con compañía telefónica IUSACELL
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania = 'IUSACELL';
```
15. Listar el login y teléfono de los usuarios con compañía telefónica que no sea TELCEL
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania NOT IN('TELCEL');
```
16. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA
``` sql
SELECT AVG(saldo) FROM Usuarios WHERE marca = 'NOKIA';
```
17. Listar el login y teléfono de los usuarios con compañía telefónica IUSACELL o AXEL
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania IN('IUSACELL','AXEL');
```
18. Mostrar el email de los usuarios que no usan yahoo
``` sql
SELECT email FROM Usuarios WHERE email NOT LIKE '%yahoo.com';
```
19. Listar el login y teléfono de los usuarios con compañía telefónica que no sea TELCEL o IUSACELL
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania NOT IN('TELCEL','IUSACELL');
```
20. Listar el login y teléfono de los usuarios con compañía telefónica UNEFON
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania = 'UNEFON';
```
21. Listar las diferentes marcas de celular en orden alfabético descendentemente
``` sql
SELECT DISTINCT marca FROM Usuarios ORDER BY marca DESC;
```
22. Listar las diferentes compañías en orden alfabético aleatorio
``` sql
SELECT DISTINCT marca FROM Usuarios ORDER BY RAND();
```
23. Listar el login de los usuarios con nivel 0 o 2
``` sql
SELECT usuario FROM Usuarios WHERE nivel IN('0','2');
```
24. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG
``` sql
SELECT AVG(saldo) FROM Usuarios WHERE marca = 'LG';
```
25. Listar el login de los usuarios con nivel 1 o 3
``` sql
SELECT usuario,nivel FROM Usuarios WHERE nivel IN('1','3');
```
26. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY
``` sql
SELECT nombre,telefono FROM Usuarios WHERE marca != 'BLACKBERRY';
```
27. Listar el login de los usuarios con nivel 3
``` sql
SELECT usuario FROM Usuarios WHERE nivel = '3';
```
28. Listar el login de los usuarios con nivel 0
``` sql
SELECT usuario FROM Usuarios WHERE nivel = '0';
```
29. Listar el login de los usuarios con nivel 1
``` sql
SELECT usuario FROM Usuarios WHERE nivel = '1';
```
30. Contar el número de usuarios por sexo
``` sql
SELECT COUNT(usuario),sexo FROM Usuarios GROUP BY sexo;
```
31. Listar el login y teléfono de los usuarios con compañía telefónica AT&T
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania = 'AT&T';
```
32. Listar las diferentes compañías en orden alfabético descendentemente
``` sql
SELECT DISTINCT compania FROM Usuarios ORDER BY compania DESC;
```
33. Listar el login de los usuarios inactivos
``` sql
SELECT usuario FROM Usuarios WHERE activo = '0';
```
34. Listar los números de teléfono sin saldo
``` sql
SELECT telefono FROM Usuarios WHERE saldo = '0';
```
35. Calcular el saldo mínimo de los usuarios de sexo “Hombre”
``` sql
SELECT MIN(saldo) FROM Usuarios WHERE sexo = 'H';
```
36. Listar los números de teléfono con saldo mayor a 300
``` sql
 SELECT telefono FROM Usuarios WHERE saldo > 300;
```
37. Contar el número de usuarios por marca de teléfono
``` sql
SELECT COUNT(usuario),marca FROM Usuarios GROUP BY marca;
```
38. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG
``` sql
SELECT nombre,telefono FROM Usuarios WHERE marca !='LG';
```
39. Listar las diferentes compañías en orden alfabético ascendentemente
``` sql
SELECT DISTINCT compania FROM Usuarios ORDER BY compania ASC;
```
40. Calcular la suma de los saldos de los usuarios de la compañía telefónica UNEFON
``` sql
SELECT SUM(saldo) FROM Usuarios WHERE compania = 'UNEFON';
```
41. Mostrar el email de los usuarios que usan hotmail
``` sql
SELECT email FROM Usuarios WHERE email LIKE '%hotmail.com';
```
42. Listar los nombres de los usuarios sin saldo o inactivos
``` sql
SELECT usuario FROM Usuarios WHERE saldo = '0' OR activo = '0';
```
43. Listar el login y teléfono de los usuarios con compañía telefónica IUSACELL o TELCEL
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania IN('IUSACELL','TELCEL');
```
44. Listar las diferentes marcas de celular en orden alfabético ascendentemente
``` sql
SELECT DISTINCT marca FROM Usuarios ORDER BY marca ASC;
```
45. Listar las diferentes marcas de celular en orden alfabético aleatorio
``` sql
SELECT DISTINCT marca FROM Usuarios ORDER BY RAND();
```
46. Listar el login y teléfono de los usuarios con compañía telefónica IUSACELL o UNEFON
``` sql
SELECT usuario,telefono FROM Usuarios WHERE compania IN('IUSACELL','UNEFON');
```
47. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA
``` sql
SELECT nombre,telefono,marca FROM Usuarios WHERE marca NOT IN('MOTOROLA','NOKIA');
```
48. Calcular la suma de los saldos de los usuarios de la compañía telefónica TELCEL
``` sql
SELECT SUM(saldo) FROM Usuarios WHERE compania ='TELCEL';
```

# JOIN
1. ¿Qué provincias no tenemos clientes?
``` sql
SELECT provincias.nombre FROM clientes RIGHT JOIN provincias ON clientes.codigoProvincia = provincias.codigo WHERE clientes.codigoProvincia IS NULL;
```
2. ¿Qué provincias tienen clientes? Pero sin repetir el nombre de la provincia. Un tip, vas a necesitar la sentencia distinct
``` sql
SELECT DISTINCT provincias.nombre FROM clientes JOIN provincias ON clientes.codigoProvincia = provincias.codigo;
```
