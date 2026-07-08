---
source_url: https://app.notion.com/p/2d52c02ab01980bfb6adc95ef44e88c0
ingested: 2026-07-08
title: Coseguros
notion_id: 2d52c02a-b019-80bf-b6ad-c95ef44e88c0
---

▶ **20251226**

<!-- unknown block type: transcription (2d52c02a...) -->



### Situación Actual y Puntos de Dolor

- Existen desajustes significativos en el circuito del proceso de liquidación de coseguros que impactan negativamente en la facturación para Suncor y el asociado 
- **Coseguro**: Costo adicional que llega al asociado en la factura de liquidación 
- **Copago**: Monto que se paga al prestador en el momento de la atención
- Múltiples áreas intervienen en el proceso actual: lista de precios, parametrización, verificación y distribución  
- El proceso involucra generación según consumo, autorizador, reintegro de peso, liquidación provisoria con controles manuales, y liquidación final 
### Herramientas Actuales

- Google y AS400 para configuración y parametrización 
- Sheets para controles
- Fluir para controles de valor y alertas de diferencias
- Tableros de liquidaciones
### Problemas Identificados

- **Cálculos descentralizados**: Existen diferentes cálculos en autorizador, reintegros y ADP 
- **Duplicidad**: Ingresos duplicados en el proceso 
- **Controles manuales**: Dependencia de personas específicas con riesgo de errores 
- **Dependencia de AS400**: Proceso tedioso y manual 
- **Falta de integridad**: Necesidad de asegurar unicidad y completitud de órdenes 
- **Ausencia de marcas**: Falta de criterios claros 
- **Rechazos**: Liquidación de coseguros en prácticas rechazadas cuando no corresponde 
- **Falta de claridad**: Conceptos de liquidaciones no estandarizados 
- **Parámetros faltantes**: Necesidad de parametrización más flexible 
- **Múltiples áreas involucradas**: Aumenta el margen de error 
### Solución Propuesta

- **Unificación de cálculos**: Centralizar cálculo de autorizador, reintegros y ADP en uno solo  
- **Controles del autorizador**: Los controles que hoy se vuelcan al autorizador serán absorbidos y mejorados en el nuevo sistema  
- **Rediseño de procesos**: Para dividir y reducir duplicidad
- **ABM de parametrización**: Configuración de tipos de coseguros, listas, valores sin necesidad de scripts en AS400 
- **Controles automáticos**: Reducir dependencia de controles manuales 
- **Mejora de marcas y rechazos**: Implementar nuevos criterios
- **Estandarización de conceptos**: Mejorar claridad en liquidaciones
### Alcance del Proyecto

**Incluye**:

- ABM de parametrización (actualmente manual desde AS400) 
- Cálculo unificado de autorizador, reintegros y ADP 
- Controles automáticos y reportes 
**No incluye**:

- Correcciones de bugs en el sistema actual (aunque se participa en las mesas de trabajo)  
- Cálculo de copago 
### Roadmap y Timeline

- **Septiembre**: Inicio de configuración 
- **Actual (Sprint 4)**: Finaliza el 29, trabajando en el último ABM de parametrización  
- **Sprint 5**: Testing de los 4 ABMs (tipo de coseguro, lista de precios, valores, y asignación de nomencladores)  
- **Febrero**: Entregable parcial de parametrizaciones para que el equipo de Adri, Sofi y Jime trabajen sin AS400  
- **Febrero**: Reingeniería del cálculo de coseguro unificado 
- **Mediados de marzo**: Servicio para medicamentos - mejora del proceso para calcular en el momento de dispensa en lugar de 2 meses después   
- **Marzo-Abril**: Integración con autorizador, ADP y reintegro 
- **Abril-Mayo**: Controles automáticos 
- **Principios de Mayo**: Pruebas de regresión, seguridad y performance para puesta en productivo 
### Medicamentos - Mejora Propuesta

- El cálculo actual de coseguro de medicamentos no es erróneo y funciona correctamente  
- Se propone mejorar el proceso para calcular en el momento de la dispensa en farmacia en lugar de 2 meses después 
- Objetivo: Reducir coseguros no cobrados por bajas de asociados entre la dispensa y la liquidación 
### Equipo del Proyecto

