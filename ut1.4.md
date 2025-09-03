# UT 1.4 Introducción a los Sistemas Informáticos: Redes de telecomunicaciones

## Red de datos de telecomunicaciones

```note
Una **red de datos** es un conjunto de dispositivos conectados entre si, que pueden comunicarse para compartir datos y recursos sin importar la localización física de dichos dispositivos.
```

¿Qué se puede **compartir** en una red de datos?

- **Datos.** Información a modo de paquetes o archivos.
- **Recursos.** Periféricos (impresoras, escáner, etc.), acceso a Internet, etc.
- **Servicios.** Streaming, chat, juegos, correo electrónico, configuraciones automáticas, VoIP, transferencia de ficheros, control remoto, etc.

![](media/377c4e9cbd8d3b5549f7e04c3b8211a2.png)

### Proceso de comunicación

En todo **proceso de comunicación**, se requiere de un **emisor**, un **mensaje**, un
**medio** y un **receptor**.

![](media/fce0b68530e47a83fa2f8140eb515846.png)

-   **Emisor**: es la entidad que transmite la información.
-   **Receptor**: es la entidad que recibe la información.
-   **Mensaje**: es la información que el emisor transmite al receptor.
-   **Canal**: es el medio por el que se transmite el mensaje.
-   **Código**: es el conjunto de signos, reglas y normas (lenguaje) que se emplean para construir el mensaje.

![](media/6de4e550ea712d191159d0a5ba2c5132.jpeg)

```note
En el proceso de comunicación, además de estos elementos, habitualmente interviene un factor adicional denominado ruido. 
```

Se considera ruido cualquier interferencia que contamine tanto el mensaje como el canal o el código. Por ejemplo, cuando hablamos con otra persona, el sonido ambiental (coches, televisión, música, etc.) es el ruido de la comunicación.

Cuando el ruido supera un determinado umbral, el proceso de comunicación peligra, de forma que la información que se transmite puede no llegar correctamente.

![](media/9dbc2c95a98eecda5843a61ad77f66f9.png)

### Objetivos y ventajas

-   **Compartir recursos (objetivo básico)**: Hacer que todos los programas, datos y equipos estén disponibles para cualquiera de la red que lo solicite, sin importar la localización del recurso y del usuario así como permitir la **movilidad**.
- **Proporcionar una alta fiabilidad**, al contar con fuentes alternativas de suministro. Todos los archivos podrían duplicarse en dos o tres máquinas de tal manera que si una no se encuentra disponible, podría utilizarse algunas de las copias.
-   **Ahorro económico**: El compartir recursos y servicios hace que se ahorre en costes ya que no es necesaria la compra de periféricos redundantes, también se aumenta la rapidez en la comunicación, pues se pueden centralizar recursos.
-  Permite mejorar la **seguridad** y control de la
información que se utiliza, permitiendo el acceso de determinados usuarios únicamente a cierta información o impidiendo la modificación de diversos datos.

### Desventajas

-   Las tecnologías evolucionan continuamente, los **estándares** a veces se usan en la práctica sin haberse consensuado e incluso, a veces, ni siquiera existen.
-   Las redes de telecomunicaciones, al ser sistemas distribuidos, necesitan mantenimiento y especialistas TI para mantenerlas operativas.  

-   Muchos programas y dispositivos tienen bugs (agujeros en la seguridad) que pueden aprovecharse para acceder a la configuración de forma remota. La **seguridad** debe ser una cuestión importante, pues algunos usuarios pueden crear problemas voluntaria o involuntariamente.

## Internet

```note
**Internet** es un conjunto inmenso de tecnologías, infraestructura (como cables, satélites y antenas) y protocolos que permiten el intercambio de información entre millones de dispositivos de forma prácticamente instantánea.
```

