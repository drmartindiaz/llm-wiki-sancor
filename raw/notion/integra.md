---
source_url: https://app.notion.com/p/2e72c02ab019802dbc23ea1b2d80c239
ingested: 2026-07-08
title: Integra
notion_id: 2e72c02a-b019-802d-bc23-ea1b2d80c239
---

▶ **20260113 Fer Ghione**

<!-- unknown block type: transcription (2e72c02a...) -->



### Objetivo de la Reunión

El objetivo principal fue revisar qué datos está generando Integra para incorporarlos a los tableros operativos, particularmente el tablero operativo ambulatorio.  

### Estado de Implementación de Integra

- **Cobertura actual**: 85% de casos ambulatorios (F4) están implementados en Integra  
- **Vías de ingreso**:
- 85% a través del equipo administrativo de autorizaciones (Dirección de Operaciones) 
- 15% cargado por el equipo de experiencia en los CARs (implementación inminente - 13 de enero) 
- 1% restante sigue en Fluir (casos excepcionales y fuera de alcance)  
- **Cobertura esperada**: Febrero será el primer mes con datos completos de ambulatorio e internaciones  
### Estructura de Integra en Salesforce

**Dos procesos principales** :

- **Proceso administrativo de autorizaciones**: Liderado por Vicky Costa Maña (Dirección de Operaciones)
- Gestión completa migrada de Fluir a Salesforce 
- Incluye autorización automática por motor de reglas 
- Genera caso padre de autorización 
- **Proceso de auditoría médica**: Liderado por Fernando
- Casos que requieren auditoría generan un caso hijo automáticamente 
- Antes no se tenía reportería de auditoría, solo del universo de autorizaciones  
### Mejoras Implementadas en Integra

**Diagnósticos**  :

- Búsqueda a través del servidor de terminología del italiano (SNOMED)
- Vinculación automática a CIE-10
- Validación obligatoria por auditor médico antes de cerrar caso
- Objetivo: Generar datos de calidad para trabajo proactivo
**Solicitud de documentación**   :

- Nueva funcionalidad que permite al auditor solicitar documentación directamente al asociado
- Envío automático de mails con link para carga de documentación
- Sistema de seguimiento: 48 horas + 24 horas adicionales
- Cierre automático del caso si no se recibe documentación  
- Todavía mejorable - faltan algunos escenarios 
**Datos de solicitante y acreedor**  :

- Solicitante es campo obligatorio
- Actuante no es obligatorio (tema de proceso, no de sistema)
- Todos los datos están relacionados y trazables 
### Revisión del Tablero Operativo Ambulatorio

**Estructura actual del tablero**  :

- F4 totales por mes con distribución de estados (autorizados, auditoría posterior, pendientes, rechazados)
- Distribución por equipo (discapacidad, auditoría médica, administrativo, especialistas) 
- Rankings por prestaciones (psicología, fonoaudiología, kinesiología dominan el volumen) 
- Ranking de acreedores
- Detalle de performance por auditor 
- Distribución de motivos de auditoría
**Problemas de calidad de datos identificados** :

- Datos hasta noviembre/diciembre provienen de sistemas viejos
- Ranking de acreedores muestra datos inconsistentes (P9999, ceros, "reintegros")  
- Ranking de prescribientes con alto porcentaje de datos faltantes o mal cargados (P0, "no definido en origen", 9999)  
- En enero se observa mejora en prescribientes, pero el tablero necesita revisión para asegurar correcta captura de datos de Integra  
### Alcance Fuera de Implementación Actual

**Casos que permanecen en Fluir** :

- Trasplantes
- Bariátrica
- Medicamentos de autorización previa
- Excepciones
**Próximos pasos de implementación**  :

- Internaciones (objetivo: enero)
- Auditorías de movimientos afiliatorios
- Servicio para levantar casos del sistema viejo e impactarlos automáticamente en Salesforce
### Temas Pendientes de Definición

**Auditoría de facturación posterior**   :

- Proceso actual "sujeto a auditoría posterior" no genera trabajo efectivo en auditoría de facturación
- Se usa solo como resguardo legal para el prestador
- Existe proceso informal de sugerencias de débito del auditor de terreno 
- Necesidad de definir criterios claros para derivación formal   
### Reportería en Salesforce

- Salesforce tiene sistema propio de reportería para monitoreo en vivo 
- No reemplaza tableros oficiales
- Utilizado para seguimiento de productividad y pendientes   
- Situación actual: 88 casos pendientes en ambulatorio, buen cumplimiento de SLA 
### Action Items

- [ ] Equipo de tableros: revisar que el tablero esté capturando correctamente los datos de Integra 
- [ ] @Martín M. Diaz Maffini coordinar con GDI la creación de tablero punta a punta que incluya todos los tipos de formularios (F4, F57, F6) 
- [ ] Equipo: separar en el tablero los casos rechazados de las solicitudes de documentación para tener KPIs más precisos 


