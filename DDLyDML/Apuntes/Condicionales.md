## Condiciones
Las condiciones se utilizan en las columnas SQL para filtrar los resultados basándose en ciertas condiciones lógicas. Estas se especifican utilizando la cláusula **WHERE** en la consulta **SELECT**

Después de su resolucion devuelven para cada fila TRUE o FALSE, en funcion de que se cumple o no.

### Operadores condicionales
| Condicional    | Acción        |
| --------       |----------     |
| `>`            | Mayor         |
| `>=`           | Mayor o igual |
| `<`            | Menor         |
| `<=`           | Menor o igual |
| `=`            | Igual         |
| `IS [NOT] NULL`| Para comprobar si el valor de una columna es o no es NULO, es decir, si tiene o no tiene algun valor |
| `BETWEEN`      | Para un intervalo de valores |
| `LIKE`         | Para comprarar un modelo    |
