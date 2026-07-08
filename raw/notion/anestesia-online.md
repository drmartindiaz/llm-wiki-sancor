---
source_url: https://app.notion.com/p/2cd2c02ab01980f9a425e05d51ee3168
ingested: 2026-07-08
title: Anestesia Online
notion_id: 2cd2c02a-b019-80f9-a425-e05d51ee3168
---

<!-- unknown block type: transcription (2cd2c02a...) -->



### Contexto y Necesidad del Proyecto

- El proyecto busca sumar el servicio de anestesia a la validación online, una necesidad planteada por analistas hace 3-4 meses 
- Anestesia es el tercer rubro más voluminoso en términos económicos para Sancor, pero es donde menos asertivos son en cuanto a presupuesto y estimación  
- Actualmente toda la auditoría de anestesia es posterior a la realización, no existe auditoría previa ni generación de formularios previos 
- El objetivo principal es tener información online para valorizar y ser asertivos en la información económica, y automatizar el proceso de facturación que hoy es manual  
### Análisis de Mercado y Proveedores

- Se evaluaron tres carriers principales: Traditum, Activia y EveWeb  
- Activia tiene implementación con ARBA pero solo llegan a hacer elegibilidad, no logran que el prestador valide o autorice 
- EveWeb es el proveedor más completo en desarrollo, permite cargar hora, vincular práctica, y determinar si es diurna/vespertina 
- EveWeb ya es utilizado por 21 de las 24 provincias para otros servicios, lo que facilita la escalabilidad  
### Codificación y Nomenclador

- Sancor trabaja con 10 códigos de complejidad para anestesia, cada provincia tiene su propio nomenclador 
- El mayor volumen económico proviene de los adicionales (feriados, geriátricos, pediátricos) que agregan 50-75% al valor base 
- Se trabajó con el Dr. Bocco, Dra. Hércoles y el comité médico para crear nuevos códigos que otras prepagas ya transaccionaban 
- Actualmente existe un problema de vinculación: los convenios solo mapean complejidad contra complejidad, sin vincular automáticamente la cirugía específica con la anestesia   
### Desafíos con ARBA

- ARBA (Asociación de Anestesiólogos de Buenos Aires) representa aproximadamente el 80% de la facturación de anestesia a nivel país  
- No existe posibilidad de integración con ARBA debido a cuestiones políticas, no técnicas   
- Se han intentado acercamientos a diferentes niveles, incluyendo gerencia, sin resultados positivos   
- El proyecto se enfocará en las otras 23 provincias que representan el 20% de la facturación  
### Prueba Piloto

- Se está realizando una prueba piloto con Salta y Tierra del Fuego utilizando EveWeb  
- El objetivo es validar que la información se cargue de manera diferida pero dentro de una semana 
- Se están ajustando datos específicos como hora y otros parámetros necesarios 
### Naturaleza del Proceso: Validación vs Autorización

- Se debatió extensamente si esto debe llamarse "autorización" o tiene otra naturaleza    
- La conclusión es que NO es una autorización previa, ya que la carga es diferida después de realizada la anestesia  
- Otros sistemas en el mercado lo llaman "validación online" o simplemente "aviso" o "carga de prestación" 
- Se sugirió usar nomenclatura explícita como "aviso", "informe" o "carga de prestación" para evitar malentendidos 
### Debate sobre Valor Agregado

- Se cuestionó qué valor aporta tener el aviso antes versus recibir la facturación después  
- Los beneficios identificados incluyen:
- Conocer el gasto en tiempo real para mejor arqueo de caja y previsibilidad   
- Automatizar procesos y eliminar papeles 
- Tener datos más asertivos sobre complejidades reales (urgencias, feriados, características del paciente) 
- Información actualizada sin esperar 60-90 días 
### Consideraciones Técnicas

- Existe dificultad para vincular automáticamente las cirugías autorizadas con las anestesias cargadas posteriormente   
- Los anestesiólogos cargan la información post-cirugía y típicamente no tienen acceso a códigos del nomenclador nacional ni a información administrativa de formularios  
- Se propuso que además de la complejidad, se cargue el código de la cirugía para crear vinculación entre ambos  
- El protocolo quirúrgico clínico obligatorio podría ser fuente de información para validar la anestesia realizada 
### Encuadre como Proyecto IT

- Marcos planteó que esto debe tratarse como un proyecto formal con presupuesto y recursos asignados  
- La decisión de si es desarrollo interno o compra externa se definirá en ese nivel  
- Este tema está incluido en el paquete de proyectos de transformación digital que se presentará con Mati Villeta 
- Se mencionaron posibles timelines de 2026 o 2030 dependiendo de la priorización  
### Próximos Pasos

- Marcos validará internamente si esto debe ser un proyecto formal y comunicará en 1-2 días  
- El equipo refinará la presentación agregando:
- Flujos de proceso más detallados  
- Información sobre homologación de códigos 
- Explicación de vinculación entre práctica y anestesia 
- Módulos de auditoría y facturación de EveWeb 
- Se continuará con la prueba piloto en Salta y Tierra del Fuego 
### Consideraciones sobre Incentivos

- Se cuestionó qué beneficio obtiene el anestesiólogo con este sistema  
- Se reconoció que no hay incentivo claro para los anestesiólogos, lo que explica parte de la resistencia  
- Se sugirió pensar en un proyecto que brinde solución al anestesiólogo a cambio de la información 
### Acción Items

- [ ] Marcos validar internamente el enfoque de proyecto y comunicar resultado  
- [ ] Tommy y Darío refinar la presentación con flujos adicionales, homologación de códigos y vinculación práctica-anestesia    
- [ ] Equipo continuar prueba piloto con Salta y Tierra del Fuego para validar tiempos de carga 


10 códigos en SS

Extras es lo que mas mueve el asunto





proceso, escribir, entiendo, este proceso con la idea de sumar el servicio de anestesia a la validación online, ¿sí? Desde hace, no sé cuántos, tres o cuatro meses largos, un poco por pedido de… de analistas de la empresa, donde hoy es un rubro, el tercer rubro más voluminoso en plata.

Y es en el que menos asertivos somos en cuanto a presupuesto y estimación para saber si estamos o no desviados, cómo venimos. Entonces un poco la necesidad era... qué podemos llegar a hacer para que tengamos información online y en base a eso obviamente tratar de valorizar y ser asertivos en cuanto a lo que refiera.

a información económica, por sobre todo, ¿no? Y es económica por el hecho de que el rubro en sí se audita, pero todo se audita pos-realización, no es previo a la realización. Todas las auditorías que hay de facturación ya son todas posteriores, son prestaciones que hoy por hoy no tienen...

