# Guía de uso de JudoComp

Para quien lleva una liga de judo en su club. Lo que cambia en cada versión, en
[Novedades](../CHANGELOG.md).

> JudoComp está en construcción. Lo que llega en la próxima versión se marca como
> *(próxima versión)*, y lo que aún no está, como *(próximamente)*.

## Instalar

1. Descarga el instalador de la última versión en
   [Releases](https://github.com/agb4455/judocomp-public/releases). Si el PC de la competición no tiene
   internet, descárgalo en otro y llévalo en un USB.
2. **Windows**: abre `JudoCompApp-win-Setup.exe`. Se instala para tu usuario, sin permisos de
   administrador, y deja JudoComp en el escritorio y en el menú Inicio. Como aún no está firmado,
   Windows avisa de una aplicación no reconocida: pulsa «Más información» y «Ejecutar de todas
   formas».
3. **Linux**: descarga `JudoCompApp.AppImage`, dale permiso de ejecución y ábrelo con doble clic.

**Actualizar** es instalar la versión nueva encima. Las ligas no se tocan: si una versión cambia el
formato del archivo, JudoComp hace una copia de seguridad de la liga antes de actualizarla.

Para generar y competir las jornadas hace falta también JudoShiai 4.4.1 en el mismo PC.

## La liga

Todo en JudoComp pertenece a una liga, que se guarda en un archivo `.comp`. Al lado del archivo,
JudoComp crea una carpeta con su mismo nombre para las copias de seguridad y los archivos de las
jornadas. **Mueve o copia siempre los dos juntos.**

- **Crear una liga**: en la bienvenida, «Crear liga nueva». El asistente pide el nombre (será
  también el del archivo) y dónde guardarla, la tabla de puntos, que vale para todas las jornadas,
  y las categorías con las que empezar, sacadas del catálogo según el año de referencia.
- **Abrir una liga**: «Abrir una liga», o una de la lista «Abiertas hace poco». Al arrancar,
  JudoComp vuelve a abrir la última. Si la liga tiene una jornada en competición y JudoShiai no está abierto, por ejemplo tras un
  apagón, JudoComp pregunta si quieres volver a abrirla en JudoShiai para seguir donde se quedó, y
  te lleva a «Competir».
- **Una liga solo se abre en un JudoComp a la vez.** Si otro PC la tiene abierta, JudoComp lo dice y
  no la abre. Si ese otro JudoComp se cerró de golpe, al cabo de un par de minutos ofrece «abrirla
  igualmente».

## Competidores y clubes

- **Competidores** muestra la lista con búsqueda (`Ctrl+F`) y filtros. Al pulsar uno se abre su
  ficha; se guarda con `Ctrl+S`. Dar de baja, volver a dar de alta o borrar (que limpia también sus
  participaciones en las jornadas) se puede deshacer desde el aviso que aparece
  abajo.
- **Clubes**: se crean al escribir el club en una ficha o desde la pantalla de clubes, donde también
  se renombran y se unen dos que son el mismo. JudoComp avisa si dos clubes tienen nombres
  parecidos.
- **Importar inscripciones** desde un CSV o un Excel (XLS, XLSX):
  1. elige el archivo;
  2. di qué columna es cada dato. JudoComp recuerda el mapeo para el próximo archivo igual;
  3. revisa qué competidores se añadirán, cuáles se actualizarán y qué filas tienen errores;
  4. importa. Antes, JudoComp hace una copia de seguridad.

## Categorías

- **Categorías** las agrupa por años de nacimiento. Desde su panel se crea, duplica, cambia o borra
  una categoría (solo si no tiene competidores, ninguna jornada la usa como «solo esta jornada» y no está en el torneo de la jornada en competición),
  se elige su sistema de competición (automático según cuántos compiten, uno fijo o una hoja personalizada) y su tiempo de combate, de 30 segundos a 10 minutos: el catálogo propone 3 minutos para infantil y 4 para el resto, y la lista de categorías lo enseña en su columna.
- **Hojas personalizadas**: desde Categorías, el botón «Hojas personalizadas» lista las hojas
  de JudoShiai que la liga guarda, con las categorías y jornadas que las usan. «Añadir hoja» pide los archivos de la
  hoja (un `.txt` con la lógica y sus páginas `.svg`); «Ver páginas» las enseña; «Borrar» solo funciona si nadie la usa.
  «Cargar en JudoShiai» la prepara y te guía: en JudoShiai eliges «Torneo» → «Load Custom Systems» y la carpeta que
  JudoComp indica, y JudoComp espera a que la cargues.
- **Proponer categorías**: JudoComp propone la categoría de quien no la tiene, por su sexo, año de
  nacimiento y peso. Marca las que te valgan y pulsa «Asignar». También se ofrece al acabar de
  importar inscripciones.
- La categoría de cada uno se ve y se cambia en la lista de competidores (también a varios a la vez)
  y en su ficha. Los avisos dicen si el peso se sale de la categoría, si no encaja en ninguna o si
  encaja en varias.

## Jornadas

**Jornadas** lista las de la liga con su fecha y su estado. Desde ahí se crea una jornada, se cambia
su fecha o nombre y se borra mientras sigue en preparación.

Cada jornada se lleva en ocho pasos, de izquierda a derecha. JudoComp abre la jornada en el paso
que le toca y, en «Qué falta», dice qué queda para pasar al siguiente.

1. **Convocar**: marca quién participa y quién no (con un motivo, si quieres). Si alguien compite
   en otra categoría, JudoComp pregunta si es solo esta jornada o a partir de ahora. Desde aquí
   también se añade un competidor nuevo. Al terminar, «Cerrar la convocatoria».
2. **Planificar**: repasa las categorías que compiten en la jornada, cuántos participantes
   tienen y con qué sistema. Puedes cambiar el sistema solo para esta jornada, también por una hoja personalizada. Si alguna categoría queda con
   un solo participante, tenga el sistema que tenga (también uno fijo), decide qué hacer con ella (darle el 1.º sin combatir, juntarla con otra más pesada, subirlo a
   otra categoría o que participe sin puesto); si la categoría con la que se junta no tiene a nadie esta jornada, gana sin combatir. Coloca las categorías en los tatamis de cada turno (arrastrando
   o con «Mover a…»). Al terminar, «Dar la planificación por buena». Si el sistema de una categoría no sirve para los competidores que irán a JudoShiai, o si una hoja personalizada no los admite, la fila lo avisa: JudoShiai solo hace «al mejor de tres» con dos, «pool» de dos a siete y «doble pool» de seis a doce, y fuera de ahí sortea una eliminatoria sin avisar; y una hoja fuera de su rango no se podrá generar. El aviso no impide dar la planificación por buena.
3. **Pesar**: pesa a los participantes solo con el teclado (número y peso) por
   turno o de toda la jornada, mira quién falta y quién no entra en su categoría (puedes pasarlo a otra
   para esta jornada o dejarlo), o da por pesados a varios sin peso nuevo. También puedes «Cargar CSV»
   para aplicar los pesajes desde un archivo, con un resumen previo de los que se pesarán y los posibles
   problemas. Al terminar, «Cerrar el pesaje» muestra la revisión con los no presentados, los que no
   entran en peso, las categorías que quedan con un participante y los sistemas que cambian; tras confirmar,
   quien no se haya pesado queda como no presentado. Si en la jornada no hay pesaje presencial, se puede
   pulsar «Cerrar el pesaje» directamente desde la jornada planificada. Puedes volver a ver la revisión
   o «Reabrir el pesaje» mientras el torneo de ese turno no se haya generado; y, con un turno ya en JudoShiai, los demás se pesan y revisan igual. La revisión avisa de los sistemas que JudoShiai no
   hace con los competidores que pesaron y de las hojas que no los admiten, y deja cambiar el sistema de la jornada allí mismo. Una categoría
   que se queda con uno se puede decidir en la revisión antes de cerrar, contando solo a los pesados; si luego se pesa a otro
   de ella, la decisión se marca como que ya no vale.
4. **Generar**: cada turno de la jornada (o toda la jornada, si no tiene turnos) tiene su tarjeta, con
   cuántos compiten y en cuántas categorías. Cuando el pesaje del turno está cerrado, «Generar y abrir en JudoShiai»
   pide confirmación, hace una copia de seguridad, genera el torneo de ese turno y abre JudoShiai con él. Después
   te indica la carpeta donde dejar los resultados (en JudoShiai, «Resultados» → «Imprimir todo (Web y PDF)»).
   Si JudoShiai no está en el PC, o es otra versión, JudoComp lo dice antes de generar nada: puedes indicar dónde
   está o, con otra versión, seguir igualmente. Si el pesaje del turno sigue abierto, la tarjeta te pide cerrarlo antes.
   Con el torneo ya generado, «Volver a abrir JudoShiai» lo abre de nuevo sin generarlo otra vez.
   «Volver a generar» vuelve a crear el torneo desde la liga: comprueba qué tiene abierto JudoShiai y solo lo cierra si tiene este mismo turno; si tiene abierto el torneo de otro turno (o un archivo propio) o no responde, avisa y no lo cierra para no dejar a un tatami sin marcador. El torneo que había
   se guarda en la carpeta de copias y se abre el nuevo. Solo se puede si en ese turno todavía no se ha competido: si ya
   hay combates con puntos o marcador, JudoComp no cambia nada. Si la carpeta de torneos y la liga no coinciden (por
   ejemplo, tras restaurar una copia de antes de generar), JudoComp dice que el torneo no cuadra y te deja seguir con el
   torneo que hay (comprobando antes que JudoShiai esté cerrado), volver a generarlo o cancelar.
5. Competir: con el torneo del turno generado y abierto en JudoShiai, la tarjeta del turno enseña sus categorías con su tatami, cuántos compiten, en qué punto está cada una (sin sortear, sorteada, empezada o terminada) y cuántos combates se han disputado, actualizándose sola en vivo. «Empezar a competir» sortea en JudoShiai, después de pedirte confirmación, todas las que faltan; también puedes sortear una sola con «Sortear» en su fila. Generar el torneo no sortea nada: así, quien llega justo después del pesaje entra sin rehacer ningún sorteo. Si JudoShiai no está abierto o tiene abierto el torneo de otro turno *(próxima versión: JudoComp lo sabe porque anota en el archivo de cada torneo de qué turno es, y un archivo suyo que no es de JudoComp cuenta como otro turno)*, la tarjeta lo dice y te lleva al paso «Generar», donde puedes volver a abrirlo; si deja de responder durante la competición, avisa con una franja roja y el botón «Qué hacer» para resolverlo sin perder nada. Cuando todas las categorías del turno han terminado, una franja verde lo confirma.

   Con una jornada en competición, la liga se puede seguir cambiando, pero lo que cambies en Competidores o en Categorías no llega al torneo ya generado: esas pantallas lo avisan, y quien pase en su ficha a una categoría de otro turno de la misma jornada sigue en el turno donde se generó. El torneo de cada turno se queda como se generó, aunque después cambies a un competidor de categoría o el sistema de una categoría; para cambiar la jornada, usa el «Cambio de última hora».

   El botón **«Cambio de última hora»**, arriba de las tarjetas cuando hay al menos un torneo generado, abre el asistente para gestionar incidencias con la jornada en marcha:
   - **Pasos del asistente**: eliges qué hacer (alta de alguien de la liga que no competía o de alguien nuevo en la liga con su nombre y apellidos, baja de un competidor o cambio de categoría), buscas al competidor por su nombre o su número (o rellenas la ficha mínima si es nuevo), seleccionas la categoría (en un cambio, de su mismo turno y decidiendo si es solo esta jornada o también a partir de ahora en su ficha; si la categoría estaba resuelta sin combates, entra en el torneo y, si no tenía tatami, se elige en cuál compite) y, en un alta, indicas su peso en kg.
   - **Qué va a pasar**: antes de confirmar, JudoComp consulta el estado en JudoShiai y detalla los efectos en cada categoría: *se hará al momento* (categoría sin sortear con el mismo sistema), *hay que rehacer el sorteo* (avisa de que JudoShiai se cerrará unos segundos para rehacer el sorteo limpio) y, en un alta, el aviso si el peso no encaja en la categoría, como en el pesaje (no impide confirmar). Si una baja o cambio deja una categoría con un solo competidor, el asistente pregunta qué hacer con él (darle el 1.º sin combatir, sin puesto o juntar con otra más pesada de su turno) y permite confirmar; la pregunta dice de qué categoría habla y solo sale por la que se queda con uno (en un cambio de categoría, la que se deja, no la de destino). Quien compite en una categoría a la que se juntó otra se da de baja o cambia de categoría como los demás: en la categoría donde compite, y si en ella se queda solo el juntado de otra categoría, este gana sin combatir y el asistente no pregunta nada. Quien tiene el 1.º sin combatir, sin puesto o gana sin combatir también se puede dar de baja o cambiar de categoría: en una baja, el asistente dice *«Solo cambia en la liga: esta persona no estaba en JudoShiai»* y no toca JudoShiai, y en un cambio de categoría lo añade a la nueva; la decisión de la categoría que deja se quita. El cambio se aplica sobre lo que se generó para el turno, y la vista previa y «Confirmar» hacen lo mismo. Si la categoría ya tiene combates disputados, el asistente indica cuántos combates hay y pregunta qué hacer: rehacer la categoría (se pierden los combates disputados para repetirlos) o, en una baja de una categoría sin terminar, que el competidor pierda los combates que le quedan por hansoku-make (se conservan los disputados); si mientras tanto se disputan más combates, vuelve a preguntar con el número nuevo. Una categoría que salió del torneo y se queda sin nadie puede volver a entrar más tarde con otro cambio de última hora: JudoComp la vuelve a crear en JudoShiai y el cambio sale hecho; una categoría con gente dentro no se toca.
   - **Si falta JudoShiai**: al pulsar «Confirmar», JudoComp hace una copia de la liga, guarda el cambio y lo pasa a JudoShiai. Si JudoShiai no lo hace, sale *«Hecho en JudoComp, falta JudoShiai»* con los pasos para hacerlo a mano en JudoShiai, con el competidor y la categoría ya escritos; si la categoría estaba resuelta sin combates, también crearla en su tatami; si hay combates disputados, marcar hansoku-make o limpiarlos en JudoShiai antes de volver a sortear. Si una categoría sale del torneo, los pasos dicen también que le borres el sorteo (y que limpies antes sus combates, si los tenía), sin volver a sortearla; y si quien cambia de categoría estaba solo en una con el 1.º sin combatir o sin puesto, dicen que lo añadas en la nueva, porque JudoShiai no lo tenía en la anterior. Si JudoShiai no responde antes de confirmar, o al dar el hansoku-make, no se cambia nada: ábrelo y vuelve a intentarlo. Si JudoShiai tiene abierto el torneo de otro turno, el asistente lo dice al llegar a la vista previa, «JudoShiai tiene abierto otro turno. Ábrelo para hacer este cambio.», y no deja confirmar: no se hace copia ni se guarda nada. Lo mismo ocurre con «Rehacer una categoría»: no cierra JudoShiai si tiene otro turno abierto.
6. Volcar *(próximamente)*.
7. Cerrar *(próximamente)*.
8. Publicar *(próximamente)*.

## Sede y puestos

En **Sede y puestos** se configura el nombre del pabellón, la lista de tatamis con su dirección IP y la ruta de JudoShiai. Un tatami usado en el plan de una jornada no cerrada no se puede quitar.

Con la liga abierta, JudoComp comprueba los tatamis cada pocos segundos y muestra el estado de cada uno:
- **Marcador conectado** (verde): el PC del tatami tiene una conexión abierta con JudoShiai.
- **Marcador abierto, sin conectar** (naranja): responde el puerto de JudoTimer en ese PC.
- **PC encendido** (gris): responde al ping en la red.
- **Sin respuesta** (rojo): el equipo no contesta.
- **Sin comprobar** (gris claro): pendiente de la primera comprobación.

Si el marcador no está conectado, el botón «¿Qué hago?» ofrece una comprobación rápida de ayuda. Además, en la barra inferior aparece el estado de JudoShiai («abierto», «no abierto» o «no responde») y un punto por cada tatami con su color; al pasar el ratón se ve su IP y cuándo respondió por última vez, y al pulsar cualquiera de los puntos se abre directamente «Sede y puestos».

Clasificación y Publicación *(próximamente)*.

## Copias de seguridad

**Copias** lista las de la liga abierta, con su fecha y su motivo. «Hacer una copia ahora» guarda una
cuando quieras, con un nombre opcional. JudoComp hace una por su cuenta antes de importar inscripciones,
de actualizar el formato de la liga y de restaurar otra copia.

Para volver atrás, restaura una copia de la lista. Si una liga está dañada y no abre, JudoComp
ofrece restaurar su última copia buena, u otra que elijas, y aparta la dañada sin borrarla.

## Cerrar JudoComp

Al cerrar JudoComp, con la ventana o con «Cerrar JudoComp» del icono junto al reloj, JudoComp
pregunta antes si hay algo a medio escribir: puedes guardarlo, descartarlo o seguir editando. Si la
liga tiene una jornada en competición, también avisa: JudoShiai y los marcadores siguen
funcionando, y al volver a abrir JudoComp podrás seguir. Si dices que no, JudoComp sigue abierto
como estaba.

## Si algo falla

JudoComp explica el error en un aviso y lo apunta en su registro técnico, que no guarda datos de los
competidores. El aviso tiene «Abrir la carpeta del registro»: manda ese archivo a quien te dé
soporte. El registro está en `%LOCALAPPDATA%\JudoComp\Logs` en Windows y en
`~/.local/share/JudoComp/Logs` en Linux.

Si el PC no puede mostrar la ventana de JudoComp, el programa se abre en el navegador y lo avisa.
Para cerrarlo entonces, usa su icono junto al reloj.
