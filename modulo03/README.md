# :star2: Módulo 3. Buscador y sección favoritos

---

## :star: Unidad 6. Creando secciones

```
- 6.1. Armado componente buscador
- 6.2. Validación formulario buscador
- 6.3. Redirección a resultados
- 6.4. Llamado a la API con palabra clave
- 6.5. Armado lógica de "Favoritos"
- 6.6. Armado componente "Favoritos" 
- 6.7. Finalizando la sección "Favoritos"
```

---

## :star: Unidad 7. Introducción a Redux

```
- 7.1 Entendiendo la problemática en el desarrollo de aplicaciones
- 7.2 Introducción y conceptos clave para manipular Redux
```

---

# :star2:Clase 30 Septiembre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> MODULO 3 * UNIDAD 6:star2: 

---

## ARMADO COMPONENTE BUSCADOR, VALIDACIONES, REDIRECCION A LOS RESULTADOS Y LOGICA DE FAVORITOS

---

### Temas:

```
- Presentación del Modulo 3
- Ejercicio de repaso
- Barra de busqueda
- Armado y validacion del componente Buscador
- Armado de la seccion de Favoritos
```

---

### MODULO 3 : BUSCADOR Y SECCION DE FAVORITOS

En este modulo vamos a seguir construyendo componentes y añadiendo nuevas funcionalidades a la aplicacion de la lista de peliculas.

#### 01 - Implementación de un buscador

Vamos a construir un componente para realizar busquedas de peliculas por palabra clave con sus validaciones y mostrando sus resultados.


#### 02 - Sección de Favoritos

Vamos a crear una seccion de favoritos y todo lo relacionado a su logica


#### 03 - Hola Redux

Vamos a conocer la libreria, hablar sobre el patron de diseño que implementa, sus ventajas y desventajas y cuando conviene usarlo.

---

## 01 - Implementación de un buscador

### <img src="https://img.icons8.com/external-others-zufarizal-robiyanto/40/000000/external-lup-mutualiz-ui-essential-others-zufarizal-robiyanto.png"/> Barra de busqueda

**Estructura basica**

Uan barra de busqueda es un elemento en la intefaz de usuario que te permite encontrar informacion en la web o dentro de una aplicacion web.

Generalmente lo encontramos en el Header cuando queremos que esté presente y accesible siempre para el usuario de nuestra aplicación.

Está compuesto por:

- Un **formulario** que posee un **input** para tomar un texto.

- Un **boton** que se encarga de procesar la busqueda.

---

## <img src="https://img.icons8.com/color/40/000000/search--v1.png"/> Armado y validacion del componente BUSCADOR

---

## ARMADO Y VALIDACION DEL COMPONENTE BUSCADOR 

---

## ARMADO DE LA SECCION DE FAVORITOS 

---

## RENDIMIENTO API REQUEST INNECESARIAS

### Rendimiento en API

Deboucing:
```JavaScript
let timer;

const debounce = (e) => {
  if(timer) clearTimeout(timer);
  timer = setTimeout(() => {
    handleChange.target.value)
  }, 500);
;

const handleChange= (e) => {
  const url = "https//www.thecoktaildb.com/api/json/v1/search.php?s=${e}";
  fetch(url)
    .then((res)=> res.json())
    .then((json) => {
      return setDrinkList(json.drinks)});
   };
```

### Rendimiento en AP

Notar que ya estamos teniendo que incorporar lógica algo compleja para prevenir las request innecesarias.

```JavaScript
function throttle(cb, delay = 250) {
  let shouldWait = false;
  
  return ( ...args) => {
    if(shouldWait) retutn
    
    cb(...args)
    shouldWait = true
    setTimeout(()=> {
      shouldWait = false
    }, delay)
  }
}
```


---
---

# :star2:Clase 03 Octubre <img src="https://img.icons8.com/clouds/40/000000/react.png"/> MODULO 3 * UNIDAD 6:star2: 

---

## Temas:
```
- 1 - Retoques finales a la seccion de Favoritos
- 2 - Verificación que el flujo de la applicacion funciona correctamente
- 3 - Ejercicio de repaso
- 4 - Introducciona  Redux
```

---