El objetivo de la reunión es ver que datos esta generando Integra para incorporarlos a los tableros particularmente al operativo ambulatorio



y estamos más o menos todos alineados. La idea es juntarnos un ratito para que nosotros estamos viendo los tableros ambulatorios, de operativos, y tenemos algunas dudas, desconocimiento básicamente, de que de toda esa información que estamos levantando de diferentes...

orígenes, iba a poder brindar íntegra probablemente toda y alguna más y bueno nada, la idea de juntarte con vos era que de lo que pudiéramos ver un poco qué repartir

reportería en sí, sino los datos que te genera algo íntegra y qué potencia tiene con eso. ¿Tenés más o menos el tablero, este cangulatorio que te digo yo, o querés que te lo abre y lo vemos para que veas más o menos por dónde viene la mano? Dale, empecemos desde ahí, si vos no lo querés proyectar, yo te doy... Sí, bájame que va a tardar un rato en abrir, si querés arranquemos por otro lado... Dale, bueno, mira, yo mientras te muestro sólo a modo de compartirte...

¿Será así? Antes de ponernos a ver esto. Nosotros cuando implementamos íntegra, bueno, viste que íntegra tiene como dos patas, la parte más administrativa de la carga de la autorización y la parte de auditoría médica. el lado administrativo, que es lo que lleva la agencia de Stefi, que está en la Dirección de Operaciones, que tiene a Vicky Costa Maña como PO, que sería como par mía.

del lado de autorizaciones, armaron todo el parodón, Vicky Costamaña, Victoria Costamaña, ella le reporta a este fin. Armaron todo el proceso de autorizaciones, que antes se gestionaba en Fluir, y lo llevaron todo a Salesforce. Entonces ahí también hay un traspaso bastante grande.

Respecto de la gestión de la autorización, después de esa gestión de autorización Puede requerir auditoría médica o no, ¿Sí? Y si de todo lo que no requiere auditoría médica es 100% dentro del proceso de... de autorizaciones, y de lo que hay que hacer. Claro, hasta ahora tenemos solo ambulatorio que son los F4, pero esos F4 pueden requerir auditoría médica o no.

Sí, por ejemplo, no se me ocurra ahora ninguna prestación, pero hay algunas prestaciones que directamente el motor de reglas las dispone como de resolución administrativa, o sea, se cargan y se autorizan automáticamente, no las tiene que ver un usuario.

Sí, sí, no pasa nunca auditoría médica. Exactamente, entonces eso lo carga directamente el equipo administrativo, el motor le devuelve un autorizado, emite el formulario F4 y se manda al asociado barra prestador y se resuelve. y después todo lo que requiere auditoría médica, hacen toda la carga administrativa y se deriva a auditoría médica, ahí se genera otro caso para que el auditor médico...

revise esa solicitud, y ahí es donde entro yo con todo lo que tiene que ver con auditoría, ¿sí? Yo, para mapearte más o menos, que son dos mundos que están totalmente conectados, pero que están separados. ¿Por qué eso es importante? Porque nosotros, olvídate de Salesforce previo a Salesforce previo a íntegra, nosotros teníamos información casi exclusivamente, creo que es eso,

tomaba una partecita, del mundo autorizaciones, y prácticamente nada de auditoría. O sea, lo que hacía auditoría era recibir solicitudes, resolverlas, y mandar una respuesta a autorizaciones. Entonces, toda la información se tomaba desde el universo autorizaciones, incluía esa respuesta de auditoría médica que le mandaba.

Pero datos como, por ejemplo...

tiempos de gestión, un reporte de pendientes en auditoría, todo lo que vos querías saber de auditoría tenías que ir al universo de autorizaciones, a ver en qué estado estaba esa autorización ¿Tenía algo pendiente? Auditoría no tenía reportería no tiene nada. Nosotros cuando llevamos estos dos procesos de autorizaciones y de auditoría a Salesforce, la premisa fue, tenemos que llevar todo exactamente igual que como está hoy para no perder datos de los tableros.

¿Sí? Y si podemos incorporarle cosas, le vamos a incorporar y vamos a generar indicadores nuevos, como por ejemplo productividad y algunas cosas que no teníamos. Pero el primer objetivo fue... Como nos seguimos integrando con los mismos servicios, vamos a usar las mismas tablas. Entonces la información se guarda en las mismas tablas, eso a nosotros nos aseguró...

que toda la información que nosotros teníamos se mantenga, ¿sí? Porque los servicios que usamos son los mismos, las tablas donde guardamos la información son las mismas. Por lo tanto tendríamos que tener exactamente la misma información capturada desde el mismo lugar. ¿Qué tenemos que sumarle a eso? Todo lo nuevo. Entonces en un primer...

como se llama, en un primer MVP, nos juntamos con el equipo, con Ana, empezamos a ver todo este tema de tabla y dijimos, bueno, listo, ya nos aseguramos que lo mínimo indispensable, que era lo que ya teníamos desde antes, lo podamos mantener, y así entiendo que está.

