                   BASES DE DATOS

 Se procede a crear una base de datos en MYSQL Workbench, donde se crea una bbdd con nombre "probas" y con una tabla "tbusuarios".
 Para el primer bloque de consultas se adjunta una serie de capturas de pantalla para comprobar las soluciones

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

Bloque 3

  1   	# Listar el login de los usuarios con nivel 1 o 3
      	SELECT usuario FROM tblUsuarios WHERE nivel IN(1, 3);
      	                                        
  2   	# Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY
      	SELECT nombre, telefono FROM tblUsuarios WHERE marca <> "BLACKBERRY";
      	                                        
  3   	# Listar el login de los usuarios con nivel 3
      	SELECT usuario FROM tblUsuarios WHERE nivel = 3;
      	                                        
  4   	# Listar el login de los usuarios con nivel 0
      	SELECT usuario FROM tblUsuarios WHERE nivel = 0;
      	                                        
  5   	# Listar el login de los usuarios con nivel 1
      	SELECT usuario FROM tblUsuarios WHERE nivel = 1;
      	                                        
  6   	# Contar el número de usuarios por sexo 
      	SELECT sexo, COUNT(*) FROM tblUsuarios GROUP BY sexo;
      	                                        
  7   	# Listar el login y teléfono de los usuarios con compañia telefónica AT&T
      	SELECT usuario, telefono FROM tblUsuarios WHERE compañia = "AT&T";
      	                                        
  8   	# Listar las diferentes compañias en orden alfabético descendentemente
      	SELECT DISTINCT compañia FROM tblUsuarios ORDER BY compañia DESC;
      	                                        
  9   	# Listar el login de los usuarios inactivos
      	SELECT usuario FROM tblUsuarios WHERE NOT activo;
      	                                        
  10  	# Listar los números de teléfono sin saldo
      	SELECT telefono FROM tblUsuarios WHERE saldo <= 0;
      	                                        
  11  	# Calcular el saldo mínimo de los usuarios de sexo "Hombre"
      	SELECT MIN(saldo) FROM tblUsuarios WHERE sexo = 'H';
      	                                        
  12  	# Listar los números de teléfono con saldo mayor a 300
      	SELECT telefono FROM tblUsuarios WHERE saldo > 300;

Bloque 4

  1   	# Contar el número de usuarios por marca de teléfono
      	SELECT marca, COUNT(*) FROM tblUsuarios GROUP BY marca;
      	                                        
  2   	# Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG
      	SELECT nombre, telefono FROM tblUsuarios WHERE marca <> "LG";
      	                                        
  3   	# Listar las diferentes compañias en orden alfabético ascendentemente
      	SELECT DISTINCT compañia FROM tblUsuarios ORDER BY compañia ASC;
      	                                        
  4   	# Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON
      	SELECT SUM(saldo) FROM tblUsuarios WHERE compañia = 'UNEFON';
      	                                        
  5   	# Mostrar el email de los usuarios que usan hotmail
      	SELECT email FROM tblUsuarios WHERE email LIKE "%hotmail.com";
      	                                        
  6   	# Listar los nombres de los usuarios sin saldo o inactivos
      	SELECT nombre FROM tblUsuarios WHERE NOT activo OR saldo <= 0;
      	                                        
  7   	# Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o TELCEL
      	SELECT usuario, telefono FROM tblUsuarios WHERE compañia IN('IUSACELL', 'TELCEL');
      	                                        
  8   	# Listar las diferentes marcas de celular en orden alfabético ascendentemente
      	SELECT DISTINCT marca FROM tblUsuarios ORDER BY marca DESC;
      	                                        
  9   	# Listar las diferentes marcas de celular en orden alfabético aleatorio
      	SELECT DISTINCT marca FROM tblUsuarios ORDER BY RAND();
      	                                        
  10  	# Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON
      	SELECT usuario, telefono FROM tblUsuarios WHERE compañia IN('IUSACELL', 'UNEFON');
      	                                        
  11  	# Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA
      	SELECT nombre, telefono FROM tblUsuarios WHERE marca NOT IN('MOTOROLA', 'NOKIA');
      	                                        
  12  	# Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL
      	SELECT SUM(saldo) FROM tblUsuarios WHERE compañia = 'TELCEL';