**Proceso y Riesgo**: Sol Smitl/Smitlen, Cristian Gauna, Belén Regiscioli (sponsor), Uriel Nicola (sponsor), Eugenio, Seba Treñier, Mauro Estorero  

**Equipo Técnico**:

- Líder técnico: Kevin 
- Dev backend: Mariano Goyanechea 
- Dev frontend: Rami Mouroua 
- CUA: No necesario por ahora, testing con equipo de Adri  
**Liderazgo**:

- Líder del proyecto: Tomás Muñoz 
- PO: Joaquín Amedijeira 
- Scrum: Franco Rimoldi 
- Soporte: Darío Gürtel 
### Stakeholders

**Directos**: Liquidación de asociados, experiencias de asociados, gestión administrativa de salud, afiliaciones, inteligencia competitiva, ADP, cadena de valor de asociados, operaciones individuales, operaciones de línea empresa  

**Indirectos**: Legales, reintegros, auditoría de copagos, autorizaciones, contrataciones, conectividad, riesgos 

### Objetivos

- Liquidación espontánea en cualquier momento del periodo o mes 
- Proceso simple y automático 
- Sistema escalable para nuevas propuestas y alternativas 
- Modernización para eliminar dependencia de AS400 
### Próximos Pasos

- Finalización del Sprint 4 el lunes 29 con último ABM 
- Sprint 5: Testing de los 4 ABMs de parametrización 
- Reuniones mensuales con toda la mesa para presentar avances 
- Reuniones puntuales cada 15 días si se necesitan validaciones específicas 
- Compartir presentación por mail para consultas 
### Acción Items

- [ ] Completar último ABM de parametrización (finaliza 29) 
- [ ] Testing de los 4 ABMs en Sprint 5 
- [ ] Entregar parametrizaciones para que Adri, Sofi y Jime puedan trabajar sin AS400 (febrero)  
- [ ] Programar reuniones mensuales de avances 
- [ ] Enviar presentación por mail al equipo 
### Agradecimientos

El equipo agradece especialmente la colaboración y disponibilidad de todos los sectores involucrados (ADP, equipo de Cris, Sol) por su respuesta positiva y apoyo continuo en las múltiples reuniones necesarias para levantar información del proceso actual  



### Situación Actual y Puntos de Dolor

- El principal problema son los desajustes en el circuito del proceso de liquidación de coseguros, que impactan negativamente en la facturación tanto para Suncor como para los asociados 
- **Diferenciación de conceptos**: Coseguro es un costo adicional que llega al asociado en la factura de liquidación, mientras que copago es un monto que se paga al prestador en el momento de la atención 
- **Proceso actual involucra múltiples áreas**: Lista de precios (inteligencia competitiva), parametrización y distribución (administración de salud), generación según consumo (autorizador, reintegro, ADP), liquidación provisoria y final, y controles manuales   
- **Herramientas utilizadas actualmente**: Google, AS400 para configuración/parametrización, sheets para controles, Fluir para controles de valor y alertas 
### Problemas Identificados

- **Múltiples cálculos separados**: Existen cálculos distintos en autorizador, reintegros y ADP que necesitan ser unificados 
- **Duplicidad de ingresos**: Se requiere rediseñar el proceso para evitar duplicidades 
- **Controles manuales**: Estos están sujetos a error humano y dependen de pocas personas 
- **Dependencia de AS400**: Se necesita crear ABMs para configurar tipos de coseguros, listas, valores, etc. 
- **Falta de integridad**: Se debe asegurar la unicidad y completitud de las órdenes 
- **Ausencia de marcas y rechazo**: Algunas prácticas rechazadas se están liquidando incorrectamente 
- **Falta de claridad**: Los conceptos de liquidaciones necesitan estandarización 
- **Parámetros faltantes**: Se requiere parametrización más flexible 
- **Múltiples áreas involucradas**: La cantidad de áreas que intervienen aumenta el riesgo de error 
### Solución Propuesta