una auditoría o requiere de una generación de formularios previo a alguna realización, ¿sí? Así que bueno, en eso simplemente... Nos pusimos a ver qué es lo que había en el mercado, ya me molé con contactos de proveedores. Nos juntamos con Traditum, nos juntamos con Activia, que son carriers de los más conocidos, y nosotros teníamos contacto con uno que es Ebeweb.

que, de hecho, nos venía pidiendo constantemente seguir sumando prestadores. Así que, bueno, con ellos nos juntamos en su momento. y nos mostraron que, cada uno nos fue mostrando qué sistema tenía y disponía, ¿no? Así que, bueno, nada, fue solo nivelación de saber qué es lo que había en el mercado y respecto a lo que había, qué es lo que nosotros necesitábamos ir ajustando internamente.

Así que bueno, ahí fuimos juntándonos entre nosotros, con contrataciones, con auditoría, con el comité médico, porque hay... faltaban códigos a nuestro entender de lo que hoy hay, de lo que podríamos pretender más como un ideal que es un todo. Esa creación de códigos tenía que ver con que hoy en la anestesia no solo es el código, anestesia como tal es un nomenclador propio.

Sí, los anestesiólogos, si bien cada provincia tiene su propio nomenclador, es un nomenclador propio que para Sancor es una codificación de 10 códigos de complejidades, no mucho más que eso. Pero la anestesia, el gran volumen económico terminan siendo los adicionales, si es feriado, si es geriátrico, si es pediátrico, tiene un extra, un 50, un 75% por sobre el valor de esa complejidad.

Entonces ahí es donde nosotros un poco estábamos en falta de información, por ende, con el doctor Bocco, la doctora Hércoles y el comité. se trabajó en analizar si correspondía o no crear códigos, ¿sí? Los códigos se han creado porque otras preparas ya lo transaccionaban, así que nos servía también.

en cuanto a codificación. Así que bueno, en esos pasos medio administrativos y muy por arriba fuimos avanzando. Así que bueno, y ahí... Darí, presentale, perdón, presentale la presentación que le armaste a Martín. Yo te pasé el link, me parece que como que está bueno ahí resumido y claro lo de anestesia.

La presentación esa que le armamos para Martín, que iba a hablar con el equipo de sistema, lo que Anestesia, yo te pasé ahí por la duración, levantá, me parece que eso está mejor. más claro y refuerza bien la anestesia, esto que vos contabas recién.

¡Bien!

proyectamos algo que muy resumen pero algo que se hizo pero bueno tiene que ver con esto que les vengo contando que es lo que ya hicimos y que es lo que nos faltaría y que es lo que después eso eso que nos falta es lo que nos trajo a esta reunión no bueno el para qué nada no no

Ya lo hablamos, creo que qué beneficio nos trae y no nos trae, tiene que ver con esto que hablamos de datos, de información, y acá es un poco donde, no sé si se ve...

¿Está de 6.000 o las anteriores? Esa, esa, un poquito arriba, dale un poquito más para atrás, un repasito, desde arranca más adelante. por eso estas anteriores una una más está como hay el paraqueda anestesia como como perfecto de que teníamos que nos traía hasta acá no sólo la necesidad del control sino también

estimaciones más de todo de la económica para para información y también para automatizar obviamente el proceso final que es la facturación no que hoy es todo carga manual y mucho papel Eso, eso se ha descontado como todo proceso. Agregábamos dominó por sobre lo que... No, perfecto. Aparte el mal chincho levantó la mano.

No, sí, para entender, porque no sé cómo está hoy el asunto de anestesia y cómo lo estamos gestionando hoy y esa es la primera pregunta. Segunda pregunta, entiendo que los procesos de anestesia, las prestaciones de anestesia, van asociadas a otra prestación habitualmente.

Digo, vos no haces una anestesia... A una cirugía, a una práctica, exacto. Y eso, si eso se registra y cómo... Y lo otro, esto que decía Dari de decir, mira, cada provincia o cada colegio tiene su propio nomenclador, nosotros teníamos unos 10 códigos y ahora resulta que creamos estos nuevos y qué sé yo, para poder avanzar. Eso está aceptado por...

los colegios y demás, ¿está charlado o no? Sí, sí, sí, con cada colegio está tincho en lo que es anestesia un poco, ahí capaz que Darío lo comentó hace un ratito. El servicio de anestesia es un servicio que está vinculado a una práctica, a una cirugía, a una prestación.

La anestesia depende de cada colegio, cada uno tiene su homologación. y nos envía y nos enteramos todo cuando factura y demás, posterior a cierre de mes y demás. Como es un servicio que nos mueve lo que es la facturación, principalmente para decirle el cuarto rubro más... Sí, Pablo.

El cuarto servicio de más volumen, de facturación en costo, y que nosotros lo recibimos posterior a la autorización, nos enteramos tiempo después. Lo que nosotros tenemos como objetivo, lo que queremos es poder llevarlo al servicio online, poder meter reglas y controles de anestesia y poder tener previsibilidad del gasto.

es como todos los rubros que ya fuimos agregando y sumando en lo que es en el ambulatorio. Anestesia es otro servicio que nos queda. por su mano, por su pie, ¿sí, Paulito? Me diste el pie. Mencionás reglas en anestesia. Bueno, acá hay dos médicos que nos expliquen cómo controlaríamos o meteríamos reglas en anestesia.

Sabiendo que lo van a hacer, el estesiólogo, cargan la fofa una vez finalizada la cirugía, lo que sea, se la dan a la secretaria y la secretaria es quien después se encarga de todo. porque si no, si hoy le vamos a dar, ya lo digo chicos, le vamos a dar el online solo para que autoricen, el impacto va a ser mucho mayor porque donde huelen sangre, estos acá, no les importa nada los anestesiólogos, nos van a facturar y van a querer que le paguemos todo lo que ellos autorizaron.

Por ahí va mi pregunta. El servicio de anestesia, no sé si les llevo a agarrarla, pero vos me encuadres. El servicio de anestesia... Tienen la siguiente situación, hay una valorización si es de lunes a viernes, hay una valorización si es a la mañana, hay una valorización si a la tarde es nocturno, si es fin de semana. Si, si, si, sacando la valorización, no solo le vamos a avisar, todo eso es parte de la regla, eh.

Pero vamos a autorizarlo. Yo lo que digo es... Si corresponde, si. Nosotros hoy no tenemos reglas por porcentaje, para corregirme esta regla, pero no existe. Lo vamos a tener que hacer. Nosotros hacemos una regla que, no sé, le autorizamos el 75% si es diurno, por decirlo así, o si es domingo. ¿Pero se lo vamos a utilizar siempre? Digo, a eso voy yo. Sí, se le autoriza la cirugía, sí, sí.

