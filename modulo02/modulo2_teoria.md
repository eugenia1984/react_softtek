# :star2: Teoría Módulo 2 - Unidad 2 - Armado y diseño de nuestros componentes :star2:

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

## :star2: MODULO 2 - UNIDAD 1 -  DISEÑO DE LA ESTRUCTURA BÁSICA :star2:

### :star: 3.1 ARMADO ENCABEZADO / NAVEGACION


#### <img src="https://img.icons8.com/ios-glyphs/40/000000/head-profile.png"/> ¿Para qué nos servirá este componente?

Este componente tiene como finalidad contener una barra de navegación que esté presente a lo largo de toda la aplicación. A su vez, servirá facilitar el ingreso a las distintas rutas que han sido configuradas y en las cuales podremos ver la información esperada.

#### <img src="https://img.icons8.com/ios-glyphs/40/000000/head-profile.png"/> ¿Por qué es importante contar con una barra de navegación?

Las barras de navegación en las aplicaciones web son algo muy común, ya que, como lo mencionamos antes, le permiten al visitante de la página, acceder a cualquier ruta que esté disponible. Además, al implementar una barra de navegación no solamente estaremos aprendiendo cómo generar la estructura a través de JSX, sino que también entenderemos cómo funciona el sistema de ruteo dentro de una SPA (single page application).

#### <img src="https://img.icons8.com/ios-glyphs/40/000000/head-profile.png"/> ¿El encabezado y la barra de navegación pueden tener lógica condicional?

Entendiendo que la lógica condicional nos va a permitir mostrar o no algunas porciones de contenido y que particularmente estamos hablando de la implementación de algunos if/else, la respuesta sería: claro que sí. Esto se debe a que particularmente ese será uno de los objetivos de esta unidad, pues de esa manera podrás aprender a implementar partes de la barra de navegación que solamente estén presentes si el visitante de la aplicación se ha autenticado correctamente.

```JSX
function Header () {
  return (
    <header>
      <nav>
        <ul>
          <li>Home</li>
          <li>Listado</li>
          <li>Contacto</li>
        </ul>
      </nav>
    </header>
  )
}

export default Header;
```

-> Me falta ver como implementar el **Link** de **react-router-dom** para los links del NavBar.

---

### :star: 3.2 ARMADO DE PIE DE PAGINA

#### <img src="https://img.icons8.com/ios-filled/40/000000/right-footprint.png"/>  ¿Es necesario que toda aplicación posea un pie de página?

No hay nada escrito al respecto y bien esto podría tener una respuesta bastante extensa. Sin embargo, para darte una respuesta más breve, la sugerencia será que siempre implementes un pie de página, así sea bastante sencillo, pues esta parte de contenido le podrá dar un cierre oficial a los demás bloques de contenido presentes dentro del documento. Además, si lo piensas un poco más, puedes aprovechar este espacio para disponer allí información no tan relevante, pero que sería bueno tener presente constantemente.


####  <img src="https://img.icons8.com/ios-filled/40/000000/right-footprint.png"/> ¿Puedo poner una barra de navegación en el pie de página?

Por supuesto, cualquier información que le aporte valor al visitante del sitio puede ir dentro de este apartado de contenido, pues aquí podrás dejar disponibles aquellos accesos directos a las secciones más relevantes de tu aplicación, los enlaces a las redes sociales o cosas por el estilo que le aporten más información a tu sitio web.
¿El pie de página se desarrolla como cualquier otro componente?
Totalmente. Pues de esta manera podrás tener de manera aislada todo su contenido y de ser necesario en un futuro, podrás modificar el mismo, sin afectar a otros apartados de la aplicación.

```JSX
function Footer() {
  return(
    <footer>
      <nav>
        <ul>
          <li>IG</li>
        </ul>
      </nav>
      <p>Copywright Alkemy Challenge</p>
    </footer>
  )
}

export default Footer;
```
---

### :star: 3.3 INTEGRACION DE ENCABEZADO / NAVEGACION


#### <img src="https://img.icons8.com/ios-glyphs/40/000000/head-profile.png"/>  <img src="https://img.icons8.com/ios-filled/40/000000/right-footprint.png"/> ¿Cómo se integra este componente con el resto de la aplicación?

