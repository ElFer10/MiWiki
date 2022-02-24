# AWK

## 1. Ejecutar programas AWL

### En línea de comando

* awk 'programa' input_file
* awk -f archivo_awk input_file
* <comando_que_será_input> | awk 'programa' 

### En archivo ejecutable

```{bash}
#!/usr/bin/env awk -f
```
## 2. Estructura de un programa

_pattern_ { acción }

* En cada línea donde se cumple el _pattern_ se ejecuta la acción.
* Si se omite el _pattern_ se aplicará la acción a cada línea del input
* Si se omite la acción, AWK imprimirá las líneas que coincidan con el pattern.

## 3. Patterns de AWK

* **BEGIN {acciones}**: las acciones se ejecutan **ANTES** de procesar input.
* **END {acciones}**: las acciones se ejecutan **DESPUÉS** de leer todo el input.
* **expresión compuesta {acciones}**: se arman con **&&**, **||** y **!**. 
* **pat1, pat2 {acciones}**: las acciones se ejecutan desde pat1 hasta que se
  cumpla pat2.
  
## 4. Acciones 

Pueden incluir:

* print lista-expresiones
* printf(formato, lista)
* if (exp) accion else accion
* while (exp) accion
* for (exp; exp; exp) accion
* for (var in array) accion
* do accion while exp
* break
* continue
* next
* exit

## 5. Variables por defecto

| Variable | Significado                                    | Default |
|----------|------------------------------------------------|---------|
| ARGC     | Número de argumentos en linea de comandos      | -       |
| ARGV     | Array de argumentos pasados al programa        | -       |
| FILENAME | Nombre del input                               | -       |
| FNR      | Número de fila (record) en el archivo          | -       |
| FS       | Separador de campos                            | " "     |
| NF       | Número de campos en la fila                    | -       |
| NR       | Número de fila (record) leído hasta el momento | -       |
| OFMT     | Formato de salida para números                 | "%.6g"  |
| OFS      | Separador de campos de salida                  | " "     |
| ORS      | Separador de filas (records) de salida         | "\n"    |
| RLENGTH  | Longitud de la cadena encontrada               | -       |
| RS       | Separador de filas (records)                   |         |
| RSTART   | Inicio de la cadena encontrada                 | -       |
| SUBSEP   | Separador de subscript                         | "\034"  |

## 6. 


