---
source_url: https://app.notion.com/p/3482c02ab019806fb6c3e290da46c5de
ingested: 2026-07-08
title: Auditor AI
notion_id: 3482c02a-b019-806f-b6c3-e290da46c5de
---

<!-- unknown block type: tab (3482c02a...) -->

Reuniones

▶ **20260420**

<!-- unknown block type: transcription (3482c02a...) -->



### Elementos de Acción

- [ ] Gastón debe crear un Excel con las 10 prácticas seleccionadas, especificando para cada una qué estudios necesita para tomar una decisión 
- [ ] Para cada estudio requerido, definir el tipo (imágenes, gráfico, texto) y adjuntar ejemplos 
- [ ] Maxi debe conectarse a los servicios de Salesforce para obtener archivos de gestiones de auditoría  
- [ ] Fer y Gastón deben coordinar para definir los 100 casos históricos a revisar 
- [ ] Revisar el tema del nomenclador en cirugías donde un mismo procedimiento puede tener múltiples códigos  
- [ ] Establecer reuniones fijas: martes y jueves a las 15:00 hasta el 20 de mayo   
### Contexto del Proyecto

- El proyecto surge del análisis de la percepción de servicio deficiente, a pesar de que entre 81-85% de los socios consumen sin requerir autorización  
- Del 15-19% que requiere trámites, solo al 15% se le niega la autorización, es decir, al 85% se le aprueba 
- Actualmente el SLA es de 24 horas para carga inicial (equipo de autorizaciones) y 48 horas para auditoría médica, totalizando 3 días 
- Los tiempos de respuesta dentro del SLA son percibidos como negativos por los socios  
### Problemas Identificados

- **Velocidad de respuesta**: Aunque se cumpla el SLA de 3 días, los socios perciben la espera como excesiva  
- **Gestión del NO**: Falta gestión activa con prestadores que solicitan reiteradamente prácticas que no serán autorizadas   
- **Carga administrativa**: Los médicos auditores dedican demasiado tiempo a tareas de bajo valor agregado en lugar de la discusión médica con prestadores 
- **Falta de relacionamiento médico**: No hay tiempo para discusiones médicas entre colegas sobre casos reiterativos  
### Solución Propuesta: Agente IA para Auditorías

- Implementar un agente de IA que procese casos después del motor de reglas y antes del auditor humano 
- El agente leerá documentos adjuntos (resúmenes de historia clínica, informes PDF de estudios) y buscará parámetros específicos para tomar decisiones  
- **Objetivo**: Automatizar al menos el 50% del 85% de casos que hoy siempre se autorizan  
- **Meta de concordancia**: >95% de coincidencia con el criterio del auditor 
- **Funcionamiento binario**: El agente solo puede "autorizar" o "no puede autorizar" (pasa al auditor humano) - nunca rechaza directamente  
- Se trabajará inicialmente con 10 prácticas seleccionadas por Gastón como las más frecuentes y más susceptibles de automatización  
### Beneficios Esperados

- Respuesta casi inmediata para casos simples, mejorando la experiencia del socio 
- Reducción del 50% de la carga administrativa del auditor 
- Liberación de tiempo del auditor para enfocarse en gestión activa con prestadores y manejo de rechazos  
- El concepto es similar a un "residente de primer año" que maneja casos simples con parámetros claros  
### Enfoque de Prueba de Concepto (POC)

- **Duración**: Aproximadamente 1 mes de trabajo 
- **Objetivo**: No crear una solución productiva, sino generar información sobre desempeño, riesgos y desafíos  
- **Metodología**: Emular una solución, probar con casos históricos (aproximadamente 100 casos), comparar decisiones de IA vs. auditor real   
- **Fase de validación**: Inicialmente el auditor revisará todo para validar que se alcance >95% de concordancia antes de autorizar automáticamente 
- **Decisiones futuras**: Después de la POC se definirá si usar solución enlatada o desarrollo custom, y se buscará proveedor 
- Se usará el modelo Gemini de Google para estas pruebas 
### Requisitos y Recursos Necesarios

- Documentación estructurada de políticas de cobertura - ya recibida de Martín 
- Históricos de casos para contexto 
- Herramienta para interpretación de imágenes (Google Gemini) 
- Disponibilidad de Gastón para validación y refinamiento continuo 
- Conexión a servicios actuales para obtener casos y adjuntos 
- Acceso a archivos de gestiones desde Salesforce, que están tipificados (pedido médico, estudios, historia clínica)  
### Desafíos Técnicos Identificados

- **Integración con Salesforce**: Los casos de auditoría (Query Case) guardan archivos de forma diferente a los casos de servicio, requiriendo ajustes en la integración  
- **Nomenclador**: Una misma cirugía puede estar codificada con múltiples códigos, lo que afecta la búsqueda de casos históricos   
- **Tipificación de archivos**: La clasificación actual de archivos no es confiable - pueden estar mal etiquetados o contener múltiples tipos de documentos en un solo archivo    
- **Variedad de formatos**: Necesidad de entender todos los tipos de archivos/estudios que existen (gráficos, textos, imágenes) para dimensionar la complejidad  
### Supuestos de la POC

- Se asume que las prácticas indicadas son correctas (no se validará el trabajo de clasificación previa)  
- Se asume que la tipificación de archivos en Salesforce es correcta, aunque se sabe que esto puede no ser así en la realidad   
- Estos supuestos pueden revisarse si durante la POC se detectan problemas sistemáticos  
### Coordinación y Próximos Pasos

- Reuniones fijas: martes y jueves a las 15:00 horas  
- Inicialmente se programó hasta el 20 de mayo 
- Se anticipan más reuniones ad-hoc según necesidad, no se esperará solo a las reuniones fijas  
- Posibilidad de ajustar frecuencia según avance del proyecto - al inicio puede necesitarse más participación de procesos  
- Pueden cancelarse primeras reuniones si Maxi aún está resolviendo conexión con servicios 
### Relación con Políticas de Cobertura

- El trabajo con el agente de IA va de la mano con la elaboración de políticas de cobertura 
- Las políticas definen condiciones específicas bajo las cuales una práctica se puede autorizar 
- Gastón trabajó en mini prueba piloto previa identificando las 10 prácticas más frecuentes y definiendo criterios de decisión 
- Es necesario que las políticas estén definidas para las prácticas piloto, especificando qué estudios se necesitan evaluar  


![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/7b5fbb80-d2e2-40a7-b904-91a0ee2f8086/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VI5QCHLP%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150137Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJIMEYCIQDmddYzpNp2CGyXIKR2nf6IVqsTkohJYocXCLt2yZsAgAIhAJG3LbItnHeednLCdWN1nhpTHUrWeYMgXpJvyDi6aDDbKogECIf%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1Igxt0ugJTB1IQtpAEeUq3AO%2BueSXxCdJWZZ%2BkHAjOmZFK39NY989T7J55esAL5D6OSRVLF4lyDypu%2BUxZcgSgAyIvoCVtgjsyUVmlOi5vkl76oOIIZv7QNlqgPw90EJZxDAqxe8AUeNAMQzD1mjkREsTAX8w0OMbjHlzsU%2FllOORk%2BkHNnwCDkPypkTy4mQQA4k%2BJlCpaIqZJM0TaNUzjim3dP%2Fwct7CcwWdYEHMeHFCazWHY9kv9IoSSJ6U%2B9h8GXa%2FQMQ9AXwo52EEUU8S8en06Iua8BI2DOBa2e8LKIwzLVh8vVfcWsjVDVNA07PfSzEhJ9oBHT%2BvSSXdAsxHPE0Vfw6aA5PO0PGawsZwvJZ5bss3gN1Q7oFjrizgnmc8PxZ4QWpNeKLeh31a%2BOqM1s6AsPCuGrXn2D2xY6csB4AwpfRvarIY2jkfwND4Q4Uv0PUCQVN9%2FRj4akqPaKBild4EgvmLvtSoSD90WoDvj0oDOVBlyTcmLwvvG%2BrLEZfPhrX2PdjFnhanU30Z3Gi%2FVTt8M1Ao%2F%2FW%2BjOMleQrc7zgVOHmN7o1aRDVUBGMXcLKYprbTQyMfI6cmQdYCVTfGBu3gO3Im2D30wCzRzBc0hG%2BVukYNsZxHJb%2BA1E6ipISaFBFi2Zz%2FCG2La3xy9TCkqbnSBjqkAX9rJyFOeC%2B%2B9oEFXv1hWkjIvzrWok8r%2BAscE%2FA%2FxHrIFn%2BiVKa3C%2BoBVc7jSP0bX4xns%2Bqws8hKY8s3rqMNilI8Lse2aBz3eZbGSK3UO4Jc9drYqbrxtQ3V5x0eMI8kiqctAH%2F16%2BY6Q%2Fe8%2FggIIakxnNCgwTCygXJSoP3yPMiVS2XdF6ujrZ6sBGE7KOgfFwtruQewyxYbnOuQwL2z4mdr9WoU&X-Amz-Signature=31cc7b1253e3d3fb2b8e4648dcb0b2536efcdd0a52c57a0b973cb6a12fce4560&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)



Bueno, esperá, lo buscamos a Pablo, a ver, si se suma, así, chapacamos.

Bueno, supongo que Pablo se demorará un ratito, si a ustedes les parece, podemos arrancar. importante. Ay, genial. Buenas. Hola, buen día. Igual me tengo que ir en unos minutos a otra mis, pero quería estar al inicio al menos. Muchísimas gracias. La idea es esa, que podamos estar todos, darnos la bienvenida. Queríamos contarles un poco de qué va este proyecto, cómo es lo que lo vamos a encarar.

para empezar a coordinar nuestras reuniones de acá en Adelante. Pablo, si querés contarles un poco, yo traje el caso de negocio para que nos lo podamos compartir, ¿te parece? ¿Escuchamos? Dale, dale. Perfecto. Sí, sí. Dale.

Bueno, igual creo que con la mayoría ya lo hablamos y les contamos un poco cuál era la idea Y esto parte de un análisis que hicimos A raíz de la percepción que incluso internamente en la empresa tenemos de que no brindamos un buen servicio o que tenemos cuestos para mejorar.

Surgió de un análisis que en realidad el gran porcentaje de nuestros socios que consumen, consumen sin pedirnos permiso, más del 81%, aproximadamente, entre el 81 y el 85%, depende de qué tomemos. consume sin que nosotros le pidamos nada, va a consultarme y consume. Hay un mínimo porcentaje que va entre el 15 y el 19 por ciento.

al cual nosotros le pedimos que haga algún tipo de trámite o gestión con nosotros y de ese porcentaje, solo algunos pasan por auditoría médica y de los que pasan por auditoría médica... al 85% nosotros le terminamos diciendo que sí, o sea, le aprobamos la gestión que está haciendo. O sea que hay un solo un 15% al que le decimos que no.

Desde ese análisis, y entendiendo un poco lo que los socios dicen, entendimos como dos puntos que nosotros creemos que podemos mejorar. Y uno tiene que ver con... la rapidez con la que decimos que sí, porque a que le decimos que sí, porque percibe o se queja del servicio y probablemente porque está esperando que se lo respondamos antes del tiempo que lo estamos haciendo.

Nosotros hoy tenemos un SLA de 24 horas para la carga, que eso es de la parte del equipo Estefi, de autorizaciones, y de auditoría médica un SLA de 48 horas. Quiere decir que cumpliendo con la CCLA, nosotros dentro de los tres días de que el socio presentó el trámite, nosotros le deberíamos responder.

Previo a la implementación de Salesforce, eso se venía cumpliendo bien. Ahora tenemos un poquitito de demora en lo que se le da producto del cambio del sistema. Pero bueno, todo esto es previo a Salesforce y no es por Salesforce esta percepción y nosotros creemos que evidentemente para el socio hacer esta gestión y esperar tres días que le respondamos.

que estaría dentro de nuestro SLA, lo perciben como negativo. Por otro lado, el otro punto o gran punto de dolor que tenemos es en la gestión del NO. Y cuando hablo de gestión no es llamar al socio y decirle te cuento por qué te voy a decir que no, o llamar al prestador, sino gestionar con los prestadores.

¿Por qué, reiteradamente, piden cosas que nosotros sabemos que no vamos a autorizar? Entonces digo, esa gestión activa tiene que ver con el relacionamiento con el prestador y con una discusión médica en la cual nosotros creemos que el socio no tiene que estar.

El sociedad debe estar fuera de esta discusión, y es una discusión médica. Por supuesto que van a seguir existiendo, pero nosotros creemos que hay una gran oportunidad de trabajar sobre las cosas que son reiteradas en el tiempo. Cuando uno ve por qué sostenemos el NO y dónde tenemos los problemas, cuando aparecen generalmente son sobre prácticas o sobre...

autorizaciones bastante reiterativas y también se reiteran los prestadores. Entonces creemos que ahí falta una gestión. ¿Y quién tiene que hacer esa gestión? Y los médicos, porque la discusión es médica. No puede ser administrativa, no puede ser, tiene que ser una discusión médica.

de un médico con otro médico, con su colega, discutiendo por qué pedís esto cuando sabés que no corresponde y terminamos teniendo un problema y generar acuerdos a mediano y a largo plazo. Bueno, hasta ahí un poco entender sobre lo que queremos trabajar y por qué hoy eso no lo hacemos. Y básicamente no lo hacemos porque...

nuestros médicos auditores pasan gran parte de su tiempo detrás de una computadora viendo un montón de casos a los que No agregan demasiado valor en muchos, y donde más deberían agregar valor, que es en la discusión médica con los prestadores, no lo hacemos porque no tenemos tiempo, porque tiene una gran carga administrativa.

Como dijimos que al 85% le decimos que sí, lo que quisimos saber es, bueno, y acá está Gastón que fue con el primero que hicimos una mini prueba piloto de decir, bueno, tomemos las 10 prácticas más frecuentes de esta especialidad y juntémonos con la persona que sabe, que es el auditor de la especialidad, para decir que es esta que vos terminás autorizando casi siempre.

digamos qué es lo que mirás para tomar esta decisión y un poco eso va de la mano con Cristina Martín acá también, con la elaboración de las políticas de cobertura de género. Porque para una determinada práctica nosotros decimos, bueno, ante estas condiciones, si se dan estas cosas, la práctica se podría autorizar.

Entonces ahí vimos una oportunidad de automatizar esto con IA, ¿por qué con IA? Porque la parte más determinística que es la de mirar reglas simples, ya las mira nuestro motor de reglas. Pero una vez pasada la capa del motor de reglas, a veces la decisión del auditor se basa en leer un resumen de historia clínica, leer el informe PDF de un estudio.

Y en base a esos resultados o a esos parámetros que encuentran esos estudios, tomar la decisión. Y eso no lo podemos hacer hoy con el motor de arreglas. pero sí podríamos intentar hacerlo con ya que lea estos documentos y busque estos parámetros que nosotros estamos diciendo en conclusión

creemos que hay una oportunidad de que una vez pasada la capa del auditor de perdón del auto del motor de regla y antes de que tome el caso el auditor, un agente lea los documentos adjuntos, lea la práctica que está requiriendo autorización. Y en base a los parámetros que habitualmente usa el auditor, y de parámetros administrativos, tome una determinación.

¿Qué es lo que queremos lograr? Nosotros queremos lograr que este agente tenga un nivel de concordancia con el criterio del auditor superior al 95% para el CIC.

Porque lo que planteamos siempre es que el auditor guía, es como yo le decía a Gastón, es tu residente de primer año, es el que vos mandás atender a la guardia y le decís, mirá... Estos casos, si tiene esto, esto y esto, lo podés manejar de esta manera. Los residentes son los médicos que están formándose en la especialidad, que tienen menos experiencia, pero que con una serie de parámetros uno le puede decir, bueno, de esto ocupate vos.

Ahora, cuando no sabés qué hacer, consultáme". Entonces, la idea es que la gente pueda, en base a algunas reglas que le va a dar política de cobertura y también el entrenamiento o el promteo que le demos de acuerdo a este ida y vuelta con Gastón, que va a ser básicamente el dueño de esta herramienta.

logré autorizar al menos la mitad del 85 por ciento que hoy se autoriza siempre. que lo autorice la herramienta, y lo que queremos lograr son varias cosas. Primero que para esas fuerzas simples, que si las puede autorizar la herramienta... La respuesta del socio va a ser casi inmediata, o sea, no va a tener que esperar esas 48 horas de SLA, con lo cual estaríamos mejorando la experiencia del socio. Y, por otro lado, liberando al auditor de carga administrativa.

de tareas en las que agrega poco valor, para concentrarse en esta tarea de la que hablamos de la gestión activa con los prestadores y la gestión activa del no. para evitar estas fricciones con los prestadores y con los socios. Esos son un poco los objetivos, ¿no? Automatizar el 50% de esto, disminuir el 50% de la carga administrativa del...

del auditor, y ser más rápido en la resolución del socio. No sé si se entendió hasta acá, fui medio rápido para que ustedes puedan trabajar, pero un poco... El concepto es ese, y para esto tomamos nosotros 10 prácticas, que son las 10 prácticas que edició Gastón.

Él dijo, bueno, estas son las que más volumen tengo y en las que siento que con tres, cuatro parámetros o cosas que yo le pueda explicar, que podría automatizar. Y me parece relativamente sencillo, las 10 prácticas, eso es importante, y esto es una prueba piloto.

La idea es probar, teniendo las políticas de cobertura de esas 10 prácticas y con la ayuda de Gastón, probar primero, en una etapa... El auditor igual no va a autorizar nada todavía, la idea es que validemos que llegue a un nivel de concordancia superior al 95%, probar que...

el agente coincide con el criterio del sí del auditor, digamos. Vuelvo y reitero, por ahí soy reiterativo en esto, pero es importante por varios aspectos. este agente nunca va a rechazar, o sea, básicamente el resultado de su paso va a ser binario, autorizo o no puedo autorizar.

y el no puede autorizar este lo pasa al auditor humano, y el auditor humano revista. La idea de esto es que no genere rechazo si tengamos errores, digamos, por rechazo, que eso tendría un impacto muy negativo en el socio y en el prestador. Y por otro lado también, digamos, es que pase por el auditor, también nos va a ayudar a ir refinando el prompt de la gente para que...

digamos cada vez tenga una precisión mayor nada cierro ahí ahí no sé si marcos explica un poco lo de la diapo anterior pero ya El concepto de la gente IA o el auditor IA es esto y se basa en lo que les acabo de contar.

Buenísimo, gracias Pablo. Le voy a contar que desde que empezamos con el equipo a trabajar en este tipo de proyectos, lo que estamos haciendo es trabajar en pruebas de concepto. Nos ponemos un tiempo objetivo. En este caso, si mal no recuerdo, Patrick seguro me va a poder corregir, pero habíamos hablado de un mes aproximadamente Donde nosotros nos juntamos con el equipo, tratamos de entender bien las necesidades y tratamos de emular un espacio

especie de solución desde nuestro lado, donde lo que buscamos es tener la mayor cantidad de información posible sobre cómo performa, después seguramente haya mejores formas de hacerlo y hacia eso vamos a ir cuando busquemos un sistema productivo. Pero nos ha rendido mucho, sobre todo tomando el caso de autorizaciones, para entender bien el proceso macro, para entender dónde están las mayores complicaciones o los mayores desafíos, si se quiere.

Así que eso es en lo que vamos a estar trabajando. Cuando se termine la POC no vamos a tener una solución implementable productiva, si eso lo vuelvo a decir por las dudas. Lo que vamos a tener es toda esta información de cómo nos fue, cómo formó esta solución que pensamos alto nivel y vamos a tener probablemente un listado de riesgos que después tendremos que gestionar.

Con eso, ahí sí iremos en búsqueda de alguna solución definitiva, probablemente con algún proveedor que nos acompañe, después se definirá si es un... o enlatado, si es que existe o si es algún desarrollo que se encabele, pero todo eso va a suceder al final, van a ser decisiones que se tomen a partir de esta prueba de concepto.

¡Hasta la siguiente!

No sé si alguien tiene alguna pregunta, también es bienvenido. Pueden interrumpir, sin problema. Después, con respecto a qué necesitamos ahora, nosotros nos estuvimos juntando con con Gastón, hicimos dos primeras reuniones, para eso lo tenemos a Maxi Matic que nos viene acompañando en este tipo de pruebas del concepto, él necesita la documentación estructural de las políticas, eso hemos recibido, Martín nos compartió algunas de estas políticas que estaban en curso.

Después, bueno, disponibilidad de históricos para contexto, comunicación a socios, esto en realidad la comunicación a socios viene más adelante, herramienta para interpretación de imágenes que en realidad hoy es una única herramienta, nosotros estamos usando un modelo específico que es el de

el de Google, que se llama Gemini, para estas pruebas de concepto, y obviamente la disponibilidad de Gastón, que seguramente lo estemos molestando. Lo que hacemos básicamente es tratar de conectarnos a nuestros servicios actuales, obtener la mayor cantidad de casos posibles como para emular un proceso con inteligencia artificial y ver qué resultados obtenemos.

Y después comparamos la realidad con, o sea, qué había decidido el auditor en su momento contra lo que hizo la inteligencia artificial y obviamente tratamos de entender por qué llegó a ese resultado, ¿no? Vamos a ir haciendo esa comparativa y ahí encontraremos un valor de eficacia, como decía Pablo, que el umbral tiene que ser bastante alto, sobre todo para el...

para el sí, así que ese es el ejercicio que esperamos y es lo que necesitamos tener al final de este mes de trabajo.

Bien, se pasó rápido la última Perdón, tengo un dedo pesado hoy, te quería explicar un poco cómo va a ser el proceso No, esta es la de autorizaciones, pero bueno, básicamente nos dio el... Esto es un poco de la información que nos dio, al principio no conocíamos, por lo menos de nuestro lado, cómo era ese proceso y cómo esperábamos construirlo. Al de autorizaciones, lo vuelvo a repetir por las dudas,

Después de finalizada la prueba de concepto entendimos que había un valor agregado en la clasificación de las recetas, en la segmentación de la demanda en función del input que estábamos recibiendo, que es toda información estructurada, porque en general son imágenes, PDFs.

Y después nos encontramos con algunos desafíos importantes que algunos que están acá ya los han escuchado también, pero era el macheo del pedido médico versus. el nomenclador, bueno, a eso nos referimos con respecto a ir entendiendo dónde están los riesgos de este tipo de proyectos, no embarcarnos...

a ciegas, sino tener información y sobre todo entender nosotros qué es lo que necesitamos del lado de Suncor para ir a exigir eso después a quien nos venga a acompañar en un proyecto de este tipo.

¿Alguna inquietud? ¿Alguna preocupación?

