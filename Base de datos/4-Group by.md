El GroupBy sirve para agrupar por una propiedad. Por ejemplo si se quiere saber cuantos productos de una marca existen se puede hacer lo siguiente

```sql
select count(id), marca from product p
group by marca
having count(id) > 1 ; -- Este having es como un where para los group by 
					   -- solo apareceran las marcas con mas de 1 producto
```