# UT1.2 Introducción a los sistemas informáticos: software 

## El software

```note
El **software** es el conjunto de **instrucciones** y **programas**, parte intangible, que utiliza un ordenador o computadora para funcionar y que se almacena en su memoria.
```

Comúnmente se utiliza este término para referirse de una forma muy genérica a los programas de un dispositivo informático, la parte **lógica** de un ordenador.

Para que un ordenador funcione necesita información o **datos** con los que trabajar. Esta información es de varios tipos dependiendo de su función. El ordenador puede servir para procesar información en forma de datos, los cuales pueden ser textos, imágenes, datos de sensores, hojas de cálculo,
tablas de una base datos, etc.

1.  **Datos de entrada**: Los que se suministran al ordenador desde los periféricos de entrada (teclado, ratón, escáner) o soportes como discos (HDDs, DVDs, etc). Forman parte de la primera fase del tratamiento de la información denominada **entrada**.
    
2.  **Datos intermedios:** Son los que se obtienen en el tratamiento de la información denominada **proceso**.
    
3.  **Datos de salida**: se denominan también resultados del proceso de tratamiento: **salida**.


Para que los componentes electrónicos de un ordenador sean capaces de funcionar y realizar un proceso determinado, es necesario ejecutar un conjunto de órdenes o instrucciones.

```note
Se denomina **programa** al conjunto de **instrucciones** ordenadas y adecuadas para llevar a cabo un determinado proceso.
```

```note
El **software básico** para hacer funcionar cualquier ordenador se denomina sistema operativo y es lo que estudiaremos en este módulo junto con diversos programas.
```

```note
El **sistema operativo** es el componente software de un sistema informático capaz de hacer que los **programas** (**software**) procesen información (**datos**) sobre los componentes electrónicos de un ordenador o sistema informático (**hardware**).
```

Para poder realizar un programa necesitamos usar un lenguaje de programación, que es un conjunto de símbolos combinados que siguen una sintaxis y que se codificarán en instrucciones al ordenador.

Existen diferentes tipos de lenguajes de programación:

- **Lenguajes de bajo nivel**. Son los más cercanos al hardware del ordenador. Dentro de este tipo podemos distinguir:
    - Lenguaje máquina: Comprensible directamente por la máquina (0’s y 1’s)
    - Lenguaje ensamblador: Lenguaje cercano a la máquina, pero basado en instrucciones muy simples.
- **Lenguajes de alto nivel**: Lenguajes independientes del hardware,mucho más comprensibles por el ser humano y que necesitan compilarse para poder traducirse a lenguaje máquina



## Clasificación del software

El software se suele clasificar de forma típica en tres tipos según su función como veremos a continuación:

- Software del sistema

- Software de programación y desarrollo

- Software de aplicación

### Software del sistema (base)

El software de sistema también llamado **software de base** es el conjunto de programas que sirven para interactuar con el sistema informático, confiriendo control sobre todo el hardware, además de dar soporte a otros programas.

Este software se divide en:

-   Sistemas Operativos
-   Controladores de dispositivos (drivers)
-   BIOS/UEFI
-   Hipervisores de Máquinas Virtuales
-   Gestores de arranque
-   Bibliotecas, APIs y otros componentesdel sistema (OpenGL, directX, .NET..)

### Software de programación y desarrollo

El software de programación es un conjunto de herramientas software que permiten al desarrollador informático escribir programas usando diferentes alternativas y lenguajes de programación (muchos de ellos específicos para cada uno de ellos)

**Edición y desarrollo**
Visual Studio Code, IntelliJ IDEA, Visual Studio.

**Compiladores e intérpretes**
GCC, Java/JVM, Python, Node.js.

**Depuración y pruebas**
Debuggers, test unitarios, analizadores.

**Control de versiones**
Git, GitHub, GitLab.

**Automatización y herramientas de desarrollo**
Maven, Gradle, npm, Docker, CI/CD.


### Software de aplicación

