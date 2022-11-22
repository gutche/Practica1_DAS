# Decisiones Aprobadas

## Nombre

* Recibir Datos de sensores

## Estado

* **Accepted**

## Problema de diseño 

* Se busca diseñar un sistema que pueda recibir los datos de los sensores y guardar dichos datos en una base de datos. 

## Identificador 

* D1 

## Decision Drivers
* RF2

## Solución

* Clase Cockpit
* Clase de filtración (API)

## Justificación

* El cockpit recibirá los datos proporcionados por los sensores, con el fin de que al cockpit le lleguen los datos clasificado se usará una clase intermedia de filtración.

# Nombre
* Almacenamiento de órdenes y suministro

## Estado

* **Accepted**

## Problema de diseño 

* Almacenar las órdenes de trabajo por operario y el suministro disponible. 

## Identificador 

* D2 

## Decision Drivers
* RF3.1
* RF3.2

## Solución
* Componente Base de datos
* Patrón Singleton

### Justificación
* Para el almacenamiento de datos se crearán diferentes tablas en una base de datos SQL. Con el fin de almacenar la información necesaria para la ejecución de ordenes y la gestión de los suministros. 
* Se hará uso del patrón de diseño Singleton para la creación de la instancia de la base de datos.

## Nombre
* Notificaciones

## Estado
* **Accepted**

## Problema de diseño 

* Notificar a los operarios sobre los distintos eventos a los que estén suscritos.  

## Identificador 
* D3

## Decision Drivers
* RF4.1

## Solución
* Pub-Sub

## Justificación
* La necesidad de notificar diversos tipos de eventos, nos lleva a pensar que necesitamos un mecanismo que pueda notificar a los distintos operarios sin someter al cockpit a extremada presión.
* Para poder relegar esta funcionalidad, emplearemos el patrón observer basado en eventos, de modo que el cockpit solo necesitará una lista de eventos. 
* El patrón pub-sub permite que la escalabilidad sea más asequible. Ya que la creación de nuevos eventos no ocasione grandes cambios en las demás estructuras, ya que heredan de una clase abstracta.
