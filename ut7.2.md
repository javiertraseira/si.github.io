# UT7.2: Programación de shell script

## Introducción

```note
El shell scripting permite utilizar las capacidades de la shellpara automatizar multitud de tareas que, de otra forma, requerirían múltiples comandos introducidos de forma manual.
```

Existen diferencias importantes entre los lenguajes de programación tradicionales y el lenguaje de **scripts** que veremos en esta unidad.

-   Los lenguajes de programación son, en general, bastante más potentes y rápidos que los lenguajes de scripting.
-   Los lenguajes de programación comienzan desde el código fuente (de un lenguaje específico), que se compila para crear los ejecutables para cada plataforma específica.
-   Un lenguaje de scripting también comienza por el código fuente, pero no se compila en un ejecutable. En su lugar, un intérprete lee las instrucciones del fichero y las **interpreta** y ejecuta secuencialmente.

### Características

**Características propias de C-shell incorporadas:**

-   Control de trabajos.
-   Manipulación de directorios.
-   Expansión de llaves, para la generación de cadenas arbitrarias.
-   Carácter especial para referenciar al directorio home.
-   Alias, que permiten referenciar más convenientemente comandos y sus opciones.
-   Histórico de comandos, que posibilita reutilizar comandos previamente usados.

**Características propias:**

-   Características de programación integrada: la funcionalidad de comandos UNIX (*test*, *expr*, *getopt*, *echo*) se integraron en el shell, permitiendo que tareas comunes de programación sean realizadas de forma más clara y eficiente.
-   Estructuras de control, como *if* o *select* (para la generación de menús)
-   Variables para personalizar el entorno.
-   Arrays uni-dimensionales que permiten fácil acceso a listas de datos.

**Cuando NO usar scripts:**

-   Tareas de uso intensivo de recursos, especialmente cuando la velocidad es un factor importante (sorting, hashing)
-   Procedimientos que involucren cálculos matemáticos pesados, en especial los que involucren aritmética de punto flotante.
-   Portabilidad (utilizar C en su lugar)
-   Aplicaciones complejas donde se requiere programación estructurada
-   Aplicaciones muy críticas
-   Necesidad de operaciones de archivo intensivas
-   Necesidad de arrays multi-dimensionales
-   Necesidad de estructuras de datos como listas enlazadas o árboles
-   Necesidad de generar o manipular GUIs
-   Necesidad de acceso directo a hardware
-   Necesidad de realizar E/S a través de puertos o sockets
-   Aplicaciones de código-cerrado (Los shell scripts suelen ser Open Source)


### Formato

```note
Un script es un fichero que contiene comandos del shell(en este caso en bash) que llevan a cabo una tarea concreta.
```

Los scripts contienen a su vez:
-   Una estructura de datos: variables
-   Estructuras de control: secuencia, decisión, bucles.

Línea inicial *shebang* para un shell script:

    #!/bin/bash 
    #!/bin/sh

Para **ejecutar** un script:

1.  Hay que hacerlo ejecutable: `chmod +x script`
2.  Invocarlo (varias formas):`./script.sh` o `bash script.sh`

```bash
#! /bin/bash 
#! Primer script echo Hola Mundo
echo Hola Mundo
```

    >./hola.sh #Tiene que tener permisos de ejecución +x

### Comando echo

El comando **echo** sirve para mostrar una cadena de texto concreta con un mensaje para el usuario en la consola:

    Sintaxis: echo [-n] [-e] cadenadetexto

Parámetros:

- -n Suprime la actuación normal de echo, que consiste en que añade una nueva línea a continuación de la salida.
- -e Permite la interpretación de una serie de *secuencias de caracteres* en la cadena.

