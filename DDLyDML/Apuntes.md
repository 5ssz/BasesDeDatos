# DDL + DML
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

## DML (Lenguaje de Manipulación de Datos)
El DML es uno de los lenguajes SQL más importantes, ya que nos permite realizar operaciones de manipulación de datos en nuestras bases de datos. Las operaciones que podemos realizar incluyen la **inserción**, **modificación**, **eliminación** y **consulta de datos**.

| Operaciones |     Acción      |
| ----------- |-------------    |
| **SELECT**  | Consultar       |
| **INSERT**  | Insertar tuplas |
| **DELETE**  | Borrar tuplas   |
| **UPDATE**  | Modificación    |

## Funciones de agregación
Las funciones de agregación en SQL permiten efectuar operaciones sobre un conjuto de resultados, pero devolviendo un unico valor añadido para todos ellos.

Estas funciones aparecen en el SELECT de la consulta.

Por ejemplo, si tienes una tabla con varios valores numéricos, puedes usar una función de agregación para sumar todos los valores y obtener un único resultado. 

### Funciones de agregación básicas
| Funciones   |     Acción      |
| ----------- |-------------    |
| **COUNT**   | Devuelve el número total de filas seleccionadas por la consulta       |
| **MAX**     | Devuelve el valor máximo del campo que especifiquemos |
| **MIN**     | Devuelve el valor mínimo del campo que especifiquemos |
| **AVG**     | Devuelve la media del campo que especifiquemos (solo se puede usar en columnas numéricas) |
| **SUM**     | Suma los valores del campo que especifiquemos (solo se puede usar en columnas numéricas) |

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

### Operador LIKE
Se utiliza para la comparacion de un modelo.

Utiliza los comodines especiales: `%` y `_`.

- `%`: Indicamos que en su lugar puede ir cualquier cadena de caracteres.
- `_`: Puede ir ualquier caracter individual (un solo caracter).

Con la combinación de estos carateres podriamos obtener multiples patrones de búsqueda.

### Ejemplo operador LIKE

| Ejemplo     | Significado        |
| --------       |----------     |
| `Nombre LIKE 'A%'`             | El nombre comienza por A         |
| `Nombre LIKE '% A'`            | El nombre acaba por A |
| `Nombre LIKE '% A%'`             | El nombre contiene la letra A         |
| `Nombre LIKE 'A_'`            | El nombre comienza por A y después contiene un solo carácter (cualquier carácter) |
| `Nombre LIKE 'A_E%'`             | El nombre comienza por una A, después cualquier  carácter, posteriormente una E y al final cualquier cadena de caracteres         |

### Ejemplo BETWEEN