## :sart: 1 - Finalización de la seccion de Favoritos

 <img src="https://img.icons8.com/ios/50/000000/likes-folder.png"/> Favoritos.js:
 
 ```JSX
 mport React from "react";
import { Link, Navigate } from "react-router-dom";

const Favoritos = ({ favorites, addOrRemoveFromFavs }) => {
  let token = sessionStorage.getItem("token");

  return (
    <>
      {!token && <Navigate replace to="/" />}
      <h2 className="text-white">Favoritos</h2>
      <div className="row my-2 mx-2">
        {favorites.length === 0 && (
          <div className="col-12 text-danger text-center">
            No Hay Nada en Favoritos
          </div>
        )}
        {favorites.map((oneMovie, index) => {
          return (
            <div className="col-3" key={index}>
              <div className="card my-2">
                <img
                  src={oneMovie.imgURL}
                  style={{ height: "300px" }}
                  className="card-img-top"
                  alt="..."
                />
                <button
                  className="favorito"
                  onClick={addOrRemoveFromFavs}
                  data-movie-id={oneMovie.id}
                >
                  🖤
                </button>
                <div
                  className="card-body text-center"
                  style={{ height: "220px" }}
                >
                  <h5 className="card-title">
                    {oneMovie.title.substring(0, 30)}
                  </h5>
                  <p className="card-text">
                    {oneMovie.overview.substring(0, 100)}...
                  </p>
                  <Link
                    to={`/pelicula/${oneMovie.id}`}
                    className="btn btn-dark "
                  >
                    View details
                  </Link>
                </div>
              </div>
            </div>
          );
        })}
      </div>
    </>
  );
};

export default Favoritos;
```

-> Armamos un boton de favoritos, que es un boton con el corazon, que al hacerle el click nos lo va a guardar en al sección de favoritos.

-> Recibe de **props**: **favorites** y **addOrRemoveFromFavs**

-> Es una estructura similar a las cards, pero ademas tiene el **boton** con el **corazon** con el **handle** para el **onClick**.

-> Este boton con el corazon lo vamos a mostrar en la seccion de **favoritos** y tambien en la parte de **listado**. Para compartir información entre componenetes **el estado lo maneja el Padre más cercano**, es decir en **App**.

-> Como entre **Favorito** y **listado** vamos a compartir pasamos como props la informacion con **addOrRemoveFromFavs** asi utilizan el **boton** para enviar el evento y remover el item de favorito, hacemos el **lifting** y lo movemos a App:

```JSX
<Route
    path="/listado"
    element={<Listado addOrRemoveFromFavs={addOrRemoveFromFavs} />}
  />
  <Route path="/pelicula/:id" element={<Detalle />} />
  <Route
    path="/resultados"
    element={<Resultados addOrRemoveFromFavs={addOrRemoveFromFavs} />}
  />
  <Route
    path="/favoritos"
    element={
      <Favoritos
        favorites={favoritos}
        addOrRemoveFromFavs={addOrRemoveFromFavs}
      />
    }
  />
</Routes>
```

-> Tenemos que manejar una **lista de favoriots** además de la lista de las movies que se obtiene de la API, esta lista de favoritos la manejamos como un estado y utilizamos el **localStorage**, usamos un useState para la primer renderizacion y vemos si en localStorage tengo algo guardado que sea **fav**, los vaforitos, si hay se guarda en la variable de estado.

A veces con una misma funcion se maneja tanto el **add** como el **Remove**, loq eu no es recomendable, si luego se complejiza, es mejor tener separadas las funcionalidades, pero en el video esta todo junto. Al hacer click al boton obtenemos lo que tenemos del listado en el localStorage, si no tenemos nada inicializamos una variable secundaria (temporal) para el manejo de quitar elementos y agregar elementos en la lista. A nosotros nos interesa que las listas sean inmutables, pero JS tiene arrays mutables (su valor en memoria y sus indices cambian) por eso es importante trabajar con variables temporales/de soporte.

Inicializamos la lista vacioa si no hay nada en el localStorage, sino le hacemos un **JSON.parse**:

```JSX
const [favoritos, setFavoritos] = useState([]);

  useEffect(() => {
    const favInLocal = localStorage.getItem("favs");

    if (!!favInLocal) {
      const favsArrays = JSON.parse(favInLocal);
      setFavoritos(favsArrays);
    }
  }, []);
```

Tengo una lista de diciconario.

Ahora para obtener la informacion del evento a añadir o remover utilizo:

```JSX
//Obtengo información del elemento
const btn = e.currentTarget;
const parent = btn.parentElement;
const imgURL = parent.querySelector("img").getAttribute("src");
const title = parent.querySelector("h5").innerText;
const overview = parent.querySelector("p").innerText;
const movieData = {
  imgURL,
  title,
  overview,
  id: parseInt(btn.dataset.movieId)
};
```