- **Análisis de reglas de negocio** mediante mesas de trabajo continuas 
- **Unificación de cálculos**: Centralizar los cálculos de autorizador, ADP y reintegros en un solo sistema  
- **Controles automáticos**: Los controles que hoy se vuelcan al autorizador serán absorbidos por el nuevo sistema  
- **ABM de parametrización**: Crear interfaz para que el equipo de administración de salud configure sin usar AS400 
- **Rediseño del proceso**: Proponer un proceso nuevo con unificación de cálculos 
- **Desarrollo de nuevo sistema**: Implementar una solución moderna que reemplace las "pantallitas negras con verde" de AS400 
### Objetivos del Proyecto

- **Liquidación espontánea**: Poder liquidar en cualquier momento del período/mes 
- **Simplicidad y automatización**: Cálculo y liquidación automáticos 
- **Escalabilidad**: Poder aplicar nuevas propuestas y alternativas 
- **Reducir errores**: Minimizar errores en liquidación de coseguros 
### Alcance del Proyecto

**Lo que incluye**:

- ABM de parametrización (actualmente manual en AS400) 
- Cálculo unificado de autorizador, reintegros y ADP 
- Controles automáticos y reportes 
**Lo que NO incluye**:

- Correcciones de bugs en el sistema actual 
- Cálculo de copago 
- Las correcciones que surgen en mesas de trabajo se vuelcan al autorizador y serán contempladas en la reingeniería, pero no son parte del proyecto actual  
### Roadmap y Cronograma

- **Septiembre**: Inicio de configuración 
- **Actual (Sprint 4, finaliza 29 de diciembre)**: Último ABM de parametrización  
- **Sprint 5**: Testing de los cuatro ABMs con equipo de administración de salud  
- ABM de tipo de coseguro
- ABM de lista de precios
- ABM de valores de coseguro
- ABM de asignación de relevamiento (nomenclador, capítulo, subcapítulo)
- **Febrero**: Entregable parcial de parametrización para que el equipo pueda trabajar sin AS400  
- **Febrero**: Reingeniería del cálculo de coseguro unificado 
- **Mediados de marzo**: Servicio para medicamentos/coseguro 
- Actualmente el cálculo de medicamentos no está erróneo, pero hay que mejorar el proceso 
- **Problema identificado**: El cálculo se hace dos meses después de la dispensa, debe hacerse en el momento 
- **Marzo-abril**: Integración con autorizador, ADP y reintegro 
- **Abril-mayo**: Controles automáticos 
- **Principios de mayo**: Pruebas de regresión, seguridad y performance, puesta en productivo 
### Equipo del Proyecto

**Proceso y riesgo**:

- Sol Smitl/Smitlen
- Cristian Gauna
- Sponsor: Belén Regiscioli y Uriel Nicola
- Eugenio, Seba Treñier, Mauro Estorero  
**Equipo técnico**:

- Líder técnico: Kevin
- Dev backend: Mariano Goyanechea
- Dev frontend: Rami Mouroua 
- **Nota**: No se incorporará QA en esta etapa; el testing de ABMs se hará con el equipo de administración de salud (Adri, Sophie, Jime)  
**Liderazgo del proyecto**:

- Líder: Tomás Muñoz
- PO: Joaquín Amedijeira
- Scrum: Franco Rimoldi
- Soporte: Darío Gürtel 
### Stakeholders

**Directos**:

- Liquidación de asociados
- Experiencias de asociados
- Gestión administrativa de salud (parametrización directa) 
- Afiliaciones
- Inteligencia competitiva (listas)
- ADP (cotizador, control, cálculo unificado)
- Cadena de valor de asociados
- Operaciones individuales
- Operaciones de línea empresa  
**Indirectos**:

- Legales, reintegros, auditoría de copagos, autorizaciones, contrataciones, conectividad, riesgos 
### Comentarios y Decisiones