Creo que lo que tenemos que empezar a trabajar ahora es en qué datos nuevos nos das. herramienta, que a lo mejor antes no teníamos, para ver cómo los atrijecemos. Creo que ese sería un diagnóstico principal. Dicho todo eso, yo insisto, tengo solamente la parte de...

de auditoría, pero te empiezo a contar un poquito lo que hay acá, al menos acercándome al tablero. Una pregunta. Hoy, el 13 de enero, digamos, la implementación de... digamos de íntegra con respecto a ambulatorio poner a los f4 que entran está el 100% no pero casi

Hoy tenemos implementado el mundo ambulatorio en un 85%. ¿Por qué? Por el origen del caso. Los casos de ambulatorio tienen dos vías de ingreso, a través de carga en el sistema, vamos a decir. A través del equipo administrativo de autorizaciones, se reporta la dirección de operaciones.

y el otro 15% lo carga el equipo de experiencia, de atención en los CARS, cuando el asociado va con el pedido médico y se lo carga el oficial de experiencia directamente en el sistema. Eso representa el 15%. Ese 15% todavía no está implementado, pero creo que se implementa hoy, y si no es hoy, es mañana. Ah, perfecto. Ya está, digamos. Ya prontito vamos a tener todo.

por este... ¿Cómo se llama? Por webservers, por... Exactamente, eso viene por... Fundamentalmente, autojectuar es casi todo internaciones. Ahí en la ambulatoria creo que no vas a tener nada. Pero sí, todo lo que viene por autogestión del asociado eso va directamente al equipo administrativo de autorizaciones. Entonces ellos son los que lo cargan. Y eso representa el 85%. Y esta es la gente... Ah, no. Esto es auditorio.

médica por lo que veo en los nombres. Esto en realidad lo que estamos viendo es auditoría, sí, ahí me meto con eso. ¿Qué te queda? Yo te dije 85-15, en realidad debe ser 84-15, porque hay un 1%, algo muy, muy, muy chiquitito. del mundo ambulatorio, que por ahora sigue cargándose en el sistema viejo que es Fluir, y llegando al sistema viejo de auditoría que es la web de auditoría. Son casos de...

excepciones, en donde o se tiene que hacer una carga por el AS, que es el sistema que salta el motor de reglas, o son casos que quedaron fuera del alcance del proyecto de autorizaciones. Es algo muy chiquitito. Más que nada creo que es de internaciones, pero hay una pequeña partecita que puede quedar afuera, pero después todo esto está abarcado en estos dos mundos.

Dicho todo eso, te muestro un poquitito de lo que tenemos en Salesforce. Salesforce tiene un sistema propio de reportería, que no tiene aspiraciones de ser el reporte oficial de información, es solamente una herramienta que tiene. que te sirve para ir viendo algunas cositas, pero que no reemplaza para nada el tablero, ni nada de eso. A nosotros nos sirve para monitorear en vivo algunas cosas. Esto, por ejemplo...

Yo acá tengo dos reportes que miro casi siempre.

En donde este es un reporte de productividad, nosotros estamos siguiendo como tuvimos después de la implementación, un cuello de botella. en donde se nos empezaron a juntar casos por que el usuario se estaba adaptando a la herramienta, por errores que teníamos en casos que teníamos que corregir puntualmente, caídas del sistema y cosas que nos fueron pasando en la implementación.

estábamos un poco preocupados por la capacidad operativa real que teníamos en esas condiciones versus los andresos. Entonces esto lo monitoreamos casi todos los días. Este es un resumen de pendientes. Yo saco acá abajo, este es un resumen de pendientes, entonces yo acá veo que tengo 88 casos pendientes, de los cuales, de lo que es la clasificación ambulatoria, que es el ambulatorio común,

Tengo 9 casos vencidos, que ya los tengo vistos, son 9 casos que tienen errores, que estamos terminando de corregir, 5 que están próximos a vencerse y 34 dentro del SLA. Venimos muy bien, tenemos un SLI que se fue mal, así que la verdad que venimos bien. Esos nueve que tienen errores, ¿te referís a errores, digamos, cuando se cargó el caso? ¿O son errores, no sé, en el proceso? El sistema. Ah, bueno. El sistema. Tenemos algunos servicios que todavía nos están fallando.

Son los más que estamos tratando de corregir, digamos. Exactamente, son bugs que estamos terminando de corregir, sí. Bien, eso es lo que es ambulatorio normal, después tenés también dentro de lo que es el universo ambulatorio, pero ya tipificado como discapacidad.

donde acá tenemos algunos casos, lo que es ambulatorio pero tipificado como especialidad, acá hay cardiología, hay todo lo que es especialidad, tal cual. Entonces ahí tenemos 25 casos, 14 vencidos. Y de internaciones, que en realidad no es internación es esto, sino que son aplicaciones de algunos medicamentos, son casi todos casos de hierro. ¿Por qué están acá?

