# MODULO 3 * TEORIA : BUSCADOR Y SECCION DE FAVORITOS

---

## Objetivos generales de aprendizaje

```
- Manipular todo tipo de query string de una URL.
- Poder renderizar datos a partir de usar mapeo de información.
- Entender los conceptos base para implementar el patrón de desarrollo con Redux.
- Reconocer cuáles son los fundamentos del patrón de Redux.
```

### Objetivos del módulo:

```
- Avanzar el desarrollo de nuestra aplicación web e implementar los fundamentos del patrón de Redux.
- Armar un sistema de búsqueda que permita encontrar películas por palabra clave.
- Validar la información suministrada de parte del usuario en este buscador para evitar hacer llamados innecesarios a la API.
- Mostrar los resultados obtenidos de la búsqueda en un nuevo componente preparado para esta finalidad.
- Implementar la lógica de "Agregar a favoritos" para que el usuario de la aplicación pueda guardar sus películas favoritas.
- Conocer la librería Redux y entender el patrón de trabajo que ella propone.
- Reconocer la problemática presente en algunas aplicaciones de React y por qué Redux es una excelente solución a implementar.
- Identificar las ventajas de trabajar con Redux.
- Asimilar los conceptos base y necesarios para usar esta librería.
- Incorporar y analizar a conciencia en qué proyectos conviene usar Redux como solución.
```


---

## UNIDAD 6 * CREANDO SECCIONES

### :star: 6.1 ARMANDO COMPONENTE BUSCADOR

#### ¿En qué lugar de la aplicación deberá estar presente la barra de búsqueda?

Generalmente, la barra de búsqueda deberá ser implementada en un lugar de fácil acceso para la persona que visita nuestra aplicación, por eso el lugar más recomendado será la barra de navegación.

#### ¿Cómo debo armar una barra de búsqueda?

En nuestro caso, la haremos realmente sencilla para no complicarnos tanto, pues solamente tendrá un campo de inserción de texto y un botón de acción. Pero tené en cuenta que en proyectos algo más grandes, esta barra de búsqueda puede ser tan compleja como sea necesario.

#### ¿Esta barra de navegación se trabaja como si fuera un formulario de HTML?

Exactamente. Así que nuestra misión será implementar una estructura HTML / JSX que tenga lo tradicional de un formulario: 

la etiqueta ```<form>```

la etiqueta ```<input />``` y

la etiqueta ```<button>```

Obviamente, con sus atributos respectivos.

---

### :star: 6.2 VALIDACION FORMULARIO BUSCADOR

#### ¿Por qué se hace necesario validar este formulario?

Puntualmente, nos interesará validar la información suministrada por el visitante, pues de esta manera nos podremos asegurar que antes de enviar la petición a la API, sabremos que tenemos la información necesaria. De este modo, evitaremos cargar nuestra aplicación de llamados innecesarios, logrando así una mejor performance.

#### Y, ¿en qué consiste este proceso de validación?

Puntualmente, nos encargaremos de validar que la persona haya ingresado una cantidad mínima de caracteres en el campo, para poder así hacer el llamado a la API. Y en caso contrario, es decir, en caso de no contar con dicha cantidad de caracteres, informaremos a la persona del error.

#### Pero, ¿cómo le podemos mostrar a la persona el error cometido?

De una manera bastante sencilla y que ya debés conocer, para este cometido implementaremos las cajas modales de Sweet Alert.

---

#### 6.3 :star: REDIRECCIONAMIENTO A RESULTADOS

#### Ahora que ya validamos el formulario de búsqueda, ¿qué sigue?

Una vez que tengamos la información necesaria, podremos redireccionar a la persona a una página de resultados, para que sea dentro de esta, donde podamos mostrar los elementos obtenidos de dicha búsqueda.

#### Y esta sección de resultados, ¿es también un listado de elementos a mostrar?

Exactamente, pues al realizar una búsqueda, no sabremos si la información obtenida nos traerá uno o muchos ítems, por lo tanto, esta deberá ser tratada como un listado. Algo con lo que quizás ya tenés algo de familiaridad.

#### Entendiendo lo anterior, ¿se podría reutilizar el componente Listado hecho en clases anteriores?

