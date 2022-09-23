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

## :star: <img src="https://img.icons8.com/color/48/000000/video.png"/> Teroía del campus con los videos

- [Aca se puede ver la teoria y la práctica que tenemos con los videos del Alkemy Challenge](https://github.com/eugenia1984/react_softtek/blob/main/modulo01/teoria_unidad_1_2.md)

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
2. node_modules -> con todas las depndencias y librerias. Tengo todos mis paquetes.
3. src -> aca ven todos mis componentes, tambien puedo agrupar en *pages* y en *components* y dentro de components puedo agrupar en carpetas los componentes.
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


## :star2: Clase 23 Septiembre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> UNIDAD 1: Introducción a React:

---

## Temas a ver

```
- Ejercicio de reapso
- Manejo de errores
- Agregar manejo de errores al componente <Login />
- Persistencia del Token de Autenticación
- Redireccionamiento
- Redireccionamiento al componente <Listado />
```

---

## 1 - Ejercicio de reapso

Coo poner el en index.js los componentes para importarlos y no tener que poner todo el path.

index.js:
```JSX
export { default as Logo} from "./Logo";
```

App.js:
```JSX
import {Header} from "/components/Header";
```

---

## 2 - Manejo de errores

### ¿ Qué es ?

Es la técnica que usamos como desarrolladores para controlar los errores durante la ejecución de un programa.

Cuando ocurre cierto timepo de error, nosotros podemos programar en el sistema un fragmento de código que resuelve la situación.

Ejemplos de estos pueden ser cuando retornamos un mensaje de error o devolvemos un error por defecto.

### ¿ Para qué sirve ?

Sirve para advertir a los usuarios que usan nuestra aplicación de los posibles errores que se encontraron en el procesamiento de la información, ya sea porque se suministro información errada o el servidor no pudo procesar la misma de manera setisfactoria.


### Maneras de manejar errores en aplicaciones React

Existen varias formas y vamos a explicar un poco algunas de ellas:

- **Alertas visuales (páginas de error, notificaciones, etc)**: son aquellos elementos en la interfaz de usuario que poseen mensajes que el usuario puede leer y entender, es decir, no muestra el mensaje original cuando ocurre un error.

- **Método try-catch**: es una gran herramienta para detectar el código que se comporta mal y garantizar que nuestra aplicaicón no deje de funcionar inesperadamente. Señala un bloque de instrucciones a intentar (**try**) y especifica una respuesta si se produce una excepción (**Catch**).

Veamos un ejemplo:

```JavaScript
try {
  somethingBadMightHAppend();
} catch(error) {
  console.log("Something bad happend");
  console.error(error);
}
```

```JavaScript
const fetchData = async () = {
  try {
    return await fetch("https://some-url-that-might-fail.com");
  } catch(error){
    console.log(error); // You might send an exception to your tracker like AssSignal
  }
}

```

-> También podemos usarlo dentro de una función manejadora de eventos
```JavaScript
const handlerCLick = () => {
  try {
    throw Error("Oh, no");
  }catch(error) {
    setError(error);
  }
}
```

-> Y en las llamadas de setTimeOut:
```JavaScript
const handlerCLick = () => {
  setTimeOut(() => {
    try {
      throw error("Oh, no, an error: (*));
    } catch(error) {
      setError(error);
    }
  }, 1880);
}
```


---

## 3 - Agregar manejo de errores al componente <Login />

Con los if voy validando que no estén vacios,  o con RegEx que cumpla con el formato de un formulario, por ejemplo.

Una vez que este ok el ingreso de los datos de los input dle login y los tengo en valores, me armo otra carpeta **Services** con el archivo **UserServices.js** donde voy a tener el **fetch** (con **async** - **await**) o uso **Axios** para hacer la llamada al servidor, lo encapsulo en una **promesa** y lo guardo.

-> Tenemos la librería **Sweet Alert** para tener una ventanas lindas al avisar al usuario que es lo que tiene el error.

---

## 4 - Persistencia del Token de Autenticación

---

## 5 - Redireccionamiento

---

## 6 - Redireccionamiento al componente <Listado />

---
---


