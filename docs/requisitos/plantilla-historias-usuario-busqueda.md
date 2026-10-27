# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Fecha | [27/10/2026] |
| Versión | [Versión de trabajo] |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Como usuario registrado, quiero poder buscar recetas mediante palabras clave, frases, los ingredientes que quiero que tenga y los que no en un campo de búsqueda dedicado en un campo de búsqueda dedicado, para facilitar la forma de búsqueda y encontrar más rápido las recetas que quiero, aparte de prevenir reacciones alergicas al usarlos.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

## Justificación de la división

Se modula cada parte para mejorar la aplicación.


## US-01

**Título:** Buscar recetas mediante palabras clave

Como usuario registrado, quiero poder buscar recetas mediante palabras  clave o frases en un campo de búsqueda dedicado, para facilitar la forma de búsqueda y encontrar más rápido las recetas que quiero.

**Fuentes:** UR-08; UC-21; FR-085 ; acta, [apartado pertinente].

### Criterios de aceptación

- **CA-01.** Dado que existen recetas con la palabra clave azafrán, cuando el cliente la mete en el campo de búsqueda, entonces aparecerán las recetas con las coincidencias en una lista.
- **CA-02.** Dado que no existen recetas con la palabra clave por ejemplo no hay ninguna receta con huevo, cuando el cliente la mete en el campo de búsqueda, entonces no aparecerá ninguna receta y pondrá no hay resultados que coincidan con tus criterios de búsqueda.
- **CA-03.** Dado que no existen recetas con la frase exacta (arroz cocido), pero si una receta con arroz y con cocido de verduras, cuando el cliente la mete en el campo de búsqueda, entonces no aparecerá ninguna receta ya que se busca tal cual, y pondrá que no hay resultados que coincidan con tus criterios de búsqueda.

## US-02

**Título:** Buscar recetas por ingredientes seleccionados

Como usuario, quiero poder buscar recetas mediante los ingredientes en un campo de búsqueda dedicado, para facilitar la forma de búsqueda y prevenir reacciones alergicas al usarlos.

**Fuentes:** UR-08; UC-21; FR-086 ; acta, [apartado pertinente].

### Criterios de aceptación

- **CA-01.** Dado que existen recetas con los ingredientes elegidos azucar, cuando el cliente los mete en el campo de búsqueda y le da a enter, entonces aparecerán las recetas con las coincidencias en una lista.
- **CA-02.** Dado que NO existen recetas con los ingredientes elegidos como por ejemplo calabaza, cuando el cliente los mete en el campo de búsqueda y le da a enter, entonces no aparecerá ninguna receta y pondrá no hay resultados que coincidan con tus criterios de búsqueda.
- **CA-03.** Dado que NO existen recetas con todos los ingredientes elegidos como por ejemplo si hay con calabaza pero no con calabaza y azucar, cuando el cliente los mete en el campo de búsqueda y le da a enter, entonces no aparecerá ninguna receta y pondrá no hay resultados que coincidan con tus criterios de búsqueda.


## US-03

**Título:** Buscar recetas por exclusión de ingredientes seleccionados

Como usuario, quiero poder buscar recetas mediante los ingredientes que no quiero en mis recetas en un campo de búsqueda dedicado, para facilitar la forma de búsqueda y prevenir reacciones alérgicas al usarlos.

**Fuentes:** UR-08; UC-21; FR-086 ; acta, [apartado pertinente].

### Criterios de aceptación

- **CA-01.** Dado que existen recetas sin los ingredientes elegidos, por ejemplo pan , cuando el cliente los mete en el campo de búsqueda y le da a enter, entonces aparecerán las recetas con las coincidencias en una lista.
- **CA-02.** Dado que NO existen recetas sin los ingredientes elegidos (no hay recetas sin sal), cuando el cliente los mete en el campo de búsqueda y le da a enter, entonces no aparecerá ninguna receta y pondrá no hay resultados que coincidan con tus criterios de búsqueda.
- **CA-03.** Dado que el usuario sale de la selección sin buscar, cuando ya haya puesto la lista de ingredientes, entonces el sistema descartará las elecciones y saldrá de ese menú, dejando las selecciones en blanco para la próxima vez que el usuario vaya a buscar algo.


## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | No | Pendiente | Dependen de que haya un sistema de recetas ya implementado y funcional, aparte para hacer la 3º se necesita la 2º |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | Si | Pendiente | Se puede implementar de cualquier forma que el desarrollador elija, pero cumple con las necesidades del cliente si se realiza correctamente |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | Sí | Pendiente | Simplemente añaden una funcionalidad de realizar búsquedas entre las recetas que hay, y asi si explica |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | No | [Sí/No/Pendiente] | [Historias y motivo] |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | Sí | Pendiente | Si se centra, primero la búsqueda por palabra, luego por ingrediente y por ultimo por ingredientes no deseados |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | Si | Pendiente | Aparece como actúa el sistema al usarlo correctamente o incorrectamente o si simplemente no hay resultados. |

## Dudas pendientes

Se pueden poner palabra clave y ingredientes a la vez?