- **Entregables parciales**: Se confirmó la posibilidad de entregar la parametrización en febrero como entregable intermedio, mientras se continúa con el resto del proyecto   
- **Modernización**: Este proyecto busca eliminar la dependencia de AS400 y modernizar el proceso 
- **Valor para el equipo**: El entregable de parametrización agregará valor importante al proceso del equipo de administración de salud 
- **Colaboración entre equipos**: Se destacó la excelente respuesta y colaboración de todos los sectores involucrados (ADP, equipo de Cris, Sol, etc.)  
### Acción Items

- [ ] Realizar reuniones mensuales con toda la mesa para presentar avances 
- [ ] Realizar mesas puntuales cada 15 días con sectores específicos para validaciones según necesidad 
- [x] Tomás/Joaquín: Compartir presentación por mail 
- [ ] Equipo técnico: Completar Sprint 4 (último ABM) para el 29 de diciembre 
- [ ] Equipo: Realizar testing de los cuatro ABMs con Adri, Sophie y Jime en Sprint 5  
- [ ] Equipo: Preparar entregable parcial de parametrización para febrero 






¿Dónde estamos hoy? ¿Cuál es el principal punto de dolores? Como todos lo conocerán, porque son todas personas que ya están involucradas en este proceso, tenemos los desajustes en lo que es el circuito del proceso de liquidación de los poseguros, que esto luego impacta...

altamente y negativamente en lo que es la facturación para Suncor y también para el asociado dejar a ellos. Hacer un poquito de diferenciación de lo que es Coseguro y lo que es Copao si bien todos lo deberíamos estar conociendo, pero bueno, lo que es el Coseguro es un costo adicional que le llega al asociado.

en la factura de su liquidación, y el copago que es un valor, un monto que se le paga al prestador en el momento de la atención, se lo paga al asociado, ¿sí? Lo que es el proceso o el soporte actual, acá se puede observar que hay varias áreas que intervienen en todo el proceso en sí.

las distintas etapas que tenemos, lo que es lista de precios, lo que es parametrización, lo que es la verificación y distribución que está con la gente, bueno, inteligencia competitiva con la lista de precios, administración de salud con lo que es la parametrización.

y con lo que es la distribución. Después seguimos con lo que es la generación de según el consumo. Acá tenemos el autorizador, reintegro de peso, los distintos ejes que tenemos hoy para esos cálculos. Una liquidación provisoria, sí, que la arma de liquidación es con sus archivos y demás, esa liquidación después también la controla la gente de administración de salud y le pasa conectividad para que podamos hacer manualmente desde ese sector los ajustes que correspondan, según más gente pueda llegar a tener algún asociado y demás, entre otros.

controles. Eso retoma a la gente de liquidaciones ya con la actualización de los controles manuales, se hace la liquidación final y posteriormente... Eso está el control de las cantidades y los valores que lo hace también el sector de... Bueno, un poquito las herramientas que se están usando, lo que es el Google, lo que es el AS400 para lo que es la configuración, parametrización, los sheets que se están utilizando para todos los controles también que se...

que se realizan, lo que es fluir para ver la parte de los controles de valor y los alertas de diferencias que se le envía Conectividad, y bueno, la parte de liquidaciones con tableros y demás. Lo que es el resultado del relevamiento, bueno acá tenemos un resultado de cómo es todo el relevamiento de todo el circuito que se hace hoy, lo que es el disparador, lo que son las reglas, el ingreso que es el cálculo en sí, los reportes, las actuaciones y facturación.

¿Quiénes son los disparadores? Bueno, los consumos que hay, las listas de precios vigentes, las líneas de planes, las grillas. Eso corre por ciertas reglas, que hoy están en los distintos controles que se hacen dentro del autorizador de ADP y de reintero.

Se genera ese cálculo en esos tres sectores que mencioné anteriormente, se hace un reporte, pues son los controles que hoy se vienen haciendo semanalmente en una mesa de trabajo, que la verdad es que es sumamente importante esto porque son controles que se van volcando al autorizador para hacer esos controles y evitar errores.

y eso después lo vamos a terminar tomando, absorbiendo nosotros cuando hagamos la unificación de ese cálculo, así que ahí está bueno resaltar que son súper válidos estos controles hoy día. la liquidación, que, bueno, es el ingreso al sistema de liquidación en sí, y la facturación que le llega de nuevo al asociado. En lo que son las épicas, acá podemos mostrar un poquito lo que son los...

