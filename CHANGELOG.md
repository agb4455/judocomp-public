# Novedades de JudoComp

Lo que cambia en cada versión, contado para quien usa el programa. Cada versión se descarga en
[Releases](https://github.com/agb4455/judocomp-public/releases); cómo usarla, en la
[guía de uso](docs/guia-de-uso.md).

Las versiones siguen `mayor.menor.corrección`. Mientras JudoComp está en construcción, cada número
menor cierra un bloque de funcionalidad; la 1.0 será la primera con una liga completa de principio
a fin.

## [0.7.0] - 2026-11-11

No hay 0.5 ni 0.6: esta versión reúne los tres bloques que se hicieron desde la 0.4.0.

### Novedades

- **La categoría que vuelve a entrar con hoja personalizada llega a JudoShiai**: si un cambio de última hora vuelve a meter en el torneo a una categoría con hoja personalizada, viaja a JudoShiai con su hoja. Si la hoja no se puede pasar (no está cargada, con otra versión o no admite a sus competidores), el cambio queda guardado en JudoComp y los pasos a mano dicen con qué hoja crearla.
- **Juntar hacia una categoría que ya no existe se rechaza**: la opción de juntar una categoría de un solo competidor rechaza como destino una categoría que haya sido eliminada de la liga, y si ya estaba guardada se marca como que la decisión ya no vale.
- **«Volver a generar» no cierra JudoShiai si tiene otro torneo abierto**: al volver a generar un torneo, JudoComp comprueba primero qué tiene abierto JudoShiai; si tiene el torneo de otro turno (o un archivo tuyo), avisa y no lo cierra, para no dejar a otro turno sin marcador. Tampoco cierra si JudoShiai no responde. Y con «Seguir con el torneo que hay» comprueba que JudoShiai esté cerrado antes de marcar el archivo que ya estaba como el del turno.
- **Quien pasa en su ficha a una categoría de otro turno sigue en el turno donde se generó**: si un competidor que ya está en el torneo de un turno generado cambia en su ficha a una categoría de otro turno de la misma jornada, sigue en el turno donde se generó; ningún otro turno lo incluye al generarse ni lo cuenta en la planificación.
- **Pasos a mano más completos en el cambio de última hora**: si el cambio queda guardado en JudoComp pero JudoShiai no lo hace, los pasos para hacerlo a mano ahora dicen también qué hacer con una categoría que sale del torneo (borrarle el sorteo, y limpiar antes sus combates si los tenía), y, si quien cambia de categoría estaba solo en una con el 1.º sin combatir o sin puesto, dicen que lo añadas en la categoría nueva, porque JudoShiai no lo tenía en la anterior.
- **JudoComp sabe qué torneo tiene abierto JudoShiai**: al generar un turno, JudoComp deja anotado en el archivo del torneo de qué turno es, y a partir de ahí sabe cuál tiene JudoShiai abierto sin adivinarlo. Si JudoShiai tiene abierto el torneo de otro turno (o un archivo tuyo que no es de JudoComp), el paso «Competir» lo dice, «Sortear» no hace nada y el cambio de última hora avisa «JudoShiai tiene abierto otro turno. Ábrelo para hacer este cambio.» antes de elegir nada: no se hace copia, no se guarda ni se cambia el historial. «Rehacer una categoría» tampoco cierra JudoShiai si tiene otro turno abierto, para no dejar a un tatami sin marcador. Con «Seguir con el torneo que hay» el archivo que ya estaba queda marcado como el del turno.
- **Una categoría que salió del torneo puede volver a entrar**: si en un cambio de última hora una categoría sale del torneo (por ejemplo, se queda con uno y se decide darle el 1.º sin combatir) y luego otro cambio la vuelve a meter, JudoComp la entra de nuevo en JudoShiai y el cambio sale hecho. Antes decía «Hecho en JudoComp, falta JudoShiai» y había que crearla a mano. Una categoría con gente dentro sigue sin tocarse.
- **Bajas y cambios de categoría de quien estaba juntado o con la categoría decidida**: en el cambio de última hora, quien compite en una categoría a la que se juntó otra, y quien tiene el 1.º sin combatir, sin puesto o gana sin combatir, se puede dar de baja o cambiar de categoría como los demás. Un juntado se da de baja o se cambia en la categoría donde compite, y si en ella se queda solo el juntado de otra categoría, gana sin combatir y el asistente no pregunta nada. A quien no estaba en JudoShiai, el asistente le dice «Solo cambia en la liga: esta persona no estaba en JudoShiai» y no toca JudoShiai. La decisión de la categoría de quien se va se quita sola. Se acabó el caso sin salida en que el asistente pedía decidir sobre una categoría que ya no tenía a nadie.
- **Competir sigue lo que se generó**: una vez generado el torneo de un turno, «Competir», el sorteo, «Rehacer una categoría» y el cambio de última hora trabajan con lo que se generó para ese turno y no con la liga de hoy: si cambias a un competidor de categoría o el sistema de una categoría después de generar, el turno no vuelve a salir como «sin generar», no pierde categorías ni competidores, y rehacer una categoría la deja con el sistema con el que se generó. A quien se borra de la liga no se le ofrece en el cambio de última hora. Las pantallas de competidores y de categorías, con una jornada en competición, avisan de que sus cambios no llegan al torneo y de que para la jornada hay que usar «Cambio de última hora»; y no se puede borrar una categoría que está en el torneo de la jornada en competición.
- **Cambio de última hora más claro**: cuando un cambio de categoría deja a la categoría de origen con un solo competidor, el asistente pregunta solo por esa categoría y dice cuál es; antes enseñaba también una pregunta falsa por la categoría de destino, cuya respuesta se rechazaba. La vista previa y «Confirmar» hacen siempre lo mismo, y el cambio se aplica sobre lo que se generó para el turno, aunque la ficha del competidor haya cambiado después. Si JudoShiai no acepta una pérdida de combates por hansoku-make, ya no queda anotado en el historial que se hizo.
- **Una categoría con uno, decidida siempre**: una categoría con un solo competidor se decide en el momento (1.º sin combatir, sin puesto, juntarla con otra o subirlo a otra categoría) tenga el sistema que tenga, también uno fijo como pool o doble pool o una hoja personalizada, en la planificación, en la revisión del pesaje, al generar y en un cambio de última hora. Hasta ahora, con un sistema fijo, pasaba sin preguntar y JudoShiai recibía una categoría sin combates.
- **Preguntar antes de cerrar**: al cerrar JudoComp, con la ventana o con «Cerrar JudoComp» del icono junto al reloj, pregunta si hay algo a medio escribir (guardarlo, descartarlo o seguir editando), como al salir de una pantalla. Si la liga tiene una jornada en competición, avisa de que JudoShiai y los marcadores siguen funcionando y de que al volver a abrir podrás seguir; con «Cancelar», JudoComp sigue abierto como estaba.
- **Seguir con la jornada al abrir la liga**: si la liga tiene una jornada que estaba en competición y JudoShiai no está abierto, al abrir la liga (o al arrancar JudoComp con la última liga abierta) un aviso pregunta si quieres volver a abrirla en JudoShiai para seguir donde se quedó; con «Seguir en JudoShiai», abre en JudoShiai el turno que estaba compitiendo, como «Volver a abrir JudoShiai», y te lleva al paso «Competir».
- **Combates disputados en cambios de última hora**: si una categoría afectada ya tiene combates disputados, el asistente pregunta qué hacer: rehacer la categoría (se pierden los combates disputados para repetirlos) o, en una baja de una categoría sin terminar, que el judoka pierda los combates que le quedan por hansoku-make (se conservan los disputados). Si mientras tanto se disputan más combates, vuelve a preguntar con el número nuevo, y si JudoShiai no lo hace automáticamente, da los pasos a mano para marcar hansoku-make o limpiar los combates.
- **Entrar en una categoría decidida en cambios de última hora**: en un alta o un cambio de categoría también se puede elegir una categoría que estaba resuelta sin combates (1.º sin combatir, sin puesto o juntada con otra): al confirmar, esa decisión se deshace y la categoría entra en el torneo con los dos. Si no tenía tatami, el asistente pide elegir en cuál va, y si JudoShiai no la crea, dice cómo hacerlo a mano.
- **Es nuevo en la liga en cambios de última hora**: en el asistente de cambio de última hora, al dar de alta a un competidor se puede elegir «Es nuevo en la liga» con su ficha mínima (nombre y apellidos, pesándolo en el propio asistente); JudoComp crea su ficha, le asigna el número libre que le corresponde y lo da de alta en la jornada y en JudoShiai en una sola operación.
- **Categoría que se queda con uno en cambios de última hora**: si una baja o un cambio deja una categoría con un solo competidor, el asistente pregunta qué hacer (darle el 1.º sin combatir, sin puesto o juntar con otra más pesada de su mismo turno) antes de confirmar.
- **Cambio de última hora en «Competir»**: el asistente de cambio de última hora permite hacer altas, bajas y cambios de categoría con la jornada en marcha, antes de que la categoría tenga combates. Explica qué va a pasar con cada categoría afectada, si hay que rehacer el sorteo y, si JudoShiai no lo hace automáticamente, indica los pasos para hacerlo a mano.
- **JudoShiai y la competición en vivo**: la barra de estado enseña si JudoShiai está abierto (verde), no abierto (gris) o no responde (rojo). El paso «Competir» se actualiza solo cuando cambia algo en JudoShiai (categorías que empiezan o terminan, combates disputados), avisa con una franja roja y ayuda si JudoShiai deja de responder, y marca con una franja verde cuando todas las categorías de un turno han terminado.
- **Comprobar los tatamis en vivo**: con una liga abierta, JudoComp comprueba los tatamis de la sede cada pocos segundos y enseña en «Sede y puestos» si el marcador está conectado a JudoShiai (verde), si está abierto sin conectar (naranja), si el PC está encendido (gris) o sin respuesta (rojo), junto a cuándo respondió por última vez y «¿Qué hago?» si no está conectado. La barra de estado añade un punto por tatami con su color y su información al pasar el ratón, y pulsar un punto lleva a la sede.
- **El paso «Competir» de la jornada**: con el torneo de un turno abierto en JudoShiai, enseña sus categorías con su tatami, cuántos compiten, en qué punto está cada una (sin sortear, sorteada, empezada o terminada) y sus combates. «Empezar a competir» sortea en JudoShiai, tras confirmarlo, las que faltan; cada una también se puede sortear sola.
- **Aviso de la hoja que no admite a sus competidores**: el plan y la revisión del pesaje avisan cuando una hoja personalizada no admite a los competidores de su categoría, antes de generar.
- **Decidir una categoría de uno durante el pesaje**: en la revisión del pesaje, una categoría que se queda con uno se puede decidir antes de cerrar el pesaje aunque falte por pesar alguien de ella; si luego se pesa, la decisión se marca como que ya no vale.
- **Preparar cada turno por separado**: con el torneo de un turno ya generado, los demás turnos se siguen pesando, revisando y cerrando, y cada turno se genera con sus propios problemas.
- **Hojas personalizadas**: desde Categorías, «Hojas personalizadas» lista las hojas de la liga, con las categorías y
  jornadas que las usan y si JudoShiai ya las tiene cargadas. Se añaden desde sus archivos, se ven sus páginas, se borran
  si nadie las usa y se cargan en JudoShiai con un paso guiado.
- **Elegir la hoja**: el panel de cada categoría, el plan de una jornada y la revisión del pesaje ofrecen las hojas
  personalizadas de la liga, por su nombre, después de los sistemas de JudoShiai. Cada jornada puede usar una hoja
  distinta de la de su categoría, y la lista de categorías enseña el nombre de la hoja.
- **Tiempo de combate de cada categoría**: en el panel de cada categoría se elige cuánto dura su combate, de 30 segundos
  a 10 minutos de 30 en 30, y la lista de categorías lo enseña en su propia columna. El catálogo propone 3 minutos
  para infantil y 4 para el resto; las categorías nuevas empiezan en 4 minutos y duplicar una copia su tiempo. Las ligas
  creadas con una versión anterior pasan a 4 minutos en todas sus categorías al actualizarlas: se corrigen desde el panel.
- **Borrar lo que usan las jornadas**: no se puede borrar una categoría que una jornada use como «solo esta jornada»
  ni quitar un tatami que esté en el plan de una jornada sin cerrar. Al borrar un competidor se borra también lo que
  tenía en las jornadas, y quien se dé de alta después ya no hereda nada suyo.
- **Jornadas**: la lista de jornadas de la liga, con nueva jornada, cambiar su fecha o nombre y
  borrar una que aún está en preparación.
- **Los pasos de una jornada**: cada jornada se lleva en ocho pasos (Convocar, Planificar,
  Pesar, Generar, Competir, Volcar, Cerrar y Publicar). JudoComp marca el paso en el que está
  según su estado y dice qué falta para el siguiente.
- **Convocar**: quién participa en la jornada y quién no (con un motivo, si se quiere), en qué
  categoría compite cada uno solo esta jornada o a partir de ahora, añadir un competidor nuevo desde
  la propia convocatoria y cerrarla.
- **Planificar la jornada**: turnos, tatamis, sistemas y qué hacer con las categorías de un solo
  participante (darle el 1.º sin combatir, juntarla con otra, subirlo a otra categoría o que
  participe sin puesto). Si una categoría juntada con otra se queda sin participantes en la de destino,
  gana automáticamente sin combatir. Al dar la planificación por buena, la jornada avanza a Pesar.
- **Aviso del sistema que JudoShiai no hace**: el plan y la revisión del pesaje avisan cuando el sistema de una categoría
  no sirve para los competidores que irán a JudoShiai. Por ejemplo, «al mejor de tres» con 5: JudoShiai solo lo hace con 2
  y con 5 sortearía una eliminatoria. El aviso no impide dar la planificación por buena.
- **Juntar solo hacia arriba**: una categoría de un solo participante solo se junta con una más pesada, nunca con una más ligera.
  Por eso la propuesta ya no baja a la categoría de al lado, y el selector solo ofrece las más pesadas.
- **Pesar**: pesar a los participantes de la jornada, por turno o de toda la jornada,
  con la entrada rápida de número y peso, ver quién falta y quién no entra en su categoría
  (para pasarlo a otra categoría para esta jornada o dejarlo), o dar por pesados a varios sin peso nuevo.
- **Pesaje con un archivo CSV**: cargar los pesajes desde un archivo CSV con resumen previo antes de aplicar,
  mostrando filas con problemas y avisos de fuera de peso.
- **Cerrar y reabrir el pesaje, con su revisión: no presentados, fuera de peso, categorías de uno y sistemas que cambian**:
  al cerrar el pesaje se revisan los no presentados, los que no entran en peso, las categorías de uno
  y los sistemas automáticos que cambian; con el pesaje cerrado se pueden filtrar los no presentados
  y reabrirlo si hace falta. En jornadas sin pesaje presencial, el pesaje se puede cerrar directamente
  desde la jornada planificada sin abrirlo antes.
- **Generar y abrir en JudoShiai**: cada turno de la jornada tiene su tarjeta en el paso Generar. Con el pesaje del
  turno cerrado, «Generar y abrir en JudoShiai» hace una copia de seguridad, genera el torneo de ese turno y abre
  JudoShiai con él; después indica en qué carpeta dejar los resultados para «Imprimir todo». Si JudoShiai no está en
  el PC o es otra versión, JudoComp lo dice antes de nada. Si el torneo ya está generado, «Volver a abrir JudoShiai»
  lo abre sin generarlo otra vez.
- **Volver a generar el torneo**: en un turno ya generado, «Volver a generar» cierra JudoShiai, guarda el torneo que había
  en la carpeta de copias y genera de nuevo el torneo desde la liga. Solo se puede si en ese turno todavía no se ha
  competido: si ya hay combates con puntos o marcador, JudoComp lo dice y no cambia nada. Si la carpeta de torneos y la
  liga no coinciden (por ejemplo, tras restaurar una copia de antes de generar), JudoComp pregunta si seguir con el torneo
  que hay, volver a generarlo o cancelar.
- **Avisos de estado**: al intentar una acción que ya no corresponde a su estado, el aviso indica el estado
  real en el que se encuentra la jornada.

Los pasos de Volcar en adelante aún no hacen nada: llegan en las próximas versiones.

## [0.4.0] - 2026-10-09

### Novedades

- **Categorías**: la pantalla de categorías, agrupada por años de nacimiento, con su panel para
  crear, duplicar, cambiar y borrar una categoría.
- **El catálogo al crear la liga**: el asistente de crear liga tiene un paso de categorías, con el
  año de referencia y las categorías del catálogo con las que empezar.
- **Proponer categorías**: JudoComp propone la categoría de cada competidor que no la tiene, por su
  sexo, año y peso; se revisan, se marcan y se asignan de una vez, con «Deshacer». Se llega desde
  Categorías y al terminar de importar inscripciones.
- **La categoría de cada competidor** en la lista de competidores (con filtros y orden) y en su
  ficha, con avisos al momento: peso por encima o por debajo, ninguna categoría o varias que
  encajan.
- **Asignar una categoría a varios** competidores a la vez desde la lista, con «Deshacer».
- **El sistema de competición** de cada categoría (automático según el número de competidores, o
  uno fijo), elegido en Categorías y visible en la lista.

### Cambios

- El formato del archivo `.comp` sube de versión. Al abrir con esta versión una liga hecha con la
  0.3.0, JudoComp hace antes una copia de seguridad y la actualiza solo. Una liga actualizada ya no
  se abre con la 0.3.0.

## [0.3.0] - 2026-10-04

Primera versión publicada.

### Novedades

- **Instalación**: instalador de Windows y AppImage de Linux, con todo dentro y sin internet.
- **La ventana de JudoComp**, que se abre desde su icono. En un PC que no puede mostrarla, JudoComp
  se abre en el navegador y lo avisa. Una segunda vez que se abre lleva a la misma ventana.
- **La liga y su archivo**: crear una liga con su tabla de puntos, abrirla, volver a la última al
  arrancar y la lista de las abiertas hace poco. Cada liga es un archivo `.comp` con una carpeta al
  lado con su mismo nombre.
- **Una liga, un JudoComp**: si otro JudoComp tiene la liga abierta, no se abre dos veces.
- **Copias de seguridad**: hacerlas a mano, verlas y restaurarlas, también de una liga dañada.
  JudoComp hace una sola antes de cada operación que lo merece (importar, actualizar el formato,
  restaurar otra).
- **Competidores**: la lista, con búsqueda, filtros y más de mil competidores sin esperas; la ficha;
  dar de baja, volver a dar de alta y borrar, con «Deshacer».
- **Clubes**: añadir, renombrar, unir dos clubes, cambiar el club de varios competidores a la vez y
  avisos de clubes con nombres parecidos.
- **Importar inscripciones** desde CSV, XLS o XLSX en cuatro pasos: elegir el archivo, decir qué
  columna es cada dato (el mapeo se recuerda para la próxima vez), revisar lo que se va a añadir,
  actualizar o saltar, e importar.
- **Si algo falla**, JudoComp lo explica con un aviso y lo apunta en su registro técnico, sin datos
  de los competidores.

[0.7.0]: https://github.com/agb4455/judocomp-public/releases/tag/v0.7.0
[0.4.0]: https://github.com/agb4455/judocomp-public/releases/tag/v0.4.0
[0.3.0]: https://github.com/agb4455/judocomp-public/releases/tag/v0.3.0