| **Formato** | **valor** | **Formato** | **valor** |
|-------------|-----------|-------------|-----------|
| Negrita     | \\e[1m    | Amarillo    | \\e[33m   |
| Negro       | \\e[30m   | Azul        | \\e[34m   |
| Rojo        | \\e[31m   | Blanco      | \\e[37m   |
| Verde       | \\e[32m   | Subrayado   | \\e[4m    |


## Caracteres especiales

### Entrecomillados

**Comillas simples [‘ ‘] (weak quote)**

Las comillas simples proporcionan la forma más estricta de citar. Todo lo que esté dentro de ellas se **interpreta literalmente**, sin ninguna expansión o sustitución.

Esto significa que las variables, los comandos y los caracteres especiales no se interpretan ni se expanden dentro de las comillas simples.

```bash
> echo 'El valor de $VAR es $VAR'
El valor de $VAR es $VAR    
```

**Comillas dobles [" "] (strong quote)**

Las comillas dobles permiten la **expansión de variables** y la sustitución de comandos, pero no interpretan ciertos caracteres especiales.

Dentro de las comillas dobles, se expanden las variables (precedidas por \$) y las sustituciones de comandos (precedidas por \`\$()\` o \`).

```bash
VAR="mi valor"
echo "El valor de \$VAR es $VAR“
El valor de $VAR es mi valor
```

> Como se puede ver, la variable se expande a su valor, pero el carácter \$ se escapa con una barra invertida \\ para que sea interpretado de forma literal.


**Comillas invertidas [\` \`] o \$( )**

Los acentos graves se utilizan para realizar la **sustitución de comandos**. El comando dentro de los acentos graves se ejecuta, y su salida se reemplaza en la línea de comandos.

La forma más actual de hacer lo mismo es mediante la forma *\$(comando)* y se recomienda usar esta forma en lugar de los acentos graves porque es más legible y se puede anidar.

Cuando se asignen datos carácter que contengan espacios en blanco o caracteres especiales, se deberá encerrar entre comillas simples o dobles.

Las dobles comillas harán que si, en su contenido se referencia una variable, ésta sea resuelta a su valor.

```bash
var="cadena de prueba"
nuevavar="El valor de var es $var"
echo $nuevavar
> El valor de var es cadena de prueba
```


| **Tipo de Comilla**              | **Descripción**                                          | **Permite Expansión de Variables** | **Permite Sustitución de Comandos** |
|----------------------------------|----------------------------------------------------------|------------------------------------|-------------------------------------|
| **Simples ('')**                 | Contenido tratado como texto literal                     | No                                 | No                                  |
|  **Dobles ("")**                 | Expanden variables, pero mantienen el contenido agrupado |  Sí                                |  Sí                                 |
| **Invertidas (\` \`) o \$(...)** | Ejecutan comandos y devuelven su salida                  | Sí                                 | Sí                                  |

### Comodines

| **Carácter** | **Significado**                                  |
|--------------|--------------------------------------------------|
| **\~**       | Directorio home                                  |
| **\`**       | Sustitución de comando                           |
| **\#**       | Comentario                                       |
| **&**        | Trabajo en background                            |
| **\***       | Estrella de kleene (expresiones regulares)       |
| **( )**      | Inicio/fin de subshell                           |
| **\\**       | Carácter de escape                               |
| **\|**       | Tubería (pipe)                                   |
| **[ ]**      | Inicio/fin conjunto caracteres                   |
| **{ }**      | Inicio/fin de bloque de comandos                 |
| **''**       | Comillas simples (weak quote)                    |
| **""**       | Comillas dobles (strong quote)                   |
| **\> \>\>**  | Redirección de salida                            |
| **\<**       | Redirección de entrada                           |
| **?**        | Reemplazo de un carácter (expresiones regulares) |
| **!**        | Negación de pipeline                             |

## Variables

Las **variables** son una forma de almacenamiento en la que depositamos un determinado dato.

Además, sirven de enlace entre el usuario remoto y el programa. Otra de sus utilidades es poder utilizarlas en distintas partes de nuestro código del script. La semejanza que se suele dar a una variable en informática es la de un contenedor en el que almacenar datos.

Existen dos tipos de variables en Linux de las que ya hablamos:

-   **Variables de entorno o del sistema.** Son las variables que crea el sistema y están disponibles para todos los scripts y programas. Se pueden visualizar usando el comando env.
-   **Variables locales o de usuario** son las que creamos nosotros mismos para su uso específico.

El *shell* permite realizar las siguientes **operaciones** básicas con las variables:

| Descripción                                | Ejemplo       |
|--------------------------------------------|---------------|
| Sólo Definición                            | VAR="" VAR=   |
| Definición y/o Inicialización/Modificación | VAR=valor     |
| Expansión (acceso al valor)                | \$VAR \${VAR} |
| Eliminación de la variable                 | unset VAR     |
| Exportar valor de la variable              | export VAR    |

-   Las variables sólo son accesibles desde el momento de su definición ‘*hacia abajo* del script’, esto es, siempre deben definirse primero e invocarse después.
-   Recordar que Linux es **case sensitive** (sensible a mayúsculas y minúsculas) con lo cual las variables VAR y var se tratarán como variables distintas.
-   Al **exportar** una variable conservará su valor al terminar el script desde donde se ejecutaba, si no se perderá.

### Variables de entorno

Las **variables de entorno**, ya conocidas por nosotros, se ven con el comando **env**. 

Algunas de las variables de entorno importantes son:

| Variable    | Descripción                                                                      |
| ----------- | -------------------------------------------------------------------------------- |
| `$HOME`     | Directorio personal del usuario actual.                                          |
| `$HOSTNAME` | Nombre de la máquina.                                                            |
| `$PATH`     | Lista de directorios donde buscar los programas ejecutables (separados por `:`). |
| `$SHELL`    | Intérprete de comandos por defecto.                                              |
| `$TERM`     | Tipo de terminal.                                                                |
| `$USER`     | Nombre del usuario.                                                              |
| `$PWD`      | Ruta del usuario actual.                                                         |
| `$PS1`      | PROMPT principal.                                                                |

### Comando source

El comando **source** en Bash es una herramienta fundamental para cargar variables y funciones de un fichero de configuración en el entorno actual de un script o sesión de terminal.

Para ello primeramente se crea un fichero de texto con las variables de entorno:

    NOMBRE_APP="MiAplicacion" 
    RUTA_LOGS="/var/log/mi_aplicacion" 
    USUARIO_DB="admin_app" 
    CONTRASEÑA_DB="supersegura123" 
    DEBUG_MODE="true"

Luego en el script principal, se utilizará el comando *source* seguido de la ruta al fichero de configuración. Más adelante veremos cómo utilizarlo mediante ficheros y el uso de condicionales:

source "\$FICHERO_CONFIGURACION"


## Paso de parámetros

El **paso de parámetros** es una operación habitual que consiste en pasar uno o varios parámetros al programa principal para luego operar con ellos.

Se denominan **parámetros posicionales**. Esto es porque preceden y son

gestionados de forma posicional. Así, por ejemplo:

    > find/ -nameprograma.sh

-   Nombre comando = find → \$0
-   1º argumento = / → \$1
-   2º argumento = **-name** → \$2
-   3º argumento = programa.sh → \$3
-   Más argumentos \$4, \$5 .. \${10}…

Valores de las variables pasadas por parámetro en un script:

| **Parámetro** | **Significado**                                              |
|---------------|--------------------------------------------------------------|
| **\$1-\$9**   | Parámetro posicional del 1 al 9                              |
| **\$\#**      | Número de parámetros introducidos                            |
| \$\*          | Todos los parámetros posicionales, “\$\*” en una cadena      |
| \$@           | Todos los parámetros posicionales, “\$@” conjunto de cadenas |
| \$?           | Devuelve el estado del comando más reciente                  |
| \$\$          | PID del proceso actual                                       |

    set tim bill ann fred
    $1 $2 $3 $4
    > echo $*
    tim bill ann fred
    > echo $#
    4
    > echo $1
    tim
    > echo $3 $4
    ann fred

## Lectura de entrada de teclado

El comando **read** lee una línea de la entrada estándar (teclado) y la guarda en variables. Solo funciona en shell interactivos (que lean la entrada del teclado), de lo contrario no hace nada. En su forma más básica, presenta la siguiente sintaxis:

    read VAR1 [VAR2 …]

Este comando espera a que el usuario introduzca una línea de texto incluyendo espacios (la entrada termina cuando el usuario pulsa la tecla "*Intro*"; la pulsación “Intro” no forma parte del valor asignado a la cadena). Esta línea se divide en campos (según la variable IFS). Ejemplo en un script:

```bash
#!/bin/bash
echo -n "Introduzca nombre de fichero a borrar: "
readfichero
rm-i $fichero
echo "Fichero $fichero borrado"
```

Parámetros del comando **read**:

- read –s (no hace echo de la entrada)
- read –nN (acepta sólo N caracteres de entrada)
- read –p “mensaje” (muestra un mensaje)
- read –tT (acepta una entrada por un tiempo máximo de T segundos) 

Ejemplo:

    read–s –n1 -p "si (S) o no (N)?" respuesta

## Operadores aritméticos

Operadores **aritméticos** usados en bash:

| Operación | Descripción  |
|-----------|--------------|
| **+**     | suma           |
| **-**     | resta          |
| **\***    | multiplicación |
| **/**     | división       |
| **\*\***  | exponenciación |
| **%**     | módulo         |

Ejemplo para la terminal evaluando entre doble (()):

    > a=((5+2)*3))
    > echo$a
    > ((b=2**3))
    > echo$a+$b

La instrucción letse puede utilizar para realizar funciones matemáticas, especialmente dentro de scripts:

    $ letn=n+1
    $ letx=10+2*7
    $ echo $x
    24
    $ letY=X+2*4
    $ echo $Y
    32

## Evaluación de expresiones

Los scripts pueden **evaluar expresiones** en sus sentencias, lo cual veremos en las estructuras de control que veremos a continuación y nos permite la toma de decisiones en nuestro programa.

Una **expresión** puede ser:

-   Comparación de cadenas
-   Comparación numérica
-   Operadores de fichero
-   Operadores lógicos

Se representa mediante [expresión]

### Comparación numérica

| Opción | Descripción |
|--------|-------------|
| **-eq** | igual que         |
| **-ge** | mayor o igual que |
| **-le** | menor o igual que |
| **-ne** | no es igual que   |
| **-gt** | mayor que         |
| **-lt** | menor que         |

Ejemplos:

    [ n1 -eqn2 ]
    [ n1 -gen2 ]
    [ n1 -len2 ]    

### Comparación de cadenas

| Opción | Descripción |
|--------|-------------|
| **=**  | igual                                              |
| **!=** | distinto                                           |
| **-n** | evalúa si la longitud de la cadena es superior a 0 |
| **-z** | evalúa si la longitud de la cadena es igual a 0    |

Ejemplos:

- [ s1 = s2 ] (truesi s1 es igual a s2, sino false)
- [ s1 != s2 ] (true si s1 no es igual a s2, sino false)
- [ s1 ] (true si s1 no está vacía, sino false)
- [ -n s1 ] (true si s1 tiene longitud mayor que 0, sino false)
- [ -z s2 ] (true si s2 tiene longitud 0, sino false)

Resumen de operadores **numéricos** y de **cadena**:

| Significado                                         | Numérica | Cadena       |
|-----------------------------------------------------|----------|--------------|
| Mayor que                                           | -gt      |              |
| Mayor o igual que                                   | -ge      |              |
| Menor que                                           | -lt      |              |
| Menor o igual que                                   | -le      |              |
| Igual                                               | -eq      | = or ==      |
| No igual                                            | -ne      | !=           |
| str1 es menor que str2                              |          | str1 \< str2 |
| str1 es mayor que str2                              |          | str1 \> str2 |
| La longitud de la cadena de texto es mayor que cero |          | -n str       |
| La longitud de la cadena es 0                       |          | -z str       |


### Operadores de fichero

| Opción | Descripción |
|--------|-------------|
| `-d` | Verifica si el *path* dado es un directorio. |
| `-f` | Verifica si el *path* dado es un fichero. |
| `-e` | Verifica si el fichero existe. |
| `-s` | Verifica si el fichero tiene un tamaño mayor a 0. |
| `-r` | Verifica si el fichero tiene permiso de lectura. |
| `-w` | Verifica si el fichero tiene permiso de escritura. |
| `-x` | Verifica si el fichero tiene permiso de ejecución. |

Ejemplos:

    if [[ -f $fichero ]]
    if [[ -d $ruta ]]

### Operadores lógicos

| Operador | Descripción |
|----------|-------------|
| &&    | Operador AND |
| \|\|  | Operador OR  |
| **!** | Operador NOT |

### Expresiones regulares

Para utilizar expresiones regulares en un if usaremos el comparador **=\~** y la

**expresión regular**, de las que hemos hablado en unidades anteriores:

| Expresión    | Descripción                                 |
|--------------|---------------------------------------------|
| \^    | Principio de línea                                 |
| \$    | Final de línea                                     |
| .     | Cualquier carácter excepto salto de línea          |
| [ ]   | Conjunto de caracteres                             |
| [ - ] | Rango                                              |
| \*    | Cero o más ocurrencias del elemento que lo precede |
| +     | Uno o más ocurrencias del elemento que lo precede  |

Ejemplos:

    if [[ $variable =~ [0-9]+ ]]
    if [[ "$TEST" =~ [^a-zA-Z0-9\ ]+ ]]

## Estructuras de control y decisión

Trataremos a lo largo de la unidad las siguientes **estructuras de control:**

-   Decisión
    -   if-then-else
    -   case
-   Blucles while
-   Bucles for

### if-then-else

    if [ expresion ]; then
    sentencias
    fi

Ejecuta las *sentencias* solo si la **expresion** o condición es verdadera

    if [ expresion ]; then
        sentencia-1
    else
        sentencia-2
    fi

-   Ejecuta la sentencia-1 solo si la **expresión** es verdadera
-   Ejecuta la sentencia-2 si la **expresión** es falsa

        if [ expresion ]; then
            sentencias
        elif [ expresion ]; then
            sentencias
        else
            sentencias
        fi

- La palabra `elif` equivaldría a usar `else if`
- Es parte de la sentencia if y no puede usarse sola, al igual que else.

| **Tipo**     | **Expresión**      | **Descripción**                                                                                                       |
|--------------|--------------------|-----------------------------------------------------------------------------------------------------------------------|
|    Enteros   | n1 -eq n2          | Verdadero si n1 igual a n2                                                                                            |
|              | n1 -ne n2          | Verdadero si n1 distinto a n2                                                                                         |
|              | n1 -gt n2          | Verdadero si n1 mayor que n2                                                                                          |
|              | n1 –ge n2          | Verdadero si n1 mayor o igual que n2                                                                                  |
|              | n1 -lt n2          | Verdadero si n1 menor que n2                                                                                          |
|              | n1 -le n2          | Verdadero si n1 menor o igual que n2                                                                                  |
|   Cadenas    | "\$VAR" = "cad"    | \$VAR vale "cad".                                                                                                     |
|              | "\$VAR" != "cad"   | \$VAR vale algo distinto de "cad".                                                                                    |
|              | -z "\$VAR" "\$VAR" | \$VAR está vacía. Equivale a "\$VAR" = ""                                                                             |
|              | -n "\$VAR"         | \$VAR no está vacía. Equivale a "\$VAR" != "" o ! -z                                                                  |
|     Ficheros | -e "\$FILE"        | \$FILE existe. Si se indica un enlace simbólico, será cierta sólo si existe el enlace simbólico y el fichero apuntado |
|              | -f "\$FILE"        | \$FILE existe y es regular. Si se indica un enlace simbólico, el tipo es el del fichero apuntado.                     |
|              | -d "\$DIR"         | \$DIR existe y es un fichero de tipo directorio                                                                       |
|              | -r "\$FILE"        | \$FILE existe y puede leerse                                                                                          |
|              | -w "\$FILE"        | \$FILE existe y puede modificarse                                                                                     |
|              | -x "\$FILE"        | \$FILE existe y puede ejecutarse                                                                                      |
|              | -s "\$FILE"        | \$FILE existe y su tamaño es mayor de cero bytes                                                                      |

Ejemplo para verificar si un directorio existe:

```bash
#!/bin/bash
echo -n "Introduce un nombre de directorio: "
read DIRECTORIO

if[ -d$DIRECTORIO ];
then
    echo "El directorio existe"
else
    echo "El directorio no existe"
fi
```

Ejemplo usando una comparación de cadenas de texto (String):

```bash
#!/bin/bash
echo "Introduce el nombre del usuario: "
read USUARIO

if[ $USUARIO = $USER ];
then
    echo "usuario correcto"
fi
```

### case

Este tipo de estructura se utiliza cuando se tienen múltiples opciones, como en un menú de opciones:

    case valor in
        pattern1)
        sentencias-1
        ;;

        pattern2)
        sentencias-2 ;;

        patternN)
        sentencias;;
    esac

Ejemplo usando una comparación de cadenas de texto (String):

```bash
case carnet in
    E) echo Remolques;;
    D) echo Autobuses;;
    C1) echo camiones;;
    B[12) echo Automoviles;;
    A*) echo Motocicletas;;
    *) echo categoriano reconocida;;
esac
```

### while

El bucle **while** se lleva a cabo mientras la condición de la expresión evaluada se cumpla. Es decir, se trata de un tipo de bucle que se evalúa al **principio** mientras la condición evaluada sea verdadera.

    while [ expresion ];
    do
        sentencias
    done

La construcción **while** es adecuada a los casos en los que hay que evaluar cuando actuar.

Ejemplo:

```bash
Cont="S"
while [ $Cont = "S" ]; do
ps -A
read -p "Deseas continuar? (S/N)" respuesta
Cont=`echo $respuesta | tr [:lower:] [:upper:]`
done
echo "finalizado"
```

Modelo de un menú sencillo usando bucle *while* y *case* para las opciones:

```bash
while :
do
echo " Escoja una opcionde las siguientes:"
echo "1) Opción1"
echo "2) Opción2"
echo "3) Salir"
echo -n "Seleccione una opcion[1 -3] "
read opcion

case $opcion in
    1) read;;
    2) read;;
    3) exit;;
    *) opcion incorrecta 