Bueno, perdón, para tratar de entender lo que dice Pablo, lo planteo de otra manera. ¿Existe la posibilidad de que venga, ponerle que esté todo andando, anestesia online, todo chichobombón, venga un anestesiólogo, cargue algo y nosotros le digamos no?

querido, ¿te lo voy a rechazar? ¿Existe esa posibilidad? No, al momento de autorizar, hoy no. Por eso todo es auditoría posterior, ya hoy aún hay un 57% de auditoría posterior. digo, dadas las características de estos estimados colegas, vamos a ponerlo en esos términos, este, que te cargan, digamos, la

estación una vez realizada incluso. Existe la posibilidad de que yo, Sancor, existe la posibilidad, me refiero a queremos hacer eso, no? Que yo desde Sancor le diga, no, no te autorizo esto por la razón que fuera, no? Digo, por la regla que correspondiera, este, no te lo autorizo.

Digo, no te autorizo esto que me estás cargando porque no corresponde. digamos. Y ahí lo que me parece que es a donde iba Pablo, y si no ayúdame Pablito un poco mejor, es, che, ¿nos van a venir al cuello como locos? Digo, ¿es un autorizador lo que queremos? Digamos, esa es la pregunta.

Mira, es así, ¿no? Hoy cómo funciona, es lo que decía Pablo, ¿no? Hoy el doctor llena los formularios, todo lo deja en la secretaria de la clínica y casi a fin de mes tratan de cargar o de informar o pasan al colegio para que se facture. ¿Cómo te va a hacer?

Como que todo lo que pasó en el mes se dio por autorizado, si ya hay una aplicación, un formulario, una internación, un F4, un F6, digo, la anestesia ya está, ¡va! Lo que queremos hacer con el servicio de tenerlo online es poder dar la información lo más actualizada posible y no al mes vencido. Es decir, hoy lo que nosotros vamos a... Y también una cosa es tener la conectividad de estos que puedan cargar e informar, que va a ser eso principalmente hoy por hoy a donde vamos a la información.

a que vuelquen esto al sistema y tenerlo en un tiempo más corto porque hay colegios que no te lo van a cargar en un momento como una prestación médica que estamos pidiéndose en el momento. Esto te lo van a hacer una vez la secretaria de los bienes, como Pablo recién explicaba.

A nosotros de lado costo efectivo nos sirve que sea así. La única forma que lo vayan haciendo a través de la conectividad es poner un sistema que lo hagan. Sabemos que va a ser diferido, que no lo van a poder hacer en el día como si fuese una práctica.

Esto se está pensando, prueba piloto con salsa y con cierra el fuego para que vayan, por lo menos, tengamos la información los viernes. Ese sería el proceso de la propuesta. La herramienta cuál va a ser... Se va a ver en todos los tiempos. Exacto. No es aplicar reglas.

Que después de ahí deriven y tengamos control, como decía Edari. Los controles vienen posterior, pero la información es que no queremos tenerla a los 60 días de cuándo... Yo creo que... Perdón Marquitos, ya te dejo, te pregunto la última, porque ya te habrán todo arriba.

Yo lo que digo es, nosotros le vamos a estar autorizando siempre al anestesiólogo. Claro, es autorización directa, no vamos a meter un... Claro, después no puede haber auditoría posterior, porque la anestesióloga... Pero Pablo, eso ya ocurre hoy. hoy ya tenés los prestadores que le autorizó la resonancia y después auditoría se las debita. La debita, eso existe. Hoy ya existe, hoy las vitaminas de... Una cosa es el prestador normal, otra cosa somos anestesiólogos.

No, pero es que nos estamos hablando de los... Sí, Palito, venimos charlando con los auditores, con el equipo de analistas, o sea, tranqui, tranqui, re tranqui, que venimos re en tema con los analistas. ¿Está bien? ¿Y hablaron para...? No, no, pero se entiende el planteo, ¿no? Es una cuestión de que después nos perdamos poder. El tema es que hoy el poder ni lo... O sea, hoy casi que ni lo tenés porque hoy te facturan.

este y está sin ningún tipo hasta de control y sumado a eso pavito arba es la asociación uno del país de anestesia de buenos aires sabemos que no se lo vamos a integrar, que nadie lo integró, o sea, llegamos al punto de decirte che, vas a saber, es tan difícil el servicio, el rubro

Y sabemos que lo que estamos planteando es para, si son 24 provincias, son para 23. Porque Arba y la más grande no. Y la más grande. Pero así sea ese 20% que me representa el resto del país, no sirve. No, no, está claro, está bien, pero yo quiero, ya, ya, ya, Marcos Juan, esta es la próxima, ahora te doy la palabra yo, quedate tranquilo, no, pero pará, quiero hacer hincapié en esto, boludo.

porque me parece súper importante. Dos cosas. Una es, por un lado, no vamos a estar autorizando, porque como decía vos, Tom y Dary, es diferido, digamos, la carga. Ergo, no es que, si te autorizo es que lo hagas. Conceptualmente no estamos autorizando.

Punto número uno. Punto número 2, como más allá que conceptualmente no estemos autorizando, le estamos dando el check, el visto bueno, el dale para adelante, en lo que fuera, digamos, cuando me carga la información, que está buenísimo mostrar la información antes, obviamente,

digamos, eso y en particular con los anestesiólogos es un posible riesgo, nada más que eso, lo quiero plantear como un posible riesgo. Marco Juan. No, gracias chicos por darme el espacio primero, la verdad que algunas de las preguntas que me han dado tenían que ver con eso, primero cómo era el proceso, pero lo respondieron de alguna manera, no sé si todos harán lo mismo, pero bueno, entiendo.

de que los anestesistas hacen lo suyo y después recién hacen lo administrativo, que además se lo hace alguien y esto que estaba diciendo Martín, para mí también es importante, no es una autorización, porque no es lo mismo. La lógica de la autorización es que suceda previamente y vos querés decir que sí o que no, digamos. Validación será el nombre, tal vez no autorización, la validación de atención. No, es informe, no sé. Aviso, es un aviso. Aviso, sí. Carga, carga, carga de tareas.

Yo pondría un nombre así muy explícito que diga realmente que se está haciendo y que no nos abra la puerta un quilombo después, ¿no? En ese plan lo digo. Ahí yo tengo una consulta capaz que me dé para abajo, pero para que sea una autorización, ¿no debería estar asignada alguna práctica?

para que realmente cumpla. Bueno, pero por eso, ¿no se podría exigir que esté autorizada la prestación y que después la anestesia acompañe esa prestación y ahí sí vos estás autorizando esa anestesia? para que cumpla la función de autorización, pero no sé cómo son los tiempos, porque son dos personas distintas las que te piden, digamos, esa autorización.

