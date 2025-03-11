# Laboratorios Sistemas Operativos

## Compilación
Para compilar los programas utilizar el comando `make`. Si se ejecuta sin parámetros, compila _todos_ los programas del laboratorio. Si se indica el nombre de un archivo _sin la extensión_ compila sólo el programa indicado.

Por ejemplo, para compilar el ejercicio 1 del laboratorio 1 (programa `sum.c`):
```
$ make sum
gcc -g -Wall -Wextra -Wshadow -Wconversion -Wunreachable-code -o ./bin/sum sum.c
sum.c: In function ‘main’:
sum.c:4:14: warning: unused parameter ‘argc’ [-Wunused-parameter]
    4 | int main(int argc, char *argv[])
      |          ~~~~^~~~
sum.c:4:26: warning: unused parameter ‘argv’ [-Wunused-parameter]
    4 | int main(int argc, char *argv[])
      |                    ~~~~~~^~~~~~
$
```

El compilador genera una serie de _warnings_ (advertencias). En este caso, nos está indicando que los parámetros `argc` y `argv` de la función `main()` no estan siendo utilizados (`unused parameter`). El objetivo es que la resolución de cada ejercicio cumpla con el enunciado y que _además_ compile *sin advertencias*.

El ejecutable se crea dentro del subdirectorio `bin` del laboratorio. Lo podemos comprobar haciendo un listado del contenido de dicho directorio:
```
$ ls bin
sum 
$
```
Para ejecutar el programa recien compilado:
```
$ bin/sum
$
```
Como todavía no se realizó una modifación al programa, no realiza ninguna acción.

## Laboratorios

- Lab0X: laboratorio.
- xv6: código fuente de xv6.
