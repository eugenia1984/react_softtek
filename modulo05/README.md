# :star2: Módulo 5. Modelando nuestra API final

---

## Unidad 13. Integrando los registros
```
- 13.1. Integración del registro
- 13.2. Obtener en el registro datos de la API
- 13.3. Registro de usuarios
- 13.4. Variables de entorno
- 13.5. Inicio de sesión
- 13.6. Creación de tareas
```

---

## Unidad 14. Creando estilos en la vista
```
- 14.1. Toast y Sweet Alert
- 14.2. Skeleton en listados
- 14.3. Filtrar listados
- 14.4. Búsquedas con debounce
- 14.5. Mostrar fecha y "Ver más"
```

---

## Unidad 15. Estructurando con Redux
```
- 15.1. Introducción a Redux
- 15.2. Reducers y Store
- 15.3. Actions y Reducers
- 15.4. Hooks de Redux
- 15.5. Eliminar con Redux
- 15.6. Actualizar en Redux
- 15.7. Consumiendo el estado desde varios componentes
```

---

## Unidad 16. Testeamos nuestro proyecto
```
- 16.1. Testing de renderizado
- 16.2. Mockear peticiones a la API
```

---
---

# :star2:Clase 11 Octubre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> MODULO 5:star2: 

---

## MODELANDO NUESTRA API FINAL

---

## :book: Temas:

```
- 1 - Presentación Módulo 5
- 2 - Registro y obtención de datos API
```

---

## :star: 1 - Presentación Módulo 5

### Modelando una API final

En este módulo nos vamos a enfocar en el diseño responsive, repasando conceptos antes mencionados y agregando testing al código.

### 01 - Principio Mobile First y diseño responsive

Vamos a continuar abordando estos temas y afianzando su importancia.

### 02 - Utilizar técnicas y herramientas para hacer un diseño responsive

Vamos a ver técnicas y herramientas que se pueden usar para lograr el diseño. 

### 03 - Testing

Vamos a ver una introducción a la parte de cómo probar el código e implementarlo en nuestro proyecto.


---

## Unidad 13. Integrando los registros

---

## :star:  2 - Registro y obtención de datos API

## <img src="https://img.icons8.com/external-phatplus-lineal-color-phatplus/40/000000/external-molecular-biochemistry-phatplus-lineal-color-phatplus.png"/> Organización de los modulos

En proyectos serios, mantenidos por un equipo es necesario establecer cierto orden para que todos sepan en que “cajon” encontrar un componente dado.

Esta categorización y organización de las partes de un sistemas también se la llama Arquitectura del sistema y sirve para definir los elementos y las relaciones entre elementos que conforman un sistema.

#### Va a variar según el proyecto

Lo importante es seguir las convenciones establecidas por el equipo, evitar ambigüedades que entorpezcan el mantenimiento del proyecto.

```
atomo - molecula - organismo - templates - pages
```

#### Basicas

```
-components
  -veiws/pages
  -layouts
  -common
    -component
      -styles.css
      -Component.jsx
      -index.js
-hooks
-contexts
-services
```

#### Plana o Profunda

Algunos proyectos simplemente agrupan funciones y clases por capas. Otros organizan el proyecto en módulos, donde un módulo puede contener sub-módulos, siguiendo el criterio de cohesión.

#### No repetir codigo, ni reutilizar por la fuerza

Cada módulo debería tener una única razón para cambiar.

---

## Postman

Es una plataforma para el desarrollo de API, más conocida por la herramienta para documentar y correr peticiones contra un API.

---

## HTTPIE

Otra herramienta muy popular para hacer http request desde la terminal

---

### CURL

Del ‘98, permite hacer todo tipo de transferencias entre servicios, en particular HTTP

---

## <img src="https://img.icons8.com/color/48/000000/json--v1.png"/> JSON Server

Ideal para desarrollar prototipos o pruebas de concepto, permite hacer request a una API REST, guardando las modificaciones en un archivo.

### <img src="https://img.icons8.com/color/48/000000/json--v1.png"/> JSON Server Auth

Extiende json con login y register


---
---


# :star2:Clase 12 Octubre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> MODULO 5:star2: 

---

### UNIDAD 13. INTEGRANDO LOS REGISTROS

----

## :book: Temas:

