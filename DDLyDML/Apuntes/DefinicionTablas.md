## Definición de tablas
**La sentencia para crear tablas al DDL:**
```sql
CREATE TABLE
```

**Sintaxi:**
```sql
CREATE TABLE nombre_de_la_tabla
(definicion_de_columnas, definicion_de_restricciones)
```

Dónde:
**nombre_de_la_tabla** es el nombre que se le dará a la tabla que se quiere crear.

**definicion_de_columnas** es el nombre de la columna, tipos de datos, etc.

**definicion_de_restricciones** son las restricciones o condiciones que se aplicaran a la tabla (clave primaria, foranea, etc).

#### Ejemplo 1
La siguiente sentencia crearia una tabla llamada **clientes** con tres columnas: **id** (entero), **nombre** (cadena de texto de longitud máxima 50) y **dirección** (cadena de texto de longitud máxima 100):
```sql
CREATE TABLE nombre_de_la_tabla (
  id INT,
  nombre VARCHAR(50),
  direccion VARCHAR(100)
);
```
