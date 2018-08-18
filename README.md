

# Introducción

## Planteo del Problema

Se pretende describir cómo las características del Cloud Computing "a demanda” y "elasticidad” están presentes en el modelo de servicio de Plataform As A Service (PaaS). Se hará una introducción al concepto de PaaS, su uso y los diferentes ejemplos de servicios.

Para esto, primero es importante tener claro ¿Qué es Cloud Computing?.El "National Institute of Standards and Technology" (NIST) lo define como:

> Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications and services) that can be rapidlyprovisioned and released with minimal management effort or service provider interaction. This cloud model is composed of five essential characterstics, three service models, and four deployment models. [7] [NIST](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-146.pdf)

Asimismo, define las características esenciales del Cloud Computing:

> **_On-demand self-service_**. A consumer can unilaterally provision computing apabilities, such as server time and network storage, as needed automatically without requiring human interaction with each service’s provider.
> 
> **_Broad network access_**. Capabilities are available over the network and accessed through standard mechanisms that promote use by heterogeneous thin or thick client platforms (e.g., mobile phones, tablets, laptops, and workstations).
> 
> **_Resource pooling_**. The provider’s computing resources are pooled to serve multiple consumers using a multi-tenant model, with different physical and virtual resources dynamically assigned and reassigned according to consumer demand. There is a sense of location independence in that the customer generally has no control or knowledge over the exact location of the provided resources but may be able to specify location at a higher level of abstraction (e.g., country, state, or datacenter). Examples of resources include storage, processing, memory, and network bandwidth.
> 
> **_Rapid elasticity_**. Capabilities can be rapidly and elastically provisioned, in some cases automatically, to scale rapidly outward and inward commensurate with demand. To the consumer, the capabilities available for provisioning often appear to be unlimited and can be appropriated in any quantity at any time.
> 
> **_Measured Service_**. Cloud systems automatically control and optimize resource use by leveraging a metering capability at some level of abstraction appropriate to the type of service (e.g., storage, processing, bandwidth, and active user accounts). Resource usage can be monitored, controlled, and reported, providing transparency for both the provider and consumer of the utilized service. [7] [NIST](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-146.pdf)

Por otra parte, define al modelo de servicio **_Cloud Platform as a Service_** (Paas):

> The capability provided to the consumer is to deploy onto the cloud infrastructure consumer-created or -acquired applications created using programming languages and tools supported by the provider. The consumer does not manage or control the underlying cloud infrastructure including network, servers, operating systems, or storage, but has control over the deployed applications and possibly application hosting environment configurations. [7] [NIST](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-146.pdf)

# Desarrollo

## Analisis de casos de uso

El servicios de PaaS le proporciona a los consumidores la posibilidad desplegar sus aplicaciónes sobre la infraestructura de la nube, sin necesidad de administrar ni controlar la infraestructura, sino que tiene control sobre la aplicación implementada y la configuración del entorno de alojamiento de la aplicación.

## Analisis de Prestadores de Servicios

A continuación se menciónan dos proveedores de servicios conocidos en el mercado y se analiza las características esenciales de "elasticidad" y "a demanda" para cada uno.

### Amazon Web Services EC2 Auto Scaling

