# AwsConcepts
## Modelos de despliegue en la nube
- *__Basados en la nube:__* Realizar todo el despliegue de las aplicaciones nuevas o existentes en la nube.
- *__On-Premise:__* Tener toda la infraestructura en data centers físicos y virtualizar algunos servicios. También se le conoce como "nube privada".
- *__Híbrido:__* Es una mezcla de los dos anteriores y comunico a ambas partes de la infraestructura.

## Beneficios de la nube
- Pasar de pagar por la infraestructura así no se use completamente, a pagar solo por lo consumido.
- No se debe preocupar por manteniemiento de la infraestructura en data centers físicos.
- Ya no se debe adivinar los recursos necesarios para desplegar una aplicación.
- Enconomía a escala, esto quiere decir que entre más clientes usen AWS, más dinero se puede ahorrar.
- Aumentar la velocidad y agilidad de despliegue de las aplicaciones.
- Llegar a todo el mundo en cuestión de minutos.

## Conceptos Generales
- Una __región__ tiene varias __zonas de disponibilidad__ separadas entre sí por 10 millas, y estas a su vez están compuestas por uno o varios data centers.
- Un __edge location__ es un data center designado para entregar contenido y servicios con la menor latencia posible a los paises donde no hay regiones cerca.
- A las __subnets__ se le configura las __*ACL (Access Control List)*__ las cuales por defecto vienen con permisos para permitir la salida y entrada del tráfico. Estas son stateless, es decir, si se aplica una regla pra tráfico entrante, esta no se aplicará en el tráfico saliente y viceversa.
- Los __security groups__ se configuran a nivel de las EC2, por defecto eststos no permiten ningun tipo de tráfico entrante o saliente. Estos son statefull.

## Pricing and Support
- *__Free Tier:__* Ciertos servicios son gratis al empezar durante un periódo o por siempre.
  - 12 meses.
  - Siempre gratis.
  - Trial.
- *__AWS Pricing Calculator:__* Este servicio permite realizar una simulación de cuanto se pagará por los servicios que necesitamos.
- *__AWS Billing and Cost Management Dashboard:__* En este se puede pagar facturas, monitorear usos y analizar y controlar los costos.
- *__AWS Budget:__* Este servicio permite crear presupuestos y alertas sobre cuanto quiero gastar al mes en determinado servicios.
- *__AWS Cost Explorer:__* Herramienta para visualizar, comprender y administrar los costos de los servicios utilizados por medio de reportes o gráficos.

### Support Plans
- *__Basic:__* Todos los clientes tienen acceso a este plan, el cual incluye:
  - Servicio al cliente y comunidades.
  - AWS Trusted Advisor en términos de rendimiento y seguridad.
  - AWS Personal Health Dashboard con una vista personalizada del estado de los servicios de AWS y las alertas cuando se afectan los recursos.
- *__Developer:__* Es recomendado si lleva a cabo pruebas en AWS.
- *__Business:__* Nivel mínimo recomendado si tiene cargas de trabajo de producción en AWS. A partir de este plan se tiene acceso a todos los niveles de AWS Trusted Advisor.
- *__Enterprise On-Ramp:__* Recomendado si tiene cargas de trabajo de producción o críticas para la empresa en AWS.
- *__Enterprise:__* Recomendado si tiene cargas de trabajo críticas o empresariales en AWS. En este plan se tiene acceso a un Technical Account Manager (TAM), el cual es una persona dedicado para ser el primer nivel de soporte y monitorear de forma proactiva los servicios.

