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
	id int,
	tipo varchar(255), //Ese 255 es el largo de la cadena
	estado varchar(255)
	PRIMARY KEY (id)
)
```

Prueba
