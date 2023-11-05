## Relational Database Management System:

Los **Relational Database Management System** son los software que se encargan de permitirnos interactuar con la base de datos ya sea mediante la consola, una app o una interfaz gráfica para gestionar esas bases de datos:
- MySQL
- PostgreSQL
- SQL Server
- Otros más

```sql
create database helloworld; //Crea una base de datos
show databases;
use helloworld; //Va a empezar a usar la base de datos helloworld
CREATE TABLE animales(
	id int PRIMARY KEY,
	tipo varchar(255), //Ese 255 es el largo de la cadena
	estado varchar(255)
	PRIMARY KEY (id)
);
-- Esto es un comentario
```

Como ya hasta ahí se tiene creada la tabla el id tiene que ser auto incremental. Eso se hace con la siguiente instrucción
```sql
ALTER TABLE animales MODIFY COLUMN id int auto_incremental; 
```

Si deseas renombrar la tabla puedes hacerlo de la siguiente manera
```sql
RENAME TABLE animales to animal 
```

Para eliminar una tabla
```sql
DROP TABLE usuarios;
```