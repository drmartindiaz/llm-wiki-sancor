---
source_url: https://app.notion.com/p/2672c02ab01980b6a544d4e0113f0618
ingested: 2026-07-08
title: Medicamentos 
notion_id: 2672c02a-b019-80b6-a544-d4e0113f0618
---

[https://docs.google.com/presentation/d/1Low5v8zc2LlKNewn_AqeCg777GjMoA5xoZGclfmE-M4/edit?usp=sharing](https://docs.google.com/presentation/d/1Low5v8zc2LlKNewn_AqeCg777GjMoA5xoZGclfmE-M4/edit?usp=sharing)

Temas pendientes con Medicamentos:
[https://docs.google.com/document/d/1qyzpp2kSe3dtrwQ_2DJS4QxgucqinYrb3mmCIyU4q_w/edit?usp=sharing](https://docs.google.com/document/d/1qyzpp2kSe3dtrwQ_2DJS4QxgucqinYrb3mmCIyU4q_w/edit?usp=sharing)

[https://docs.google.com/document/d/1ohpTg4l_2t5WAflqETZicQ2qQPPaVO_3mKU_NKXf5Qw/edit?usp=sharing](https://docs.google.com/document/d/1ohpTg4l_2t5WAflqETZicQ2qQPPaVO_3mKU_NKXf5Qw/edit?usp=sharing)

[https://docs.google.com/document/d/1H7ojawIFyGtUrUb-0ZhnJxt-lA13b_iTVaoaBez_-ow/edit?usp=sharing](https://docs.google.com/document/d/1H7ojawIFyGtUrUb-0ZhnJxt-lA13b_iTVaoaBez_-ow/edit?usp=sharing)

▶ **P1: ABM Programas**

Impacto de este tema:

Impacto en experiencia de asociado

Bajar carga operativa de SS

Salir de AS/400 y vieja intranet

Ahorro de consultas médicas por recetas

Fomento de uso de receta electrónica

Reunion con Pablo y Cami para ver estado de implementación de funcionalidad

▶ **P2: Cotizador**

Integración con droguerias — Modelo Scienza

Hoy es un pdf, debería ser un servicio web estándar (Cargan la orden de compra en el Cotizador, eso genera un sheet que es levantado por un par de bots y eso envia un mail a la drogueria)

Definición de modelo de datos: Cami

Temporalidad de consulta de stock (pasarlo a cuantitativo - P2) y de envío de pedidos (P1), no Cron sino por evento.

Tracking de pedidos de droguerias a farmacia (Logistica propia, tercerizada o lo que sea)

▶ **20250107 Validaciones de AMPS y PAMI en servicios de autorizacion de mandatarias de farmacia **

<!-- unknown block type: transcription (2e12c02a...) -->



### Estado del Nuevo Servicio

- Se está desarrollando un nuevo servicio para Colegio de Compañía con migración de seguridad en SHIP 
- Ya incluye la validación de MPS con identificador (válido MPS o válido Sanco) 
- La parte de recetas ya fue enviada a Praxis, MyCRX y equipos de telemedicina (Fluir y otros) que están desarrollando 
- El servicio está en últimas etapas de aprobación por seguridad 
### Complemento de MPS y Farmacia

- Actualmente el complemento de MPS no está incluido en las validaciones online - se enteran del pago cuando llega la factura 
- El servicio de elegibilidad de farmacia es un complemento que pertenece a la asociación de empleados de la láctea, no de sal y la asociación mutual 
- El complemento originalmente daba cobertura adicional en farmacia 
- Algunos planes cambiaron después, había otros planes de AMPS y complementos 
### Desafíos Técnicos

- Cada nuevo agregado (como códigos postales) debe implementarse tanto en el servicio actual como en el nuevo, lo que genera demoras 
- Esto retrasa la actualización de documentación porque hay que hacer desarrollos en paralelo 
- El proceso de seguridad está en ida y vuelta con observaciones y correcciones, pero no está trabado 
- Los agregados posteriores no requieren nueva validación de seguridad 
### Alcance del Nuevo Servicio

- Incluye el formulario 4 dentro del mismo servicio de elegibilidad 
- Todos los ajustes que no salieron a producción se llevaron al nuevo servicio 
- El desarrollo se hizo solo para compañía 
### Timeline y Próximos Pasos

- La validación de seguridad debería completarse este mes o el siguiente como máximo 
- [ ] Matías Maina to confirmar con Rubén el timeline exacto de validación de seguridad 
- [ ] Organizar reunión cuando el servicio esté listo para explicar todos los cambios 
### Reclamos Actuales

- Hay reclamos de socios porque no se les aplican los dos complementos 
- El problema venía por error conceptual de compañía que entendía todos los complementos como AMPS 
- Hay planes como Línea Dorada que son planes de salud pero actúan como complemento de otra obra social (PAMI) 
- Compañía no venía presentando archivos de MPS correctamente - cuando empezaron a presentarlos incluyeron todo lo que conceptualmente entendían como MPS (productos MPS + productos de salud que actuaban como complemento)  








Perdón, se me cortó, Magui, no, no, está bien, soy yo, porque se me fue el internet, podés... Está bien, tengo congelado. Ahí le decía a los chicos, sobre todo, era conocer de parte de ellos qué es lo que faltaba. en cuanto a las validaciones para el lado de compañía que hoy por hoy no está el 100% validándose online. Hay productos como lo son el complemento de MPS.

que no esté incluido en las validaciones, es decir, nos enteramos cuando llega la factura de lo que hay que pagar. ¿Tengo entendido ahí? Estaban haciendo un desarrollo... Refrescame, Mati, qué es lo que faltaba para que podamos incluir todo. Todo lo de AMPS lo agregamos en el nuevo servicio que tenemos que pasarle a Colegio de Compañía, que es con seguridad, migrado, en SHIP y todo.

Ahí ya se contempló lo de la validación de MPS como tiene colegio. De la misma manera sería con un identificador que ellos dicen válido MPS o válido Sanco. Eso ya está en el nuevo servicio. Lo que falta es terminar de aprobarlo por seguridad y demás, pero ya están en la última etapa. La parte de recetas, por ejemplo, yo ya se la pasé a Praxis y mi CRX.

y a los chicos que la usan de telemedicina, fluir y demás, y ya están desarrollando. Quedaron más lo que es el servicio elegibilidad de farmacia. Es un complemento, es un producto que no es de sal y la asociación mutual. Era asociación de los empleados de la láctea, digamos, y originalmente cuando les vendían el... les daban un complemento, como un adicionario.

¿Vos tenés ese complemento? ¿Tenés una adicional de cobertura en farmacia? ¿En cuánto en farmacia, digamos? Claro, o alguna otra cosa que le daban también en ese momento. Y quedaron algunos planes después los cambios. Había otros planes de AMPS, otros complementos y después los cambiaron, me parece.

Sí. Ahí, Mati, entonces, lo que estaría faltando para agregar esto es la validación de seguridad. Claro, para mandarles el nuevo servicio a colegios y compañías, o sea, una vez que esté OK. Y que obviamente es un desarrollo nuevo para el Colegio de Compañía Funciona de la misma manera, pero es otra URL, es otro servicio Lo que sí no, perdón, iba a agregar a eso Maga antes

nos hace como que nos demoremos cada vez más, cada agregado que tenemos ahora, por ejemplo, lo de los códigos postales, lo de es agregarlo en el actual y en el nuevo, entonces digo, por eso nunca terminamos de actualizar la documentación porque Cada vez que yo cargo una petición para algo nuevo de farmacia, tengo que hacerlo en el que usamos hoy en día y en ese nuevo, porque si no después no va a quedar ese actualizado. Pero bueno, se va haciendo siempre en paralelo.

Por más que falte lo de seguridad, no digo que estamos frenados por las cosas que vamos agregando Y lo de seguridad, no sé si es algo que nosotros podamos destrabar o... ¿Cómo funciona eso? No, no, nosotros le vamos pasando la documentación y demás, le van haciendo observaciones a los chicos, ellos van corrigiendo, no está demorado o trabado por decir, sino que está en ese ida y vuelta de...

de seguridad. Pero paneles, cada agregado que le hagas, ¿tenés que validarlo con seguridad o no? No, no, esas cosas no. Ellos miran más lo que es el desarrollo y toda la parte de seguridad del servicio. ¿Y cuándo podría estar esa validación? Me llevo para, o sea, tendría que estar en este mes o en el siguiente como mucho, me llevo para preguntarle a Rubén

en el lío técnico que lo va, los chicos lo van viendo con él y le van pidiendo a él los go walk donde piden la aprobación y demás y les confirmo, pero ya están en las últimas instancias de él Ah buenísimo, y encima del token, que valía en el token No, perdón, el formulario 4 dentro del mismo servicio de elegir. Está todo metido en este nuevo, eso también está contemplado, todo, sí. Ah, buenísimo. Solo para compañía se hizo eso, ¿no? Sí, sí, sí, sí.

Y lo habíamos hablado con ellos, sí. Sí, todos los nuevos ajustes, por decir que no salíamos a producción ya, se llevaron todo para el nuevo. Después, cuando esté, obviamente, armemos una mítica y les comento todo. Buenísimo. Vengo dos segundos y me tocan timbres, justo. Sí. Bueno, no sé, ahí Jiméz y José. ¿Qué falta?

¿Qué faltaría? Digo, porque acá el problema que tenemos es que tenemos reclamos de los socios que no se les está aplicando los dos complementos, ¿sí? Ninguno de los dos. Sí, el tema del reclamo venía por una cuestión de error conceptual sobre todo el lado de compañía, digamos, que entendían a todos los complementos como MPS.

Siendo que no es así, digamos, hay algunos planes como son Línea Dorada que actúan como complemento, son planes de salud pero actúan como complemento de otra obra social principal, en este caso de PAMI. la mayoría son esos, que se venían presentando mal, esto que pasó con los archivos de MPS, compañías no los venían presentando.

Cuando los empieza a presentar, presentan esos archivos todo lo que conceptualmente ellos entendían como MPC. Productos de MPC y productos de salud que actuaban como complemento de otra obra social. Ahí es como que se arma un alboroto, digamos, porque empezaron a darse cuenta



▶ **20260109 Configuración de producto de medicamentos**

<!-- unknown block type: transcription (2e32c02a...) -->



### Problema Principal

- El sistema actual requiere crear un plan nuevo completo cada vez que se necesita una variación en el porcentaje de cobertura de farmacia (40%, 50%, 60%, etc.) 
- Actualmente hay aproximadamente 10 nuevos planes GEN con 50% de cobertura en farmacia esperando parametrización, que son básicamente variantes del mismo plan base  
- Se estima que un 70% del total de planes (aproximadamente 100 planes) podrían darse de baja si se implementa la solución propuesta  
- La situación es "inadministrable" y se vuelve más compleja con cada nueva variación requerida  
### Soluciones Propuestas

- **Sistema modular de farmacia:** Separar la cobertura de farmacia del plan base, convirtiéndola en un atributo independiente que se puede combinar con diferentes planes   
- **Concepto "Supra":** Crear un plan adicional (ej: "Supra 10%") que se asigna manualmente a ciertos asociados para agregar porcentaje extra de cobertura, sin modificar el plan base   
- **Visión a largo plazo:** Sistema de producto personalizable tipo "carrito de compras" donde los asociados puedan elegir módulos/packs adicionales al plan base, manejando cada extra como un atributo del plan    
### Consideraciones Técnicas

- **Sistemas afectados:** Cualquier cambio debe considerar tres servicios principales que leen el porcentaje de farmacia:
- Validación de farmacia (actualmente gestiona Colegio y Compañía mediante marcas)  
- Reintegros (Juan Bertero/Juan Cruz confirma que leen del AS - AS Producto Plan Subgrupo)  
- ADP (algunas farmacias todavía presentan directo, aunque la mayoría pasa por Colegio y Compañía)   
- **Complejidad adicional:** La cobertura de farmacia no es solo un porcentaje lineal - incluye múltiples listados y porcentajes diferenciados: 
- 6 listados diferentes de anticonceptivos con distintas combinaciones de marcas y porcentajes  
- Vademecums (Sustentable, R3D, VPC, Programa 29) 
- Exclusiones de drogas
- Vacunas y nutrientes dérmicos 
- **Propuesta ABM de Planes:** Crear una "burbuja de medicamentos" dedicada dentro del ABM de planes para parametrizar todas estas reglas, que actualmente están dispersas en sheets, Excel y múltiples sistemas   
### Contexto Actual

- Se está removiendo el porcentaje de farmacia de las credenciales porque ya no se usa (las farmacias validan con su propio sistema) 
- Medida comercial en curso: Se está otorgando 10% extra en farmacia a ciertos asociados según criterio etario, actualmente se gestiona mediante marcas en el padrón  
- El prestador (Colegio) ya se queja de estos "parches" y "atadas con alambre"  
- Falta de visibilidad: Los puntos de control están desagregados en múltiples sistemas (motor, validador, AS), dificultando dar respuestas completas 
### Próximos Pasos

- [ ] @Martín M. Diaz Maffini hablar con Pablo para evaluar factibilidad técnica de ambas alternativas (atributo vs SUPRA) y determinar impacto en performance   
- [ ] Anto agregar a Magui e Iba a la reunión de ABM de Planes del viernes próximo  
- [ ] Anto hablar con Cele Solaro sobre la propuesta antes de que salga de vacaciones  
- [ ] Equipo trabajar con Cami para documentar y sistematizar los problemas actuales que se resuelven "con parches"  
- [ ] Evaluar creación de "burbuja de medicamentos" en ABM de planes para centralizar configuración 
### Reuniones y Contexto Previo

- El equipo ya presentó esta problemática a gente de transformación digital como parte de proyectos para 2026, bajo el nombre "Sistema de Producto Personalizable"   
- La presentación incluyó problemas de configuración de productos, especialmente el tema del 10% extra de descuento en farmacia 
- También se mencionó la necesidad de sacar el producto del S-400 y hacer reingeniería del proceso de ABM de producto 






farmacia hablo, ¿no? Eh en a lo mejor pensar al momento de comercializar un plan, no pensar el plan como un todo, es decir, creo este plan que tiene cuarenta por ciento de farmacia. No, que pensar en un plan que tenga, no sé, una cobertura general y que la cobertura en farmacias se determine por una especie de módulos, es decir,

Yo tengo el módulo del 40%, un módulo del 50, y que cada afiliado pueda tener no sé si el módulo que se venga como paquete o que pueda elegir su propio módulo. que por un lado sería el porcentaje de cobertura, y por otro lado, definir los listados de productos a reconocer.

A los bademekum te referís Magui cuando decís eso, te referís a los bademekum Bueno, ahí chicas, esta misma semana estuvimos reunidos con Martín y Adri, porque bueno todos tenemos el mismo problema, la verdad que Últimamente, o sea, y no va a cambiar porque cada vez más los productos tienen alguna diferenciación, alguna cosita, algo, no sé qué, que le ponemos.

Y la verdad es que es muy complejo que cada pavada que queramos cambiar implique la creación de un plan nuevo. Ahí, nada, lo que pensábamos con los chicos, y bueno, también digo, considerando que la gerencia ustedes la comparten, lo que pensábamos con los chicos fue, digo, esto a lo mejor es un proyecto macro porque va a abarcar a toda la compañía, tal vez la administración de una nueva forma de de armar productos o de crear productos, entonces tal vez tengamos que plantearlo, digamos, a la dirección de operaciones.

para ver digamos algo más a fondo, pero creo que a lo mejor podríamos para esto de medicamentos ver si podemos arrancar con algo intermedio. para ver cómo le podemos poner a lo mejor un parche, por lo menos para la parte de medicamentos, que bueno ahora, Adri, viste que tenemos...

15, creo que son 10, no sé cuántos planes más nuevos que tengo que pedir que habiliten, porque son los GEN, con el 50% en farmacia, que se venden en línea empresa. Entonces tengo 10 planes nuevos que le decía Adri, estoy esperando, le digo... que terminemos de parametrizar los otros, para mandar el mail nuevo, que la gente no me odie básicamente, o sea. Esos 10 planes, ¿qué tienen de distinto con otros?

planes que ya estén creados, digamos, porque se crearon nuevos. Nada, es una variante de los genes nuevos que se crearon con el 50% en farmacia. En lugar del 40. En lugar del 40. Claro, ves, podría ser un único plan GEN que ya esté creado, solo que a esto se le agrega el módulo de 50 en vez del 40.

Es como diferenciar lo que es la cobertura en farmacia. Exacto. Incluso, chicos, ahí también, justo ayer hablaba con Lore Pacheco. Que me pidió que, va, me dijo que Daniel le pidió que habláramos con marketing y eso, para sacar el porcentaje de farmacia de la credencial también, porque eso ya ni se usa, la farmacia valida ya tiene todo, digo, es confuso, entonces como que también le pido a marketing que reacomode las credenciales para que no se muestre más ese porcentaje.

digamos, de farmacia ahí. Así que digo, nada, me parece que tenemos algo como más macro para trabajar, que nos va a llevar más tiempo. pero creo que a lo mejor podríamos plantear, por lo menos para lo de farmacia, un plan B, porque la verdad que muchos de los planes que tenemos que crear son porque tienen alguna condición distinta de farmacia.

Nosotros desde la gerencia tenemos unas reuniones con la gente transformadora.

alguna necesidad de la gerencia para lo que sería 2026, así bien macro a nivel proyecto y uno de los proyectos justamente es sobre producto. De hecho, la vez que se lo presentamos, también vino Jimmy y le presentó cosas de medicamentos, pero que no eran cosas nuevas, sino pendientes del lado.

de lo que hay de Vablog ahora. Estaba buscando la presentación, a ver si les podía mostrar eso que le presentamos de productos, si me dan dos segundos. Creo que lo tengo acá. Martín, ¿vos sabés que? ¿Jimén me mencionó algo? Sí. Cuando nosotros fuimos con esta idea, bueno, despegar el porcentaje del plan.

El porcentaje en farmacias del plan, ella mencionó algo de que vos habías tirado una propuesta Martín, por eso te sumé ahora en esta misma Pero bueno, gracias a vos por sumarte, la idea es que por ahí no estemos trabajando lo mejor en lo mismo, pensando en lo mismo, podamos...

No, por eso, digo, si les parece les muestro, les prometo que les mostramos a la gente de transformación digital, para ellos, pa' qué.

Vean que estamos, obviamente, alineados y en qué contexto lo incluimos, digamos, ¿no es cierto? Entonces, eran varios temas, este era uno de los temas, se llama, no, Sistema de Producto Personalizable, se llama así, no importa, después les explico por qué, pero fíjense que cuando empezamos a plantear la problemática del asunto...

los problemas actuales de configuración de productos, fíjense el segundo que dice dificultad para manejar atributos del plane 10% extra descuento en farmacia digamos, o sea, cuando empiezas a hacer esto, como decía creo que Anto, van a tener que estar creando planes porque esta intervención del 10% extra descuento en farmacia para un grupo de asociados, hay que de alguna manera ponerla en marcha.

en juego, ¿no es cierto? En función de esos comentarios, qué sé yo, bueno, también tenemos el problema del S-400, lo paso rápido porque no hacia el punto, pero... Una de las cuestiones era, a corto plazo, sacar el producto de S-400, que es algo que todo el mundo viene pidiendo, queriendo hacer, etcétera, pero bueno, estamos con un proyecto directamente. Ver en qué pega todo eso, obviamente, y si hay que hacer una reingeniería del proceso de ABM de producto, que es lo que creemos que hay que hacer.

Y ahí, obviamente, vamos a tener que sentarnos con Comercial, con Contrata, con todo el mundo, para ver cómo miércoles hacemos la reingeniería esta. Y lo que queríamos hacer, y por eso les digo, después les voy a contar por qué se llama así, era finalmente tener una especie de, a vista del asociado, una especie de carrito de compras donde vos puedas, bánquenme, yo ya voy a llegar a lo de los medicamentos, un carrito de compra donde vos puedas elegir, tipo, viste, cuando...

no sé, cuando contratas el cable que decís quiero, no sé, el pack de fútbol, quiero el pack de videojuego, quiero el pack de... bueno, una cosa por el estilo para pensarlo y que eventualmente cada una de esas cosas que vos contrates extra al base, vamos a decirlo así, sea un atributo en realidad del plan.

No es que vos generas un plan nuevo para cada asociado, porque si no tendrías tantos planes como asociados y es ridículo, es inmantenible. Entonces vos lo que tenés es un plan base que respeta, ponele no sé si es un plan completo, respeta el PMO y después tenés un montón de extras, comillas, que son nada más que atributos, es decir, che mira, Anto tiene el plan base más el pack, como si fuera un

sucesivamente y uno de esos packs puede ser el descuento extra de farmacia de cuánto y son packs diferentes, hay un descuento de entrada de 10, uno de 20, uno de 30, lo que sea, digamos una mierda, entonces, luego lo que terminas teniendo son una especie de productos base con una serie de atributos asociados y eso es mucho más fácil de manejar, digamos, porque es un sistema de atributos y valores desde el punto de vista de la farmacia.

sistema y es a lo que creemos que hay que tender para, por ejemplo, subsanar el problema del tema de la farmacia. Ahora, esto es futuro mediano-largo plazo. Digamos, en lo inmediato, esto, si no cambiase El modelo de datos, digamos, no es tan fácil de hacer, me digo que no se pueda, digo que no es tan fácil de hacer. Pero ese sería como el norte del asunto. Con lo cual, les dije un montón de cosas hermosas, pero concretamente no tenemos nada.

Lo que digo es, para pensarlo, quizás la forma de encarar el tema es por acá, es decir, Podemos pensar incluso, digo, con lo que tenemos hoy, sin cambiar nada, podemos pensar... Lo tiro, no lo doblé con nadie, lo estoy tirando acá... para que me ayuden a pensar si es factible. ¿Puedo pensar un plan supra, digamos como para la parte de medicamentos, que eventualmente vos tengas el 40 que corresponde, según plan, 50, lo que fuere, y si eventualmente queremos agregarle un 10 extra, como es el caso actual, o el número que sea extra, se gestione como un plan supra.

Lo que pasa es que sería medio automático, no sería un supra que vos tuvieras que agregar medio manual, sino que debería ejecutarse para un grupo de asociados en particular. ¿Es ese el sentido o es imposible gestionarlo así? No, sí, sí. No, no, no lo veo mal porque la realidad, digamos, es que hoy...

generalmente todo lo que es, digamos, adicionales en farmacia, digamos del 10%, se usa a priori para línea empresa, digamos, la venta individual es o al 40% o con el 50% o 60% o 70% porque el plan tiene esa condición. Después, si vos, por ejemplo, tenés un plan 1000 y querés el 50% como individuo vos, contratando retail a un asesor, no lo podés hacer. Eso está habilitado para venta de empresa. Ahora.

Ahora, por ejemplo, sacamos algunas medidas comerciales que tienen que ver con reforzar un poco un stock de asociados, a los cuales se definió, che, a este mundo de gente, que es gente que tiene una condición etaria, Le vamos a dar el 10% en farmacia. Que bueno, eso me comentó Lore que lo estuvieron viendo con Jime, van a tratar de hacer como algo ahí medio caserito por padrón.

Pero, no sé, digamos... Eso es pan para irme para mañana, porque se te desmadra en 10 minutos la configuración Sí, chino, chino total Pero nada, me parece que a lo mejor podríamos ver, digamos... algún supra, o sea, después digo alguna cosita manual se me hace que vamos a va a tener que ver porque digamos alguien le tiene que asignar a ese socio

ese SUPRA con tal porcentaje de medicamento distinto. Pero bueno, una vez que ya lo tiene asignado, debería operar, digamos, sin ningún problema.

No hay problema, ese no hay problema porque le hacemos un plan a medida para esa empresa. Ah, ok. Sí. Ok, perfecto. O sea, no a medida, digamos, pero hay planes genéricos. Por ejemplo, esto acá que yo le decía, ahora que tenemos que crear ahora porque son los gen con el 50%, esos planes ya están en las grillas de venta a empresa y después cuando se vende, se vende, digamos.

la condición de... es por plano, exacto. Y suponente que vamos, exploremos un segundo si les parece la... la idea de Supra. Hacemos un Supra 10% se llama, no importa. Y decimos, bueno, mira de estos cinco asociados que tenemos acá en la MIT, a Anto y Adri les va a tocar el Supra este. Se los ponemos a mano. Decimos, che mira, Anto y Adri ahora tienen el Supra 10%.

Digo, para pensarlo, van a la farmacia, voy yo a la farmacia que no tengo el 10%, me cobran el 40% de coso, como cualquier hijo vecino. Ellas tienen el mismo plan que nosotros. Pero cuando van a la farmacia el autorizador debería devolver que la cobertura de ellas no es del 40 sino que es del 50, digo bien?

Sí. Bien, y ese 50 lo debería calcular el autorizador fijándose que tiene un Supra 10 a diferencia de nosotros que no lo tenemos. Exacto. Eso es una alternativa, o bien la otra, en un futuro mediano, digamos, y no tan lejano como esta propuesta que uno sueña, como Norte,

No sé, a lo mejor se puede inventar un atributo al código de plan y que ese atributo sea 40 o 50 o 60, 70 u 80. y obviamente que el autorizador validador de farmacia tiene que ir a leer este atributo Bueno, en el A.S. o donde vayamos migrando, sí. No sé, no, en el A.S. hoy no va a estar porque no tenemos mantenimiento.

Pero se han creado, hoy en el ABM de planes, está el porcentaje de farmacia, ¿sí? Lo que hay que reconvertir... es que el plan va a tener todo su menú prestacional menos el concepto de farmacia. ¿Por qué? Porque eso va a estar en un campo aparte. Y después hay que hacer que los sistemas, que son sistemas nuevos, que ese porcentaje ya existe a nivel del ABM de Planes, no es en el AS desde cartillas de coberturas.

Lo que después hay que hacer es que los sistemas vayan a leer el porcentaje S. Independiente del plan. Bueno, exactamente. Las voy a sumar también a la reunión, chicas, a ustedes, el próximo viernes. a la bm planes porque ahí te acordás de amor y más y yo no sé si vos estaba así bueno en un momento le tuviste llegado a estar y habíamos hablado con

con él y back, ahora digamos es Cindy, pero de sumar la burbuja de medicamentos al ABM, una burbuja exclusiva para que ustedes puedan ahí también hacer como sus parametrizaciones. Entonces digo, capaz que a lo mejor aprovechamos el tiro. Se lo planteamos a Cinti y después vemos que sistémicamente también veamos si eso se puede tomar e impactar, digamos, en algún lado. Porque otro problema que hay es que hoy por hoy.

al no estar esa burbuja o ese espacio donde plasmar esa regla, viste, se dice, bueno, cobertura de farmacia al 40, pero excluye tales cosas e incluye esto. pero no hay dónde visualizarlo. Sí, claro, que digamos, a todo lo que después nosotras en las reuniones tenemos que chequear, debiera ser un checklist, digamos, que esté ahí.

Que de última, o sea, nosotros podemos poner, bueno, esto sí tiene esto, tiene esto, esto no lo tiene, no tiene, no tiene, listo, ya está. Ustedes ya saben qué es lo que tienen que hacer y se terminó. Exacto. Y si pensar el porcentaje como un atributo como hacía Adri, independiente del plan, está el plan S-1000

Y puede estar combinado con una cobertura de 40, con una cobertura de 50, y no tenés que crear otro plan distinto, digamos. Sí. Eso, bueno, escuchen, lo del AVM de Planes ya la reunión está, yo la sumo a ustedes, chicas. Y yo voy a hablar con Cele Solaro

que ella está ahora con nosotros en un montón de proyectos para planteárselos, yo sé que Cele se va de vacaciones la semana que viene, sale dos semanas, Pero bueno, para plantearle esta idea y que de última, nada, me deje a alguien con quien poder empezar por lo menos a planteárselo y ver si le podemos dar forno.

Ya le escribo el teléfono, antes de que se vaya y no la vea más después por dos semanas. Yo ahí, digo, me parece perfecto todo.

de las dos, digo, sí, agregar un atributo en algún lugar para que lo vaya a leer el autorizador y tenga en cuenta eso y no la configuración habitual digamos que tiene medicamentos en la S versus dejar todo como está desde el punto de vista del modelo, porque lo vamos a retocar en algún momento, no demasiado lejos, y agregarle como este, yo digo Supra porque es el nombre que dan acá, pero digamos esta cosa extra de configuración que va más de la mano de lo que decía antes, tanto de tener como la burbuja.

de medicamentos para el plan y demás. Lo que pasa es que estoy pensando en voz alta, si nosotros mantenemos esta estructura de decir bueno mira yo a nivel de plan te voy a decir cuál es la cobertura Seguimos teniendo la misma historia de siempre, yo voy a tener que crear un plan especial para un porcentaje de cobertura en farmacia, independientemente, digamos, de cualquier otra cosa, me prefiero, si agregamos este 10%, yo voy a tener que crear un plan que agregue el 10% para ese grupo de asociados, no voy a poder zafar de eso, por más que lo haga en una burbuja dedicada, por más que lo haga

que es otra cosa que hay que hacer, pero no soluciona el problema, me parece. Claro, yo lo que había pensado Martín es sacar del menú del plan el porcentaje de medicamentos y llevar eso a un atributo aparte. Entonces yo en el contenido, pero si tengo que ir a leer ambas cosas, es este plan.

con este otro atributo que tengo que leer, ¿sí? Y ahí, hoy por hoy, tenemos varias tablas de porcentajes de farmacia, ¿no? Cuando aparecieron todos estos planes... nuevos de Gen, yo volví a preguntar, cada tanto pregunto si lo que cargamos en el AS alguien lo seguía leyendo, no, porque ahora todo lo que es validación de farmacia

No se lee desde la S, el porcentaje, se lee de una tabla nueva que hicieron. Pero apareció Reintremo y me decía, no, sí, por favor, seguí cargándomelo porque yo lo leo de ahí. Juan Bertel me dice, mirá, si yo tengo que cambiar y leer desde otro lugar, no hay problema, nos ponemos de acuerdo y lo hacemos, ¿sí? Pero bueno, yo dije, mirá, espera porque justamente estamos pensando en alguna cosa nueva.

Si pudiésemos concretar a mediano plazo, pero bueno, hay que pensar en lo que es validación de farmacia, hay que pensar en lo que es reintegros. Y además, si logramos hacer eso, podríamos dar de baja un montonazo de planes, digamos, o sea, nos quedarían solamente como los planes.

Digo, nos van a quedar algunos planes con algunas particularidades, pero digo, el porcentaje de farmacias, si pasaría a ser un atributo, podemos dar de baja un montón de planes. Sí, tal vez. Y la administración de un montón de cosas. Sí, sí. Tal cual.

¿Quién era? Juan Bartero Bartero. ¿Quién es Juan Bartero? ¿Cómo? Juan Cruz, más conocido como Juan Cruz. No, Juan Manuel. ¿Cómo Juan Manuel? Juan Cruz Vázquez. ¡Ah, que es Renuncio Negro! ¡Ah! ¿De dónde? ¿Qué sector es Juan Martero? Es Reintegros, que en realidad creo que está como pego este, reemplazante, ¿no? De élite, me parece.

Pero en realidad cuando vos preguntá, no es que la tienen así clara, van a leer un código de sistema y te lo dicen, hicimos mínimo 10, 12 pruebas para llegar a esta conclusión, porque no es que la gente sabe, ah, para que voy y leo, no, che, seguí cargándolo, hicimos

como te digo, un montón de pruebas en testing para constatar que realmente en reintegro de medicamentos va a ver el porcentaje que yo le cargo en el AS, AS Producto Plan Subgrupo. Sí, pero bueno, hay que tenerlo en cuenta. Y después la otra tercer pata es ADP, que también lo leía de mi cartilla de la S.

¿Por qué? Porque había un par de farmacias, no sé si sindicales o qué, que no pasaban por Colegio y Compañía, pero capaz que ahora esa situación cambió, no sé chicas cómo estamos con eso, o si podemos garantizar que el 100% pasa por Colegio y Compañía.

No, hay dos o tres farmacias perdidas que siguen presentando directo pero la idea sería pasarlos a compañía de colegio, eso, para... Bien, nada más como para indicar, Martín, que son los tres servicios donde tenemos que ir a decir che, mirá, si hacemos esto nuevo, ustedes tienen que venir y leer de acá ese porcentaje de farmacia.

Sí, que además no es lineal, o sea, porque tampoco termina teniendo solo el 40% El porcentaje que va a tener el afiliado va a estar relacionado también a un listado Porque vos tenés un plan del 40, pero en anticonceptivos tenés el 100, pero en crónicos tenés el 70

O sea, tampoco es lineal, por lo cual habría que pensar en esa burbuja también si no asociar porcentajes alistados de medicamentos o de MECUM. A ver si yo te contesto, habilitó el BADMECUMB de anticonceptivo número uno, más el PMO, que entiendo que eso iría para todos los planes.

más listado de antiartrócicos, y bueno, te asigno un porcentaje de cobertura a cada uno de esos BADMECU. Ay, Iba, y eso hoy, ¿desde dónde lo manejan a eso? Eso está todo destrómico en el tiempo, no sirve lo que yo tengo. Todo desde el sistema de validación lo resuelve compañía y colegio.

pero nosotros lo administramos a partir de marcas. Ejemplo, esto de los socios que pasan a tener un porcentaje del 10% extra se resuelve agregando una marca a nivel del socio. para que el colegio lo traduce como un 10% extra. Pero eso también va a llegar un momento que va a ser inadministrable.

Ya el espectador cada vez que vamos a pedir algo de eso, se queja, le estamos trasladando el problema a ellos también. Y ni hablar que también tenemos los tiempos de ellos, cuando hablábamos de las burbujas y demás. que no es solamente el nuestro, de parametrización y de creación de esa marca y después de eso ir con el prestador, que hagan las pruebas. Sí, sí. Y la falta a mí siempre me preocupa.

la falta de visibilidad para el usuario, ¿no? Yo cada vez que me hacen una consulta, respondo por lo mío y me pongo a pensar que los puntos de control, que en el motor, que acá, que en el validador, qué hice yo. o la respuesta que das, no es una respuesta completa, porque está todo tan desagregado en un montón de sistemas, que la verdad que nos quedamos siempre a mitad de camino con las respuestas que damos.

¿Cómo les parece que lo podríamos encarar? Yo pongo una propuesta y si les gusta la vamos, y si no, cambiamosla. A mí me gustaría primero hablar con alguien de sistemas para que evalúen, aunque sea a alto nivel... si es factible esto que estamos planteando, de tener un atributo para cobertura de farmacia, vamos a decir así, un porcentaje de farmacia por fuera de los planes y que sea leído en el momento de la elegibilidad, autorización, etcétera, el autorizador va, y que eso no afecte demasiado, digamos, la performance del asunto.

Eso por un lado. Versus la alternativa que planteamos de los SUPRA. a ver cuál es la más factible a corto plazo, mediano plazo y cuál impacta menos o cuál se puede hacer más rápido y qué sé yo. Hasta ahí vamos, ¿bien? ¿Les parece que podamos hacer eso?

Sí, sí. Perfecto. Perfecto. Yo me lo llevo al hablago y le pregunto a Pablito a ver cómo quiere hablarlo.

Eso por un lado. Segundo, segundo punto. Estos otros problemas que no son estrictamente este del 10% extra y que se yo que estamos comentando, eso cómo los encaramos, digamos. relevados y documentados en algún lado o son cosas que ustedes saben que pasan pero que no tenemos, no tenemos relevamiento, no están, no sé...

queridos o cosas por el estilo. Están en el backlog de Cámico Atricochi, por ejemplo, para decir algo, Magui. No, no, porque hoy lo resolvemos, estamos levantando la mano. diciendo, che, esto en algún momento va a ser inadministrable, el prestador ya se queja también, viste, de estos parches, de estas atadas con alambre, hoy lo estamos resolviendo, pero bueno.

Nos gustaría pensar en algo superador, armar algo... Totalmente, digo...

Son dos temas diferentes de lo que dijimos antes y esto, digamos, o vos crees que la solución a el tema del 10% extra, para ponerle un nombre, también va a solucionar alguno de estos problemas? problemas. No, no, no, no creo que, que soluciones. Y entonces, mi sugerencia ahí, digo, a ver qué te parece, es, che, estas cuestiones que, muy bien decís vos, mirá, hoy lo podemos gestionar.

así con un parche, pero esto se nos va a desmadrar prontamente. Vamos a hacerlo así. Vale la pena evaluarlos con Kami y tratar de sistematizarlos en el sentido de tratar de tener buena información concreta y demás del problema y decir, che mira, el quilombo es este, ya sabemos cuál es el quilombo, ya sabemos eventualmente cuál es la solución y lo ponemos en backlog para poder tenerlo, aunque sea, solucioname esto, que hoy no podríamos decirlo, no?

Sí, igual me gustó lo que mencionó Anto, esto de crear la burbuja de medicamentos, porque hoy medicamentos se entiende como que es definir un porcentaje de cobertura, y no es así, no es solo el porcentaje de cobertura. Y no hay un apartado, no hay un lugar donde hoy podamos plasmar la regla de medicamentos. Están todos en Sheet, Excel, en… ¿Me explico? No hay campo.

Entonces son tres cosas, una es lo del 10%, vamos por esa que yo hablo con Pablo y vemos y les traigo una respuesta de esta misma. Sí, perdón. No, quería aclarar que lo del 10% hoy, esta medida, ya está, digamos, definida con el prestador que reciben una marca ellos, ¿no?

No, no, está bien, está bien, Dio, pero eso es lo del padrón. Exacto, como lo vamos a marcar en adelante, perfecto. Perfecto, perfecto. Entonces, son tres cosas. Lo del 10%, ver una mejora a esta marca que tenemos hoy por padrón para que sea más fácil de mantener. Segundo, las cosas que son pasibles de ser vistas como

en ese paquete, ya toda tuya. Y tercero, pensar. Bueno, que Anto nos iba a invitar a la reunión de productos, perdón, viernes que viene. Perfecto, para pochar el pancito ahí y ver si tenemos una burbuja de medicamentos donde, como muy bien decir vos, la configuración de medicamentos no es solamente el porcentaje de cobertura en farmacia, sino un montón de otras cuestiones que hacen al plan, digamos, en particular. Insisto igual en este punto, pero conceptualmente, y lo digo casi para yo entenderlo, a ver si lo estoy entendiendo bien.

Eso de la burbuja está fenómeno y hay que hacerlo, obviamente, para no estar dependiendo de... cosas que están configuradas en algún lado, pero eso afecta a cada plan individual, correcto? Bien, listo. O sea que eventualmente si hiciéramos lo del 10% por fuera, no iría ahí en la burbuja.

Claro, yo aprovecho para preguntar a Magui y a Iba porque un poco lo tenía ahí como como duda Además de porcentaje, además del listado de exclusiones, ¿qué otras cosas manejan? Bueno, anticonceptivos. De acuerdo al plan, se dice si se dan todas las marcas o solo algunas. Ahí está. Hay seis listados.

¿Qué? Que contemplan productos distintos y porcentajes distintos. Es decir, uno que contempla cinco marcas comerciales, todas al cien. Y todos que contemplan, 50 marcas comerciales, 25 con cobertura al 100, 25 con cobertura de plan. O sea, seis listados de anticonceptivos. Otro de anticonceptivos, sí. Después tenemos Vademecum. Sí. Sustentable, R3D, el VPC, ta, ta, ta, no sé si hay algún otro más. Programa 29, que es el listado de exclusión de droga del 1000 para abajo.

Claro, bueno, todo eso ya no, nutrientes dérmicos, claro. Eso es sí. Y también que vos decías, bueno, eso también entra a jugar después. Vacunas. Bueno, no, nada, pero simplemente para...

Se desconocían mis perrachas. Bueno, Anto. Gracias por el tiempo. No, por favor. Esperamos entonces que lo veas con Cami, en todo caso nos empezamos a juntar para trabajar. Lo veo con Pablito primero, para ver si hay que hablar con alguien más, aparte de con la PO, viste, por el tema de...

de los de los supres, qué sé yo, para armar un poquito de discusión y sí, les contesto o les mando autorizaciones en el chat de esta misma reunión, ¿les parece? Bueno, a mí me parece también que va a ser muy importante tener como una visión del contexto y hacia dónde queremos ir.

y a partir de eso decir bueno y en el mientras tanto qué podemos hacer cuál es el entregable en un tiempo que se yo para el 2026 aunque sea para fin mediados este año. Muy lejos Adri, a la solución. Bueno, siempre que se planteó nos sacaron a los bolsazos, a una alternativa distinta de no generar este...

tengo respuestas de gente de Sistema que me decían, tendrás que crear un plan por asociados si fuera necesario. Bueno, yo no lo pudo mostrar más a eso, ya está, vamos allá otra vez. Ojalá se pueda hacer en un tiempo mucho más corto, claro que sí, pero bueno.

pudiéramos sacar de la configuración de plan en tema del porcentaje de cobertura en farmacia, que es un poco digamos lo que estamos tratando de ver, ¿no es cierto? Anto decía, che, yo te haría debajo un montón de plan Digo, ¿tienes un estimado, no te estoy pidiendo la métrica, pero un estimado en tu cabeza de cuánto estamos hablando? Digo, ¿son 5 planes o son 100?

No, deben ser como 100 por lo menos. Mínimo. Mínimo. Me arriesgaría a decir que un 70% del total de planes. ¡Epa! ¡Me gusta! Sí, sí, sí, sí.

cuando les gritan mucho se hacen pis encima, así que vamos a gritarles, no te preocupes. Ok, ok. Bueno, nos vemos. Muchas gracias. Chau amigos. Chau, chau.



▶ **20260119 **Reunión de Definición de Nuevo Endpoint para Programas Preventivos****

<!-- unknown block type: transcription (2ed2c02a...) -->



### Objetivo Principal

- Se decidió crear un nuevo endpoint específico para que Colegio y Compañía puedan consultar los programas preventivos/crónicos de afiliados  
- Este nuevo servicio no requerirá validación de token del afiliado, a diferencia del servicio actual 
- El objetivo es que sea un servicio informativo que devuelva información sin realizar validaciones 
### Integración y Flujo de Trabajo

- Colegio y Compañía primero realizarán la elegibilidad en su servicio actual para obtener datos de cobertura y la marca de crónicos 
- Cuando reciban el ID del programa 1 (Crónicos), llamarán a este nuevo endpoint para conocer los medicamentos y demás información 
- El servicio se actualiza automáticamente, no requiere esperar ejecución de procesos batch  
### Definiciones Técnicas Pendientes

- **Datos a devolver**: Pendiente definir qué campos específicos necesitan Colegio y Compañía del servicio de Cami  
- Existen dos servicios disponibles: uno para Salesforce y otro para webapp/canal conversacional 
- El servicio de Salesforce devuelve: código afiliado, marca comercial, monodroga, potencia, droga, presentación, acción farmacológica, porcentaje de cobertura, cantidad de envases 
- Se sugiere incluir datos del formulario y porcentaje de autorización, pero excluir información que la farmacia ya tiene por otros medios   
### Estrategia de Implementación

- Se desarrollará un único servicio para ambos prestadores (Colegio y Compañía) con credenciales distintas  
- La decisión es ir con una propuesta propia en lugar de adaptarse a lo que los prestadores tengan actualmente    
- Colegio tendrá que adaptarse sí o sí ya que no tienen alternativa (no pueden ir con Farmalinguis)  
- El mismo endpoint funcionará para ambos prestadores sin ajustes específicos por prestador 
### Timeline y Próximos Pasos

- El próximo sprint inicia el lunes  
- Refinamiento programado para el jueves, con planning el lunes   
- El equipo necesita tener el requerimiento detallado para el jueves para poder hacer preguntas antes del inicio del sprint 
- Se espera poder responder con las definiciones durante la semana 
### Consideraciones del Programa Preventivo

- La herramienta actual genera un formulario y receta por cada medicamento 
- En el futuro, los socios podrían prescindir de generar documentación y solo recibir la información mediante servicio 
- Algunos programas solo generan receta, otros generan receta más formulario 
- Se mencionó que el programa saldrá primero con discapacidad 
### Action Items

- [ ] Cami compartir documentación del servicio con Maga  
- [ ] Maga definir qué campos son obligatorios para devolver en el servicio 
- [ ] Equipo preparar requerimiento detallado para refinamiento del jueves 
- [ ] Informar a Colegio y Compañía sobre el nuevo servicio y compartir documentación 


[https://docs.google.com/document/d/1_iRxiXtuIpv0IxZekdKO9y5m6VZXUhWErjmG47FJIsQ/edit?usp=sharing](https://docs.google.com/document/d/1_iRxiXtuIpv0IxZekdKO9y5m6VZXUhWErjmG47FJIsQ/edit?usp=sharing)



incorporábamos al servicio actual, se hacía un nuevo servidor y demás. Lo estuvimos viendo con el equipo y bueno, el líder técnico participó de las reuniones y lo que se... ser un nuevo endpoint, más que todo también por el tema de la validación del token del afiliado, que si no, si colegio y compañía quisieran consultar los programas que tiene cada afiliado van a tener que ingresar un token, porque ese servicio requiere token sí o sí.

Así que la idea que surgió es hacer un nuevo standpoint, solo para consultar y para hacerse de los programas, colegios y compañías, que no tenga la variación de token del afiliado, que va a ser... posterior a la elegibilidad que ellos van a hacer en el servicio para traerse los datos de cobertura y demás, donde van a recibir o no la marca de crónicos.

Quizás el ajuste que puede tener Colegio y Compañía de su lado es que cuando reciben el ID, el programa 1 Crónicos, llamar a este nuevo INPUT y conocer cuáles son... los medicamentos, demás, que eso sería la integración con el servicio de Cami. Ahí en base a eso lo que nos surgieron eran algunas dudas, bueno después igual si no lo voy viendo con vos Cami, pero es en base a lo que trae ese servicio.

Y para ustedes, Maga o Jime, ¿qué necesitamos devolverle a Colegio y Compañía? ¿Qué necesitamos mostrarles? ¿Qué de todo lo que devuelve el servicio de Cami? ¿Qué sí o sí tiene que estar en ese servicio que no? Viste, porque ahí desconozco qué información es la que necesita Colegio y Compañía para tomarlo, y lo otro es cómo se actualiza o de qué manera impacta, no sé, cuando vos cargas un nuevo alfibiado crónico.

Si es el servicio automático.

las motos que pasan acá. Si ese servicio es automático o hay que esperar que corra algún Spoon o algo para que impacte, no sé, una nueva alta, por decir. Eso es automático, Mati. Ah, genial. No, viste, por ahí quizá tenía que esperar, si no, al día siguiente para que corra el Spoon, decíamos, íbamos a estar por ahí con esa demora.

Bueno, buenísimo. Eso es automático. Y esperate que quiero buscar la documentación. Sí.

Yo te había compartido el que devuelve toda la info El que llegan a consumir desde Salesforce Vos me pasaste dos, uno que es el para desde Salesforce dice, y otro que es para consumir desde webapp y canal conversacional ¿Y ustedes tomaron? Tenemos los dos cargados en la Betty, después tenemos que definir también cuál de los dos vamos a usar en base a los datos que necesitemos, ¿no?

Ahí, bueno, en The Salesforce te devuelve el código alfabeto, la marca comercial, Monodroga, potencia, droga, presentación, la acción farmacológica. el porcentaje de cobertura, la cantidad de envases, etcétera, de completa. Claro, por eso la idea era conocer de qué dictó esa respuesta y lo que le tenemos que devolver a Colegio, a compañía y más.

Ah, no vi que estabas compartiendo Sí, mi compu le lleva, pero ahí va Hay no sé, más necesario validar los conejos o lo podemos definir nosotros. Hay que pensar bien en el objetivo, digamos, qué es lo que queremos. de este intercambio, porque pensábamos, la semana pasada hablábamos con Jime pensando en el programa preventivo que se va a implementar, primero vamos a salir con discapacidad.

Y bueno, hay casos donde por ahí son muchos los medicamentos que se empadronan, hoy por hoy la herramienta está preparada para generar un formulario y una receta por medicamento. Tal vez el día de mañana los socios podrían prescindir de generar esa documentación y devolverle mediante servicio, que es lo que está empadronado, digamos, que solo tengan que generar la autorización.

y puedan consumirlos sin llevar ningún tipo de documentación, se me ocurre. Es decir, para algunos casos podríamos devolver incluso el porcentaje de autorización que se emitió. Así que bueno Tiene la receta ahí, pero por ejemplo esto no creo que sea necesario porque la tiene por otro lado ya la farmacia Exacto, exacto, pero sí los datos referentes al

formulario, digamos. Es claro. Así que, y también creo que va a depender de lo que tiene empadronado o la funcionalidad del programa preventivo, vieron que en algunos casos se van a habilitar programas que solo generan receta, otros que generan receta más formulario.

Pero bueno, ¿nos lo llevamos para analizar a eso? Claro, este por lo que veo del otro servicio Cami devuelve como más acotado

Bueno, cuál es su compañía, Vigencia D, ¿está? ¿Será necesario? Ah, perdón, nada. Sí, sí, sí. No, quería decir respecto de la vigencia que entiendo que ellos deberían consultar al momento de la validación Y si no lo devuelve, no lo devuelve, claro. Exacto, no deberían, en principio, conocer hasta cuándo lo tiene habilitado. Ahí, Mati, no sé si validaron, de última si necesitan que generemos un servicio nuevo para ustedes.

No, nosotros el análisis lo hicimos en base a estos servicios que vos nos compartiste, o sea, para utilizar esto, consumirlo, pero sí nosotros crearíamos un nuevo endpoint para compartir con cualquier compañía. Muchas gracias.

En.

Pero sí, lo que necesitamos definir es eso, qué tiene que devolver ese servicio en base a esa persona puntual que va a buscar, por número de personas, por lo que veo acá. tomar los datos y devolvérselo en este nuevo servicio para colegio y para compañía. Perfecto. Ahí, Mati, nosotros iríamos con una propuesta a los prestadores.

¿O se tuvo en cuenta algo de lo que ellos hoy tienen, esta documentación que en su momento habían compartido? Sí, de eso no tenemos nada, creo que habíamos hablado, Jime, que lo tenía Jero en su momento, pero yo no tengo nada de esa nueva, de ese... La propuesta sería de nosotros hacia ellos o les gustaría conocer si hay algún servicio que ya tengan?

Y si es más factible que desarrollen o que nosotros ajustemos en base a algo que ya tienen, en total no lo tenemos desarrollado, sería que lo podemos acomodar o almoldar a ellos, vamos por eso, también vamos a consultar. a ellos que tienen disponible y de qué manera les serviría, ¿sí, Jimena? Ahí, Mati, pensar que son los dos, ¿no? Colegio y compañía, dice que no suelen, digamos, tener las mismas ideas a veces.

¿Conviene esto, de ver qué es lo que tienen y amoldarnos, o conviene pedir algo desde Sandor para que ellos amolden? ¿Cuál es...? ¿Cuál es el ejercicio que tendríamos que hacer para ver quién se tendría que llevar el esfuerzo mayor? Claro, a ver, lo ideal sería nosotros irle con el Belélem...

Tenemos este servicio que te va a volver los programas preventivos de esta forma y hacerlo, pero bueno, si es después que se demore el desarrollo o que sea una negativa de ello y. Y ya que no lo tenemos desarrollado, digo, eso me lo dirán ustedes, chicas del lado de... Que ellos no lo hagan, es que ellos no pueden vender básicamente, así que olvidate de eso, lo van a tener que hacer sí o sí, porque nosotros siempre tenemos ahí como, ah bueno, me voy con farmalinguis, no somos los malos.

Nada, digo, es muy difícil que te digan que no, sí, tenés razón en eso, sobre todo colegio, compañía, las prioridades un poco se las damos nosotros, pero creo que es lo más difícil. pero no me preocupa tanto como el otro, y es más manejable desde lo político colegio.



Para mí lo ideal es hacer algo y que ellos amoldan. Sí, a ver, ¿qué nos beneficia a nosotros que vamos a hacer un único servicio para los dos y no vamos a estar ajustando…? Esto para colegio, esto para compañía, porque si le vamos a preguntar, como decís vos, nos van a pedir cosas distintas o cada uno nos va a pedir, nos volvemos a como lo tienen.

En este caso desarrollamos un servicio para ambos, con credenciales distintas de última para saber quién lo está consumiendo, pero el mismo endpoint y ya está. Ah, ese es mi pensamiento, no sé, Marco, ¿vos hay alguna? ¿Qué opinás? Por cualquier cosa, capaz que la compañía tiene que ir para otro lado y nada que ver, pero... La verdad que no tengo una respuesta ahora porque no sé cómo lo han manejado antes, lo que les haya funcionado anteriormente

Y creo que siempre vamos planteándole lo que tenemos y cómo lo vamos a devolver y creo que esa línea nos viene funcionando, por decir esto, no sé, la cobertura diferencial. Sí, y por ahí haciendo memoria a experiencias anteriores, creo que se ha solicitado la documentación de lo que tenían los prestadores

y de hecho para lo que es información de consumo en línea creo que se tomó la base de lo que tenía colegio, Praxis, en función a eso se desarrolló internamente, después se pidió a compañía que se adapten a eso, digamos. es como que también se basaron en desarrollar en lo que algunos de los prestadores tenían, pero por eso pregunto, digamos, ¿íbamos a ir nosotros con la propuesta o les interesa conocer?

Y los prestadores hoy ya tienen algo.

Es que por eso digo, no lo tenemos desarrollado, si nos vamos a moldar a lo que tienen ellos lo podemos hacer también, no es que tenemos que modificar lo que ya hicimos, por suerte no lo tenemos que modificar porque es algo nuevo Pero si la postura es vamos a armarlo y se lo pasamos a ambos como está, también lo tomamos por eso.

Bueno, si les parece, entonces lo que quedaría pendiente es que definamos qué necesitamos que se devuelva a los prestadores, qué info ahí para ICAM y vos le podés compartir a Maga lo que se devuelve, y en base a eso, mira, estos campos sí o sí son obligatorios para devolver en el servicio.

Y bueno, te pido, Maga, como te hacemos últimamente con el GoWop, entonces yo les voy terminando de ahí. De todos modos, la idea sería poder arrancarlo en el Spring, que arranca el lunes próximo. Nosotros tenemos refinamiento ahora el jueves. bien porque tenemos espacio para meterlo en el equipo web service obviamente si no se llegó a definir algo no lo ponemos después lo subimos a mitad screen

pero si tenemos definiciones o qué, al menos para empezar a desarrollar el servicio nuevo, genial. Bueno, ¿verdad? Obviamente si vamos a ir a consultar a Colegio Compañía no sé qué se va a demorar, pero... Yo diría, Magui, que hagamos lo propio y ya le vayamos informando a Colegio y a Compañía que se le va a pasar la documentación y listo.

es un servicio que no te va a devolver ningún es informativo o sea vuelva a consultar con el número de la persona en este caso ellos van a ingresar credencial o lo que quieran y le va a devolver info, más que eso, no hace ninguna validación ni nada Bárbaro, bárbaro Bueno, llevamos para ver eso y...

Y en el transcurso de la semana, entiendo, ya podríamos responderle. ¿Cuándo inicia el próximo RIM, Mati? El lunes, pero nosotros tenemos el recinamiento jueves, o más tardar podemos hacerlo viernes, y el lunes la planning, que ya dividimos las tareas.

Ah, ok. O sea, nosotros tenemos que llevarle al equipo el jueves la petición con el requerimiento ya detallado de lo que hay que hacer. Para que ellos nos planteen dudas o algo para que nos podamos dar vuelta y preguntarle antes del lunes que arranca el sprint.

Bien. Maggie, vos estás libre ahora, si querés, nos quedamos.







### 📄 Propuesta de QMT

[https://docs.google.com/document/d/1uR4kXzlHVxcukgXtTjPPKdmtlOJ8whbZIq9iggApf5o/edit?usp=sharing](https://docs.google.com/document/d/1uR4kXzlHVxcukgXtTjPPKdmtlOJ8whbZIq9iggApf5o/edit?usp=sharing)