Son casos que se tipifican como de internaciones, que los resuelve el equipo zonal de internaciones de auditoría médica, pero que carga el equipo de ambulatorio. Es como una inconsistencia más de estructura de equipos que otra cosa, entonces por eso está acá.

Pero bueno... Se llama como hospitalidad con el empeor de los casos. Sí, sí, tal cual. Entonces esto es solamente para mostrarte qué es lo que tiene Salesforce. Acá si a vos te interesa... model de un usuario, te ponés a revisarlos, a jugar con total tranquilidad. Y acá un reportecito normal de productividad, donde vamos viendo...

cuántos casos vamos sacando por día a colugueses. Y después, como para mostrarte alguna cosita, que puede ser interesante...

Esta es la estructura de un caso de autorizaciones, que es el de arriba, y de auditoría, que es el de abajo. Viste que yo te decía, el proceso padre es el de autorizaciones, que está representado dentro de este caso de acá. Este caso, con este número de casos,

Epa, lo vamos a abrir acá. Este caso es el caso administrativo de autorizaciones. Lo carga el equipo administrativo, completa cuáles son las prestaciones que se tienen que... que autorizar, sube la documentación en la parte de archivos, hace todo lo que tiene que ver con la carga administrativa, después invoca el motor de regla, y el motor de regla le devuelve.

un autorizado o un requiere auditoría. Este caso, acá fíjate en la barra de estado, figura en auditoría, o sea, esto se derivó a auditoría, por lo tanto generó automáticamente este segundo caso de acá. que es el caso que tiene Auditoría Médica pendiente. Que es un caso prácticamente igual, con alguna pequeña modificación en la visualización, en donde el auditor médico ingresa y analiza las prestaciones, confirma...

o modifica los diagnósticos que vienen recargados, mira los archivos que le cargaron, puede hacer un pedido de documentación y demás. ¿Y se gestiona, digamos? Gestiona todo lo que tiene que ver con auditoría. Viene en sus propios estados, tal cual, exactamente. Un poco para hacer tiempo, mientras cargaba el tablero, a mostrarte un poquitito cómo es la...

Es truco.

¿Qué más? No hay mucho, mucho, mucho más. Tiene como pasos fundamentales, por lo menos, lo que es la parte de auditoría. tiene la visualización de documentos, cosas que hacen siempre los auditores, ¿no? Visualización de documentos también.

El control prestacional, acá, que básicamente te dice el motivo de por qué se derivó ese caso a auditoría médica, y te genera algunas alertas. como, por ejemplo, si tiene una posible preexistencia por antigüedad del asociado, te lo marca el control, es lo mismo que teníamos antes. Acá tenemos un cambio importante en diagnósticos,

Nosotros usamos todos los diagnósticos de SID-10 en el sistema anterior, se cargaban también de SID-10, pero como era tan difícil llegar al diagnóstico, porque muchas veces el administrativo no conocía exactamente o no... no entendía bien la letra, el auditor no lo revisaba prácticamente, el diagnóstico era un dato que nosotros no teníamos de manera correcta. Lo que nosotros implementamos ahora es una validación de diagnóstico, una primera capa.

de SNOMED, el servidor de terminología del italiano, para que sea más fácil de buscar, eso está todo vinculado al diagnóstico de C.E.10, y seguimos persistiendo el diagnóstico de C.E.10, pero buscando desde Snowmed, pero fundamentalmente el cambio es que le agregamos una validación obligatoria al equipo de auditoría. Todos los casos de auditoría médica vienen con un diagnóstico precargado, pero el caso no se puede cerrar hasta que el auditor no confirma o modifica el diagnóstico.

Esto para empezar a generar datos de calidad, de diagnósticos calidadados por auditores médicos, que después nos permitan trabajar en algo proactivo. ¿Buscan en Nomad en el servidor del italiano? Sí. ¿En el servidor del italiano no buscan en Nomad? En realidad...

Por lo que me explicaron a mí, son como tres capas distintas, que están todas vinculadas. Vos buscás con el servidor del italiano, pero todos los términos del italiano tienen una vinculación a uno de SNOMED, y ese de SNOMED tiene una vinculación al de SIDE10.

Nosotros no los estamos mostrando, pero sí estamos persistiendo los tres datos. Ok.

saco ahí. ¿Quién está en la parte, digamos, de terminología? ¿Es alguien nuestro o es algo que hizo la gente de Globant? digamos. No, es nuestro, esos servicios son nuestros. ¿Cómo se llama este chico? Santi, ¿vas a ser maestro? Sí, sí, Santi. Sí, por lo menos él está como líder de ese equipo. Sí, sí, era el líder del equipo en el italiano cuando yo lo usaba, así que...