```
- 1 - Registro de usuarios
- 2 - Variables de entorno
- 3 - Inicio de sesión
- 4 - Creación de tareas
```

---

## :star:  1 - Registro de usuarios

###  <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/40/000000/external-unique-visitor-big-data-flaticons-lineal-color-flat-icons-2.png"/> UUID

**Universal Unique Identifier**, o **Global Unique Identifier**, es un número de 128 que se puede generar de forma distribuida sin utilizar una secuencia.

Permite a distintas partes de un sistema generar **claves únicas (con baja probabilidad de colisión)**.

- Web [https://www.uuidgenerator.net](https://www.uuidgenerator.net)
---


### Instalacion

Para crear un UUID random

1. Lo instalamos con: ```npm install wwid```

2. Creamos un UUID (sintaxis de ES6)

```JSX
import { v4 as uuid4 } from "uuid";

uuid4(); // bc3afbb1-0a05-4da7-8062-343877dd6577
```

O usamos la sintaxis de JavaScript anterior:
```JSX
const{ v4: uuidv4} = required('uuid');
uuidv4(); // bc3afbb1-0a05-4da7-8062-343877ad6872
```

---

### MUI 

### <img src="https://img.icons8.com/external-basicons-solid-edtgraphics/40/000000/external-component-ui-components-basicons-solid-edtgraphics-3.png"/> ¿Que es?

Librería de componentes de react basada en los principios de “material design”.

Material Design es un lenguaje visual de diseño creado por google en 2014. 


### <img src="https://img.icons8.com/external-basicons-solid-edtgraphics/40/000000/external-component-ui-components-basicons-solid-edtgraphics-3.png"/> Web

[https://miu.com/](https://miu.com/)

[https://material.io](https://material.io)

###  <img src="https://img.icons8.com/external-basicons-solid-edtgraphics/40/000000/external-component-ui-components-basicons-solid-edtgraphics-3.png"/> Instalacion

Para instalarla y verla en la lista de dependencias del package.json:

Con **npm**
``` npm install @mui/material @emotion/react @emotion/styled```

Con **yarn**
``` yarn add @mui/material @emotion/react @emotion/styled```

---

### MUI Switch & Formik 

### <img src="https://img.icons8.com/external-basicons-solid-edtgraphics/40/000000/external-component-ui-components-basicons-solid-edtgraphics-3.png"/>  Switch

El switch es un componente de material que cambia de valor cuando se hace click.

Formik no tiene handle que maneje el toggle, pero nos da funcionalidad que permite implementarlo.

```JSX
import {Switch, FormControlLabel } from "@mui/material"

<FormControlLabel
  control={
    <Switch
      value={values.switch}
      onChange={() =>
        formik.setFieldValue("switch", !formik.values.switch)
      }
      name="switch"
      color="secondary"
    />
  }
/>
```

El componente Switch por defecto no tiene label, pero combinándolo con FormControlLabel se puede agregar el label.

---

## useNavigate y useParams

### <img src="https://img.icons8.com/external-justicon-lineal-color-justicon/40/000000/external-hook-pirates-justicon-lineal-color-justicon.png"/> ¿ Que nos permiten ?

Estos hooks en combinación permiten pasar parámetros entre rutas de react-router-dom.

```JSX
.then(data => navigate("/registered/")
data?.result?.user?.teamID, {replace:true})
```


```JSX
<Route
  path="/registered/:teamID"
  element={
    <motion.div
      className="page"
      initial="out"
      exit="out"
      variants={pageTRansition}
    >
     <Registered />
    </motion.div>
  }
/>
```

```JSX
import {useParams} from "react-router-dom"
export default function Registered() {
  const {teamID} = useParams()
  return (
    <div className="container">
      El team ID de tu equipo es: {teamID}
    </div>
  )
}
```


---


## :star: 2 - Variables de entorno

### <img src="https://img.icons8.com/material-two-tone/40/000000/variable.png"/> Definicion

Son variables que residen en el ambiente de ejecución del servidor, ya sea en desarrollo o
producción.

Permite parametrizar la aplicación para que utilizar configuración del ambiente.

Por ej: en el ambiente desarrollo configuramos un api endpoint apuntando a un mock, pero en
producción se configurar apuntando a la api productiva.


### <img src="https://img.icons8.com/material-two-tone/40/000000/variable.png"/> Archivo.env

En los proyectos react se pueden configurar variables de ambiente, mediante un archivo “.env”

React solo hará visibles en la aplicación las variables que empiecen con el prefijo “REACT_APP_”

```
REACT_APP_API_URL=https://keelfj.sse.codesandbox.io/register
REACT_APP_COLOR=blue
NO_SE_VA_A_VER=red
```


```JSX
import "./styles.ss"

const API_URL = process.env.REACT_APP_API_URL;
const COLOR = process.env.REACT_APP_COLOR;

export default function App() {
  return(
    <div className="App"> 
      <div>API_URL: {API_URL} </div>
      <div>COLOR: {COLOR}</div>
    </div>
  )
}
```

---

### Ejercicio 1

#### Registro

Cuando un usuario se registra, puede crear un equipo nuevo, o registrarse bajo un equipo existente. Los equipos son identificados por un uuid. Si el usuario pertenece a un equipo entonces ingresará el uuid correspondiente, en caso contrario no será requerido ingresar un uuid sino que se creará uno al realizar la petición.

1 - Agregar al registro un switch que renderice condicionalmente el input correspondiente para pedir el uuid del equipo. Si el switch está activo el uuid debe validarse como requerido.

2 - Al hacer submit del registro, si el usuario seleccionó que no pertenece a un equipo se debe generar un nuevo uuid independientemente de los que haya cargado en el campo.

3 - Hacer el registro contra el json-server disponible en el sanbox 
[https://codesandbox.io/s/siglo21-softek-backend-kellfj](https://codesandbox.io/s/siglo21-softek-backend-kellfj) endpoint [https://kellfj.sse.codesandbox.io/register](https://kellfj.sse.codesandbox.io/register).

Si el registro es exitoso navegar con el router hacia “/home/{teamId}”.

Bonus: Usar el setFieldValue de formik para que cuando se seleccione continente distinto de america el valor de región sea ”otro”.

---


## :star:  3 - Inicio de sesión

### <img src="https://img.icons8.com/external-fauzidea-gradient-fauzidea/40/000000/external-login-online-learning-fauzidea-gradient-fauzidea.png"/> Login

Usando el sanbox, mediante postman podemos ver que si se ingresan las email y password, el
mismo devuelve, un accessToken.

Dicho token se suele guardar en el localStorage para indicar que el usuario está logoneado.


Si el sistema está protegido por autenticación, el token deberá enviarse como header Authorization en las peticiones a los recursos protegidos.

### Axios defaults

Al utilizar tokens de Authorization para acceder a endpoints, axios nos permite definirlos como defaults, de forma que se envían automáticamente en las peticiones.

```JSX
axios.defaults.baseURL="https://api.example.com";
axios.defaults.headers.common["Authorization"] = AUTH_TOKEN;
axios.defaults.headers.post["Content-Type"] = "application/x-www-form-urlencoded";
```

En el caso del server mock, los recursos protegidos esperan el token de la siguiente manera.

```Authorization: Bearer <token>```

---

## Ejercicio 2 :Login

Cuando un usuario ingresa sus credenciales, email y password, el backend devuelve un accessToken, que deber ser reenviado en cada petición a recursos protegidos.

1 - Actualizar el Login, para obtener el accessToken del backend y lo guarden en localStorage, y lo agregue como default header a axios.

2 - Cuando el login se realiza con éxito navegar a la home (lista de tareas) 

---



## :star:  4 - Creación de tareas

### Ejercicio 3: Creación de tareas

1 - Crear un componente que permita hacer el alta de una tarea.

Una tarea posee los siguiente atributos:

-task: nombre de la tarea,
 
-createdAt : la fecha de creación es el instante en el que se crea la tarea

-author: autor de la tarea, deber ser usuario logoneado
 
-type: tipo de tarea puede tomar 3 valores, nuevo, en proceso y finalizada,
 
-priority: la prioridad de la tarea puede tomar 3 valores, alta, normal, baja
 
-description: la descripción de la tarea, es un texto largo que describe la tarea.

El alta de la tarea se hace con un post de los datos al servicio:

[https://kellfj.sse.codesandbox.io/tasks](https://kellfj.sse.codesandbox.io/tasks) , se de enviar el Authorization header correspondiente al usuario logoneado.
---
---
