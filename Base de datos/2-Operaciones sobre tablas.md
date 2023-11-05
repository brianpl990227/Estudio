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

Este comando va a devolver todos los animales de la tabla. Ahora si queremos hacer un filtrado se debe de poner un **where

```sql
SELECT * FROM animales WHERE estado = 'feliz'
```

Se pueden añadir operadores lógicos al **where 

```sql
SELECT * FROM animales WHERE estado = 'feliz' AND tipo = 'perro'
```