Para tener una infomación más completa sobre que ofrece cada plan, acceder a este [link](https://aws.amazon.com/es/premiumsupport/plans/).

## Cloud Adoption Framework
Este servicio permite acelerar la transformación digital con la tecnología de la nube, sacando partido de la experiencia y prácticas recomendadas de AWS. Esto lo hace por medio de seis perspectivas:
- *__Business:__* Se centra en garantizar que las inversiones en la nube acelelren las metas del negocio y tecnología.
- *__People:__* Sirve como puente entre la tecnología y la empresa para ayudar a las organizaciones a evolucionar más rápido hacia una cultura de crecimiento y aprendizaje continuos, donde los cambios se conviertan en un proceso normal, con un enfoque en la cultura, la estructura organizativa, el liderazgo y el personal.
- *__Governance:__* Se enfoca en organizar las iniciativas de la nube con el fin de maximizar el valor del negocio minimizando el riesgo.
- *__Platform:__* Se enfoca en describir la arquitectura que se usará. 
- *__Security:__* Esta ayuda a lograr la confidencialidad, integridad y disponibilidad de los datos y cargas de trabajo en la nube.
- *__Operation:__* Se centra en garantizar que los servicios en la nube se entreguen a un nivel acordado con las partes interesadas de la empresa.

Si se quiere una información más profunda, acceder a este [link](https://docs.aws.amazon.com/whitepapers/latest/overview-aws-cloud-adoption-framework/welcome.html).

## Identity and Access Management (IAM)
- Por medio de este servicio se puede tener la creación de usuarios y configuración los diferentes accesos que tendrán dentro de la organización de forma centralizada.
- Los permisos se pueden dar de forma granular, es decir, por usuarios se pueden tener permisos muy específicos.
- También se puede activar el log in para que sea por medio de Active Directory, Facebook o Linkedin, activar MFA y cofigurar políticas en las contraseñas.
- Desde IAM se manejan __usuarios__, __grupos__ y __roles__.
- Por medio de los roles se le otorgan permisos temporales a usuarios, dispositivos o servicios.
- Por otro lado, están las *__IAM Policies__*, que son documentos que definen uno o muchos permisos. Son asignados a los usuarios, grupos o roles.
  
## EC2 (Elastic Compute Cloud)
Una EC2 es una "máquina virtual" que se puede usar para desplegar aplicaciones. Después de seleccionar el tipo de instancia, solo es necesario desplegar la aplicación y empezar a usarla.

### Tipos de instancias:
- *__Propósito General:__* Proveen un balance entre cómputo, memoria y recursos de red. Son ideales para servidores de aplicación o juegos, servidores backend o bases de datos pequeñas o medianas .
- *__Cómputo Optimizado:__* Pueden ser usadas para propósitos generales, sin embargo son recomendadas para tranajos o aplicaciones que requieran un alto performance.
- *__Memoria Optimizada:__* Como su nombre lo indica, están hechas para aplicaciones o trabajos que tengan un alto consumo de memoria o CPU.
- *__Computo Acelerado:__* Estas instancias utilizan aceleradores de hardware o co-procesadores para mejorar el rendimiento en la aplicación. Son ideales cuando se requiere graficar o hacer streaming de un juego.
- *__Almacenamiento Optimizado:__* Son ideales cuando requerimos un buen rendimiento en cuento a lectura/escritura en memoria. Cuando necesitamos rápidez al acceder a archivos del sistema.

### Tipos de Facturación:
- *__On-Demand:__* Se factura por el tiempo que se utiliza la instancia. Es ideal para cortos tiempos de uso o para trabajos que se deben ejecutar sin interrupciones de vez en cuando. En el caso en que se deba ejecutar continuamente durante un año o más, se recomienda otro tipo de facturación para optimizar costos.
- *__Saving Plans:__* En este se compromete a un uso de cómputo constante en un término de 1 - 3 años, permitiendo ahorrar hasta un 66% respeceto a on-demand.
- *__Reserved Instances:__* En este se hace una reserva de las instancias para uso propio durante un periodo entre 1 - 3 años; entre más tiempo se reserve mayor será el descuento. Se puede ahorrar hasta un 72% respecto a on-demand y es a nivel regional.
- *__Spot Instances:__* Este tipo de facturación es recomendada cuando se tienen trabajos flexibles en cuanto al inicio y fin de este sin afectar la operación del negocio. Permite ahorrar hasta un 90% respecto a on-demand.
- *__Dedicated Host:__* En esta se paga por servidores físicos con EC2 completamente dedicadas para el uso propio. Es la opción más cara de todas.

## Amazon S3
Este servicio de AWS permite almacenar cualquier tipo de objeto o archivo. Estos son alamcenados en buckets que son similares a carpetas. En estos no hay restricción en cuanto a memoria, pero el tamaño máximo de un objeto es de 5 TB.

### Tipos de S3
- *__Standard:__* Es recomendado para data que se requiere frecuentemente. Almacena la data mínimamente en tres AZ, es un poco costosa a comparación de los demás tipos.
- *__Standard Infrequent Access:__* Como su nombre lo indica, es recomendado para data que no se requiere con un acceso tan frecuente. Almacena la data de la misma forma que el standard, pero es un poco más barato, pero su precio aumenta al momento de recuperar el objeto. Cómo mínimo los objetos deben estar almacenados 30 días.
- *__Standard IA One Zone:__* Es igual que el Standard IA, pero como su nombre lo indica solo se almacena en una AZ. Tiene un ahorro del 20%.
- *__Intelligent-Tiering:__* Es una mezcla entre el Standard y el Standard IA, si el objeto no ha sido accedido en los últimos 30 días pasa a ser Standard IA.
- *__S3 Glacier:__* Es de bajo costo y para recuperar un objeto se puede demorar entre 1 minuto o 12 horas, los objetos se deben alamacenar mínimo 90 días.
- *__S3 Glacier Deep Archive:__* Es la oción más barata de todas, pero recupera los datos entre 12 horas o 180 días.

