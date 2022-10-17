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

## JSON Server

Ideal para desarrollar prototipos o pruebas de concepto, permite hacer request a una API REST, guardando las modificaciones en un archivo.

###JSON Server Auth

Extiende json con login y register


---
---
