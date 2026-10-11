# JudoComp

Programa para llevar una liga de judo de varias jornadas, pensado para el personal de los clubes:
gente que sabe de judo, no de informática. Funciona en el PC de la competición, sin internet, desde
un icono en el escritorio.

Mientras está en construcción, JudoComp se apoya en [JudoShiai](https://www.judoshiai.org/) para
los sorteos, las tablas y los combates, y se encarga de todo lo demás: inscripciones, categorías,
jornadas, clasificación y publicación. «JudoComp» es un nombre provisional.

## Descargar

La última versión está en [Releases](https://github.com/agb4455/judocomp-public/releases):

- **Windows**: `JudoCompApp-win-Setup.exe`.
- **Linux**: `JudoCompApp.AppImage`.

Llevan todo dentro y se instalan sin internet. Si el PC de la competición no tiene conexión,
descarga el instalador en otro y llévalo en un USB.

## Documentación

- [Guía de uso](docs/guia-de-uso.md): instalar, crear la liga, competidores, categorías, copias de
  seguridad y qué hacer si algo falla.
- [Novedades](CHANGELOG.md): lo que trae cada versión.

Las dos se ponen al día con cada versión.

## Dudas y fallos

Abre una [incidencia](https://github.com/agb4455/judocomp-public/issues) contando qué hacías y qué
pasó. Si JudoComp mostró un aviso de error, adjunta su registro técnico, que no guarda datos de los
competidores (dónde está, en la [guía](docs/guia-de-uso.md#si-algo-falla)). **No adjuntes nunca el
archivo de la liga (`.comp`)**: tiene datos personales de los competidores, muchos de ellos menores.

El código de JudoComp no es público: este repositorio guarda las versiones, la documentación y las
incidencias.