De la manera más sencilla posible, pues debemos pensar que es un componente más, como cualquier otro. Y para implementarlo lo debemos tratar como tal.

####   <img src="https://img.icons8.com/ios-glyphs/40/000000/head-profile.png"/>  <img src="https://img.icons8.com/ios-filled/40/000000/right-footprint.png"/> ¿Por qué nos conviene hacerlo como un componente externo en vez de implementarlo directamente dentro del componente principal de la aplicación?

Siempre que pensemos que un apartado de código de la aplicación deberá estar presente a lo largo de la misma, es un buen indicador de que deberá ser tratado como un componente aparte, pues, de esta manera, podemos procurar un eficiente desarrollo del componente, pensando incluso en su futura escalabilidad.

####  <img src="https://img.icons8.com/ios-glyphs/40/000000/head-profile.png"/>  <img src="https://img.icons8.com/ios-filled/40/000000/right-footprint.png"/> La NO integración de este componente, ¿pone en riesgo el resto de la aplicación?

Realmente no, pero siendo sensatos, la mejor manera de permitir que quienes usan nuestra aplicación puedan acceder a cualquier parte de la misma, es haciendo uso de un encabezado que contenga una llamativa y contundente barra de navegación.

```JSX
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Login from "./components/login/Login.jsx";
import List from "./components/list/List.jsx";
import Header from "./components/header/Header.jsx";
import Footer from "./components/footer/Footer.jsx";
import "./css/App.css";

function App() {
  return (
    <div className="app">
      <Header />
      <BrowserRouter >
        <Routes>
          <Route path="/" element={<Login />} />
          <Route path="/listado" element={<List />} />
          <Route path="*" element={<Login />} />
        </Routes>
      </BrowserRouter>
      <Footer />
    </div>
  );
}

export default App;
```

---

### :star: 3.4 INTEGRACIÓN LIBRERIA CSS

#### <img src="https://img.icons8.com/external-others-pike-picture/40/000000/external-Library-knowledge-others-pike-picture.png"/> ¿Qué es una librería de CSS?

Quizás puede sonar un poco tonta la pregunta, pero recuerda: no hay pregunta tonta, lo tonto es no preguntar. 

Una librería de CSS es una serie de archivos que ya vienen preparados para ser usados directamente, sin escribir siquiera una línea de código CSS. 

Existen varias librerías de reconocida fama en el mercado. Quizás te suenen los nombres de Bootstrap, Tailwind o Bulma ¿no? Pues bien, estamos seguros que, en algún momento de tu vida, te habrás encontrado con alguna de ellas.

Te permite enfocarte más en la lógica de la aplicación que en el estilo visual.

#### <img src="https://img.icons8.com/external-others-pike-picture/40/000000/external-Library-knowledge-others-pike-picture.png"/> ¿Cuál es la ventaja de usar una librería de CSS?

La principal ventaja es la rapidez con la que podemos construir nuestra aplicación, pensando particularmente siempre en el código funcional, más no en el visual. Además, gracias a las librerías de CSS podemos implementar efectos muy llamativos que de otra manera nos hubiesen costado bastante esfuerzo.


#### <img src="https://img.icons8.com/external-others-pike-picture/40/000000/external-Library-knowledge-others-pike-picture.png"/> No me gustan las librerías de CSS, ¿puedo implementar mi propio código CSS dentro de React?

Claro que sí. Y no necesitas ser un experto para hacerlo. Es más, a lo largo de esta clase te vamos a mostrar cómo puedes, además de usar una librería, implementar tu propio CSS dentro de los componentes de React. Para que de esa manera puedas ponerle un poco de tu impronta a los estilos visuales de la aplicación.

-> Algunas librerias: Bootstrap, Tailwind, Bulma, Materialize

-> Solo necesitas descargarla e implementarla. Solo con Tailwind es distinta su implementación.

-> En el video se descargan todo bootstrap para usar solo la hoja de estilos: **bootras.min.css** para poder implementar las clases de bootstrap, en mi caso me voy a instalar por teminal **ReactBootstrap** y **Bootstrap**.

