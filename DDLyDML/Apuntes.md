# DDL + DML
## Definición de tablas:
**La sentencia para crear tablas al DDL:**
```sql
CREATE TABLE
```

**Sintaxi:**
```sql
CREATE TABLE nombre_de_la_tabla
(definición_de_columnas, definición_de_restricciones)
```

Dónde:
**nombre_de_la_tabla** es el nombre que se le dará a la tabla que se quiere crear.

**definición_de_columnas** es el nombre de la columna, tipos de datos, etc.

**definición_de_restricciones** son las restricciones o condiciones que se aplicaran a la tabla (clave primaria, foranea, etc).

#### Ejemplo 1:
La siguiente sentencia crearia una tabla llamada **clientes** con tres columnas: **id** (entero), **nombre** (cadena de texto de longitud máxima 50) y **dirección** (cadena de texto de longitud máxima 100):
```sql
CREATE TABLE nombre_de_la_tabla (
  id INT,
  nombre VARCHAR(50),
  dirección VARCHAR(100)
);
```
## Tipos de datos:
Cuando creamos una tabla debemos indicar los tipos de datos de los atributos.

Se pueden ver clicando aquí: [POSTGRESQL.ORG](http://www.postgresql.org/docs/9.5/interactive/datatype.html)

#### Ejemplo 2:
La siguiente sentencia crearia una tabla llamada **departamento**, que define una columna llamada "codigo" de tipo **SERIAL** (es equivalente a un tipo de dato entero autoincremental), la columna **nombre** como una cadena de texto de longitud máxima 20 y se establece la columna **codigo** como la clave primaria de tabla usando la cláusula PRIMARY KEY.
```sql
CREATE TABLE departamento (
  codigo SERIAL,
  nombre VARCHAR(20),
  PRIMARY KEY (codigo)
  );
```
