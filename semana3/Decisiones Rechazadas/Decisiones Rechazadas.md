# Decisiones Rechazadas

## Nombre

* Detectar y almacenar datos

## Estado

{**Proposed** | rejected | accepted | deprecated }

## Problema de diseño 

* Se busca diseñar un sistema que pueda recibir los datos de los sensores y guardar dichos datos en una base de datos. 

## Identificador 

* D1 

## Solución 

## Justificación 

## Decision Drivers
* RF2

## Opciones consideradas 

* Singleton 

#

## Nombre
* Asignación de ordenes

## Estado

* **Rejected**

## Problema de diseño 

* Integrar la funcionalidad de asignar órdenes a operarios y que componentes fabrica cada máquina.

## Identificador
* D4.2

## Solución 
* Apalear con un Mediator la comunicación entre el cockpit, las máquinas y las personas.

## Justificación
* Al tener que ser un sistema escalable, es arriesgado usa un mediator ya que con el tiempo puede acabar convirtiendose en una godClass,es decir, una clase de la que dependen demasiados procesos.

## Decision Drivers
* RF1.1
* RF1.2

<!---
## Nombre
* Asignación de ordenes

## Estado

{**Proposed** | rejected | accepted | deprecated }

## Problema de diseño 

* Integrar la funcionalidad de asignar órdenes a operarios y que componentes fabricar a cada máquina. 

## Identificador 

* D3 

## Solución 

## Justificación 

## Decision Drivers
* RF1

## Opciones consideradas 

* Patrón Facade 

* Patrón Decorator 

* Patrón Command 

* Patrón Mediator
-->