Perdón, porque vos no vas a autorizar una anestesia si no estás autorizando una práctica, ¿o sí? No, porque la práctica va por formulario, la mayoría van todas por formulario, ¿sabes? Tiene que acompañar una prestación, entonces ahí sí, vos deberías tener ese complemento.

Va complementado a una práctica. Y esa información, ¿ahí la tenemos, Tommy? Hoy, digo, como está el proceso hoy, ponele. Sí, pero pasa esto. Vos tenés la del formulario. Después tenés que en el momento de la cirugía puede ser que yo en vez de utilizar, no sé, me autorizaste...

Un módulo tal. Necesité dos de estos. Perdón mi tecnicismo médico es cero, pero el cuadro fue más grande, la persona era más obesa, puse más, puse menos. termino facturando más. Eso es por ahí lo que pasa. Por ahí uno autoriza, según la homologación, según el diagnóstico, según la práctica.

pero después lo que ellos facturan termina puede variar eso ya lo que estén facturados, es lo que se controla y después se puede llegar a evitar o no Por eso no es tan lineal lo que se da como formulario y lo que falta. ¿Pero vos en el formulario no das la cantidad de anestesia? Módulos, te pueden agregar más módulos, creo que es así.

perdón hablaron los dos juntos, no entendí. No se autoriza, no se carga. Por eso, entonces vos independientemente de lo que estás autorizando, después lo que te haga el anestesista te lo enteras en la facturación. Vos acá te lo estarías enterando previo a que te lo facture, pero con la condición de que lo relacione a una prestación, vos después obviamente... Tiene el sistema la vinculación, vos tenés que poner el código 2020...

por decirte, y que ha vinculado el formulario al tratado. No, ellos hablan del formulario, Tommy. Vincularlo al formulario... No, el problema es así. Los formen que están cargados de los convenios de anestesia... No tiene esa vinculación entre el código de la cirugía y cada código de complejidad de anestesia. Solamente está cargado...

El valor, digamos, del módulo de la anestesia y después en los PDF está la vinculación, por así decirlo, sistémicamente no... No, no digo que de todas formas te pueden decir che para esta cirugía va este módulo pero cuando está ahí en la cirugía la anestesióloga te puede decir no, usé este, este y este módulo.

No, está bien, yo entiendo eso, digo, y probablemente, no sé cómo es la tasa de recambio después a partir de lo que vos decís que vas a hacer y lo que terminás haciendo en anestesia, no tengo idea, capaz que es enorme, capaz que bajita, otra discusión.

Lo que digo es… en el plan de entender cuál es la ventaja más allá de tener los datos antes, que es un montonazo, y cómo llamar a este proceso para no incumplir ocurrir en el riesgo de que nos vengan a tocar la puerta los anestesiólogos o los colegios anestesiólogos que como también decía Marquitos... Hoy la competencia le llama validación online. Llamémosle que no le autoriza en línea, pero activa, exacto, otros sistemas...

que están en el mercado por todo esto. Nosotros qué queremos hacer, no es hacer el desarrollo propio. Vamos a ver qué es lo que está en el mercado y es lo que traemos, digamos, por acá. Analizamos tres sistemas. De los tres sistemas, en el de lectividad, lo que le llaman autorización o validación y después que puedan sacar una suerte de pre-licitación o integrar la parte del resumen de facturación al fin de mes.

De los tres sistemas que vimos, Activia lo tiene con Arba, que es de los más grandes, pero no logran hacer que el prestador valide o autorice, como le llamamos nosotros. ellos llegan a hacer hasta la elegibilidad, lo que es la autorización, por qué no, porque esto es una pelea, una apunteada en el colegio, en la asociación.

automotorista, solamente hacen la elegibilidad. El otro prestador que funciona a nivel país o del otro sistema o del proveedor de sistemas... Tecnológico es EVE web, con la que estamos viendo de avanzar y hacer alguna prueba piloto con salta y tierra al fuego, que es mucho más completo en el desarrollo, lo que tiene para cargar la hora, vincular una práctica que es diurna hacia la mañana, hacia la tarde.

Ahí es donde estamos para contarles. Ya hay una selección de prestadores. Mirá, y acá les mostramos, yendo un poquito al caminito, recorrido, a ver lo conceptual de la idea de la Anesthesia Online. Ahí Dari, continúas si querés vos que lo armás tú, ¿verdad? Tomi, yo tengo otra pregunta nomás. Dari, Dari. Ponele que nosotros...

No guardemos una autorización, porque es lo único que hoy podríamos guardar, ¿sí? Hoy nosotros lo único que podríamos guardar es una autorización. Dijimos, che, no, no sería lo conveniente porque nos van a... No van a facturar eso y después se van a agarrar de eso y la auditoria posterior no va a resultar. ¿Cómo se imaginan ustedes que guardemos eso? ¿Y dónde guardar esa...?

pre-facturación, pre-validación, ¿cómo se imaginan ustedes para que después se pueda facturar? No, no estuvo en el radar porque siempre fue por la vía de la autorización tal lo tiene. los tiene nosotros, pero ¿por qué? O al menos yo no lo pensé, porque se pensó en reutilizar lo que ya tenemos. A eso vamos. Insisto.

a lo mejor hay que analizarlo o hay que verlo 100% con auditoría para ver cuánto realmente se factura distinto o generaría algún tipo de ruido y cuánto delimitamos también Yo tengo un problema con la carga de la fórmula que están grabados los convenios para esto ¿Les puedo mostrar una pantalla de un convenio de auditaria?

Bueno, díganme cuando se ve. Ahí se ve. Bien. Estos convenios tienen... Ahí, esto es la Asociación de Anestesia de Misión. Estos convenios tienen una particularidad... Como código del prestador está cada una de las complejidades Y ese código del prestador está cargado tantas veces como el código Sancor esté dentro de esa complejidad Con cada una de las ibuquías

Pero el problema es que hoy, si lo cargan por webservice y solamente te mandan el código de la complejidad, te va a agarrar el primero de Sancor que encuentre. ¿Por qué no tiene un criterio para decir? No entendí eso, perdón, discúlpame Gervan. Puedes decir, a mí me pasa el, no sé, el...

cardiovascular de misión, a mí me pasa un cero ocho cero tres seis, yo lo mampeo a un dieciséis cero uno cincuenta y dos, voy bien hasta ahí. Bueno, obviamente. Por el primero que Ok, y depende obviamente del plan en el que cuesta el que tenga el paciente, etcétera. ¿Y la prestación prestador que me pasa es una artroscopía simple para tu OLED, cualquier articulación? Eso no es un código de cirugía, por eso pregunto. No, no. Ah, a ver.