Co la funcion **find** veo si en mi lista de favoritos tego esta pelicula a agregar o eliminar, si no esta lo paso de objeto JSOn a un objeto String para guardar en la varaible de favs que tengo en el localStorage.

```JSX
let movieIsInArray = tempMoviesInFavs.find((oneMovie) => {
  return oneMovie.id === movieData.id;
});
```

Tambien lo seteamos y loc ambiamos en la variable de estado, y le lanzamos el aviso de que esta todo ok y se agrego la peli a favoritos.

Si quiero eliminar, busco que este en el array y con un filter me guardo el resto de las pelis, menos la que quiero eliminar, y aviso que ya quedo eliminada.

```JSX
 if (!movieIsInArray) {
    localStorage.setItem(
      "favs",
      JSON.stringify([...tempMoviesInFavs, movieData])
    );
    setFavoritos([...tempMoviesInFavs, movieData]);
    swal.fire("Bien", "Se agrego la pelicula a favoritos", "success");
  } else {
    let moviesLeft = tempMoviesInFavs.filter((oneMovie) => {
      return oneMovie.id !== movieData.id;
    });
    localStorage.setItem("favs", JSON.stringify(moviesLeft));
    setFavoritos(moviesLeft);
    swal.fire("Bien", "Se elimino la pelicula de favoritos", "success");
  }
};
```

Estos **favoritos** lo voy a compartir en el Listado y en Favoritos, tambien lo puedo incluir en el Layout, se lo podria pasar en el **Header**.


Entonces, me queda **App.js**:
```JSX
import { useState, useEffect } from "react";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import swal from "sweetalert2";

import Login from "../Login/Login";
import Listado from "../Listado/Listado";
import Detalle from "../Listado/Detalle";
import Resultados from "../Resultados/Resultados";
import Favoritos from "../Favoritos/Favoritos";
import Header from "../Header/Header";
import Footer from "../Footer/Footer";

import "./App.css";

function App() {
  const [favoritos, setFavoritos] = useState([]);

  useEffect(() => {
    const favInLocal = localStorage.getItem("favs");

    if (!!favInLocal) {
      const favsArrays = JSON.parse(favInLocal);
      setFavoritos(favsArrays);
    }
  }, []);

  const addOrRemoveFromFavs = (e) => {
    const favMovie = localStorage.getItem("favs");

    let tempMoviesInFavs = [];

    if (favMovie.length) {
      tempMoviesInFavs = JSON.parse(favMovie);
    }

    //Obtengo información del elemento
    const btn = e.currentTarget;
    const parent = btn.parentElement;
    const imgURL = parent.querySelector("img").getAttribute("src");
    const title = parent.querySelector("h5").innerText;
    const overview = parent.querySelector("p").innerText;
    const movieData = {
      imgURL,
      title,
      overview,
      id: parseInt(btn.dataset.movieId)
    };

    let movieIsInArray = tempMoviesInFavs.find((oneMovie) => {
      return oneMovie.id === movieData.id;
    });

    if (!movieIsInArray) {
      localStorage.setItem(
        "favs",
        JSON.stringify([...tempMoviesInFavs, movieData])
      );
      setFavoritos([...tempMoviesInFavs, movieData]);
      swal.fire("Bien", "Se agrego la pelicula a favoritos", "success");
    } else {
      let moviesLeft = tempMoviesInFavs.filter((oneMovie) => {
        return oneMovie.id !== movieData.id;
      });
      localStorage.setItem("favs", JSON.stringify(moviesLeft));
      setFavoritos(moviesLeft);
      swal.fire("Bien", "Se elimino la pelicula de favoritos", "success");
    }
  };

  return (
    <BrowserRouter>
      <div className="app">
        <div className="principal">
          <Header favorites={favoritos} />
          <Routes>
            <Route exact path="/" element={<Login />} />
            <Route
              path="/listado"
              element={<Listado addOrRemoveFromFavs={addOrRemoveFromFavs} />}
            />
            <Route path="/pelicula/:id" element={<Detalle />} />
            <Route
              path="/resultados"
              element={<Resultados addOrRemoveFromFavs={addOrRemoveFromFavs} />}
            />
            <Route
              path="/favoritos"
              element={
                <Favoritos
                  favorites={favoritos}
                  addOrRemoveFromFavs={addOrRemoveFromFavs}
                />
              }
            />
          </Routes>
          <Footer />
        </div>
      </div>
    </BrowserRouter>
  );
}

export default App;
```

---

### :star: 3 - Ejercicio de repaso

