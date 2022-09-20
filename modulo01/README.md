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
---


## :star: Clases

---

## :star2: Clase 20 Septiembre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> Introducción a React: Configuración de Herramients y Estructura Básica


- Mentores: Andreína Marcano y Rodrigo Tonso ( tiene 5 años de experiencia en React y TS, e inclina más por las start-ups).

Temas:
```
- Bienvenida e Introducción al Programa
- Presentacion del Modulo 1
-  Configuración de Herramientas
- Introducción a React.
- Estructura básica de un proyecto en React
```


### <img src="https://img.icons8.com/external-others-zufarizal-robiyanto/40/000000/external-lup-mutualiz-ui-essential-others-zufarizal-robiyanto.png"/>  ¿ Que tenemos ?

Repasemos brevemente qué contine el programa!

- **5 módulos** con **videos** y **calses**. Teoría y práctica y al final un **cuestionario** de preguntas para evaluar el aprendizaje.

- Talleres privados el inicio del proyecto. Un trabajo en grupo para desarrollar y entregar una app en React con los conocimientos obtenidos en la teoría.

### Módulo 1 : Primeros pasos en React JS

Es el inicio en la librería reconociendo su sintaxis, funcionalidades y componentes básicos.

#### 1 - Herramientas

Vamos a identificar, instalar y configurar las herramientas necesarias para el desarrollo de una aplicación.

#### 2 Armado de un primer componente y validaciones

Vamos a crear un componente Login, validar su formulario y enviar esos datos a una API para obtener un token de autenticación. 

#### 3 Manejos de errores y redireccionamiento

Vamos a implementar mensajes de error, ver cómo persistir el token obtenido de la API y hacer un redireccionamiento a un nuevo componente luego de la validación de credenciales.


###  <img src="https://img.icons8.com/doodle/40/000000/maintenance.png"/>  Herramientas


- **VSC**, editor de codigo para escribir codigo de programación. No es igual aun **IDE** (Entrno de Desarrollo Integrado, en general para un lenguaje específico, como por ejemplo IntelliJ, Eclipse, Wenstorm y PyCharm; son más robustos, con más herramientas, pero son pesados). En cambio con el Editor de código lo tenemos gratis, es ligero, y tienen pluggins para personalizar

- **Node.js**, es un entorno de ejecución para JavaScript que nos va permitir usar este lenguaje de programación con React. Nos
va a permitir ejecutar código JavaScript desde el lado del servidor (desde nuestra computadora). Veamos cómo instalarlo:

Al entrar a la página de NodeJS nos aparecerán 2 botones, debemos hacer clic en el que indica LTS y automáticamente comenzará la descarga

Durante el asistente, podremos cambiar la ruta de instalación y las características que se instalarán.

Recomendamos no cambiar nada dejándolo como indica por defecto, en especial el apartado npm package manager que es el gestor de paquetes de Node.js y nos será de especial utilidad.

- **CRA** (Create React App), es una interfaz de línea de comando (CLI) desarrollado por React que te permite inicializar un proyecto de forma rápida y haciendo las configuraciones necesarias automáticamente.

Configura un ambiente de desarrollo de forma que puedas usar JavaScript, brindando una buena experiencia de desarrollo, y optimizando tu aplicación. Te permite crear una aplicación de página única (Single-Page Application/SPA).

Para inicializar el proyecto, sin tener que configurarlo desde cero. Creamos un ambiente de dearrollo, permite crear una SPA (Single Page Aplication).

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


## <img src="https://img.icons8.com/clouds/40/000000/react.png"/> Introducción a React

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


###   <img src="https://img.icons8.com/color/40/000000/javascript--v1.png"/> Conocimientos importantes


Para utilizar esta librería hay que tener en cuenta:

- comprensión de JavaScript

- prácticas en el uso de ECMAScript 6 (ES6) como : arrow functions, templates, métodos, desestructuración, spread operator, etc.

- manipulación del HTMl, sus etiquetas y el DOM. BYTES -> CHARACTERS -> TOKENS -> NODES



### React y el DOM Virtual


El **DOM Virtual** es una representación del DOM en la memoria del navegador (no afecta al DOm real de la aplicación).

Asi cuando interactuamos con el verdadero DOM, le pedimos únicamente los cambios que realmente necesitamos.



