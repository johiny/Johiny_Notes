- Básicamente el encoder One-hot convierte cada categoría de una variable categórica en una variable en si que puede contener 2 valores 0 o 1, como un bombillo encendido o apagado.
- En simples palabras cada dato va a tener interruptores que van a identificar si ese dato esta dentro de esa categoría o no.
  ![An example of one-hot encoding. | Download Scientific Diagram](https://www.researchgate.net/publication/344409939/figure/fig1/AS:940907041918978@1601341128930/An-example-of-one-hot-encoding.png)
- Esto trae una solución y un problema:
- Nuestras categorías a pesar de ser texto y de ser algo abstracto y humano como colores o tipos de autos, ahora nuestro modelo las puede ver como simples 1 y 0 que representan esa información.
- Pero esto conlleva a que nuestro dataset pueda crecer exponencialmente ya que una nueva variable nacerá por cada valor diferente que puedan tener nuestras variables categóricas lo que hará el dataset enorme.
- Para mitigar esto se utilizan varias técnicas para reducir la cantidad de datos a partir de la [[Correlación]]