El software de aplicación son los programas diseñados para los usuarios para la realización de tareas específicas en los ordenadores o dispositivos para los que han sido diseñados.

**Creación de documentos**
Word, Writer, Google Docs

**Navegar y buscar información**
Chrome, Firefox, Edge

**Comunicarse**
Outlook, Gmail, Teams, Slack

**Crear contenido**
Photoshop, GIMP, Canva, OBS

**Trabajo con IA**
ChatGPT, Gemini, Copilot

#### Aplicaciones de propósito general

Son aplicaciones diseñadas para resolver tareas comunes en múltiples sectores y entornos profesionales, no para una actividad especializada concreta.

Categorías:
- Ofimática (procesadores de textos, hojas de cálculo, presentaciones..)
- Bases de datos.
- Navegadores web.
- Correo electrónico.
- Mensajería y videoconferencia.
- Compresión de archivos.
- Transferencia de ficheros.
- Edición básica multimedia.
- Lectores y editores PDF.
- Herramientas colaborativas 

#### Aplicaciones de propósito específico

Son aplicaciones diseñadas para una actividad o sector determinado:

Ejemplos:
- Ingeniería
- Gestión empresarial
- Asesorías
- Creación 3D
- Redes de telecomunicaciones

La elección del software debe depender de las necesidades, compatibilidad, coste, seguridad, soporte, facilidad de uso y licencia.


#### Inteligencia artificial aplicada al software
La IA se está incorporando como una funcionalidad más dentro del software tradicional y también está dando lugar a nuevas aplicaciones.

**Asistentes conversacionales**
ChatGPT, Gemini, Claude, Copilot.

**Generación de contenido**
Texto, imágenes, audio, vídeo y presentaciones.

**Asistencia profesional**
Redacción, resumen, análisis, traducción y búsqueda.

**Asistencia al desarrollo**
Generación y explicación de código, documentación, pruebas y depuración.

#### Aplicaciones locales, web y cloud
La IA se está incorporando como una funcionalidad más dentro del software tradicional y también está dando lugar a nuevas aplicaciones.

**Aplicación de escritorio (local)**
Se instala y ejecuta principalmente en el equipo.

**Aplicación web**
Se ejecuta mediante un navegador.

**Aplicación cloud / SaaS**
El proveedor ofrece la aplicación como servicio a través de Internet.

#### Tendencias en el software actual

![](media/tendency.png)

### Otras clasificaciones

El software también se suele clasificar siguiendo el siguiente esquema:

![](media/clasificacion_software.png)


### Tendencias del software actual

**Inteligencia Artificial**

Integración de algoritmos de IA en aplicaciones para mejorar la toma de decisiones. IA generativa.

**Computación en la Nube**

Transición hacia servicios basados en la nube para mayor accesibilidad y colaboración.

**Desarrollo Ágil**

Adopción de metodologías ágiles para una entrega más rápida y flexible del software.

## Licencias de software

Para cada uno de los tipos de software vistos anteriormente, es necesario distinguir entre software libre o software, dependiendo de las **licencias** y permisos de uso:

**Software libre**

Es aquel al que se le otorga libertad de uso, copia y distribución a los usuarios. Su código puede ser totalmente abierto o estar sometido a ciertas normas según la licencia asociada concreta a ese programa.

**Software propietario**

Es aquel cuyas condiciones de uso, copia y distribución están sometidas a normas o restricciones. Su código fuente es cerrado, es decir, no está disponible para el usuario (el propietario puede mostrarlo, pero esto no implica que pase a ser software libre en cuanto a su uso).

