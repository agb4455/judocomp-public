# Novedades de JudoComp

Lo que cambia en cada versión, contado para quien usa el programa. Cada versión se descarga en
[Releases](https://github.com/agb4455/judocomp-public/releases); cómo usarla, en la
[guía de uso](docs/guia-de-uso.md).

Las versiones siguen `mayor.menor.corrección`. Mientras JudoComp está en construcción, cada número
menor cierra un bloque de funcionalidad; la 1.0 será la primera con una liga completa de principio
a fin.

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

[0.4.0]: https://github.com/agb4455/judocomp-public/releases/tag/v0.4.0
[0.3.0]: https://github.com/agb4455/judocomp-public/releases/tag/v0.3.0