#### ¿ Por qué crear un virtual DOM ?


Actualizar el DOM es una operación costosa para el navegador y muchas veces solo es necesario actualizar secciones específicas en la aplicación. Por esta razón , React apuesta a hacer una copia en memoria del DOM para hacer sus cálculos y procesos de optimización y ofrecer un mejor rendimiento en las aplicaciones al renderizar solo el html modificado.



### Estructura básica de un proyecto en React

```
1. Nombre de mi proyecto
2. node_modules -> con todas las depndencias y librerias. Tengo todos mis paquetes.
3. src -> aca ven todos mis componentes, tambien puedo agrupar en **pages** y en **components** y dentro de components puedo agrupar en carpetas los componentes.
4. App.css
5. App.js -> El primer componente, el componente macro, de el salen los hijos y nietos.
6. favicon.svg
7. index.css -> el main(core) de los estilos, pero tambien se pueden poner otros más dentro de las carpetas de los componentes o armarlos en archivos css, pueden ser acorde a los componentes.
8. logo.svg
9. index.js -> no lo vamos a modificar mucho
10. .gitignore -> para que no se suban los node_modules, variables de entorno (utilizarlas en un .env para agregar este archivo en la lista de lo ignorado), etc.
11. public -> los archivos estáticos, puro HTML5, CSS3, JavaScript.
12. index.html
13. package-lock.json -> es la configuración para el desarrollo (no se suele modificar)
14. package.json -> esta la configuración, con los scripts y las dependencias
15. App.test.js -> donde vamos a hacer los test por componentes, con unitesting y de integración.
```

---

- [Acá se puede ver un ejemplo de componente creado con JavaScript vanilla, sin JSX](https://github.com/eugenia1984/react_softtek/blob/main/modulo01/opcion_con_plain_js.pdf)


---

### Componentes de clases y Componentes Funcionales

Actualmente se traabja con **componentes funcionales** y **hooks**, antes se trabajaba con **componentes de clases**, debían especificar muchas cosas, quedaba muy largo y complicado de entender o leer, mientras más funcionalidades tenían.

---

## Consejo

- Utilizar buenas practicas

- Ajustarse a al documentación y a lo que más se utiliza, asi se puede encontrar ayuda en la counidad.

---

## <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/40/000000/external-terminal-computer-programming-flaticons-lineal-color-flat-icons.png"/> Comandos por terminal

```mkdir nombre``` para crear carpeta, en nombre pongo el nombre de la carpeta que quiero

``` cd ..``` para volver un directorio atras

```cd .``` el directorio en el que estoy

``` code .``` para abrir en VSD el directorio que tengo


-> node, con **nvm** me permite ir cambiando de version de node

-> con node tenemos **npm** y con ello podemos utilizar CRA para armar el proyecto mucho más ráìdo que tneer que ir haciendo todo manual. Con **npx** tenemos **x** de ejecutable.


## <img src="https://img.icons8.com/dusk/40/000000/babel.png"/> Babel

Adapta lo que escribimos en ES6 a las versiones que tenga el navegador (más viejas).


## <img src="https://img.icons8.com/dusk/40/000000/webpack.png"/> Webpack

Hace muchas cosas, nos ayuda para que no tengamos que configurar el proyecto. Trae **ESLint** que nos va mostrando warnings o errores las malas practicas en el codigo, apra ir corrijiendo.

### Creamos un proyecto

```npx create-react-app my-app``` -> para crear mi proyecto, my-app es el nombre de la aplicación, el nombre no puede tener mayúscuar, ni espacios, ni caracteres especiales.

``` cd my-app``` -> me tengo que ir adentro de mi app creada

```npm start``` -> para arrancar el proyecto y verlo en la web.

.gitignore es super importante, para no subir el node_modules y para no subir las variables de entorno

- **dev dependencies** son las librerias con las que viene el proyecto creado con CRA .

- **package.jon** las dependencias y los scrips ```npm run start ``` o ```npm star``` para arrancar el proyecto. ```npm build``` para buildear el proyecto. ```npm eject``` OJO al usar este. ``` npm i -D lodash```  para poner las dependencias en desarrollo, no estaran en producción.

README.md -> es aaconsejable mantenerlo actualizado.

---
---