esac
done
```

### for

El bucle **for** en Bash es algo distinto a los bucles for tradicionales.

    for VARIABLE in 1 2 3 4 .. N
    do
    sentencias
    done

En realidad, se parece más al bucle **for each** de otros lenguajes, ya que aquí no se repite un número fijo de veces, sino que se procesan los elementos de una lista uno a uno.

```bash
for planeta in Mercurio Venus Tierra Marte Jupiter Saturno
do
echo $planeta #Imprime cada planeta en una línea
done
```

No obstante, también existe el bucle for clásico, recorriendo un índice e incrementando o decremento un índice contador, llamado también for aritmético:

```bash
for((i=1;i<=20;i++))
do
    echo "$i"
done
```

### Continue y break

Igual que en otros lenguajes, es posible romper el funcionamiento normal de las estructuras for y while. Sin embargo, hacerlo supone romper el código a no estructurado y no se aconseja su uso.

-   **continue** se utiliza en estructuras de control repetitivas para detener la iteración actual y continuar con la siguiente.
-   **break** se utiliza también en estructuras de control repetitivas para detener todas las iteraciones restantes de la estructura de control actual.

```bash
while [ $contador -le $max ]
do
    contador=$((contador + 1))
    if [ $contador -eq 5 ]
    then
        break
    fi