No, tío. Acá, acá... A ver, estos códigos 16 son... Esos son los 10 códigos de los módulos que tiene Sancor, porque Sancor agrupa en 10 códigos todos, la anestesia en Sancor son 10 códigos. Ah, están involucrados, sí. Son las únicas diez complejidades que tenemos, obviamente, el código de complejidad según la capacidad de la cirugía. Me parece mal, la cirugía solamente está detallada como descripción.

Claro, pero ese código que vos mostrabas, Terba, que es el 080306, que tiene esa descripción artroscopía, obviamente no es el mismo 08 o la misma artroscopía del nomenclador nacional. ¿Por qué? No, no hay ninguna vinculación con nuestro código Sancor de artroscopía en ese nivel.

No, no, no, exacto. Yo no le quería mostrar nada más que eso. las cirugías que hace el prestador y los códigos de anestesia que nosotros le damos para esas cirugías, digamos, y ahí es donde se hace la magia. Claro, pero no hay un mapeo con los códigos de la cirugía, hay un mapeo de complejidad-complejidad, excluyendo el código de la cirugía, y la cirugía solamente está reflejada en esta descripción.

que es una descripción propia de la práctica que se pone a nivel de la carga del convenio o sea que si cargarían ellos, cargarían códigos de complejidad no de la cirugía en sí, para poder identificar el código, autorizar, digamos. de que se autorizan el código de la cirugía en un formulario automáticamente identifique que le corresponde este módulo de anestesia.

Ok, igual entiendo que son dos momentos diferentes, digamos, la actualización de la cirugía y la actualización de la anestesia, Gerba, digo, ¿bien? Sí, pero bueno, yo pensé que esto iba a llevar un poco más adelante eso, que es un problema que siempre tuvimos, digamos, de no haber vinculación. Pensé que iba a suceder algún tipo de vinculación. Yo entiendo esto, lo que digo es, en la realidad, y corríjame por favor si estoy equivocado, lo que pasa es que se pide la autorización de poner la artroscopía simple para actuales de cualquier articulación, independientemente de lo que diga, y una artroscopía de rodilla simple, se pide

Capaz que al mes viene el anestesista que hizo la anestesia de esa cirugía de artroscopia de rodillas simple y dice yo hice una anestesia de complejidad 1 o como se llame o el código que tenga el prestador, no importa, pero a nosotros nos va a terminar convirtiéndose en una anestesia de complejidad 1 a este paciente.

Pero son dos eventos cronológicamente separados. Sí, lo que pasa es que si queremos hacer algún control medio automático de eso, de la forma en que están cargados estos convenios no podríamos hacer, no podremos verificar si tiene una artroscopía real.

para poder saber si realmente estuvo bien que la autoriza en una anestesia de complejidad 3. Ese sería el problema, no podríamos hacer un match automático. La primera pregunta fue esa, decir, che, ¿las anestesias están vinculadas a las prácticas que las originan o no?

Por lo que vos estás contando, pareciera que no. No, están vinculadas a las complejidades. Es complejidad contra complejidad, digamos. Y le ponen acá la descripción en la homologación, pero... ¿Y ese papeo está a nivel de convenio? O sea que no habría una chance de hacer una detección automática de saber si tiene autorizada la cirugía equivalente o la prestación equivalente a la complejidad que usted está autorizando.

Excepto que se haga a mano, evidente. Claro. Bueno, es algo para laburar, pero me pensé que no tenía que... Era eso, como para que quede... a nivel de convenio. No, perfecto. Me parece que es algo súper interesante para trabajar, pero que no...

de la autorización online de anestesia, ¿no? Ahí yo me quedé con unas cosas, pero vos dijiste, bueno, fuimos a buscar las opciones. Estaba lo de Activia, lo de Triditum, lo de. la otra no me acuerdo cómo se llama, ebweb o algo así, el autorizador que tenemos nosotros ahora, el nuestro digamos, el común, no podría contemplar este caso también?

Digo, como para agregar un caso más de uso que fuera el de las anestesias. 20-30. ¿Eh? 20-30. Si quieren que agreguemos datos. 20-26, boludo. No, 20-30. Ah, son capos. Yo te firmo. ¿Dónde firmo? No, pero está bien. Perdón, ahora te he interrumpido yo, pero... Me parece bien, Marcos. Adelante.

Siguiendo la línea de cómo se viene manejando IT y también la experiencia ¿Me suena a esto que es un proyecto, Tomás, y hay que plantearlo a ese nivel? para que tenga su presupuesto, sus recursos asignados y después la definición final, si es un evolutivo de un producto interno o no, será algo que se tomará en conjunto con IT también.

Veo porque no hay nadie puro de ese equipo acá. Esa es la bajada y es lo que se está pidiendo de cómo procedamos. Así que, si es 20-30 o si es 20-26, va a depender de... de lo que se charle digamos y lo que se defina ese nivel y se destinarán los recursos y por ejemplo quiere que sea un desarrollo interno se destinarán los recursos necesarios para que eso suceda si es que el objetivo de Sancon es que sea 2026

¿Será para el 2026? ¿Será el proyecto? Me suena muy bien Marcos, me parece perfecto. Ahí este punto de validación de si es proyecto, lo seguimos operando en una mesa más chica, operativa. ¿Vos no lo llevarías para validar? ¿Querés que hagamos otra instancia y lo veamos? ¿O cómo te parece mejor tener esa... Estoy bastante convencido de que tiene que ir por ese canal, pero lo valío y les escribo hoy o mañana.

Y bueno, este tema de Anestesia Online estaba metido, viste Marquitos, el paquete ese que íbamos a tener una reunión con... Mati Villeta, para mostrarle todas las necesidades de proyectos de transformación digital de la gerencia estratégica y que se yo, uno de los proyectos es este. Está en ese radar, independientemente de cómo lo quieras gestionar, te lo tiro para para tu acervo de conocimiento.

No, digo, porque si no nos sesgamos de vuelta, ¿no? Como que la solución rápida... es ir a buscar afuera, y no necesariamente tiene que ser así Se está realizando de esta manera Suncor, y creo que si va por ese camino y se decide que sea un proyecto y que avance

va a seguir el curso que tenga que seguir con el presupuesto de vuelta asignado y los recursos asignados para que suceda lo que nos pongamos como objetivo.

Tal cual, comparto, me suena muy bien. Genial. Boa, ahí Marco avísame, carlalo internamente, nivelalo para arriba, si necesitamos que armemos un espacio puntual y que sumemos gente que no esté acá para terminar de definir esto nosotros igual ahí con Dario vamos a ir trabajando un poquito más la presentación para traer la parte del contenido, creo que había un módulo de...

