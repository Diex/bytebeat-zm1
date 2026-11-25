# ZM1 — Bytebeat IV

**Autor: Diego Alberti**

**Proyecto: ZM1**, una computadora para la experimentación artística basada en la arquitectura 6502.

ZM1 es el desarrollo informático y electrónico que forma parte de **Bytebeat IV**. Está concebida para ejecutar algoritmos generativos de tipo Bytebeat y transformar sus resultados en patrones visuales, con una matriz de LEDs como dispositivo de salida previsto para esta obra.

## Una computadora como obra

El proyecto parte de una pregunta: **¿qué formas estéticas pueden emerger del funcionamiento de una computadora cuando se la libera de cualquier finalidad utilitaria?**

En lugar de reproducir imágenes almacenadas, ZM1 propone generarlas en tiempo real mediante operaciones aritméticas y lógicas. Su arquitectura busca reducir el sistema a los componentes necesarios para explorar esa producción visual. La computadora se exhibe como parte constitutiva de la instalación: sus circuitos y su materialidad también integran la obra.

Bytebeat IV continúa la investigación de Diego Alberti sobre arte generativo, lenguajes simbólicos y electrónica como lenguaje artístico, desarrollada en la serie Bytebeat desde 2011. El proyecto se lleva adelante desde Zombiemachines, su plataforma cultural y taller de experimentación electrónica.

## Base técnica y créditos

El diseño de ZM1 parte del repositorio **[justjoheinz/6502](https://github.com/justjoheinz/6502)**, que proporciona un diseño de microcomputadora 6502 y sus archivos de KiCad. Ese proyecto está basado, a su vez, en los **[proyectos de Ben Eater](https://github.com/beneater)**.

La adaptación de esta base a una computadora orientada a la producción estética corresponde al proyecto ZM1 de Diego Alberti. Estos antecedentes se reconocen como fundamento del desarrollo electrónico.

El documento de avance también identifica al proyecto **20C de Osolabs Tech** como referencia y recupera circuitos propios de obras anteriores para la salida visual: comunicación serial, registros de desplazamiento **74HC595** y controladores **ULN2803**.

## Estado del proyecto

Según el documento de avance, ZM1 se encuentra en etapa de **diseño electrónico y experimentación mediante emulación**, con una arquitectura definida y un primer esquemático completo.

Las etapas pendientes incluyen:

- Revisar y validar el diseño y preparar los archivos de fabricación.
- Fabricar las placas, montar los componentes y programar las memorias ROM.
- Realizar pruebas de funcionamiento e integrar la salida visual.
- Diseñar y fabricar el gabinete de exhibición.

También se prevé un kit de desarrollo para que otras personas puedan construir y programar su propia ZM1.

## Contenido del repositorio

- [`kicad/`](kicad/): proyectos, esquemáticos, placas, modelos 3D y archivos de fabricación.
- [`kicad/6502.csv`](kicad/6502.csv): listado de materiales de la base electrónica.
- [`kicad/README.md`](kicad/README.md): documentación técnica de la base, imágenes de las placas y mapa de memoria.
- [`pdf/Bytebeat IV - Avance.pdf`](<pdf/Bytebeat IV - Avance.pdf>): memoria conceptual, antecedentes y plan de desarrollo que sirven de fuente para esta presentación.

Los archivos de fabricación existentes deben revisarse y validarse como parte del desarrollo de ZM1 antes de producir las placas.