En el video:

App.js:
```JSX
import "./css/bootrap.main.css";
```

-> [https://react-bootstrap.github.io/](https://react-bootstrap.github.io/)

Instalación: ```npm install react-bootstrap bootstrap```

En el index.js o en App.js debo importarlo: ```import 'bootstrap/dist/css/bootstrap.min.css';```

---
---


## :star2: MODULO 2 - UNIDAD 2 -  ARMADO DE LA VISTA DE LISTADO :star2:

---

## :star: 4.1 ARMADO DE LA VISTA DE LISTADO

### <img src="https://img.icons8.com/bubbles/40/000000/list.png"/> ¿Para qué nos servirá este componente?

Este componente tiene como finalidad mostrar todos los datos recibidos desde la API. Aquí se deberán listar cada uno de los ítems recibidos, mostrando brevemente alguna parte de su información.


### <img src="https://img.icons8.com/bubbles/40/000000/list.png"/> ¿Cualquier aplicación hecha con React cuenta con este tipo de componente?

Generalmente sí, pues siempre que se quiera mostrar un gran conjunto de información (listado de productos, servicios, platos de comida, cartelera de cine, etc.) se necesita este tipo de lógica en el ámbito de frontend que permita, no solo tomar los datos de la API, sino también presentar esta información lo mejor posible de cara al visitante de la aplicación.


### <img src="https://img.icons8.com/bubbles/40/000000/list.png"/> ¿Cómo se presenta la información dentro de este componente?

Justamente eso es lo que aprenderemos en esta clase. Pero, para hacerte un breve resumen, lo primero será hacer el llamado a la API y una vez tengas su respuesta, almacenar los datos en el estado local del componente, para posteriormente a través de una iteración ir renderizando uno a uno los elementos obtenidos de dicha respuesta.

Tengo el componente **List**:

```JSX
return (
    <>
      <h2 className="listado-title">Listado</h2>
      <div className="row">
        <div className="col col-sm-6 col-md-4 col-lg-3">
          <CardList />
        </div>
      </div>
      <div className="btn-container">
        <button onClick={handlerClick} className="btn-listado">Cerrar</button>
      </div>
    </>
  );
  ```
  
  Y dentro el componente **CardList**:
  
  ```JSX
  import Button from 'react-bootstrap/Button';
import Card from 'react-bootstrap/Card';
import { Link } from "react-router-dom";

function CardList () {
  const url = "https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/000000/external-movie-movie-theater-flaticons-lineal-color-flat-icons-7.png";
  return (
    <Card >
      <Card.Img variant="top" src={url} />
      <Card.Body>
        <Card.Title>Movie Title</Card.Title>
        <Card.Text>
          Movie review
        </Card.Text>
        <Button variant="primary"><Link to="/">View Detail</Link></Button>
      </Card.Body>
    </Card>
  )
}

export default CardList;
  ```

---

## :star: 4.2 PROTECCION RUTA

### <img src="https://img.icons8.com/ios/50/000000/route.png"/> ¿Por qué es necesario proteger esta ruta?

Puntualmente en este challenge, es un requerimiento para que puedas demostrar tus habilidades. Pero es bueno que sepas que este proceso de "protección" de rutas es algo muy común, ya que el mismo te permite evitar que personas que no estén autenticadas en la aplicación, puedan ver información sensible de la misma.


###  <img src="https://img.icons8.com/ios/50/000000/route.png"/> ¿Cuál es el flujo exacto que se genera dentro de la aplicación al proteger esta ruta?

Como punto de partida, a esta ruta no se podrá ingresar si no se cuenta con la correspondiente autenticación de parte de la aplicación. Por eso, en dicho escenario, cualquier persona que carezca de credenciales válidas, será redireccionada al formulario de log in y su ingreso a esta ruta no será posible a menos que su usuario y contraseña sean los correctos.


### <img src="https://img.icons8.com/ios/50/000000/route.png"/> ¿Qué se necesita para poder proteger una ruta?

Una de las principales cosas que son necesarias para poder llevar a cabo esto, es una respuesta de parte del servidor que nos certifique en la parte del front que la persona que está usando la aplicación se ha autenticado correctamente. Generalmente a esto se le llama token. Y es gracias a la existencia del mismo que vamos a poder implementar toda la lógica que nos permita dar acceso o no a esta ruta.


### <img src="https://img.icons8.com/ios/50/000000/route.png"/> ¿Por qué el token tiene que ser generado del lado del servidor?

Esto se debe a que es el servidor quien almacena las credenciales (usuario y contraseña) de los usuarios de la aplicación. Pues, tener esta información del lado del frontend no solamente es casi imposible, sino que a su vez es altamente peligroso, pues cualquier persona con un poco de conocimiento, gracias a las herramientas de desarrollo del navegador, podría corromper esta información.

---

### :star: 4.3 OBTENCION DE LA API

### <img src="https://img.icons8.com/dotty/40/000000/api-settings.png"/> Listo, ya estamos logueados ¿y ahora?

Una vez logueados de manera satisfactoria en la aplicación. Lo que vamos a hacer ahora es disparar un pedido a la API para que la misma nos responda con la información esperada (listado de películas) y así poder renderizar dicha información correctamente en nuestra interfaz.


### <img src="https://img.icons8.com/dotty/40/000000/api-settings.png"/> ¿El uso de esta API demanda algún tipo de información especial?

No, pero sí. Generalmente para consultar una API, la misma demanda algo que tradicionalmente se conoce como una API key. La API key es algo que debemos obtener previamente de la API para, a través de esta, poder identificar que somos nosotros quienes haremos consultas al servidor.

Básicamente la API key es la que nos permite que nuestro llamado sea atendido. Y si bien no todas las APIS usan esta característica, la gran mayoría sí lo hace.


### <img src="https://img.icons8.com/dotty/40/000000/api-settings.png"/> Pero, ¿entonces la API key es lo mismo que el token?

No. El token es la confirmación de que la persona que se ha logueado en la aplicación lo hizo con las credenciales correctas, mientras que la API key es la llave que nos identifica frente a la API, para que la misma pueda atender nuestros llamados.


### <img src="https://img.icons8.com/dotty/40/000000/api-settings.png"/> Listo. La API nos respondió con la información ¿y ahora?

Ahora viene la parte divertida, pues después de recibir la información, tendrás que poner en práctica tus habilidades de HTML, CSS y JS para mapear esta información y poder presentarla de una manera linda y agradable.


### <img src="https://img.icons8.com/dotty/40/000000/api-settings.png"/> En un proyecto real, ¿qué tan común es trabajar con APIs?

Es lo más común de todo, pues la información que presentamos dentro de nuestro frontend, generalmente viene desde una API. Por ello es tan importante procesar estos conocimientos e implementarlos como algo habitual.


---

### :star: 4.4 RENDERIZACION DATOS EN COMPONENTE


### <img src="https://img.icons8.com/material-two-tone/40/000000/important-file.png"/> Cuando ya tenemos los datos ¿cómo mostramos los mismos en el componente?

Para esta labor vamos a necesitar trabajar con mucho JSX y con algunas herramientas como el método Map o Filter de JavaScript, pues son estos métodos los que comúnmente se utilizan para llevar a cabo dicho proceso.


### <img src="https://img.icons8.com/material-two-tone/40/000000/important-file.png"/> Pero, ¿se hace necesario usar si o si un Map o un Filter?

Sí, pues dentro del esquema JSX que trabaja React, no es posible usar un iterador como un for o un forEach para renderizar la información, por tal motivo se hace necesario entender cómo funciona el Map o el Filter y reconocer cuál es su estructura. 


### <img src="https://img.icons8.com/material-two-tone/40/000000/important-file.png"/> ¿Qué tan habitualmente se usa esto en un proyecto real?

Demasiado. Prácticamente cuando desarrollas dentro del entorno de React, te acostumbras a usar tanto el map o el filter, que se terminan volviendo tus mejores aliados de batalla en el proceso de desarrollo.


---

### :star: 4.5 MANEJO DE ERRORES (SWEET ALERT)


### <img src="https://img.icons8.com/color/48/000000/error--v1.png"/> Realmente, ¿es indispensable el manejo de errores en mi aplicación?

Como ya lo hablamos en momentos anteriores, el manejo de errores es la técnica a través de la cual como desarrolladores podemos manejar las distintas respuestas obtenidas después de procesar la información obtenida desde la API. Por tal motivo debemos servir de mecanismos funcionales a la persona que visita nuestra aplicación, para que sepa en qué momentos alguna petición generó un error como respuesta y sepa cómo actuar en consecuencia.


### <img src="https://img.icons8.com/color/48/000000/error--v1.png"/> Entendido, pero ¿necesito instalar otra librería para esto?

No, pues si anteriormente ya instalaste Sweet Alert, con ella es más que suficiente, aquí tu objetivo será entonces, identificar en qué momento tu aplicación pudiera generar un mensaje de error e implementar justo ahí un elemento visual informativo con dicha librería.


### <img src="https://img.icons8.com/color/48/000000/error--v1.png"/> En un proyecto real, ¿es obligatorio usar Sweet Alert para el manejo de errores?

No. El manejo de errores es algo crucial que debes implementar sí o sí, pero la manera como lo lleves a cabo y la implementación que decidas, corre 100% por tu cuenta en función de lo que te sea más cómodo y más útil de implementar.


---

## :star: 4.6 INGRESO AL DETALLE DE CADA ITEM


### <img src="https://img.icons8.com/color/48/000000/details-pane.png"/> ¿De qué trata el detalle de cada ítem?

Aquí vas a poder mostrar la información detallada de cada uno de los elementos recibidos como respuesta de la API. Como es común que en el listado completo de ítems solamente se muestre una pequeña porción de información, vamos a necesitar de un lugar determinado en donde mostrar el completo de la información. Y ese lugar, será el componente Detalle.


### <img src="https://img.icons8.com/color/48/000000/details-pane.png"/> Pero si tengo muchos ítems, ¿tengo que hacer muchos componentes "Detalle"?

No, ya que la idea fundamental es que este mismo componente te pueda servir para mostrar el detalle de cualquier ítem que el usuario haya seleccionado.


### <img src="https://img.icons8.com/color/48/000000/details-pane.png"/> Y eso, ¿cómo se hace?

Bueno, para lograr esto vamos a tener que hacer uso de las "rutas dinámicas" que nos provee React Router. 


### <img src="https://img.icons8.com/color/48/000000/details-pane.png"/> Y, ¿qué es una ruta dinámica?

Básicamente es una ruta como cualquier otra, pero que va a recibir como parámetro un bloque de información crucial que permitirá que el componente que se renderiza sea dinámico. Por ejemplo, en la siguiente ruta: http://localhost:3000/productos/45gb32F, la última parte (45gb32F) sería la parte dinámica, la misma vendría a representar el ID de un producto y dependiendo del ID:

http://localhost:3000/productos/56bhF

http://localhost:3000/productos/67rfG

Vamos a poder renderizar el detalle del producto que coincida con ese ID en particular. 

---
---

## :star2: MODULO 2 - UNIDAD 3 -  VISTA DE DETALLE :star2:

---

### :star: 5.2 VERIFICACION DE USUARIO Y TOKEN


### ¿Por qué es necesario seguir teniendo en cuenta el token?

Como hemos hablado anteriormente, no deseamos que algunas rutas sean accesibles si la persona no está correctamente logueada. Por ello, en el desarrollo de cualquier componente que estimemos que debe estar protegido, deberemos hacer siempre esta validación.

### Si tengo muchas rutas "protegidas", ¿deberé hacer siempre el mismo proceso para protegerlas?

Generalmente sí, pero si pones un poco más en desafío tus conocimientos, puedes incluso crear un componente reutilizable que constate si el token existe dentro de la aplicación. De esa manera no vas a tener que hacer muchas veces el mismo proceso.

### ¿Existe otra manera de proteger rutas que no sea a través de un token?

Realmente no, pues la más sencilla y habitual es manejar al token como un elemento prioritario e identificatorio único que te permita saber si la persona que usa la aplicación se ha identificado correctamente con sus credenciales.

---

### :star: 5.2 ARMADO DE VISTA DETALLE

### ¿Pará qué usamos este componente?

Dentro de este componente podremos mostrar la información específica de un ítem en particular. El desarrollo de este componente nos va a permitir crearlo y que el mismo sirva para mostrar cualquier ítem, sea que tengamos uno o sea que tengamos cien.

### ¿Dentro de este componente se hace necesario usar algún estado?

Generalmente sí, pues es en el estado en donde vamos a poder almacenar la información para posteriormente renderizarla en el JSX.

### ¿El componente detalle depende del componente listado para funcionar?

Si bien no están estrictamente vinculados para que uno funcione dependiendo del otro, sí será el componente listado quien envíe un identificador que nos permite saber a qué elemento en específico deberemos renderizar.

---

### :star: 5.3 OBTENER LOS DATOS DE LA API

### ¿De dónde sacaremos el identificador que nos permitirá hacer el llamado a la API?

Este identificador llegará a este componente en la URL, más exactamente dentro del query string y desde allí lo deberemos tomar para poder hacer el correspondiente llamado a la API.

### ¿Se suele usar este tipo de implementación en proyectos de la vida real?

Totalmente. Te puedes fijar por ejemplo en cualquier sitio de venta de productos y verás que siempre en la URL hay un elemento identificador que nos permite diferenciar este elemento de otro presente en nuestro listado de elementos.

### Pero, ¿cómo se obtiene esa información desde la URL?

Particularmente JS tiene un objeto que nos permite acceder a esta información para que, de esa manera, podamos tomar la porción de la URL que realmente necesitamos para hacer el llamado a la API.

---

### :star: 5.4 MOSTRAR LOS DATOS, RENDER DE LA INFORMACION

### Y ahora que tenemos la información necesaria, ¿qué haremos con ella?

A esta altura quizás ya te hayas percatado de que el trabajo dentro de los componentes de React suele ser algo similar, pues generalmente pedimos la información que necesitamos y posteriormente disponemos de la misma en pantalla para que sea consumida por las personas que usan nuestra aplicación. Así que ese será nuestro objetivo puntual en esta clase: mostrar el detalle de la información.

### Entiendo, pero ¿aquí también necesitamos usar el método .map()?

Posiblemente no, pero todo dependerá de la información recibida. Lo más importante que debes tener en cuenta para el uso del método .map(), es que cuando recibes un listado de información (array de objetos por ejemplo), allí es cuando el .map() cobra real significado y te brindará potencial ayuda.

###  ¿Este es el único componente que necesitaremos para mostrar el detalle de cualquier ítem de la lista?

Sí, y de eso se trata: de que un solo componente funcione para mostrar la información de cualquier elemento del listado, por ello aquí deberemos prestar especial atención a qué información recibiremos y sobre todo saber qué hacer si, por ejemplo, algunos elementos del listado no cuentan con esa información. Pero no te preocupes, pues hacer que todo funcione será realmente sencillo.

---

### :star: Enlaces y documentación

- [Bootstrap CSS](https://getbootstrap.com/): documentación oficial de esta gran librería de CSS. Estamos seguros de que ya la conoces, pero nunca está de más contar con el enlace a la mano.


- [Tailwind CSS](https://tailwindcss.com/): documentación oficial de esta genial librería que le viene comiendo los talones a Bootstrap. Si bien su uso difiere un poco de esta última, Tailwind se viene consolidando como una de las mejores librerías actualmente en el mundo del desarrollo de aplicaciones web.


- [Sass - Preprocesador de CSS](https://sass-lang.com/): si eres fanático del CSS y quieres llevar su potencial mucho más allá, no puedes dejar de leer esta documentación oficial, pues aquí vas a encontrar todas aquellas cosas que hacen de este preprocesador una de las mejores herramientas al momento de escribir CSS por tu cuenta.


- [Styled Components](https://styled-components.com/): si lo tuyo es escribir todo a la "React Way" esta librería de NPM para trabajar con componentes de estilo es lo mejor que podrás encontrar, pues implementa toda la lógica de un componente de React, con la virtud de poner implementar estilos CSS de una manera mucho más lógica y funcional.

---
---
