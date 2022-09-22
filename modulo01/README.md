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

## Unidad 2. Creando nuestro primer componente
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

## :star2: Clase 20 Septiembre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> UNIDAD 1: Introducción a React: Configuración de Herramients y Estructura Básica


- Mentores: Andreína Marcano y Rodrigo Tonso ( tiene 5 años de experiencia en React y TS, e inclina más por las start-ups).

Temas:
```
- Bienvenida e Introducción al Programa
- Presentacion del Modulo 1
- Configuración de Herramientas
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

### <img src="https://img.icons8.com/plasticine/40/000000/question-mark.png"/> ¿ Cómo arrancar ?


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

... permiten tener un código más organizado y mantenible (hay carpetas, archivos, hya compoenntes padres, componentes hijos, componentes nietos)

... facilidad a la hora de comprobar su funcionamiento, al integrar test tendremos buen codigo y buen funcionamiento.


###   <img src="https://img.icons8.com/color/40/000000/javascript--v1.png"/> Conocimientos importantes


Para utilizar esta librería hay que tener en cuenta:

- comprensión de JavaScript

- prácticas en el uso de ECMAScript 6 (ES6) como : arrow functions, templates, métodos, desestructuración, spread operator, etc.

- manipulación del HTML, sus etiquetas y el DOM. BYTES -> CHARACTERS -> TOKENS -> NODES



### React y el DOM Virtual


El **DOM Virtual** es una representación del DOM en la memoria del navegador (no afecta al DOm real de la aplicación).

Asi cuando interactuamos con el verdadero DOM, le pedimos únicamente los cambios que realmente necesitamos.



#### ¿ Por qué crear un virtual DOM ?


Actualizar el DOM es una operación costosa para el navegador y muchas veces solo es necesario actualizar secciones específicas en la aplicación. Por esta razón , React apuesta a hacer una copia en memoria del DOM para hacer sus cálculos y procesos de optimización y ofrecer un mejor rendimiento en las aplicaciones al renderizar solo el html modificado.



### Estructura básica de un proyecto en React

```
1. Nombre de mi proyecto
2. node_modules -> con todas las depndencias y librerias. Tengo todos 
mis paquetes.
3. src -> aca ven todos mis componentes, tambien puedo agrupar en *pages* 
y en *components* y dentro de components puedo agrupar en carpetas 
los componentes.
4. App.css
5. App.js -> El primer componente, el componente macro, de el salen los 
hijos y nietos.
6. favicon.svg
7. index.css -> el main(core) de los estilos, pero tambien se pueden 
poner otros más dentro de las carpetas de los componentes o armarlos 
en archivos css, pueden ser acorde a los componentes.
8. logo.svg
9. index.js -> no lo vamos a modificar mucho
10. .gitignore -> para que no se suban los node_modules, variables 
de entorno (utilizarlas en un .env para agregar este archivo en la 
lista de lo ignorado), etc.
11. public -> los archivos estáticos, puro HTML5, CSS3, JavaScript.
12. index.html
13. package-lock.json -> es la configuración para el desarrollo 
(no se suele modificar)
14. package.json -> esta la configuración, con los scripts y 
las dependencias
15. App.test.js -> donde vamos a hacer los test por componentes, 
con unitesting y de integración.
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

## :star2: Clase 22 Septiembre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> UNIDAD 2: Armando de componente, validación y envío de formulario

## Agenda del dia
```
- Ejercicio de repaso
- Inicio de sesion
- Armado del componente <Login />
- Implementación del componente <Login />
- Validación de formularios
- Envío de formularios
```

---

### :star: Ejercicio de repaso

1. Partimos de un App.js con muchas etiquetas y las separamos en componentes.

2. Tener un ```<Header />``` con sus componentes hijos:  ```<Logo />```, ```<Menu />```, ```<Search />```.

3. Armamos el CSS

---

### :star: Inicio de sesion


