# Amazon Web Services (AWS) <!-- omit in toc -->

- [Semana 1. Introducción](#semana-1-introducción)
  - [¿Qué es la informática de la nube?](#qué-es-la-informática-de-la-nube)
  - [Ventajas de la nube](#ventajas-de-la-nube)
  - [Tipos de implementación de cómputo en la nube](#tipos-de-implementación-de-cómputo-en-la-nube)
  - [Modelos de servicios](#modelos-de-servicios)
  - [Infraestructura global](#infraestructura-global)
  - [Historia](#historia)
  - [¿Qué se necesita  para tener un Data Center?](#qué-se-necesita--para-tener-un-data-center)
  - [Capex vs Opex](#capex-vs-opex)
  - [Videos](#videos)


## Semana 1. Introducción

### ¿Qué es la informática de la nube?

También es llamada computación en la nube (cloud computing) o simplemente nube.

**Definición de los grandes**

Estas son las definiciones que dan algunas entidades importantes:

- Amazon:
    La informática en la nube es la distribución de recursos de TI bajo demanda (on-demand) a través de Internet mediante un esquema de pago por uso. En lugar de comprar, poseer y mantener servidores y centros de datos físicos, puedes acceder a servicios tecnológicos, como capacidad informática, almacenamiento y bases de datos, en función de tus necesidades a través de un proveedor de la nube como AWS.

- Salesforce:
    La informática en la nube es la prestación de servicios informáticos, tales como software, bases de datos, servidores y conexiones a red, a través de Internet. Esto significa que los usuarios finales pueden acceder a software y aplicaciones desde cualuier punto donde se encuentren.
    El alojamiento de los programas informáticos lo lleva a cabo un tercero, y estos residen en "la nube". Esto significa que los usuarios no se tienen que preocupar por cosas como el almacenamiento y la capacidad, solo tienen que disfrutar del resultado final.

- Microsoft:
    Dicho de manera sencilla, la informática en la nube es el suministro de servicios informáticos (incluyendo servidores, almacenamiento, bases de datos, redes, software, análisis e inteligencia) a través de Internet ("la nube"), cuyo objetivo es ofrecer una innovación más rápida, recursos flexibles y economías de escala. Lo habitual es pagar solo por los servicios en la nube utilizados, a fin de reducir los costes operativos, ejecutar la infraestructura con más eficacia y escalar a medida que cambian las necesidades de tu negocio.

- Google
    Conocer los tipos de recursos de cloud computing puede requerir mucho tiempo y dinero. Las empresas necesitan comprar servidores físicos y otra infraestructura por medio de procesos de aprovisionamiento que pueden durar meses... Los sistemas adquiridos requieren espacio físico, por lo general, una sala especializada que ofrezca suficiente potencia y refrigeración [Data Center]. Después de configurar y desplegar los sistemas, las empresas necesitan expertos que los gestionen.

    Escalar este proceso de larga duración cuando hay picos de demanda o mientras que el negocio crece es complicado. Las empresas pueden adquirir más recursos de computación de los que necesitan y acabar con un bajo nivel de utilización.

    El cloud computing soluciona estos problemas ofreciendo recursos de computación como servicios escalables y bajo demanda (on-demand).

- IBM:
    La computación en la nube es el acceso bajo demanda (on-demand), a través de Internet, a recursos informáticos (aplicaciones, servifores físicos y virtuales, almacenamiento de datos, herramientas de desarrollo, capacidadesde red, etc.) alojados en un centro de datos remoto gestionado por un proveedor de servicios en la nube (o CSP). El CSP pone a disposición estos recursos por una cuota de suscripción mensual o los factura en función del uso.


- Red Hat:
    La computación en la nube es el acto de ejecutar cargas de trabajo dentro de nubes, que son entornos informáticos que abstraen, agrupan y comparten recursos escalabes a través de una red. Ni la computación en nube ni las nubes son tecnologías en sí mismas.

    La computación en la nube es un acto: ejecutar cargas de trabajo en la nube.

    Las nubes son entornos, lugares en donde se ejecutan las aplicaciones. Las tecnologías son cosas: software y hardware utilizados para constuir y utilizar nubes.

**Nuestra definición**

Entonces, para nosotros la informática en la nube es:

    - usar servicios informáticos bajo demanda, dados por un CSP a través de Internet, 
    - para ejecutar cargas de trabajo 
    - sin adquirir la infraestructura física necesaria para ejectuar estas cargas (la nube se encarga).

Servicios informáticos, recursos de TI y recursos de computación son sinónimos de lo mismo (lo que da un provedor de servicios en la nube o CSP, por Cloud Solutions Provider).

Los servicios son bajo demanda (on-demand). La computación bajo demanda (ODC, por "On-Demand Computation") es un modelo de entrega a nivel empresarial que permite a los usuarios 

- aprovisionar y desaprovisionar fácilmente recursos en la nube cuando los necesitan. Solo usas lo que necesitas cuando lo necesitas.

Estos servicios pueden ser 
- software, servidores, bases de datos, redes, entornos de desarrollo, análisis e inteligencia, etc.

Pagas por el uso (pay-as-you-go), por lo que es una solución que evita los costos iniciales altos y escala con las necesidades del cliente.

### Ventajas de la nube

Se nos explican 6 ventajas principales:

1. Cambias costos de capital por costos variables

    No tienes que gastar en costosos servidores, firewalls, UPS y demás equipos solo para darte cuenta de que quizás la aplicación no era muy buena idea. Con la nube pagas solo por los recursos que usas, y solo en la medida en que los usas.

2. Te beneficias de la economía de escala
    
    Un proveedor de servicios en la nube como AWS ha optimizado sus instalaciones y sus gastos para ofrecer de forma competitiva recursos TI a millones de usuarios y empresas de todo el mundo. Por eso los costos variables que piden son bajos.

3. Dejas de precuparte por planificar la capacidad

    No tienes que anticipar cuánta capacidad de cómputo o de almacenamiento necesitas para tu aplicación. Con solo unos clics puedes aprovisionar o desaprovisionar los recursos que necesitas cuando los necesitas. Es un gran ahorro de tiempo y una preocupación menos.

4. Aumentas la agilidad y flexibilidad

    Los desarrolladores pueden hacer pruebas y comenzar a desarrollar más rápido gracias a la facilidad de uso de los servicios de AWS.

5. Dejas de gastar dinero en un centro de datos

    La informática en la nube te permite centrarte en tu propuesta de valor en vez de en el arduo trabajo indiferenciado de la infraestructura. 
    
    El trabajo indiferenciado (undifferentiated heavy lifting) es lo que toda aplicación necesita para funcionar, pero que no agrega valor. Por eso AWS lo hace por ti.

6. Tu alcance es global en minutos

    Gracias a la infraestructura global de AWS, en unos mintuos puedes implementar tu aplicación en una región cercana a tus clientes para disminuir el tiempo de latencia y así aumentar la performance de tu aplicación.

### Tipos de implementación de cómputo en la nube

**Nube**



**On-premises**

La palabra _premises_ significa 'instalaciones'. Se trata de la temida implementación de un centro de datos completo para soportar nuestra aplicación.

**Híbrido**



### Modelos de servicios

Los modelos de servicios se corresponden con el nivel de control y flexibilidad que tienes sobre los recursos TI.

**IaaS**

Ofrece el mayor nivel de control sobre los recursos informáticos, como conexión de red, máquinas virtuales y espacio de almacenamiento de datos. Contiene los bloques fundamentales para crear aplicaciones.

**PaaS**



**SaaS**


### Infraestructura global

Actualmente, la infraestructura de AWS está distribuida por el mundo en 32 regiones y 102 zonas de disponibilidad (AZ). Una región de AWS es un área geográfica que contiene varias AZ (al menos 3). Las AZ son ubicaciones aisladas que tienen uno o más centros de datos (hasta 8). Los centros de datos son edificios que tienen entre 50000 y 80000 servidores físicos.

Las regiones están completamente aisladas y separadas entre sí, y en cada AZ hay uno o más centros de datos en instalaciones independientes, y con líneas eléctricas y conexiones de red redundantes. Además, las AZ son zonas de error independiente. Todo esto se hace para aumentar la tolerancia a cualquier fallo. 

Además, el cliente puede seleccionar la región geográfica en la que más le conviene aumentar el rendimiento disminuyendo la latencia de red.

### Historia

![](2023-08-18-21-02-17.png)
![](2023-08-18-21-02-35.png)
![](2023-08-18-21-02-58.png)

1970s IBM lanza sus VM.
1990s Las VM se vuelven populares.
1999 Salesforce es uno de los pioneros en computación en la nube.
2002 Amazon lanza AWS.
2008 Microsoft lanza Azure.
2008 La NASA desarrolla las primeras nubes privadas e híbridas open-source.
2010 OpenStack hace una nube privada open-source DIY que se vuelve popular.
2011 Nubes híbridas
2013 Multinubes

**¿Qué se viene?**

Gartner es una consultora insternacional especializada en tecnología.

![](2023-08-18-21-07-41.png)

### ¿Qué se necesita  para tener un Data Center?

![](2023-08-16-16-25-35.png)

Mucho dinero. ¿Por qué?

- Sistema contraincendios
- Administrador de ancho de banda
- Servidor
- WAF
- SW
- Storage
- UPS
- ISP
- IDS/IPS
- FW
- BKP
- LCP
- Aire acondicionado de precición
- Transformador de aislamiento
- Estabilizador
- Piso falso
- Techo falso
- Generador eléctrico
- Luces de emergencia
- Repuestos
- Cableado estructurado


### Capex vs Opex

![](2023-08-16-17-39-02.png)

### Videos

Intro to AWS - The Most Important Services To Learn

https://www.youtube.com/watch?v=FDEpdNdFglI