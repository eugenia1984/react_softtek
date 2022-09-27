# :star2: Módulo 2. Armado y diseño de nuestros componentes

---

## Unidad 3. Diseño de la estructura básica
```
- 3.1. Armado encabezado/navegación
- 3.2. Armado pie de página
- 3.3. Integración de encabezado/navegación
- 3.4. Integración de librería CSS
```

---

## Unidad 4. Armado de la vista de Listado
```
- 4.1. Armado de vista "Listado"
- 4.2. Protección ruta
- 4.3. Obtención datos de la API
- 4.4. Renderización datos en componente
- 4.5. Manejo de errores (sweet alert)
- 4.6. Ingreso al detalle de cada ítem
```

---

## Unidad 5. Vista de detalle
```
- 5.1. Verificación de usuario y token
- 5.2. Armado de la vista de detalle
- 5.3. Obtener los datos de la API
- 5.4. Mostrar los datos, render de información
```

---
---

# :star: Clase 26/9 * Modulo 2 * Unidad 3
---

## Temas a ver en clase:
```
- 1 - Presentación del Módulo 2
- 2 - Repasamos: importancia de los componentes
- 3 - Los componentes padres e hijos ( Children)
- 4 - Los props en React
- 5 - Componentes Layout
- 6 - Estilos en React
- 7 - Principales librerías de estilo
```

---

## MODULO 2 *  DISEÑO Y ARMADO DE COMPONENTES

####  <img src="https://img.icons8.com/material-outlined/40/000000/add-property-1.png"/> 1 - PRESENTACION DEL MODULO

En este módulo vamos a profundizar en la utilización de compoenntes como estructura básica de nuestro sitio web e implementar estilos a nuestro sitio web.

**1 - Armado de components y el flujo de información**

Vamos a implementar varios componentes y ver cómo se integra el flujo de información entre ellos.

**2 - Agregar estilos a nuestros componentes**

Vamos a ver cómo agregar estilos a cada uno de los componentes que vamos creando para que sean atractivos a los usuarios.

**3 - Renderización de la información**

Vamos a ver diferentes técnicas para mostrar la información de nuestros componentes de acuerdo a cómo están almacenados en las estructuras de objetos que nos provee JavaScript.

---

#### 2 - REPASAMOS: IMPORTANCIA DE LOS COMPONENTES

#### <img src="https://img.icons8.com/ios/40/000000/block.png"/> Los componentes permiten separar la interfaz de usuario en piezas independeintes, reutilizables y pensar en cada pieza de forma aislada.

Si por ejemplo estamos renderizando una calculadora, vamos a tener:

- Display number component

- Display Screen component

-> Toda la calculadora tiene un componente que envuelve a los otros subcompoenntes.

Documentación oficial de React: "no tengas miedo de dividir los componentes en otros más pequeños".


#### <img src="https://img.icons8.com/ios/40/000000/block.png"/> Repasamos la importancia de los Componentes

```
¿Se utiliza varias veces?                       ¿Es demasiado complejo?
Button  <---------------  ¿ Cuál es un    ----> App
Fields  <---------------  candidato a una ---->  Formularios
Labels  <---------------  extracción de   ----> Enrutamientos
Avatars <---------------  un componente?  ----> Chats
Menu    <--------------                  -----> Editor de imagenes
```

---

### 3 - LOS COMPONENTES PADRES E HIJOS (CHILDRENS)

#### <img src="https://img.icons8.com/external-flaticons-flat-flat-icons/40/000000/external-family-vacation-planning-trip-abroad-flaticons-flat-flat-icons-3.png"/> ¿ Qué es un componente padre ?

Un componente padre es un componente principal que puede o no tener secundarios (hijos).


En React , la relación entre un **componente padre** con sus **componentes hijos** no se da mediante herencia sino por **composición**.

#### ¿Qué es la composición ?

La composición es el acto de combinar partes o elementos para formar un todo. React posee un modelo potente de composición el cual se puede usar para dividir un componente complejo en componentes más pequeños y luego estructurar estos en componentes más pequeños para completar la aplicación.