Auditoría y facturación que tiene BWM Sistema, creo, ¿no? No sé si es uno. Agregarle unos pequeños flujos más para entender, para extrair. Y nosotros se los contamos hoy en lo que veo cómo lo hacemos y cómo lo haríamos que esté bueno. Lo entendieron, pero estaría bueno reforzarlo con 2, 3 flujos ahí también.

Vamos a seguir trabajando en esa presentación. Ahí, en eso, si querés que volvamos a presentarlo y mostrarlo a alguien y cargarlo y validarlo, avísame, hermano. Estamos con Dario Rubén ahí. Atentos. Bueno, quedamos entonces atentos a eso, Marco. Me parece bien que así sea.

Yo les escribo dentro de hoy o mañana. Bueno, ¿alguna consulta o duda más, chicos? No, yo, yo, yo. A mí me quedó una duda, perdón. Cualquiera que consulta con los netos que lo ha hecho. Eso, eso que vos estás mencionando, que facturan un montón, pero de poder implementar este control, este aviso, no abarcaría la totalidad de los anestesiólogos, sino un 20% dijiste. Entiendo que sí, lo venimos analizando del año pasado, pero entiendo que era un 20%, sí, un 80% de la facturación, ¿no?

representación de facturación y que va al rubro de los cien mil millones de sanco del rubro

No, por eso, eso es lo que no sé de Luis y qué pregunta, si del rubro o del facturado. No, no, no. Me quedó la misma duda, si es un 20% de la facturación de Sancor o de Lohan. Es así, lo paso en limpio por la duda. Esto es lo que yo tengo charlado con Ani, puede ser más o menos, ¿no?

Es, si la factura es 100 pesos de anestesias, el servicio viene 100 pesos a nivel país. 80 le tengo que pagar a Arba, un 20% de la energía es el resto del país. Ese 20% si metemos el resto del país en Arba... O sea que con la que conecté a los 31 colegios de los 32, igual va a representar el delito. Era, claro. ¿Era el de 100 pesos o era 30 pesos?

Bueno, igual mi pregunta venía ahora. ¿Qué valor agregamos nosotros teniendo el dato antes? ¿Qué haríamos? ¿Una auditoría previa a decirle, ahí recién te dejo que me la factures o no? Claro. ¿Qué se busca con eso, digamos? Control. Primero conocer el gasto. Primero conocer el gasto. ¿Pero vos el gasto hoy ya lo tenés? Porque ya lo tenés con la facturación, pero hoy ya lo conocés. ¿Qué te implica a vos? ¿Anestesia?

Solo tiene una organización, nada más.

tiempo y forma, ¿no? No lo tenés en tiempo, pero lo tenés. Sí, sí, yo estoy con vos, Lucina, hasta ahora. Claro, ¿qué buscamos con tener el aviso previo? ¿Qué acción vamos a hacer nosotros para...? ¿Qué queremos? ¿Mejorar el número? ¿Nos están sobrefacturando anestesias que no corresponden? ¿Nos están poniendo una complejidad que no es en comparación a la práctica? ¿Qué buscamos con esto?

Eso es lo que yo no terminé de llevarme, digamos. Automatizar, eliminar papeles y, segundo, ser asertivos en el dato. Pero ser asertivo en el sentido de que hoy vos podés saber cuántas cesáreas tal vez tenés autorizadas. formularios 6, lo que no sabes si es de urgencia, si es fin de semana, si es una obesa, si es un geriátrico, donde tienen que agregarle el 50% más, el ANSI que no sé cuánto, entonces se termina siendo también un poco, no tal vez...

no asertivo, pero te ayuda también. Si vamos, o sea, si el final. Vos hoy tenés la cesárea y fue un feriado porque sea un feriado. No, vos tenés el formulario autorizado. No sabés cuándo fue la cesárea. Te van a enterar a los 60 días cuando la facturen. Bien, pero si hoy te avisan que hoy se la están haciendo a vos, ¿en qué te cambia? ¿A que te avise hoy o a que te la facture después? Porque el importe va a ser el mismo, digamos.

Lo que te va a facturar el anestesiólogo va a ser lo mismo porque fue en un feriado. Sólo que hoy te está avisando que te va a facturar X cantidad de plata. ¿Qué valor aporta a nosotros tener ese aviso antes? A ver, por ejemplo eso, tenemos la re-pregunta, Luis, a ver si lo entendís. Si vos agarré y decís, me da un cheque en blanco, que es el formulario, vos me decís, te dejo, que compré, no se yerba, en cualquier lugar, cualquier día.

Vos querés saber cerrar tu caja, vas a poder pagar ese cheque cuando venga. Ahora, si vos sabés que fue hoy, 18 del 12, vos sabés en tu arqueo de tu caja de diciembre si vas a poder pagar todos los cheques que te entraron y aparecieron hoy. de no tenerlo ahora visualizado, te enteras a los 60, a los 90 días. O no, o a los 30. Entonces, es como que no sabes cuándo te termina aca con esa actitud, con mayor precisión.

¿Qué gasto vas a tener en diciembre? ¿Qué gasto te va a caer en enero? ¿Qué gasto te va a caer en febrero?

Los dejo a los chicos a ver si ayudan o aclaren un poco esto. A mí me queda ese vacío, como que no termino de entender. Lo veo como un... A lo mejor es un desarrollo que va a necesitar esfuerzo y no termino de entender para qué. Sí, no, mi otra pregunta era cómo tenemos garantías de que efectivamente porque tengan la herramienta lo van a hacer en el momento que nosotros pensamos.

No, no, por eso... Hoy estamos probando... Por eso también hay cuando hablaba del proyecto, Marco. Hoy nosotros Ebweb lo tenemos como proveedor. Y hoy estamos probando, haciendo una prueba piloto en dos provincias. Estamos yendo a terminar de pulir con los datos y los ajustes que tenemos que mostrar a nadie en una de las slides.

los ajustes para tener el dato de la hora y otro dato más. Ya lo estamos haciendo y queremos ver si en el circuito con estas provincias funciona que hagan esto que yo te decía. No lo hacen en el momento, lo hacen diferido, pero diferido a una semana, por ejemplo.

y que esa información nosotros podamos tener, y poder evaluar y decir, che, con Salta pude tener tanta información del 100% con antelación, en el curso y demás. Queremos ver esto si es viable o no. tomando estas provincias como muestra que se lo puede aplicar con este proveedor hay otras provincias, casi todo el interior va con el web, por decirte de 24 sitios, provincias, punto 23