done
```

### exit

El comando **exit** se puede utilizar para finalizar la ejecución de un script o para devolver un valor, el cuál estará disponible al proceso padre del script. Al comando exit se le puede agregar un valor numérico (si es distinto de cero implica que no se ha ejecutado correctamente)

Cuando un script termina con *exit* sin parámetros, el estado de salida será el del último comando ejecutado en el script. 

Por ejemplo:

```bash
echo "Introduzca el nombre del fichero: "
read filename
if [ ! –r "$filename" ]
then
    echo "No se puede leer el fichero"
    exit 1
fi
```

## Lectura de ficheros

La forma más sencilla de leer un fichero de texto **línea a línea** en bash, es de la siguiente forma mediante un bucle while:

```bash
while read linea;
do
    echo "$linea"
done < ficherotexto.txt
```

No obstante, la forma recomendada es utilizando el separador de campo interno llamado *IFS* y dejarlo a vacío para que conserve los espacios en blanco iniciales y finales que pudiera haber en el fichero de texto.

```bash
while IFS='' read -r linea; 
do
    echo "$linea"
done < ficherotexto.txt
```

> El parámetro -r en el comando read hace a su vez que no se interpreten los caracteres escapados (con \\).

Si quisiéramos que al leer un fichero de texto con **separadores** sus **campos** fueran asociado a variables, lo haríamos de la siguiente forma.

Dado el siguiente fichero.txt:

    Camila;Parker;4
    Bill;Gates;12
    Ellon;Musk;1

Estableceríamos el nuevo separador en *IFS* y asignaríamos nombres a las variables de los campos leídos:

```bash
while IFS=';' read -r nombre apellido pos; 
do
    echo "$nombre" "$apellido" ha escalado "$pos" posiciones.