#### <img src="https://img.icons8.com/external-fauzidea-flat-fauzidea/40/000000/external-login-online-learning-fauzidea-flat-fauzidea.png"/> ¿Qué es ?

Hoy en día se pueden encontrar varios tipos de autenticación y uno de los más comunes son:

- **autenticación basada en contraseña**: es el método más común de autenticación. Las contraseñas pueden tener la forma de una cadena de letras, números o caracteres especiales. Una opción bastante usada actualmente son las contraseñas de un solo basadas en el tiempo (time-based one-time password, a.k.a. TOTP) -este ejemplo seria cuando te pasan una clave que expira-

- **autenticación mutifactor(MFA)**: requiere 2 o más independientes para identificar a un usuario (códigos generados desde el teléfono inteligente del usuario, pruebas de Captcha, huellas dactilares, etc).

- **autentificación basada en Token**: permiten a los usuarios ingresar sus credenciales una vez y recibir a cambio una cadena cifrada única de caracteres aleatorios. Luego puede usar el token para acceder.

####  <img src="https://img.icons8.com/external-fauzidea-flat-fauzidea/40/000000/external-login-online-learning-fauzidea-flat-fauzidea.png"/> Tipos de Inicio de Sesión

A partir de diferentes tipos de autenticación, existen diferentes formas de realizar un inicio de sesión.

A su vez, una plataforma te puede ofrecer una o más formas de inicio de sesión.

- Inicio de Sesión con usuario/email:

-Autenticación basada en contraseña

-Autenticación Multfactor (MFA)

- Inicio de sesión con un link mágico a tu em-amil

-Magic Link Email

- Inicio de sesión con Redes Sociales

-Aca se deben integrar las plataformas (los enpoints) de estas redes sociales, se hace un frujo de autenticación doble. Del sing in llamamos al endpoint o URL de la red social.

---

### Armado del componente <Login />

- Se compone de dos campos:
```
-Usuario
-Contraseña
```

- Es un formulario con dos campos: correo electrónico y contraseña.


---

### Implementación del componente <Login />

- El formulario tiene un evento **onSubmit** que se invoca la hacer click en el button de type="submit". Ese **nSubmit** va a invocar a la función **handleSubmit** que va a usar el **preventDefault** para evitar que se envie de una los datos, para tener tiempo de capturarlos.

```JSX
import "../../components/App/App.css";

function Login () {

  const handleSubmit = (event) => {
    event.preventDefault();
    
    const email = event.target.email.value;
    const password = event.target.name.value;
    
    console.log(email);
    console.log(password);
    
    const emailRegex = /^\w+([.-_+]?\w+)*@\w+([.-]?\w+)*(\.\w{2,10})+$/;
    
    if(email === "" && password === "") {
      alert("Email y password no pueden ser vacíos");
    }
    
    if(email !== "" && !emailRegex.test(email))
      alert("No e sun email valido")
    
    alert(`Email y contraseña: ${email} , ${contraseña}`);
  }
  
  return (
    <div className="login">
      <h3>Formulario>
      <form onSubmit={handleSubmit} className="formulario">
        <div>
          <label htmlFor="email">Correo electrónico:</label>
          <input type="email" name="email" placeholder="E-mail..."/>
        </div>
        <div>
          <label htmlFor="password">Password</label>
          <input type="password" name="password" placeholder="Passowrd..." />
        </div>
        <button type="submit">Ingresar</button>
      </form>
    </div>
  )
}

export default Login;
```


---

### Validación de formularios


#### <img src="https://img.icons8.com/fluency/48/000000/password-check.png"/>  ¿A qué nos referimos cuando hablamos de validación?

Es el proceso que nos permite corroborar (como desarrolladores) que la información suministrada 


#### <img src="https://img.icons8.com/fluency/48/000000/password-check.png"/>  Ejemplo de validación de Formulario

El más común lo encontramos en los formularios de registro. 

Se verifica que la información coincida con un formato habitual o tipo de no coincidir, se genera un mensaje avisando de este error.

Es decir tener una validación personalizada por cada input.