21 tiene Ebeweb, con 2 está conectando a Suncor, pero Ebeweb ya tiene estos círculos de anestesia para el resto del país, una gran cantidad de provincias, lo cual hasta provincias de Buenos Aires creo que viene con Ebeweb. Pensar en la escalabilidad que era uno de los puntos que decíamos, pensar en los ajustes y demás. Es probable que, vamos a nuestro entendimiento y lo que estamos proyectando es que con Ebweb...

puedan lograr que tener la información para lo que es todo el país, menos para Conarva, que es una cuestión más política. Y hoy probar con salta y cierra el fuego para ver si el circuito funciona, si lo cargan en el tiempo como esperado. que nos sirva.

Está buenísimo. Chico, se acaban las preguntas, chico. Una más todo y chao. Una más, cerremos, generalicemos, y ya estamos por abrir. hay una propuesta. Me parece bárbaro lo que decías de B-Web, eso está buenísimo porque ya está como ese camino llanado, digamos, y lo que decía Marquitos, que es súper atinente, digo, ya está, cocinado, o semicocinado. Ahora, a mí me tengo una sensación, creo, similar a Luisina, voy a interpretar las palabras de Luisina, a ver si vamos por ese lado, pero digo, a mí me parece que, como digo, tengo la sensación como que nos quedamos cortos, digo, y entiéndanme, digo,

me parece que podríamos hacer como algo más, independientemente del quilombo con arba y toda esa historia, pero digo, por ejemplo, y esto que presentó Gerba, la posibilidad de que una prestación tipo cirugía, digamos, no tenga una anestesia es relativamente bajada, casi nula para algunos casos, por ejemplo, un trasplante de corazón no se puede hacer sin anestesia.

no sé, una sutura de una lesión de piel puede ser, pero en general todas llevarán anestesia. R2, ahí yo ya tengo un driver y un indicador bastante pesado de, no es, yo voy a me voy a encontrar con un consumo dentro de 60-90 días cuando me lo factura el anestesista. Yo sé que voy a tener un consumo dentro de lo que sea, con los tiempos que sea, porque acaba de producirse el consumo padre o madre, no sé qué género tienen, de esa prestación que es la cirugía.

Entonces ahí yo podría de alguna manera usar de proxy. las intervenciones quirúrgicas para acercarme un poco más a las anestesias. Como cosa complementaria, no digo hacer esto en lugar de, no, digo como cuestión complementaria, es decir, che, mirá, también tengo esto, digamos, a ver cómo lo podemos enganchar para tener un poco más de información.

Y después Eso es una sugerencia, digo, simplemente. Y lo otro es, a mí me queda la sensación de, como a poco en el sentido de, independientemente de que, como decías vos, Tommy, EveWeb ya tiene hecha la entrada con los colegios y qué sé yo, de vuelta, somos anchor, ¿viste?

Digo, también podemos ir a charlar con los colegios y abrir esa puerta y decirle, che, usen mi sistema de autorización que ya utilizan los prestadores. Porque los anestesistas, en general, sino que están dentro de una, de un creador o de una, como es que le dicen ustedes, cuando agarran a varios, una colectora, una contenedora, gracias, una contenedora.

probablemente esa contenedora, ese acreedor, ese lo que fuera, esa institución ya utiliza los servicios de autorización de SancorWeb, de SancorSalud. Entonces, digamos, sería simplemente, digo, lo digo así muy sueltito de cuerpo, probablemente no sea tan simple, pero sería tan simple como decir, bueno, esto que usas, esta herramienta que estás utilizando para el resto de las prestaciones, agregale también lo de los anestesistas, informámelo vos.

Yo después me arreglo con los anestesistas para facturar, pero vos informame que se regresó una cirugía y que el tipo de anestesia se regresó a la cirugía. parte es parte del protocolo quirúrgico como documento clínico, es decir, che mira se hizo una cirugía de apéndices, qué anestesia se hizo, no sé, una potenciada de tales características, yo sé qué cirugía, qué anestesia se hizo, ergo sé qué complejidad, ergo sé cuánto van a cobrar, porque sé a qué hora se hizo, si el paciente era joven, viejo, etcétera, etcétera, entonces ahí tengo un montón de información que podríamos complementariamente

estratégicamente nos conviene ir a buscar un proveedor externo o pensar en incorporar anestesia como una como un nomenclador más digamos adentro del autorizador que tenemos actualmente cambio Yo voy a hacer otra cosa. Una sola y para irnos. ¿Qué beneficio le damos al anestesiólogo con esto?



¿Por qué? A ver, ¿por qué no podemos entrar en ARBA? ¿Por qué el 80% dice no, no quiero sacar? Porque no le damos nada. O sea, nosotros pretendemos que ellos nos hagan todo. No, y aparte porque la mafia no centra, así que hay que ir de otra manera. Claro, porque no pensamos en la anestesia. Ahí tenés que, es como... Me pasa, ¿no? Presentó un proyecto que le demos solución a la anestesiólogo

y que él, con la solución que nosotros le damos, nos dé la información. Está bueno desde la idea, estaba muy guay Pablo, después nos fuimos enterando y comprendiendo que no es muy claro. No sé cómo explicarte y ponerte en palabras. Yo, digamos, tengo de André Arbas un poco de información, pero por ahí que vos puedas relevar y buscar por tu lado.

está bueno porque no es por lo que intentamos nosotros dijimos lo mismo un proyecto escuchar actividad ya tiene elegibilidad que hagan un pasito más yo quería solamente tradicional porque la decisión no es el tradicional médico y no es la herramienta es algo político pablo no es pensemos en el proyecto y les llevo el proyecto y por más bonito que sea tratar de decir que sí

Hay algo político... Porque está teniendo tensión lo mal, Tommy. Mirá lo que dijo Consolar. Mirá lo que te voy a decir y con esto yo tengo que que vos lo indagues, por tu lado. Nosotros de ofrecerle un sistema, por ahí hablamos en un momento, che, si esto en vez de comprar un tercero les llevo dos, un sistema hermoso, y que le traiga mucho beneficio al anestesiólogo.

Arva no te agarra ningún servicio, ningún sistema, ningún sistema, que no sea el que ellos manejan. Es como un web-service. ¿Cuál es el fin que vos le querés dar a Arva? ¿Controlarlo? Escucha, al italiano, anda a llevarle un sistema. Te dicen, este es mi sistema.

¿Con qué fin? Digo, vos no importa, lo que vos yo te digo es que no le vas a poder llevar un sistema. si lo podés hacer, buenísimo, enhorabuena. Arba no te va a agarrar un sistema que no sea el primero quiera y tenga algún interés. No va a haber algo que es sanco para mí, no lo hizo 2B, no lo puede hacer 2B, podría ser que seamos los disruptivos.

