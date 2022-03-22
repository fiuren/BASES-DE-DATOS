 BASES DE DATOS

Se procede a crear una base de datos en MYSQL Workbench, donde se crea una bbdd con nombre "probas" y con una tabla "tbusuarios".

En ella se van a solicitar los siguientes datos.

1. Solicitar el saldo maximo con sexo M.
2. Listar el nombre y telefono de los usuarios con telefono NOKIA,BK o SONY.
3. Contar los usuarios sin saldo o inactivos.
4. Listar el login de los usuarios con nivel 1,2 o 3.
5. Listar los números de teléfono con saldo menos a 500.
6. Calcular la suma de saldos de los usuarios de la empresa telefónica NEXTEL.
7. Contar el número de usuarios por compañía telefónica.
8. Listar el login con usuarios con nivel 2.
9. Mostrar el email de los usuarios que usan gmail.
10. Lisatr nombre y telefono de los usuarios que tengan marca de telefono LG, SAMGUNG Y MOTOROLA.

Bloque 2

1. Listar nombre y telefono de los usuarios con telefono que no sea de la marca LG o SAMSUNG
   SELECT nombre, telefono FROM tblUsuarios WHERE marca NOT IN('LG', 'SAMSUNG');
2. Listar login y telefono de los usuarios con empresa telefonica IUSACELL.
   SELECT usuario, telefono FROM tblUsuarios WHERE compañia = 'IUSACELL';
3. Listar login y telefono de los usuarios con empresa telefonica DISTINTA A TELCEL.
   SELECT usuario, telefono FROM tblUsuarios WHERE compañia <> "TELCEL";
4. Mostrar el saldo medio de los usuarios que usen la marca NOKIA
   SELECT AVG(saldo) FROM tblUsuarios WHERE marca = 'NOKIA';
5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL
   SELECT usuario, telefono FROM tblUsuarios WHERE compañia IN('IUSACELL', 'AXEL');
6. Mostrar el email de los usuarios que no usan yahoo
   SELECT email FROM tblUsuarios WHERE email NOT LIKE '%yahoo.com';
7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL
   SELECT usuario, telefono FROM tblUsuarios WHERE compañia NOT IN('TELCEL', 'IUSACELL');
8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON
   SELECT usuario, telefono FROM tblUsuarios WHERE compañia = 'UNEFON';
9. Listar las diferentes marcas de celular en orden alfabético descendentemente
   SELECT DISTINCT marca FROM tblUsuarios ORDER BY marca DESC;
10. Listar las diferentes compañias en orden alfabético aleatorio
    SELECT DISTINCT compañia FROM tblUsuarios ORDER BY RAND();
11. Listar el login de los usuarios con nivel 0 o 2
    SELECT usuario FROM tblUsuarios WHERE nivel IN(0, 2);
12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG
    SELECT AVG(saldo) FROM tblUsuarios WHERE marca = 'LG';