### <img src="https://img.icons8.com/external-flaticons-flat-flat-icons/40/000000/external-family-vacation-planning-trip-abroad-flaticons-flat-flat-icons-3.png"/> ¿ Qué son los componentes hijos (Children)?

Los componentes hijos son aquellos elementos que se encuentran dentro de un componente padre.

Un componente hijo puede ser de varios tipos que vamos a ver a continuación:

- **componentes**: un componente hijo puede ser a su vez un componente padre.

- **elementos JSX**: aquellos que poseen la sintaxis de JSX.

- **objetos o vlaores de JavaScript**: como arrays, funciones, etc.


```
<Component > ---> un componente que acepta hijos
 //.....  ------>componentes / elementos (etiquetas HTML) / texto, numeros.
</Component>
```

---

### 4 - LAS PROPS EN REACT

#### <img src="https://img.icons8.com/material-outlined/40/000000/add-property-1.png"/> ¿ Qué son las props en React?

Las **props** en React se refiere al conjunto de **propiedades**, es decir, al **conjunto de datos que podemos compartir de un componente a otro** (**Desde un compoennte pare a un componente hijo**).

Las props son como **argumentos** que pasan a una función.

Las props pueden recordarte a los atributos HTML, pero en este caso puedes pasar cualquier valor de JavaScript a través de ellos, incluidos objetos, matrices, funciones e incluso JSX.

-> Las props no deben cambiar. Las variables de estado si pueden variar.


```
props ----> COMPONENT  ----> DOM
```

-> Las props solo se reciben del padre y son **read only**:

---

### ¿ Los componentes hijos se pueden pasar como props?

Dado a que los componentes hijos pueden ser elementos JSX, objetos o valores de JavaSCript, son válidos pasarlos como props. Hay escenarios donde te gustaría implementar **compoenntes genéricos**.

Los componentes genéricos son básicamente aquellos componentes que representan contenido intercambible y donde el padre no conoce a sus hijos.

React tiene una propiedad especial llamada **children** que permite pasar a sus hijos directemente al componente sin necesaidad de especificarlos individualemtne en las props.

---

## 5 COMPONENTE LAYOUT


### <img src="https://img.icons8.com/ios/40/000000/template.png"/>  ¿ A qué nos referimos con Layout ?

Es un **componente genérico que se utiliza para compartir una sección común entre varias páginas**.

-> El Header y Footer que se repite en todas las paginas.

- Generalmente este componente tendrá las secciones de encabezado y pie de pagina.

```
>src
   >compoents
      >layout
        >footer
           Footer.js
        >header
           Header.js
```

- Algunos ejemplos de layouts que puedes conseguir son:

-**Grid system** de **react-bootstrap**

-**Grid layout** de **Material UI**

---


### <img src="https://img.icons8.com/ios/40/000000/template.png"/> Implementación del Layout

---

### 6 - ESTILOS EN REACT

### <img src="https://img.icons8.com/office/40/000000/rgb-circle-2.png"/> Estilos con React

Los estilos en React los manejamos con **CSS**.

El CSS plano carece de ciertas funcionalidades que podrían hacer que el mantenimiento fuese más sencillo.

Por esta razón, axisten los llamados **preprocesadores** de CSS:

En React es posible usar varios tipos de preprocesadores como **Less**, **Sass**, **Stylus**, o **PostCSS**.

---

#### <img src="https://img.icons8.com/office/40/000000/rgb-circle-2.png"/> Principales librerías de estilo en React

Una librería de CSS es una serie de archivos que ya vienen preparadospara ser usados directamente, sin pensar en escribir siquiera una sola línea de código en CSS.

La principal ventaja es la rapidez con la que podemos construir nuestra aplicación, pensando particularmente en el código funcional, más no en el visual.

Algunas de las librerías más populares (incluyendo librerías de componentes) son:

- Bootstrap CSS, es muy usado en el mercado

- Tailwind CSS, es muy usado en el mercado.

- Styled Components

- Chakra

- MUI