| **Software libre**                                                                                                                                                                                                   | **Software propietario**                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| No está limitado a los usuarios y garantiza las libertades de usar, modificar, copiar y distribuir software                                                                                                          | Tiene licencias que limitan a los usuarios y que, en algunos casos, son costosas. Estas licencias restringen las libertades de usar, modificar y distribuir software. |
| Puede intervenir en su desarrollo cualquier persona, empresa u organización, por lo que se generan gran cantidad de ideas innovadoras, y permite la adecuación a los avances tecnológicos.                           |  El desarrollo, la actualización y la programación de este software solo lo realiza la empresa que tiene los derechos.                                                |
| Los avances, modificaciones y descubrimientos tecnológicos son constantes y se encuentran en Internet de forma gratuita. "La principal meta del software libre es compartir los avances tecnológicos con los demás." |  El futuro del software que adquirió el usuario solo depende de una empresa comercial.                                                                                |
| Compatible tanto en software como en hardware, no obliga al usuario a cambiar de sistema operativo o equipo.                                                                                                         | Siendo creado con fines de lucro, las actualizaciones o mejoras al software quedan estipuladas bajo contrato.                                        

![licencias](media/soflibrepropietario.png)

```note
Una **licencia de software** es un contrato entre el licenciante (autor/titular de los derechos de explotación/distribuidor) y el licenciatario del programa informático (usuario consumidor/usuario profesional o empresa), para utilizar el software cumpliendo una serie de términos y condiciones establecidas en sus cláusulas.
```

Cuando compramos o bajamos de Internet un programa, al instalarlo solemos aceptar sin leer (*mala costumbre*) un contrato que especifica el tipo de **Licencia** de uso del software, en inglés **EULA** o *End User License Agreement*: licencia por la cual el uso de un producto sólo está permitido para un único usuario (el comprador). Es un acuerdo unilateral puesto que el usuario no tiene más opción que aceptar o rechazar el contenido del mismo.

### Software libre (GNU)

>   💡 El proyecto GNU fue iniciado en 1984 por Richard Stallman y fundó la Free Software Foundation sin ánimo de lucro.
Se fundamenta en la moral y exige la libertad absoluta del software. 

Las **cuatro libertades** del software libre son:

1.  La libertad de usar el programa, con cualquier propósito (libertad 0)

2.  La libertad de estudiar cómo funciona el programa, y adaptarlo a tus necesidades (libertad 1)
    
3.  La libertad de distribuir copias, para ayudar a otros (libertad 2)
    
4.  La libertad de mejorar el programa y hacer públicas las mejoras a los demás, de modo que toda la comunidad se beneficie (libertad 3)

>   📌 Para proteger estas libertades existe el concepto de **copyleft**: el copyleft garantiza que cualquier modificación o distribución de un programa libre deba mantenerse también como libre, evitando que alguien lo convierta en software propietario.


![](media/libertades_software.png)


>   📌 El software libre no hace referencia a que sea gratuito (de hecho, no siempre lo es).

El término libre en software libre se refiere a la libertad del usuario, no al precio del programa. Un software libre puede ser gratuito, pero también puede venderse o tener un coste asociado (por ejemplo, servicios de soporte, formación o distribución). Lo importante es que, sea gratis o de pago, el usuario siempre conserva las cuatro libertades fundamentales: usar, estudiar, modificar y redistribuir el programa.

Aunque se confunden, el **software de código abierto** (open source) y **software libre** no son exactamente lo mismo debido a diferencias sutiles de concepto. Ambos permiten acceder al código fuente, pero sus objetivos y filosofías no son iguales como veremos a continuación


### El software de código abierto (Open Source)

El software de código abierto trata de suavizar las condiciones del *GNU* para facilitar su uso por las compañías y fomentar la colaboración entre empresas y comunidades.

>   💡 El término **Open Source** (código abierto) surge a finales de los años 90 con la creación de la Open Source Initiative (**OSI**).

Es un movimiento más ‘**pragmático**’, que se enfoca más en los beneficios prácticos como acceso al código fuente que en aspectos éticos o de libertad que son tan relevantes en el Software Libre.

![](media/081baa59bfc621dadfc7baa92280bc27.jpg)

### Software propietario

El software propietario es aquel que sin permiso del propietario queda prohibida la copia, redistribución o modificación como hemos visto. Para poder usar se suele pedir permiso a la organización que lo desarrollo. Generalmente para su disponibilidad hay que pagar bajo unos derechos de autor (un **Copyright**).