En la parte superior, lo que son los problemas, cuáles son los puntos de dolor que hoy tenemos o las situaciones que se están presentando y cómo querríamos o cómo la vamos a abordar nosotros, en la línea de abajo donde está la manito. Por un lado tenemos diferentes cálculos, acá lo que vamos a hacer es unificar lo que es el cálculo de autorizador, lo que es el cálculo de reintegros y de ADP, acá lo vamos a centralizar todo en uno.

Acá es donde yo mencionaba recién lo de los controles que se vuelcan al autorizador. Ese es el control, el cálculo que nosotros vamos a utilizar y que vamos a buscar mejorar y centralizar tanto ADP y reintegro en este mismo. Bueno, la duplicidad, los ingresos duplicados, la idea es poder rediseñar ese proceso para que se dividan esos, por la mayor capacidad de duplicidad.

Controles manuales, que hoy lamentablemente el control manual está sujeto a una persona, dos o cinco las que sean, y cierto riesgo hay de poder hacer algún control erróneo. La independencia de Haití, que acá lo que vamos a buscar hacer es este ABM, con el cual se van a configurar todos los tipos de ecoseguros, sus listas, valor y demás. Y bueno, la falta de integridad, que es con lo que vamos a buscar asegurar la unicidad y completitud de las órdenes.

Algunos otros puntos que son de dolor también es buscar mejorar las ausencias de marcas que hoy tenemos, implementando criterios nuevos. presencia de rechazo, acá hacemos mención a los rechazos que hoy se dan en un formulario, que son tres, cuatro prácticas, algunas de esas prácticas por ahí están rechazadas y hoy día se está liquidando ese Fonseguro también cuando...

cuando no correspondería, la ausencia de claridad, acá se nos menciona un poquito más a lo que son los conceptos de esas liquidaciones de ecoseguro, poder estandarizarlas, poder mejorarlas también. faltantes en los parámetros, bueno, incorporar una parametrización que sea más flexible, funciona a variables que vayamos teniendo o a situaciones que vayan surgiendo, y principalmente esto que se vio antes en la filmina anterior de la cantidad de áreas que hoy intervienen

para poder reducir lo mayor posible el error en lo que es la liquidación de los cosechudos. ¿Cómo lo vamos a lograr? Bueno, lo que se viene haciendo y se está haciendo es analizar las reglas de negocio con las distintas mesas de trabajo que se llevaron a cabo y que se van a seguir llevando a cabo, analizar ese proceso actual para poder mejorarlo.

analizar un software actual, analizar el software que tenemos hoy día para que este control y estos cálculos que se hagan sean lo más seguros posibles, proponer un proceso nuevo que es esta unicidad de una unificación de los distintos cálculos. y desarrollar ese nuevo sistema. Los objetivos, bueno, el objetivo principal es poder tener una liquidación que sea espontánea, que sea en cualquier momento del periodo o del mes en que se requiera.

ya teniendo todas las bases con las informaciones actuales y teniendo todo en el sistema, se podría llegar a liquidar en cualquier momento, que sea simple y automático ese cálculo, esa liquidación, y que sea calable, en la medida que vayan surgiendo nuevas...

nuevas propuestas o nuevas alternativas, poder aplicarlas también y volcarlas a este proyecto de ecoseguros. Acá hacer un poquito mención a cuál es el alcance de este proyecto para dejar en claro y para también estar todos bajo un mismo criterio. Lo que incluye y lo que no incluye, lo que incluye es toda la parte de la BM de parametrización es que hoy la gente del equipo de Adri, con Jime y con Sofi lo vienen haciendo desde la S, todo manual

la parte de la AVM de parametrización, el cálculo unificado que mencioné antes, hoy tenemos el de autorizador, el de reintegros y el de ADP, la idea es unificar todo en uno. que sea seguro, los controles automáticos, barra reportes que se necesite en general. ¿Qué no incluye? Bueno, las correcciones de bugs en el sistema actual y el cálculo de copago. Acá estas correcciones de bugs y demás son también aquellos que se van haciendo en las distintas mesas de trabajo en las cuales estamos participando también.

