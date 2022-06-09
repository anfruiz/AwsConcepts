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
 