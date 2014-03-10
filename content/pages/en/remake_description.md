Title: Remake
Lang: en

# Remake description

Recrear el Comdasuar en su forma original sería una tarea prácticamente
imposible. Aunque los documentos publicados por Asuar presentan con mucho
detalle sus ideas, propósitos y razonamientos, no son suficientes técnicamente
para lograr una recreación exacta. Por esto, para hacer una recreación que sea
fiel al espíritu del original, hemos decidido ceñirnos a los conceptos e ideas
originales, sin buscar crear una copia exacta.

Para lograr la meta de hacer un sistema económico -el Comdasuar era para la
época un sistema muy económico- decidimos basar la síntesis en un RaspberryPi y
el control en un Arduino. Ambos son componentes de fácil acceso y bajo costo.
De nuevo, para facilitar la construcción y mantener el precio bajo, elegimos
hacer todo el proceso de sonido en software, en vez de hacer un sistema híbrido
como el Comdasuar.

La síntesis y procesamiento de sonido se programó usando[Csound](http://csounds.com),
un lenguaje para música y sonido, que fue publicado inicialmente a mediados
de los años 80 por Barry Vercoe en el MIT Media Lab y tiene raíces en los
primeros sistemas de música por computador de Max Matthews desarrollados en
Bell Labs, pero que aún hoy se mantiene en desarrollo. Los procesos de
síntesis y transformación siguen los propuestos por Asuar: generadores de onda
cuadrados, que luego pasan por filtros, modulación de anillo y reverberación.

Como el Comdasuar era no sólo un sintetizador sino también un sistema de
composición, fue necesario desarrollar un sequenciador programable. El
sistema de secuenciación, programación de eventos y la interfaz de texto
fueron escritos en Python. Con este, el usuario además de poder entrar notas
al secuenciador, puede escribir programas sencillos para la transformación de
los eventos.

El lenguaje para la representación de los eventos musicales (notas, tempo,
etc.) sigue fielmente el modelo de Asuar, por ejemplo una escala de negras a
partir de do, se vería así:

**C4 N**

**D4 N**

**E4 N**

**F4 N**

**G4 N**

**A4 N**

**B4 N**

**C5 N**

La interfaz de usuario es una interfaz de texto, algo anacrónica, pero muy
apropiada para el RaspberryPi ya que evita tener que usar recursos para
correr todo un sistema de escritorio, lo que permite tener más recursos
disponibles para la generación de sonido.

# Tutorials

* [Raspberry Pi](tutorial_pi.md)
* [Wiring](tutorial_wiring.md)
* [C-sound](tutorial_csound.md)
