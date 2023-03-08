## Tipos de datos
Cuando creamos una tabla debemos indicar los tipos de datos de los atributos.

Se pueden ver clicando aquí: [POSTGRESQL.ORG](http://www.postgresql.org/docs/9.5/interactive/datatype.html)

#### Ejemplo 2
La siguiente sentencia crearia una tabla llamada **departamento**, que define una columna llamada "codigo" de tipo **SERIAL** (es equivalente a un tipo de dato entero autoincremental), la columna **nombre** como una cadena de texto de longitud máxima 20 y se establece la columna **codigo** como la clave primaria de tabla usando la cláusula PRIMARY KEY.
```sql
CREATE TABLE departamento (
  codigo SERIAL,
  nombre VARCHAR(20),
  PRIMARY KEY (codigo)
  );
```