#### <img src="https://img.icons8.com/office/40/000000/pushups.png"/> Implementar el handleAdd y el handleRemove para esta lista de supermercado

- Lo podes ver en [https://codesandbox.io/s/add-remove-exercise-supermarket-list-forked-uehhti](https://codesandbox.io/s/add-remove-exercise-supermarket-list-forked-uehhti)

---

## :star: 4 -  Introducción a Redux ( Unidad 7)

```
- 7.1 Entendiendo la problemática en el desarrollo de aplicaciones
- 7.2 Introducción y conceptos clave para manipular Redux
```

### <img src="https://img.icons8.com/ios/40/000000/redux.png"/> Cómo hace un componente para...


... informar un cambio de estado a un hermano o ancestro?

... acceder el dato de un ancestro?

- Si sólo usamos props, podemos comunicarnos desde el componente que está más afuera hacia el que está más adentro, es decir dle padre hacia el hijo. -> La **comunicación** es **top-down**

- Ponemos todo lo del estado en el componente de más arriba y lo hacemos pasar hasta llegar al componente de abajo.

```         {firstName:"M E", lastName: "C"}
      -----
      |   |
      -----
      |
      v
    ----
    |   |
    ----
     |
     v
   -----
   |   |
   -----
   firstName
```

El componente de más abajo necesitaría recibir un **handler** para poder informarle al padre de ese cambio de estado y el Padre puede volver a hacer el cascadeo.

<img src="https://img.icons8.com/ios/40/000000/redux.png"/> **Props Drilling** (esto es malo)

- Informar un cambio de estado a un hermano o un ancestro ? Necesita recibir un **callback** por **props**

- Acceder al dato de un ancestro? Necesita recibir el **dato** por **props**

Drop drilling -> se hace lifting, se esta taladrando hacia abajo desde el root. A veces es suficiente, pero... no es bueno. El problema es que si luego nececito algo mas en el componente hijo o nieto, tengo que ir modificando todos los componentes intermedios para que llegue esta nueva prop.

-> <img src="https://img.icons8.com/ios/40/000000/redux.png"/> La problemática es ...


... complejidad de comunicar componentes a traves del arbol

...muchos componentes, varios niveles de anidación

... prop drilling no escala en desarrollo


-> como solución a esta problemática surge **Redux**

---


## :star: Redux


## <img src="https://img.icons8.com/ios/40/000000/redux.png"/> Conceptos de Redux


#####  Una sola fuente de verdad

Todo el estado de la aplicación está centralizado en un único lugar.


##### Cambios de estado mediante funciones puras

Los componentes no pueden aplicar las acciones, sino que se configuran funciones puras encargadas de interpretar la acción y avanzar el estado.


#####  Estado de solo lectura

Los componentes pueden leer el estado de forma directa, pero para modificarlo deben disparar una acción indicando la modificación a realizar.


-> Redux nacio de otro lenguaje de programacion para front end, End. Lo que propone es tener todo el estado cetnralizado en un punto (inmutabilidad).

-> Los componentes van a disparar funciones

-> Se va a actualizar el estado

###  <img src="https://img.icons8.com/ios/40/000000/redux.png"/>Estado central

- Evita el prop drilling (es como si lo tuviera por fuera de la aplicación, no tengo que pasarlo por componentes intermedios)

- solo se subscribe componentes que los necesitan (no intervienen los componentes intermedios)

- solo participan en modificaciones componentes que lo necesitan (no recibe el callback por prop, sino que tiene un mecanismo para comunicarse con el estado central)


### <img src="https://img.icons8.com/ios/40/000000/redux.png"/> ¿ Cómo se nombra en Redux?

- **selectors** para leer datos del estado cada vez que cambia

- **dispatch** para provocar cambios de estado

- **reducers** define como la accion actualiza el estado: logica independiente de vista, testeo sencillo.


-> Se usa **useSelect** que es un hook que nos permite pasarle una función para seleccionar  fragmentos que nos interesen del Estado. Para realizar una modificación sobre el estado vamos a usar **useDispatch** y **deipatch** que nos permite pasarle una definición de la acción a realizar sobre el estado cental. Esa acción se la va a pasar al reducer junto con el valor anterior del estado y se va a generar un nuevo estado que se va a actualizar en todos los componentes que están leyendo de ese estado.

A esta combinación del estado centralizado y la funciones de reduccion se las conoce como **STORE**

```
----         reducer
|  | <------ function <-----------
----                             |
 |                               | 
 |             -----             |
 |             |   |             |
 |             -----             |
 |             |    |            |
 |             v    v            |
 |           ---    ---          |
 |           |  |   |   |        |
 |           ---    ----         |
 | useSelect()      dispatch()   |
   leer estado     modificar estado
```

-> **useSelec** es un hook que nos permite pasarle una funcion para seleccionar fragmentos que nos interese del estado

-> para hacer una modificacion sobre el estado usamos **useDispatch** y **dispatch** que nos permite pasarle una  definicion de la accion a realizar sobre el estado central. Esa accion se la va a pasar al reducer junto con el valor anterior del etado y se va a generar un nuevo estado que se va a renderizar en todos los componentes que estan leyendo de ese estado.


La combinación del **Estado centralizado** y las **funciones de reduccion** se la conoce como**STORE**


---

###  <img src="https://img.icons8.com/ios/40/000000/redux.png"/> Ciclo de cambio de estado

1. Los componentes despachan acciones que modifican el estado central.

```JavaScript
const dispatch = useDispatch()
dispatch(action)
```

2. Los reducers actualizan el estado central a partir de las acciones:

```JavaScript
nuevoEstado = previoEstado + accion
```

3. Los componentes utilizan selectores para leer la informacion que les interesa del estado central:
```JavaScript
const dato = useSelect(selector)
```

El modelo que propone Redux es:


```    actions
      /      \
    /         \
  view <----- state
```

#### Otro modo de verlo


```
                               (previousState, action)
ACTION ----dispatch----> STORE -----------------------> REDUCERS
  |          (action)      |    <----------------------
  |                        |          (newState)
  |                        |
  |                 (state)|
  |                        v
  ---------------------- VIEW
```

Del STORE lleo el ESTADO en una VISTA, mediante ACCIONES DE UN USUARIO (generalmente los cambios se diparan cuando el usuario hace click, ingresa algo en un input, marca un checkbox, hace algo). Entonces desde el HANDLER se lanza una ACCION, esta accion llega al STORE y el store utilizando el REDUCER aplica la accion y general UN NUEVO ESTADO que se pasa a las vistas y se actualiza.

---

### Ejemplo sencillo de codigo

[se puede ver aca]([https://codesandbox.io/p/github/paulocesarcuneo/redux-simple-example/csb-dvpob8/draft/autumn-violet?file=%2Fsrc%2Fcomponents%2FFooter.js&workspace=%257B%2522activeFileId%2522%253A%2522cl8s5g4ms000flshp49rw1wko%2522%252C%2522openFiles%2522%253A%255B%2522%252FREADME.md%2522%255D%252C%2522sidebarPanel%2522%253A%2522EXPLORER%2522%252C%2522gitSidebarPanel%2522%253A%2522COMMIT%2522%252C%2522sidekickItems%2522%253A%255B%257B%2522type%2522%253A%2522PREVIEW%2522%252C%2522taskId%2522%253A%2522start%2522%252C%2522port%2522%253A3000%252C%2522key%2522%253A%2522cl8s5gtt8000k2v6gd17luwg5%2522%252C%2522isMinimized%2522%253Afalse%257D%255D%257D](https://codesandbox.io/p/github/paulocesarcuneo/redux-simple-example/csb-dvpob8/draft/autumn-violet?file=%2Fsrc%2Fcomponents%2FFooter.js))

```
>public
>src
  app
      actions.js
      reducers.js
      store.js
  components
      Footer.js
      Header.js
      TodoList.js
  App.js
  bootstrap.css
  index.js
```

**App.js**:
```JSX
import React from "react";
import { Footer } from "./components/Footer";
import { Header } from "./components/Header";
import { TodoList } from "./components/TodoList";
import "./bootstrap.css";

function App() {
  return (
    <div
      className="container d-flex gap-2 flex-column justify-content-center"
      style={{width: 600}}
    >
      <Header />
      <TodoList />
      <Footer />
    </div>
  );
}

export default App;
```

**Footer.js**:
```JSX
import { useState } from "react";
import { useDispatch } from "react-redux";
import { addTask } from "../app/actions";

export const Footer = () => {
  const [text, setText] = useState("");
  const dispatch = useDispatch();

  const handleAddTask = () => {
    dispatch(addTask(text));
    setText("");
  };

  const handleChangeText = (e) => {
    setText(e.target.value);
  };

  const handleKeyDown = (e) => {
    if (e.code === "Enter") {
      handleAddTask();
    }
  };

  return (
    <div className="input-group w-100 my-4">
      <label className="input-group-text">Agregar</label>
      <input
        className="form-control"
        type="text"
        value={text}
        placeholder="Nueva Tarea"
        onKeyDown={handleKeyDown}
        onChange={handleChangeText}
      />
      <button className="btn btn-primary" onClick={handleAddTask}>
        +
      </button>
    </div>
  );
};

```

**Header.js**:
```JSX
import { useSelector } from "react-redux";
import { todosSelector } from "../app/selectors";

export const Header = () => {
  const todos = useSelector(todosSelector);
  const selectedCount = todos.filter((todo) => todo.selected).length;

  return (
    <div className="d-flex flex-row align-items-center border px-3 mt-4">
      <input type="checkbox" className="form-check-input flex-shrink-0"></input>
      <span className="p-4 fs-5 fw-bold">
        {selectedCount ? `${selectedCount} Seleccionados` : "Tareas"}
      </span>
      {selectedCount ? (
        <button
          className="btn btn-danger m-4"
          onClick={() => console.log(`borrar seleccionados`)}
        >
          BORRAR
        </button>
      ) : null}
    </div>
  );
};
```

**TodoList.js**:
```JSX
import { useSelector, useDispatch } from "react-redux";
import { toggleSelection } from "../app/actions";
import { todosSelector } from "../app/selectors";

export const TodoList = () => {
  const todos = useSelector(todosSelector);
  const dispatch = useDispatch();

  const handleToggleSelection = (index) => () => {
    dispatch(toggleSelection(index));
  };

  return (
    <div className="list-group mx-0 w-auto">
      {todos.map(({ text, selected }, i) => (
        <label
          className="list-group-item d-flex gap-2 align-items-center justify-content-between"
          key={`row-${i}`}
        >
          <input
            type="checkbox"
            className="form-check-input flex-shrink-0"
            value={selected}
            onChange={handleToggleSelection(i)}
          />
          <span className="d-block">{text}</span>
          <button
            className="btn btn-close"
            onClick={() => console.log(`remove el item ${i}`)}
          ></button>
        </label>
      ))}
    </div>
  );
};
```

-> En **app**:

**actons.js**:
```JSX
export const ADD_TODO = "todo/add";
export const TOGGLE_SELECTION = "todo/toggle-selection";
export const TOGGLE_SELECT_ALL = "todo/toggle-select-all";
export const DELETE_ALL_SELECTED = "todo/delete-all-selected";
export const DELETE = "todo/delete";

export const addTask = (text) => {
  return { type: ADD_TODO, text };
};

export const toggleSelection = (index) => {
  return { type: TOGGLE_SELECTION, index };
};
```

**reducers.js**:
```JSX
import {
  ADD_TODO,
  DELETE,
  DELETE_ALL_SELECTED,
  TOGGLE_SELECTION,
  TOGGLE_SELECT_ALL,
} from "./actions";

const removeNth = (arr, n) => {
  return [...arr.slice(0, n), ...arr.slice(n + 1)];
};

export const todosReducer = (state, action) => {
  switch (action.type) {
    case ADD_TODO: {
      const { todos } = state;
      const { text } = action;
      return { ...state, todos: [...todos, { text }] };
    }
    case TOGGLE_SELECTION: {
      const { index } = action;
      const { todos } = state;
      const updatedTodos = todos.map((item, i) => {
        if (i === index) {
          return { ...item, selected: !Boolean(item.selected) };
        }
        return item;
      });
      return { ...state, todos: updatedTodos };
    }
    case TOGGLE_SELECT_ALL: {
      throw new Error("Not implemented");
    }
    case DELETE_ALL_SELECTED: {
      throw new Error("Not implemented");
    }
    case DELETE: {
      throw new Error("Not implemented");
    }
    default:
      return state;
  }
};

export const initialState = {
  todos: [{ text: "Aprender Redux", selected: false }],
};

```

**selectors.js**:
```JSX
export const todosSelector = (state) => state.todos;
```

**store.js**:
```JSX
import { configureStore } from "@reduxjs/toolkit";

import { todosReducer, initialState } from "./reducers";

export const store = configureStore({
  reducer: todosReducer,
  preloadedState: initialState,
});
```

-> https://recordings.rna1.blindsidenetworks.com/ilumnotech/9245ae6957e39f5d8f43aa41bec37fa03f820e1b-1664805529357/capture/ 24mins

---
---

- [**TEORIA Y VIDEOS**](https://github.com/eugenia1984/react_softtek/blob/main/modulo03/modulo3_teoria.md)

---
---
