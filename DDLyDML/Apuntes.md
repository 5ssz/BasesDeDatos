# DDL + DML
## Definición de tablas:
- La sentencia para crear tablas al DDL:
```sql
CREATE TABLE
```

- Sintaxi:
```sql
CREATE TABLE nombre_de_la_tabla
(definición_de_columnas, definición_de_restricciones)
```

Dónde:
`nombre_de_la_tabla` es el nombre que se le dará a la tabla que se quiere crear.
`definición_de_columnas` es el nombre de la columna, tipos de datos, etc.
`definición_de_restricciones` son las restricciones o condiciones que se aplicaran a la tabla (clave primaria, foranea, etc).

Ejemplo:
La siguiente sentencia crearia una tabla llamada `clientes` con tres columnas: id (entero), `nombre` (cadena de texto) y `dirección` (cadena de texto):
```CREATE TABLE 
id INT
nombre VARCHAR(50)
dirección VARCHAR(100)
);
```