Internet se basa en una arquitectura de red de telecomunicaciones distribuida que utiliza protocolos de comunicación para conectar dispositivos y permitir la transmisión de datos. Esta red global proporciona una variedad de servicios, como el acceso a información, comunicación, entretenimiento, comercio electrónico y muchas otras aplicaciones.

La tecnología subyacente a Internet ha revolucionado la forma en que vivimos, trabajamos e interactuamos entre nosotros, y continúa evolucionando a un ritmo acelerado.

### Historia y origen

En 1958 los EEUU fundaron la *Advanced Researchs Projects Agency* (**ARPA**) a través del Ministerio de Defensa. El ARPA estaba formado por unos 200 científicos de alto nivel y gran presupuesto. El ARPA se centró en crear comunicaciones directas entre ordenadores para comunicar las diferentes bases de investigación.

En 1962, el ARPA creó un programa de investigación computacional bajo la dirección de John Licklider, un científico del MIT.

En 1967 ya se había hecho suficiente trabajo para que el ARPA publicara un plan para crear una red de ordenadores denominada **ARPANET**. La red recopilaba las mejores ideas de los equipos del MIT, el National Physics Laboratory (UK) y la Rand Corporation.

![](media/be98cd6514de9e94def06817c5493ac3.png)

En diciembre de 1969 se habían conectado los cuatro primeros nodos universitarios: Universidad de California en LA, su sede en Santa Bárbara, la Universidad de Utah y Stanford.

La red fue creciendo y en 1971 ARPANET ya tenia 23 puntos conectados.

![](media/f3c1d1eae32960a0f0818f8e15db56ed.jpeg)

Entre 1974 y 1982 se crearon gran cantidad de redes entre las que destacaron:

-  Telenet (1974): Versión comercial de ARPANET.
-  Usenet (1979): Sistema abierto centrado en el e-mail y que aun funciona.
-  Bitnet (1981): Unía las universidades americanas usando sistemas IBM.
-  Eunet (1982): Unía Reino Unido, Escandinavia y Holanda.

En aquél momento el mundo de las redes era un poco caótico, a pesar de que ARPANET seguía siendo el ‘estándar’. EN 1981, ARPANET adoptó el protocolo **TCP/IP** y en aquel momento se creó **Internet** (*International Net*).

A principios de los 80 se comenzaron a desarrollar los ordenadores de forma exponencial. El crecimiento era tan veloz que se temía que las redes se bloquearan debido al gran número de usuarios y de información transmitida, hecho causado por el fenómeno del e-mail. La red siguió creciendo exponencialmente.

### Historia de la web

El concepto de **WWW** fue diseñado por Tim Berners-Lee y científicos del **CERN** en 1990 en Ginebra. Estos científicos estaban interesados en poder buscar y mostrar fácilmente documentación a través de Internet. Los científicos del CERN diseñaron un navegador/editor y le pusieron el nombre de **World Wide Web**. En 1991 dicha tecnología fue presentada al público a pesar de que el crecimiento en su utilización no fue muy espectacular, a finales de 1992 solamente había 50 sitios web en el mundo, y en 1993 había 150.

![](media/1d3d8631393d66366a3728d0886db82c.png)

En 1993 Mark Andreesen, del *National Center for SuperComputing Applications* (NCSA) de Illinois publicó el **Mosaic X**, un navegador fácil de instalar y de usar. Sus creadores fundaron a su vez una empresa llamada Netscape en Silicon Valley.

A partir de la publicación de la tecnología **WWW** y de los navegadores se comenzó a abrir Internet a un público más amplio: actividades comerciales, páginas personales, redes sociales junto la explosión de equipos cada vez más potentes y portables.

¿Qué pasa en un minuto en **Internet** en 2024?

![Gráfico, Diagrama  Descripción generada automáticamente](media/e2fb04468abba87bfcaa450c16d0ef11.jpeg)

## Criterios de clasificación

![](media/440ec800de754bb0804ea3f63ff11c39.png)

### Según su tamaño o alcance