Totalmente, en la medida de lo posible, ese es el objetivo ideal. Pero si te resulta algo complejo o enredado, podemos generar un componente nuevo, por más que sea muy similar al que ya tenías anteriormente.


---

#### :star: 6.4 LLAMADO A LA API CON PALABRA CLAVE

#### Puntualmente, ¿de dónde sacamos la información para la sección de resultados?

Aquí, será la API la que nos provea de un endpoint para poder hacer dicho llamado. Y dependiendo de la palabra clave que enviemos en ese llamado, obtendremos los resultados esperados.

#### Pero, ¿cómo haremos para que el formulario de búsqueda pueda enviar al componente de resultados la "palabra clave"?

Para este objetivo utilizaremos el query string de la URL. Allí, enviaremos la palabra clave escrita por la persona y la dejaremos disponible para que el componente de resultados pueda tomarla y usarla para la petición de información a la API.

#### ¿Esto es algo que suele usarse en la vida real?

Totalmente. De por sí, es uno de los procesos más habituales al momento de desarrollar aplicaciones web, pues pasar información a través de la URL nos permite que, dependiendo de estas, podamos mostrar o no una determinada información. 

#### Micro-tip: te invitamos a que revises más a menudo la barra de dirección de tu navegador, para que puedas ver toda la información que los sitios suelen enviar a través de ella.

---

#### 6.5 :star: ARMADO LOGICA DE "FAVORITOS"

#### ¿Por qué vamos a implementar esto?

En las aplicaciones web es muy común darle la posibilidad al usuario de que agregue a un listado sus opciones preferidas. Esta opción genera una buena experiencia de uso y brinda a la persona la sensación de que nuestra aplicación escucha sus necesidades.

#### Y… ¿cómo funciona esto de "Agregar a Favoritos"?

En teoría es sencillo, pues deberemos implementar antes que nada algún elemento que permita a la persona llevar a cabo esta acción. Por otro lado, de nuestra parte lo que tendremos que hacer será agregar ese elemento clicado por el usuario a algún almacenamiento en nuestra aplicación (puede ser una base de datos o al almacenamiento local del navegador).

##### Pero puntualmente, ¿qué es lo que nos interesa almacenar?

Puntualmente en esta aplicación estaremos almacenando toda la información del ítem elegido de parte del visitante. De esta manera, nos va a ser mucho más sencillo rescatar dicha información más adelante, cuando queramos mostrarla en su totalidad.

---

#### :star: ARMADO COMPONENTE "FAVORITOS"

### ¿Cómo debemos "pensar" a este componente?

Este componente se parecerá un poco al listado de ítems que hemos venido desarrollando, pero con la particularidad de que aquí, la información no vendrá de la API sino de la información local que previamente hemos guardado.

### ¿Y los elementos agregados a "Favoritos" se pueden eliminar de este listado?

Completamente. Justamente ese será uno de nuestros objetivos, permitir que, así como se pueden agregar elementos, también se puedan eliminar cuando sea necesario.

#### ¿Y cómo podremos visualizar aquellos elementos que han sido agregados a "Favoritos" en el resto de nuestra aplicación?

Para ello tendremos que implementar una lógica que nos permita preguntar a cada uno de los elementos del listado general presentes en nuestra aplicación, si se encuentra en el listado de elementos favoritos almacenados. Y en la situación de que exista esa coincidencia, implementar un elemento visual (💖) que ilustre dicha coincidencia.

---

##### :star: FINALIZACION DEL COMPONENTE "FAVORITOS"

#### Para finalizar

Terminamos de pulir aquellos detalles que nos hayan hecho falta para dejar nuestra aplicación 100% lista y prolija para que pueda ser presentada.
​​​​​​​
Vamos a verificar que todo el flujo de la aplicación funcione correctamente, al mismo tiempo, vamos a implementar los ajustes necesarios para cubrir un manejo de los errores si fuese necesario. De esta manera, podemos dar los últimos retoques finales a esta sección para dejarla lo más prolija posible. 

---

## Referencias

[Sobre request/reponse](https://miro.medium.com/max/1050/1*W-YLHnMseUTuvs5zb7tDhw.png)

[Sobre lista de favoritos](https://dribbble.com/shots/2457700/attachments/2457700-Favorites?mode=media)

---

---