En conclusión, los propietarios son los que establecen los derechos de uso, distribución, redistribución, copia, modificación, cesión y en general cualquier otra consideración que se estime necesaria. 

Los fabricantes de programas sometidos a este tipo de licencias por lo general ofrecen servicios de soporte técnico y actualizaciones durante el tiempo de vida del producto, también regulan el número de copias que pueden ser instaladas e incluso los fines concretos para los cuales puede ser utilizado.

## Licencias de software propietario

### Tipos licencias de software propietario

Tipos de licencias de software propietario:

- **Licencias de usuario final**: Es el tipo más común de licencia en software propietario. Define los derechos y responsabilidades del usuario final en el acuerdo EULA, incluyendo las restricciones de uso, instalación y la prohibición de ingeniería inversa, redistribución o modificación del software.

- **Licencias OEM**: se trata de un tipo de licencia que supedita su venta a que forme parte de un equipo nuevo, estando prohibido venderlo si no es bajo esta condición.
    
- **Licencias Retail**: son las versiones a la venta ‘normal’ de software a través de cualquier canal. En este caso, el programa es de la entera propiedad del usuario, pudiendo éste cederlo libremente a terceros o venderlo. Estas licencias permiten utilizar el programa en otros equipos siempre que no se ejecuten ambos a la vez.
    
- **Licencias por volumen (VLM)**: es un tipo de licencia de software destinado a grandes usuarios (empresas), normalmente bajo unas condiciones similares a las de las licencias OEM, aunque sin estar supeditadas a equipos nuevos.
    
- **Alquiler o suscripción**: El cada vez más habitual modelo de suscripción. El tipo más común es el conocido como Software como servicio (**SaaS**). Estas son cada vez más habituales, especialmente en las implementaciones cloud. Con este modelo de pago de licencias, la empresa paga una cantidad bastante menor de coste inicial. Algunos proveedores permiten que el número de licencias usadas cambie de mes en mes, otros requieren que las licencias se alquilen por periodos de tiempo más largos.

- **Otro tipo de licencias especiales**: Por ejemplo, las licencias de educación, empresariales, desarrollo o de sectores específicos como el militar. También las licencias shareware, demos o freeware.

## Licencias de software libre

### Tipos licencias de software libre

Podemos clasificar las licencias de software en diferentes tipos, ya que no todas cumplen con un grado de libertad absoluto que da la licencia GNU estándar:

- **Licencias libres (copyleft fuerte o recíprocas estrictas)** se basan en las cuatro libertades vistas anteriormente. Todo lo que derive de ellas debe mantenerse con la misma licencia. Garantizan que el software siempre sea libre.

- **Licencias semi-libres (copyleft débil o recíprocas flexibles)**: permiten mezclar partes libres con propietarias, siempre que las piezas originales se mantengan libres. Fomentan la adopción de librerías en entornos comerciales.

- **Licencias permisivas (no recíprocas)**: se puede hacer casi de todo, incluso reutilizar el código en software propietario, siempre reconociendo la autoría. 

> El copyleft obliga a que las obras derivadas mantengan la misma licencia.


### Licencias libres (copyleft fuerte)

- **Licencias GPL (General Public License).** 
Se la puede considerar como Licencia de software libre con protección heredada. Creada por la Free Software Foundation (FSF), es una de las licencias más usadas y estrictas en cuanto a copyleft:

    -   El nuevo software o modificación deberá tener la misma licencia.
    -   El uso de partes en otro software también obliga a hacer uso de la misma licencia.
    -   Gratuito para el programador (salvo gastos de copia o distribución) pero no dice nada que establece restricciones sobre lo que se puede cobrar por distribuir una copia.
    
        ![](media/gpl_logo.png)


- **Licencia GNU.** 
 El caso de licencia GPL más destacada es Licencia Pública General de GNU (**GNU GPL**) en la que autor conserva los derechos de autor (copyright) en la que autor conserva los derechos de autor (copyright), y permite la redistribución y modificación bajo términos diseñados para asegurarse de que todas las versiones modificadas del software permanecen bajo los términos de la propia licencia.
 

    ![](media/gnugpl_logo.png)