La idea es que a partir de hoy, de esta semana, tengamos una instancia de por lo menos tres veces a la semana, juntarnos una horita para trabajar y lo que… Lo que, no sé si hay otras instancias fuera, pero en principio pedirles la participación de ustedes tres veces por semana.

Cuéntenme, por favor, cuándo les parece que sean los días o los horarios que sean más oportunos para que nos empecemos a juntar.

Yo hice un jueguito y no encontré ningún lugar que esté óptimo, pero si podemos llegar a un acuerdo… Sería el ideal.

el que sea menos complejo. Yo veo, por ejemplo, los miércoles 10.30 tengo a menos personas. La tarde, vamos por la tarde. Sí, tipo siesta podría ser, tipo dos o tres de la tarde como decía Martín. Bien. A ver que vamos a buscar un horario decente.

Tres de la tarde. Veo varias personas, a las dos y a las tres, ocupadas, pero no sé, por ejemplo, a ver...

¿Quién puedo sacar de que sea restrictivo? Los que estamos acá no, tenemos que estar todos. Quizás esta semana podemos acomodarnos y a partir de la que viene ya fijar a la tarde porque como esta semana por ahí ya tenemos agendas. Sí. La sugerencia, ¿no? Sí. Y día por medio está bueno para si nos llevamos tarea cuando volvamos, o sea, tener un día entre reunión y otra también podría ser.

¿Les parece miércoles y viernes? ¿Les parece martes y jueves? ¿Lunes, martes y jueves? Voy a hacer un disclaimer Patri, en función de también un poco de lo que nos pasó con autorizaciones Al principio necesitamos mucha participación por ahí de procesos

Maxi está tratando de conectar los servicios y ahí tiene un desafío, con lo cual si quieren dejar las reuniones puestas me parece bien, así se bloquean los espacios porque acá cotizan en bolsa. Pero, primero lo haría dos veces por semana, después de lo último vamos buscando a las personas, y tres me parece mucho. Y lo otro también, sepan que puede que por ahí las primeras se cancelen, si es el miércoles, no sé Maxi ahí si querés abrir el micrófono y comentar, pero bueno, estaba con un desafío Maxi ahí para...

Lo que necesitamos es traernos todos los casos y gestionarlo en un proceso que él está armando y no tenerlo que hacer manual Si no, eventualmente nos vamos a tener que traer todos esos casos que empezamos a usar de prueba de forma manual, vamos a tener que hacer ese trabajo entre todos

A ver si estaba tratando de resolver esa parte.

Bueno, como dice Marco, la idea era, siguiendo con lo que mencionaba antes, tener un equipo Pensar un proceso y después ponerlo a prueba con una mínima cantidad, algo medio masivo, de cien auditorías para ver, digamos, cómo se comporta, para ir teniendo idea, porque eso nos hace un poco lo que fuimos haciendo con autorizaciones y eso nos permite ir viendo la realidad, qué tipos de archivos hay, y ver que, no sesgarnos con, bueno, tomamos un caso

y lo probamos, y el tema de lo que decía Marcos de contactar con los servicios, lo que hago es, Fer, por ejemplo, y Gastón me definen la lista de, no sé, de estos 100 casos a revisar. Y yo lo que necesito por ahí son de cada uno de los adjuntos, los estudios, por ahí no el pedido médico, porque si por ahí por ahora asumimos que la persona anterior hizo correctamente su trabajo y la prestación indicada es la…

La que va, pero yo necesito los adjuntos, y para no tener que estar pidiéndolos a mano, estaba viendo de qué forma hacer, como hicimos en otras sesiones, de obtener esos archivos de las gestiones. que entiendo que es distinto a autorizaciones, porque en autorizaciones me basaban en el caso service y en auditoría vuelven a subir los archivos, digamos, el...

El sector los agarra y los vuelve a subir, ya tipificándolos, diciendo este es el pedido médico, este es un estudio, esta es una historia clínica y demás, bueno, tuve que ajustar, bueno, ver cómo usa los servicios de Salesforce para obtener... Esos archivos, pero ya... Tenemos la luz verde, ahora.

No, ahí Maxi con lo que decías, yo entiendo que la dificultad estaba en los links dinámicos para obtener los activos. No, en obtener la lista en sí, digamos, cada gestión tiene una lista de archivos, una lista de números, de IDs, con los que se generan esos links.

Es eso, digamos, la forma en la que un caso como el John Kerry guarda esos archivos es distinto a como los guarda un caso service y los servicios contra los que yo ya me integraba no me servían, digamos, yo, en el proceso le decía dame los archivos de tal gestión y no me traía nada porque los tenía que buscar en otro lugar así que tuve que ajustar el procesito para buscarlos de la forma en la que los guardan los querry-quests

Pero ya estaríamos, ya no pude conectar a Salesforce para eso. Ok. Encuentro menos dificultades martes y jueves a las 15. ¿Cómo lo ven? ¿Alguien tiene algo imposible de salvar?

No, no. Yo por lo menos. Vicky todavía tenemos muchas de la otra POC. No sé si las vamos a ir. enviando o bajando, porque justo martes y jueves a la tarde tenemos, no, martes y miércoles tenemos de las pocas autorizaciones, que no sé si ya las podemos ir

ramando digamos, modificándolas, ¿o no? ahí tenemos los próximos pasos, hay que empezar a decidir cómo seguimos De mínima el cheque tenemos que dejar, pero no sé, después los espacios de trabajo no los tenemos. Pero sí, martes y jueves, ¿podemos a las 3 de la tarde?

avanzo así y y vemos, ¿te parece? Me parece bien, empecemos y en todo caso vamos calibrando como decía Marcos, ¿eh? Bueno, así que nos vemos mañana de nuevo. ¿Tenemos que preparar algo, algo, Maxi, para traer?

¿Preparar quién? ¿De qué lado? Todos. Si necesitaba ayuda con algo de los casos, bueno, entiendo que lo de documentación está resuelto, pero si... Si hace falta algo sobre casos, asuntos, tipología o lo que sea, hay disposición. Lo que venía pensando que en algún punto vamos a necesitar es, no sé si más casos o más políticas, si vienen ahora entiendo que vamos a...

enfocados en Estados de otro Reino, entender un poco mejor cómo van a estar construidas esas políticas para, digamos, la idea es entender cuáles son todos los tipos de... de archivos, de estudios que hay que extraer, digamos, si son gráficos, si son textos, digamos, conocer eso un poco, la amplitud de eso, porque eso puede llegar a determinar un poco la complejidad.

Y lo mismo, bueno, como lo que decía antes, si bien se pretende que esto no controle, no responda bien el 100% del porcentaje que se quiere o de las prestaciones o especialidades que se quiere, sobre eso mínimamente tener en claro cuál es la política, si es que está definido el criterio, no me importa tanto el criterio de si está definido así es, en el caso de Torreón así es.

mayor o menor a 20 o ese detalle estino, pero es entender qué tipo de estudios se necesitan y por lo menos que me sepan explicar. o mostrar qué es ese estudio, si es un gráfico, si es una tabla, si es un texto, para seguir dimensionando a ver si dentro de todo lo que se hace viene pensando, si se puede incorporar eso, o si eso por alguna cuestión...

tendría una dificultad extra que me llevaba por lo menos a levantar las manos y decir, mira, esto puede tener esta complejidad y, como hicimos en autorizaciones, que detectábamos cosas que dijimos, bueno, esto quizás requiere que durante más tiempo lo revisé bien a mano o requiere otra estrategia o lo que sea.

Ahí Fer lo que podríamos hacer es que por ahí te juntes con Gastón y hagamos un Excel con las prácticas. con las diez que elegimos, que Gastón defina para cada una de esas prácticas qué necesita él para tomar una decisión, suponete la audiometría, la tomografía...

y que le ponga también a cada uno de esos estudios que él sí o sí va a necesitar para utilizar esa práctica, qué tipo de estudio es, si es un estudio de imágenes, si es un gráfico, si es un formato... O que me lo adjuntes, si me pones un ejemplo, para mí por ahí sería...

Yo de las 10, Omar, para esta práctica solo resumen de historia clínica, para esta odiometría, resumen de historia clínica y tomografía, no sé, cualquier cosa digo. y definirle ahí qué tipo de estudio es y cómo suele venir. Me parece bien. Tenemos que ir a la otra reunión, me parece, también. Sí, sí. Solamente quiero cerrar una cosa.

Ahí Pablo cuando hablas de prácticas, haces referencia también a cirugías o prácticas te referís solamente a audiometrías también cirugía, sí? Sí. Ok, es importante que ahí Marcos veamos el tema del nomenclador porque una misma práctica, cirugía... Puede tener más de un código que significa lo mismo, ¿sí? Ahí lo tendríamos que ver porque justo eso es lo que estamos viendo nosotros desde la parte del nomenclador.

No, no en prácticas es más sencillo pero en cirugías sí puedes tener que una misma cirugía esté codificado con más de un número, con más de un código. Sí, nosotros como había comentado Maxi acá, para no complejizarlo aún más, asumimos que las prácticas son correctas, porque en eso nos basamos para dar inicio al proceso.

Yo no digo que sean incorrectas, yo lo que te digo es que una misma cirugía puede estar nomenclada con dos códigos distintos, entonces cuando van a ir a ver la cantidad de casos por ahí si solamente toman un código van a ver pocos casos. Ah, ok. Está bien. Dale. Lo tenemos en cuenta entonces para buscar el histórico. Perdón, no había entendido. Bueno, nosotros nos tenemos que ir a otra reunión.

¡Muchas gracias! ¡Gracias! ¡Chau!

¿Y nosotros entonces? ¿Necesitamos algo más? Yo me estaba por ir justo, creo que no, Maxi nos va a contar seguramente... cómo se puede avanzar y ahí vamos a ir convocando. Lo estábamos manejando así, sobre todo con Fer y con Gastón, en el momento, cómo vayamos avanzando.

Y después en las reuniones fijas que tenemos iremos dando feedback de cómo estamos. Pero seguro que los convoquemos fuera de esas reuniones, no vamos a esperar.

Bien. Creo que estamos.

Perfecto, entonces, yo mando la invitación martes y jueves desde acá hasta el 20 de mayo y estamos en contacto siempre. Un comentario más por las dudas, ya que estábamos hablando recién de las cosas que confiamos Otra cosa en la que por ahora en la POC estoy confiando es en la clasificación de estos archivos que yo decía Porque la política, por ejemplo, define, bueno, evalúa audiometrías que yo asumo que están dentro de un archivo catalogado como

estudio, si aún al archivo donde está la audiometría le pusieron esto es pediomédico, hoy en la POC lo estoy ignorando, digamos, por una cuestión de tiempos y costos de analizar digamos, de desconfiar de lo que cargan, se podría, pero eso implicaría que la FOC, la gente tiene que revisar todos los archivos y decidir según su criterio.

cuál es un estudio, o en qué archivos hay un estudio, y por ahora lo estoy ignorando, así que bueno, eventualmente sí llegué a ver, no sé si eso está medio, no, si hay... Error en tipificación de archivos, quizás en la FOX salte y bueno, habrá que haber que hacer, pero hoy es otra cosa en la que confío, que las prestaciones están bien y que la tipificación, la clasificación de los archivos

Yo en el día a día, perdón que te interrumpa Masi, en el día a día te voy diciendo que no, que no es así. O sea, no es que están correctamente clasificadas las cuestiones, o sea... Puede venir como estudio, que diga estudio previo y que sea el pedido médico o que diga estudio y que sea absolutamente todo desde el pedido médico.

Estudios previos, resumen de historia clínica, en ese sentido habría que pulirlo un poquito más para lograr lo que vos estás pidiendo, porque si no, como decís vos, no lo vas a poder leer. Bueno, es bueno saberlo, pero bueno, por ahora puedo avanzar así y vemos que incluso hasta para la POP es bloqueante.

O sea, lo que entiendo en el sentido de que donde me dicen esto es un estudio médico adentro, no hay lo que necesita la política, bueno, podemos, digamos, incorporar que revise o reclasifique. los archivos, pero bueno, por ahora lo estaba armando así, pero tenía contemplado que se pueda desconfiar, digamos, y era algo que iba a mencionar, pero bueno, ya que no subra tiempo lo menciono

esto de, eventualmente, desconfiar de las prestaciones o desconfiar de los archivos, digamos, que entiendo también que a veces es una cuestión de cómo lo clasifican. Entiendo que a veces te pueden mandar un único archivo que es medio ensalada, o sea, la sociedad te manda todo junto y no te vas a poner a cortarlo, entiendo, y bueno, entiendo que le pueden poner una sola...

tipificación, así que a lo mejor, bueno, puede pasar. Pero bueno, esos son el tipo de cosas que nosotros imaginamos que con la POC, digamos, cuando haces pruebas... Así es, digamos que agarrás un X volumen con mi computadora y decís, bueno, a ver si acierto o falle, y cuando mirás el por qué falla, empezás a ver si es bueno.

Hay una tendencia de, bueno, es porque clasifican mal, es porque está mala prestación, es porque este estudio es, no sé, es un informe y lo escriben a mano y eventualmente puede llegar a decir bien, falla siempre que es este médico porque escribe muy mal, bueno.

lo podrías descartar o darle tratamiento especial a cualquiera de esas casuísticas. Pero bueno, lo vamos viendo. el avance. Perfecto.

Nos vemos entonces mañana. Muchísimas gracias. Muchas gracias. Chao, chao.

▶ **20260421**