que la idea es poder trabajarlo todo junto y en la medida que se vayan haciendo esas correcciones, lo importante que tiene esto es que esas correcciones que se van haciendo, como mencioné antes, y se vuelcan en el autorizador, nosotros ya las vamos a estar contemplando.

al momento de realizar esa reingeniería que necesitamos hacer. Así que ese es un detalle no menor también. Pero sí entender que hoy no lo absorbe el proyecto, cualquiera que surge, si bien estamos involucrados y estamos participando y demás. con la gente en mitigación de riesgo y demás, nada, no es algo que compete al proyecto en sí hoy día. Por otra parte, ver un poquito lo que es el roadmap.

contemplando un poco las ausencias en cuanto a lo que son los días no laborales de diciembre, las vacaciones que van tomándose cada uno de los participantes del equipo, que después lo vamos a ver, la parte de configuración que inició por allá por septiembre.

La parametrización de los ABMs, acá como verán, 1, 2, 3 y 4, después yo voy a mencionar bien cuáles son esos ABMs, el tipo de coseguro, la lista de precios, los valores y la unificación. De ahí vamos a seguir, tenemos un blanquito acá que es la idea de poder hacer todo un testing en conjunto con, y unas pruebas en conjunto con el equipo de Adri, con Sofi y con Jimé sobre estos cuatro AVM que de los cuales ya algunos hemos ido.

mostrándoles a ellos los avances que tuvimos en cuanto a pantalla y del lado del VAT también cómo funciona el servicio. Seguido de eso, bueno, vamos a estar en febrero trabajando en toda la reingeniería del cálculo de ecoseguro, esta unificación que mencioné antes.

Mediados de marzo, empezando la segunda semana de marzo, vamos a estar con lo que es el servicio que se tiene que llevar a cabo para la parte de medicamentos o seguro. Acá un detalle no menor, después de trabajos que fuimos haciendo y análisis que fuimos trabajando en conjunto con las distintas mesas, entendemos que hoy el cálculo del coseguro de medicamentos no está erróneo, no es que funciona mal.

Si lo que vimos es que deberíamos mejorar o repensar el proceso para que ese cálculo que se lleva dos meses después de… de que el asociado tiene esa dispensa de medicamento que se la da la farmacia, lograr que ese cálculo sea en el momento en que se hace esa dispensa. Entonces es poquito rever ese proceso y ahí nosotros ir a trabajar en un.

en un servicio para que pueda consumir esto, este cálculo en ese momento. Lo que es, bueno, la integración con el autorizador, ADP y reintegro, que es parte de ese cálculo que luego se va a unificar. Vamos a estar trabajando los mediados de marzo, abril, y en conjunto también vamos a estar con la parte de controles automáticos, ¿sí? Para abril, mayo. La idea es poder tener, en lo posible, ya para principio de mayo, las pruebas de regresión, seguridad y performance para poder ir poniéndolo ya productivo también.

Esto obviamente va a depender un poquito de los avances que se vayan teniendo en cada uno de los sprints, en la necesidad de poder avanzar. y tener completa cada una de las peticiones y los trabajos que se llevan, las tareas que se vayan necesitando. Y hoy en día, bueno, estamos trabajando en todo esto con un equipo de trabajo, que bueno, está la parte de proceso y riego, que bueno, está Sol Smitl, Smitlen,

Cristian Gauna también trabajando con nosotros, como sponsor Belén Regiscioli y Uriel Nicola, tenemos a Eugenio, tenemos a Seba Treñier y a Mauro Estorero también. Equipo técnico está compuesto, líder técnico Kevin, como dev de la parte de servicios de VAC está Mariano Goyanechea, como dev está de la parte de front Rami Mouroua y el CUA que hoy no lo tenemos pendiente pero la idea es poder, al momento no lo vamos a estar necesitando.