done < fichero.txt
```

## Arrays

En Bash existen diferentes formas de **declarar** un array:

-   Asignando valores:

```bash
    distros[0]='Ubuntu’
```

-   Utilizando la palabra clave declare:

```bash
    declare -a distros=('Ubuntu' 'Linux Mint’)
```

-   Directamente:

```bash
    array_distros=('Ubuntu' 'Linux Mint’)
```

Para **mostrar valores** podemos los siguientes formas:

-   Mostrar todos los elementos del array:

```bash
    echo ${array[*]}
```

-   Mostrar un elemento concreto

```bash
    echo ${array[2]}
```

-   Mostrar el nº de elementos

```bash
    echo ${#array[*]}
```

Para **recorrer** un array utilizaremos la siguiente forma mediante un bucle for:

```bash
for i in "${array[@]}"
do
    echo $i
done
```

## Funciones en bash

Es posible declarar y utilizar **funciones** en bash, al igual que en la mayoría de los lenguajes de programación.

Las dos formas de declararlas son las siguientes:

-   El **valor devuelto** por la función se recuperará en el cuerpo del programa principal usando la variable \$?
-   Si se le **pasan valores** a la función se recuperan \$1, \$2, \$3 ... \$n, correspondientes a la posición del parámetro después del nombre de la función.

```bash
suma_numeros(){
    suma=$(($1+$2))
    return $suma
}
```

## Logs de scripts

**logger** es una utilidad que escribe mensajes en el sistema de registro gestionado normalmente por servicios como *rsyslog* o *systemd-journald*. Esto es especialmente útil para:

-   Registrar eventos de un script (inicio, fin, errores…)
-   Depurar (debugging)
-   Auditar acciones del sistema

 El comando tiene la siguiente **sintáxis**:

    logger [parámetros] mensaje

Por ejemplo:

    # Envía un mensaje básico al sistema de logs
    logger "Mensaje simple"
    # Añade una etiqueta para identificar qué script genera el mensaje
    logger -t mi_script "Inicio del script"
    # Registra un error con prioridad alta y etiqueta "backup"
    logger -p user.error -t backup "Error en copia"
    # Incluye el PID del proceso para facilitar la trazabilidad
    logger -i -t test "Mensaje con PID"
    # Envía al log todo el contenido del fichero errores.txt
    logger -f errores.txt