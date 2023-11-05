## Llaves
Para hacer los joins entre las tablas es importante establecer la llave foránea que no es más que la representación de una fila de otra tabla en la que estamos creando

```sql
create table products(
	id int primary key,
	created_by int,
	name varchar(100),
	marca varchar(100),
	foreign key(created_by) references usuarios(id)
);
```

## Left Join
Suponiendo que en la tabla de arriba created_by contenga el id del usuario creador del producto, el left join lo que hará en nuestra consulta será traer todos los usuarios con sus productos creados y si este usuario no tiene productos en la columna de productos aparecerá null pero el usuario seguirá apareciendo.

```sql
--En la directiva on se ponen las propiedades de las tablas por las cuales
--se van a enlazar en este caso el id del usuario y created_by de producto
select u.id, u.email, p.name from usuarios u
left join product p on u.id = p.created_by
```

## Right join
Es lo mismo que **left join** pero con la tabla de la derecha. En este caso se toma la tabla de productos como la tabla principal, por lo que aparecerán todos los productos registrados en esa tabla ya que todos deberían de tener asociado como llave foranea un usuario

```sql
select u.id, u.email, p.name from usuarios u
right join product p on u.id = p.created_by
```

## Inner join
Inner join asocia solamente los elementos que tienen una relación entre ellos, si los elementos no tienen relación no los muestra.

```sql
select u.id, u.email, p.name from usuarios u
inner join product p on u.id = p.created_by
```
