# UT2.2 Funcionamiento elementos CPU

## Instrucciones

```note
Se denomina **instrucción**  al conjunto de datos insertados en un programa de ordenador y que el procesador interpreta y ejecuta.
```

Las instrucciones del computador son las que determinan el funcionamiento de la CPU que las ejecuta.

Los tipos de instrucción permitidos están definidos y determinados dentro de cada plataforma en lo que se **llama** el **conjunto o juego de instrucciones** (*ISA Instruction Set Architecture*).

Las instrucciones a su vez tienen un **formato concreto** (según establece su diseño del juego de instrucciones), que divide cada instrucción de *n bits* (*normalmente 32 o 64*) en **varios campos**.

Para determinar el tipo de instrucción usaremos su *Opcode*.

![](media/5e53f8134c0c1432ce765807e1ef48ab.png)


![](media/a03a01ed8765399a7ec278f7dbe9c4ad.jpeg)

En todas las CPU modernas se pueden encontrar el siguiente **conjunto de instrucciones**:

-   Instrucciones de transferencia de datos *(mem-cpu)*
-   Instrucciones aritméticas
-   Instrucciones lógicas
-   Instrucciones de control
-   Instrucciones de transferencia Entrada/Salida

![](media/e746a4975ee5a5b1413533dfaef773bd.jpeg)

Cada instrucción se suele identificar con un **nemotécnico** que hace referencia a la función que realiza la instrucción *(MOVE, STORE, LOAD, ADD, MULTIPLY, SET, INCREMENT...)*

-   Ejemplos de instrucciones de **transferencia** de datos del modelo x86:

    ![](media/f663416a37d6c362b60eba3c2ddfd309.jpeg)

-   Ejemplos de instrucciones **aritméticas** de datos del modelo x86:

    ![](media/1fca05373ee465c10d96e7b87034c1f3.jpeg)

-   Ejemplos de instrucciones **lógicas** de datos del modelo x86:

    ![](media/da7bc643f19f40bfff08d3dbae0c8f7b.jpeg)


-   Ejemplos de instrucciones **de control** de datos del modelo x86:

    ![](media/97d543131ec7ebb25ddbb4a53ea4e8cb.png)

-   Ejemplos de instrucciones **de transferencia E/S**:

    ![](media/8e2c54cdb2abceafd98c2e5717460fbf.jpeg)

## Fases de una instrucción

Toda instrucción residente en memoria principal pasa por una serie de fases que van desde su captura a su interpretación y ejecución. Éstas son:

1.  **Carga, búsqueda o lectura (fetch).** La UC envía a la memoria principal la dirección de la instrucción a ejecutar, que está almacenada en el registro contador de programa (PC) y activa las señales de control necesarias para que ésta le entregue la mencionada instrucción.
2.  **Decodificación (decode)**. La UC recibe la instrucción, la analiza y, en su caso, lee los operandos de la memoria principal, enviando su dirección y activando las correspondientes señales de control.
3.  **Ejecución (execution)**. La ALU, bajo las órdenes de la UC, realiza la operación sobre los operandos, y, si es necesario, se graba el resultado en la memoria principal (store) o en un registro.
4.  **Incremento del contador de programa** (PC). Con lo que se puede pasar a ejecutar la instrucción siguiente, aunque existen instrucciones que pueden modificar el contenido del PC dando lugar a ‘saltos’.

## Funcionamiento de un programa

![](media/c76d490a5177045f6737c29d92ba467c.jpeg)

![](media/766535505914dc648a4ab833f462cd4f.jpeg)

![](media/e99bd257714f0530317b166d97c451ad.jpeg)

![](media/d25f9a3868176d4009604361e23c543d.jpeg)

![](media/5d5c313e6e7922952bf79e60a02c34c4.jpeg)

![](media/c2634b8eefd0ae40f0e8c65de3d93d4b.jpeg)

![](media/9b2d99b0491c8a85ed729e242f090c60.jpeg)

![](media/af93b50488dd9aa84e691921175970dd.jpeg)

![](media/ccce3350f4bfebecb621f37690080b17.jpeg)

## Funcionamiento arquitectura interna

Una vez estudiada la **arquitectura** podemos deducir que existen una serie de parámetros que sirven para determinar la **capacidad de proceso** de una CPU, que básicamente serían:

-   **Velocidad de procesador**. Determina el ritmo de ejecución de instrucciones. Se mide en hercios y múltiplos de éstos.
-   **Juego de instrucciones**. Cada tipo de CPU tiene un juego de instrucciones característico.
-   **Tamaño del bus de datos y direcciones**. Se mide en bits, siendo hoy día habitual los 64 y 128 bits de tamaño.
-   Número de registros de que dispone.
-   Líneas y señales de interrupción que implementa.

Recordar los registros de la CPU con los que vamos a trabajar vistos previamente:

-  **El Registro de Instrucciones (IR)** es un registro de propósito especial. Se utiliza para guardar la instrucción que se ha buscado desde la memoria.
-  **El Registro Contador de Programa** (PC – *Program Counter*): Se utiliza para guardar la dirección de memoria de la próxima instrucción a buscar.
-  **Registro de Direcciones de memoria** (MAR – *Memory Address Register*) se usa para guardar exclusivamente direcciones de memoria.
-  **Registro de datos** (MDR - *Memory data Register*): Almacenamiento temporal entre los datos de la memoria y la ALU.
-  **Registro Acumulador (RA)** en el que son almacenados temporalmente los resultados aritméticos y lógicos intermedios que serán tratados por el circuito operacional de la unidad aritmético-lógica (ALU).
-   **Registros de Entrada de operandos de la ALU:** Registro de entrada de operandos a la ALU.

![](media/93feb8b2c8956aa13902ca6880b9d1d4.jpeg)

![](media/680235859cda646f7c2a88102ccd522a.jpeg)

![](media/6f4aef3c87c13e3293df44a450e4cde0.jpeg)

![](media/57ac39ebaf5143b65081af13619febce.jpeg)

![](media/83359042309bcedc28c784efa6a894c1.jpeg)

![](media/ef8a906e20fe02f9a35cd13b139ee75a.jpeg)

![](media/df48bb8d176b3079fd4aa41d676a3f6e.jpeg)

![](media/d525e9ebf01151d8e63df7ea8e890cf8.jpeg)

![](media/685356c7d5e99367c14305b937d92a81.jpeg)

![](media/5145aba562502a8e573d4bbf4971c292.jpeg)

![](media/8599d5aeb6d34d974ff238d1f96ed140.jpeg)

![](media/85c94f75d4db73de48d4aaa996e09ae5.jpeg)

![](media/acec30e82f20fa35f6a324ce039d8ec3.jpeg)

![](media/47f70506a973b30cfda89e1ca5411abe.jpeg)

![](media/c14c5bde7d1dd1026f6cfe88b0a4aeee.jpeg)

![](media/3f148e856f99bd05aea67b9fd8bb9023.jpeg)

![](media/284754736f8a8a0b9eb7712499e904ca.jpeg)

![](media/65abfe924089729ad9613576192b5bb5.jpeg)

![](media/138d201c4307407dc77944c42c56be4b.jpeg)

![](media/9468cc82f4c8909ac8240a3d47aa46ee.jpeg)

![](media/d5462889bafb97084913fd13796d6d7a.jpeg)