-> En realidad se utiliza el **useState** y el **useEffect**, pero... todavia no vimos los estados.

->  Son muy importants en el front, como experincia de usuario. Pero es super importante hacerlas en el Back por seguridad.



---

### :star:  Envío de formularios


###  <img src="https://img.icons8.com/external-vitaliy-gorbachev-blue-vitaly-gorbachev/40/000000/external-https-internet-security-vitaliy-gorbachev-blue-vitaly-gorbachev.png"/> ¿ A dónde van los datos ?

Cuando se validan los datos de un formulario, la acción siguiente es enviarlos. Tradicionalmente se envían usando un protocolo de comunicación llamado **HTTP**


####  <img src="https://img.icons8.com/external-vitaliy-gorbachev-blue-vitaly-gorbachev/40/000000/external-https-internet-security-vitaliy-gorbachev-blue-vitaly-gorbachev.png"/> ¿ Que es HTTP (Hypertext Transfer Protocol)?

Es la base de cualquier intercambio de datos en la web. Nos permite enviar y recibir datos y recursos, como pueden ser documentos HTML. Es un protocolo de estructura cliente-servidor.

El cliente (normalmente un navegador Web) inicia una **petición** de datos a un servidor Web. El servidor Web la recibe y este le envía una **respuesta** (favorable o no) al cliente.

-> El Front se comunica con el Back mediante el protocolo, el servidor recibe la peticion y envia una respuesta.

```
USUARIO ---->   URL    -----> NAVEGADOR -----> PETICION HTTP  -----> SERVIDOR 
       <----PAGINA WEB <-----           <----- RESPUESTA HTTP <----    WEB
```

#### :star: Métodos de Petición HTTP


Este protocolo posee un conjunto de métodos para indicar la acción que se desea realizar al momento de realizar una petición al servidor web. Los más usados son:


- **GET** -> solicita una informacion específica. Las peticiones que usan el método GET sólo deben recuperar datos. -> Es como un READ.

- **POST** -> se utiliza para enviar una información que genera cambios en el estado o efectos secundarios en el servidor (para crear el usuario, se recibe la informacion con el body).

- **PUT** -> sirve para actualizar o modificar un recurso o información alojada en el servidor con datos nuevos que se encuentran en la petición (para actualizar, actualiza más cosas que patch, sobreescribe).

- **PATCH** -> es utilizado para aplicar moficicaciones o actualizaciones parciales a un recurso o información (para actualizar, modifica).

- **DELETE** -> borra un recurso o información en específico.

-> **soft delete** en realidad no eliminas de la base de datos, sino haces un borrado logico, por ejemplo le guardas la fecha de eliminacion para no mostrarlo, pero sigue estando en la base de datos.


### :star:  JSON JavaScript Object Notation

La notación por excelencia para la comunicación en JavaScript es JSON, no es más que enviar la información como objetos literales.


#### <img src="https://img.icons8.com/external-soft-fill-juicy-fish/40/000000/external-json-microservices-soft-fill-soft-fill-juicy-fish.png"/> ¿Qué es un objeto ?

La definición y concepto de objeto puede ser muy amplio dependiendo el enfoque al que querramos hacer referencia, pero en nuestro caso lo vamos a considerar una estructura de datos.

(Por le momento lo podemos pensar como un tipo de dato más auqnue esto es incorrecto).


####  <img src="https://img.icons8.com/external-soft-fill-juicy-fish/40/000000/external-json-microservices-soft-fill-soft-fill-juicy-fish.png"/> La estructura de un objeto 


```JavaScript
{
  user: "Jhon",
  lastName: "Doe"
}
```

####  <img src="https://img.icons8.com/external-soft-fill-juicy-fish/40/000000/external-json-microservices-soft-fill-soft-fill-juicy-fish.png"/> ¿ Qué es un formulario ?

Un formulario es un elemento gráfico para que un usuario introduzca **datos estructurados**.



### :star: Network en el navegador

