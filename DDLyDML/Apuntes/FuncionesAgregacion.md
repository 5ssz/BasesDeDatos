## Funciones de agregación
Las funciones de agregación en SQL permiten efectuar operaciones sobre un conjuto de resultados, pero devolviendo un unico valor añadido para todos ellos.

Estas funciones aparecen en el SELECT de la consulta.

Por ejemplo, si tienes una tabla con varios valores numéricos, puedes usar una función de agregación para sumar todos los valores y obtener un único resultado. 

### Funciones de agregación básicas
Estas son algunas funciones de agregación básicas y la explicación de su acción:
| Funciones   |     Acción                                                                                |
| ----------- |------------------------------------------------------------------------------------------ |
| **COUNT**   | Devuelve el número total de filas seleccionadas por la consulta                           |
| **MAX**     | Devuelve el valor máximo del campo que especifiquemos                                     |
| **MIN**     | Devuelve el valor mínimo del campo que especifiquemos                                     |
| **AVG**     | Devuelve la media del campo que especifiquemos (solo se puede usar en columnas numéricas) |
| **SUM**     | Suma los valores del campo que especifiquemos (solo se puede usar en columnas numéricas)  |

La siguiente consulta devuelve el **número total** de productos, el precio **máximo**, el precio **mínimo**, el precio **promedio** y la **suma** de los precios de todos los productos en la tabla "productos".
```sql
SELECT COUNT(*), MAX(precio), MIN(precio), AVG(precio), SUM(precio)
FROM productos;
```
