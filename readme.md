# Construye las siguientes consultas:

• Aquellas usadas para insertar, modificar y eliminar un Customer, Staff y Actor.

## Customer : agregar , eliminar y actiualizar

```sql
/* Insertar nuevo Customer puesto 600*/
INSERT INTO
	customer( store_id,first_name,last_name,email,address_id,activebool,active)
VALUES
	(2,'Pedro','Picapiedra','pedro@sakilacustomer.com',605,'t',1);

/*Modificar Customer el email de pedro@sakilacustomer.com a pablo@sakilacustomer.com*/

UPDATE customer SET email = 'pablo@sakilacustomer.com' WHERE customer_id = 600;

/*Eliminar Customer elimine el creado por mi con el customer_id =  600*/

DELETE FROM customer WHERE customer_id = 600;

```

## Staff : agregar , eliminar y actiualizar

```sql
/* Insertar nuevo staff */
INSERT INTO
	staff( first_name,last_name,address_id,email,store_id,active,username,password)
VALUES
	('Alejandro','Perez',5,'alejandro@sakilastaff.com',3,'t','Shaoran','8cb2237d0679ca88db6464eac60da97487597545');

/*Modificar Staff el username de shaoran a shaoran el loco*/

UPDATE staff SET username = 'Shaoran el loco' WHERE staff_id = 3;

/*Eliminar Staff elimine el creado por mi con el staff_id =  3*/

DELETE FROM staff WHERE staff_id = 3;

```

## Actor : agregar , eliminar y actiualizar

```sql
/* Insertar nuevo Actor puesto 201 */
INSERT INTO
	actor( first_name,last_name)
VALUES
	('Firifilfolfino','Gutierrez');

/*Modificar Actor  el first_name de Firifilfolfino a Pedro*/

UPDATE actor SET first_name = 'Pedro' WHERE actor_id = 201;

/*Eliminar Actor  elimine el creado por mi con el staff_id =  3*/

DELETE FROM actor WHERE actor_id = 201;

```

## • Listar todas las “rental” con los datos del “customer” dado un año y mes.

```sql


```

## • Listar Número, Fecha (payment_date) y Total (amount) de todas las “payment”.

```sql
SELECT
	  payment_id AS lista_numero,
	  payment_date :: DATE AS fecha,
	  amount AS total
FROM
	  payment
;

```

## • Listar todas las “film” del año 2006 que contengan un (rental_rate) mayor a 4.0.

```sql
SELECT
	film_id,
	title,
	rental_rate,
	release_year
FROM
	film
WHERE
	rental_rate >= '4.00'
;

```
