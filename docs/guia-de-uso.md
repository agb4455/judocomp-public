# Guía de uso de JudoComp

Para quien lleva una liga de judo en su club. Lo que cambia en cada versión, en
[Novedades](../CHANGELOG.md).

> JudoComp está en construcción. Lo que aún no está se marca como *(próximamente)*.

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

Para las jornadas hará falta también JudoShiai 4.4.1 *(próximamente)*.

## La liga

Todo en JudoComp pertenece a una liga, que se guarda en un archivo `.comp`. Al lado del archivo,
JudoComp crea una carpeta con su mismo nombre para las copias de seguridad y los archivos de las
jornadas. **Mueve o copia siempre los dos juntos.**

- **Crear una liga**: en la bienvenida, «Crear liga nueva». El asistente pide el nombre (será
  también el del archivo) y dónde guardarla, la tabla de puntos, que vale para todas las jornadas,
  y las categorías con las que empezar, sacadas del catálogo según el año de referencia.
- **Abrir una liga**: «Abrir una liga», o una de la lista «Abiertas hace poco». Al arrancar,
  JudoComp vuelve a abrir la última.
- **Una liga solo se abre en un JudoComp a la vez.** Si otro PC la tiene abierta, JudoComp lo dice y
  no la abre. Si ese otro JudoComp se cerró de golpe, al cabo de un par de minutos ofrece «abrirla
  igualmente».

## Competidores y clubes

- **Competidores** muestra la lista con búsqueda (`Ctrl+F`) y filtros. Al pulsar uno se abre su
  ficha; se guarda con `Ctrl+S`. Dar de baja, volver a dar de alta o borrar se puede deshacer
  desde el aviso que aparece abajo.
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
  una categoría (solo si no tiene competidores) y se elige su sistema de competición: automático
  según cuántos compiten, o uno fijo.
- **Proponer categorías**: JudoComp propone la categoría de quien no la tiene, por su sexo, año de
  nacimiento y peso. Marca las que te valgan y pulsa «Asignar». También se ofrece al acabar de
  importar inscripciones.
- La categoría de cada uno se ve y se cambia en la lista de competidores (también a varios a la vez)
  y en su ficha. Los avisos dicen si el peso se sale de la categoría, si no encaja en ninguna o si
  encaja en varias.

## Jornadas, clasificación y publicación *(próximamente)*

Llevar cada jornada paso a paso con JudoShiai, la clasificación y su publicación llegan en las
próximas versiones. Sede y puestos, también.

## Copias de seguridad

**Copias** lista las de la liga abierta, con su fecha y su motivo. «Hacer una copia ahora» guarda una
cuando quieras, con un nombre opcional. JudoComp hace una por su cuenta antes de importar inscripciones,
de actualizar el formato de la liga y de restaurar otra copia.

Para volver atrás, restaura una copia de la lista. Si una liga está dañada y no abre, JudoComp
ofrece restaurar su última copia buena, u otra que elijas, y aparta la dañada sin borrarla.

## Si algo falla

JudoComp explica el error en un aviso y lo apunta en su registro técnico, que no guarda datos de los
competidores. El aviso tiene «Abrir la carpeta del registro»: manda ese archivo a quien te dé
soporte. El registro está en `%LOCALAPPDATA%\JudoComp\Logs` en Windows y en
`~/.local/share/JudoComp/Logs` en Linux.

Si el PC no puede mostrar la ventana de JudoComp, el programa se abre en el navegador y lo avisa.
Para cerrarlo entonces, usa su icono junto al reloj.