Para clasiﬁcar las redes tradicionalmente se consideran dos grandes categorías según su **tamaño o alcance geográfico**: las redes de área extensa (**WAN**) y las redes de área local (**LAN**). Cada vez es más difícil diferenciar entre estos dos tipos porque la diferencia en tecnología que utilizan y las aplicaciones es mínima.

Tipos de redes:

-   Redes de área Personal (**PAN**)
-   Redes de área Local (**LAN**)
-   Redes de área Metropolitana (**MAN**)
-   Redes de área Extensa (**WAN**)
-   Redes Virtuales (**VPN**) \*
-   Redes Cloud Computing\*

![](media/aa22533cb7a5bd52558c3e01cb50030e.jpeg)

![](media/2e860528622d770f35221baa2e282aed.jpeg)

![](media/network_sizes.png)

A menudo, las redes físicas pueden conformar la base para varias redes de comunicación lógicas, llamadas **Virtual Private Networks (VPN)** de tamaño generalmente global.

![](media/260b47ce3eaab9d0e510c8b020901cca.png)



```note
Las **redes de área personal PAN** (Personal Area Network) son aquellas redes comprenden el entorno del usuario y los dispositivos con los que interactúa.
```

Se trata de redes inalámbricas cuyo radio de acción es de pocos metros. Hace uso de tecnologías inalámbricas como Bluetooth, infrarrojos o NFC.


![](media/5c619f2a73f4022b52b750d9b8011985.png)


```note
Las **redes de área local LAN** (Local Area Network) son aquellas redes que interconectan varios dispositivos dentro de un edificio o vivienda.
```

El alcance de este tipo de redes está limitado por la longitud máxima de los cables o por el alcance de las antenas inalámbricas. Dentro de este tipo de redes están también las **WLAN** (Red de Área Local Inalámbrica), en las que habitualmente nos conectamos a través del protocolo **WI-FI**.

![](media/55634d2c0ceeb907376c00177a91142d.png)

```note
Las **redes de área metropolitana MAN** (Metropolitan Area Network) son aquellas redes formadas por un conjunto de redes LAN que interconecta equipos en el entorno de un municipio.
```

Las MAN abarcan un área más extensa que las redes LAN pero más pequeña que las redes WAN. Existe una subdivisión más pequeña que MAN llamada CAN (Campus Area Network). Una red WAN está formada por varias redes MAN.

![](media/907778527ae78bfc532f6de69478c795.jpeg)

```note
Las **redes de área extensa WAN** (Wide Area Network) son aquellas redes lógicas que cubren una extensa área geográfica, del tamaño de un país o continente.
```

El cableado y equipamiento está distribuido por canalizaciones que unen diferentes poblaciones. De la instalación y mantenimiento se encargan las compañías de telecomunicaciones. Se construyen redes WAN especialmente para alguna empresa que tiene varias oficinas en partes del país o del continente. Internet es otro ejemplo de red de servicios estructurada sobre una red de área extensa.

![](media/208ae6fa4e6e127aa31407602bc0d5a5.jpeg)

El **backbone de Internet** es un concepto relacionado con las redes WAN. Se refiere a las principales conexiones troncales de Internet y que permiten su funcionamiento a nivel global. Están compuestas de un gran número de enrutadores interconectados comerciales, gubernamentales, universitarios y otros que llevan los datos a través de países, continentes y océanos mediante cableado de fibra óptica.

Parte de la extrema resiliencia de Internet se debe a su diseño estructural, ubicando las funciones de estado y control en los propios elementos de la red y relegando la mayor parte del procesamiento a los extremos finales. De esta manera se asegura la integridad, la fiabilidad y la autenticidad de los datos.

![](media/e4c78b668d364311a90b1335abc03ccf.png)

