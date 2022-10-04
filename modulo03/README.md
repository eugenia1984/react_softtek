# :star2: Módulo 3. Buscador y sección favoritos

---

## Unidad 6. Creando secciones
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

## Unidad 7. Introducción a Redux
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
- Retoques finales a la seccion de Favoritos
- Verificación que el flujo de la applicacion funciona correctamente
- Ejercicio de repaso
- Introducciona  REdux
```

---

## Finalización de la seccion de Favoritos

 Favoriots.js:
 
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


---
---

- [**TEORIA Y VIDEOS**](https://github.com/eugenia1984/react_softtek/blob/main/modulo03/modulo3_teoria.md)

---
---
