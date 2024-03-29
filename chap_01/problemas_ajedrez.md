# Problemas del tablero de ajedrez

## 1.1 Problemas del tablero de ajedrez
Suponga que tiene un tablero de ajedrez (cuadrícula de 8x8 cuadrados) y un montón de fichas de dominó (cada ficha de 2x1 cuadrados), de modo que cda ficha de dominó puede cubrir perfectamente dos cuadrados del tablero de ajedrez [^nota1]. 

![tablero ajedrez 01](img/01_fig.jpg)

Tenga en cuenta que con 32 fichas de dominó puede cubrir las 64 casillas del tablero de ajedrez. Hay muchas 
maneras diferentes de colocar las fichas de dominó para hacer esto, pero una forma es cubrir la primera columna con 4 fichas de dominó de un extremo a otro, cubrir la segunda columna con 4 fichas de dominó y así sucesivamente.

![tablero ajedrez 02](img/02_fig.jpg)

Por supuesto, esa no es la única manera. Aquí hay una forma ingeniosa de cubrir todos los cuadrados:

![tablero ajedrez 03](img/03_fig.jpg)

Las matemáticas se basan en definiciones, así que démosle un nombre a esta idea de cubrir todos 
los cuadrados. Además, no lo definamos solo para tableros de 8 × 8 ; permitamos que la definición se 
aplique a tableros de otras dimensiones.


`````{admonition} Definición 1.1
:class: tip
:name: def_1.1
Definición 1.1 Se denomina "cubierta perfecta del tablero" a cubrir el tablero de ajedrez de m × n con fichas de dominó de 2 × 1 sin que existan casillas descubiertas, y sin fichas de dominó apiladas o colgando fuera del tablero de ajedrez.
`````

Como demostramos anteriormente, existen cubiertas perfectas del tablero de ajedrez de 8 × 8. Este es un libro sobre demostraciones, así que escribamos esto como una **proposición** (algo que es verdadero y requiere demostración) y luego escribamos una demostración formal de este hecho.


`````{admonition} Proposición 1.2
:class: tip
:name: prop_1.2
Proposición 1.2. Existe una cubierta perfecta de un tablero de ajedrez de 8 × 8.
`````
Antes de hacer otras demostraciones, discutiremos algunos de los ingredientes clave de las demostraciones. 

**La idea de una prueba:** La proposición afirma que "existe" una cubierta perfecta. Al decir "existe", significa que hay al menos una forma posible de cubrir el tablero. Por lo tanto, cualquier proposición como ésta puede probarse simplemente presentando una forma de cubrir el tablero y la proposición estará satisfecha.

**La prueba:** Observe que la siguiente imagen es una opción de cubierta perfecta. 
![tablero ajedrez 04](img/04_fig.png)

Hemos demostrado por medio de un ejemplo que una cubierta perfecta existe. Con esto, hemos probado la proposición 1.2 [poner tumba]


Típicamente ponemos un pequeño cuadrado al final de una prueba, indicando que hemos completado el argumento. Esta práctica fue introducida por el matemático Paul Halmos, que también se la llama la *lápida de Halmos* [^nota2]

Hemos visto dos diferentes coverturas perfectas del tablero de ajedres. Cuántas pueden existir en total? Esta es una pregunta muy difícil, pero los matemáticos han encontrado la respuesta sorprendentemente grante: existen exactamente 12,988,816 coverturas perfectas. 


Esto se descubrió en 1961, mucho antes de que los ordenadores modernos pudieran descubrir la respuesta por fuerza bruta [^nota3]. Volviendo a si se puede cubrir un tablero de ajedrez, demostramos que un tablero de ajedrez estándar de 8 × 8 se puede cubrir perfectamente con fichas de dominó. ¿Qué pasa si tacho los cuadros inferior izquierdo y superior izquierdo, todavía podemos cubrir perfectamente los 62 cuadros restantes?




[^nota1]:  A lo largo de los bordes izquierdo e inferior del tablero de ajedrez hay números y letras. Estos son simplemente para etiquetar las filas y las columnas del tablero de ajedrez.

[^nota2]: Una historia apócrifa dice que Halmos consideraba que las pruebas estaban vivas hasta que se lograban probar. Una vez probadas, morían. Y así escribió una pequeña lápida para concluir cada una de sus pruebas. 

[^nota3]: De hecho, en ese artículo de 1961 de Temperley y Fisher (y de forma independiente por Kasteleyn), mostraron que la respuesta para un tablero general de m × n es esta locura:
\[
\prod_{j=1}^{\left\lceil \frac{m}{2} \right\rceil} \prod_{k=1}^{\left\lceil \frac{n}{2} \right\rceil} \left( 4 \cos^2 \left( \frac{\pi j}{m + 1} \right) + 4 \cos^2 \left( \frac{\pi k}{n + 1} \right) \right)
\]