Internet es un enorme árbol cuyas ramas se extienden lejos, pero que cuenta con al menos 13 sólidas raíces. Son los denominados **servidores raíz de Dominio,** que contienen la información para resolver todas las direcciones existentes. Esta información indica cuales son esos servidores y que direcciones IP tienen, así como cuales son los nombres y direcciones IP de los servidores de dominios de 1er nivel.
> Por ejemplo, informa de cuáles son las direcciones IP de los servidores DNS del dominio .es. Aunque solo hay 13 servidores raíz principales hay otros muchos otros repartidos por el mundo que son copia de alguno de los principales.

![](media/51d34088f6e489d12c8f296ff35345f7.png)

Mapa de cables submarinos:

![](media/e00acca80f701cc2160b698c05dbeea3.jpeg)

[www.submarinecablemap.com](http://www.submarinecablemap.com/)

```note
Un **VPN** (Virtual Private Network) es una Red Privada Virtual que utiliza una conexión segura (**túnel**) a través de una red pública como puede ser Internet.
```

Una red VPN es un caso particular que ofrece las ventajas y flexibilidad de una red local, pero sin necesidad de estar conectados físicamente, sino de manera virtual.

Las conexiones VPN generan lo que se denomina como **túneles VPN** mediante los cuales los datos irán directamente cifrados a un servidor VPN y desde ahí dirigirán la petición al proveedor de Internet. Lo que provoca dicho camino, es que el proveedor identifique a la dirección del VPN como la que pide los datos y no al propio usuario.

![](media/a96f452e913bfb34e62bf4ab0f6ba2c2.jpeg)

### Según su direccionalidad

Si el criterio que utilizamos es la **direccionalidad de la transmisión**, los sistemas de comunicación pueden clasificarse en:

- Simplex: Cuando la comunicación se efectúa en un sólo sentido. Emisor emite, receptor recibe. Ejemplo: Cuando escuchamos música por radio analógica. Sólo nosotros recibimos.
- Semidúplex (half duplex): Cuando la comunicación se realiza en los dos sentidos, pero no de forma simultánea. Emisor emite, receptor recibe, receptor pasa a ser emisor, y emisor pasa a ser receptor. Ejemplo: Hablar por emisoras o funcionamiento del WiFi.
- Dúplex (full duplex): Cuando la comunicación se realiza en ambos sentidos de forma simultánea. Ambos son emisores y receptores a la vez.

### Según su tecnología de interconexión

Las redes basadas en su tecnología de interconexión pueden ser:

- Medios **guiados**
    - Redes Ethernet
    - Redes de fibra óptica
    - Redes a través de línea telefónica
    - Redes de comunicación de línea de potencia

- Medios **no guiados**
    - Microondas terrestres o satelitales.
    - Ondas de radio.

### Según su método de transmisión

Existen dos métodos de trasmisión en las redes modernas:

-   **Banda base**: El método de banda base define que solamente una señal digital puede viajar por el medio y que su velocidad está limitada. Todos los equipos compartirán el mismo canal en diferentes intervalos de tiempo y solo se admitirá por tanto una transmisión simultánea empleando todo el ancho de banda disponible.
-   **Banda ancha**: Este método de transmisión permite enviar varias señales que pueden viajar al mismo tiempo por el medio. Se divide el medio físico en varios canales. La información se modula antes de transmitirla. Permite enviar distintos tipos de información: video, voz y datos.

![](media/5b0bbef838dfb570a7528526cc01111b.jpeg)

### Según funciones

- **Redes de igual a igual o entre iguales**, también conocidas como **redes peer-to peer**. Son redes donde ningún ordenador está a cargo del funcionamiento de la red. Cada ordenador controla su propia información y puede funcionar como cliente o servidor según lo necesite.

- **Redes cliente-servidor**, se basan en la existencia de uno o varios servidores, que darán servicio al resto de ordenadores que se consideran clientes. Este tipo de redes facilitan la gestión centralizada. Para crear redes de este tipo necesitamos sistemas operativos de tipo servidor.

![red cliente-servidor](media/368d94ffecaed4f63548d1859da2e57c.jpeg)![Red peer-to-peer](media/510d800e5c57588d4bc2912192fcc5b2.jpeg)

### Según el tipo de enlace

-   **Enlace de difusión**. Existe un único canal de comunicación compartido por todas las computadoras. Cuando una de las máquinas envía un mensaje, todas las demás pueden verlo. Se distinguen varios modos de direccionamiento:
    -   A todos (*broadcast*)
    -   A uno (*unicast*)
    -   A un subconjunto (*multicast*)
    -   Al más cercano o de menor latencia (*anycast*)


-   **Enlace punto a punto**. La conexión se realiza entre pares de máquinas, con canales dedicados. Un paquete puede que visitar nodos intermedios para llegar al destino.

    ![](media/881118973feeba43631444a5fe980c26.png)

Modos de direccionamiento según el enlace de difusión visto anteriormente:

  ![](media/modos_enlace.png)


### Según el propietario de la red

- **Redes privadas**: son redes instaladas y gestionadas por particulares, empresas u organizaciones privadas. Puede ocurrir que sean alquiladas a
compañías para su uso exclusivo. Sólo tendrán acceso los propietarios autorizados.

- **Redes públicas**: Son redes de titularidad pública. Las líneas de comunicación soportan información de diferentes usuarios. Se trata en todo caso de redes de servicio público ofertadas por compañías de
telecomunicaciones bajo cuotas de alquiler en función del uso realizado. Las redes de área extensa suelen ser públicas.

- **Redes mixtas o dedicadas**: Una línea puede ser pública, pero también puede ser exclusiva para quien la alquila, apareciendo lo que se denomina las líneas dedicadas.

### Según la velocidad de transmisión

La unidad que se utiliza al medir el caudal de datos transmitidos por las redes es el bit por segundo. Normalmente hablamos de Mbs o Mbps (megabit por segundo), que son un millón de bits por segundo. Así según la velocidad de transmisión de datos tenemos los siguientes tipos de redes:

-   **Ethernet** Standard (IEEE 802.3) - *10* Mbps.
-   **Fast Ethernet** Standard (IEEE 802.3u) - *100* Mbps.
-   **Gigabit Ethernet** Standard (IEEE 802.3z) - *1000* Mbps. 
-   **10 Gitabit Ethernet** Standar (IEE 802.3a) - *10000* Mbps


## Características de una red

### Velocidad

Hace referencia a la velocidad a la que se transmiten los datos por segundo a través de una red. La rapidez de subida y descarga de datos será diferente según los estándares que utilicemos y también según el tipo de red o medio a través del que se transmiten los datos (inalámbrica, fibra óptica, cables de teléfono o coaxial).

No se debe confundir la velocidad de una red con su **ancho de banda** o la **latencia** de dicha red. El **ancho de banda** mida la cantidad de datos que se pueden transmitir en la unidad de tiempo, mientras que la **latencia** hace referencia es el tiempo que tarda en transmitirse un paquete dentro de una red y es otro factor clave en las conexiones a Internet.

![](media/2859471311e2111dd8e92f94ed7c1979.jpeg)

En función del tipo de actividad para la que se utiliza una red, se ofrecen algunos rangos de velocidad mínima que debería ser suficiente para sus necesidades.

-   **Streaming de video**: Dependiendo del tipo de vídeo, necesitará 3 Mbps para vídeo estándar, 5Mbps para HD, y 25 Mbps para 4k Ultra HD.
-   **Streaming de música**: Una velocidad de 2 Mbps debería ser suficiente para la reproducción de música en streaming.
-   **Juegos**: Los jugadores deben tener velocidades de hasta 10 Mbps para obtener el mejor rendimiento y una latencia baja.
-   **Correo electrónico o redes sociales**: Para acceder a una página de correo o red social sencilla necesitará velocidades de 0,5 — 5 Mbps.
-   **Videollamadas**: 0,5 Mbps para llamadas estándar y 1,5 Mbps si utiliza HD.
-   **Descargar archivos grandes**: Se requiere una conexión rápida para alcanzar velocidades de hasta 50 Mbps.

### Confiabilidad

La confiabilidad o **tolerancia a fallos** mide el grado de probabilidades que existe de que uno de los nodos de la red se averíe y por tanto se produzcan fallos. En parte dependerá de la topología de la red que hallamos instalado y del lugar que ocupa el componente averiado. Cuando uno de los componentes no funciona, puede afectar al funcionamiento de toda la red o por el contrario constituir un problema local.

Por esta razón resulta determinante contar con un **hardware redundante** para que, en caso de fallo en uno de los componentes, haya una gran tolerancia a los errores y los demás equipos puedan seguir trabajando.

![](media/353a202c8ee384ac5bf3f6963389c8e4.jpeg)

### Seguridad en la red

-   Es un conjunto de estrategias que sirven para proteger una red de accesos indebidos o pérdida de datos. En el caso de redes inalámbricas, la **seguridad** es uno de sus aspectos más peligrosos y controvertidos. El uso de cifrados o contraseñas inseguras junto con la aparición de intrusos que puedan robar información y drenar ancho de banda es una de las razones que convierte estas redes en bastante más vulnerables.
-  Por otro lado, las redes cableadas pueden sufrir interferencias (ruido) como consecuencia del uso de otros aparatos electrónicos. A diferencia de estas, la fibra óptica es la que ofrece una mayor seguridad.

![](media/a0c49a96b71dfe3afdfb18ca216eb898.png)


### Escalabilidad

-   La **escalabilidad** hace referencia a la capacidad y facilidad para cambiar de tamaño de una red. Una red no puede añadir nuevos componentes de forma continua y esperar que funcione a la misma velocidad. A medida que añadimos nuevos nodos y estos se hallan funcionando a la vez, la conexión a Internet se reduce, la velocidad de transmisión de datos en general es menor y hay más probabilidad de errores.
-   Es por eso importante ver la facilidad y las posibilidades de añadir o cambiar componentes de hardware y software o nuevos servidores para mejorar el rendimiento de la red.

    ![](media/d3ee695c2c06bcfef04e6e7be9f2b48c.jpeg)

### Disponibilidad

Es la capacidad que posee una red para hallarse disponible y completamente activa cuando la necesitemos. Evidentemente no es lo mismo hablar de una red local del hogar que la de una empresa o institución. Se habla de la cantidad de tiempo posible en que podemos someter los nodos a unas condiciones de rendimiento necesarias en nuestra empresa. El objetivo es conseguir que la red se halle disponible según las necesidades de uso para las que se ha instalado.

![](media/755541bd19a935494ec237c499d0eb22.png)


## Modelo cliente-servidor

El **modelo cliente-servidor** es un concepto fundamental en las redes de computadoras. En este modelo, se distingue entre dos tipos de roles principales: el cliente y el servidor, cada uno con funciones específicas y complementarias.

**Cliente**

Es el dispositivo o software que realiza solicitudes para acceder a un servicio o recurso. Por ejemplo, cuando un usuario utiliza un navegador web para acceder a un sitio, el navegador actúa como cliente al enviar una solicitud de información (por ejemplo, acceder a una página web) a un servidor.

**Servidor**

Es el dispositivo o software que responde a las solicitudes de los clientes, proporcionando los recursos o servicios solicitados. Un servidor web, por ejemplo, responde con páginas HTML, imágenes u otros contenidos a los clientes que lo solicitan.

![](media/2fc70c14a00bf7f9324daa0f5cd6ef61.jpg)

## Servicios web

```note
Un **servicio web** es cualquier software que se pone a su disposición a través de Internet y utiliza un formato estandarizado (como XML o JSON) para la solicitud y la
respuesta de una interacción con la interfaz de programación de aplicaciones (API).
```

![](media/web_service.jpg)