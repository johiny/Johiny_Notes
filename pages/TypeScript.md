- A que prevenir bugs desde antes de ejecutar el código suena bien?
- [[JavaScript]] con super poderes?
- Las principales habilidades de [[TypeScript]] son encontrar posibles errores desde antes de ejecutar el código y colocar tipado a [[JavaScript]] para controlar el poder que da JavaScript a comparación de otros lenguajes con tipado fuerte nativo, algo que comienza guardando un string puede pasar a ser un número y al final del programa a ser un objeto, lo que puede llevar a errores en algún momento, con typescript todo va a tener un tipo definido con eso se puede tener un software a mi aparecer menos flexible a la hora de pensar en una solución o hasta menos elegante talvez?. pero se logra dar con una solución mucho más segura y estable que es lo más importante cuando se habla de [[BackEnd]].
- ese control se logra con el Type Annotation!
- ***Type Annotation*** #code
  ```typescript
  let fruta : string = "manzana"
  			// ahora sabemos que fruta es una variable que guarda strings
  ```
- Parece ser que el tipo any es lo peor!, úsalo solo como solución temporal mientras arreglas el error real o si la librería que estas usando no tiene soporte para TypeScript.
collapsed:: true
	- ![image.png](../assets/image_1659205036208_0.png)
- algo buenísimo son los union types con ellos ganas la flexibilidad perdida sin perder el control.
- ***Union Type*** #code
  ```typescript
  let fruta : string | null = "manzana"
  	// con esto ahora fruta puede ser un string como manzana o no 
  	//contener nada osea null
  ```
- con typescript también puedes crear tu propio tipo de dato combinando varios en uno solo como las struct [[C]] parecido pero no igual, lo que mas me sorprendió es que estos custom types pueden ser literales ósea pueden ser algo en especifico y solo eso como un select de [[HTML]] con sus opciones donde solo se pueden seleccionar lo que esta dentro de sus opciones bien definidas.
- ***Custom Type With Literal Options*** #code
  ```typescript
  type fruta = "manzana" | "banana" | "coco"
  let unafruta : fruta = "naranja"
  			// esto dara error ya que ahora las unicas frutas que puede contener
  		// una variable de tipo fruta son las definidas literalmente en el tipo fruta.
  ```
- null y undefined son tipos de datos independientes aunque uno podría pensar como tengo un numero que esta indefinido al principio pero luego ya tendrá un valor eso dará un error en typescript la manera de hacer eso seria crear un dato mixto de number y null o algo así, además de ello es bastante extraño que el motor de inferencia le asignara a las variables que tengan null o undefined el tipo de dato any lo que tiene sentido ya que si lo piensas bien es muy extraño que quieras algo que se mantenga null por siempre por eso le agrega el any para que cambie por cualquier cosa durante el runtime.