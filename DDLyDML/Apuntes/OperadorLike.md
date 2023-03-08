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
