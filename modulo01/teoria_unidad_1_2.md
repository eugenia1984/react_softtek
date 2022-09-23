# :star2: TEORIA DE MODULO 1 - UNIDAD 1 Y 2

---

## OBJETIVOS DEL MODULO

```
-Iniciar nuestros primeros pasos en la librería de React reconociendo su sintaxis, 
funcionalidades y componentes básicos.
-Identificar las herramientas necesarias para el desarrollo de la aplicación.
-Instalar las tecnologías indispensables para nuestro trabajo.
-Configurar nuestro entorno de trabajo.
-Armar el componente login que permitirá a las personas que usan tu aplicación, 
loguearse en ella.
-Lograr validar el formulario de logueo para evitar que una persona con 
credenciales erradas pueda hacer uso de la aplicación.
-Poder enviar los datos suministrados por la persona a una API para que de 
esta última puedas obtener el token de autenticación.
-Implementar el manejo de mensajes de error con la librería Sweet Alert.
-Persistir el token obtenido de la API, en el almacenamiento local del navegador.
-Generar un redireccionamiento al componente "Listado" una vez las credenciales 
de usuario estén validadas y la API haya entregado el respectivo 
token de autenticación.
```

## :star: UNIDAD 1

---

## SET UP DE TOOLS  

- [VSC](https://code.visualstudio.com/)

- [Create Reaact App](https://es.reactjs.org/docs/create-a-new-react-app.html)

- [Node.js](https://nodejs.org/es/)


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
-2. node_modules: es un directorio que se crea en la carpeta raíz de nuestro proyecto cuando instalamos paquetes o dependencias mediante npm.
-3. src: directorio en donde se encontrarán todos los archivos referidos a React.
-4. App.css: archivo de CSS que usa el archivo App.jsx (en las próximas lecturas veremos qué es JSX).
-5. App.js: este va a ser el archivo en el que trabajaremos inicialmente como "padre" de todos los demás componentes que crearemos.
-6. favicon.svg: si queremos que tenga un ícono como imagen la url al navegar por nuestro sitio.
-7. index.css: archivo de CSS global que usa el sitio.
-8. logo.svg: imagen que se encuentra en App.jsx.
-9. index.js: este archivo no lo tocaremos nunca, lo dejaremos siempre así.
-10. .gitignore: si vamos a usar GIT, ya tendremos este archivo preparado para no subir archivos 
a github que no sean necesarios.
-11. public: directorio en donde encontrarán todos los archivos referenciados a la vista.
-12. index.html: donde se inicializará nuestro proyecto, y podremos incluir en el "head" llamadas a otros archivos, tales como CSS, JS, etc.
-13. package-lock.json: se genera automáticamente para cualquier operación en la que npm modifique el árbol 1 node_modules o package.json. Describe una representación única de un árbol de dependencias de modo que se garantice que los compañeros de equipo, las implementaciones y la integración continua instalen exactamente las mismas dependencias.
-14. package.json: contiene todos los metadatos acerca del proyecto, tal como descripción, licencia, dependencias y scripts.
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

-App.js (donde vamos a  venir a codear todo y es el que se va a montar dentro del compoennte index)
```JSX
function App() {
  return (
    <h2>Hola Mundo </h2>
  )
}

export default App;
```
---

## :star: UNIDAD 2 - CREANDO NUESTRO PRIMER COMPONENTE

---

### 2.1 ARMANDO COMPONENTE LOGIN

- Voy a crear la carpeta **components** y dentro mi primer componente **Login.js**
- 
```
├── src
| |
| |──components
| |   |──Login.js
| |
│ ├── App.js
│ ├── index.js
```

Y me queda así, con mi **form**, con los **input** para el e-mail y el password y el **burron** de Ingresar:

```JSX
function Login() {
  return (
    <form>
      <input 
        type="email" 
        name="email"
      />
      <input
        type="password"
        name="password" 
      />
      <button
        type="submit"
      >
        Ingresar
      </button>
    </form>  
  )
}

export default Login;
```

- Ahora tengo que hacer que este Login se vea en el App, para lo cual debo importarlo e invocarlo:

```JSX
import "./styles.css";
import Login from "./components/Login.js";

export default function App() {
  return (
    <div className="App">
      <h1>Hello world!</h1>
      <Login />
    </div>
  );
}
```

- Ahora vuelvo a mi Login y voy a agregarle un header, al tener en el return al header y al form en el mismo nivel debo encerrarlos en un **fragment** ya que JSX solo retorna uno. Y voy a agregar **labels**:

```JSX
 return (
    <>
      <h1>Formulario de Login</h1>
      <form>
        <label>
          <span>Correo electrónico:</span>
          <input 
            type="email" 
            name="email"
          />
        </label>  
        <br />
        <label>
          <span>Contraseña:</span>
          <input
            type="password"
            name="password" 
          />
        </label>
        <br />
        <button
          type="submit"
        >
          Ingresar
        </button>
      </form> 
    </> 
  )
}

export default Login;
```

-> Lo importante es tener los dos **input** que tengan sus respectivos **name** para poder luego capturar la información que llevan ingresada por el usuario.

- ¿ Qué es un **componente funcional** ? Es una función.


#### ¿Qué es el componente "Login"?

Este componente es el que va a permitir que las personas que usan la aplicación se logueen en la misma.

El mismo estará compuesto por un breve formulario con dos campos: **correo electrónico** y **contraseña**, los cuales funcionarán como un mecanismo de entrada de información para el proceso de autenticación de usuarios.


#### ¿Para qué sirve el componente "Login"?

Este componente tiene como objetivo principal servir como un **filtro de usuarios**, para que, **solamente aquellas personas que se loguean con las credenciales válidas puedan usar el completo de la aplicación**.


#### ¿Cómo se implementa el proceso de Login en un proyecto real?

Esto es algo bastante habitual, pues muchas aplicaciones para que puedan ser usadas, necesitan autenticar al usuario para así proveer de toda su funcionalidad. 

Por ello es importante conocer cuáles son los pasos a dar para poder llevar adelante esta implementación, la cual, posteriormente seguramente usaremos en muchas ocasiones en nuestra vida diaria.

---

### 2.2 VALIDACION DE FORMULARIO 


#### ¿Qué es la validación de formularios?

La validación es el proceso que **nos permite corroborar** (como developers) **que la información suministrada de parte del usuario y que requiere nuestro sistema para funcionar, sea la correcta**.


#### ¿Para qué sirve la validación de formularios?

La validación de formularios nos permite **corroborar que la información que estamos recibiendo y que posteriormente enviaremos al servidor sea correcta y no presente errores**. 

En el desarrollo de aplicaciones siempre estaremos en la búsqueda constante de la optimización y no sería lógico ni performante enviar al servidor información errada, pues lo estaríamos **sobrecargando** con responsabilidades y tareas que podrías resolver fácilmente del lado del cliente. La **validación de formularios**, entonces, sirve **para resolver en el entorno del cliente los posibles problemas que se puedan llegar a presentar**.



#### ¿Qué ejemplos existen sobre la validación de formularios?

El más común lo encontramos en los **formularios de registro**. 

En estos formularios, al momento de poner nuestra **dirección de correo electrónico**, se **verifica que la misma coincida con el formato habitual: "user@server.ext"**. 

De no coincidir nuestra información ingresada con este formato, obtendremos algún mensaje alertándonos de este error.



#### ¿Cómo se implementa la validación de formularios en un proyecto real?

De la misma manera que lo haremos en esta 
. 

Siempre que deseemos verificar que la información ingresada por el usuario es la correcta, es entonces allí en donde necesitaremos de estos procesos de validación.

1. Necesito ua función de tipo **handler** para que cuando se quiera ejecutar el formulario yo implemento toda la logica. En los **componentes funcionales** la lógica está al iniciod e la función, antes del return. Llamo a la función **submitHandler** y la voy a invocar dentro de la etiqueta del form **onSubmit={submitHandler}**

2. Necesito evitar el comportamiento de recarga (re renderización) que toene el formulario al hacer click en el botón de typo submit. Mi **submitHandler**  va a tener que recibir el **evento** y dentro ejecutar el método **preventDefault()**. Si ahora hago click en Enviar no se me recarga la pagina.

3. Ahora necesito capturar lo que se ingresa en el campo e-mail y password. Voy a guardar en las constantes, tomando lo que desencadena el **evento** con el **e.target** obtengo el campo y para agarrar el valor con **value** obtengo lo ingresado.

4. Ahora con el valor capturado voy a validar con un simple if, para ver que no llegue vacio.

```JSX
const submitHandler = (e) => {
    e.preventDefault();
    const email = e.target.email.value;
    const password = e.target.password.value;
    if(email === "" || password === "") {
      console.warn("Los campos no pueden estar vacíos");
    }
}
```

5. Ahora quiero verificar con una **regEx** que el string que se escribio en el input email, tenga la forma de un correo electrónico. 
```JavaScript
const regExEmail =  /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
```
Como voy a validar un String puedo utilizar le método **.test()** si lo que recibie por parametro cumple con mi RegEx, entonces me retorna true.

Voy a tener que cambiar en mi innput de name email a **type="text"**

```JSX
const submitHandler = (e) => {
    e.preventDefault();
    const email = e.target.email.value;
    const password = e.target.password.value;
    const regExEmail =  /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    
    if(email === "" || password === "") {
      console.warn("Los campos no pueden estar vacíos");
      return;
    }
    
    if(email !== "" && !regExEmail.test(email)) {
      console.log("Debes escribir una dirección de correo electrónico válida");
      return;
    }
    
    if(email !== "challenge@alkemy.org" || password !== "react") {
    
    }
    
}
```

-> Hago el return en el primer if, asi primero me quequea que los campos no esten vacios, de estar vacios entran aca, me lo consologuea y se termina por el return. Si los campos están completos, entonces ahi me va a quequear la regEx del correo que sea un formato valido.

-> Ahora nos valta verificar la información que se ingresó. Voy a validarlo con **challenge@alkemy.org** al e-mail y con **react** el password.
```JSX
if(email !== "challenge@alkemy.org" || password !== "react")  {
      console.warn("Credenciales inválidas");
      return;
}
```
-> Me queda:

```JSX
const submitHandler = (e) => {
    e.preventDefault();
    const email = e.target.email.value;
    const password = e.target.password.value;
    const regExEmail =  /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    
    if(email === "" || password === "") {
      console.warn("Los campos no pueden estar vacíos");
      return;
    }

    if(email !== "" && !regExEmail.test(email)) {
      console.warn("Debes escribir una dirección de correo electrónico válida");
      return;
    }

    if(email !== "challenge@alkemy.org" ||
      password !== "react")  {
        console.warn("Credenciales inválidas");
        return;
    }

    console.log("Ok estamos listos para enviar la información");
}
```
 
-> Cuando tanto el email como el password estén bien voy a ver: **console.log("Ok estamos listos para enviar la información");**

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


Existen diversas maneras de hacerlo, pero una muy común es hacerlo usando librerías que nos permitan disparar cajas modales que alerten e informen al usuario del error resultante de la operación. Puntualmente en esta clase implementaremos la librería [**Sweet alert**](https://sweetalert.js.org/guides/) para poder mostrar estos mensajes de una manera mucho más amigable para el usuario.

-> [Docmuentacion: https://sweetalert2.github.io/](https://sweetalert2.github.io/)

-> Intalacion: ```npm install sweetalert2``` o por CDN : ```<script src="//cdn.jsdelivr.net/npm/sweetalert2@11"></script>```

Y al usarla con React nos recomiendan también tener [Sweet Alert with React](https://www.npmjs.com/package/@sweetalert/with-react), que la instalamos asi: ```npm install @sweetalert/with-react```

Si nos da error probar con: ``` npm i @sweetalert/with-react --force```

-> Para poder usarlo lo importo en mi LoginForm:

```JSX
import swAlert from "sweetalert2";
```

-> Cada vez que queiera lanzar un alert utilizo la constante como funcion:

```JSX
swAlert.fire("Esto va a funcionar")
```

-> Entonces ahora reemplazamos los console.log con los alertas de weet alert.

---

### Axios

[https://axios-http.com/docs/intro](https://axios-http.com/docs/intro)

- Instalacion: ```npm i react```

- Lo importo:
```JSX
import Axios from "react";``` 
para poder utilizarlo

```JSX
axios
  .post("https://challenge-react.alkemy.org", {email, password})
  .then(res => {
    swAlert.fire("Perfecto, estás dentro")
    console.log(res.data);
  })
```

---

## 2.5 PERSISTENCIA DEL TOKEN

#### ¿Qué es un token y qué significa la persistencia del mismo?

Un token es **un identificador único obtenido tras un proceso de autenticación que le permite saber al servidor que la persona que usa la aplicación se ha logueado satisfactoriamente**. 

Por otro lado, **persistir un token** significa **mantenerlo guardado en algún lugar para posteriormente usar su información**. Para que, de esta manera, evitemos solicitar al usuario en cada momento sus credenciales de acceso.


#### ¿Para qué sirve la persistencia del token?

Cómo ya lo dijimos con anterioridad, sirve **para evitar hacer múltiples solicitudes de autenticación al servidor**, cada vez que el usuario de la aplicación desea llevar a cabo una determinada actividad. Por este motivo, el token es tan importante ya que lo obtendremos en el primer llamado de autenticación y desde ese momento en adelante usaremos el mismo cada vez que sea necesario.

-> El token es como la puerta de entrada a la siguiente petición, de modo que no voy a estar enviando constantemente la información de logueo, se manda una vez, se guarda y se usa esa información.


#### ¿Cómo se implementa la persistencia del token en un proyecto real?

Existen algunos caminos para lograr este resultado, pero el más sencillo y cómodo para nosotros será **guardar el mismo en el almacenamiento local del navegador**, de esta manera aprovecharemos las múltiples ventajas de este tipo de almacenamiento.

```JSX
axios
  .post("http://challenge-react.alkemy.org", {email, password})
  .then(res => {
    swAlert.fire("Perfecto, ingresaste correctamente");
    console.log(res.data);
  })
  ```

 -> Ya la API me esta dando el token.
 
 -> Vamos a almacenar el token directamente en el navegador. Para eso hay dos opciones, una vez recibida la información cpn **Res.data** y de ahi accedo a **token**:
 
 ```JSX
 const token = res.data.token;
 ```
 
 Ahora lo voy a almacenar directamente en el navegador a través del **localStorage** (aquello que el navegador nos provee para almacenar información). LocalStorage es un objeto que ya existe, por eso lo llamo y le voy a setear un item con **setItem**, y va a recibir dos argumentos...
 
 ... el 1ro va a setear el nombre de la propiedad bajo la cual voy a guardar la información.
 
 ... 2do es la informaicón que quiero guardar en él.
 
 ```JSX
 localStorage.setItem("token", token);
 ```
 
 -> Me queda seteado el token recibido de la API en la constante, gracias al metodo **setItem**. El token recibido es un String.



- ¿Cómo se que el token efectivamente quedó guardado?

-> Cuando quiera acceder al mismo lo hago con **getItem**.

```JAX
localStorage.getItem("token")
```

-> Si lo quiero borrar:

```JSX
localStorage.clear()
```

---

## 2.6 REDIRECICONAMIENTO AL COMPONENTE "LISTADO"


#### ¿Qué es un redireccionamiento?

El redireccionamiento **es un proceso mediante el cual, después de ejecutar una acción determinada, llevamos a la persona que usa nuestra aplicación a una ubicación específica**. Es muy común de implementar en el proceso de logueo, en el cual después de validar las credenciales de una persona, le daremos acceso completo a la aplicación.

Vale aclarar que una redirección también se puede generar cuando nos damos cuenta que sin tener los permisos correspondientes, una persona desea ingresar a una sección a la que no tiene permiso.


#### ¿Para qué sirve la redirección?

Sirve para enviar a la persona que usa nuestro sistema a un determinado lugar después de ejecutar una acción.

**Sirve puntualmente para proteger secciones de la aplicación que requieren que la persona usuaria tenga permisos específicos**.


#### ¿Qué ejemplos existen sobre el redireccionamiento?

El más sencillo y el que puedes probar por tu cuenta es el siguiente: 

-estando logueado en tu cuenta de correo

-dirígete a la bandeja de entrada

-allí copia la dirección presente en la barra de direcciones. 

-Ahora, ve a una ventana de incógnito en tu navegador y pega la dirección que copiaste anteriormente. 

¿Pudiste entrar a la bandeja de entrada de tu correo electrónico? Estamos seguros que no. 

Y que lo que sucedió fue que el sistema te redireccionó a la sección en donde debes loguearte en tu cuenta de correo. Si esto fue lo que sucedió, tienes un ejemplo claro de lo que es una redirección.

---

-> **React-Router-Dom** vamos a instalar la versión 6, en el video trabajan con la versión 5.

-> Lo instalamos con ```npm install react-ruter-dom```` ó ```npm i react-ruter-dom````

-> En el **index.js** voy a importar **BrowserRouter**:
```JSX
import { BrowserRouter } from "react-router-dom";
```

-> Voy a generar un envoltorio para todo mi componente App.

```JSX
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';
import { BrowserRouter } from "react-router-dom";

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <BrowserRouter >
      <App/> 
    </BrowserRouter>
  </React.StrictMode>
);
```

-> Me va a permitir gestionar una SPA.

-> Vuelvo a mi componente **App.js**, donde vamos a definir que compoennte se va a cargar dependneidno de la ruta.

Importamos dos componentes: **Route** y **Routes**:

```JSX
import { Routes, Route } from "react-router-dom";
```

Van a ser como un switcher que dependiendo la URL muestro cierto componente.

Para ello vamos a crear un nuevo componente llamado **Listado** y lo vamos a lalmar en App.js:

```JSX
import { Routes, Route } from "react-router-dom";

import Login from "./components/login/Login";
import Listado from "./components/listado/Listado";
```

-> Voy a tener a **Route** (ex Switch en version 5) con las rutas dentro con **Route** y cada una tendrá el **path** (la direccion de URL) y el **element**(ex component en version 5) que va a decir que componente renderizar

```JSX
import { Routes, Route } from "react-router-dom";

import Login from "./components/login/Login.js";
import Listado from "./components/listado/Listado.js";

function App() {
  return (
    <div className="App">
      <Routes>
        <Route path="/" element={Login}/>
        <Route path="/listado" element={Listado}/>
      </Routes>
    </div>
  );
}

export default App;
```
---

### Enlaces y documentación

- [**Visual Studio Code**](https://code.visualstudio.com/): Desde este enlace podrás descargar el editor de texto más utilizado por todo el mundo desde hace ya un par de años. Excelente para escribir código en cualquier lenguaje de programación.

- [**NodeJS**](https://nodejs.org/en/): Descarga este entorno de ejecución para JavaScript, que te permitirá construir cualquier tipo de aplicación usando JS.

- [**ReactJS**](https://reactjs.org/): Documentación oficial de esta librería para el manejo de interfaces en el Frontend. Siempre que tengas una duda, seguramente vendrás a este enlace.

- [**Axios**](https://axios-http.com/): Descubre la documentación oficial de la librería más utilizada en el ambiente del desarrollo para hacer peticiones asíncronas y aprende un poco más sobre la misma.

- [**Sweet Alert**](https://sweetalert.js.org/): Descubre todo el poder de las cajas modales gracias a Sweet Alert.

- [**React router dom**](https://reactrouter.com/en/main): Si estás buscando construir una SPA (single page application) con React esta librería es infaltable. Ya que la misma te permite gestionar todo el sistema de ruteo de la misma. Con esta sencilla pero eficiente documentación, cualquier duda que tengas, será resuelta.

---
---
