# Amazon Web Services (AWS) <!-- omit in toc -->

- [Semana 1. Introducción](#semana-1-introducción)
  - [¿Qué es la informática de la nube?](#qué-es-la-informática-de-la-nube)
  - [Ventajas de la nube](#ventajas-de-la-nube)
  - [Tipos de implementación de cómputo en la nube](#tipos-de-implementación-de-cómputo-en-la-nube)
  - [Modelos de servicios](#modelos-de-servicios)
  - [Infraestructura global](#infraestructura-global)
  - [Evolución](#evolución)
    - [Historia](#historia)
    - [El futuro](#el-futuro)
- [Semana 1. A lo concreto](#semana-1-a-lo-concreto)
  - [¿Qué se necesita  para tener un Data Center?](#qué-se-necesita--para-tener-un-data-center)
  - [Capex vs Opex](#capex-vs-opex)
- [Servicios de AWS](#servicios-de-aws)
- [Videos](#videos)
- [Semana 2. Clase 1](#semana-2-clase-1)


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

2. Te beneficias de la economía de escala masiva
    
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

La palabra _premises_ significa 'instalaciones'. Se trata de la temida e infame implementación de un centro de datos completo para soportar nuestra aplicación, con todas las complicaciones y gastos de tiempo y dinero que ello supone.

**Híbrido**



### Modelos de servicios

Los modelos de servicios se corresponden con el nivel de control y flexibilidad que tienes sobre los recursos TI.

**IaaS**

Ofrece el mayor nivel de control sobre los recursos informáticos, como conexión de red, máquinas virtuales y espacio de almacenamiento de datos. Contiene los bloques fundamentales para crear aplicaciones.

**PaaS**



**SaaS**


### Infraestructura global

![](sources/2023-08-21-14-44-28.png)

![](sources/2023-08-21-21-44-57.png)

Actualmente, la infraestructura de AWS está distribuida por el mundo en 32 regiones y 102 zonas de disponibilidad (AZ). Una región de AWS es un área geográfica que contiene varias AZ (al menos 3). Las AZ son ubicaciones aisladas que tienen uno o más centros de datos (hasta 8). Los centros de datos son edificios que tienen entre 50000 y 80000 servidores físicos.

Las regiones están completamente aisladas y separadas entre sí, y en cada AZ hay uno o más centros de datos en instalaciones independientes, y con líneas eléctricas y conexiones de red redundantes. Además, las AZ son zonas de error independiente. Todo esto se hace para aumentar la tolerancia a cualquier fallo. 

Además, el cliente puede seleccionar la región geográfica en la que más le conviene aumentar el rendimiento disminuyendo la latencia de red.

### Evolución

#### Historia

1960s: Se inicia el desarrollo de Internet como una red de comunicación entre organismos del gobierno de Estados Unidos.
1970s: Se introduce el concepto de máquina virtual, que permite crear entornos aislados y configurables dentro de un mismo servidor.
1990s: Se populariza el uso de Internet como una plataforma para ofrecer servicios y aplicaciones a los usuarios finales.
2000s: Se consolidan los proveedores de servicios de nube, como Amazon, Google y Microsoft, que ofrecen infraestructura, plataformas y software como servicio a través de Internet.
2010s: Se desarrollan tecnologías de contenedores y orquestación, como Docker y Kubernetes, que permiten empaquetar, desplegar y gestionar aplicaciones de forma más ágil y eficiente en la nube.
2015: Se funda la Cloud Native Computing Foundation (CNCF), una organización que promueve el desarrollo y la adopción de tecnologías de cómputo en la nube nativas, como Kubernetes, Prometheus, Istio y muchos más.
2016-2020: Se lanzan servicios de cómputo sin servidores, como AWS Lambda, Azure Functions y Google Cloud Run, que permiten ejecutar código sin necesidad de administrar ni aprovisionar servidores. También se lanzan servicios híbridos y multicloud, como AWS Outposts y Azure Arc, que permiten extender y administrar los recursos de nube desde cualquier lugar.


![](sources/2023-08-18-21-02-17.png)


**1960**

![](sources/2023-08-23-00-44-35.png)
- La idea de computadoras compartidas surge en torno a 1960.
- Las computadoras compartidas en sus comienzos eran máquinas muy grandes y costosas llamadas mainframes o centrales que podían ejecutar varias tareas al mismo tiempo, pero con una velocidad y capacidad muy limitadas.
- Las computadoras comparatidas no se desarrollaron mucho hasta los años 90.
- During 1961, John MacCharty delivered his speech at MIT that “Computing Can be sold as a Utility, like Water and Electricity.”
  
**1999**

![](sources/2023-08-22-23-52-26.png)
- Salesforce fue fundada en 1999.
- Salesforce demostró que se puede ofrecer un servicio de calidad a  través de Internet, siendo una de las primeras en ofrecer un servicio del modelo SaaS.
- Salesforce se encarga del CRM (Client Relation Management) de otras empresas. El CRM mejora los procesos de ventas, marketing, sevicio al cliente, gestión de proyectos, análisis de datos y otros aspectos del negocio.
- Salesforce ofrece soluciones para el sector financiero, sanitario, educativo, manufacturero, etc. 
- Algunas soluciones importantes: Sales Cloud, Marketing Cloud, Platform, MuleSoft, Tableau. Por ejemplo, Sales Cloud gestiona el ciclo de ventas (_sales cycle_ en inglés), desde la captación de clientes potenciales hasta el cierre de acuerdos.
- Algunas empresitas que son clientes de Salesforce: Spotify, Amazon, Adidas, Coca-Cola.

**2002**

![](sources/2023-08-22-23-53-31.png)
- AWS fue fundada en 2002.
- AWS es una empresa filial de Amazon (la empresa matriz o holding que gestiona AWS).
- AWS es una plataforma de servicios de computación en la nube.
- Salesforce migró su infraestructura a la nube de AWS en 2003, y fue una de las primeras. Desde entonces, AWS y Salesforce tienen una alianza estratégica mediante la cual ofrecen soluciones conjuntas a sus clientes.
- AWS lanzó sus primeros productos en la nube en 2006 (productos como S3 o EC2).
  
**2006**

![](sources/2023-08-22-23-46-32.png)
- Google Apps se lanzó en 2006.
- Google Apps es un conjunto de aplicaciones de productividad y colaboración en la nube ofrecido por Google. 
- Google Apps se lanzó como una versión para empresas de los servicios que ya ofrecía gratis: Gmail, Google Calendar, Google Docs.
- Google Apps fue añadiendo nuevas apps: Google Drive, Google Meet, Google Sites.
- Entonces, Google Apps ofrece SaaS. Pero también permite a los desarrolladores crear y ejecutar sus propias aplicaciones usando API.Por eso Google Apps también ofrece PaaS. Lo que no ofrece es IaaS. Google crea Google Coud Platform para ofrecer IaaS, y todo lo demás.
- Google Apps cambió su nombre a Google Workspace en 2020.

<br></br>
![](sources/2023-08-18-21-02-35.png)

**2008**

![](sources/2023-08-23-00-37-38.png)
- OpenNebula lanza su primera versión en 2008.
- OpenNebula fue creada en 2005 como un proyecto de investigación de la Universidad Complutense de Madrid.
- OpenNebula es una plataforma de computación en la nube de código abierto.



**2009**

![](sources/2023-08-23-00-40-16.png)
- Microsoft lanza Azure en 2009.
- Azure es una plataforma de computación en la nube que ofrece los tres modelos de servicios.

**2010**

![](sources/2023-08-23-00-37-07.png)
- OpenStack fue creada en 2010 por Rackspace y la NASA.
- OpenStack es una plataforma de cómputo en la nube de código abierto, al igual que OpenNebula.
- Tanto OpenStack como OpenNebula te permiten construir y gestionar infraestructuras de nube privada, pública e híbrida.
- OpenStack vs. OpenNebula:
  - Arquitectura: OpenStack tiene varios subsistemas gestionados por 14 subproyectos distintos, mientras que OpenNebula ofrece una plataforma integrada.
  - Modelo de gobernancia: OpenStack está impulsado por las necesidades de las empresas que participaron en su desarrollo, mientras que OpenNebula está impulsado por las necesidades de los usuarios finales.
  - Experiencia de usuario: OpenStack requiere una gran cantidad de tiempo y recursos para instalar, configuarar y mantener la plataforma, mientras que OpenNebula ofrece una solución que se puede instalar en minutos y es fácil de usar.
  - Compatibilidad: OpenStack tiene una mayor compatibilidad con otros proovedores de nube pública, como AWS.
  - Comunidad: OpenStack tiene comunidad más grande.
  - Variedad: OpenStack ofrece más opciones y funcionalidades para construir y gestionar la nube.

**2013**

- Los contenedores se popularizan gracias al lanzamiento de Docker.
- Los contenedores son entornos que empaquetan el código y todas sus dependencias para que puedan ejecutarse de forma aislada y consistente. Los contenedores les resolvieron la vida a los desarrolladores que tenían el famoso problema «en mi máquina sí funcionaba».
- Antes de los contenedores, el cómputo en la nube se basaba en VM (máquinas virtuales). Las VM ofrecían seguridad y aislamiento, pero por contra eran complejas, rígidas y consumían muchos recursos.
- Los contenedores han permitido una mayor agilidad y flexibilidad en el desarrollo de aplicaciones en la nube.
- AWS comenzó a ofrecer servicios de contendores desde 2014, cuando lanzó Amazon ECS (Elastic Container Service).

<br></br>
![](sources/2023-08-18-21-02-58.png)

**2014**

![](sources/2023-08-23-00-48-23.png)
- La CNCF se crea en 2014 (Cloud Native Computing Foundation).
- Antes de la CNCF, el cómputo en la nube era más heterogéneo y fragmentado. Había distintos proveedores, plataformas y estándares, y eso dificultaba la interoperabilidad de las aplicaciones.
- La CNCF promovió una mayor colaboración y armonía entre los diferentes actores del cómputo en la nube.

**2015**

![](sources/2023-08-23-01-10-14.png)
- Microsoft lanza Windows Server Containers
- Windows Server Containers se integra en el sistema operativo Windows Server 2016, como lo cuentan [en este artículo](https://learn.microsoft.com/en-us/archive/msdn-magazine/2017/april/containers-bringing-docker-to-windows-developers-with-windows-server-containers). 
- Taylor Brown es la cabeza detrás de proyectos como este, relacionados con la virtualización en Windows.



#### El futuro

Gartner es una consultora internacional especializada en tecnología.

![](sources/2023-08-18-21-07-41.png)

| Critical enablers | Productivity revolution | Smart world | Transparency and privacy |
|:---|:---|:---|:---|
| **Blockchain** <br/> **Foundation Models** <br/> Hyperautomation in Security <br/> Knowledge graphs <br/> **Hyperscale Edge Computing** <br/> Web3 <br/> **Tokenization** <br/> Neuromorphic Computing <br/> 6G | Edge Computer Vision <br/> **Edge AI** <br/> Model Compression <br/> Synthetic Data <br/> **Intelligent Applications** <br/> Generative AI <br/> Self-Supervised Learning <br/> <br/> <br/> | **Digital Twins** <br/> Multimodal UI <br/> **Smart Space** <br/> Spatial Computing <br/> Digital Human <br/> **Metaverse** <br/> <br/> <br/> <br/> | Human-Centered AI <br/> Digital Ethics <br/> Decentralizaed Identity <br/> Responsible AI <br/> <br/> <br/> <br/> <br/> <br/> |

**Las 4 tendencias tecnológicas**

- Critical Enablers (CE)

    Son tecnologías que funcionan como un pegamento para unir otras tecnologías emergentes. También remodelan las prácticas, procesos, modelos y métodos existentes en los mercados donde se aplican.

- Productivity Revolution (PR)

    Son tecnologías que impulsan la productividad de las personas, instituciones y máquinas, promueven la innovación, y permiten usar mejor los recursos.

- Smart World (SW)

    Son tecnologías que crean un mundo más inteligente, conectado y adaptable. Con tecnologías de smart world, los entornos físicos y virtuales integran datos, análisis, sensores y dispositivos.

- Transparency and Privacy

    Son tecnologías que promueven la transparencia y la privacidad de los datos, al permitir el control, el consentimiento y la verificación de los usuarios y las organizaciones.


**Las 9 tecnologías futuras más importantes** 

(orden alfabético)

1. Blockchain (CE)

   - El blockchain es un tecnología que permite crear redes descentralizadas y seguras. Estas redes se basan en cadenas de bloques, que son registros inmutables y verificables de las transacciones que ocurren en la red.
   - Con las redes de blockchain, los participantes pueden intercambiar información o valor sin intermediarios.
   - Aunque el blockchain se creó en 2008 y se le ha dado varios usos desde entonces, como los Bitcoin o NFT, aún no alcanza su máximo potencial.
   - El blockchain aplicado a las cadenas de suminitro podría ser una de las mayores disrupciones, y beneficiará tanto a proveedores como a consumidores porque aumentará la eficiencia (contratos inteligentes), la trazabilidad y la confianza (registro inmutable y verifibable por todos).

2. Digital Twins (SW)

    - Un digital twin copia cómo es y cómo funciona algo real. Es una representación virtual de un objeto, servicio o sistema real, que se actualiza continuamente con los datos y las condiciones del mundo real.
    - Un digital twin nos permite experimentar con diferentes escenarios y cambios, y luego aplicar las mejoras o soluciones en el mundo real.

    A lo Black Mirror

3. Edge AI (PR)
   
    - 

4. Foundation Models (CE)

    - Un modelo fundacional es una inteligencia artificial que puede adaptarse a diferentes tareas y dominios gracias a que aprende de grandes cantidades de datos no etiquetados. 
    
    - Estos modelos pueden generar conocimiento, lenguaje, imágenes, sonido o código. Un ejemplo de esto es GPT-3.

5. Hyperscale Edge Computing (CE)

    - Es una arquitectura de computación distribuida que aprovecha los recursos de hardware y software del borde de la red, es decir, cerca de las fuentes de datos y los usuarios finales.

    - Se utilizará para soportar las demandas de servicios en la nube cada vez mayores. Será utilizado especialmente donde se requiera baja latencia, alta disponibilidad y gran capacidad de procesamiento.

    https://www.youtube.com/watch?v=aKoIPbb_rCs

    https://www.e-spincorp.com/from-edge-computing-to-hyperscale-edge-computing/



6. Intelligent Applications (PR)



7. Metaverse (SW)

    - El metaverso un mundo virtual conectado a la Internet. En el metaverso los usuarios pueden interactuar entre sí y con el contenido digital del entorno usando realidad virtual o realidad aumentada.
    - En el metaverso podríamos jugar a juegos inmersivos con amigos alrededor del mundo, aprender nuevas habilidades como hablar en público o un nuevo lenguaje mediante escenarios simulados, o colaborar con compañeros de trabajo de una forma más cercana a pesar de la distancia.

8. Smart Space (SW)



9.  Tokenization (CE)

    - La tokenización es el proceso de convertir las cosas en tokens digitales.
    - La tokenización del dinero es muy interesante.


## Semana 1. A lo concreto

### ¿Qué se necesita  para tener un Data Center?

![](sources/2023-08-16-16-25-35.png)

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

![](sources/2023-08-16-17-39-02.png)



## Servicios de AWS

https://calculator.aws/#/addService

| Cómputo | Almacenamiento | Transferencia | Networking | Base de datos | Administración |
|:---|:---|:---|:---|:---|:---|
| EC2 <br/> ECS <br/> EKS <br/> Fargate <br/> Lambda <br/> Elastic Beanstalk | S3 <br/> Glacier <br/> EBS <br/> EFS <br/> FSx | Direct Connect <br/> Snowball <br/> STA <br/> Storage Gateway <br/> Kinesis Firehose | VPC <br/>  ELB <br/> R53 <br/>  | RSD <br/> DDB <br/> Aurora   | CloudFormation <br/> ClouWatch <br/> CloudTrail <br/> Config  |

**Cómputo**

- EC2
    - Elastic Computer Cloud
    - Servicio de instancia de cómputo
    - EC2 te permite lanzar y administrar servidores virtuales (instancias) en la nube. 
    - Te aporta capacidad informática para que puedas ejecutar tus cargas de trabajo.
- ECS
  - Elastic Container Solution
  - Servicio de contenedores.
  - ECS es un  que te permite ejecutar aplicaciones en contenedores Docker en la nube.
  - ECS te permite administrar y escalar tus contenedore.
- EKS
  - Elastic Kubernetes Service
  - Servicio de contenedores.
  - EKS es un servicio de Kubernetes totalmente administrado que te permite ejecutar aplicaciones en contenedores en la nube.
- Fargate
  - Servicio de contenedores.
  - Fargate es el motor informático de ECS.
  - Te permite ejecutar aplicaciones en contenedores sin preocuparte del aprovisionamniento y la administración de servidores.
  - Fargate aprovisiona, configura y escala los clusteres de máquinas virtuales para ejecutar los contenedores, todo sin que tengas que pensar en ello.
- Lambda
  - Servicio de cómputo sin servidor (completamente administrado).
  - Solo cargas tu código y Lambda hará todo lo necesario para ejecutarlo y escalarlo con alta disponibilidad.
  - Puedes configurar Lambda para ejecutar código automáticamente en respuesta a eventos.
- Elastic Beanstalk
  - Servicio de cómputo sin servidor (completamente administrado).
  - Elastic Beanstalk implementa y escala aplicaciones y servicios web desarrollados con Java, .NET, Node.js, Python, Ruby, Go y Docker en servidores familiares, como Apache o Nginx.
  - Elastic se encarga de la implementación automáticamente, desde el aprovisionamiento de capacidad y balanceador de carga hasta el escalado y el monitoreo del estado de las aplicaciones.
  - Esto no quita que se pueda acceder a los recursos subyacentes también.

**Almacenamiento**

- S3
  - Simple Storage Service
  - Servicio de almacenamiento de objetos.
  - Con S3 almacenas y recuperas datos en cualquier momento.
- Glacier
  - Servicio de almacenamiento de objetos.
  - Con Glacier almacenas datos a los que no necesitas acceder con frecuencia.
  - Almacenas datos a largo plazo.
- EBS
  - Elastic Block Storage
  - Servicio de almacenamiento de bloques.
  - Con EBS creas volúmenes de almacenamiento para adjuntarlos a instancias EC2.
  - EBS almacena datos persistentes para tus instancias de EC2.
- EFS
  - Elastic File System
  - Servicio de almacenamiento de archivos.
  - Completamente administrado.
  - Los sistemas de archivos de EFS son escalables y accesibles desde múltiples instancias EC2.
- FSx
  - Servicio de almacenamiento de archivos.
  - Completamente administrado.
  - Los sistemas de archivos de FSx son escalables y accesibles desde múltiples instancias EC2

> La principal diferencia entre EFS y FSx es:
    - EFS soporta Linux (compatible con el protocolo NFSv4).
    - FSx soporta Windows (compatible con los protocolos SMB y Lustre).

**Tranferencia de datos**

- DC
  - Direct Connect
  - Servicio de transferencia de datos
  - Direct Connect te permite establecer una conexión dedicada y privada entre AWS y tu centro de datos, tus instalaciones locales.
  - La conexión dedicada no se establece a través de Internet.
  - Direct Connect enlaza tu red con una ubicación de Direct Connect a través de un cable de fibra óptica Ethernet estándar.
  - El cable conecta tu router con un router de Direct Connect.
- Snowball
- STA
- SG
- KDF

**Networking**

- VPC
- ELB
- Route 53
  - 

**Base de datos**

- RDS
  - Relational Database Storage
- DDB
- Aurora
  - 
- ElastiCache

**Administración**
- CloudFormation
  - Permite crear y administrar recursos AWS de forma predecible y consistente.
  - La infraestructura se define y se implementa a partir de archivos de código.
  - La infraestructura se define en JSON o YAML, por lo que puede llegar a ser engorroso. Por eso existe el servicio CDK, que permite definir realmente la infraestructura con código.
- CloudWatch
  - Servicio de monitoreo.
  - Monitorea los recursos de AWS.
  - Con Cloud Watch puedes ver las métricas de cualquiera de tus servicios.
  - Puedes detectar y solucionar problemas.
  - Puedes establecer alarmas y reaccionar automáticamente a cambios en tus recursos de AWS.
- CloudTrail
  - Servicio de monitoreo
  - Monitorea el registro de eventos en tu cuenta de AWS.
  - CloudTrail audita tus recursos.
  - CloudTrail te permite saber quién hizo un cambio, cuándo lo hizo y dónde lo hizo (qué recurso cambió), así como asegurar el cumplimiento de las políticas acerca del uso de los recursos.
- Config
  - Servicio de monitoreo
  - Config se centra en cómo ha cambiado el recurso.

**Seguridad, identidad y conformidad**
- IAM
- WAF
- Cognito
- Detective
- Inspector
- Shield

## Videos

Intro to AWS - The Most Important Services To Learn

https://www.youtube.com/watch?v=FDEpdNdFglI


## Semana 2. Clase 1

En cuanto a la facturación en la nube, no se habla de cotizaciones, sino de estimaciones.

Aprende subneting. En la nube se ven redes muy elaboradas.

El Anti-DDOS separa las conexiones legítimas de las maliciosas. métodos de identificación antbots.