porque creemos que podemos hacer esas pruebas de testing que mencioné anteriormente finalizadas con estos sprints de ABM, entonces la idea es poder seguir probándolo nosotros mismos junto con el equipo de ABRI y no tener que absorber por ahí un... una persona más al equipo que lo podemos absorber nosotros. Bueno, el equipo en sí, el líder del proyecto, Tomás Muñoz, quien les habla, Joaquín Amedijeira, en la parte del PO.

Scrum está Franco Rimoldi y como soporte del proyecto está Darío Gürtel. Estas son las partes que las personas que hoy estamos trabajando en el día a día con el proyecto y que, bueno, tenemos como objetivo poder implementarlo. en tiempo y forma. Un poquito, bueno, el impacto en sí que pueden tener y los stakeholders, la parte de los stakeholders directos como los indirectos, la parte de liquidación de asociados, experiencias de asociados, ya estamos mencionando esto por toda la parte de esas liquidaciones de ecoseguros que por ahí se cobran y que no corren.

respondería por la práctica forrollazada o con problemas con los conceptos, etcétera. Gestión administrativa de salud, que son quienes van a estar abocados directamente con la parametrización y demás, bueno, afiliaciones. inteligencia competitiva con las listas, la gente ADP con su cotizador, su control también, su cálculo unificado, la cadena de valor de asociados, operaciones individuales de individuos.

operaciones de línea empresa y como indirecto la parte de legales, reintegros, auditoría de copagos, autorizaciones, contrataciones, conectividad y riesgos. Obviamente que por más que hoy son stakeholders tan diferenciados entre directo e indirecto, con todo vamos, en la medida que se va necesitando, vamos teniendo las reuniones, vamos participando también en las reuniones que nos van...

nos van involucrando y en la medida que se necesita vamos, bueno, levantando la mano como para poder ir trabajando en paralelo y con un mismo criterio para lograr el objetivo. Los próximos pasos, bueno, estamos terminando lo que es el Spring 4, que finaliza el lunes, 29, el 29, sí, el lunes, en donde estamos terminando con el último Spring.

el último ABM, acá se está trabajando el ABM último para finalizar toda la parte de parametrizaciones y en el Spring 5 la idea es poder testear todos esos ABM que son los que se mencionan acá, que es el ABM de tipo de coseguro, el de lista de precios, el de parametrización de valores de coseguro y asignación de relevamiento de cada nomenclador, capítulo y subcapítulo al tipo de coseguro que corresponde.

No sé si hay alguna consulta, fui medio rápido, no quería tampoco robarles mucho tiempo, la idea, bueno, como se mencionó al principio, fue poder mostrarles la situación en la que estamos, en qué parte y etapa estamos del proyecto. y que sepan que, bueno, que se está trabajando ya para poder avanzar con los requerimientos

Yo. Joaquín, una pregunta, ¿está previsto entregables intermedios o la solución, el entregable va a ser final por allá en mayo? ¿Qué quiero decir con eso? Viste que hay una gran parte que es toda la parte de parametrizaciones, que la verdad que no sé si son la, digamos, se nutren con los mismos modelos de datos o ahí se hizo un cambio.

porque por ahí, viste, que la parametrización hoy requiere de una intervención a través de script, y a lo mejor sí eso se puede empezar a disponibilizar antes. Repito, siempre y cuando no se hayan cambiado sustancialmente los modelos de datos, podría fijarse entregables parciales.

más allá de que falte el servicio y que falte después la adaptación de los otros de los otros squad. Sí, ahí la idea es bueno justamente terminar con esta parametrización Libby que hacías mención vos. que son estos cuatro tipos de ABM, y ver la posibilidad de ya poder hacer un entregable para que el equipo de ADRI y demás puedan ya ir trabajando ahí, no sobre esto de la S que es un tanto tedioso, bueno, tú lo conoces, las famosas pantallitas negras con verde.

La idea es poder hacer ese entreable, que ellos puedan ir trabajando ahí porque los servicios están trabajando, y después sí avanzar con toda la parte del cálculo del Código Seguro en sí y toda la parte del medicamento, que esto se… se fue sumando después de lo que fue el objetivo inicial del proyecto, consideramos que en ese jacatón que hubo donde surgió esto del medicamento, era importante trabajarlo.

