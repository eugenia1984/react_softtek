# :star2: Teoría Módulo 2. Armado y diseño de nuestros componentes

---

## Objetivos del módulo

- Profundizar en la utilización de componentes como estructura básica de nuestro sitio web e implementar la librería de Bootstrap para incorporar CSS a nuestro sitio.

- Poder armar la componente “cabecera” en donde dispondrás todo lo referente a la barra de navegación de la aplicación.

- Elaborar un componente “pie de página” en donde deberás disponer los créditos y los elementos claves que deben estar presentes en el footer de una aplicación.

- Integrar los componentes anteriores con los demás componentes y permitir que formen parte del flujo de toda la aplicación.

- Implementar una librería de CSS para comenzar a gestionar los estilos visuales de la aplicación.

- Armar el componente "listado", para que puedas mostrar allí todos los resultados obtenidos desde la API.

- Crear un componente "detalle" que permita visualizar allí, la información de solamente un ítem en particular.

- Entender cómo se renderiza un bloque de información (array) dentro del componente.

- Identificar cómo realizar un renderizado condicional, para que mientras la información llega desde la API la persona que usa la aplicación, pueda esperar cómodamente (mensaje: “Cargando…”).

---

## :star2: UNIDAD 3 - DISEÑO DE LA ESTRUCTURA BÁSICA

### :star: 3.1 ARMADO ENCABEZADO / NAVEGACION


#### ¿Para qué nos servirá este componente?

Este componente tiene como finalidad contener una barra de navegación que esté presente a lo largo de toda la aplicación. A su vez, servirá facilitar el ingreso a las distintas rutas que han sido configuradas y en las cuales podremos ver la información esperada.

#### ¿Por qué es importante contar con una barra de navegación?

Las barras de navegación en las aplicaciones web son algo muy común, ya que, como lo mencionamos antes, le permiten al visitante de la página, acceder a cualquier ruta que esté disponible. Además, al implementar una barra de navegación no solamente estaremos aprendiendo cómo generar la estructura a través de JSX, sino que también entenderemos cómo funciona el sistema de ruteo dentro de una SPA (single page application).

#### ¿El encabezado y la barra de navegación pueden tener lógica condicional?

Entendiendo que la lógica condicional nos va a permitir mostrar o no algunas porciones de contenido y que particularmente estamos hablando de la implementación de algunos if/else, la respuesta sería: claro que sí. Esto se debe a que particularmente ese será uno de los objetivos de esta unidad, pues de esa manera podrás aprender a implementar partes de la barra de navegación que solamente estén presentes si el visitante de la aplicación se ha autenticado correctamente.

---

### :star: 3.2 ARMADO DE PIE DE PAGINA

#### ¿Es necesario que toda aplicación posea un pie de página?

No hay nada escrito al respecto y bien esto podría tener una respuesta bastante extensa. Sin embargo, para darte una respuesta más breve, la sugerencia será que siempre implementes un pie de página, así sea bastante sencillo, pues esta parte de contenido le podrá dar un cierre oficial a los demás bloques de contenido presentes dentro del documento. Además, si lo piensas un poco más, puedes aprovechar este espacio para disponer allí información no tan relevante, pero que sería bueno tener presente constantemente.


#### ¿Puedo poner una barra de navegación en el pie de página?

Por supuesto, cualquier información que le aporte valor al visitante del sitio puede ir dentro de este apartado de contenido, pues aquí podrás dejar disponibles aquellos accesos directos a las secciones más relevantes de tu aplicación, los enlaces a las redes sociales o cosas por el estilo que le aporten más información a tu sitio web.
¿El pie de página se desarrolla como cualquier otro componente?
Totalmente. Pues de esta manera podrás tener de manera aislada todo su contenido y de ser necesario en un futuro, podrás modificar el mismo, sin afectar a otros apartados de la aplicación.

---

### :star: 3.3 INTEGRACION DE ENCABEZADO / NAVEGACION


#### ¿Cómo se integra este componente con el resto de la aplicación?

De la manera más sencilla posible, pues debemos pensar que es un componente más, como cualquier otro. Y para implementarlo lo debemos tratar como tal.

#### ¿Por qué nos conviene hacerlo como un componente externo en vez de implementarlo directamente dentro del componente principal de la aplicación?

Siempre que pensemos que un apartado de código de la aplicación deberá estar presente a lo largo de la misma, es un buen indicador de que deberá ser tratado como un componente aparte, pues, de esta manera, podemos procurar un eficiente desarrollo del componente, pensando incluso en su futura escalabilidad.

#### La NO integración de este componente, ¿pone en riesgo el resto de la aplicación?

Realmente no, pero siendo sensatos, la mejor manera de permitir que quienes usan nuestra aplicación puedan acceder a cualquier parte de la misma, es haciendo uso de un encabezado que contenga una llamativa y contundente barra de navegación.

---

### :star: 3.4 INTEGRACIÓN LIBRERIA CSS

#### ¿Qué es una librería de CSS?

Quizás puede sonar un poco tonta la pregunta, pero recuerda: no hay pregunta tonta, lo tonto es no preguntar. 

Una librería de CSS es una serie de archivos que ya vienen preparados para ser usados directamente, sin escribir siquiera una línea de código CSS. 

Existen varias librerías de reconocida fama en el mercado. Quizás te suenen los nombres de Bootstrap, Tailwind o Bulma ¿no? Pues bien, estamos seguros que, en algún momento de tu vida, te habrás encontrado con alguna de ellas.

#### ¿Cuál es la ventaja de usar una librería de CSS?

La principal ventaja es la rapidez con la que podemos construir nuestra aplicación, pensando particularmente siempre en el código funcional, más no en el visual. Además, gracias a las librerías de CSS podemos implementar efectos muy llamativos que de otra manera nos hubiesen costado bastante esfuerzo.

#### No me gustan las librerías de CSS, ¿puedo implementar mi propio código CSS dentro de React?

Claro que sí. Y no necesitas ser un experto para hacerlo. Es más, a lo largo de esta clase te vamos a mostrar cómo puedes, además de usar una librería, implementar tu propio CSS dentro de los componentes de React. Para que de esa manera puedas ponerle un poco de tu impronta a los estilos visuales de la aplicación.

---
