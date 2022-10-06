# :star2: Módulo 4. Diseño responsive & tests finales

---

## Unidad 8. Modo responsive
```
- 8.1. ¿Qué es Mobile First?
- 8.2. Dev tools para Mobile First
- 8.3. Login con Mobile First
```

---

## Unidad 9. Trabajando con formularios
```
- 9.1. Revisión formulario login
- 9.2. ¿Qué es Formik?
- 9.3. Login con Formik
- 9.4. Registro con Formik
```

---

## Unidad 10. Trabajando con las rutas
```
- 10.1. React router Dom 6, rutas y roles
- 10.2. Creación de rutas con react router dom 6
- 10.3. Implementación con react router dom 6, rutas y roles
- 10.4. Transición entre rutas
- 10.5. Lazy import y suspense
```

---

## Unidad 11. Adaptado a Mobile First
```
- 11.1. Header
- 11.2. CSS Global y estilos del login
- 11.3. Lista de tareas Mobile First
- 11.4. Listados en escritorio y utilidades
- 11.5. Refactorizaciones
```

---

## Unidad 12. Trabajando con Formik
```
- 12.1. Creación con Formik
- 12.2. Validación con Yup
- 12.3. OnBlur en Formik y UX
```

---
---


# :star2:Clase 4 Octubre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> MODULO 4 * UNIDAD 8:star2: 

## ¿Qué es Mobile First?, Dev Tools Mobile First, Login con Mobile First

---

## :star: Temas:

```
- 1 - Presentación del Módulo 4.
- 2 - Principio Mobile First.
- 3 - Herramientas para Mobile First.
- 4 - Login Mobile First y Flexbox.
- 5 - Media Queries y breakpoints
```

---

## :star: 1 - Presentación del Módulo 4 : Mobile First y Responsive

En este módulo vamos a ver los principios y herramientas para crear aplicaciones responsive.

### 01 - ¿Que es Mobile First?

Entender los conceptos de diseño responsive y mobile first. El diseño se adapta a la pantalla de los dispositivos.

### 02 - DevTools para Mobile First

Revisar herramientas para testear el diseño de la aplicación y ver cómo se comporta con distintos dispositivos.


### 03 - Login con Mobile First

Vamos a aplicar los principios vistos previamente a la construcción de una pantalla de login


---


## :star: 2 - Principio Mobile First

## <img src="https://img.icons8.com/ios/40/000000/two-smartphones.png"/> ¿A qué nos referimos con Mobile First ?

Es un concepto de diseño web,  donde inicialmente se crea un diseño e implementación de una página web pensando primero en el uso para dispositivos como tablets y smartphones, para luego adaptarla a las necesidades de un navegador de escritorio.

Hasta hace unos años, era común que los diseñadores y los programadores se hicieran cargo de la ejecución de páginas web pensadas únicamente para ser visualizadas en ordenadores


## <img src="https://img.icons8.com/ios/40/000000/two-smartphones.png"/> ¿Cuál es el propósito del Mobile First ?

Es desarrollar una solución web óptima para dispositivos móviles; y sólo después, basándose en la estrategia de mejora progresiva (en inglés **Progressive Enhancement**), dichas páginas web son optimizadas para todo tipo de pantallas de ordenadores y portátiles.

#### ¿Por qué elegir este tipo de estrategia?

Desde hace un tiempo, el diseño web para dispositivos móviles no es solo un nicho, sino que se ha convertido en un mercado principal.



## <img src="https://img.icons8.com/ios/40/000000/two-smartphones.png"/> ¿A que llamamos diseño responsive?

El diseño web responsive, también llamado adaptativo, es un método de diseño web que tiene como objetivo principal lograr una correcta visualización de una misma página en varios tipo de dispositivos, ya sean ordenadores de mesa, portátiles, tabletas o teléfonos móviles.

#### ¿Por qué usar este método ?

A día de hoy los usuarios acceden a los contenidos de las páginas webs desde diversos dispositivos, por lo que es necesario que una misma página pueda verse correctamente desde cada uno de estos terminales y según el tamaño de la pantalla del mismo.


## <img src="https://img.icons8.com/ios/40/000000/two-smartphones.png"/> ¿Cómo lograr un diseño web responsive?

Hoy en día existen diferentes patrones que podemos usar para hacer nuestras páginas web responsives. Algunas opciones son:


- **Mostly Fluid** Es un diseño multi-columna que introduce márgenes más grandes a medida que va aumentando el tamaño de la pantalla. Como cuando tenemos desde el mobil que vamos viendo todos bloques de sections unas debajos de las otras, que nos ocupan el 100 % del ancho.

- **Column Drop**: Comienza con un diseño de varias columnas y termina con un diseño de una sola columna, eliminando columnas en el camino a medida que el tamaño de la pantalla se vuelve más estrecho. A diferencia del patrón Mostly Fluid, el tamaño total de los elementos en este diseño tiende a permanecer constante. Un ejemplo es ver  4 columnas en desktop, ver 3 en tablet y solo 2 o 1 en mobile.

- **Layout Shifter**: Es el patrón más receptivo, con múltiples puntos de interrupción (**breakpoints**) en varios anchos de pantalla. La clave de este diseño es la forma en que se mueve el contenido, es decir, no lo hace redistribuyendo y dejando “caer” columnas una debajo de otra. Debido a las diferencias significativas entre cada punto de interrupción principal, es más complejo de mantener y probablemente implique cambios dentro de los elementos, no solo en el diseño general del contenido.

- **Main Column with Sidebar**: Un diseño familiar donde el contenido principal está acompañado por una barra lateral. A medida que aumenta la ventana, la barra lateral aparecerá junto al contenido principal para utilizar mejor el espacio en pantalla.


- **Table Cell**: Las tablas son un patrón de diseño para mostrar grandes cantidades de datos en filas y columnas, lo que las hace eficientes para realizar análisis comparativos

- **Grid System**: Es un sistema para organizar el diseño. El más usado para la pantalla (como una página web, una aplicación u otras interfaces de usuario), es el basado en columnas. Implica tomar una página y dividirla en una serie de campos verticales, a los que luego se alinean los objetos. En desktop uso las 12 columnas y a veces ordeno dejando 1 de cada costado y uso las 10 del centro. En tablet separo en 4 y uso las 4 juntas o 2 y 2 . Y en mobil es 2 o 1.

- **Flex Box**: Es un mecanismo de diseño que sirve para agrupar elementos en una dimensión. Se destaca por tomar un montón de elementos que tienen diferentes tamaños y devolver el mejor diseño para esos elementos.



## <img src="https://img.icons8.com/ios/40/000000/two-smartphones.png"/> ¿Como podemos implementar este principio?


Vamos a ver que se puede implementar usando CSS y algunas de sus características:

- **Media Queries**: Son Reglas de CSS que permiten aplicar estilos condicionalmente según características de la pantalla o la página a imprimir.

- **Breakpoints**: Definen el punto a partir del cual empieza a aplicar las reglas condiciones 

```CSS
@media screen and (min-width:600px) {
  body {
    background-color: blue;
  }
}

@media screen and (min-width: 900px) {
  body {
    background-color: green;
  }
}
```

- **Display Flex**: Permite disponer elementos en una dirección (row ó column) y configurar cómo se alinean y justifica los mismos.

```CSS
dislplay: flex;
flex-direction: row | column;
justidy-content: flex-start (default) | flex-end | center | space-between | spacearound | space-evenly | stretch;
```

### ¿Donde puedo aprender FlexBox?

Tenemos juegos, como:

[http://flexboxfroggy.com/](http://flexboxfroggy.com/)

[http://www.flexboxdefense.com/](http://www.flexboxdefense.com/)

---


## :star: 3 - Herramientas para Mobile First

---


## :star: 4 - Login Mobile First y Flexbox

Corresponde al área del browser donde se pinta el html. 

Si no se indica los dispositivos mobile asume un área de 980px que suele ser más grande que el ancho de pantalla mobile, y por lo tanto el browser mobile hace un zoom out para mostrar toda la pantalla.

###  Usar el ancho del dispositivo 

Para que el browser mobile use el ancho del dispositivo, en lugar de los 980px default se configura un meta tag

```HTML
<meta name="viewport" content="width=device-width, initial-scale=1" />
```

Nota: create-react-app lo configura correctamente por defecto. 




---


## :star: 5 - Media Queries y breakpoints


- **Media Queries**: Son Reglas de CSS que permiten aplicar estilos condicionalmente según características de la pantalla o la página a imprimir.

- **Breakpoints**: Definen el punto a partir del cual empieza a aplicar las reglas condiciones 

```CSS
@media screen and (min-width:600px) {
  body {
    background-color: blue;
  }
}

@media screen and (min-width: 900px) {
  body {
    background-color: green;
  }
}
```

### Unidades relativas

Existen distintas formas de definir el tamaño de los componentes, algunas definiendo tamaño fijo y otras con unidades relativas al viewport o al componente padre.

```CSS
/* Relativa al viewport */
container {
  width: 100%;
  height: 100vh;
}

/* Relativa al padre */
container {
  width: 100%;
  height: 100%;
}

/* No relativas: pixels */
container {
  width: 1920px;
  height: 1080px
}
```

CSS es muy poderoso y complejo. Permite relativizar el tamaño de las fuentes en base a un fuente root o a la fuente del tag padre utilizando unidades em y rem.


---
---

# :star2:Clase 5 Octubre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> MODULO 4 * UNIDAD 9:star2: 

---

## LIBRERIAS PARA FORMULARIOS EN REACT

---

## :star: Temas:

```
- 1 - ¿Por qué usar una librería para manejar formularios?.
- 2 - Opciones de librerías para manejar formularios.
- 3 - Agregar Formik a nuestro formulario de Login.
- 4 - Crear un formulario de registro con Formik.
```

---

## :star: 1 - ¿Por qué usar una librería para manejar formularios?

A medida que la aplicación crece, se debe optar por la optimización de sus componentes y los formularios son un ejemplo de ello.

Para crear un formulario, debemos tener en cuenta los siguientes aspectos:

- **Accesibilidad**: Millones de usuarios en el mundo sufren algún tipo de discapacidad y navegan los sitios web a través de herramientas diferentes al mouse y el teclado, por lo tanto, debemos tener en cuenta la semántica de los elementos HTML que usemos para crear el formulario.

- **Validaciones**: Cada campo que existe en el formulario puede tener unas reglas particulares. Unos campos pueden ser opcionales, otros obligatorios, también permiten ingresar correos electrónicos, pueden requerir valores mínimos o máximos, entre otros.

- **Serialización**: La información del formulario se encuentra en algún espacio de memoria de la aplicación. Obtener esa información, manipularla y enviarla adecuadamente puede ser un reto en algunas ocasiones.

Se ha convertido en un reto saber cómo efectivamente implementar formularios. Para lograrlo en React, tenemos que tener en cuenta qué estilo de componente vamos a crear para los formularios (**controlado o no controlado**) y sus validaciones pertinentes (síncronas y asíncronas).

###  Componente No Controlado

Es aquel que no usa el estado o las props para representarse en el DOM, es decir, el valor de los elementos del componente no pueden ser manejados en un determinado momento. Una de las maneras en la que React obtiene los valores es usando el hook de **useRef**.

```JSX
import React from "react";

function Form() {
  const formRef = React.useForm():
  
  function handleSubmit(evt) {
    evt.preventDefault();
    /*
      1. Usamos FormData para obtener la informacion
      2.FormData requiere la referencia del DOM, 
        gracias al REF API podemos pasar esa referencia
      3. Finalmente obtenemos los datos serializados  
    */
    const formData = new FormData(formRef.current);
    const values = Object.formEntries(formData);
    // Aqui puedes usar valores para enviar la informacion
  }
  
  return (
    <form onSubmit={handleSubmit} ref={formRef}>
      <label htmlFor="email">Email</label>
      <input id="email" name="email" type="email"/>
      <label htmlFor="password">Password</label>
      <input id="password" name="password" type="passwprd"/>
      <button type="submit">Submit</button>
    </form>
  )
}
```

### Componente Controlado

Es aquel que usa los cambios de estado o cambios de props para representarse en el DOM. Es un componente que mantiene una
sincronización entre el estado y el valor del campo, si el estado cambia, el valor cambia.

```
   Component
  /        \
State <--- SetState 
```

### Validaciones Síncronas

Son aquellas que ocurren sin bloquear la ejecución esperando alguna respuesta. La mayoría de las validaciones son de este tipo, y los casos de uso más normales son validaciones de correos electrónicos, nivel de seguridad de contraseña, etc.


### Validaciones Asíncronas

Son aquellas que determinan el estado del campo usando algún servicio externo, lo que genera un bloqueo de la ejecución hasta que
se obtenga alguna respuesta.

---

## :star:  2 - Opciones de librerías para manejar formularios

---

## :star: 3 - Agregar Formik a nuestro formulario de Login

---

## :star: 4 - Crear un formulario de registro con Formik

---
---

---
---