> El software comercial se basa en que para usarse hay que realizar un pago. Puede existir software libre y propietario de este tipo. 

### Licencias semilibres (copyleft débil)

- **Licencia MPL (Mozilla Public License)**

- Creada por Mozilla para el navegador Firefox.
- Obliga a mantener bajo MPL los archivos de código originales y modificados, pero permite combinarlos con otros módulos bajo licencias distintas (incluso propietarias).
- Se considera un término medio entre GPL (muy restrictiva) y MIT/Apache (muy permisivas).

- **Licencia EPL (Eclipse Public License)**

- Similar a MPL, usada en el proyecto del IDE Eclipse.
- Obliga a que las modificaciones directas al código EPL se mantengan con esa licencia, pero permite coexistencia con código propietario.


### Licencias permisivas (no recíprocas)

-  **Licencia BSD (Berkeley Software Distribution).** Es un tipo de licencia conocida por ser menos “restrictiva” lo que permite que desarrolladores puedan modificar, distribuir e incluso vender el software derivado.

   ![](media/0a2b39a8862349d551c17c4b1a83fc11.png)


-  **Licencia MIT** Muy permisiva, permite a los usuarios usar, modificar y redistribuir el software, incluso en productos propietarios, siempre y cuando se mantenga el aviso de copyright original.

-  **Licencia Apache** Ofrece más protección legal que la licencia MIT o BSD, incluyendo cláusulas sobre patentes. Permite la modificación y redistribución del software bajo otras licencias, siempre que se mantengan los avisos de derechos de autor y licencias.

 ![](media/apache_license.png)

### Licencias software libre vs open source

**Software Libre (FSF – Free Software Foundation)**
- Se centra en la defensa de las **4 libertades**.
- Muchas licencias libres (como la **GPL**) imponen copyleft fuerte; si distribuyes software derivado, estás obligado a hacerlo bajo la misma licencia.
- Filosofía ética/moral: la obligación no es solo legal, también es un compromiso con la comunidad.

**Open Source (OSI – Open Source Initiative)**
- Se centra en la **apertura del código**, no en la libertad como principio moral.
- Incluye tanto licencias con **copyleft fuerte** (GPL) como licencias **permisivas** (MIT, BSD, Apache).
- Dependiendo de la licencia elegida, las obligaciones cambian:
    - Con copyleft fuerte → mismas obligaciones que en software libre.
    - Con licencias permisivas → muy pocas obligaciones, basta con reconocer la autoría.


### Creative Commons

Las licencias **Creative Commons (CC)** son unas licencias que no están pensadas para software, sino contenido de obras culturales, educativas o artísticas.   
Esta licencia posibilita un modelo legal de distribución y uso de contenidos basada en 4 condiciones principales que pueden ser combinadas para hacer licencias mixtas:

    -  **Atribución** (**BY**).- Se conceden derechos de copia, distribución, exhibición y derivación siempre y cuando se reconozca y cite la obra de la forma especificada por el autor o el licenciante.
    -  **No Comercial** (**NC**).- Se puede copiar, distribuir, exhibir y representar la obra y hacer obras derivadas pero sin fines comerciales.
    -  **No Derivadas** (**ND**).- En este caso podemos copiar, distribuir, exhibir y representar copias literales de la obra pero no producir obras derivadas.
    -  **Compartir Igual** (**SA**) -El usuario tiene el derecho de distribuir obras derivadas pero siempre con una licencia idéntica a la de la obra original.
    
    
![](media/1de27f98de5390429fb01adbc544ee22.jpeg)