-> **Bootstrap** se utiliza en el mercado laboral, **Bulma** también se usa la igual que **Style components**. Se ven en proyectos más viejos.

-> **Tailwind** y **Chakra** se usan en proyectos más nuevos.

---

-> **Libreria de componentes**, una librería es un codigo desarrollado por alguien más.

---

-> Atomizar bien los estilos.

---

-> Evitar de usar **!important**

---

-> [Para poder comparar tendencias en: https://npmtrends.com/](https://npmtrends.com/)

---
---

# :star: Clase 27/9 * Modulo 2 -  Unidad 4. Armado de la vista de Listado

## ESTADO DE LOS COMPONENTES, PROTECCIÓN DE UNA RUTA, OBTENCIÓN DE DATOS DE UNA API

### ¿ Cómo personalizar los Pop Ups de Sweet Alet 2 ?

1. Se usa el ```<Template>```

2. Se puede usar un **Theme** (tema), se instala y hay estilos similares a Bootstrap, Bulme, Materia-ui y otros estilos como minimalista, etc.

3. Usando una libreria extra, con **MySwal.fire(<Alert variant="warning" style=({font-size:30px}>)**

---
 
 ## Temas:
 
 ```
- 1 - Ejercicio de repaso
- 2 - Estados en los COmpoenntes de React
- 3 - Hooks
- 4 - Flujo de datos en React
- 5 - Ejemplo: flujo de Datos entre Hermanos (Lifting)
- 6 - Protección de una ruta
- 7 - Obtener datos de una API
 ```
 
 ---
 
 ## - 1 - Ejercicio de repaso
 
- Vemos el codigo y pensamos como refactorizar, hay un titulo, un avatar y una lista, se pueden armar 3 compoenntes: Title, Avatar, List y el estilo guardarlo aparte.
 
- Tiene estilo en linea, es mejor pasarlos por **className** 
 
---
 
 ## 2 - Estados en los Compoenntes de React

 
### Introducción a los estados
 
Hasta ahora hemos usado lo somponentes prácticamente como plantillas HTML, que podemospersonalizar con props.
 
 
### ¿ Qué es el estado ?
 
El estado son los datos que necesitamos para representar el comportamiento de un componente en un momento específico, es decir, son todos aquellos que varían de acuerdo a eventos que ocurren mientrs el componente se encuentra renderizado.
 
 Por ejemplo el email de entrada del Gmail...
 
 ... cuando un correo está marcado como favorito para mostrar la estrella completa o vacia
 
 ... al marcar algún correo con un check y muestre nuevas opciones
 
 ## ¿Qué colocar en el estado ?
 
 Como regla general deberíamos colocar en el estado del componente a todas aquellas características que van a ser modificadas en su parte visual, es decir, cosas que afectan la representación visual de la página.
 
 Ejemplos de alguna scosas que tiene sentido colocar en el estado:
 
 - entrada ingresada por el usuario (campos de formularios)
 
 - elemento actual o seleccionado (la pestaña actaul, la fila seleccionada)
 
 - datos del servidor (una lista de productos, el número de me gusta / favoritos)
 
 - estado abierto / cerrado ( modal abierto / cerado o barra lateral expandida/oculta)
 
 -> Con los hooks nos podemos comunicar entre el componente padre e hijo sin tener efectos secundarios.
 
---
 
 ## 3 - Hooks
 
 ### ¿ Qué son los hooks  ?
 
 Es una **función especial** que permite **modificar o añadir/enganchar características de React a un componente**.
 

 
 Por ejemplo, **useState** le permite agregar el estado a los componentes.
 
 Los hooks **no funcionan dentro de clases**, sólo en funciones (no se pueden usar en componentes de clase).
 
 ### ¿ Cuándo usar un hook ?
 
 Si tienens un componente (de función) y te das cuenta que necesitas agregarle algún estado o manejar efectos o eventos. Anteriormente, si querías hacer esto, tenías que convertir en función en una clase.
 
 ### Reglas especiales para los hooks
 
 La documentación oficial de React nos proporciona esta información.
 
 Nos dice que los hooks deben seguir dos reglas principales al usarlos:
 
 1. **Llamar a los Hooks en el niverl superiior de la función**: no se debn llamar a los hooks dentro de bucles, condicionales o funciones anidadas. En su lugar, siempre debemos usar hooks en el nivel superior de la función React para evitar cualquier retorno anticipado . Al seguir esta regla, te aseguras de que los hooks se llamen en el mismo orden cada vez que se represente un componente.
 
 2. **Solamente llamar a los hooks en componentes de función** es decir, puedes llamarlos desde los componentes y desde hooks creados por vos (custom). Haciendo esto garantizas que sea legible y visible la lógica de los estados del componente.
 
 ### El hook useState
 
 La llamada de este Hook declara una **variable de estado**. Esta es una forma de "preservar" algunos valores entre lasllamadas de la función.
 
 Normalmente, las variables "desaparecen" cuando sale de la función.
 
 -> **useState** es **asíncrono** cuando hacemos setVariable, por eso usamos los hooks que reaccionan al cambio de estado, como el **useEffect** que nota el cambio de estado y dispara el callback. Otro medo es dentro del **useState** tenemos una función que lo modifica, pero hay limitantes de que hacer.
 
 -> Se van a tener muchos useStates dentro de los componentes, y es un problema al leer el codigo, por eso se empiezan a usar otras cosas, como las librerias, y usar loading, setLoading (que se usa por ejemplo para el ruteo con el react-router-dom)

 ### El hook useEffect
 
 Este hook nos sirve para indicarle a React que el componente debe realizar alguna acción luego de renderizarse. Se le pasa como argumento una función **callback** que se ejecuta luego de actualizar el DOM.
 
 Como característica importante de este hook es que, por defecto, **se ejecuta después del primer renderizado y después de cada actualización**.
 
 Para evitar que se ejecute en cada actualización, se le puede pasar como argumento una lista de valores. Estos valores le permiten al useEffect que se ejecute sólo cuando cambien de estado esa lista de valores.
 
 Ejemplo de una llamada a una API utilizando fetch:
 
 -> es una llamada que retorna una promesa
 
 ```JSX
 useEffect(() => {
  fetch("https://pokeapi.co/api/v2/pokemon/${name}")
  .then(res => res.json())
  .then(pikachu => {
     setPokemonInfo(pikachu)
 }, [name])
 ```
 

 
 ---
 
 ## 4 - Flujo de datos en React
 
 Hay un **componente padre** que tiene uno o varios **componente hijos** y se va a comunicar con ellos medinte **props**.
 
 Cada uno de los **compoenntes hijos** tiene su propio **state**(estado).
 
 Para mandar información de padre a hijo, se pasa por props, y son datos de solo lecturas.
 
Para mandar información de hijos a padres, se usan los eventos, se pasan como propos, los hijos los invocan y los pasan a los padres.
 
 

 
---
 
 ## 5 - Ejemplo: flujo de Datos entre Hermanos (Lifting)
 
Como sabemos, cada componente en React tiene su propio estado. Debido a esto, a veces los datos pueden ser redundantes e inconsistentes. Entonces, al elevar el estado, hacemos que el estado del componente principal sea una fuente unica de verdad.
 
 
 
 ---
 
 ## Armado de Vista Listado
 
 ### La key
 
 Al crear componentes en React mediante algún bucle, serás advertido que una **key* debería ser proporcionada para ítems de lista. Una "key" es un **atributo** especial string que se debe incluir al crear una lista de elementos.
 
 Las keys ayudan a React a identificar qué ítems han cambiado, son agregados o son eliminados. Las keys deben ser dadas a los elementos dentro del array para darle a los elementos una identidad estable.
 
 ```JSX
 const listItem = numbers.map((number) => {
  <li key={number.toString()}>
     {number}
  </li>
 })
 ```
 
 - Evita usar indices para keys si el orden de los items puede cambiar.
 
 
 ---
 
 ##  6 - Protección de una ruta
 
 ---
 
 ##  7 - Obtener datos de una API
 
 ---
 ---




