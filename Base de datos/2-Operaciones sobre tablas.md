## Insertar
Para insertar información en una tabla primero se debe de seleccionar la tabla donde se quiere insertar la data, luego entre ( ) las columnas y luego los valores correspondientes tambien dentro de ( ) 

```sql
INSERT INTO animales (tipo, estado) VALUES ('gato', 'furioso')
```

## Leer tabla
Empecemos por la selección más básica, la tabla completa

```sql
SELECT * FROM animales
```

Este comando va a devolver todos los animales de la tabla. Ahora si queremos hacer un filtrado se debe de poner un **where**

```sql
SELECT * FROM animales WHERE estado = 'feliz'
```

Se pueden añadir operadores lógicos al **where** 

```sql
SELECT * FROM animales WHERE estado = 'feliz' AND tipo = 'perro'
```

```sql
-- Revisa en la columna email si está la cadena gmail sin importar inicio ni final
SELECT * FROM usuarios WHERE email LIKE '%gmail%'
```

```sql
-- Revisa en la columna email si está la cadena gmail al final
SELECT * FROM usuarios WHERE email LIKE '%gmail'
```

```sql
-- Revisa en la columna email si está la cadena gmail al principio
SELECT * FROM usuarios WHERE email LIKE 'gmail%'
```

```sql
-- ordena ascendentemente, para decendente es DESC
SELECT * FROM usuarios ORDER BY edad ASC
```

```sql
-- Obtiene el usuario de mayor edad, min(edad) para el de menor
-- mayor es el nombre de la columna de la respuesta
SELECT max(edad) as mayor FROM usuarios 
```

```sql
-- Escoge solamente los datos que me interesan de la tabla de usuarios
-- Se puede cambiar el nombre de la columna con as
SELECT name as nombre, email FROM usuarios 
```
## Actualizar 
Para actualizar un valor en una tabla se procede de la siguiente manera

```sql
UPDATE animales SET estado = 'feliz', tipo = 'Lagarto' WHERE id = 2
```

## Eliminar
Es importante a la hora de eliminar especificar el **where** de lo contrario se elimina la tabla completa
```sql
DELETE animales WHERE id = 3
```

### Nota
En las últimas versiones de MySQL se fuerza a que en el where de debe de poner un ID, esto se puede desactivar.