Ahí va, sí, sí, esto lo armó todo él. Después otra cosa que tiene nuevo, que no teníamos antes, es la funcionalidad de solicitud de documentación, como cosas que van cambiando. ¿Qué pasaba antes? El auditor médico, en general, cuando tiene alguna sospecha de preexistencia, cuando tiene alguna resolución de algún caso un poco más complejo, lo que hace es pedir documentación extra, estudio complementario extra, sospecha de una preexistencia, pide una historia de clínica más detallada, con fechas de diagnóstico y demás.

Eso volvía al equipo administrativo, el caso volvía para atrás hacia el equipo administrativo, el equipo administrativo se encargaba de rastrear la documentación de alguna manera. ¿Metió un rechazo por documentación o alguna cosa? Sí, lo rechazábamos y el equipo administrativo se encargaba de buscarla, a veces la encontraba, a veces no, y se quedaba todo como rechazado. Ahora implementamos una funcionalidad que está buena, pero todavía tiene que seguir creciendo, porque no.

llegaron afuera un par de escenarios, donde el auditor hace un pedido de documentación desde este botón de acá arriba, tratar de no avanzarlo todo, ¿no? Pero yo desde acá... pido documentación, entonces lo que hago es generar un link desde acá y mandarle al asociado una plantilla, que ya está precargada.

¿Qué dice? Buenos días, señor asociado, en relación a su autorización número 158608078, la está realizando el equipo de auditoría médica para poder avanzar con su trámite, vamos a necesitar... dos puntos, y esto que escribe el auditor acá. Necesita de historia clínica completa de Sarasa Sarasa. Le agradecemos, que por favor lo envíe dentro de las próximas 48 horas para que podamos resolver. ¡Felicitud!

manda el mail al asociado y este caso queda en un estado en esfera de documentación. Si el asociado ingresa y carga la documentación en el link, automáticamente carga la documentación y el caso vuelve a ingresar a Auditoría Médica. Si pasan 48 horas y el asociado no subió la documentación, se le manda un segundo aviso diciéndole, yo lo digo en criollo, ¿no? ¿Te acordás que te pedí la documentación? Bueno, te habíamos dado dos días, no lo subiste, te damos 24 horas más, subí la documentación a este link, si no, vamos a tener que cerrar el caso y lo vas a tener que cargar de nuevo.

Le dan 24 horas más. Carga la documentación, entra automáticamente a auditoría, no ingresa la documentación, se le manda una última notificación que dice, no recibimos la documentación. Te pedimos que, si tenés que avanzar con la gestión de la autorización, te vuelvas a contactar con el equipo de experiencia. Y el caso se cierra automáticamente. Esa es la funcionalidad de documentación.

¿Por qué digo que es mejorable? Porque nos faltan algunos escenarios que estamos desarrollando, como por ejemplo, no tengo más documentación, ¿qué nos pasa? Después de estas pruebas vemos que la sociedad lo llama al CAR y dice, che, yo no tengo más nada, ¿qué hago?

¿no me van a autorizar nada? Hay algunos escenarios que nos quedaron un poco afuera que estamos tratando de hacer crecer Pero como funcionalidad está bastante bueno Y después tenemos la... ¿Pinta bien? Sí, me parece que sí, me parece que sí, que va a tener un buen...

Un buen impacto. Y bueno, no hay mucho más para mostrar. Después todo lo que tiene que ver con tableros, me parece, no los conozco demasiado. Pero me parece que en función de la información transaccional, toda la información está, la identificación del cliente está, las prestaciones están, los diagnósticos están.

están, los resultados de cada una de las prestaciones están. ¿Tenés, perdón, te pregunto, ¿tenés algún...

por acreedor o por los chefes cuatro, digo, ¿no? ¿Alguna forma de verlo? ¿O por acreedor o por solicitante? Sí, dentro del caso de autorización, no desde auditoría, pero desde la autorización. Vos tenés, si lo encuentro.

El solicitante es obligatorio, el actuante no, pero entiendo que es más un tema de proceso que de sistema, porque para cargar una autorización no es obligatorio indicar el actuante. Vos podés hacer eso, así van en cualquier lado, pero el solicitante sí, el dato está.

Y está, no es un campo de texto, o sea, este es un account dentro de Salesforce con el prestador identificado, su número, sus datos y demás. Bien. O sea que sí. El solicitante. ¿Y después? No, estamos hablando, sí. El solicitante. Todos los datos están relacionados con todo. O sea, todo lo que vos ves acá, levantás desde el Luis Carabajal y querés ver todos los casos que se cargaron para él, tanto de los administrativos como los que fueron auditoría, más la resolución de auditoría, más quién fue el auditor que...

todo eso se puede levantar.

errores de datos tenemos en los tableros, digo, por un tema como decías vos probablemente de proceso, de carga o de lo que fuere. Todo esto está siendo alimentado obviamente, yo tengo hasta noviembre o diciembre, no me acuerdo, ahora me fijo bien, está siendo alimentado por sistemas viejos, no por íntegra y tenemos bastante quilombo con eso, cuando querés ir a ver un poco por acreedor o por solicitante, falta mucha info.