El dominar las herramientas que nos dan los navegadores para desarrollar puede facilitar demasiado el trabajo.

Algo de lo que disponemos es de la sección **network** que nos permite ver la comunicación de nuestra web.


#### ¿Donde encontrarlo ?


1. Abrir el navegador en la página que se desea y apretar F12 o click derecho y luego inspeccionar.

2. Se abrirá un menú con diferentes opciones, seleccionar en la parte superior la tab network.

3. Se podrá ver mucha información y opciones entre las que se destaca un listado de todas las peticiones realizadas.

-> [Listado de los estados](https://es.wikipedia.org/wiki/Anexo:C%C3%B3digos_de_estado_HTTP)

4. Al clickear en una de las peticiones se puede ver su detalle.



### Consideración de seguridad

El protocolo de comunicaicón HTTP es conssiderado inseguro, hoy se utiliza el protocolo **HTTPS** que es prácticamente igual pero la información viaja cifrada, autenticada e integra. Hoy en día es prácticamente obligatorio su uso en proyectos que ya estén publicados.


#### ¿ Cómo utilizar un protocolo HTTP ?

Para utilizar un protocolo HTTPS se necesita obtener un **certificado SSL** de una certificadora reconocida.Hoy en día es muy fácil obtener el certificado de cualquier proveedor de hosting o cloud.

También existe la opción de obtenerlo de proveedores gratuitos donde destaca https://letsencrypt.org.

Comunmente la implementación de estos certificados no es llevada por los desarrolladores Front-End pero es importante que conozcan su importancia.

---
---

# :star2: TEORIA DE MODULO 1 - UNIDAD 1 Y 2

---

## OBJETIVOS DEL MODULO

```
-Iniciar nuestros primeros pasos en la librería de React reconociendo su sintaxis, funcionalidades 
y componentes básicos.
-Identificar las herramientas necesarias para el desarrollo de la aplicación.
-Instalar las tecnologías indispensables para nuestro trabajo.
-Configurar nuestro entorno de trabajo.
-Armar el componente login que permitirá a las personas que usan tu aplicación, loguearse en ella.
-Lograr validar el formulario de logueo para evitar que una persona con credenciales erradas pueda 
hacer uso de la aplicación.
-Poder enviar los datos suministrados por la persona a una API para que de esta última puedas 
obtener el token de autenticación.
-Implementar el manejo de mensajes de error con la librería Sweet Alert.
-Persistir el token obtenido de la API, en el almacenamiento local del navegador.
-Generar un redireccionamiento al componente "Listado" una vez las credenciales de usuario estén 
validadas y la API haya entregado el respectivo token de autenticación.
```

## :star: UNIDAD 1

---

## SET UP DE TOOLS  

- [VSC](https://code.visualstudio.com/)

- [Create Reaact App](https://es.reactjs.org/docs/create-a-new-react-app.html)

- [Node.js]([Node.js](https://nodejs.org/es/))


### 1.1 SET UP DE HERRAMIENTAS

- extension en VSC: JS JSX Snippet 

- Node.js en su ultima versión estable, con **node** se instala un **entorno de desarrollo**, para ver que esta bien instalado desde la terminal ponemos ```node -v``` o ```node -version``` y si ves la version de Node.js es que ya está instalado correctamente.

- **Create React App (CRA)** configura un ambiente de desarrollo de forma que puedas usar JavaScript, brindando una buena experiencia de desarrollo y optimizando tu aplicación. Necesitarás tener **Node >= 14.0.0** y **npm >= 5.6** instalados en tu máquina. Para crear un proyecto ejecuta:

```
npx create-react-app my-app ./
cd my-app
nmp start
```

- Create React App no se encarga de la lógica de backend o de bases de datos, tan solo crea un flujo de construcción para frontend, de manera que lo puedas usar con cualquier backend. Para ello internamente usa Babel y Webpack, pero no necesitas saber nada de estas herramientas para usar Create React App.

- React Developer Tools. Si bien esta herramienta es opcional, constituye un gran aliado para poder ver cómo fluyen los datos entre componentes de React


---

## 1.2 INTRODUCCION A REACT (parte 2)

### ¿Qué es React? 

Es una biblioteca desarrollada inicialmente por **Facebook** (ahora llamado **Meta**) y su principal ventaja es ser de software libre. Sus primeros usos fueron en aplicaciones como Facebook e Instagram. Otras empresas web de primer nivel también lo incorporaron, como Wallmart, Netflix, Airbnb, Dropbox, Spotify, etc.

Se creó para hacer el **desarrollo de los componentes de las interfaces del usuario más fácil** y su requisito principal es **ofrecer un rendimiento mayor al de las otras alternativas existentes en el mercado**.

### ¿Cómo funciona?

#### Componentes

Al ser una librería moderna, nos permite crear una aplicación con conceptos novedosos como la noción de **componentes**, que permite **dividir una aplicación en pequeñas partes para así poder crear y administrar una aplicación compleja de una manera mucho más sencilla y entendible**, ya que estos componentes de React tienen la ventaja de ser:

- Reusables.

- Fáciles de crear y usar.

- Fáciles para comprobar su funcionamiento.

Para utilizar esta librería necesitamos tener un par de requisitos básicos en cuenta: 

- Manipulación de HTML: sus etiquetas y el DOM.

- Compresión de JavaScript.

- Práctica en el uso de ECMA6 como: arrow functions, template, métodos, etc.

#### DOM Virtual

React enfatiza la **necesidad de actualizar las vistas** cuando el desarrollador lo requiera y lo consigue mediante el **DOM Virtual**.

El DOM Virtual es una de las características principales de React. Este hace referencia a **una representación del DOM**, pero en lugar de seguir la forma tradicional, **lo hace en la memoria**, es decir, que **rerenderizará solo el HTML modificado**.

Se utiliza para aumentar el rendimiento de las aplicaciones y componentes con las que interactúa el usuario directamente. Así, se puede ofrecer una **mejor experiencia de usuario y una mayor fluidez**.

#### (SPA) Aplicación de página única

Una aplicación de página única (single-page application) es **una app que carga una única página HTML y todos los componentes necesarios (tales como JavaScript y CSS) para que se ejecute la aplicación**. Cualquier interacción con la página o páginas subsecuentes no requiere hacer solicitudes al servidor, lo que significa que **la página no es recargada**.

Aunque se puede construir una aplicación de página única con React, esto no es un requerimiento. React también puede ser utilizado para mejorar pequeñas partes de sitios web existentes con interactividad adicional. 

#### Las diferencias de crear un sitio común de cero

Demos un paseo por el espacio de la tecnología antes de 2015, cuando el desarrollo web se trataba de secuencias de comandos y renderizado. La época en que lenguajes como HTML, CSS dominaban el frontend y PHP dominaba el backend.

El desarrollo web era distinto en ese entonces. Todo lo que teníamos que hacer era maquetar páginas HTML estáticas en algunas carpetas y renderizar usando PHP. Aunque esa no es una forma única e intuitiva de desarrollar sitios web, aun pudiendo establecer una conexión bidireccional entre el cliente y el servidor.

Todo el mérito es para la representación del lado del servidor (SSR). Hemos estado construyendo aplicaciones web de esta manera durante mucho tiempo, pero lo que no vimos venir es la revolución de los sitios web después de las librerías JavaScript como React.

---

## 1.3 INTRODUCCION A REACT (parte 3)

### Sistema de archivos de React

Luego de finalizar la instalación de React, nuestro sistema de archivos se parecerá a lo siguiente:

```
-1. Nombre de mi proyecto: el nombre que le dimos al instalar vite.
-2. node_modules: es un directorio que se crea en la carpeta raíz de nuestro 
proyecto cuando instalamos paquetes o dependencias mediante npm.
-3. src: directorio en donde se encontrarán todos los archivos referidos a React.
-4. App.css: archivo de CSS que usa el archivo App.jsx (en las próximas lecturas veremos qué es JSX).
-5. App.js: este va a ser el archivo en el que trabajaremos inicialmente como "padre" de todos 
los demás componentes que crearemos.
-6. favicon.svg: si queremos que tenga un ícono como imagen la url al navegar por nuestro sitio.
-7. index.css: archivo de CSS global que usa el sitio.
-8. logo.svg: imagen que se encuentra en App.jsx.
-9. index.js: este archivo no lo tocaremos nunca, lo dejaremos siempre así.
-10. .gitignore: si vamos a usar GIT, ya tendremos este archivo preparado para no subir archivos 
a github que no sean necesarios.
-11. public: directorio en donde encontrarán todos los archivos referenciados a la vista.
-12. index.html: donde se inicializará nuestro proyecto, y podremos incluir en el "head" llamadas 
a otros archivos, tales como CSS, JS, etc.
-13. package-lock.json: se genera automáticamente para cualquier operación en la que npm modifique 
el árbol 1 node_modules o package.json. Describe una representación única de un árbol de dependencias 
de modo que se garantice que los compañeros de equipo, las implementaciones y la integración 
continua instalen exactamente las mismas dependencias.
-14. package.json: contiene todos los metadatos acerca del proyecto, tal como descripción, 
licencia, dependencias y scripts.
```


Y me queda:
```
myfirstreactapp
├── node_modules
├── public
│ ├── favicon.ico
│ ├── index.html
│ └── robots.txt
├── src
│ ├── App.css
│ ├── App.js
│ ├── App.test.js
│ ├── index.css
│ ├── index.js
│ ├── logo.svg
│ ├── serviceWorker.js
│ └── setupTests.js
├── .gititgnore
├── package.json
├── package-lock.json
└── README.md
```

#### Iniciar el servidor de desarrollo de aplicaciones React

¡Comencemos juntos con nuestro primer código usando React!

A continuación, simplemente estaremos modificando "App.js". Quizás notaste que está en mayúsculas, pero eso lo veremos más adelante. 

Actualmente, el código de la imagen anterior es el que aparece cuando lo abrimos, sin embargo, debe quedar como el de la figura a continuación. Te habrás dado cuenta de que hay archivos que deberemos eliminar porque no los usaremos.

```
myfirstreactapp
├── node_modules
|
├── public
│ ├── favicon.ico
│ ├── index.html
│ └── robots.txt
|
├── src
│ ├── App.js
│ ├── index.js
|
├── .gititgnore
├── package.json
├── package-lock.json
└── README.md
```

- index.js (define que va a renderizar mi aplicación):
```JSX
import React from "react";
import ReactDOM from "react-dom";
omport App from "./App";

ReactDOM.render(
  <React.StrcitMode >
    <App />
  </React.StrictMode>,
  document.getElementById("root")
);
```

-App.js (donde vamosa  venir a codear todo y es el que se va a montar dentro del compoennte index)
```JSX
function App() {
  return (
    <h2> Hola Mundo </h2>
  )
}

export default App;
```
---

## :star: UNIDAD 2 - CREANDO NUESTRO PRIMER COMPONENTE

---

### 2.1 ARMANDO COMPONENTE

#### ¿Qué es el componente "Login"?

Este componente es el que va a permitir que las personas que usan la aplicación se logueen en la misma. El mismo estará compuesto por un breve formulario con dos campos: correo electrónico y contraseña, los cuales funcionarán como un mecanismo de entrada de información para el proceso de autenticación de usuarios.

#### ¿Para qué sirve el componente "Login"?

Este componente tiene como objetivo principal servir como un filtro de usuarios, para que, solamente aquellas personas que se loguean con las credenciales válidas puedan usar el completo de la aplicación.

#### ¿Cómo se implementa el proceso de Login en un proyecto real?

Esto es algo bastante habitual, pues muchas aplicaciones para que puedan ser usadas, necesitan autenticar al usuario para así proveer de toda su funcionalidad. Por ello es importante conocer cuáles son los pasos a dar para poder llevar adelante esta implementación, la cual, posteriormente seguramente usaremos en muchas ocasiones en nuestra vida diaria.

---

### 2.2 VALIDACION DE FORMULARIO 

#### ¿Qué es la validación de formularios?

La validación es el proceso que nos permite corroborar (como developers) que la información suministrada de parte del usuario y que requiere nuestro sistema para funcionar, sea la correcta.

#### ¿Para qué sirve la validación de formularios?

La validación de formularios nos permite corroborar que la información que estamos recibiendo y que posteriormente enviaremos al servidor sea correcta y no presente errores. En el desarrollo de aplicaciones siempre estaremos en la búsqueda constante de la optimización y no sería lógico ni performante enviar al servidor información errada, pues lo estaríamos sobrecargando con responsabilidades y tareas que podrías resolver fácilmente del lado del cliente. La validación de formularios, entonces, sirve para resolver en el entorno del cliente los posibles problemas que se puedan llegar a presentar.

#### ¿Qué ejemplos existen sobre la validación de formularios?

El más común lo encontramos en los formularios de registro. En estos formularios, al momento de poner nuestra dirección de correo electrónico, se verifica que la misma coincida con el formato habitual: "user@server.ext". De no coincidir nuestra información ingresada con este formato, obtendremos algún mensaje alertándonos de este error.

#### ¿Cómo se implementa la validación de formularios en un proyecto real?

De la misma manera que lo haremos en esta clase. Siempre que deseemos verificar que la información ingresada por el usuario es la correcta, es entonces allí en donde necesitaremos de estos procesos de validación.

---

## 2.3 ENVIO DE FORMULARIO

#### ¿Qué es el envío de formularios vía HTTP?

Los formularios en HTML no son nada más que presentacionales, y para poder usar la información suministrada por el usuario tendremos que enviar la misma a algún lugar, tradicionalmente a una API. Y para poder generar el envío de dicha información necesitaremos implementar algún método HTTP que nos permita hacer esto. 

#### ¿Para qué sirve el envío de información vía HTTP?

Tal como lo mencionamos anteriormente, un formulario HTML no es funcional si no enviamos su información a algún lugar. Y por este motivo es que los métodos HTTP tales como GET, POST o PUT nos van a ser de gran utilidad, pues con estos métodos tendremos la posibilidad de hacerle llegar al servidor aquellos datos que el usuario ha dejado en nuestra aplicación.

#### ¿Dónde se pone en uso el envío de información vía HTTP?

Generalmente, siempre que diligencies un formulario (como el de login, registro, contacto, etc) y des click en el botón "ENVIAR", allí mismo estás disparando un envío de la información vía HTTP, para que sea el servidor quien procese dicha información y pueda darte una respuesta dependiendo de la información suministrada.

#### ¿Cómo se implementa el envío de información vía HTTP en un proyecto real?

En los formularios de contacto, de registro, de logueo o en cualquier otra petición que obtenga o envíe datos desde y hacia el servidor se implementan este tipo de solicitudes HTTP.

---

#### 2.4 MANEJO DE ERRORES


#### ¿Qué es el manejo de errores?

El manejo de errores es la técnica a través de la cual como desarrolladores podemos manejar las distintas respuestas obtenidas después de enviar información a una API o incluso cuando nos encontramos validando la información de un formulario.

#### ¿Para qué sirve el manejo de errores?

Sirve para advertir a la persona que usa nuestra aplicación de los posibles errores que se encontraron en el procesamiento de la información, sea porque suministró información errada o quizás porque aun habiendo suministrado la información correcta, el servidor no pudo procesarla de manera satisfactoria.

#### ¿Cómo se implementa el manejo de errores en un proyecto real?


Existen diversas maneras de hacerlo, pero una muy común es hacerlo usando librerías que nos permitan disparar cajas modales que alerten e informen al usuario del error resultante de la operación. Puntualmente en esta clase implementaremos la librería "Sweet alert" para poder mostrar estos mensajes de una manera mucho más amigable para el usuario.


---

## 2.5 PERSISTENCIA DEL TOKEN

#### ¿Qué es un token y qué significa la persistencia del mismo?

Un token es un identificador único obtenido tras un proceso de autenticación que le permite saber al servidor que la persona que usa la aplicación se ha logueado satisfactoriamente. Por otro lado, persistir un token significa mantenerlo guardado en algún lugar para posteriormente usar su información. Para que, de esta manera, evitemos solicitar al usuario en cada momento sus credenciales de acceso.

#### ¿Para qué sirve la persistencia del token?

Cómo ya lo dijimos con anterioridad, sirve para evitar hacer múltiples solicitudes de autenticación al servidor, cada vez que el usuario de la aplicación desea llevar a cabo una determinada actividad. Por este motivo, el token es tan importante ya que lo obtendremos en el primer llamado de autenticación y desde ese momento en adelante usaremos el mismo cada vez que sea necesario.

#### ¿Cómo se implementa la persistencia del token en un proyecto real?

Existen algunos caminos para lograr este resultado, pero el más sencillo y cómodo para nosotros será guardar el mismo en el almacenamiento local del navegador, de esta manera aprovecharemos las múltiples ventajas de este tipo de almacenamiento.

---

## 2.6 REDIRECICONAMIENTO AL COMPONENTE "LISTADO"


#### ¿Qué es un redireccionamiento?

El redireccionamiento es un proceso mediante el cual, después de ejecutar una acción determinada, llevamos a la persona que usa nuestra aplicación a una ubicación específica. Es muy común de implementar en el proceso de logueo, en el cual después de validar las credenciales de una persona, le daremos acceso completo a la aplicación. Vale aclarar que una redirección también se puede generar cuando nos damos cuenta que sin tener los permisos correspondientes, una persona desea ingresar a una sección a la que no tiene permiso.

#### ¿Para qué sirve la redirección?

Sirve para enviar a la persona que usa nuestro sistema a un determinado lugar después de ejecutar una acción. Sirve puntualmente para proteger secciones de la aplicación que requieren que la persona usuaria tenga permisos específicos.

#### ¿Qué ejemplos existen sobre el redireccionamiento?

El más sencillo y el que puedes probar por tu cuenta es el siguiente: estando logueado en tu cuenta de correo, dirígete a la bandeja de entrada, allí copia la dirección presente en la barra de direcciones. Ahora, ve a una ventana de incógnito en tu navegador y pega la dirección que copiaste anteriormente. ¿Pudiste entrar a la bandeja de entrada de tu correo electrónico? Estamos seguros que no. Y que lo que sucedió fue que el sistema te redireccionó a la sección en donde debes loguearte en tu cuenta de correo. Si esto fue lo que sucedió, tienes un ejemplo claro de lo que es una redirección.
Enlaces y documentación
Visual Studio Code: Desde este enlace podrás descargar el editor de texto más utilizado por todo el mundo desde hace ya un par de años. Excelente para escribir código en cualquier lenguaje de programación.

- **NodeJS**: Descarga este entorno de ejecución para JavaScript, que te permitirá construir cualquier tipo de aplicación usando JS.

- **ReactJS**: Documentación oficial de esta librería para el manejo de interfaces en el Frontend. Siempre que tengas una duda, seguramente vendrás a este enlace.

-**Axios**: Descubre la documentación oficial de la librería más utilizada en el ambiente del desarrollo para hacer peticiones asíncronas y aprende un poco más sobre la misma.

-**Sweet Alert**: Descubre todo el poder de las cajas modales gracias a Sweet Alert.

-**React router dom**: Si estás buscando construir una SPA (single page application) con React esta librería es infaltable. Ya que la misma te permite gestionar todo el sistema de ruteo de la misma. Con esta sencilla pero eficiente documentación, cualquier duda que tengas, será resuelta.

---
---