> Amazon Elastic Compute Cloud (Amazon EC2) es un servicio web que proporciona capacidad informática en la nube segura y de tamaño modificable. Está diseñado para facilitar a los desarrolladores el uso de la informática en la nube a escala de la Web.
> 
> Tiene una sencilla interfaz de servicios web de Amazon EC2 la que permite obtener y configurar la capacidad con una fricción mínima. Proporciona un control completo sobre los recursos informáticos y puede ejecutarse en el entorno informático acreditado de Amazon.
> 
> Amazon EC2 reduce el tiempo necesario para obtener y arrancar nuevas instancias de servidor en cuestión de minutos, esto permite escalar rápidamente la capacidad ya sea aumentándola o reduciéndola, según cambien sus necesidades. Amazon EC2 cambia el modelo económico de la informática, ya que solo tendrá que pagar por la capacidad que realmente utilice.
> 
> El escalado automático de Amazon EC2 ayuda a mantener la disponibilidad de las aplicaciones y permite aumentar o reducir automáticamente su capacidad de Amazon EC2 según las condiciones que defina. [4][Amazon EC2](https://aws.amazon.com/es/ec2/autoscaling/?sc_channel=ba&sc_campaign=ec2-autoscaling&sc_country=mult&sc_geo=mult&sc_category=mult&sc_outcome=aware)

Claramente esta solución cumple con todas las características esenciales de Cloud Computing. En lo que refiere a "elasticidad", los recursos se pueden aprovisionar en cuestión de minutos con la apariencia de contar con recursos ilimitados, en cuanto a lo referente "a demanda" puede aumentar automáticamente la capacidad de los recursos informáticos sin interacción humana, cobrando únicamente por los recursos realmente utilizados lo que reduce los costos de manera considerable.

### Mi Nube Antel

Este producto se define como una plataforma de autogestión especializada en la entrega de servicios en la nube en modalidad "as a Service", donde se puede disponer de un paquete estándar de servidores virtuales con despliegue y gestión en línea a través de un portal de administración de fácil acceso.

Al analizar esta solución lo primero que podemos apreciar es que la misma no es "elastica", se ofrecen paquetes de servidores privados virtuales con determinados recursos y períodos de suscripción mensuales y frente a un aumento o decrecimiento de la demanda, al estar suscripto a un contrato mensual, no se proporciona la capacidad de poder aumentar o disminuir respectivamente los recursos de manera rápida y elástica.

Esto también impacta en los costos porque de no estar usando la máxima capacidad contratada se estaría pagando por recursos que no se están utilizando.

En lo que refiere "a demanda" se puede ver que hay un panel de control, pero en ningún lugar se menciona el uso de una API para gestionar la plataforma. Así mismo, en algunos casos no se puede aumentar la capacidad informática de forma automática sin requerir intervención humana por que, en el proceso, la empresa tiene que verificar el cliente no cuente con deudas.

Por otra parte, se puede apreciar que cumplen con las otras características (acceso ubicuo, multi-tenencia, mediciones, resiliencia).

Al no cumplir dos de las características esenciales de la Cloud Computing se puede decir que no es una solución "as a Service", es un producto que claramente tiene varios puntos a mejorar. [6][Mi Nube](http://www.antel.com.uy/web/datacenter/inicio/-/asset_publisher/LxZ0YL2nowQu/content/servicios-en-la-nube/maximized)

## Analisis de Implementaciónes

### Amazon Web Services EC2 Auto Scaling

> Amazon EC2 presenta un auténtico entorno virtual de cómputo que permite utilizar interfaces de servicios web para lanzar instancias con distintos sistemas operativos, cargarlas con su entorno de aplicaciones personalizado, administrar sus permisos de acceso a la red y ejecutar su imagen utilizando los sistemas que desee.
> 
> Para utilizar Amazon EC2, simplemente se necesita:
> 
> -   Seleccionar una imagen de máquina de Amazon (AMI) de plantilla preconfigurada para que entre en funcionamiento de inmediato. O bien crear una AMI que contenga sus aplicaciones, bibliotecas, datos y valores de configuración asociados.
>     
> -   Configure la seguridad y el acceso a red en su instancia de Amazon EC2.
>     
> -   Seleccione los tipos de instancia que desee y, a continuación, inicie, finalice y monitorice tantas instancias de su AMI como sea necesario, a través de las API de servicio web o la variedad de herramientas de administración proporcionadas.
>     
> -   Determine si desea una ejecución en varias localizaciones, utilizar puntos de enlace de IP estática o adjuntar almacenamiento de bloques continuo a sus instancias.
>     
> -   Pague solo por los recursos que realmente consuma, como las horas de uso de instancias o la transferencia de datos.
>     
> -   Realizar el deploy de la aplicación utilizando la API antes mencionada.
>     
>     [4] [Amazon EC2](https://aws.amazon.com/es/ec2/autoscaling/?sc_channel=ba&sc_campaign=ec2-autoscaling&sc_country=mult&sc_geo=mult&sc_category=mult&sc_outcome=aware)
>     

Claramente esta realidad les permite poder hacer el deploy de las aplicaciones muy rápidamente y resuelve automáticamente muchos puntos en comparación a tener un centro de cómputos propio (mantenimiento, administración, personal, etc.)

# Conclusiones

El trabajo de investigación nos permitió conocer distintos servicios de PaaS y aprendimos como implementarlas en para crear poder hacer el desarrollo y despliegue de aplicaciones.

Pudimos apreciar que el servicio de AWS EC2 Auto Scaling cumple con todos los principios especiales de Cloud computing por lo que es una solución "as a Service" a diferencia de Mi Nube Antel que no lo es.

El desarrollo de aplicaciones en la nube es fundamental hoy en día. En la actualidad, cada vez más tendemos a utilizar aplicaciones donde sea que estamos desde cualquier dispositivo y el tener al alcance este tipo de servicios genera grandes oportunidades a las pequeñas empresas.

# Anexos

## Bibliografía

1.  A. 2012, 08. Entendiendo la nube: El significado de SaaS, PaaS e IaaS. Genbeta:dev. Obtenido 09, 2016, de [http://www.genbetadev.com/programacion-en-la-nube/entendiendo-la-nube-el-significado-de-saas-paas-y-iaas](http://www.genbetadev.com/programacion-en-la-nube/entendiendo-la-nube-el-significado-de-saas-paas-y-iaas)
    
2.  B. Stiller, T. Bocek, F. Hecht, G. Machado, P. Racz, and M. Waldburger, “Unidad didáctica 1. Introducción al cloud ¿computing,” Colegio de Ingenieros, Tech. Rep., Segunda Edición. .
    
3.  Amazon Web Services, Inc. (2018). _AWS | Elastic compute cloud (EC2) de capacidad modificable en la nube_. [online] Available at: [https://aws.amazon.com/es/ec2/?nc2=hm1](https://aws.amazon.com/es/ec2/?nc2=hm1) [Accessed 18 Aug. 2018].
    
4.  Amazon EC2 Auto Scaling. (2018). Retrieved from [https://aws.amazon.com/es/ec2/autoscaling/?sc_channel=ba&sc_campaign=ec2-autoscaling&sc_country=mult&sc_geo=mult&sc_category=mult&sc_outcome=aware](https://aws.amazon.com/es/ec2/autoscaling/?sc_channel=ba&sc_campaign=ec2-autoscaling&sc_country=mult&sc_geo=mult&sc_category=mult&sc_outcome=aware)
    
5.  (2018). Retrieved from [https://store.minubeantel.uy/index.php?NAME_PATH=VPS_HOSTING_WINDOWS](https://store.minubeantel.uy/index.php?NAME_PATH=VPS_HOSTING_WINDOWS)
    
6.  Servicios en la Nube - inicio - Antel. (2018). Retrieved from [http://www.antel.com.uy/web/datacenter/inicio/-/asset_publisher/LxZ0YL2nowQu/content/servicios-en-la-nube/maximized](http://www.antel.com.uy/web/datacenter/inicio/-/asset_publisher/LxZ0YL2nowQu/content/servicios-en-la-nube/maximized)
    
7.  (2018).nvlpubs Retrieved from [https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-146.pdf](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-146.pdf)