Yo se te preguntaba específicamente, pero si lo tienen controlado por el mismo sistema, me parece que va a ser más mejor. Me quedé colgado con algo también. La carga primaria del F-4 por parte de experiencia del CAR, digamos, ¿va a seguir siendo el mismo sistema y va a impactar acá en este CRM?

No, lo carga directamente acá en CRM. Ah, primariamente acá. Genial, perfecto. Si obviamente lo del asociado lo cargan en el portal del asociado, Impacta acá. Claro, sí, sí, exactamente. O sea que ya te digo, todo va a terminar cargándose acá. Entiendo yo que el proyecto de autorizaciones dejó algunas, como te decía antes, algunos temas fuera de alcance, que no se van a implementar ahora en esta primera etapa.

De los que recuerdo así rápido, te puedo decir, trasplantes, bariátrica, medicamentos, medicamentos de autorización previa, medicamentos no los de provisión, sino los que se compran en farmacia. Y todo lo que tiene que ver con excepciones no están incluidos dentro del alcance, del primer alcance del proyecto de autorizaciones. ¿Qué quiere decir? Que se van a seguir cargando desde Fluir como se cargaban antes.

Eso es dentro de la parte de autorizaciones. En auditoría médica nosotros lo que desarrollamos es, o lo que estamos armando en realidad cuando terminemos con este, ahora estamos en ambulatorio, el siguiente paso es implementar todo lo que tiene que ver con internaciones.

Y después algunas otras cositas chiquititas más que no tienen que ver con autorizaciones en sí mismas, auditorías de movimientos, afiliatorios y otras cosas. Y después lo que vamos a hacer es un servicio que nos levanta directamente de las bases de datos todos estos casos que se van a seguir cargando desde el sistema viejo, van a estar en la base de datos.

para que nos los impacte automáticamente en Salesforce. Entonces auditoría sí va a tener, dentro del primer alcance, el 100% de los casos en Salesforce. Estamos yendo progresivamente. Autorizaciones, no. Ya tiene planteado que una parte no va a estar ahora.

y lo dejará para alguna etapa posterior. Bien, y mirándolo desde autorizaciones, digamos, el...

El primer mes que va a tener completito adentro, más allá de estos casos que decías de decepciones médicamente y qué sé yo, va a ser febrero, digamos. Sí, ambulatorios sí, y en función de cómo avanza Internaciones, que estamos ahora terminando de hacer las últimas pruebas en preproducción, quizás también. El objetivo es salir con Internaciones en enero.

Así que, si todo va bien, febrero sería un mes donde tendríamos las dos cosas completas. ¿Y auditoría? Sí, auditoría estaría al cien por cien.

En febrero también, primer mes completo. Yo tengo una idea de cuándo, digamos, switchear también de tableros. Te muestro qué es lo que es el LORE.

Este se llama tablero... no me acuerdo como se llama... Tablero Ambulatorio Operativo o Operativo Ambulatorio, no me acuerdo. Ah, me quedo ahí atrás, qué boludo, espérate. Esto se llama tablero operativo ambulatorio. Acá lo que ve, voy a agarrar un mes para hacer la vida más fácil, voy a agarrar...

diciembre, acá ves un tablero general con todos los F4 que entraron en el mes de diciembre, son 43.500, cuáles fueron autorizados y eventualmente fueron a auditoría posterior, auditoría MF se refiere a eso, bueno cuáles faltan datos, cuáles están pendientes y cuáles están rechazados.

Acá los rechazados incluyen los pendientes por documentación en realidad también, que no están diferenciados. por equipo, digamos, discapacidad, auditoría médica, propiamente dicho, 25%, administrativo y especialistas. Bueno, lo propio, la misma distribución que acá arriba, pero acá por mes, porque por más que filtré diciembre, te muestra los últimos seis, por tipo de auditoría, médica versus administrativa, según la clasificación.

Es otra clasificación, es exactamente la misma que ésta. Y después bajo un poco, tenés los rankings por... prestaciones, sí, psicología, fono y psicopedagogía, que es lo que está relacionado más con discapacidad, viste, es lo que se lleva por lejos el mayor volumen. Después viene kinesio, bueno, transporte, bueno, todo esto es discapacidad, los primeros cinco o seis son discapacidad, casi todos.

Y después acá lo que te decía yo antes, el ranking de acreedores, digamos, sí, el acreedor cargado dice que es el 67%, pero fíjate, el primero, sí, esto está meses. El primero es el P9999, o sea, no me dice nada. Y el segundo es medicamentos, compañía de servicios farmacéuticos, reinteros y otros de farmacia. Los primeros cuatro no me dicen nada.

Si reitero, reitero, es porque cargan el cero y el cero está identificado como reitero, ¿no? Claro, tal cual, tal cual, no es real, digamos. Sí, sí, sí. Después sigo un poquito para abajo, opa, perdón.

