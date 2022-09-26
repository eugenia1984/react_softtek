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

###  <img src="https://img.icons8.com/material-outlined/40/000000/add-property-1.png"/> 1 - PRESENTACION DEL MODULO

En este módulo vamos a profundizar en la utilización de compoenntes como estructura básica de nuestro sitio web e implementar estilos a nuestro sitio web.

### 1 - Armado de components y el flujo de información

Vamos a implementar varios componentes y ver cómo se integra el flujo de información entre ellos.

### 2 - Agregar estilos a nuestros componentes

Vamos a ver cómo agregar estilos a cada uno de los componentes que vamos creando para que sean atractivos a los usuarios.

### 3 - Renderización de la información

Vamos a ver diferentes técnicas para mostrar la información de nuestros componentes de acuerdo a cómo están almacenados en las estructuras de objetos que nos provee JavaScript.

---

### <img src="https://img.icons8.com/material-outlined/40/000000/add-property-1.png"/> ¿ Qué son las props en React?

Las **props** en REact se refiere al conjunto de **propiedades**, es decir, al **conjunto de datos que podemos compartir de un componente a otro** (**Desde un compoennte pare a un compoennte hijo**).

Las props son como **argumentos** que pasan a una función.

Las props pueden recordarte a los atributos HTML, pero en este caso puedes pasar cualquier valor de JavaScript a través de ellos, incluidos objetos, matrices, funciones e incluso JSX.

-> Las props no deben cambiar. Las variables de estado si pueden variar.

---

### ¿ Los componentes hijos se pueden pasar como props?

Dado a que los componentes hijos pueden ser elementos JSX, objetos o valores de JavaSCript, son válidos pasarlos como props. Hay escenarios donde te gustaría implementar **compoenntes genéricos**.

Los componentes genéricos son básicamente aquellos componentes que representan contenido intercambible y donde el padre no conoce a sus hijos.

React tiene una propiedad especial llamada **children** que permite pasar a sus hijos directemente al componente sin necesaidad de especificarlos individualemtne en las props.

---

## Layout

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

### Estilos

### <img src="https://img.icons8.com/office/100/000000/rgb-circle-2.png"/> Estilos con React

Los estilos en React los manejamos con **CSS**.

El CSS plano carece de ciertas funcionalidades que podrían hacer que el mantenimiento fuese más sencillo.

Por esta razón, axisten los llamados **preprocesadores** de CSS:

En React es posible usar varios tipos de preprocesadores como **Less**, **Sass**, **Stylus**, o **PostCSS**.

---