Si bien como se mencionó antes, no hay un cálculo erróneo ahí del coseguro de medicamentos, eso está perfecto, eso está funcionando bien, sí hay que mejorar o repensar esta parte de... ¿En qué momento hacer el cálculo para lograr reducir mucho más el margen de esos poseguros que no cobramos? Porque el asociado dos meses atrás se llamó.

se dio de baja, digamos, que sí, ese es el objetivo sin duda. Perfecto, perfecto, sí, demás está decir que, bueno, deberíamos, y esta era justamente una de las partes, modernizar todo lo que no deberíamos más estar usando puntos de la ESTE, así que este es...

el camino con este proyecto de modernización, por así decirlo, así que bueno, buenísimo, me parece que por el cronograma estábamos hablando tal vez de febrero. poder que las chicas puedan contar, al menos con esa parametrización, no por AS-400, ¿no? Como un entregable parcial, mientras...

se sigue con todo lo que falta para hacerlo lo más reutilizable y, bueno, estándar posible, ¿no? Ahí por eso va a ser fundamental, y se menciona que entendíamos que no íbamos a necesitar en esta instancia lo que es el CUA, porque creemos que nadie es mejor que Adri, Sophie, Jime, que ya las estamos volviendo locas, pobres.

para ayudarnos a testearlo y lograr ponerlo productivo como un entregable, porque entendemos que vamos a agregar un valor bastante importante también en el proceso de ellos. Así que sí, la idea es esa. Ahí por ahí vamos. Gracias, Joaquín.

¿Alguna otra consulta? Si no, bueno, cualquier cosa, estamos por mail o por el chat y si necesitan Hay un sumo a lo que dice Joaco, la idea es hacer una reunión mensual Eso me iba a preguntar, Tome, justo, ¿a cuánto vemos las avances? La pedimos hacer una reunión mensual para poder traerle avances a toda la mesa y si necesitamos por ahí alguna reunión o algún encuentro puntual con algún sector y también ir haciendo validaciones, capaz que en 15 días podremos hacer mesas puntuales, poco.

o la mensual donde vamos a juntarnos todo y vamos a traerle nuevamente el estado. Sí, ahí nada, agradecer también un poco a la, bueno, un poco no, agradecer. a todos los sectores que se vieron ahí involucrados, porque realmente es un trabajo difícil porque, bueno, hay muchas cosas, muchos puntos de dolor y muchas situaciones que no están plasmadas en papel, por de alguna manera decirlo, están en la cabeza de alguna de las personas, entonces nada.

Muchas veces estamos requiriendo reuniones y volvemos a citar reuniones y volvemos a tener dudas y la verdad que en ese sentido siempre están todas las partes del ADP, el equipo de Cris, Sol La verdad que tenemos una respuesta super positiva y está bueno trabajar esto para poder

Hacerlo de la mejor manera posible, así que gracias por el tiempo y por aceptar que jodamos tanto nosotros. Bueno, perfecto. Bueno, muchas gracias. Le compartimos por mail esta presentación. Para cualquier duda, cualquier consulta que se busque más adelante, nos avisa. Muchísimas gracias a todos, que tengan un buen día lo que nos vean, chau.

Aparecerá esta ventana. Seleccionamos Lista, y en Origen ponemos los nombres que usaremos. Aceptamos. Ahora seleccionamos toda la tabla. Vamos a Inicio y Formato condicional. Clique en Nueva regla. Aquí vamos a la última opción. Ahora vamos a la casilla vacía. Damos un clic en la primera celda de la tabla. Presionamos dos veces F4 para fijar los datos.

Y ahora escribimos. Vamos a Formato y elegimos el color que queremos usar. Repetimos el mismo proceso con el otro nombre de la lista. Observa esta magia jefito.

Subtítulos realizados por la comunidad de Amara.org



[https://docs.google.com/presentation/d/1CQIyeP562Se6kkTPiBCmt4G0_IpxddBiO-G1xGEoNDw/edit?usp=sharing](https://docs.google.com/presentation/d/1CQIyeP562Se6kkTPiBCmt4G0_IpxddBiO-G1xGEoNDw/edit?usp=sharing)