[https://docs.google.com/document/d/1LebI2zhyBZf-GwWcYBOK7FArKYx6l26NQawVxJBgNZA/edit?usp=sharing](https://docs.google.com/document/d/1LebI2zhyBZf-GwWcYBOK7FArKYx6l26NQawVxJBgNZA/edit?usp=sharing)

▶ **20260430**

<!-- unknown block type: transcription (3522c02a...) -->



### Acciones Pendientes

- [ ] Gastón revisar casos aprobados sin audiometría para verificar si hay documentación alternativa o procesos especiales  
- [ ] Gastón evaluar casos de excepción (discapacidad, línea empresa) para determinar si requieren criterios de aprobación diferentes  
- [ ] Maxi buscar casos en Salesforce usando números de práctica del listado con políticas definidas  
- [ ] Equipo enfocarse en casos basados en texto/informes en lugar de interpretación de imágenes y gráficos   
- [ ] Equipo realizar nueva evaluación con casos que tengan políticas definidas (cirugía endoscópica, septumplastia, turbinectomía, timpanoplastia, mastoidectomía)   
- [ ] Reunión de seguimiento programada para el martes a las 3 PM  
### Resultados de la Prueba Inicial con IA

- Maxi ejecutó flujo que trae datos de Salesforce, procesa información y cruza archivos contra políticas de cobertura 
- Se procesaron 22 casos totales en la muestra inicial 
- Aproximadamente 30% o menos de casos tuvieron resultados correctos   
- La IA mostró inconsistencia en decisiones: mismo caso ejecutado tres veces dio resultados diferentes (aprobado vs pendiente) a pesar de temperatura cero     
- Problemas significativos en detección de valores de audiometría: desfasajes de 20-30 decibeles entre valores detectados y gráficos reales 
### Problemas Identificados en Selección de Casos

- Algunos casos procesados eran de autorizaciones en lugar de auditoría   
- Casos de autorizaciones no tenían archivos obligatorios porque es responsabilidad del equipo de autorizaciones solicitarlos 
- Casos de auditoría tenían archivos en ubicación diferente (objeto hijo vs padre) que no fue contemplado inicialmente   
- Se identificaron casos de excepción resueltos por Laura Schwery, Dr. Quiroga, y casos derivados incorrectamente a línea empresa  
### Desafíos Técnicos de Interpretación de Gráficos

- IA tiene dificultad significativa interpretando audiometrías donde vía aérea y vía ósea coinciden (circulitos, piquitos y crucecitas superpuestos)    
- Calidad variable de archivos: escaneos, fotos de tickets térmicos, formatos muy diferentes    
- Productos como Gemini chat hacen preprocesamiento de imágenes que no está disponible vía API directa    
- Cuando se entrega archivo completo con múltiples estudios, la IA se dispersa y pierde foco    
### Estrategia de Preprocesamiento Desarrollada

- Maxi desarrolló enfoque de recortar cada estudio individualmente y hacer llamada separada por estudio   
- Se definieron 6 prompts específicos, uno por cada estudio y lateralidad  
- Política se pasa preprocesada (solo partes relevantes de 13 páginas) 
- Este enfoque logró mayor consistencia pero requiere más mantenimiento   
- Salida estructurada define valores de frecuencias específicas (100, 1000, 2000) más interpretación opcional de Gemini  
### Complejidad por Tipo de Estudio

- Timpanometría parece más simple de interpretar (más automatizada, menos manual)  
- Logoaudiometría presenta complejidad variable: algunos casos tienen gráfico por oído, otros todo junto con diferentes colores  
- Audiometría es la más compleja debido a gráficos manuales superpuestos   
### Cambio de Enfoque Propuesto

- Equipo decidió pivotar hacia casos basados en texto/informes en lugar de interpretación de imágenes    
- Se descartará análisis de imágenes médicas en primera etapa  
- Cuando existe informe de diagnóstico por imágenes, se basará en el texto del informe   
- Mayoría de casos de auditoría se basan en informes textuales, no en interpretación de imágenes  
### Casos con Políticas Definidas para Próxima Prueba

- Cirugía endoscópica (septumplastia, turbinectomía) - en revisión 
- Sinusotomía - debe tener política 
- Timpanoplastia y mastoidectomía - revisados previamente 
- Timpanoplastia puede requerir gráfico además de informe  
### Preocupaciones Principales Expresadas

- Martín expresó preocupación por resultados tan negativos en crudo y falta de coherencia con temperatura cero 
- No hay forma de manejar inconsistencia cuando modelo da respuestas diferentes con mismos parámetros  
- Modelos actuales no están especializados para imágenes médicas ni gráficos médicos   
- Posible necesidad de preprocesamiento adicional de imágenes (contraste, blanco y negro) si se continúa con gráficos   






Bueno, vamos. Ah, no, Estefi, ¿la esperamos o arrancamos? Vamos. No, arranquemos porque... ¿Quieren que tomemos nota? Vamos a tomar nota. Maxi esta semana hizo una corrida del flujo que armó, donde básicamente se trae los datos de Salesforce, le hace el procesamiento, cruza...

la información, los archivos de Salesforce contra las políticas de cobertura y nos da un resultado Tiene algo de procesamiento que después le dejo a Maxi si quiere aportar algo extra Pero medio a la fuerza bruta, como dijimos en su momento, así medio crudo, nos fue dando distintos resultados. Yo hice un procesamiento muy inicial y pido perdón porque está un poquito...

sobre todo cómo armé las categorías, pero ¿qué nos fuimos encontrando? Primero nos encontramos con un problema que yo no me di cuenta hasta hace un rato cuando Fer me dijo que algunos de los casos que estábamos corriendo eran de autorizaciones y no de auditoría

Entonces, ¿qué pasaba? La gente agarraba y decía, che, le faltan los archivos obligatorios Bueno, ese es el caso de uso de la gente de autorizaciones, eso es lo que debería hacer la gente de autorizaciones Con lo cual, digamos, si bien esa lógica funcionó bien, decía, che, le falta la biometría, mostró

No, no puedo hacer nada con esto y se cortaba ahí. Después sí nos encontramos con casos ya de auditoría que estaban aprobados. pero que estaban aprobados sin la audiometría Yo acá, solo para saber, no sé Gastón, si después los querés revisar porque no sé si buscan los archivos en otro lado, si se comunican vía mail con el paciente y no está quedando registrado en Salesforce ahí

Te dejo los casos después para que vos los revises Sí, sí, porque sería raro que yo pueda autorizar unos audífonos sin la audiometría, salvo que sea algún niño que con otras emisiones acústicas o potenciales evocados me suplan esa necesidad. No, en este caso no había nada que quería comentar, pero no había nada, estaba haciendo un pedido ahí. Sí, ahí lo que iba a decir de la muy, muy pequeña muestra que vimos hoy...

Perdón, hago paréntesis. Está bueno que los mires, Gastón, para quedarnos bien tranquilos de todo, pero en la pequeña muestra que vimos hoy a la mañana con Marcos, yo encontré algunos que estaban resueltos por Laura Schwery, imagino que en alguna cobertura.

hecho ella. Había un caso de discapacidad del doctor Quiroga y había un caso que se derivó por error a partir de un problema que tuvimos a línea empresa directamente y lo autorizó directamente línea empresa sin que pase el problema. Por otorri, ¿no? Lo cual es un error también, no es que hay una parte del proceso que es así. Eso justifica una parte, entiendo, bueno, de todos esos casos. Estaría bueno verlos otros por las dudas.

Más que nada, como dice Marco, para entender si puede pasar, cuándo, si está bien que siempre se deriven a ojo o si hay que construir alguna rama diferente Bien, acá los de Discapaciel y la empresa están diferenciados, ¿sí? Y tampoco tenían archivos, eso lo aclaro por las dudas porque no sé cómo funciona el caso de ellos

Los de Gastón en todo caso son estos que están acá, que son los que después Gastón si necesitas ayuda yo te ayudo a rastrearlos o te paso bien los casos que ponen en la guía, facilitas un poco más así Sí, ahí sumar y aprovechar este momento de revisión para detectar si hay alguna condición o particularidad en el proceso que tengamos que tener en cuenta para después

tenerlo bien pulido en el momento de las condiciones, no sé, porque quizás tenemos en la generalidad que tenemos que pedir la audiometría, y quizás hay ciertas condiciones que dice no, si pasa esto y esto, no, y lo vamos para adelante también tenerlo en cuenta.

Claro, las marcas, por ejemplo, en este caso, podrían ser también el presidente de Camasosa, lo que le va a hacer igual y no te preguntás nada, no lo sé. Un punto de la muestra que agarramos… que son los casos que estaban en Salesforce, vimos esto, y esto que está acá. Después, bueno, esto acá pido disculpas porque estábamos viendo los casos de autorizaciones, así que nunca corrió los casos de auditoría, acá hay cuatro casos más para revisar.

y me digan, che, mire los archivos, no podemos correr en Dolby. Perdón, Marquitos, te interrumpo un cachito antes. Lo que no entendí es, ¿los casos de autorizaciones es porque la pifieron y agarraron casos que eran de autorizaciones? ¿O porque se colaron de alguna manera en el proceso?

No, nos equivocamos si eran casos de autorizaciones. Viste que dentro de Salesforce hay como una jerarquía. El caso padre siempre es de autorizaciones, nos equivocamos, agarramos ese. Y después el caso de auditoría, en realidad sí tenía los documentos bien Lo que pasa es que ya el proceso se cortó antes, porque me dijo Che, mostro, no tenés los estudios, ya está, y no llegó nunca a la audiometría

copa te diga monstruo y bueno. Sí, me habla así. Max, perdón, iba a preguntar porque eso no me había quedado claro cuando hablamos de esos casos que son de autorizaciones. Bien, un caso hijo de la auditoría, y en la auditoría sí estaban bien los archivos, estaban completados. Sí, porque hubo un pedido.

puntual que hace el auditor, en donde se le dispara un mail al asociado pidiéndole que adjunte la documentación, y esa documentación se adjunta de manera automática al listado de archivos en el caso de auditoría, pero no se muestra en el caso padre de autorizaciones.

Entonces, vos tenés esos casos, el caso de padre de autorizaciones tiene los documentos que se cargaron originalmente, pedido médico de historia clínica, por ejemplo, y el caso de auditoría, hijo, tiene pedido médico de historia clínica y además lo que cargó el asociado en ese pedido de documentos.

Bueno, eventualmente creo que lo podría procesar, pero claro, yo de los que agarré para deducir dónde dentro de todos esos objetos estaban guardados los archivos, habría agarrado uno que era... de autorizaciones, miré su objeto AWS Files, creo que es, y ahí estaban los archivos y dije bueno, yo para buscar los archivos voy acá quizás en la autorizaciones, en la auditoría

Tengo que ir a otro lado que hoy no lo estoy contemplando. Lo digo, podría buscar. Los problemas se hacen esto, pero ahora no. La POC no estaba preparada para buscar archivos en dos lugares. Entiendo, bien, y una más, estos 22 son toda la muestra con esta evaluación del resultado de la AI por un humano.

Estas 22 son todas las muestras, no son solamente las que la IAPI fio o fue bien o no. Es todas las muestras. Es todas las muestras, perfecto. Y la evaluación esta del comentario, ¿es el comentario tuyo o de Maxi o de alguien? No, si es un comentario mío que me ve así.

¿En qué me enfoqué? Más que nada en tratar de entender si la respuesta que nos estaba dando estaba cercana a la realidad. En principio en función de los valores que me dicen, o sea, que nos pasó, y voy al caso que necesitaba por decir Te dice aprobado o rechazado, entonces vos podés mirar y decir

Bueno, éste lo aprobó, y cuando te vas a fijar los motivos por los que los aprobó te dice Mirá, el promedio de pérdida auditiva da tal valor Y por eso lo está probando Y después te fijás el gráfico y en general hay un desfasaje importante en los valores O sea, está lejos de los valores reales que están en el gráfico

En algunos casos, a niveles que es mucha diferencia, 20-30 decibeles Y acá un comentario de algo que entiendo Maxi, vos estuviste bien y también le preguntamos a la misma Ida El tema de los productos terminados como son Chachipití y... Gemini, como tenemos nosotros, hacen un procesamiento de esas imágenes Por ahora lo dejamos ahí, no es que le dan la imagen así como se la está dando a nosotros Sino que hacen algún preprocesamiento de esa imagen para que los resultados sean más óptimos o sean mejores

Eventualmente se pueden reproducir si requieren más esfuerzo, no es que simplemente estirárselo. Quiero dejar la idea de que no es lo mismo ir por la API directo que... Usar un producto terminado como puede ser Gemini o GPT o el que sea Después acá en el que pongo toma de decisiones diferentes me encontré con que

Nosotros corrimos el mismo caso tres veces, para ver si tomaba la misma decisión las tres veces, porque debería ser consistente Bueno, ahí dos casos que nos encontramos, en realidad hay un par de casos más, lo que pasa es que lo más relevante era por ahí lo que le estaba errando la audiometría, pero en dos casos concretos nos encontramos con que le estaba dando cosas distintas.

Por ejemplo, en uno te dice que lo aprueba, en otro te dice que lo dejas pendiente porque le falta tal documentación o tal estudio

¿Tiene temperatura la API, Marquitos? Sí, estaba en cero, creo. Bien útil.

Después tenés, bueno acá puse algunos bastante acertados, más o menos 10 decibeles, eso es lo que consideré yo bastante acertado Después se los dejo a Gastón para que los... los mire a los casos y los puede ir rastreando y de su opinión profesional, acá con un poco de vergüenza digo que yo los miré, pero me encantaba fijar en los datos más duros.

Después nos encontramos una hermosura que va a quedar para que algún día hagamos una presentación de una persona que subió los archivos de una manera... Que no se le ocurriría, creo que a casi ningún ser humano, debe ser el único en la Tierra que lo subió de esa manera, así que algún día se los mostramos Había un caso que daba error de sistema, así que este en realidad habría que descartarlo de la muestra Lo dejé para hacerlo con esto nomás

No sé, ¿habrá sido un caso de prueba, Fer, en su momento, cuando están implementando? No lo sé. Acá había una combinación de dos cosas, detectaba mal los valores de la geometría y encima decía que había archivos obligatorios que no estaban adjuntos, no sé si era la...

los potenciales evocados, o cual otro estudio, pero no era el caso. Acá están los otros dos casos que comentamos, que parecían medios de excepción, hay que ver si discapacidad y línea de empresa tienen otro criterio para aprobar o rechazar. Otra cosa es que estábamos considerando, no estábamos diferenciando la vida ósea de la aérea entonces ahí a veces como que también parecía que estaba tratando de armar un promedio entre las dos

No lo sé, no lo especificamos. Y acá había otro caso de excepción, el mismo caso decía que estaba como rechazado porque pero había aguditado a alguien por afuera, no sé si estaría duplicado o lo que fuera. Por ahí también hay que sacarlo de la muestra, no lo sé.

Esto fue sin hacer ningún refinamiento, o en algunos casos sí, pero sin haber hecho algunos refinamientos, que lo dejo a Maxi de Cuente, que estuvo trabajando, pero es Estamos tirando el archivo crudo, tomá, arreglate, y te encontrás con todo, ¿no? Escaneos, había uno que era una tira, era un escaneo de una tira fina donde estaban todos los valores de...

de la audiometría y del estudio, con formatos muy diferentes, con calidades muy diferentes, lo que hace que también sea lógico que les cueste identificar los gráficos. Para entender de los que hice correcto AI, tenés 4, 5, 6... 7, 7 de 22, un 25%, 7 por 4, 28, no, un poco menos, un 30% a ponerle, de que anduvo bien.

¿Qué era más o menos los números? ¿Cómo? No, te hago una aclaración. Hay que separar dos correctos. Nosotros estamos haciendo la validación de los archivos y después que sea correcta la... no te voy a decir la interpretación, pero ponele que sea la interpretación.

Acá lo que está correcto es que identificó y te dijo, che, nunca me mandaste la audiometría Pero no avanzó, o sea, no puede avanzar con algo que no tiene, ¿no? No te estaba diciendo... Ok, ok, está bien, es correcto en algún lugar En realidad, o sea, que debe ser menos el valor de correcto Es menos, es menos Con lo cual, va al 20% ese que había mostrado vos en algún momento La fantasía de tirarle el paquete y que lo resuelva no existe, digamos, obviamente

vamos a tener que preprocesar todo y ahora lo que viene seguramente Maxi. Claro y ahí ya lo dejo a Maxi hablar pero también el laburo que implica nosotros estamos hablando de una sola práctica en este caso. Y el laburo que le implica a Maxi, trabajar sobre estas solas, con el desarrollo de los distintos prompts que tuvo que hacer, ahora lo dejo a la Israel

Pero tuvo que recortar las imágenes también para mejorar la performance, como que hay un montón de variables Por eso la vez pasada, y con esto ya cierro, planteábamos esto de decir Por ahí hay otras prácticas que tengan menor complejidad y mayor volumen Menor complejidad con respecto a que, y por ahí...

De base ya te digo que no tengan imágenes ni tengan gráficos Cosas que sean texto, pueden ser informes, por ejemplo, de diagnóstico por imágenes Otros tipos de informes, pero pareciera ser que acá está difícil Sobre todo, bueno, estuvimos viendo más esta, que es la de gráficos Pero en la de imágenes me suena que va a ser igual, excepto que traigas un modelo específico de imágenes

Te vas a encontrar con un desafío igual y ahí sí, Max, te paso por si querés comentar algo más. La primera pasada fue agarrar cada gestión, todos sus archivos, y en una pregunta, en una llamada, Germín le daba todos los archivos Y del pdf de política no se le dio el pdf entero, sino que lo pasé por un preproceso de extraer las partes importantes, porque la política tenía 13 páginas y la parte de aprobar o rechazar, son muy acotados los criterios de aprobar o rechazar. Así que esa es la única.

como dices, el único procesamiento que tiene que dar una política un poco más concisa pero después es, se le da todo y lo que genera, bueno, esto que venía a enseñar Marcos, cuando vos le das todo No es que se distrae, pero quizás es mucho y no hace foco en cada cosa y lo que decía Marco, por eso lo probamos tres veces en igualdad de los casos y a veces o lee mal los valores y lo lee

formas más diferentes y a veces se los inventa completamente. Respecto a lo que estamos hablando de imágenes gráficas. Sí, aparentemente hay una tendencia a que sea más complejo, pero también creo que depende de cuál sea el input que tenemos porque en este caso, como decía Marco antes, si es una foto rotada, un screenshot dentro de un PDF

Por más que lo que está adentro quizás sea texto, igual capaz que no lo puedes procesar Y si fuera gráficos que son, creo que son los de la timpanometría, que creo que son más... en los pocos casos que me di a mano, es como algo más impreso, te lo tiras a la máquina no hay marquitas manuales que pone Plotorrino, entonces eso quizás podría ser más fácil de entender que una biometría donde...

son circulitos, callitas y tipo una llavecita, todo junto, en el mismo gráfico, lo mismo en la logometría, donde ahí sí tenés el factor de... de Virome, y además, indigno por la particularidad del estudio, que se te mezcla el circulito de la vía aérea más la rayita de la vía ósea

Entiendo que si escuchás igual de la misma forma, queda todo junto, que la audiometría queda un chino en un circulito, o una rayita con el circulito y un piquito en el medio. es complicado que a Jaime le diga identificar el circulito y tomar el valor del centro del circulito para vía aérea no es tan fácil, hay audiometrías donde, no sé por qué, te da que los circulitos a lo mejor están más abajo y los piquitos del aviado están más arriba, y quizás sí los puede distinguir, pero cuando coinciden

es un chino y eso, no sé si lo que hemos visto son la regla o la excepción, no sé, en masa digamos con qué nos vamos a encontrar y eso es un poco lo que queremos tratar de... de ver en masa qué es lo que vemos. Bueno, bueno, Pablo. Maxi, mira, la audiometría, la normal va a ser así, digamos. Claro. Encuentres.

el circulito y el piquito de un lado y el circulito y la crucecita del otro, pegaditos porque es como funciona normalmente el oído, si vos ves como decís que están separados que eso lo puede leer mejor, en realidad la persona no es que esté bien, sino justamente que tiene un tipo de enfermedad en el oído y eso, bueno, obviamente se grafica así, pero si no, lo normal es así.

que vayan las dos cuestiones juntas Claro Después, en cuanto a los archivos que hemos visto también, señores Marcos, creo que es en la parametría, creo que Por el archivo que veis siento que debe haber una máquina que te mide y te saca un informe, parece un ticket Tenés de los dos, tenés de...

de profesionales que tienen como decir, bien voz, digamos una maquina de estilo ticket donde te marca, digamos, los reflejos acústicos y las... y las presiones en el oído medio, y tenés también a las profesionales o a las licenciadas en foro que te lo hacen manual también a eso, o sea que también tendría que leer

manual y es el más automatizado, como decías vos, de las dos maneras se puede venir. Ahí lo menciono porque, por ejemplo, en el caso este que sale como chiquita como un ticket, Más allá de que parecía un ticket y no era una impresión térmica por la calidad, salía medio comprimido, a eso hay que sumarle el factor de la foto que tiene la sociedad, porque tiene el papelito y le saca una foto, es una foto de un ticket, digamos, y eso ya...

te suma, digamos, para más, digamos, complejidad. Hicimos unas cuantas pruebas y donde por ahí pude obtener buenos resultados, problemas consistentes, es en lugar de esta estrategia de... Te doy todos los archivos, con todos los estudios y la política, y una instrucción de, no sé, detectar todos los estudios, evaluar cada uno Una estrategia...

mucho más trabajosa, que requiere más mantenimiento, pero es lo que Finotek va a terminar siendo necesario para ganar productos, digamos, y que sea consistente en lo que hace es... por ejemplo, agarrar cada archivo, según la política, identificar dentro de todos los archivos, dentro de todas las páginas, dónde está cada estudio, recortarlo y después...

una llamada a Gemini por cada estudio y con cada pedacito de imagen decirle interpretá esta audiometría sin nada extra que lo pueda confundir, es darle el pedacito de audiometría y que vaya creciendo los valores. Se siguen enfrentando con los mismos problemas de si está el piquito, la rayita, el circulito, todo menos junto. Más se confunde y a veces te dice, para mí está en 3, para mí está en 20, o en 30, o está en el medio 25.

puede seguir pasando, pero no un pasarelondo que empiece a confundirse o que invente, digamos porque está dando concretamente el pedacito de... de gráfico. Eso lo que implica es también, cada llamada es decirle que tienes que extraer los valores de las tres frecuencias que se usan, serán 100, 1000 y 2000

de cada gráfico y se implica tener que, no es programar, pero bueno, definir el prompt para cada estudio por cada estudio Ahora tengo definidos los 6 prompts, uno por cada estudio y por cada lateralidad porque, o por lo menos en el caso de la biometría, hay que explicarle a uno que tiene que mirar los circulitos en el otro las crucecitas, cuestiones de colores

Rodrigo, querido, ¿cómo estás? Más laburo de un catálogo de estudios Los micrófonos también los van a llevar ustedes Perdón que justo estoy manejando Quería saber más o menos para cuánta gente es O si sabés qué más o menos que necesitan de TEA Y de retorno, ¿cuánto sería?

Para nosotros, ¿cómo se lee un audiometría? ¿Qué valores nos interesan? Más o menos, ¿qué necesitan de pegar? Y, sobre todo, ¿cuánto valen? Se define una salida estructural, ¿eh? Yo quiero que nos valoren las frecuencias. ¿Querías saber más o menos cuánta gente es?

¿Y el promedio? Y lo que le sumé fue, en caso de una interrupción eventual de Chemina y Beck, qué opinan de esos valores, digamos, que después pueden o no tenerse en cuenta contra la política, digamos, porque la política solamente va a volverlo... los valores crudos que se trajeron pero, para tenerlo pero bueno, ese fue como después de un montón de pruebas, fue como que

la forma de que sea consistente, y probé un montón de veces con el mismo caso que creo que lo había pasado en el chat que tenemos, de que me entienda la audiometría y de pasárselo un montón de veces y que me lo lea bien y que lo lea consistente teniendo en cuenta que solamente si le vas acotando lo que le das como entrada, no darle todo el archivo

No darle todos los archivos, ni darle todo el archivo, ni darle toda la página, ni incluso llegar al punto de darle como un recorte para aislarle cualquier otra cosa que... y lo pueda confundir. Ese fue el punto donde logré, por lo menos lo lea mejor, digamos, y todo eso mayormente con audiometría

El primero que agarré fue el que más peleé, después del resto también puede tener su dificultad. Por los ejemplos que vi, la timpanometría no tanto, porque en los casos que vi no estaba tan hecha a mano digamos, era más fácil que los interprete La logobiometría vi también casos donde en un estudio tenés dos gráficos, uno por cada oído y otro donde tenés uno solo para todo y tenés todas las lignitas con distinto color

pero está todo junto y eso también puede ser una complejidad que puede afectar, digamos, a la gente en mayor o menor medida depende del volumen que tengamos de la normalidad de lo que nos den nuestros... asociado digamos, si todos los asociados nos dan la mayoría, las audiometrias que están separadas y que son fáciles de leer nuestro éxito igual que el éxito de la gente va a ser mayor, si la mayoría de los asociados te dan

Por ejemplo, las biometrías que están todas en el mismo gráfico, que no son claras y que la calidad del archivo tampoco ayuda, es difícil. Así que para eso creo que lo que hablamos al principio es una muestra un poco más grande y ver o, decía Marcos también antes de...

ver si podemos identificar esa posible complejidad o simpleza en otras prestaciones. Si esto que vimos es... De todo lo que se pasa por auditoría, de todas las especialidades, si esto es lo más fácil, es lo normal, es lo más difícil, para saber a la hora donde ir.

No sé en qué momento entró Pablo, o cuánto escuchaste.

Entré cuando estaban hablando de la biometría y de la separación de la crucecita y el circulo Estaban mostrando los resultados que nos habían dado, que son variados, pero nos está costando, en resumen, nos está costando que identifique bien los valores.

Algo que comenté antes es que es diferente Gemini como producto porque hace un procesamiento de las imágenes hoy nosotros no lo estamos haciendo a la hora de entregárselo vía API las trata diferente, por ahí por eso obtenés en algunos casos, no siempre, resultados mejores a través del chat

Que de vuelta, no se trata ni siquiera del modelo, porque Maxi probó, si no me equivoco, Maxi probaste con el modelo más caro que estaba disponible Así que también se llevó el modelo a... el mejor que estaba disponible Y ahí el planteo era, bueno, por ahí...



O sea, alguna vez hay que, o se siga refinando esto y se trata de recortar los archivos Y tratar de dárselo lo más curado posible a la inteligencia artificial O de tratar de mejorar la calidad de las imágenes o lo que fuera como para seguir intentando mejorar la eficacia, en este caso en particular, o la otra también, es decir, bueno, ¿qué otras opciones tenemos de prestaciones que sean más en vivo?

de mayor volumen y que, en principio, no requieran, como para ir por el camino un poco más sencillo, que no requieran ni de imágenes ni de gráficos, como es este caso. Y ahí es un poco la tarea para que pensemos todos cuáles pueden llegar a ser esos casos.

práctica no necesitaban la audiometría. ¿Por qué empezamos por la de la audiometría?

Porque teníamos volumen y porque elegimos esa, pero después en el archivo, que ahí si querés lo comparto, les había pedido que me armen... ¿Me completas esto?

Y acá ya se ve que en todos estos casos, si bien no se requiere de un gráfico, acá hay imágenes médicas No sé si en todos los casos realmente las necesitan o no Por ahí esa parte nos la pueden decir ustedes Pero si hay imágenes médicas Lo más probable es que nos pase algo parecido a lo que pasa con los gráficos Estos modelos no están especializados para ver imágenes médicas

ni para interpretarlas, ahí hay que buscar otros modelos que sean buenos Gastón, ahí dijo Martín, perdón, y ahí Gastón, de todos los que vos pusiste imágenes, son imágenes, solo imágenes o imágenes con informe? No, no, no, sí podemos basarnos en el informe, yo lo puse como para tenerlo más completo porque puede tener digamos de las dos

Pero la mayoría de las veces viene con el informe que es texto y ya está, digamos, difícilmente nosotros no estemos de acuerdo con el informe, es raro. No, no, perfecto. Respecto a lo que decía Marcos de las imágenes médicas y los gráficos y demás, el tema de los gráficos, no sé si pudieron, no sé si había gráficos de compu y gráficos a manopla, supongo que para esa biometría debería haber de los dos, supongo que los de...

mano, deberían ser un poco más difíciles de interpretar a priori desde el prejuicio, no, desde la evidencia de autorizaciones y eso es todo un tema. Y después para imágenes médicas hay modelos especializados en imágenes médicas que andan bastante bien, depende la imagen, depende de que esté buscando obviamente.

Y supongo que para el caso de los que acá dice análisis de imagen, que por lo que veo son todas las cirugías, es tratar de buscar cuestiones anatómicas, digamos, dentro de las imágenes, no es que estás buscando... digamos, variaciones de densidades así raras, sino que son más cuestiones anatómicas para la cirugía. Por lo tanto, digamos, pensando en un modelo de imágenes médicas específicamente, quizás sea un enfoque un poco más copado. De todas maneras...

por lo menos en la experiencia que pude tener yo con imágenes médicas, no esperen grandes cosas, digamos. Si lo que están buscando le digan, che, mira, tiene o no tiene, qué sé yo, a ver, un aumento en el tamaño de las amígdalas, en la resonancia... te va a dar cualquier cosa. No es claro, ni fácil, ni simple de interpretar, por más que tenga su modelo de imágenes médicas. Quizás deberíamos, y con esto cierro, pensar en no incorporar el análisis de imagen, por lo menos en una primera etapa. Cambio.

Sí, ahí lo que podemos hacer es tomar estos casos, darlos como que no requiere análisis de imagen, así que lo cambio acá y lo dejamos para analizar con el proceso que está. que analice el texto y lo cruce contra las políticas y creo que es, perdón Tejo, por eso pregunté lo del informe, digo pues la imagen del informe, no todos ya tenemos la resolución en un informe, digo para que vamos a ir a mirarla de nuevo

Quizás podemos de alguna manera pedirle que como resultado nos diga, porque no vamos a tener discriminado el informe de la imagen.

como para poder medir una tasa de volumen de casos que sí vamos a poder trabajar, que nos diga si existe o no existe el informe relacionado a ese documento de imagen. Porque la categoría tiene estudios previos, con suerte. No, no entendí, sorry, perdón. Vamos a tener de esos casos en donde pusimos análisis de imagen, no vamos a tener casos que vengan con el informe y casos que no vengan con el informe y que tengan solo la imagen, que es lo que contaba Gastón.

Bueno, ahí si está sobre la imagen. Que nos diga si tiene o no tiene el informe de última, como para poder sacar un porcentaje de todos estos casos, en este porcentaje tenemos el informe. No, no, está bien, por eso la idea era que nos juntemos y lo podamos charlar, si consideramos que...

digamos, descartamos lo de la imagen, en los casos que viene Perdón, ¿hacemos eso que dijiste? ¿Hacemos la validación? Si está el informe, nos basamos en el informe, si no está el informe... Habrá que derivar lo humano, pero en este caso, estamos haciendo las pruebas, miramos si está el informe y con eso, cruzándolo con las políticas, vemos qué resultado nos da y hacemos la evaluación otra vez y nos volvemos a apuntar.

Ok, revisamos el archivo de los 22 con Gastón o ya no vale la pena y nos enfocamos en esto. No, no son focalidad en esto, la verdad. Lo que necesitamos son casos que ahí no sé si vos no los podés pasar o... ¿O tenés alguna forma masiva, Maxi, de detenerlos? No, necesitas los case ID, ¿no?

No, quizás lo pueda buscar, porque de lo que fui buscando ahora, termino buscando contra Salesforce y entiendo que puedo mirar él Que hay ricos ítems, con el número de práctica, creo que podría buscar casos, pero pruebo y les digo. Ahí lo que quería preguntar es, de estos casos...

Entiendo que vamos a revisar eso y responderle a la política, si de estos están las políticas, porque entiendo que habíamos arrancado también con el de los audífonos porque esa estaba definida en la política. Y sé que hay algunas más, pero no sé de cuáles está la política. Si es que la queremos y si no, bueno, se puede hacer el control de una prueba de ver si está o no el informe, pero.

Max el de cirugía endoscópica todavía está medio como en revisión, de lo que es septumplastia, migralectomía Turbinectomía, sinusotomía, tiene que estar. Y bueno, timpanoplastia y mastoidectomía también, ya los habíamos visto. El timpanoplastia, creo que decía que requería imagen Timpanoplastia, sí. O sea, puede venir informe, puede venir imagen, puede venir...

El gráfico también. Ah, pero puede tener gráfico, por eso estaba encargado.

Estas son las que nos habían compartido Martín en su momento, que venían trabajando, no sé si era una reversión. No, lo que te compartí estaban cerrados, que eran los que estábamos viendo de hecho con Gaspi. en los viernes, y quizás haya alguno más porque se sigue avanzando. Ok, bueno, tomamos los que tengan política de ese listado que quedó ahora.

Y bueno, hacemos la evaluación de cómo da con los resultados.

La pregunta de rigor, ¿nos volvemos a juntar el martes o necesitamos más tiempo?

No sé, Maxi, ahí ¿cuándo tenés que ir? El lunes a la mañana, si no recuerdo mal, ¿no? Sí, el lunes nos juntamos también, si tenemos... Si podemos, lo hacemos el lunes a la mañana, pero me parece muy pronto, por eso... No, no, para la evolución, el lunes a la mañana, no, no...

No, porque no hay tiempo para todo, pichamos y nos vamos. No, el lunes es muy de cheque semanal, nada más con Pablo. Ah, perdón, perdón, perdón.

por eso si nos juntamos el martes y definan la semana si nos juntamos el martes como como lo vemos máximo De acá al lunes a las 8 de la mañana, pichamos todo y nos vamos. Martes última hora. Ah no, claro, mañana hay que trabajar el doble. Mañana el día del trabajador se trabaja al dólar y se paga la mitad.

Por eso Maxi, ¿cómo lo ves vos? ¿Martes, última hora o directamente el jueves? Sí, lo dejaría para el martes porque además el lunes veo bastantes reuniones, así que... o sea, todo lo que, la del lunes la cancelamos porque ya estamos acá todos, y quedamos entonces el martes.

Muchísimas gracias.

A las 3 de la tarde. Perfecto. ¿Sí? Excelente. Dale, buenísimo.

¿Tenemos algo que nos preocupe respecto a esto, además de lo que vimos hoy? Sí, que el crudo... A mí me preocupan mucho dos cosas. Una, que el crudo tiene... tan horribles resultados. Y segundo, que no haya coherencia a pesar de tener temperatura cero en el modelo. Eso me preocupa mucho, mucho, mucho, mucho porque no hay forma de manejarlo.

Digo, Maxi, corregime, si me equivoco, pero no hay forma de manejar con temperatura cero el modelo que te siga generando incoherencia en la respuesta contra el mismo modelo. Eso es choto. Jodido. Por eso lo probamos un par de veces, que es literal sin tocar nada, llamo una vez, guardo el resultado y tera, y ahí es donde te da resultados diferentes.

¿Qué se supone que es producto mayormente de que tengan que interpretar los gráficos? ¿Gráficos y de archivos, como si, como Pérez decía, cuando le das el archivo entero, o en este caso muchos archivos, por algo que hablábamos la otra vez, de...? También, si vamos a confiar o no en la tipificación que te dan, si no vas a confiar y tenés que procesar todos los archivos en esta primera versión que fue te doy todos, te daban, en la gestión quizá le daban tres archivos donde estaba

Dice, uno era el pedido médico, otro era el informe, que tenía tres o cuatro páginas, y otro era no sé si estaba catalogado como historia clínica, que eran dos renglones, pero le tenías que dar todo, y cuando le das todo y le pedís un montón de cosas, dispara un poco para donde quieras, y ahí sí, una forma de controlarlo por más temperatura que te pongas.

Nada, se agarra para otro lado, sonaste y no tenés forma, yo sabía que estaba haciendo cualquiera porque veía el gráfico y le preguntaba a Gastón de Che, ¿cómo se tiene que interpretar esta audiometría? Me dijo los valores y yo veía que nada, daba cualquier cosa. Y por ahí te dice, no, sí, los dos oídos dan 60 y ni siquiera se parecen los gráficos, o sea, se pone vago y...

para cualquier lado y esa y por más que lo que tiene difícil de hacerlo incluso en un solo prompt que no por más que le quieras decir No te equivoques, o un estudio, en esta política, y no sé en el resto de políticas, tiene que evaluar tres estudios por dos lateralidades, es un montón, entonces no le podés, es muy complicado decirle que sea específico mirando todo.

No encontré forma, probé un montón de formas, pero en una sola pasada que entienda y que sea consistente, no logré. Como decía, solo logré cuando... lo pasé por un proceso de recortar la imagen e irle estudio por estudio y lo analice como que se enfoca solo en ese archivo que le das chiquito y en la instrucción precisa de

que esto es una biometría analizada, la única forma más consistente de que lea un poco mejor y que además, si lo ejecuto dos o tres veces, lee lo mismo, que eso es por lo menos lo más... importante que sea consistente porque si no, en la primera prueba no hay forma de confiarle nada.

Che, Maxi, ¿una? Ah, perdón, dale, dale, Pablo. No, no, no, tocino mal. Ah, perdón, vi que se movió y... Che, Maxi, me quedé pensando que dijo Marcos, que decía que cuando tenías paquete cerrado de Gemina y qué sé yo, preprocesaba las imágenes y nosotros la estábamos pegando con lápiz derecho y no hay preprocesamiento de la imagen, ¿entendí bien?

Son dos cosas, y que Gemina en el chat cuando vos le das un archivo y le pedís que haga algo lo que hace atrás es, no es un solo prompt, digamos hace todo un procesamiento de de que él solo va decidiendo qué es lo que tiene que hacer y revisa todo lo que tiene que revisar la imagen, si la tiene que rotar en la parte de su modelo de visión, y si necesita alguna...

tool para recortar o lo que sea, lo hace. Cuando vos lo llamás por API, no estás como simulando el chat, estás dando una sola instrucción, estás pegando al modelo, no es lo mismo. Y ese pre-procesamiento, lo que se hace ahora es, lo hace Sheminer, digamos, lo hace el proceso que es a través de Sheminer, por ejemplo, le digo, ubicáme en los estudios, dónde están, en qué página, en qué parte.

y después con un código, ya no lo sé, para agresiones, recorto ese pedacito de la imagen y le doy la imagen recortada, o no hace nada, Gemini, digamos Claro, no hay detección de bordes, no hay ningún algoritmo de nada para mejorar, digamos, la imagen y la interpretabilidad de la imagen. Claro, acá solamente la recorto. Eventualmente, también dependiendo de la naturaleza de los estudios y de lo que tengamos que pensar, posiblemente tendrías que pensar en un paso de...

no sé, mejorar contraste o ese tipo de cosas, el tratamiento de la imagen para ayudarlo, porque acá también son o papeles arrugados, torcidos, con poca luz o con sombra, que eso también puede ser confundido, pero bueno ahora no avanzamos en eso Era tiempo, pero, y porque quizás no hace falta, pero también, como decíamos antes, todo depende de cuál sea la normalidad, la naturaleza de lo que nos dan nuestros asociados para decir.

Tengo que avanzar incluso en eso de, lo tengo que recortar y tengo que hacer un post-procesamiento de pasarlo a blanco y negro, mejorar el contraste, comistarlo, que eso Shemenya no te lo va a hacer, bueno. Hay que ver, o probar otros modelos, pero son variantes, y variantes, y variantes. Sí, sí, necesitamos más Maxis.

Y claro, me quedé pensando porque si lo que te está, de alguna manera, en función de lo que dijiste vos de que el error o potencialmente la diferencia en interpretación está en que reprocesa las imágenes cada vez y a mí da cuenta de que no le estamos haciendo ningún preprocesamiento a la imagen, sino que está yendo el recorte crudo, digamos, para que lo reconozca, quizás metiéndole algún preprocesamiento a la imagen sí mejore la

la coherencia, ¿viste? Para bajarle volumen de info a la imagen, bajarle dimensiones a la imagen y que sea un poquito más fácil de interpretar, o por lo menos de interpretar siempre igual, ¿no? En ese plan lo decía. Marquitos, perdón. No, sí, iba a responder sobre eso. La pregunta de eso es, si seguimos haciendo ese trabajo, eso implica que Maxi siga iterando y viendo cómo ajustarlo para lograr mayor eficacia en...

en las respuestas. Y la pregunta que sigue, ¿ese es el camino que queremos seguir para estos estudios? ¿O entendemos que hay otro camino de menor esfuerzo con más ganancias? tratando de que eventualmente por ahí llegue este punto, ¿no? Lleguemos acá y digamos, che mirá, ya recorrimos este camino y, bueno, ahora nos toca la saudiometría y sí, veamos cómo lograr que sea lo mejor y ahí tratamos la imagen, la recortamos, hacemos diez millones de cosas para que sea mejor

Sí, Marco, por eso yo arranqué preguntando por qué habíamos arrancado por el más difícil. Arranquemos por un éxito, digamos, y después veamos cómo va. Lo yo hoy vería de empezar a probar con los que son básicamente basados en texto o en lectura de texto, informes, pedidos.

y ver cómo nos va a ir. Digo, coincido, porque también, si no, lo que dijo Martín recién, es desalentador que ya lo primero sea tan negativo. Yo me parece por lo menos, primero porque no son la mayoría de los casos, la verdad que uno que está auditando la verdad, en el volumen que tenemos...

No son la mayoría los que tenemos que interpretar una imagen o interpretar un dibujo hecho a mano. La mayoría lo basamos en texto, en informes. Yo iría por ahí, por lo menos por probar esos casos de uso y ver qué tasa tenemos de efectividad. Y después veríamos si queremos resolver esto, esto que están planteando, que me parece que está muy bien.

Sí, sí, igual el trabajo que se hizo hasta ahora, que es el que viene haciendo Maxi desde la semana pasada, es armar el flujo que es medio genérico Les habíamos pasado ese Excel que estaba compartiendo antes, donde estaba la tablita, como habían puesto que interpretaban imágenes, bueno, obviamente también entrábamos en un problema similar Ahora que nos dicen que no, la mayoría no requiere de interpretar imágenes, listo, bien, vamos con eso

Así que nada, nos enfocamos en eso y la próxima semana nos juntamos y vemos cómo nos va.

Creo que ahí va a andar mejor, probablemente. Ok. Buenísimo. Nos encontramos el martes entonces. Excelente fin de semana. Gracias.

[https://docs.google.com/document/d/1CIA7j58bPMJLoMGa1O7K8eJm2HllFMzxXVhEJy4-EXA/edit?usp=sharing](https://docs.google.com/document/d/1CIA7j58bPMJLoMGa1O7K8eJm2HllFMzxXVhEJy4-EXA/edit?usp=sharing)

▶ **20260511**

<!-- unknown block type: transcription (35d2c02a...) -->



### Acción Items

- [ ] Martín y Marcos: Correr la IA nuevamente con la política actualizada y más flexible  
- [ ] Buscar casos que tengan toda la documentación completa para la nueva corrida 
- [ ] Pablo y Fer: Pensar sobre si existen criterios más objetivos ("datos duros") que se puedan usar en lugar de síntomas subjetivos  
- [ ] Equipo: Definir si se mantendrán las políticas estrictas y se educará a los prestadores, o si se ajustarán las políticas a la práctica actual 
- [ ] Agendar próxima reunión para revisar los resultados de la nueva corrida 
### Resultados de la Reunión Anterior

- La IA rechazó casi todos los casos en la corrida anterior 
- El problema principal fue que la política era demasiado estricta comparada con lo que los prestadores realmente documentan en la práctica 
### Revisión de Criterios de Cobertura para Septoplastia

- **Deformidad "severa"**: Se discutió eliminar la palabra "severa" ya que la mayoría de casos no especifican severidad, y cuando lo hacen, generalmente reportan deformidades leves   
- **Fracaso de tratamiento conservador**: Los prestadores rara vez especifican tratamientos previos en las historias clínicas, por lo que se propuso hacerlo opcional   
- **Síntomas obstructivos relevantes**: No suelen venir explicitados en esos términos específicos en la documentación  
- **Imágenes (TAC/RMN)**: Se mantienen como parte de los criterios, ya que la mayoría de casos las incluyen 
### Debate Estratégico: Políticas vs. Realidad

- **Posición de ajustar políticas a la práctica actual**: Flexibilizar criterios para evitar burocracia y fricción con afiliados, reconociendo que los prestadores no documentan exhaustivamente  
- **Posición de mantener políticas estrictas**: Los prestadores deberían hacer un esfuerzo por justificar las prácticas adecuadamente, similar a cómo otros especialistas justifican tratamientos específicos   
- Pablo enfatizó que es una oportunidad para educar a los prestadores sobre requisitos de documentación   
- Martín destacó que se debe decidir si se busca concordancia con el pasado o si se define una nueva política a partir de ahora  
### Decisión sobre el Enfoque

- Se acordó que la política debe reflejar lo que el auditor realmente utiliza, pero no debe adaptarse a la falta de documentación de los prestadores  
- La IA debe resolver problemas de interpretación cuando la información está presente, no cuando falta documentación  
- Si falta documentación, es parte del proceso que los auditores eduquen a los prestadores   
- Martín propuso que si un caso tiene toda la información necesaria pero falta algo, se autoriza igual si la evidencia objetiva (como imágenes) está presente 
### Aspectos Técnicos del Modelo de IA

- Marcos explicó la diferencia entre usar Gemini en el chat público versus su implementación: en su caso, deben construir todas las capacidades y el proceso paso a paso   
- Están usando Gemini 2.5 en lugar de versiones más nuevas por cuestiones de costo y disponibilidad 
- Se discutió la posibilidad de crear un enfoque más "agéntico" versus el proceso ordenado actual  
### Consideraciones sobre Implementación

- Marcos planteó que al cambiar las políticas habrá una "ola" inicial de rechazos, y sugirió enfocar la IA primero en detectar y procesar rechazos por documentación faltante    
- Los auditores deberían enfocarse en casos rechazados por incumplimiento de política, no por falta de documentación  
- Uno de los objetivos del proyecto es que los auditores tengan más tiempo para relacionarse con prestadores y menos tiempo administrativo 
### Desafíos Identificados

- Muchos criterios dependen de síntomas subjetivos (dificultad respiratoria, insuficiencia ventilatoria) que son difíciles de verificar objetivamente    
- Marcos preguntó si hay otras especialidades donde existen "datos duros" más objetivos, como registros de glucosensor para bombas de insulina 
- Pablo reconoció que en muchos casos médicos hay síntomas que no se traducen en mediciones objetivas y hay que confiar en la palabra del médico  
### Próximos Pasos

- Se correrá nuevamente la IA con la política actualizada y más flexible  
- Se buscarán casos con documentación completa para evaluar si la IA interpreta correctamente  
- Los casos sin documentación completa serán rechazados, y el proceso incluirá educar a los prestadores sobre requisitos 






Un placer.

Un poquito dormido, pero bien.

Buenos días.

ahí está la Patricia, ¿Escuchaba

En la medida de lo posible. No, hace un rato ya estoy. Ya estoy para la siesta. Ya estamos para la siesta. Por Dios que llegue rápido.

Yo les decía que no es un horario la limitante de la siesta, no es una limitante el horario de la siesta, vos decís son las cuatro o cinco de la mañana.

Adiós, adiós, adiós, adiós,

¿Lo esperamos a Pablo? ¿Sabemos? No dijo nada.

No, yo le pregunto, pero arranquemos, arranquemos.

Yo les dije que nos juntemos porque quería que me cuenten cómo les fue la reunión de la semana pasada. Le van a revisar las políticas. Vi el resultado, así huelo de pájaro, les digo, va a volver a rechazar casi todo. Bueno, también un poco qué es lo que pensaron y...

¿Quieres contarlo vos o lo cuento yo? No, no, contá, contá, tranquilo

¿Está bien? Sí. Sí, perfecto.

de barreros y lujano en cabeza y cuello, ese queda, digamos, obviamente. Porque necesito la indicación de de la de la prestación. Resumida, eh, diagnóstico, eh, diagnóstico documento

fibro larinco, la rino débito humano, son opcionales ambas, y para perforaciones septales, estiología documentada. Cuando pusimos los criterios de cobertura, que es lo que suponemos que va a leer la... el algoritmo, la gente, pusimos que el núcleo confirmado por ORL, estoy teniendo que especifique deformidad radio, todo esto, ¿sí?

suficiencia, y o, acá lo que le cambiamos, y o, imágenes de TAC o RMN, orribo, ribo, fibro, la lengua, que objetiven la alteración anatómica. Bien, hay algunas cosas que triggerean a la idea generativa como esto de ser tan severa. La severa no entra dentro de lo que por lo menos en la práctica estuvimos viendo de los casos. La mayoría de los casos no son severas ni moderadas, digamos, son leves.

Por eso les digo, hay ciertas cosas, lo que está escrito acá, que me da la impresión, lo corremos igual, no pasa nada, pero me da la impresión de que va a volver a pasar lo mismo que pasó al principio, que es que rechazaba a todas. Presento que esto sea la definición de auditoría de qué es efectivamente lo que se quiere hacer y bueno, por ahí esté bien que la rechace toda, no sé, es una pregunta para...

O sea, puedo decir que sacaría la palabra severa y que queda como deformidad acertal. En la práctica, Gastón, ¿cuántos de los que te mandan dicen severa? No, no, bajo porcentaje. Por eso. Excepto que ustedes quieran ponerse, pero esto no tiene que ver con la IA, esto tiene que ver con la definición de ustedes, excepto que ustedes se quieran poner más duros y decir, si no vienen con una deformidad severa, no hacemos nada.

Esa es la pregunta, Gastón. Si no dice sedera, ¿vos la rechazás? No, no dice sedera. Con ese criterio tenemos que revisar toda la política. Específicamente eso. todo lo que diga acá va a ser totalmente inflexible para la guía. Entonces, si acá dice Severa, tiene que decir Severa del otro lado y así con absolutamente todo.

No sé si hay alguna otra cosa para comentar. Y por ejemplo, estoy leyendo lo que dice, fracaso del tratamiento conservador. La mayoría de los casos yo no vi que especifiquen nada de tratamientos previos conservadores. Por eso lo habíamos puesto ahí como opcional.

muy poco lo describen dentro de las historias clínicas.

¿Se lo puede poner como opcional a eso?

Sí, sí, pues en realidad digamos no siempre, o sea, el código este lo es el que piden siempre para corrección de tablique, pero no siempre son por cuestiones. de perforación que sí o sí vayan a requerir un IHERT.

Sobre todo porque no viene explicitado, no quiere decir que no sea real, pero en la práctica no se veía, por lo menos en los casos que yo estuve mirando, que son pocos la verdad. pero si ese ese digamos no viene así muy muy muy aclarado el tema de la.

los síntomas si son obstructivos o relevantes o no.

Dentro de las imágenes, oh, oh, oh, historia clínica, se ponen.

Se pueden llegar a poner dificultad respiratoria, bloqueo nasal, pero no es que lo vayan a poner en esos términos así como relevantes.

Sí, Valo va a rechazar.

Y si se puede poner como opcional ese también.

¿Desclusión? Sí. Bien. Bien. Entonces sí lo sacarían.

Hay una duda, dos cosas se me ocurren, porque también si empezamos a sacar todo.

Los prestadores también deberían hacer un esfuerzo por justificar las cosas, también es un criterio de educación.

Hoy, mi esposa que es diabetóloga, cuando llena la planilla de la diabetes para que den algo, ella sabe lo que tiene que justificar para que se lo den. Si no lo ponen, no se lo van a dar, digamos. Me parece también que los profesionales, que hoy un profesional va a pedir una septuplastia simplemente poniendo Olor a barcos, Sanco Salud.

Número tanto, septuplastia, obstrucción nasal, y pretende que nosotros se la probemos, y me parece que no.



No sé, creo que también parte de este proyecto es que nosotros tengamos tiempo de hablar más con los prestadores y educarlos, ¿no? Che, justificáme, hace un esfuerzo. No sé, porque lo que siento es que estamos quitando, quitando, quitando, quitando criterio entonces ya prácticamente hasta pierde la razón de ser tener una política.

eh coincido, coincido Pablo con vos digamos eh de que estaría buenísimo de poder digamos que el que los los profesionales justifiquen a la perfección la práctica realizar, el tema es que en la práctica digamos en la diaria no pasa eso y muchas veces para evitar, digamos, lo que justamente no se quiere tanta burocracia ahí de vuelta de del afiliado en su momento, porque ahora sí podemos de últimas hablar directamente con los prestadores.

Es como que se flexibiliza un poco para no dejar de por medio al afiliado. Pero sí, yo considero lo mismo que digamos que podría llegar a hacer. Porque hay profesionales que hacen muy buenas historias clínicas y otros que, o la gran mayoría, que no. Sí, ahí lo que me pregunto es, ¿qué queremos nosotros como zancos? Perdón Martín, ya te dejo. ¿Qué queremos nosotros como zancos?

Entiendo cuál es el punto de partida hoy, ahora, nosotros queremos ir a bueno, no le vamos a romper las bolas de hacer tu plata, la vamos a autorizar toda, bueno, listo. Digo, hagámoslo, o que nosotros queremos cambiar esto y la verdad es que queremos desburocratizar, pero a lo mejor desburocratizar es...

comunicar. Yo no sé cuántos son el pareto de los prestadores, de los que hoy hacen centroclasia, cuántos son. Cuánto esfuerzo nos demanda hacer una comunicación, es decir, el estimado colega... A partir de ahora, para la solicitud de una septuplastia, necesitamos que usted adjunte esto, esto, esto y esto, y justifique esto, esto y esto. Si no tiene ahí estos criterios, nosotros no lo vamos a poder auditar.

No sé, si me decís no, son 280.000 prestadores, nos va a llevar un año y bueno, pero... Pero también es a dónde queremos ir, yo entiendo que en el medio la realidad es esta, no la discuto. Y en esta realidad entiendo que tratamos de ser menos burocráticos porque sabemos que a la larga lo terminamos autorizando y no queremos friccionar con el socio, justamente estamos hablando de calidad de servicio y calidad médica.

Pero por ahí deberíamos decir, esta es nuestra situación actual y para mejorarla. Nosotros estamos haciendo un esfuerzo con estos proyectos tecnológicos para ir más rápido, para hacer todo. Pero del otro lado, quizás también tenemos que pedirle al prestador que esto, si vos querés comprar un medicamento tenés que hacer la receta y tenés que poner el diagnóstico, y si no pones el diagnóstico y no haces la receta, no te van a dar el medicamento.

Entonces, quizás nunca le dijimos tan bien qué es lo que tiene que presentar. Entonces, presentan lo que le pinta.

Martín, vos querías decir algo, perdón. No, no, parece la misma línea, Diego.

nosotros en cuanto a ¿Qué ponemos en la política de cobertura? O ¿Cuánto reflejan la realidad? Si querés eh que

Yo creo que con otra nos va a pasar exactamente lo mismo, me parece que lo que nos dimos cuenta es que nosotros tenemos que ponernos a, tenemos que tomar una decisión en realidad de qué es lo que queremos cubrir y qué no. y tenemos que decidir si vamos a tomar una definición diferente a la que venimos tomando en la práctica y vamos a asumir que vamos a tener una discrepancia con el pasado, justamente porque cambiamos la política.

O si vamos a ajustarnos a lo que pasó, en busca de esa concordancia. Pero con otra práctica, a ver si nos va a pasar lo mismo. Acá nos encontramos con un lugar en el que tenemos que tomar una decisión. o mantenemos lo que venimos haciendo en la práctica, y ahí sí apuntamos a tener ese 95% de concordancia con el pasado, o tomamos la definición de escribir una política más allá de lo que se venía haciendo y a partir de ahora definir qué queremos hacer.

y validar los resultados de la IA solamente con el nuevo criterio y no con el pasado. Creo que con otra prestación nos va a pasar lo mismo. Esto es diferente a lo que nos pasó antes, me parece.

está el asunto. Y coincido también con Pablo, perdón, me olvidé de eso, digo, quise hacer una oportunidad, eso sucede habitualmente cuando se estigmatizan este tipo de cosas, una oportunidad de darse vuelta y hablar con el prestado y decirle que unico, si no...

¿Cómo querés que te audite? No tenemos las herramientas para auditarte, convenceme. Hacer un esfuerzo por convencerme de que lo que estás pidiendo corresponde. Las sensaciones que no ponen cero esfuerzo en tratar de convencerme. Y es algo que requiere autorización. Entonces yo me lo planteaba como médico. Yo a veces me preocupaba de cuando pedía un estudio que el diagnóstico tuviera coherencia con el estudio que estuviera pidiendo para que no me lo rechazaran, digamos.

A lo mejor era demasiado tonto yo, pero no ponía solicito a un perfil reumatológico, ponía control clínico, ponía poliartritis, no sé. Trataba de poner algo que tuviera sentido. Yo siento que acá, y me pasa cuando audito, digo, estos tipos hacen el mínimo esfuerzo porque nosotros los... Digo, sí, sí.

Están diciendo que requiere autorización, quiere decir que alguien del otro lado lo va a ver. Es usar un poco la cabeza, digo. No sé, digo. Sí, sí, creo que sí que puede ser una buena oportunidad como para... para empezar a exigirles un poco más, sí, sin duda que sí. De la cantidad de prestadores, Pablo, sinceramente eso no...

El número no te lo podría dar yo, capaz que ahora hablando con los chicos de contrataciones nos tirarían más o menos la cartella de prestadores y hacerles un informe. Yo te preguntaba que por ahí vos tenías la percepción, aunque sea no el número exacto, pero son...

Si hay mucha variabilidad en el día a día o si más o menos ronda entre, por decirte algo, 50 prestadores, que son los que siempre hacen la centriplagia. Son cincuenta y más fácil, digo yo.

Sí, sí, sí. Hay obviamente una predominancia, pero pueden venir de todos lados, digamos. La mayoría son de Rosario, Buenos Aires, Córdoba, pero también... vienen del resto de las provincias, pero las predominantes son esas, obviamente, por tener mayor flujo de gente también.

Pero digamos, estaría bueno poder hacer algo así. El tema es que, viste, cuando vos iniciás un... un cambio, siempre del otro lado también puede haber algo de resistencia. Estará en nosotros tratar también de convencerlos de que nosotros para poder auditar si o si vamos a necesitar eso y si van a tener que terminar adecuado tarde o temprano.

Que no es mucho, ¿no? Es escribir tres palabras en un papel. Es escribir tres palabras, no le estamos pidiendo un gran esfuerzo. es un papelito con dos renglones, a paciente con una deformidad, con fracaso terapéutico, con obstrucción, con dificultad respiratoria.

Listo, si te dijera eso, vos no necesitás más nada, y la otra duda que tenía, que yo, por ahí esto es una pregunta más técnica, por muy tonta de mi parte, Pero entiendo que el modelo que nosotros estamos usando, tenemos que darle muchas instrucciones de lo que tiene que hacer, a diferencia de Gemini en común.

Porque si yo no te entendí mal, Max, el otro día cuando explicabas, era como que la gente nuestra, nosotros le vamos diciendo qué es lo que tiene que ir a mirar digamos, organizadamente, y el gémini común que utilizamos suele consultar a otros modelos, digamos.

No sé si sigue ahí la pregunta. Si la diferencia es que cuando usas Gemi en el chat usas un producto que es un agente que atrás está armado para hacer un montón de cosas. Acá en lo que hacemos nosotros la gente es. Vos usas Gemini como modelo, pero vos sos el responsable de construir todas las capacidades que puede tener, vos querés que el primero que piense que vaya que procese imágenes, todo lo que querés que haga lo tenés que construir, esa es la diferencia que esta gente no consume directamente lo mismo.

cuando vos escribís en el chat. Eso es lo que, si querés que haga lo mismo, te lleva a desarrollar como tu propio Gemini, no el modelo, sino el producto, se llevaría a eso, digamos. Acá, además, lo que tienen para ahí es que cuando vos... ¿Podrías hacer algo similar de esperar que sea más agéntico y que decida sobre la marcha todo lo que quiera hacer? Por ejemplo, que lo que hagamos luego en un momento de...

le das, armás un agente simple donde le das el pdf y todos los estudios y andá a evaluar, donde le das la responsabilidad libre de decir a cada vez qué va a hacer, distinto a lo que estamos haciendo que es como... un proceso un poco más ordenado, inteligente artificial, donde separamos etapas de primero identificar estudios, después los bienalizamos, después bienalizamos la política, y vas usando ya en distintos pedacitos, bien enfocados en lo que querés que sea.

Después el modelo de fondo, la inteligencia, es la misma o casi la misma Quizás, creo que cuando usan ustedes el Gemi creo que es el modelo, no sé 3.1 Pro quizás, y nosotros estamos usando el 2.5 por una cuestión de que no lo puedo usar mucho el 4.1 y el 3.1 no lo puedo usar mucho, además del costo que tiene, digamos, no...

No podría, pero igual el 2.5 es el que venimos usando en las otras POCs y funciona bien, pero bueno Esa es la única diferencia a nivel modelo Yo quería plantear algo respecto a lo que habían diciendo recién de si se van a hacer dos cosas, que una es automatizar el proceso, o buscar eso, más cambiar la política, digamos, en lo que se le pida a los médicos.

No sé si es en esta prestación en especialidad o más en general. Pensar que cuando se ponga eventualmente la gente, bajate en una etapa, primero un tsunami de rechazo todo o rechazo un montón, porque. no cumplí con los nuevos criterios. Quería preguntar si conviene pensar que el proceso, el proyecto primero se enfoque quizás en eso, en saber que si primero voy a cambiar las políticas y voy a tener muchos rechazos.

enfocar la evolución de la gente en cómo detectar y tratar esos rechazos quizás que se automatice porque digamos las respuestas de bueno si está faltando o que lo automatice 100%, que ya le deje, por ejemplo, a Gastón, él, che, esta gestión le falta este, este, este, que Gastón tenga que ir, con un voto sí se manda, porque mucho se lo va a derivar a Gastón, digamos, o a los auditores.

En lugar de enfocar a la gente en que sepa entender cuándo aprobar, si van a ser los menos casos, primero hacer el esfuerzo en que la gente entienda qué es lo que quiere rechazar. y ver cómo simplificarse el trabajo, porque si no al principio vas a tener una gente que sabe autorizar, pero va a autorizar el 5% porque todo el resto le van a faltar cosas y le va a caer todo a los auditores.

Entonces, como esa balanza se va a invertir en lo que es hoy, ver que el proyecto contemple, bueno, si voy a tener toda esa ola de... ya sean NRL o cualquier otra especialidad de rechazo, que la gente sepa él, bueno, cómo te ayudo a que los auditores no colapsen ahora llenos de cosas que rechaza la gente, y la gente ya diga, bueno, esto lo voy a rechazar porque...

y eventualmente que responda automático, si es que se puede y se quiere. Entonces los auditores solamente van a quedar con rechazos, pero no por documentación faltante, sino rechazos por... Porque la gente dijo, che, no, la política acá no la cubre y eventualmente la gente también podrá... Yo digo que no sé cómo va a ser ese tsunami que eventualmente pueda haber de...

cambiar las políticas y realmente ponerse estricto por lo que dicen, porque es lo que correspondería de justificarme lo que me estás pidiendo, ver que la gente primero ataque esa ola. Yo creo que acá primero es tomar una decisión, quizás esto sea un camino y lograr que autorice

la misma cantidad o una concordancia igual a la del auditor, va a tener por un lado soluciones tecnológicas y por otro lado de proceso o de relacionamiento con el prestador. Y quizás debemos asumir que eso va a ser parte del proceso y que todas las que caigan al auditor, porque no las pudo autorizar la IA,

Porque el problema fue que faltaba documentación, que el prestador será parte de la tarea del auditor de relacionarse con ese prestador y educarlo, que para la próxima... tenga que entregar la documentación necesaria. Creo que acá lo que nosotros tenemos que solucionar son cuestiones de que la IA no interprete bien si la información estaba.

A lo que voy es que había un resumen de historia clínica que decía que tenía una obstrucción nasal, que tenía dificultad respiratoria, que había fracasado el tratamiento y la IA no lo entendió, eso es lo que tenemos que solucionar acá. digamos porque la información estaba y no la interpretó bien, si la información no estaba y nosotros creemos que tiene que estar y tendremos que asumir que será parte del proceso también.

de empezar a mejorar nuestras auditorías y el relacionamiento con nuestros prestadores es uno de los objetivos. Porque uno de los objetivos es gestionar mejor el neodoque el auditor tenga más tiempo para relacionarse con los prestadores. y menos tiempo administrativo, y quizás sea un camino. Digo, todo esto nos trajo porque me parece que está bien que la política sea real a lo que el auditor utiliza.

Lo que no me parece que esté bien es que nosotros adaptemos la política a que los prestadores no nos den la documentación necesaria para poder auditar. Entonces digo, porque si no ya, ahí estamos cruzando una barrera. Me parece que flexibilizar está bien, digamos lo que vos decías Gastón la otra vez, ejemplo, que yo si tengo la imagen, si no me punto que para que haya un tratamiento, yo la autorizo igual, porque ya veo que la oposición está.

A mí me parece que es modificar la política. Ahora, si necesito que me diga que la obstrucción es severa o que tiene una dificultad respiratoria, ¿en algún lado me lo dice? Y le tendré que decir al espectador que necesito que me lo diga.

Me parece que la solución ahí no es cortar la política, porque ahí nos vamos a cruzar vamos a cruzar una línea y vamos a terminar rompiendo la política. Y después eso es todo nuestro, quizás no es de esta mesa en particular. Acá lo que tenemos que solucionar es si la guía lo ha hecho mal, lo interpretó mal o tomó una mala decisión con la información que estaba.

No sé, me parece que yo iría por ahí.

Y no me importa si al principio le sigue cayendo todo al auditor, porque en definitiva es lo que pasa hoy. Pero si le cae al auditor porque tenemos que educar a los prestadores, los educaremos. Si le cae al auditor porque la guía falló, tenemos que arreglar la guía.

No sé qué opinan, lo dejo abierto, digo.

A mí me parece que está bien, es una definición definitiva.

Bueno, perdón, pero se nos está por acabar el tiempo. Puede ser, hay que pensarlo. Esas definiciones estaría bueno que las piensen. y nos juntemos de vuelta y veamos qué hacemos. No sé si vale la pena correr de vuelta la gente con lo que se cambió o no sé Martín si querés cambiar las políticas de vuelta con los comentarios que han hecho ustedes y vemos a ver qué resultado nos da.

Yo y Marcos creo que lo que podríamos hacer es con la política nueva, que es más flexible, sin eliminar todo. Con la política nueva... Lo que tendríamos que hacer es buscar casos que tengan toda la documentación.

que tengan toda la información necesaria y correrla con eso, a ver que esté interpretando bien y que lea bien porque los casos que no tengan la documentación Lo va a rechazar y está muy bien que lo rechace, y el proceso va a ser que nosotros al prestador le vamos a tener que decir, señor, mire, la próxima, por favor, usted déme toda esta información y yo se lo voy a autorizar más rápido de lo que se lo autorice ahora.

Está bien, lo corremos de vuelta entonces, porque es lo mismo identificar los casos antes o que lo corra y la gente te lo va a probar, te va a probar esos casos que estén bien y te va a rechazar los otros. lo podemos correr de vuelta. Yo lo único que sí me gustaría dejarles para que piensen, por ahí Pablo y Fer, es si no hay casos, porque acá hay otra cosa que me hace un poco de ruido, que es todo lo que es más funcional o blando, por decirlo así, ¿no?

Vos decís... Bueno, que me pongan bien o que me escriban bien la historia que me toca. Qué sé yo, hay cosas que son, digo, corríjame acá, pero me suenan un poco más flexibles, como... Insuficiencia ventilatoria, ¿no? Y sí, qué sé yo, te está bien, yo te agrego que le cuesta respirar. Listo. ¿No hay datos que sean más duros, que podamos...? Porque me parece que ahí está el valor, en encontrar esos datos que sean duros y por ahí no aplica para este...

para esta práctica pero sí aplica para otras, porque la mayoría de los casos que veíamos, la tomografía, vos podés tomar ahí y decir listo, yo confío en el informe diagnóstico por imágenes, la gran mayoría decía leves, desviaciones leves. Entonces vos se lo rechazás y el te va a poner no tiene insuficiencia ventilatoria, no puede respirar bien. ¿Y qué te va a llegar? ¿Y eso nos sirve a nosotros para tomar una decisión? ¿O es un escape? Te entiendo Marcos, te entiendo y lamentablemente...

Hay cuestiones que son síntomas y que tenés que creer en que el médico no te está mintiendo. Digo, a ver, que te puede mentir, sí, te puede mentir. No, pero por eso digo, ahí yo ya no conozco todo el mundo de la auditoría, pero vos Pablo que lo tenés más claro, por ahí encontras otras prácticas donde digas, che, acá sí me puedo agarrar de datos que sean más o menos... Si vos me querés justificar una bomba de insulina por la habilidad...

por la habilidad, por gas y poluciones reiteradas, me lo podés decir pero te puedo pedir que me mandes los registros del glucosensor. digamos, ahora vivo acá en dificultad respiratoria en general, no, es una, una... no se traduce en una hipoxia, digamos. Entonces, no, corregime Gastón, pero tiene que ver más con una dificultad ventilatoria, pero no...

Sí, si no, no va a tener problema. Digamos, entonces es sintomatológica, entonces como es síntoma, y te puedo mentir.

Claro, por eso digo, por ahí en el mundo del Torino te pasa mucho, pero por ahí hay otras especialidades donde no te pasa tanto, no sé, o podés agarrarte de otros datos. No lo sé, lo estoy tirando para que lo pensemos.

Yo creo que nos vamos a encontrar mucho con esto, de que el médico va haciendo una justificación que puede no ser cierta. Nosotros, pero bueno, ya lo estás obligando a que te mientas.

Bueno, corremos de vuelta y vemos. en el compartido es la última sin las modificaciones de ahora.

Muchas gracias.

cuando lo volvemos a tener, el resultado con la próxima, con la nueva corrida.

Porque hay que buscar más casos, me imagino. Perdón, me tengo que ir a otra, eh. Dale, Martín.

▶ **20260521**

▶ **20260528**

[https://docs.google.com/document/d/1LqRO5aHfWHApZ7zk7slSY-Id-B37pGrflf5-oNO_NCg/edit?usp=drivesdk](https://docs.google.com/document/d/1LqRO5aHfWHApZ7zk7slSY-Id-B37pGrflf5-oNO_NCg/edit?usp=drivesdk)

▶ **20260603**

<!-- unknown block type: transcription (3742c02a...) -->



### Acción Items

- [ ] Ampliar la muestra de casos analizados, buscando más casos hacia atrás en el tiempo para aumentar la confianza en los resultados  
- [ ] Buscar y revisar los 7 casos que no se encontraron inicialmente debido al cambio de número de pedido  
- [ ] Martín actualizará el documento de conclusiones con los aprendizajes de esta reunión  
- [ ] Revisar el consumo promedio de tokens por caso para cálculos de costo del agente 
- [ ] Definir con Pablo y el equipo de políticas el enfoque a seguir: ajustar políticas a la realidad o mantener adherencia estricta  
### Contexto del Proceso de Autorización

- El autorizador valida si existe presupuesto antes de derivar al auditor 
- Cuando no hay presupuesto cargado, el caso se rechaza desde la parte administrativa 
- El control de si una práctica está convenida con el prestador debería ocurrir antes de la auditoría  
- En algunos casos excepcionales, el auditor médico puede cambiar la prestación, lo cual activa nuevas validaciones 
### Resultados de las Pruebas con Septumplastia

- Se analizaron 24 casos de septumplastia, de los cuales 16 eran solicitudes de la práctica sola  
- De los 16 casos solos, se encontraron 5 discrepancias: 2 estaban anulados y 3 no se encontraron en la web por cambio de número de pedido 
- El resto de los casos mostraron coincidencia entre el agente y los rechazos reales 
- Se identificó un caso atípico donde el auditor rechazó indicando que "la práctica no está convenida en el prestador"  
- El período analizado fue desde septiembre hacia atrás para encontrar volumen suficiente 
### Discrepancias entre Políticas y Práctica Real

- **Hallazgo principal**: El agente funciona correctamente según las políticas que se le proporcionan, pero existe una discrepancia entre las políticas escritas y la práctica real de auditoría  
- Las políticas de cobertura fueron diseñadas de forma más flexible, mientras que el agente las interpreta de manera estricta  
- Ejemplo: Una política puede requerir tomografía o resonancia, pero en la práctica los auditores humanos aceptan un informe que mencione obstrucción nasal 
- Al inicio del proyecto, el agente rechazaba el 90% de las solicitudes por adherirse estrictamente a las políticas  
### Limitaciones Técnicas Identificadas

- El agente no performa bien con imágenes y gráficos, se recomienda trabajar con prácticas que requieran únicamente documentación de texto 
- Las prácticas que se aprueban en el 95% o más de los casos deberían considerarse para autorización online en lugar de auditoría con IA  
- Ya se está trabajando en pasar prácticas con referencia 14 y baja tasa de rechazo a autorización online  
### Estructura de Políticas vs. Reglas de Auditoría

- **Debate clave**: ¿Se deben usar las políticas completas o solo las reglas específicas de auditoría?  
- El agente no consume toda la política de cobertura, solo utiliza los criterios explícitos de cobertura y exclusión  
- Las políticas incluyen justificaciones médicas y bibliografía que no son relevantes para la decisión del agente  
- Se plantea la posibilidad de crear una sección específica en las políticas para el auditor IA 
- Alternativa sugerida: Usar un motor de reglas estructurado en lugar de texto libre si solo se van a usar criterios específicos  
### Implicancias Operativas

- Adaptar el agente a las políticas actuales resultaría en un aumento significativo de rechazos y quejas  
- La política ahora se convierte en "la norma" y no solo en "una guía", lo cual cambia fundamentalmente su rol   
- Antes los auditores humanos aplicaban sentido común y flexibilidad, ahora el agente requiere instrucciones explícitas  
- Se necesita cambiar la forma de validar las políticas, no necesariamente la forma de crearlas 
### Criterios para Selección de Prácticas Futuras

- Considerar cuatro variables: volumen, tasa de rechazo, tipo de documentación requerida, y existencia de política validada  
- Priorizar prácticas que requieran resolución médica y no incluyan imágenes 
- Se está trabajando con prácticas de alto rechazo para tratarlas de manera diferente  
- Disponibilidad de información sobre todas las prácticas por pareto para seleccionar las más adecuadas 
### Conclusiones de la POC

- **Técnicamente exitosa**: El agente cumple correctamente con las políticas que se le proporcionan  
- **Operativamente problemática**: No refleja la práctica actual de auditoría  
- La herramienta funciona bien cuando está "bien alimentada" con políticas validadas  
- Se confirma que las políticas necesitan ser reformuladas para este uso específico  
- Es necesario decidir si ajustar la realidad a las políticas o las políticas a la realidad  
### Próximos Pasos Estratégicos

- Ampliar la muestra de casos para confirmar los resultados con mayor confianza   
- Llevar la discusión sobre el enfoque de políticas a Pablo y otros decisores clave  
- Definir si se usarán políticas completas, reglas de auditoría específicas, o una combinación  
- Documentar las conclusiones en el archivo compartido por Patri  
- Esta discusión debe ir en paralelo con la ampliación de casos 






Bueno, todo el autorizador, ¿no Macu? Viste que se me mezcla cual. Pero es a nivel sistémico, digamos. Pero es el autorizador, lo que pasa es que el autorizador no... no le dice, tenés un presupuesto o tenés que pedir un presupuesto, me parece que eso es antes, Iba. Claro, cuando se carga, es así, cuando se carga, si es que hay un presupuesto, se carga que es un presupuesto, eso mira la regla y le deriva al auditor para que después vaya a contrata, digamos.

Si no tiene un presupuesto, eso se rechaza, o sea, si no está cargado, se rechaza. De la parte administrativa. Exacto. El punto es, yo tengo un caso, quizás es un caso. puntual, de un error, que se destapó y me llamó, o pasó algo... Lo que pasa es que si tenés dos prácticas, a lo mejor una no está convenida y la otra sí, por eso la recibiste también, ¿no? No, no, no, esta estaba sola. Ah, ok, ok. Esta estaba sola. Y está, el caso rechazado, con el motivo de rechazo, la práctica no está convenida en el prestador.

Entonces por eso me hizo ruido, porque no sé si existe esa... posibilidad de que eso suceda o no, si no debería, no debería, no, ok, perdón para ubicarme en estos casos. donde haces este control de si está contratado o no, entiendo que es cuando conoces al efector, en este caso entiendo que lo conoces, pero entiendo que no en todas las autorizaciones conoces quién es el efector. Vos generás un F4 que es para...

cuando hayas hablado con quien te guste, que ahí entiendo que lo más común no es conocerlo, entonces sí sería fuera de las reglas de esta gente. Y yo te miro la parte de auditoría. Después sí está el espector porque, no sé, por el tipo de práctica o porque está cargado y se quiere incorporar al proceso un...

dáselo al autorizador, que entiende que igual debería haber ocurrido antes, es algo que ahora el auditor lo controle. control contra el autorizador, que al de carga no, porque no supo quién era el inspector o... Por eso mismo, la pregunta iba justamente ahí, a si el auditor tenía que hacer el control o no, porque en este caso, en este ejemplo que nosotros vimos, el auditor rechazó indicando que la práctica no estaba convenida para el prestador.

pasó auditoría y auditoría dijo eso entonces mi pregunta era eso es una práctica habitual o es un caso que se escapó por error y punto por lo que yo entiendo es un caso que se escapó por error y punto porque porque debería funcionar como decís vos se analiza antes de que pase auditoría si eso es así no me preocuparía

pero mi pregunta iba justamente a calculo que sí o lo mismo que el de carga en este caso que el de carga haya cargado otro código y fue el auditor dijo no lo que está pidiendo es esto y ahí recibo el código real puede ser el motor valió de esta no lo tenés la otra que valió el de carga ante sí está no

Pero entiendo que sí debería ser, lo menos en general, no sé en el autorribo si ocurre o no, pero entiendo que a nivel autoresor general no debería ser lo más común.

Pero si cambia la prestación el médico, en ese momento se debería validar de vuelta, digamos. Sí, pero ahí está bien que lo haga el auditor médico, no me preocupa, porque ya no estamos en distancia de auditoría. estamos en instancia de auditor humano. Si alguien lo está cambiando, porque ya pasó esa instancia, el auditor ya dijo, no lo puedo resolver, lo derivó el humano, y el humano está manipulando el caso, reemplazarlo y demás. Ok, se puede dar en cualquiera de los dos escenarios.

Ese era el único que a mí por lo menos me hacía ruido, porque no entendía eso. En el resto me parece que hay coincidencia. Podemos llegar a ser... Había unos cuantos que habíamos marcado que no aparecían.

Pero el tema es que vamos a necesitar algún otro dato para poder buscarlo.

Pero bueno, yo creo que puedo buscarlos, ahora que entiendo esto que pasó. Uno, dos, tres, cuatro, cinco, seis, son siete casos que nosotros no encontrábamos. Aparentemente tienen otro. Otro número de pedido.

Esos son los casos que tenemos que revisar de nuevo.

Lo que no tuvimos entonces, estoy interpretando, son los casos que habíamos dicho que son los rechazos firmes, ¿no? Para comparar.

rechazo firmes de solo sento que son como se piden muy pocas veces solo y muy pocas veces de rechazo entonces yo desde ahora O de cualquier otra prestación, como habíamos charlado sobre la posibilidad de buscar otra prestación. que por ahí sea más representativa para lo que eran los rechazos Pero entiendo Marcos que esto que recién comentaba Fer, que eran justamente los rechazos Claro

Sí, pero son muy pocos casos, ¿no? ¿Cuántos casos eran?

Si no, bueno, probaremos con eso si nos...

Gracias.

acá tenemos

24 casos. Entiendo que los que figuran abajo que dice SEPTUM solas, están incluidas en los de arriba, Maxi, ¿no? Sí, puede haber, porque los de arriba podían tener 1, 2, 3, 4 felicitaciones, puede haber uno repetido, pero hay muy pocos. De septiembre hasta ahora hay muy pocos.

Y ahí, escuchando lo que decían recién, buscar otra prestación o sumar centum y que la gente agarre las que tienen uno, dos, tres, ocho, y por el otro lado que Gastón las audite Ignorando el resto de las que están, como entiendo que es lo que hicieron, es agarrar, si querés, cien gestiones de septumplastia, que la gente dé el resultado, ignorar lo que dice Cypher.

y revisarla, auditarla una por una, a ver si coincide o no. ¿Qué es lo que hicimos con esas 24? perdón es lo que hicimos con las que de esas 24 el auditor lo dijo provado en realidad que son menos

Ustedes lo que dicen es subir ese número a 100, buscar 100 casos.

o no entendí lo que planteaban y la cantidad no sé hay que definir la cantidad acá entiendo que es un poco más complejo digamos pues no sé qué tanto tiempo le lleva a evitar digamos si lo vamos a matar a Gastón, porque hubiste 100 sentumplastias o no, digamos. El otro, si ya tomabas el estado de Salesforce, tenías un termómetro un poco más afilado y bueno, los dos los rechazó.

lo dejabas de lado, acá vas a tener que revisar todo.

Pero bueno, eso, como quieran. O, repito, como decía antes, tomar otra prestación, siguen otra prestación, otra política, donde sí haya más. casos de la prestación, que se pide sola y está rechazado y hay volumen, no que sea frecuentemente pedida con otra cosa, porque nos va a pasar lo mismo que si la gente no conoce esas 1, 2, 3 políticas y no las aplica todas juntas.

No te lo va a resolver, digamos. Por lo que veo acá, ¿desde cuándo estabas tomando casos? ¿Desde septiembre dijiste? Creo que me fui a este septiembre para encontrar volumen, porque creo que aprobé este año desde enero y fue la primera tanda que no sé si encontré diez y para buscar un poco más, creo que me fui a este septiembre arbitrariamente.

y para atrás a ver qué he encontrado. ¿Tomemos casos de la Septim Sotra? Hay 16 ahí. Yo veo que hay 24 casos y 16 están solas. No sé si es el mismo plazo del analizado. Hay 16 casos dentro de la lista de septum zona. Si hay un número objetivo que ustedes plantean, que puede ser 100 o el que ustedes digan, vamos a buscar eso. Si nosotros buscamos eso...

Ahí sí ya tenemos la remisión de 100 casos, pero tenemos que auditar solamente donde haya discrepancias, donde estén aprobados en vez de rechazados.

Porque ahí la diferencia de estado sí ya puede tener que ver con... con otra cosa. Rico.

Sí.

Pero nombraste a Nico, no sé quién es Nico. Bueno, no, Nico. No, sí, sí, se entendía lo que... ¡Ah, boludo! Yo estaba esperando que hablara Nico. No, no veo ninguno. De esos 16, lo que vimos es que había 5 casos que tenían discrepancias. de los cuales 2 estaban anulados y 3 no los encontrábamos en la web por ese tema de cambio de número de pedido.

Y después el resto habían dado todo, el mismo rechazo.

Si tenemos esa muestra, me pongo a buscar casos. Si consideramos que la muestra es suficiente, ya está chicos. O sea, la idea era probar y ver cómo respondía. La vez pasada habíamos hablado que... que la muestra sea significativa como para tener cierta certeza, habíamos dicho Che sobre lo que se estaba probando se acercaba mucho y dijimos

que los que habían dado por rechazados no preocupaba tanto porque los tenía que ver un ser humano Acá el problema era al revés Bueno, pero si con esa cantidad de casos que vimos estamos bien Yo entendí como que había muy pocos casos Por eso en su momento sugerí otra práctica, pero si probaron con la misma y la cantidad de casos que tenemos y estamos de acuerdo, estamos ok y avanzamos con eso.

A mi me parece poco, agrandemoslo, agrandemoslo, vayamos mas atrás, lo que si, en la medida de lo posible, busquemos ser punzola.

¿Es posible el más atrás? El tema es que no se mezclen con los casos de rechazo, que igual tampoco es que estaría mal, pero los casos de rechazo que eran por falta de documentación. ¿Tienen que ser rechazos firmes? No, no, no. Cualquier rechazo. Cualquier rechazo en la instancia de auditoría. Para revisar si la norma está funcionando bien. Claro. Si justamente hoy debería ser hasta el único motivo de rechazo.

o casi el único, porque en realidad no te dice, no te lo apruebo porque la documentación que vos me diste tiene un parámetro que contradice la política. Lo que te dice es, no hay documentación que acompañe. y lo que dice la política en todos los casos. O sea, que más o menos lo mismo.

Bueno, si podemos agrandar la muestra, agrandémosla. Igual, nada, podemos ir dando por cerrado este proceso. La idea era probar, a ver si se acercaba a los valores que pretendíamos. Entendemos que sí. Por otro lado se está avanzando con la adquisición de la herramienta para la construcción de los agentes

con el proyecto de manera formal.

Bueno, y concluimos que sí. Me parece que concluimos que sí con un montón de peros. Pero con un montón de peros. Si bien más lejos es, che, y perdón que insista con esto, tenemos que reconstruir todo el andamiaje de políticas de cobertura para que, si vamos a dárselas de comer a la herramienta, funcionen según lo que la realidad de auditoría, no en terreno, digo, la auditoría real funcione y no según lo que dicen las políticas de cobertura.

artura. Digo, me pararía un segundo y preguntaría de vuelta, che, ¿queremos hacer todo eso? Si la respuesta es sí, sigamos para adelante. Si no, pensemos alguna alternativa. Digo, así como está esta herramienta, más allá del problema ADN, digo que entiendo lo que dice Max y dale, Maxi, tranqui.

Y demás. yo creo que si ponemos esto a andar en el mundo real hoy, hoy así con la información que tenemos hoy, anda como el ojete, digamos, pero por este tema de que tenemos las políticas de cobertura pensadas de otra manera, digamos, y adaptarlas no, como se llama, no es inmediato eventualmente si el camino es adaptarlas, nos va a llevar tiempo, de hecho nos llevó un par de semanas, hacerlo sobre dos políticas de cobertura, entonces digo yo

digo no no no no no digo no sigamos avanzando ni nada es che tengamos claro cuáles son los pelos de seguir avanzando y que el resultado de este no sé cómo le dicen pop piloto etcétera fue che sí pero todo esto En ese plan, digo, Marquitos, no sé si estás de acuerdo. Sí, estoy de acuerdo. Entendí que esas discusiones se estaban dando en paralelo. No sé si se dieron al final o no, si definirán algo. No sé, Fer o Gas, si tuvieron alguna otra... Diendo que no, el punto es que...

Me parece que es parte del resultado, justamente, de la POP, es, en función de la política que nosotros subimos, el agente funciona, porque no hemos encontrado una discrepancia entre el resultado del agente y la política. Lo que hemos encontrado es una discrepancia entre la realidad y la política.

Y tenemos que definir si nos vamos a ajustar más a la realidad, más a la política, o vamos a buscar un punto intermedio. Pero me parece que ese es un buen resultado de la POP. No quiere decir que nosotros podamos salir con esto mañana para nada, porque no era la intención, es el resultado de la poca ejercicio. Tenemos la confianza de que tenemos una herramienta que, bien alimentada, con una política validada por todos, funciona.

Ahora, ¿qué política vamos a tener? La primera que nos instruimos, la última que nosotros ajustamos, vamos a ir al medio. Pero me parece que esa es ya una decisión mucho más blanda de negocio. va más allá de lo que es la POC en sí misma, es una de las con grandes conclusiones. ¿Qué quiero decir? Coincido con vos Martín, hay que dar esa discusión ahora. No creo que invalide el resultado de la POC, sino que justamente...

va marcando el camino de todo el trabajo que tenemos que hacer para que esto funcione. Con la tranquilidad de que el agente cumple con la política. Totalmente, entonces digo, coincido plenamente, yo diría, técnicamente la POC fue muy exitosa, fue excelente, operativamente es una porquería, digo, porque no es lo que vamos a usar.

Claro, sí. Bien, perfecto. Pero no era el objetivo de la POC, digo, no era el objetivo de la POC. Yo creo que hay que analizar eso, digamos, si yo me tengo que adaptar a las políticas nuevas obviamente me adapto, desflexibilizo la humanización o la vista humana de la auditoría, cero problemas, el tema que eso va a traer...

justamente lo que no se está buscando, poner mucha más traba a los afiliados para autorizarles una práctica, ¿me entiendes? lo lleva más al terreno de lo cotidiano y no tanto de lo bibliográfico porque si no, obviamente... Vamos ahora al 15% de disconformidad, como dice Pablo siempre, lo vamos a duplicar o lo vamos a triplicar porque le vamos a poner traba por todos lados

a todos los afiliados y en muchas de las prácticas que son muy frecuentemente requeridas. Creo que estamos diciendo todo más o menos lo mismo. Desde el punto de vista del proyecto en general, lo que hay que discutir es esto que decía Ferrante, qué carajo vamos a hacer con esto. Cambiamos la política, nos bancamos lo que decía Gass de tener peores quejas que las que tenemos hoy.

Ahí va la discusión y me parece que no somos nosotros los que la vamos a terminar de dar. Creo que acá, perdón, a lo mejor me meto en un terreno que no me toca, Martín, es más tuyo, pero creo que un buen resultado o un buen entregable de la POC puede llegar a ser algún tipo de estructura, que a lo mejor no es política, a lo mejor es una estructura de órdenes relacionadas a la política para que funcione la gente.

porque, en definitiva, entiendo yo, no está Manzi, pero los últimos ajustes fueron no autoricen la política, díganme qué quieren, cuál es el criterio de aprobación y el criterio de rechazo, yo los configuro acá y esto funciona así. Y lo mejor es eso. Sí, pero ahí le está sumando el factor a la IA que tenés que después administrar. Sí, sí, sí, sí. Si sos explícito y tenés una sección explícita donde dije cuáles son los criterios de cobertura, que de hecho la mayoría de las políticas lo tienen, el tema es que...

deberías ajustar todo eso a lo que termina realmente pasando en la realidad digo y pongo como ejemplo si querés dos segundos la política no me acuerdo de qué era la política la primera no sé si la deceptum plastia que decía che mira tiene que tener una tomografía o una resonancia o tal o tal otra cosa y qué sé yo y después resulta que cuando el auditor humano miraba eso decía bueno si tiene un informe que en algún lugar dice que más o menos tiene un inicio en directoría le damos para adelante tiene que decir la política

Exactamente. Esa es la conclusión que yo tengo de la POC. Todas las políticas, digo, las políticas no se empezaron a armar para la auditoría. Las políticas se iban armando desde antes, probablemente de que Marquitos y yo estuviéramos acá. Están armadas de esa otra manera.

Y las nuevas, porque de hecho todas son políticas nuevas, están armadas de la misma manera. Entonces, o cambiamos la forma de hacer las políticas, y de hecho hay un cacho de la política que dice ¿Cuáles son los criterios explícitos de cobertura y de exclusión?

y son estos, o reflejamos ahí la realidad o como decía Gastón, le hacemos caso a lo que dicen las políticas y damos para adelante, qué sé yo. Yo creo que... No tenemos que cambiar la forma en la cual hacemos las políticas, tenemos que cambiar la forma en la cual validamos las políticas. Si yo valide que... Si nosotros vamos a decir, tiene que estar el informe del ataque, tiene que estar el informe del ataque, no tiene que haber un texto en el pedido médico.

Si nosotros necesitamos que esté el texto en la política, tenemos que validar que diga que tiene que haber un texto en cualquier lado que diga eso. Me parece que va por ahí. La estructura del camino, no es el mismo. Este es un caso en particular, esto es una cirugía, estas imágenes que tienen que estar asociadas para que esa cirugía pueda ser comprobable, que esa patología exista. O sea, hay medio mundo ahí de las políticas, de qué podés pedir o no en una cobertura y demás.

montón de peros o de considerandos cuando uno plantea la política. Pero de vuelta, insisto, digo, coincido con vos, Fer, La POC fue exitosa, si le das de comer adecuadamente, va a comportarse adecuadamente. Si le das de comer mal, se va a comportar mal. Punto, digamos, esa es la conclusión, me parece a mí. Ahora hay que ponerse de acuerdo en qué le vamos a comer.

Pero eso es una discusión que no tiene que ver con esto.

No sé si están de acuerdo. Fui medio brevemente. ¿Esto es así? No sé si es así. Se entendió, se entendió. Perfecto. Como decís vos, estamos diciendo lo mismo en realidad. Sí, sí, sí. Tenemos que asegurarnos de que la discusión se va a dar, chicos. Porque si no...

La podemos poner como condición para que esto eventualmente se implemente. No, hay que explicitarlo también en la devolución que hay que hacer de la POC. O sea, tiene que estar explicitado ahí para que tengan esa discusión. Si no... Sí, esa era mi intención con mi comentario. Y es complejo, además, lo que estaba diciendo Gastón, por un lado decimos, bueno, dale, acerquemosnos a las políticas que tenemos hoy. Está bien, acercarnos implica lo que pasó con el agente al principio, rechazó el 90% de la...

de las prestaciones que se habían pedido, estoy seguro que eso nos incendia todas las caras claro, pero eso insisto, no habla en sí mismo, habla de que hemos validado lo mejor una política que restringe el 90% de los casos, o sea, tenemos que cambiar la forma, nos vamos dando cuenta que la política que quizás hasta este momento era una guía y algo, una forma de consulta, ahora es la regla, la norma, y si se cumple o no se cumple, y no existe lo que dicen acá.

Entonces, nos cambia la forma en la cual vemos las políticas también. Yo les agrego que desde el lado técnico, después tengo que mirar cuántos tokens en promedio estábamos consumiendo por caso, porque es un dato que me interesa para hacer cálculos promedio de lo que cuesta el agente. Después, lo que sí les dejo como mensaje es…

Sabíamos que para imágenes, que era lo que suponíamos, pero bueno, está confirmado que para imágenes y para gráficos no performa bien, hay que ir por otro tipo de prácticas que a veces sean únicamente de texto, en esos casos performa bastante bien Y lo otro que iba a decir, y se me olvidó recién, bueno, ya estoy sin mi acuerdo

El otro que iba a decir es, también por ahí podemos sistematizar la forma de decidir Si esta práctica o las que sean, en algún punto no se tienen que ir hacia la autorización online o a otro tipo de autorización ¿Por qué vamos a poner un agente de inteligencia artificial para que apruebe lo que ya hoy se aprueba en el 99% de los casos, digamos? Y esa charla, no sé si la tuvimos, pero creo que este caso nos reflejó un poco eso, ¿no? Es como que estamos aprobando todo, ¿por qué...?

¿Por qué vamos a ponerle más tecnología a algo que hoy ya tenemos una solución? No entiendo que tenemos una solución para eso. Sí, Martín. No, te iba a decir, ese proceso está corriendo en paralelo, digamos, con... algunas prestaciones, quizás todavía no llegamos a esta, pero si estamos viendo justamente todas aquellas prestaciones que tienen referencia 14 y que tienen una tasa de rechazo muy baja, tratar de pasarlas online. De hecho venimos pasando como 50 prestaciones.

Sí, hoy pasaron varias. Sí, tal cual. Entonces, ¿qué es lo que está pasando, Marquitos? Quedate tranquilo, está corriendo. Por otro lado, quizás no atacamos justo a esta, porque no se dio por el pareto, pero sí está pasando. Estamos detrás de ese tema. Bueno, genial. Buenísimo, porque también eso nos va a marcar la hora cuando nosotros empezamos a trabajar y elijamos qué prácticas vamos a pasarle al auditor.

Por ahí hay que poner un número y fijarse, che, de esta práctica, no sé, un umbral. 95% se aprueba. autorizarse ya fue o más, no sé, yo no sé bien cuál sería un número lógico, pero si hay otras que se rechazan mucho más y eso se justifica, por ahí esas son las donde haya que atacarlas más rápido de la gente.

En esa línea también estamos trabajando con la otra punta, digamos, y viendo las que se rechazan muchísimo, digamos. digamos si lo sea y yo no parezco alguien. Estamos trabajando con la otra punta, con las que se rechaza mucho, para ver si hay que tratarlas de otra manera ¿viste?

Pero sí, en esa línea se está laburando, de vuelta, por un pareto, capaz que llegamos acá después de 10 años. Pero tengo toda esa info, si querés, la podemos poner a disposición para decir, che, mira, ataquémoslas del medio, no sé, por decir algo, la lógica que planteemos, pensemos en esas del medio y que tengan políticas de cobertura ya generadas, si no tenemos que generar una nueva, a ver qué onda, o revisar esas políticas de cobertura.

el resultado de la POC, es decir, bueno, mirá, en vistas de que nos pasa esto, esto, esto y lo otro y que eventualmente vamos a tener que tocar las políticas de cobertura y que necesitamos hacer un piloto con que el resultado de la POC sea, hagamos una nueva POC con un caso mejor, no sé, algo por el estilo.

Yo les sumaría todo eso que dijeron como la cuarta variable de análisis. Es el tipo de documentación. que requiere esa prestación de agua, que es la otra limitante que tenemos con el agente. Básicamente sería ver si la prestación mantiene o no la resolución médica, establecer el volumen de esa prestación.

si vamos a mantener la que sea de resolución médica, establecer la política y después si esa política establece que las documentaciones no son imágenes Sería potable de que vaya con un agente y haga esa prestación, digamos.

Una aclaración por las dudas. Para este proyecto, la verdad es que no hace falta la política por cómo la conciben hoy. Lo vuelvo a decir porque creo que Fer lo había dicho, pero es más una cuestión de órdenes, de reglas que hay que darle a la gente, porque las políticas son...

mucho más complejas, tienen toda la justificación del por qué desde la perspectiva médica, de negocio, de todo eso, la verdad que hoy no lo está usando la gente, porque no es información que le vaya a cambiar Está bien, pero esa información no está en otro lado hoy, teóricamente. No, ya sé, pero si vamos a elegir tres prácticas, ponele, mañana agarrás y decís estas tres prácticas me parece que van bien. No tiene ni gráficos ni nada, listo, se lo limpiamos, tiene un volumen bastante alto y hay bastante rechazo.

No sé, ponele, elegiste esos criterios para elegir tres prácticas. Las tenés a las tres prácticas, pero no tenés las políticas de cobertura, lo que voy es no hace falta entregar una política de cobertura completa con diez hojas, porque lo que nosotros agarramos de la política de cobertura para que la gente tome decisiones fue la parte que decía, estos son los documentos que se requieren, y esto es lo que tenés que mirar, estos son los criterios que hacen que las tengas que rechazar, estos son los que hacen...

que lo apruebes. Y chao. Está bien, ahí tengo dos comentarios. Si esto es exactamente así, digamos yo entendí que la idea era justamente utilizar las políticas de cobertura como input. para el auditor de AI para que hiciera las veces de auditor humano y que eventualmente interpretando las políticas de cobertura de la forma que sea

dijiste vos, actúe lo más parecido posible un editor humano. Ese creo que era como el origen del asunto. Después está lo que decís vos de decir, mira en realidad estrictamente, sea porque nosotros le estamos diciendo que lo haga, sea porque en la caja negra terminamos dándonos cuenta que hace eso o lo que fuera, termino utilizando un pedacito chiquitito de la política.

Si es porque nosotros le decimos que lo haga, ahí me pregunto, che, ¿necesitamos hacer una herramienta de inteligencia artificial o simplemente un sistema de reglas tipo motor cerrado y se termina la discusión? Porque si voy a usar solamente estas cuatro pavadas de la política, agarro esas cuatro pavadas de la política, las estructuro y las meto dentro de una base de datos y fíjate si cumple con esta regla o no cumple con estas reglas.

Me saco de encima el tema de la IA y de la automatización y toda esa historia, digo que pierdo un poquito si Y tercero es, si no estamos haciendo esto explícitamente adentro del automatizador, o sea, que le estamos dando la política completa y la está ingiriendo, yo no sé si todo lo que está alrededor de esos criterios está o no influyendo en la toma de decisión.

Aparentemente no por los resultados, pero la verdad es que no lo sé porque termina siendo medio caja negra también, viste, la herramienta. Eso es, digamos, nada más. Si no vamos a usar las políticas, usemoslas. Si no vamos a usar las políticas, usemos otra cosa capaz, capaz que no es el camino de ir por acá.

Digo, en la línea de esto que decías vos, ¿no? Digo, decir, che, mira, si encuentro tres que me van pero no tienen política de cobertura, les armo así medio ad hoc una serie de reglas. No digo que esté mal, digo, eso no es lo que habíamos planteado al principio y quizás sea la evolución de eso que habíamos planteado al principio, ¿no?

El agente nunca consumió directamente las políticas de cobertura. Que nosotros le hayamos puesto las políticas de cobertura no quería decir que la gente esté haciendo uso a la hora de pasárselo al LLM para que haga el procesamiento del caso. No estaba haciendo uso de todo.

¿Por qué? Porque cuando vimos las políticas, tenía un montón de información que justificaban el por qué las políticas eran así y eso no le cambia nada, digamos. Pero bueno, No parece ser un problema, lo comenté simplemente por una cuestión metodológica.

no parece ser el problema de eso claramente. Por eso lo decía, por una cuestión de lo que implica por ahí construir formalmente toda la política, nada más. A eso me refería, como que no trabajen. Desconozco qué tiempo les lleva el esfuerzo, pero digo, si hoy más o menos tienen ciertas reglas de finidad, no trabajen la política completa, que seguro les lleva más tiempo.

Justificar, no sé, ir a buscar la bibliografía, justificar, poner números, no sé, bla, bla, bla Lo que vi que tenían las políticas Porque a la gente lo que le interesa son las reglas, al final que usted le hayan puesto en texto libre En vez de que sea estructurado como puede ser un motor de reglas como estabas diciendo vos recién, Martín

O sea, lo que entiendo es que la política tal como la escribieron no es necesaria así de completa para la gente, lo que necesitaríamos sería únicamente las reglas.

estoy diciendo lo que la gente necesita. Nosotros necesitamos que la política esté completa, es otra cosa, ¿sí? Sí, sí, pero es tricky lo que está diciendo Soledad. Lo mismo estoy diciendo yo. O sea, o ponemos las políticas o no ponemos las políticas. Digamos, usamos otra cosa. Esa otra cosa es una parte de las políticas, como decía vos, Marquitos, de la parte de criterios y qué sé yo, que está todo fenómeno, pero eso implica entrar en la política.

Si no, tenemos que dedicarnos a escribir criterios de auditoría, que es otra discusión. Quizás tengamos que dedicarnos a escribir criterios de auditoría, no lo sé. Pero de vuelta, insisto, no es una discusión que quizás podamos dilucidar nosotros desde nuestro

tenga que meter el pancito Pablo y otras personas, digamos, para definir para qué hacemos. Yo soy responsable del área que hace las políticas, pero yo no afino qué política se hace y por qué necesitamos políticas. Yo hago políticas, digamos, a lo sumo, consensúe, digo, che, ¿cómo querés la política?

Si es A, ¿cuáles querés primero? ¿Cuáles querés después? Pero el que dice qué políticas se tienen que hacer y por qué tenemos que hacer políticas es Pablo, bueno, Pablo por ser el gerente médico, yo construyo información para la gerencia médica. digamos, si Gerencia Médica me dice, no, pará, loco, no la hagamos más así, hagamos las asadas, las hacemos asadas, no hay ningún problema, obviamente, pero esa discusión, como decía Fer, es la que hay que dar, es decir, che, ¿cómo queremos hacer esto?

Y que no es que salta por el auditor AI. Lo venimos discutiendo hace un montón, pero no venimos, digo, Fer es testigo y Gastón también. Digo, lo venimos discutiendo hace un montón, pero no habíamos llegado, o mejor dicho, habíamos llegado a este modelo, que era el mejor modelo que teníamos hasta ahora.

Quizás no sea mejor para este Figma. Veamos, qué onda. Digamos, es agregarle unas secciones, hacer solo esto, no lo sé, no sé cuál es la mejor opción. Eso que dijiste está bueno y ahí le dejo la tarea a Fer de última. que no se sumó. No, pero digo, vos dijiste algo recién, que es, para este fin, para el fin de la gente, por lo menos al momento, no necesitamos políticas de cobertura. Si querés poner otro nombre, necesitamos una parte de la política de cobertura, que es la que usamos para darle las reglas de vuelta a la gente y que actúe en función de eso.

Ahora, necesitan las políticas de cobertura por otro motivo, porque ustedes cuando piensan esas reglas necesitan justificarlo, No sé, eso se lo dejo a ustedes que lo definan, desconozco la verdad. No, eso es una consecuencia. Si vos le digas explícitamente, che mirá, si está esto tenés que hacer esto, si está esto otro, haz esto otro. Y con eso trabaja.

No es que la justificación después de si el costo es alto o bajo, eso no le cambia nada.

Ok, me parece que hay que llevar esta discusión a, esta discusión más blanda que decía Fer, digo, con Pablo y no sé quién sea, y tratar de pensar esto, y que la respuesta de, como decías vos Marquitos, digo, de la POC, nos fue muy bien, tuvimos este inconveniente, no sabemos cómo resolverlo o tenemos otras sugerencias, tenemos que discutir.

Yo creo que lo único que agregaría a todo lo que dijeron que coincidió al 100% es, como punto número uno, seguro que me voy a olvidar de todo, voy a empezar por el uno. Si podemos ampliar la cantidad de casos procesados, como decíamos recién, aunque tengamos que ir un poco más atrás, para poder medir exactamente el ajuste del resultado.

A la política, no a la realidad. Bueno, ahora estamos muy cerca, igual por cómo lo vemos medio manipulado. Me parece que va a estar bueno. Y evidentemente el punto 2 me lo olvidé. Pero primero yo subiría esa cantidad, me parece que eso es importante. Eso es una decisión de todos y es para quedarnos tranquilos de que por lo menos lo que probamos, que era el punto de la prueba de concepto...

nos cierra, eso era, si entre todos decidimos que igual no lo queremos hacer, podemos no hacerlo, nada más, es una cuestión de riesgos después Che, mirá, estos casos que identificaste, los probaste, hoy la respuesta es ni, probamos algunos Si podemos aumentar la muestra, quedamos un poco más tranquilos, mejor, si no...

Sí, me parece que sí, porque en los términos en los que estamos hablando es el agente funciona bien en relación a cómo lo alimentamos, lo que decías vos Martín, lo que nos queda es... de definir cómo vamos a alimentarlo. Para poder confirmar la primera parte, de que la gente funciona bien según cómo lo alimentamos, me parece que lo único que nos falta es agregar un poco más de volumen. En los casos que vimos, no es demasiado grande, vimos que sí, funciona muy bien en relación a cómo lo alimentamos.

Si podemos agrandar ese número, nos vamos a quedar más tranquilos todavía. y va a confirmar más todavía que la parte más importante está en el punto número dos, que es, definamos cómo lo vamos a alimentar, y tengamos esa discusión y todo lo que hablamos recién. Entonces, yo haría eso, y me parece que con eso tenemos todas las conclusiones necesarias para definir cómo vamos a seguir.

Bueno, vimos un corrancia en el sí, vimos un corrancia en el no, vimos en funcional lo que nosotros definimos que lo vamos a alimentar.

Sí, sí, estaría bueno eso, y después también, como decías vos, definir bien si vamos, como dice Martín también, si vamos a usar la política estrictamente política... y yo me adapto, o sea, me establezco por detrás de la de la política, la uso como escudo y punto pero ahí van los rechazos, van a venir a la orden del diálogo. Depende de lo que diga la política, por eso la discusión es qué le vamos a escribir a la política lo que es seguro es que la gente va a funcionar como diga la política, la política o las órdenes o lo que sea nosotros partimos de la hipótesis

que la auditoría en la realidad funcionaba ajustada 100% a la política. El resultado de la POC es que no. Y a partir de ahí, tenemos que ver para dónde salimos.

Darío.

No, esto de que no me termina de quedar claro, o sea, entiendo la necesidad de ampliar la muestra por un tema de mayor seguridad. Pero esta discusión que estamos teniendo con respecto a la política, digamos, estaría bueno que ya la vayamos viendo porque puede ir en paralelo tranquilamente.

Y también esto de, bueno, ¿cuál es el objetivo de las políticas? Porque por algo se puso para que la IA interprete y por algo el auditor es su guía y demás, digamos. también establecer eso. El objetivo de las políticas es que los auditores utilicen las políticas para tomar decisiones coherentes entre ellos y homogeneizadas. Ese es el objetivo de las políticas.

Y dos cosas, creo que me acordé del segundo punto, no solamente eso. Acá lo que estamos viendo es si vamos a alimentar el auditor y a con la política completa o con una parte de las políticas que sean las instrucciones específicas, o sea, si vamos a traducir la política a una serie de instrucciones para alimentar el auditor.

Dicho eso... Incluso hacerle una sección, ¿no?, a la política de, che, mira, esto lo tiene que leer el auditor y punto. pero porque además en el escenario hiperideal que nosotros nos planteamos que queremos llegar con la auditoría esperábamos insisto escenario hiperideal

automatizar, creo que dijimos el 50% de los casos, va a tener la otra mitad donde lo va a tener que ver un humano con toda la política, el contexto, los estudios, los informes, los paper y todo lo que tiene la política. No es que estamos hablando de la política. Me parece que de lo que estamos hablando puntualmente es, nosotros creíamos que la realidad usaba la política para definir. Nos dimos cuenta que hay una discrepancia en eso. Bueno, ahora la política cobra tanta importancia para la auditoría, porque se basa estrictamente en eso, que tenemos que redefinir lo que queremos poner.

No es inocente ahora poner que necesitamos la tomografía y en realidad nos sirve una historia clínica. No, no, ahora ponemos que necesitamos la tomografía y si la tomografía no está, se rechaza. Y si eso implica que vamos a rechazar el 95% de los casos, tenemos un problema.

Esa es la conclusión que tengo. Y me parece que está bien. Bueno, comparto, está bien por eso, pero eso ya lo podemos empezar a trabajar y ver para no... para ir avanzando. Eso es lo que no me ha quedado claro, ¿quién se lo lleva? ¿Quién lo tiene que discutir? Y eso es un poco lo que decía Martín, tiene que ver Pablo, con Martín y con el equipo de políticas, y va a haber que hacer una revisión de todas las políticas con las que vamos a trabajar bajo esta mirada que es distinta a la mirada que teníamos antes.

La mirada que tenemos ahora es se te escapa una coma y rechazás el 90% de los casos. No es lo que nosotros, no es la forma al menos en la cual nosotros pensábamos que estábamos mirando esa política. Ahora es mucho más determinante de lo que nos imaginábamos. Quizás siempre fue así, lo único que cambió fue nuestra cabeza, que antes lo dábamos por sentado, que era más...

Flexible, y ahora nos damos cuenta que no, seguramente sea eso, ahora cuando es un tipo de tipo Si, o era más sentido común o... O de otra manera Y ahora hay que ser más explícito Antes era un humano y ahora es... No es más una guía a la política, es la norma. Y creo que esa es la conclusión. Sí, me gusta.

Chicos, Patrick había mandado un documento que es como donde se va poniendo el resumen de los aprendizajes, las conclusiones que fuimos sacando, no sé si lo vieron, pero aprovecho para comentarles. Porque muchas de las cosas que hablamos acá, que estuvimos hablando en estos últimos minutos que estuvieron muy buenas, primero no las grabamos, así que la mitad nos las vamos a olvidar.

Pero no, estaría bueno que... ¿Está tomando nota? No, no está tomando nota, ¿viste? No, no está tomando nada. No, estaría bueno que pasamos poniendo ahí... ¿Podés decir que de la parte más importante de todas estas reuniones nos olvidamos de tomar nota?

No, no, yo... una minuta... Memoria de corto plazo tengo buena, después de 10 minutos me olvido, pero si queremos que nos cortamos, armamos algo. Yo quiero decir dos ideas y cuando estuve empezando la primera me olvidé de la segunda, así que conmigo no cuenten.

¿Tú no le compartiste a Marcos ese documento que está en el chat? Sí, yo tampoco lo veo, che. ¿O en una conversación? Ahí me fijo, espera. ¿Privada con vos? Había sido conversación, Chango, vos no estás en el chat. Puede ser, puede ser. Esperen, esperen.

Si fuese privado conmigo igual no debería estar todos, pero vamos a ver. Si no lo tenemos, no lo veo yo. Bueno, pegálos si podés en el auditor ahí en el chat. No, no, ahora quiero que se queden porque si están acá los voy a bardear. Esperen un minuto. Ay, se corta, no se escucha bien. No, no saben que no están. Ay, qué lástima, chicos, que tengamos razón. Qué boludo. Nos dejaron afuera, o sea. Llegaron muchachos y dejarte joder.

Era una charla privada, obvio, Iba. No, no, hay muchas cosas, pero no sé lo que es. Tengo compañerismo. Conozco de antes a Marcos, no ha cambiado nada. No, no, por eso, hasta ahí llegué con el comentario.

Ahí va.

Bueno, supongo que le habrá empezado a trabajar a Patri, así que ahí hay espacio para editar. Bueno, dale. ¿Nos mandás entonces, Martín? Ya que te comprometiste. Yo me comprometí. Me ofrecí, pero me puedo comprometer. No soy como vos, Marco. No hay problema.

Ya está, quedaste pegado. Si querés, grabo solamente los dos minutos de la ronda. Dale, dale, ponelo, ponelo. Ponés en el chat. Bueno, Martín, se lleva a actualizar lo que vimos hoy. no hay ningún problema, les mando 3 o 4 ideas de lo que me acuerde agreguen todo lo que quieran, obviamente

Bueno, gente, nos vemos. Chau, chau.

▶ **20260706**

<!-- unknown block type: transcription (3952c02a...) -->



### Acción Items

- [ ] Hablar con Fer para reclutar casos y revisar políticas de cobertura para tener todo listo eventualmente 
- [ ] Martín a agregar detalles de proceso a la presentación antes del viernes 
- [ ] Patri a compartir el link de la presentación para revisión offline con comentarios  
- [ ] Marcos a revisar la presentación e incorporar comentarios de forma offline 
- [ ] Convocar a todos (incluyendo a Soles) para la reunión de presentación del viernes 17  
### Estado de las API Keys y Presupuesto

- El equipo ha venido pagando de su propio bolsillo las pruebas con modelos de IA  
- Se espera obtener las API keys de la compañía la semana siguiente 
- El presupuesto estaría aprobado, lo que permitiría cubrir los costos de las pruebas 
### Disponibilidad del Equipo

- Julio es un mes complicado: muchas personas de vacaciones y bajas  
- Pablo está de vacaciones esta semana 
- Martín viaja a Salta la semana siguiente (lunes a miércoles) y luego se ausenta tres semanas  
### Conclusión de la POC

- La discusión central fue si realizar más casos de prueba o dar por concluida la POC  
- Posición de Martín: el objetivo de la POC era determinar si el proyecto era viable, **no** validar la herramienta para producción  
- Conclusión acordada: **la herramienta es viable** y puede convertirse en un proyecto formal, reconociendo las limitaciones encontradas   
- Los casos no probados quedan como incertidumbre a resolver dentro del proyecto  
- Se coincidió en la necesidad de avanzar con celeridad dado el contexto organizacional  
### Próximos Pasos: Presentación del Caso de Negocio

- Se acordó avanzar a la etapa de presentación del caso de negocio como revisión final de la POC  
- **Fecha acordada: viernes 17** (Marcos y Soles participarán por el área de Ibas)   
- La revisión de la presentación se hará de forma **offline**, con comentarios en el documento compartido, para no consumir tiempo de reunión 


[https://docs.google.com/presentation/d/1JhM0UG4fzv_T3bzEMDn-aJgmBMSyNy0OxWepndX6J1M/edit?usp=sharing](https://docs.google.com/presentation/d/1JhM0UG4fzv_T3bzEMDn-aJgmBMSyNy0OxWepndX6J1M/edit?usp=sharing)



Podríamos no haber probado nada y empezar el proyecto igual también, ¿no? Sí, sí, totalmente. Qué sé yo, me parece que lo que sí amerita es que si lo vamos a hacer tenemos que hacerlo lo más rápido posible y acá se aclara una cosa que es que venimos probando...

con modelos y lo estamos pagando nosotros, entonces ya llegó un punto en el cual no tengo más ganas de pagar nada Porque no tengo ganas de pagarle yo a Google Estamos a punto de conseguir las API keys, pero se estiró un poquito más de lo que corresponde Entonces, nada, se supone que la semana que viene vamos a tener acceso

Y ya el presupuesto también en teoría está aprobado, con lo cual podría destinar el dinero que había puesto para eso, que era más que suficiente. Pero hoy en día está saliendo de nuestro bolsillo. Entonces, cada vez que interamos, lo pagamos nosotros. No es mucha plata, pero me parece que ya no da para más. No, no, totalmente. Entonces, digo, si te parece, para alinear con esto último que dijiste, que me parece también...

conducente, esperemos a ver qué pasa con eso de la piquí del presupuesto y en función de eso vemos si aumentamos la casística, ¿qué parece? Si queremos hacerlo hay que saber que hay que esperar a la semana que viene. Hablar con Fer para ir reclutando los casos y ver de qué prestaciones tenemos las políticas de cobertura y qué sé yo, para tenerlo todo listo eventualmente.

Ah, que uno estaba mirando la pantalla. Perdón. ¿Qué hacés, Pablo? ¿Cómo andás? Hola, buen día. Buen día. Perdón, lo demora. Pero está de vacaciones esta semana. Bueno, hablamos con Vero, no sé, no hay problema, lo ademina. Sí, sí, sí. semana complicada, mucha gente se fue de vacaciones, tuvimos varias bajas

Julio lo es completo en realidad, porque durante todo el mes va a haber bajas. Es así, en dos semanas me voy yo, así que bueno, esta semana tenemos bastantes bajas. ¿Te parece que pongamos fecha de la presentación esta como para que nos alineemos todos a terminar o terminar para esa fecha, cuando vuelva Pablo o antes de que se vaya?

Como lo ves, Marcos.

Sí, cuando quieran. Recién Martín estaba poniendo para ir a revisar unos casos más y discutamos eso, si es algo que queremos hacer o no, y creo que eso nos va a marcar un poco el camino. Ahí está.

A ver, yo en lo personal creo que el aprendizaje de lo que quería demostrar esta prueba lo tenemos. Sabemos dónde, no estamos en una etapa ya de proyecto y productiva para tomar una decisión La decisión que debía tomar con esta prueba era si valía la pena seguir avanzando y convertirlo en un proyecto o desestimarlo. No estábamos en una etapa de validación de la herramienta para ponerla en producción.

Lo que quiero decir es que, nada, los tiempos son complicados, es lo que decía Patri y este mes va a ser complicado, la semana que viene para mí es hiper complicada Yo viajo a Salta por la comisión directiva, no voy a estar casi toda la semana, la otra semana me voy, me voy tres semanas. Yo lo que no quiero es que esto se dilate más. Creo que la decisión que teníamos que tomar en esta mesa es que esto...

Puede ser viable, no puede ser viable, se puede convertir en un proyecto, después dentro del proyecto habrá que resolver todo Y mi impresión, por las pruebas y por lo que aprendimos, es que... con el aprendizaje que tenemos, es viable, dentro del marco que corresponda y con las limitaciones que tiene o que encontramos.

pero que es viable.

Díganme si coinciden o no, pero yo creo que estamos en etapa de decir que esto fue lo que aprendimos, esto fue lo que nos dio esta POC, creemos que se puede convertir en un proyecto y tenemos ya los recaudos para... para avanzar a una etapa de refinamiento, de pruebas y de todo lo que nos dejó esta POC.

porque si no siento que se va a estirar todo mucho y la realidad también es que esto quizás es un poco más político que otra cosa Pero la compañía está pidiendo celeridad en un montón de cosas. Y me parece que deberíamos pasar esta y pasar a la siguiente etapa. Esa es mi opinión.

¿Entonces? No, no, está bien, con los pasos que tenemos. ¿Esta semana? ¿Cómo? ¿Teníamos que pensar esta semana? Si es la semana que viene, ¿no está? ¿La semana que viene no estás? No, la otra. Estaba en Salta. Ah, está en Salta, sí, sí. Ahí está en Salta. Yo ya vuelvo el miércoles, o sea, lunes, martes y miércoles no estoy, pero jueves o viernes podríamos hacerlo. Ah, perfecto.

Perfecto.

Si estamos de acuerdo, digo, en las conclusiones que yo saqué, digo, pero si les parece que no estamos seguros de que esto pueda funcionar y que hay que hacer más pruebas, sigamos haciendo pruebas. Digo, el objetivo de esta POC era ver si se podía convertir en un proyecto viable, entiendo yo. No si podíamos, la herramienta, validarla para ponerla en producción.

Claramente en esa situación no estamos, digamos, no estamos en una instancia en la cual podríamos pensar en avanzar. Muchas gracias.

Pero bueno, nada, esa es mi opinión, acá estamos para discutir y que cada uno opine.

Yo lo que estaba comentando recién, justo antes de que ingreses, es una cuestión de riesgos nada más, y entendemos que... Si vos decías recién, para el objetivo que teníamos, lo pudimos cumplir, a pesar de que hay ciertos casos que no los probamos Nos quedaremos con esa incertidumbre, entendiendo también que, bueno, después lo...

lo vamos a poder sortear durante el proyecto y que ese también será uno de nuestros objetivos.

Yo diría que sí, que podemos avanzar. Nosotros estamos tratando ahora de que se cierre el contrato con esta empresa y de buscar recursos para que, obviamente, podamos llevar adelante los proyectos que tenemos, por lo menos los prioritarios.

Si estamos de acuerdo, pongamos fecha. Hagamos la convocatoria. La presentación yo la ordené un poco. Por ahí le agrego algunas cositas más, pero son más del proceso, no cambian. Por ahí las conclusiones a las cuales se había llegado y bueno, avancemos

en la presentación del caso de negocio, porque es una review, y ustedes, ya que son los que están participando hoy acá, que los tengo cerquitas, ¿Cuándo les es un momento mejor? El jueves, el viernes, mañana, mediodía, tarde?

Acordemos uno porque nos vamos a romper las agendas del resto. No juegues. El jueves 16 sería... El jueves sería... Ah. Si puede ser el viernes mejor, si no me adapto.

Yo no tengo problema por ahora. El jueves tengo bastante libre y el viernes también tengo bastante libre entre las nueve. y las dos. Perfecto, vamos entonces coincidencia el viernes. Marcos y Ibas ¿están bien? Sí, sí. Yo no estoy, pero está Soles seguramente.

Así que bien, la invitamos a eso entonces. Sí, sí.

Bueno, ¿querés que la repasemos, Marcos, a la prensa por las dudas? Eh, yo les... Yo, para utilizar tiempo, hagamos offline, me parece mejor. Hagamos una de las revises, pongan en los comentarios si quieren y... Y las ajustamos así, así no estamos acá todos mirando la presentación, pero como prefiero Compartí entonces el link y ya...

y nos liberamos para el viernes 17 Sí, el link es el que vos hiciste Patri, ¿no? ¿Es la misma? ¿La querés compartir? Si la miramos todos en la misma. Ahí vamos. Gracias. Buscándola.

Hasta entonces, compartida.

Buenísimo. Bueno, vamos entonces que vamos para el jueves que viene. Para el viernes. Viernes. Ah, perdón, el viernes. Sí, viernes de etiqueta. Ahí en un ratito termino de chequear que seamos todos y la comparto. Muchísimas gracias. Gracias, nos vemos.

Si no, avísame Marcos y nos vemos de vuelta.

Autorizaciones AI

![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/aa10ce88-03fc-486b-8a9d-bfbf780e83b6/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VORG53TY%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150151Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJGMEQCIBnctDyyR5uZKUPTskv6jq3TnEahtDWrwpF1sV%2BCNI7uAiAneNKdUFC8hElNu1%2FuqNRrsAFWt4fYWRByt6Op8dEOFSqIBAiH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMuiZK7iEhmt05zHd%2BKtwDR1S8ZmUg8FGOpX3y8MdScNltbQV4AoCrlBJ%2Fce2zVxeifDPLxMKsuAsjTw%2By83SYnatS8JCu4xoGbcSztcGwphDNa3ZYhk0i4Wjwr5J3BpsSw8ej91vRpPb8zYslsEvBrMLRzUV0crZrEZdUWf7Wbrwsqw9ApyaLW771zeJ6Ggyw3xnzcvsE3QqW3JhF7FWLWwu3mm0Wd96ff6%2BOjCH%2F7x6D1JyZtpP%2FpO6qbzYLRe0bQ%2FNJ19GOPktReQcF8a%2FGB6F2lR9CzkgpCdDYugtYiFu3ILydRO%2BAmR5A0XWsfbGIoEWQWD0spLv2enqma4UavY0kl2VIF8%2FnEO567WgDLFj%2B%2Bd1vgxRcl6ggl%2BPLf7wG3pVNZOcTzzYwJEvCovQCljJC5RkK%2FJ9%2BX1aewgGSrCjxfI1uiq26eUIAG1V0vMe9Hm5DjkXv4casHLTm0pADYiVoulYv5RqLxd19nPExPr3UmZkZp3K9AAKXzCL8lvLCdeY1Zcj9dy8ZnhA3DX3BzXPzy4hg0XA1DufldA9FaD3eCIBmCAiv6go8yv3h9w%2FSmqooez%2B1RNx%2Bjl0Bfyo2%2FAIHQ4tTi5xWl4gixKEFfSvwMy5WYFFkLVyyQCL9zevXm4T65BgodBg%2F4eAwraa50gY6pgGerLt6EmZuRzkcfgK8kkGJO3jAHU%2FeLLu3Uz1ENNBlKK5MMOwF16FWxfbVJNSLya6BGjz9tREpwH%2BzTywDn%2FTvRyrbXAiVsmK5qBkpPlINHba4RTcmfcl%2BnkPhcS9zgtO1AEJSFU49KG8%2FsGyxxMMY29u%2BtqcyW2NO4%2FeEVgs98iap%2FwnSptDjfXdW2RbQwPOUYXKdfsRlJn89mkLqA6XT44Atb3OR&X-Amz-Signature=80e4b1458f3475038e6cc1afc2ec3d84dafc567385b845f283fff1de3aee8414&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/338f5dca-b60d-4eb6-933c-e29149a02443/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VORG53TY%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150151Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJGMEQCIBnctDyyR5uZKUPTskv6jq3TnEahtDWrwpF1sV%2BCNI7uAiAneNKdUFC8hElNu1%2FuqNRrsAFWt4fYWRByt6Op8dEOFSqIBAiH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMuiZK7iEhmt05zHd%2BKtwDR1S8ZmUg8FGOpX3y8MdScNltbQV4AoCrlBJ%2Fce2zVxeifDPLxMKsuAsjTw%2By83SYnatS8JCu4xoGbcSztcGwphDNa3ZYhk0i4Wjwr5J3BpsSw8ej91vRpPb8zYslsEvBrMLRzUV0crZrEZdUWf7Wbrwsqw9ApyaLW771zeJ6Ggyw3xnzcvsE3QqW3JhF7FWLWwu3mm0Wd96ff6%2BOjCH%2F7x6D1JyZtpP%2FpO6qbzYLRe0bQ%2FNJ19GOPktReQcF8a%2FGB6F2lR9CzkgpCdDYugtYiFu3ILydRO%2BAmR5A0XWsfbGIoEWQWD0spLv2enqma4UavY0kl2VIF8%2FnEO567WgDLFj%2B%2Bd1vgxRcl6ggl%2BPLf7wG3pVNZOcTzzYwJEvCovQCljJC5RkK%2FJ9%2BX1aewgGSrCjxfI1uiq26eUIAG1V0vMe9Hm5DjkXv4casHLTm0pADYiVoulYv5RqLxd19nPExPr3UmZkZp3K9AAKXzCL8lvLCdeY1Zcj9dy8ZnhA3DX3BzXPzy4hg0XA1DufldA9FaD3eCIBmCAiv6go8yv3h9w%2FSmqooez%2B1RNx%2Bjl0Bfyo2%2FAIHQ4tTi5xWl4gixKEFfSvwMy5WYFFkLVyyQCL9zevXm4T65BgodBg%2F4eAwraa50gY6pgGerLt6EmZuRzkcfgK8kkGJO3jAHU%2FeLLu3Uz1ENNBlKK5MMOwF16FWxfbVJNSLya6BGjz9tREpwH%2BzTywDn%2FTvRyrbXAiVsmK5qBkpPlINHba4RTcmfcl%2BnkPhcS9zgtO1AEJSFU49KG8%2FsGyxxMMY29u%2BtqcyW2NO4%2FeEVgs98iap%2FwnSptDjfXdW2RbQwPOUYXKdfsRlJn89mkLqA6XT44Atb3OR&X-Amz-Signature=fba7a30c59e06b121cfbf420c5748ffde54c6081e45ad3bdb44150d845353e4f&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

GLM OCR para lectura de recetas


![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/92a37ecb-0996-4cf7-99aa-3d1a0ac3f3b7/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VORG53TY%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150151Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJGMEQCIBnctDyyR5uZKUPTskv6jq3TnEahtDWrwpF1sV%2BCNI7uAiAneNKdUFC8hElNu1%2FuqNRrsAFWt4fYWRByt6Op8dEOFSqIBAiH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMuiZK7iEhmt05zHd%2BKtwDR1S8ZmUg8FGOpX3y8MdScNltbQV4AoCrlBJ%2Fce2zVxeifDPLxMKsuAsjTw%2By83SYnatS8JCu4xoGbcSztcGwphDNa3ZYhk0i4Wjwr5J3BpsSw8ej91vRpPb8zYslsEvBrMLRzUV0crZrEZdUWf7Wbrwsqw9ApyaLW771zeJ6Ggyw3xnzcvsE3QqW3JhF7FWLWwu3mm0Wd96ff6%2BOjCH%2F7x6D1JyZtpP%2FpO6qbzYLRe0bQ%2FNJ19GOPktReQcF8a%2FGB6F2lR9CzkgpCdDYugtYiFu3ILydRO%2BAmR5A0XWsfbGIoEWQWD0spLv2enqma4UavY0kl2VIF8%2FnEO567WgDLFj%2B%2Bd1vgxRcl6ggl%2BPLf7wG3pVNZOcTzzYwJEvCovQCljJC5RkK%2FJ9%2BX1aewgGSrCjxfI1uiq26eUIAG1V0vMe9Hm5DjkXv4casHLTm0pADYiVoulYv5RqLxd19nPExPr3UmZkZp3K9AAKXzCL8lvLCdeY1Zcj9dy8ZnhA3DX3BzXPzy4hg0XA1DufldA9FaD3eCIBmCAiv6go8yv3h9w%2FSmqooez%2B1RNx%2Bjl0Bfyo2%2FAIHQ4tTi5xWl4gixKEFfSvwMy5WYFFkLVyyQCL9zevXm4T65BgodBg%2F4eAwraa50gY6pgGerLt6EmZuRzkcfgK8kkGJO3jAHU%2FeLLu3Uz1ENNBlKK5MMOwF16FWxfbVJNSLya6BGjz9tREpwH%2BzTywDn%2FTvRyrbXAiVsmK5qBkpPlINHba4RTcmfcl%2BnkPhcS9zgtO1AEJSFU49KG8%2FsGyxxMMY29u%2BtqcyW2NO4%2FeEVgs98iap%2FwnSptDjfXdW2RbQwPOUYXKdfsRlJn89mkLqA6XT44Atb3OR&X-Amz-Signature=111ae133de3b5ab54cdb9fa76a7908e179c7f3073d319b26a5f69e85a40d48df&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/092f69d1-5894-4871-80c4-869e66ee0e4b/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VORG53TY%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150151Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJGMEQCIBnctDyyR5uZKUPTskv6jq3TnEahtDWrwpF1sV%2BCNI7uAiAneNKdUFC8hElNu1%2FuqNRrsAFWt4fYWRByt6Op8dEOFSqIBAiH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMuiZK7iEhmt05zHd%2BKtwDR1S8ZmUg8FGOpX3y8MdScNltbQV4AoCrlBJ%2Fce2zVxeifDPLxMKsuAsjTw%2By83SYnatS8JCu4xoGbcSztcGwphDNa3ZYhk0i4Wjwr5J3BpsSw8ej91vRpPb8zYslsEvBrMLRzUV0crZrEZdUWf7Wbrwsqw9ApyaLW771zeJ6Ggyw3xnzcvsE3QqW3JhF7FWLWwu3mm0Wd96ff6%2BOjCH%2F7x6D1JyZtpP%2FpO6qbzYLRe0bQ%2FNJ19GOPktReQcF8a%2FGB6F2lR9CzkgpCdDYugtYiFu3ILydRO%2BAmR5A0XWsfbGIoEWQWD0spLv2enqma4UavY0kl2VIF8%2FnEO567WgDLFj%2B%2Bd1vgxRcl6ggl%2BPLf7wG3pVNZOcTzzYwJEvCovQCljJC5RkK%2FJ9%2BX1aewgGSrCjxfI1uiq26eUIAG1V0vMe9Hm5DjkXv4casHLTm0pADYiVoulYv5RqLxd19nPExPr3UmZkZp3K9AAKXzCL8lvLCdeY1Zcj9dy8ZnhA3DX3BzXPzy4hg0XA1DufldA9FaD3eCIBmCAiv6go8yv3h9w%2FSmqooez%2B1RNx%2Bjl0Bfyo2%2FAIHQ4tTi5xWl4gixKEFfSvwMy5WYFFkLVyyQCL9zevXm4T65BgodBg%2F4eAwraa50gY6pgGerLt6EmZuRzkcfgK8kkGJO3jAHU%2FeLLu3Uz1ENNBlKK5MMOwF16FWxfbVJNSLya6BGjz9tREpwH%2BzTywDn%2FTvRyrbXAiVsmK5qBkpPlINHba4RTcmfcl%2BnkPhcS9zgtO1AEJSFU49KG8%2FsGyxxMMY29u%2BtqcyW2NO4%2FeEVgs98iap%2FwnSptDjfXdW2RbQwPOUYXKdfsRlJn89mkLqA6XT44Atb3OR&X-Amz-Signature=369c63384dfe590e1b5d70d42eafe5b20c566aa19663e7b2295898dd377401a0&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/2648e6e4-dde4-46b5-a65a-28ce1fc2433a/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VORG53TY%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150151Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJGMEQCIBnctDyyR5uZKUPTskv6jq3TnEahtDWrwpF1sV%2BCNI7uAiAneNKdUFC8hElNu1%2FuqNRrsAFWt4fYWRByt6Op8dEOFSqIBAiH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMuiZK7iEhmt05zHd%2BKtwDR1S8ZmUg8FGOpX3y8MdScNltbQV4AoCrlBJ%2Fce2zVxeifDPLxMKsuAsjTw%2By83SYnatS8JCu4xoGbcSztcGwphDNa3ZYhk0i4Wjwr5J3BpsSw8ej91vRpPb8zYslsEvBrMLRzUV0crZrEZdUWf7Wbrwsqw9ApyaLW771zeJ6Ggyw3xnzcvsE3QqW3JhF7FWLWwu3mm0Wd96ff6%2BOjCH%2F7x6D1JyZtpP%2FpO6qbzYLRe0bQ%2FNJ19GOPktReQcF8a%2FGB6F2lR9CzkgpCdDYugtYiFu3ILydRO%2BAmR5A0XWsfbGIoEWQWD0spLv2enqma4UavY0kl2VIF8%2FnEO567WgDLFj%2B%2Bd1vgxRcl6ggl%2BPLf7wG3pVNZOcTzzYwJEvCovQCljJC5RkK%2FJ9%2BX1aewgGSrCjxfI1uiq26eUIAG1V0vMe9Hm5DjkXv4casHLTm0pADYiVoulYv5RqLxd19nPExPr3UmZkZp3K9AAKXzCL8lvLCdeY1Zcj9dy8ZnhA3DX3BzXPzy4hg0XA1DufldA9FaD3eCIBmCAiv6go8yv3h9w%2FSmqooez%2B1RNx%2Bjl0Bfyo2%2FAIHQ4tTi5xWl4gixKEFfSvwMy5WYFFkLVyyQCL9zevXm4T65BgodBg%2F4eAwraa50gY6pgGerLt6EmZuRzkcfgK8kkGJO3jAHU%2FeLLu3Uz1ENNBlKK5MMOwF16FWxfbVJNSLya6BGjz9tREpwH%2BzTywDn%2FTvRyrbXAiVsmK5qBkpPlINHba4RTcmfcl%2BnkPhcS9zgtO1AEJSFU49KG8%2FsGyxxMMY29u%2BtqcyW2NO4%2FeEVgs98iap%2FwnSptDjfXdW2RbQwPOUYXKdfsRlJn89mkLqA6XT44Atb3OR&X-Amz-Signature=7f530a9a08e8b58e243d495780342ea24032a0dc11eaf5eb839e9067b9a44a6d&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/a522ff62-be14-4b70-bd38-49d1240fdee9/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VORG53TY%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150151Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJGMEQCIBnctDyyR5uZKUPTskv6jq3TnEahtDWrwpF1sV%2BCNI7uAiAneNKdUFC8hElNu1%2FuqNRrsAFWt4fYWRByt6Op8dEOFSqIBAiH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMuiZK7iEhmt05zHd%2BKtwDR1S8ZmUg8FGOpX3y8MdScNltbQV4AoCrlBJ%2Fce2zVxeifDPLxMKsuAsjTw%2By83SYnatS8JCu4xoGbcSztcGwphDNa3ZYhk0i4Wjwr5J3BpsSw8ej91vRpPb8zYslsEvBrMLRzUV0crZrEZdUWf7Wbrwsqw9ApyaLW771zeJ6Ggyw3xnzcvsE3QqW3JhF7FWLWwu3mm0Wd96ff6%2BOjCH%2F7x6D1JyZtpP%2FpO6qbzYLRe0bQ%2FNJ19GOPktReQcF8a%2FGB6F2lR9CzkgpCdDYugtYiFu3ILydRO%2BAmR5A0XWsfbGIoEWQWD0spLv2enqma4UavY0kl2VIF8%2FnEO567WgDLFj%2B%2Bd1vgxRcl6ggl%2BPLf7wG3pVNZOcTzzYwJEvCovQCljJC5RkK%2FJ9%2BX1aewgGSrCjxfI1uiq26eUIAG1V0vMe9Hm5DjkXv4casHLTm0pADYiVoulYv5RqLxd19nPExPr3UmZkZp3K9AAKXzCL8lvLCdeY1Zcj9dy8ZnhA3DX3BzXPzy4hg0XA1DufldA9FaD3eCIBmCAiv6go8yv3h9w%2FSmqooez%2B1RNx%2Bjl0Bfyo2%2FAIHQ4tTi5xWl4gixKEFfSvwMy5WYFFkLVyyQCL9zevXm4T65BgodBg%2F4eAwraa50gY6pgGerLt6EmZuRzkcfgK8kkGJO3jAHU%2FeLLu3Uz1ENNBlKK5MMOwF16FWxfbVJNSLya6BGjz9tREpwH%2BzTywDn%2FTvRyrbXAiVsmK5qBkpPlINHba4RTcmfcl%2BnkPhcS9zgtO1AEJSFU49KG8%2FsGyxxMMY29u%2BtqcyW2NO4%2FeEVgs98iap%2FwnSptDjfXdW2RbQwPOUYXKdfsRlJn89mkLqA6XT44Atb3OR&X-Amz-Signature=013c048043ffeaeb321e75578d051d1243db9172103a7b7ed62bdc6aa2af1889&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

![Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/d115ebf0-04d4-4a37-969d-6c92b512ce86/3be95b4c-8801-43d2-8fd4-daeceb9d0770/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466VORG53TY%2F20260708%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260708T150151Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEL7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJGMEQCIBnctDyyR5uZKUPTskv6jq3TnEahtDWrwpF1sV%2BCNI7uAiAneNKdUFC8hElNu1%2FuqNRrsAFWt4fYWRByt6Op8dEOFSqIBAiH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMuiZK7iEhmt05zHd%2BKtwDR1S8ZmUg8FGOpX3y8MdScNltbQV4AoCrlBJ%2Fce2zVxeifDPLxMKsuAsjTw%2By83SYnatS8JCu4xoGbcSztcGwphDNa3ZYhk0i4Wjwr5J3BpsSw8ej91vRpPb8zYslsEvBrMLRzUV0crZrEZdUWf7Wbrwsqw9ApyaLW771zeJ6Ggyw3xnzcvsE3QqW3JhF7FWLWwu3mm0Wd96ff6%2BOjCH%2F7x6D1JyZtpP%2FpO6qbzYLRe0bQ%2FNJ19GOPktReQcF8a%2FGB6F2lR9CzkgpCdDYugtYiFu3ILydRO%2BAmR5A0XWsfbGIoEWQWD0spLv2enqma4UavY0kl2VIF8%2FnEO567WgDLFj%2B%2Bd1vgxRcl6ggl%2BPLf7wG3pVNZOcTzzYwJEvCovQCljJC5RkK%2FJ9%2BX1aewgGSrCjxfI1uiq26eUIAG1V0vMe9Hm5DjkXv4casHLTm0pADYiVoulYv5RqLxd19nPExPr3UmZkZp3K9AAKXzCL8lvLCdeY1Zcj9dy8ZnhA3DX3BzXPzy4hg0XA1DufldA9FaD3eCIBmCAiv6go8yv3h9w%2FSmqooez%2B1RNx%2Bjl0Bfyo2%2FAIHQ4tTi5xWl4gixKEFfSvwMy5WYFFkLVyyQCL9zevXm4T65BgodBg%2F4eAwraa50gY6pgGerLt6EmZuRzkcfgK8kkGJO3jAHU%2FeLLu3Uz1ENNBlKK5MMOwF16FWxfbVJNSLya6BGjz9tREpwH%2BzTywDn%2FTvRyrbXAiVsmK5qBkpPlINHba4RTcmfcl%2BnkPhcS9zgtO1AEJSFU49KG8%2FsGyxxMMY29u%2BtqcyW2NO4%2FeEVgs98iap%2FwnSptDjfXdW2RbQwPOUYXKdfsRlJn89mkLqA6XT44Atb3OR&X-Amz-Signature=266c2c27d88a1b11c9e2275b1681b49e84c895b7f43310870f5b774c555b371d&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)



Materiales

[https://drive.google.com/drive/folders/19eEW5CnM-2ZlwRDx7BNNb2yvagYJZcAB?usp=sharing](https://drive.google.com/drive/folders/19eEW5CnM-2ZlwRDx7BNNb2yvagYJZcAB?usp=sharing)

[https://docs.google.com/document/d/1wiWBnu5VF3ZGZbhkfsEzlQmUJ7oqZNRw/edit?usp=sharing&ouid=102832160443662348564&rtpof=true&sd=true](https://docs.google.com/document/d/1wiWBnu5VF3ZGZbhkfsEzlQmUJ7oqZNRw/edit?usp=sharing&ouid=102832160443662348564&rtpof=true&sd=true)

[https://docs.google.com/presentation/d/1JhM0UG4fzv_T3bzEMDn-aJgmBMSyNy0OxWepndX6J1M/edit?usp=sharing](https://docs.google.com/presentation/d/1JhM0UG4fzv_T3bzEMDn-aJgmBMSyNy0OxWepndX6J1M/edit?usp=sharing)