Y acá tenés la cantidad por agrupador de motivo de auditoría, de los que dice, bueno, solicita documentación, notificación, criterio médico, cobertura, o sea, los rechazos, perdón, no me salía. Y el detalle de motivo. Motivo de auditoría de autorización, acepta automática por formación online, al juntar histérico y evolutivo, son los diferentes mensajes que aparecen.

Y después... También tenés, y esto va a tardar un poquito, el detalle deambulatorio del asunto, en particular.

es medio grande este, por eso tarda un poco, igual está fijado en la data, que son, dice que vamos a agarrarlo de vuelta al mismo mes, diciembre Y acá ya te habla de la performance de cada auditor, cuántas solicitudes auditadas por auditor por hora, con los nombres de los auditores, la distribución del estado de auditoría para este paquete de diciembre de ambulatorios. Bueno, más o menos lo mismo la distribución de individuo o empresa.

Bajo un poquito. La evolución del estado de auditoría después de agosto a enero. Bueno, enero no está cerrado y diciembre es chiquito. Lo mismo acá, la distribución de los motivos de auditoría, fíjate, solicita documentación es el 67% casi, 66,2%. Y después acá abajo está por rubro.

obviamente laboratorio prácticas imágenes se lleva casi todo y por ranking por prestación está arriba de todo la bcc 527 BCC, que son las BCC que entran a Auditorio, o sea, menores de 45 creo que está el corte y cosas por el estilo, no son todas obviamente las BCC de SACO. Lo mismo que el estudio de hidrógeno aspirado, bueno, antimuniriano y que se yo. De hecho desde esto estamos laburando a ver si les ponemos algún otro nivel de...

de control de alguna otra manera, alguna otra regla o algo por el estilo. Y acá se terminó, ahora, sí, pará, no se terminó. Lo podés ver, acá está por sector, lo podés ver por prestación, lo podés ver por prescribiente, que era lo que yo te decía, que cuando lo mirabas por prescribiente había medio basura porque creo que era el 50%, no estaban bien cargados, viste, una cosa así, que eso mejoraría con Integra en particular.

Por lo que veo hasta ahora, creo que todos los datos, como hacías vos, fue medio premisa eso, que todos los datos que se tenían se pudieran también generar desde íntegra. Ves acá por prescribiente tenés P0 como el principal prescribiente y el segundo profesional prescribiente no definido en origen y el tercero es 9999.

Recién en el cuarto aparece alguien. Bueno, y después las mismas distribuciones, pero en este caso miraba del lado de... Pregunto, esto se levanta directamente de las tablas, por lo tanto la información de Salesforce vos ya deberías tenerla acá. De hecho todo lo de diciembre es todo Salesforce.

Ya es, y claro, bueno, yo estoy... Eso, para, vamos a mirar una cosa entonces. Yo para ver si hubo algún pequeño cambio... No. Porque nosotros arrancamos... Después de las pruebas, alrededor del 10 de diciembre ya empezamos a trabajar casi exclusivamente en Seifert

El que hace el tablero tiene que adaptar el tablero a los nuevos estados de Cypher, por ejemplo. esté pendiente, que comentabas vos y demás. Me olvidé preguntarte eso, ¿tienen una marca en auditoría médica para los casos que requiere auditoría médica de facturación después?

No, en realidad hay un proceso roto ahí, que todavía no nos hemos sentado a arreglar, que tiene que ver con ese estado sujeto a auditoría posterior Eso se pensó de una manera hace mucho tiempo, yo ni siquiera estaba como para que, de alguna manera, genere algún tipo de trabajo de auditoría de facultación después, la realidad es que no sucede, entonces se termina cargando...

Solamente para que el prestado, para que en caso de que auditoría de facturación le quiera discutir algo el prestador, el prestador no diga, ah, pero esto dice autorizado. Bueno, ahora dice sujeto de auditoría posterior. Solamente para eso. No hay ahí...

vinculación caso a caso. Lo que sí hay es una sugerencia de débito hecha por el auditor de terreno derivamos directamente a auditoría de facturación, en un proceso informal, para que lo que el terreno sugiere, después lo analice uno a uno a auditoría de facturación. Por eso va por fuera del CRM, porque todavía no está formalizado.

Es lo que, una de las cosas que charlamos ahí en FUN es el otro día que mostrábamos con Nati Peratonis.

La idea es hacerlo posta o mantenerlo así como tipo, me quedo con el mensajito para que no me rompas después si te hago una auditoría y me digas que te gusta. La idea es pensar un proceso que sirva para casos que realmente tiene que volver a auditoría de facturación después. Como todo, la idea es buenísima, que es lo que falta el criterio. ¿Cuándo sí yo te lo mando? ¿Cuándo yo como auditoría médica de autorización considero que esto es indispensable que vos lo mires después?