- La siguiente licencia **CC-BY-SA** significa que se es libre para:
    - *Compartir:* copiar y redistribuir el material en cualquier medio o formato.
    - *Adaptar*: remezclar, transformar y crear a partir del material
    - Para cualquier propósito, *incluso comercialmente.*
    - El licenciante no puede revocar estas libertades si usted sigue los términos de la licencia. 
    
    Bajo los siguientes términos:
        - **Atribución (BY)** Usted debe reconocer el crédito de una obra de manera adecuada, proporcionar un enlace a la licencia, e indicar si se han realizado cambios . Puede hacerlo en cualquier forma razonable, pero no de forma tal que sugiera que tiene el apoyo del licenciante o lo recibe por el uso que hace.
        - **Compartir Igual (SA)** Si usted mezcla, transforma o crea nuevo material a partir de esta obra, usted podrá distribuir su contribución siempre que use la misma licencia que la obra original.


### Dominio público

Las licencias de **dominio público** (como la **CC-0**) son licencias que otorgan derechos de dominio público o actúan como exenciones. Se utilizan para hacer que los trabajos con derechos de autor sean utilizables por cualquier persona sin condiciones, al tiempo que se evitan las complejidades de la atribución o la compatibilidad de licencias que se producen con otras licencias.

No se requiere ningún permiso o licencia para usar trabajos del dominio público, así como aquellos con un copyright expirado.

![](media/986ed41efd72225fb2cdbe2c6dcc759f.png)

## Resumen licencias de software

![](media/23ec0eaa562ac6f1ed4e469b8907a4d8.jpeg)


El **software comercial** se basa en que para usarse hay que realizar un pago. Puede existir software libre y propietario de este tipo. 

Un programa libre debe estar disponible para uso comercial, desarrollo comercial y distribución comercial. El desarrollo comercial del software libre ha dejado de ser inusual; el software comercial libre es muy importante.
   
### Otras licencias


| **Software Libre**  | **Software privativo o propietario**  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Software Libre** Uso gratuito (existen excepciones) Se puede modificar Se pueden distribuir los cambios.              | **Software privativo o propietario** Se paga por cada licencia No se puede modificar. |
| **Dominio público** Software sin licencia. Se permite uso, copia, modificación o redistribución con o sin fines de lucro. |    **Freeware** Uso gratuito No se puede modificar.                                                            |
|               | **Shareware** Se prueba y luego se paga. No se puede modificar. |
|               | **Adware** Uso gratuito de software a cambio de una gran cantidad de publicidad.
 |

![](media/cuadro_resumen.png)


![](media/dbd29cf8de14860ca5a64ac44a50cc36.jpeg)


## Selección y evaluación de software

![](media/eleccion_aplicacion.png)

### Selección y evaluación del software de aplicación

En un entorno profesional no siempre debemos elegir la aplicación más conocida, la más cara o la que tenga más funciones.

La aplicación adecuada es aquella que **responde mejor a las necesidades reales del usuario o de la organización.**

Antes de seleccionar una aplicación debemos analizar diferentes criterios:

- **Funcionalidad:** qué tareas permite realizar.
- **Compatibilidad:** con sistemas operativos, dispositivos y formatos.
- **Modelo de uso:** aplicación local, web o cloud.
- **Coste y licencia:** compra, suscripción, software libre o propietario.
- **Seguridad y privacidad:** tratamiento y protección de la información.
- **Usabilidad:** facilidad de aprendizaje y utilización.
- **Integración:** capacidad para trabajar con otras aplicaciones.
- **Soporte y mantenimiento:** actualizaciones y asistencia técnica.

### Criterios técnicos y funcionales

**Funcionalidad**

- ¿Qué tareas debe realizar?  
- ¿Qué funciones son imprescindibles?  
- ¿Qué tipo de usuario va a utilizarla?

**Compatibilidad**

- Sistema operativo: Windows, GNU/Linux, macOS, Android...  
- Requisitos de hardware: CPU, RAM, almacenamiento o GPU.  
- Compatibilidad con formatos: PDF, DOCX, CSV, ODF, imágenes, vídeo...  
- Compatibilidad con otros programas y dispositivos.

**Modelo de uso**

- **Local:** se instala y ejecuta en el equipo.  
- **Web:** se utiliza desde un navegador.  
- **Cloud:** se ofrece como servicio a través de Internet.