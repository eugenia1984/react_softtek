# :star2: Módulo 1. Incursionando en React JS

---

## :star:  Temas:

### Unidad 1. Primeros pasos en React JS
```
- 1.1. Setup de herramientas
- 1.2. Introducción a React (parte 1)
- 1.3. Introducción a React (parte 2)
```

---

##· Unidad 2. Creando nuestro primer componente
```
- 2.1. Armado componente
- 2.2. Validación de formulario
- 2.3. Envío del formulario
- 2.4. Manejo de errores
- 2.5. Persistencia del token
- 2.6. Redirección al componente "listado"
```

---

## :star: Clases

---

### :star2: Clase 20 Septiembre <img src="https://img.icons8.com/clouds/36/000000/react.png"/> Introducción a React: Configuración de Herramients y Estructura Básica


- Mentores: Andreína Marcano y Rodrigo Tonso

Temas:
```
- Bienvenida
- - Presentacion Modulo 1
- Introducción a Herramientas
- Estructura básica de React
```


### ¿ Que tenemos ? <img src="https://img.icons8.com/external-others-zufarizal-robiyanto/36/000000/external-lup-mutualiz-ui-essential-others-zufarizal-robiyanto.png"/>


- 5 modulos con teoría y práctica y al final los cuestionarios.

- un trabajo en grupo de una app en React.


### Herramientas <img src="https://img.icons8.com/doodle/36/000000/maintenance.png"/>


- **VSC**, editor de codigo para escribir codigo de programación. No es igual aun **IDE** (Entrno de Desarrollo Integrado, en general para un lenguaje específico, como por ejemplo IntelliJ, Eclipse, Wenstorm y PyCharm; son más robustos, con más herramientas, pero son pesados). En cambio con el Editor de código lo tenemos gratis, es ligero, y tienen pluggins para personalizar

- **Node.js**, entorno de trabajo

- **CRA** (Create React App), para inicializar el proyecto, sin tener que configurarlo desde cero. Creamos un ambiente de dearrollo, permite crear una SPA (Single Page Aplication).

Documentación oficial en [https://create-react-app-dev/](https://create-react-app-dev/)

Nació como respuesta al trabajo generalmente repetitivo al que se enfrentaban los desarrolladores a la hora de configurar un entorno eficiente. Antes debían instalar manualmente: webpack, babel, ESLint, Jest, y luego estaba toda la configuración manual. Ahora con solo el comando : ```npx create-react-app``` ya está.


**webpack** crea unos bunfles, que es tu codigo optimizado para el deploy a producción.


**Babel** es el compilador de JavaScript que permite transformar todo lo que escribimos desde ES% en adelante para que sea compatible en navegadores más viejos, que tiene el código anterior.


**ESLint** nos ayuda a identificar si tenemos problema en el codigo, son los warnings que nos avisan si nos falta un ; o si lo tenemos mal identado.


**Jest** es un framework para testing, teniendo codigo de prueba nos aseguramos que tenemos buen codigo.

---

### ¿ Cómo arrancar ?


**npx** es un ejecutador, viene desde npm versión 5 en adelante, te permite utilizar un paquete y probarlo en un entorno de ejecución.

```npx create-react-app my-app``` -> para crear mi proyecto, my-app es el nombre de la aplicación, el nombre no puede tener mayúscuar, ni espacios, ni caracteres especiales.

``` cd my-app``` -> me tengo que ir adentro de mi app creada

```npm start``` -> para arrancar el proyecto y verlo en la web.


-> En el caso de tener una versión más vieja hay que hacerlo de forma global:

```npm install -g create-react-app my-app```

```create-react-app my-app```

### React Developer Tools

Nos ayudan mucho al hace debuging, vamos a ver como fluyen los datos entre los diferentes componentes de la aplicación.

Tenemos **Components** (vamos a poder ver los componentes, sus propiedades, datos y su estado) y **Profiles**



---


## <img src="https://img.icons8.com/clouds/36/000000/react.png"/> Introducción a React

- Librería de JavaScript

- Creada por Facebook (Meta)

- Basada en **componentes**, un elemento o conjunto de elementos de un **interfaz de usuario** (UI) que posee su propio estado y apariencia.

- Hay dos formas de crear componentes...

... desde lo macro a lo micro

... desde lo más mínimo a lo más general

-> No hay una sola forma posible de armar los componentes, depende de la lógica que uno utilice, hay varias formas, por eso React es tan flexible.

-> Usar un enfoque de componentes nos permite crear y adminsitrar una aplicación compleja de manera sencilla y entendible, las características de los componentes...

... son reusables, se puede crear una sola vez y reusarlo en varias vistas.

... permiten tneer un código más organizado y mantenible (hay carpetas, archivos, hya compoenntes padres, componentes hijos, componentes nietos)

... facilidad a la hora de comprobar su funcionamiento, al integrar test tendremos buen codigo y buen funcionamiento.


### Conocimientos importantes  <img src="https://img.icons8.com/color/36/000000/javascript--v1.png"/>


Para utilizar esta librería hay que tener en cuenta:

- comprensión de JavaScript

- prácticas en el uso de ECMAScript 6 (ES6) como : arrow functions, templates, métodos, desestructuración, spread operator, etc.

- manipulación del HTMl, sus etiquetas y el DOM.


---
---