¿Y bajo qué criterio? O sea, ¿qué es lo que vas a ver? Yo te mando este caso, Victoria Frantulezón, después porque le avisé al prestador que solamente se lo... Yo te lo autorizo, pero solamente se lo voy a pagar si tal cosa. Eso va a requerir una mirada después de la auditoría de facturación posterior, que seguramente requiere la presentación de algún otro estudio complementario, que en el tiempo se desarrolla después de la primera auditoría.

Todo eso es un criterio que hay que definir para que ese proceso funcione, hay que sentarse a hablarlo, a negociarlo entre la Auditoría Médica de Autorización y la Defauturación, y todavía no se hizo, sabemos todos que es un pendiente que tenemos ahí porque

le puede sacar jugo a eso. Sí, sí, pero la idea es poner el proceso andando bien, digamos, y registrar lo que se tenga que registrar, pero cuando sea necesario. Exactamente. Si querés dejar el mensajito, dejalo, digo, no pasa nada, pero ahí filtré. Igual.

Había filtrado de diciembre, no había mucho cambio. Voy a poner ahora de enero. con los poquitos casos que hay, a ver si se ve. Se sigue viendo, esto es enero. Dice que hay 170 formularios F4 con P0 como prescribiente, pero ya no hay... mira, bajó el no definido en origen, viste? Bajó de ranking. Yo creo que porque están tomando los datos...

no sé si debe estar tomando No dudo que Integra esté impactando los datos en la tabla, lo que dudo es que lo esté tomando bien. Habrá que revisar el tablero, me parece. Yo creo que acá, yo no me di cuenta antes, la verdad. Acuérdate que tendríamos que verlo sumado a Vicky.

o te va a servir mucho también conversar con ella, porque el corazón de todo el proceso sigue siendo la autorización. Y ahí ella te va a poder explicar mucho más que yo, que por ahí demasiado enfocado en auditoría, toco un poco más de oído la parte de autorización.

Sí, sí, igual, este talento en particular es el de Lore, así que es el de auditoría, pero yo, sí, yo le estoy rompiendo las bolas a los chicos de... de GDI, para que me armen un tablero tipo punta a punta y que no me incluya solo los F4, poneme los F57, diferenciamelo, pero poneme todo, digamos, F6, todo, todo, todo. Yo quiero ver toda la transacción, después sí meterme, pero quiero ver primero toda la transacción completa y ver de todo lo que entra a dónde termina, viste, más o menos, tener una idea y también utilizarlo como

como KPI, rechazando el 25% y ese 25% en realidad, por ejemplo, en este tablero de ese rechazado 25% yo estoy seguro que el 15% son solicitudes de documentación. En este. Entonces digo, bueno, pará. Necesito información posta, no esto mezclado acá. Entonces, bueno, nada, estamos laburando en eso. Yo lo que voy a hacer, si te parece bien, es, bueno, primero hablar con los chicos de Tableros para comentarles un poco, porque estuvimos juntos mirando esto y qué sé yo, y tratar de promover alguna reunión, quizás, con quien esté a cargo de este Tablero, que esté, la gente del Tablero, que esté Lore como usuaria, digamos, primaria.

con Lore por otra cosa. Y te voy a invitar, si te parece bien, a vos Fer y a Vicky, para que entre todos digamos, digamos, che, loco, mirá, este dato en realidad lo podemos tener, no lo podemos tener, lo queremos gestionar así, me sirve así, me sirve así y tratar de pegarle un refresh a este, ¿te parece?

Me parece muy bien, sí. Me parece bien y Lore seguramente a partir de este mes que lleva auditando en Salesforce. Te vas a ver decir, más que nadie, este dato antes no lo tenía y ahora lo veo y capaz que me interesa calcular o cosas así. Así que me parece bárbaro, che.

Bueno, ¿vos cuándo vas de vacaciones? Yo ya salí, me fui una semanita en diciembre, así que por ahora vamos a tirar. ¡Jajaja! No, no, no, pero me fui, aproveché ahí la fiesta y me fui, metí como 10 días en total, eran 5 días algo y me fui. Ah, ya, ya estamos listos. Sí, ahora hay que... Cuando terminemos internaciones, capaz salgo un ratito otra vez. Sí, para respirar un poco. A vos te toqué. Bueno, de todo, che. Hoy día, vos sos nuevo.

¿Le tocó algo? ¿Negociaste algo? Sí, sí, negocié, pero en marzo me voy. ¿En marzo? Sí, sí, ya... Ya, ya está. Ya lo negocié, si no me va a volver loco, boludo. Importante eso. Sí, totalmente. Bueno, che, mil gracias. No, por favor. este quizá un poco más adelante para que también tenga más recorrido

ya viste sobre íntegra y lo que necesite es este, digo que te puedo dar una mano o me chiflas, dale. Dale, dale, seguro que sí, igual vos cualquier cosa o si tenés alguna duda o lo que sea nos juntamos un ratito y nos vemos. Dale. Te mando un abrazo. Te mando un abrazo. Hasta luego. Chau.