que hagan lo que queremos que hagan en el online. A Ode no lo puede hacer. Compa, eso yo creo que entienda. Creo que ahí está el problema. Hay que pensar algo distinto, no esperar que hagan lo mismo que hacen los demás portadores en el online, que yo quiero. Yo digo, che, vamos con Arba. A ver, tenemos esta necesidad. Necesitamos conocer y tener datos en línea, datos fiables. No te voy a controlar, necesitamos trabajar en conjunto, no sé, vamos a...

desarrollar... Todo eso, todo ese planteo, queremos que lo hicimos, pero igual está bueno que vuelvan a indagarnos, y lo podemos, obviamente. Ya fuimos por todo eso. Pero terminamos llegando siempre a lo mismo. Hacer un validador para que no... O sea, indagamos, indagamos, pero terminamos en lo mismo que tenemos siempre.

Son políticos, yo no sé con qué argumento explicarte para ir de lo que en mi criollo básico es político y por más que vos les quieras hacer todo trabajo, todo colaborativo, todo constructivo... con beneficio para ellos, entiendo que hay algo político, y ahí es donde yo no tengo tan de modos para decirte, mira, no lo van a hacer por esto, por esto, por esto, y que vos digas así. Por eso digo, capaz que vos puedas buscar por tu lado y a ver qué encontramos.

La idea de ir con algo novedoso, distinto, a lo que hace el otro, bla, bla, bla... Intentamos, créeme, que no vimos opción. Si la encontramos, buenísimo. Perdón, te piso un segundo, Gerba, pero es un comentario muy ingenuo el mío. Por ahí ninguno de nosotros estamos a nivel de ir a tener esa discusión, ¿no? ¿Hay alguien que ante una propuesta diferente pueda apoyarnos? No sé.

Perdón, soy una boludez, ¿eh? Pero, no sé, Fernando que puede ir a traccionar algo así, no sé, si somos nosotros los que vamos a poner la cara, yo creo que... Hola, sí, Tomás, te llamás, bueno, qué bueno. Excelente. Ahora, perdón, a ver ejemplos, Tommy, eh, si querés. No. Incluso a mí, no tiene problema. No, no, no, se entiende, se entiende. Pero digo... Hasta con Inés, hasta con Gerente fuimos.

Hasta con Jerente se habló y se gestionó tiempo atrás, y se viene gestionando esto, capaz que tenga aquí como la figura, o sea, ¿sí? Tomando lo que dice Pablo, de tratar de hacer algo diferente, por lo menos intentarlo ser disruptivos, por ahí el que tiene que tener esa bandera sea...

estoy dando trabajo, me van a mandar a friturro, pero que se yo, no sé, es una respuesta el chico, digo, entiendo que es difícil, nosotros seguro que no tenemos el peso para ir a cambiar eso, bueno, si es algo de interés para Zancor, por ahí alguien más.

arriba nuestro, más arriba del gerente, puede ir a traicionarlo, no sé. Con esto me callo y lo dejo Germán, que va a decir algo sobre lo más interesante. Eso seguro. No, yo, no, yo... A ver, lo único, si llegara a darse alguna integración, tal vez exista la chance de que saquemos algún beneficio de un...

de que además de cargar la complejidad de anestesia, carguen la cirugía, el código de sangre, elijan la cirugía con la cual hicieron esa anestesia de una lista de anestesia, de cirugía de práctica, cosa de que podamos crear esa... porque ahí estaríamos metiendo un nuevo dato en la empresa que sería provechoso y que hoy no existe, que es la vinculación entre la cirugía y la anestesia. Si te lo podés declarar...

Se crea una nueva lógica de datos que vincule tal formulario con tal práctica, quizá va a tener el nivel actual que es el de la complejidad de la anestesia, y va a tener una vinculación nueva con... a cirugía o lo que sea. Son dos debates a replantear porque como, o sea, con quien hables te va a decir el anestesiólogo no conoce del código médico del nomenclador nacional porque sólo maneja su propio nomenclador

que es más agrupado, más acotado, pero te agrupa ciertas prestaciones y te va a decir que ellos no tienen contacto con la parte administrativa de la clínica que es la que gestiona el formulario 6 de la internación o el formulario 4 de la internación breve y que ellos no se dedican como a esas tareas administrativas ni tienen secretarias.

Eso es más o menos lo administrativo. Lo que sí tiene que ocurrir es un poco, a lo mejor es esto, el cambio de peso que tengamos que hacer eso disruptivo y poner las medidas que nosotros pagamos. clínico que es el protocolo quirúrgico que es obligatorio para cualquier cirugía y en ese documento dice que la anestesia se hizo por protocolo dice. No, no, no, no, eso sí Martín, eso sí se puede. No, el tema lo que dice Gerba es que si realmente se hizo una artroscopía y el código del nomenclador o el número de formulario 6...

que autoriza esa prestación, SX, sea también cargado para lograr obviamente ese traqueo o ese punta a punta en todo. Para darle ese beneficio, que ya que se va a hacer, si se puede hacer online... Pero bueno, será la parte del proyecto de lo que haya que pedir o ver.

para la razón final que pueda tener. Hoy, hasta ahora lo que te dicen es que lo cargan todo posterior, ¿por qué? Porque es así, o la modalidad de trabajo, o porque así lo vienen haciendo, o porque así se maneja. Sí, pero bueno, no quita que haya que cambiarlo, cada uno tendrá algún contacto al que le pueda preguntar.

si en el momento que está dentro del quirófano puede ir cargando, haciendo, pidiendo información que sirva, ¿no?

da para debate, está bueno. Bueno chicos, queda un minuto, me tengo que ir a otra. Marco Buabisano, nosotros seguimos puliendo con todo esto, escribimos bien el adjetivo, lo que nos dijo Luis en el internet, para qué, vamos a agregarle flujo, vamos a agregarle el tema de homologación de los códigos, por qué cuesta o entender la vinculación entre la práctica y la anestesia.

Vamos a ir puliendo esto para que quede súper, súper completo, porque hoy todo lo que surgió me da, esta pregunta que me hizo Pablito, nos mató a preguntas, nos sirve para poder retroalimentar la presentación, el por qué, el para qué, y qué queremos hacer, y lo que estamos haciendo, y si todos están de acuerdo, bueno, como el mejor camino de llevarlo adelante. Así que voy a avisar, Juanito, cualquier cosa.

Sí, quedamos atentos. Gracias, chicos. Que termine lindo el día. Adiós, adiós, chau, chau.

¿Quiénes son los tres acá? ¡Ah, mirá! ¡Qué bárbaro! ¿Cómo están? Bien, ¿ustedes? ¿Cómo están, Marquito? No, boludo. Para mí hay que repensarlo esto, eh. No hay que presentarlo así. Para mí.

Va a estar difícil.

