# :star2: MODULO 4 * DISEÑO RESPONSIVE & TEST FINALES:star2:

---

## :star: OBJETIVOS DEL MODULO

```
- Realizar nuestros primeros pasos en el diseño responsive y a medida 
que avanzamos en nuestro proyecto, llevar adelante el testeo de nuestro código.
- Poder hacer aplicaciones front end responsive.
- Comprender la importancia del principio Mobile First y sus orígenes.
- Comprender los elementos incluidos en el principio Mobile First.
- Diseñar un login con Mobile First y Flexbox.
- Entender lo que es una media query y un breakpoint.
- Poder utilizar herramientas que analicen el diseño responsive.
```

---

## :star: UNIDAD 8 * MODO RESPONSIVE

### 8.1 ¿Qué es mobile First ?

## <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/40/000000/external-smartphone-digital-nomading-relocation-flaticons-lineal-color-flat-icons.png"/>  Diseño responsive

Este concepto refiere a una técnica que permite que el diseño de nuestra aplicación se adapte al tamaño de la pantalla de los diferentes dispositivos, teniendo en cuenta el diseño y tamaño de los recursos que se cargarán. 

Esta técnica piensa en el diseño de la aplicación en función de una rejilla flexible imaginaria basada en porcentajes y columnas o elementos que aparecen, desaparecen o se redibujan, según sea necesario para mejorar la experiencia del usuario en el dispositivo en que lo visualiza. 

Su funcionamiento se basa en unas reglas de estilo llamadas media query, que plasmamos en nuestros archivos CSS.

### <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/40/000000/external-smartphone-digital-nomading-relocation-flaticons-lineal-color-flat-icons.png"/>  ¿Pero, qué es Mobile First?

Es un concepto de diseño web que comienza optimizando el diseño para móviles y solo después, es optimizado para pantallas más grandes como la de ordenadores y portátiles.

En este tipo de diseño debemos prestar especial atención a que el contenido sea accesible fácilmente, la lectura sea clara y se cuente con tiempos cortos de carga de los elementos. También es importante que los enlaces sean visibles y se pueda hacer clic en ellos, teniendo en cuenta que en dispositivos de pantallas pequeñas, donde utilizamos el dedo, contamos con menos precisión. 

---

## 8.2. Dev tools para Mobile First

Las herramientas para desarrolladores de las que disponen los navegadores nos permiten, entre otras cosas, analizar cómo se verían las aplicaciones en los diferentes dispositivos móviles. 

Si utilizamos el navegador Chrome podemos acceder a estas herramientas:

- Haciendo click con el botón secundario del ratón en una página y seleccionando "Inspeccionar elemento". 

- Ingresando al menú > más herramientas > Herramientas para desarrolladores.

- Utilice la combinación de teclas “Ctrl + Mayús + I” o "alt+comando+ I", dependiendo del sistema operativo.

![image](https://user-images.githubusercontent.com/72580574/194799378-0c22f68c-a0c0-4b54-b298-f10c4762794f.png)

Al dirigirnos al ícono de herramientas del dispositivo podemos acceder a visualizar el sitio en el tamaño de una variedad de dispositivos o indicar una resolución personalizada, zoom o velocidad de conexión que necesitemos. 

![image](https://user-images.githubusercontent.com/72580574/194799432-1c626e48-4e55-40cf-ab0d-9334c9c5a9d3.png)


---

##  8.3. Login con Mobile First

## <img src="https://img.icons8.com/external-nawicon-flat-nawicon/40/000000/external-responsive-seo-and-marketing-nawicon-flat-nawicon.png"/> Las media query

Las media query son reglas condicionales, que permiten que ciertos estilos sólo se ejecuten cuando el navegador tiene determinado tamaño o, que ciertas propiedades sean suplantadas por otras o agregadas a la clase. 

En el ejemplo, la clase container tendrá las propiedades enunciadas en las primeras líneas, pero si el tamaño del navegador es inferior a 600 px la propiedad background-color será sustituida por la enunciada en la media query y border se sumará a la lista de propiedades de la clase container. 

![image](https://user-images.githubusercontent.com/72580574/194799525-2814e712-5066-4871-8fb5-5cdcdbda690f.png)

También podemos indicar más de una condición para que se apliquen las nuevas reglas. Como verás en el caso de ejemplo abajo, donde las reglas solo afectan a un rango de tamaños de pantalla, comprendido entre el valor mínimo y el valor máximo. 


![image](https://user-images.githubusercontent.com/72580574/194799567-91f75351-a997-4199-af0c-acfc1336450c.png)


En este punto, es importante aclarar que una propiedad Css que se encuentra debajo de otra, la sobrescribe si se trata de su misma clase. 

---

## :star: UNIDAD 9 * TRABAJANDO CON FORMULARIOS

## 9.1 REVISION DE FORMULARIO LOGIN

En esta unidad aprenderemos a construir un formulario con validación de datos utilizando Formik, pero primero veremos cómo validar los datos de un formulario de la forma clásica, para ayudarnos a entender mejor cómo hacerlo con Formik.

## ¿Que es JSX ?

Como en React el código JavaScript está unido a la lógica de la interfaz de usuario, en lugar de separar el maquetado y la lógica lo hacemos todo en un mismo archivo de extensión JSX.


JSX es una extensión de la sintaxis de JavaScript, en la que también podremos desarrollar nuestros componentes, aunque podemos seguir usando archivos JS, pero de todos modos usar JSX puede ayudar a visualizar mejor el código cuando estemos trabajando con una interfaz de usuario. 

## ¿Por qué usar Fragments? 

Cuando es necesario retornar varios elementos en un mismo componente los fragmentos permiten agrupar una lista de hijos sin agregar nodos extra al DOM.

La sintaxis más corta para hacerlo es <></> de la misma manera que usarías cualquier otro elemento, excepto que este parece una etiqueta vacía, no soporta llaves o atributos y no crea etiquetas div innecesarias en nuestro DOM. 

![image](https://user-images.githubusercontent.com/72580574/194800673-407f172e-2ddb-409a-a769-e54b9a9aa405.png)


## <img src="https://img.icons8.com/external-justicon-flat-justicon/40/000000/external-hook-pirates-justicon-flat-justicon.png"/> El hook useState

Insert your text hereUseState es un hook que permite usar el estado y otras características sin escribir una clase. 

Como todo hook, para utilizarlo primero debemos importarlo. En la declaración del hook notaremos que no se declara de forma clásica, sino que tendrá dos partes: por un lado, su nombre y, por otro lado, una función que permitirá darle valores, que por convención se suele escribir sin el prefijo set.

Lo primero que debemos hacer al declarar useState() es pasarle como argumento su estado inicial, como en el ejemplo donde le estamos pasando un string vacío, aunque podríamos darle el valor que necesitemos. 

![image](https://user-images.githubusercontent.com/72580574/194800775-550fd4e4-5313-48b8-aea7-0ab66f81a524.png)

*Ejemplo de asignacion de argumento para useState()*

Una vez declarados los useState podremos usarlo en cualquier parte de nuestro componente. 

En el código de ejemplo, se aprecia que al cambiar el valor de la etiqueta input (onChange) se asigna su valor a la variable de estado email por medio de setEmail(event.currentTarget.value) donde el argumento es el valor de la etiqueta. 

![image](https://user-images.githubusercontent.com/72580574/194800831-7fc4fa00-4e7d-4192-a134-acdf29850f09.png)


*Cambio de valor de la etiqueta input*


###  <img src="https://img.icons8.com/color/40/000000/security-checked--v1.png"/>¿ Qué es preventDefault?

Utilizamos preventDefault cuando necesitamos que un formulario ejecute funciones y se requiere que la página no se refresque y borre todo lo ingresado. Esto se produce porque al llamar a preventDefault hace que cualquier acción por defecto que deba producirse como resultado del evento e, no ocurrirá.

En la función a la que llama el formulario podremos utilizar **e.preventDefault()**, siendo **e** el evento del formulario.

![image](https://user-images.githubusercontent.com/72580574/194800931-f253c35a-b28f-437b-a274-cd6c16d43d83.png)


---

## 9.2 ¿ Qué es Formik?

Formik es una biblioteca que nos ayudará a obtener valores dentro y fuera del estado de un formulario, validaciones de datos, emitir mensajes de error o advertencias y simplificar el envío de datos de formularios. 

## <img src="https://img.icons8.com/clouds/100/000000/form.png"/> Instalar Formik

El primer paso para usar Formik es instalarlo y podemos hacerlo desde la consola por medio de npm con el comando: 

![image](https://user-images.githubusercontent.com/72580574/194801022-f524dc94-da2a-43e8-94c6-6103b916061c.png)


O con:

![image](https://user-images.githubusercontent.com/72580574/194801042-6beb33b9-f279-464f-8d3e-88c023bad34e.png)


##  ¿Y si ya lo instalaste, pero no lo recuerdas?

En caso de que no recordemos lo que instalamos podemos ver todas las dependencias que tenemos dirigiéndonos al archivo package.json que se encuentra en la raíz de nuestro proyecto y ver en la lista de dependencias. Si está ahí, es porque lo instalamos o ya venía instalado. 

![image](https://user-images.githubusercontent.com/72580574/194801078-e1d45c1d-c464-453f-8e7f-2ebf4c30b7b7.png)

Como podemos ver en la imagen, ya tenemos Formik instalado y listo para ser usado. 

---

## 9.3 Login con Formik 

## <img src="https://img.icons8.com/clouds/100/000000/form.png"/>  Implementando Formik como un hook

Si llegaste hasta aquí imagino que pudiste implementar el formulario con validador de errores de forma manual. 

Ahora vamos a realizar algunos cambios en ese código para mejorarlo con Formik.

¿Por qué usar Formik como hook? Hay varias formas de implementar Formik que podrás examinar en el apéndice de éste documento, pero nosotros elegimos implementarlo como hook porque creemos que es más sencillo de entender, ya que la lógica es parecida a lo que vimos anteriormente. 

![image](https://user-images.githubusercontent.com/72580574/194801174-ef8e785c-28c2-42b6-88c3-1a88fbfff7e4.png)
*Importar Formik*

### Crear la constante Formik

Crearemos una constante que nos proporcionará los valores y las funciones para validar nuestro formulario y también para realizar las acciones si las validaciones pasan.

![image](https://user-images.githubusercontent.com/72580574/194801216-c1b2320b-29d9-4011-ade6-94a169778110.png)
*Crear la constante Formik*

Vamos a proporcionar a useFormik tres constantes: 

- **initialValues**: donde inicializaremos los campos del formulario.

- **validate**: donde declararemos la forma en la que se validará nuestro formulario.

- **onSubmit**: donde indicaremos las acciones que se llevarán adelante al enviar el formulario correctamente. 


##  Declarar los estados iniciales (initialState)

Nosotros tenemos solo dos elementos, pero podríamos tener muchos más, y es aquí donde declararemos qué valores tendrán al cargar el formulario por primera vez. 

![image](https://user-images.githubusercontent.com/72580574/194801270-898c074b-e1bc-487d-969b-dcf07245ec9e.png)

---

## 9.4 Registro con Formik

## <img src="https://img.icons8.com/clouds/100/000000/form.png"/> Crear los validadores (validate)

Y aquí llegamos a lo más importante: el validador. 

¿Qué es el validador? 

Una constante que tendrá una función flecha que retornará los errores que se produzcan en el formulario. 

Pero claro que Formik no es adivino, por lo que le indicaremos **qué es lo que consideramos errores** (que en nuestro ejemplo, es simplemente cuando no completan el campo). 

Para indicar lo que deberemos evaluar, declararemos tantos **if** como condiciones a analizar que consideremos necesarias.

En nuestro caso pondremos como condición en los if: **!values.campo** siendo “!” la negación que devolverá verdadero cuando no exista el campo en el formulario.

![image](https://user-images.githubusercontent.com/72580574/194801383-7b5c462a-be2d-4243-b7cd-8468ad9be9c9.png)


##  Que pasará al enviar el formulario (onSubmit) 

Si se ha validado correctamente todo se ejecutará onSubmit. En el ejemplo crearemos un ítem en el localStorage, donde se almacenan datos de manera local, y en donde guardaremos “yes” para saber si la validación fue exitosa. 

![image](https://user-images.githubusercontent.com/72580574/194801405-5ebddf7f-5056-43bc-bea0-012c34fc8049.png)
*Crwacion de un item en el localStorage*

Para ver si todo salió como debía, podemos utilizar las herramientas de desarrolladores del navegador e ir a la consola y llamar al localStorage:

![image](https://user-images.githubusercontent.com/72580574/194801440-4dc3f7ac-c80c-47ca-8f6d-c19a9c4a1425.png)



## Informar al usuario de los errores

Una vez que tengamos contemplado qué hacer en cada uno de los errores, debemos informar al usuario cuando estos ocurran.

Para ello podemos utilizar el renderizado condicional {si_esto_existe&&se_muestra_esto} que nos indicará si hay errores. 

![image](https://user-images.githubusercontent.com/72580574/194801456-b3e2d6dc-9518-4ada-b349-c3690866da76.png)
*Verificacion de errores*

Y si para este punto, logramos desarrollar todo el complemento deberíamos ver algo parecido a esto:

![image](https://user-images.githubusercontent.com/72580574/194801483-cd92ede4-f052-4333-992f-eec7c02b480d.png)


---

## :star: UNIDAD 10 * TRABAJANDO CON LAS RUTAS

---

## 10.1 React Router Dom 6, rutas y roles

## <img src="https://img.icons8.com/office/16/000000/route.png"/>  ¿Para qué es necesario administrar las rutas?

React nos permite desarrollar aplicaciones SPA (single-page application), una aplicación web de una sola página. Esto permite una experiencia similar al de una aplicación corriente, y si bien esto es bueno para mejorar la experiencia del usuario, muchas veces nos priva de otros elementos como la creación de rutas fijas donde colocar partes específicas de nuestro sitio (por ejemplo, misitio.com/contacto) o para crear rutas dinámicas (por ejemplo, un producto cuya url es misitio.com/producto/id).

Con una herramienta que administre rutas, podemos utilizar todo el potencial de React y a la par poseer URL amigables. 

Para ello, podemos utilizar React Router Dom y de forma relativamente sencilla establecer rutas, crear páginas públicas y privadas, realizar redirecciones a otras páginas según ciertas condiciones y crear rutas para páginas 404. 

##  <img src="https://img.icons8.com/office/40/000000/route.png"/> ¿Qué es React Router Dom?

Es una biblioteca de enrutamiento del lado del cliente y del servidor con todas las funciones para ser aplicado en React.

### Instalación

Para instalarlo ejecutamos el siguiente comando en la raíz de nuestro proyecto. 

![image](https://user-images.githubusercontent.com/72580574/194801711-e54840f2-2b11-4f97-82fc-bcb6fbea5f9b.png)


###  <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/40/000000/external-forbiden-summer-olympics-flaticons-lineal-color-flat-icons-4.png"/>¿Por qué es necesario que existan tipos de usuarios y permisos?

Si necesitamos crear una aplicación que posea autenticación de usuarios, probablemente debamos tener rutas que alguien que no tiene una sesión activa no pueda ver. Para la administración de estas rutas, podemos crear tipos de usuarios y permisos asociados a estos como, por ejemplo, que un usuario logueado tiene permiso de acceder a determinadas rutas. 

### <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/40/000000/external-forbiden-summer-olympics-flaticons-lineal-color-flat-icons-4.png"/> ¿Qué son las páginas públicas y las privadas?

Las rutas que pueden ser accedidas sin la necesidad de tener sesión activa en nuestro sitio son las públicas y las que necesitan una autenticación previa son las privadas.

---

## 10.2 Creacion de rutas con React Router Dom 6

###  <img src="https://img.icons8.com/office/40/000000/route.png"/>  Envolver nuestra App

Una vez que React Router esté instalado como una dependencia, abrimos src/index.js e importamos BrowserRouter desde react-router-dom y luego envolvemos la App en un ```<BrowserRouter>```

![image](https://user-images.githubusercontent.com/72580574/194801838-3f84c976-a39a-4afa-8705-1e3f597a2a75.png)

###  <img src="https://img.icons8.com/office/40/000000/route.png"/> Desarrollar las rutas

Ahora ya podemos trabajar con React Router en nuestra aplicación. Para ello, importamos Routes y Route desde react-router-dom y luego podemos reemplazar el marcado predeterminado con algunas rutas en nuestra App.js

```<Routes>``` debe envolver a todas nuestras rutas que serán declaradas de la siguiente forma: 

![image](https://user-images.githubusercontent.com/72580574/194801897-55afcd41-0a2e-4fb8-8e8a-f7f33f4e614c.png)

El código en App.js podría ser algo así:

![image](https://user-images.githubusercontent.com/72580574/194801908-c5c95b68-ff8c-4d1d-b9e2-2b195d6c6570.png)


En el ejemplo podemos ver cómo la ruta “/login” nos mostrará el componente Login.

![image](https://user-images.githubusercontent.com/72580574/194801928-9ac7b002-289e-45d1-9a84-d31c58f88973.png)


---

## 10.3 Implementación con React Router Dom 6, rutas y roles

Si vamos al componente donde declaramos nuestro enrutamiento, podremos limitar el acceso a las páginas que consideremos privadas.

Para realizar esta tarea usaremos un componente de react-router-dom llamado Navigate, por lo que debemos importarlo. 

![image](https://user-images.githubusercontent.com/72580574/194801978-9c4b9cc4-62b9-4816-b60e-00fb6d3564f1.png)

Luego de esta importación, debemos definir cuáles serán las condiciones a cumplir para que sea posible acceder a las rutas privadas. Esto lo definiremos en un componente RequirAuth que, a modo de ejemplo, preguntamos si no existe un elemento del localStorage llamado logged. 

Cuando no exista este elemento, que significó para la lógica de nuestra aplicación que el usuario no se ha logueado, retornaremos el elemento Navigate y en el parámetro to indicaremos cuál es la ruta a la que debe ir. 

![image](https://user-images.githubusercontent.com/72580574/194802012-706ec7c6-2384-4d5f-a559-e90713ed15f4.png)

Como habremos visto, el parámetro del componente al que llamamos children, es el componente al que podemos ir si estamos logueados, es decir, que existe el ítem logged en el localStorage.

![image](https://user-images.githubusercontent.com/72580574/194802023-a969a16f-146b-43e6-aafb-2c0e4a4103b9.png)

Habrás notado que el parámetro de este elemento es children. Esto es porque es el hijo del elemento RequirAuth, que en nuestro ejemplo es el componente Task. 

Lo que se hace aquí es pasar por el componente RequirAuth como un parámetro.

![image](https://user-images.githubusercontent.com/72580574/194802039-00ea2f7d-21df-4161-bfb7-296224673793.png)

Ahora, si hacemos esto podremos encontrarnos con la limitante de crear ese elemento en el localStorage o eliminarlo si ya lo creamos. Por eso, te dejamos aquí los comandos que debes ejecutar en la consola de tu navegador para ver esto: 

![image](https://user-images.githubusercontent.com/72580574/194802050-ce911430-19d1-447b-8fbd-1d0ec71d5204.png)
*Crear el item y darle un valor*

![image](https://user-images.githubusercontent.com/72580574/194802073-d631a6e7-4340-4c55-89de-8558de2e5941.png)
*Remover el item*

---

## 10.4 Transicion entre rutas

###  <img src="https://img.icons8.com/pastel-glyph/40/000000/planned-path.png"/> ¿Por qué es necesario pensar en la transición entre rutas?

Desde el punto de vista de la funcionalidad, no son una necesidad las transiciones animadas entre rutas, pero crear este tipo de efectos permite mejorar la experiencia del usuario en nuestras aplicaciones.


### <img src="https://img.icons8.com/pastel-glyph/40/000000/planned-path.png"/>  ¿Qué es Framer Motion?

Es una biblioteca de movimiento lista para producción en React y que, entre una variedad de aspectos/cuestiones que podría explorar en su documentación oficial, sirve para que realicemos transiciones animadas entre una ruta y otra. 


### <img src="https://img.icons8.com/pastel-glyph/40/000000/planned-path.png"/> Animación en las transiciones entre rutas

Para darle animación a nuestra aplicación cada vez que se cambia de ruta debemos seguir los siguientes pasos: 

1. 
 
a) **Instalar la biblioteca con npm**
![image](https://user-images.githubusercontent.com/72580574/194802174-d48f2bf0-3cb5-4744-8c4c-0bdd5569e932.png)

b) **Instalar la biblioteca con yarn**
![image](https://user-images.githubusercontent.com/72580574/194802224-a21e4c19-ca7c-4bb9-a727-97720e0cc9e6.png)

2. ** Importamos en nuestro componente**
![image](https://user-images.githubusercontent.com/72580574/194802256-c215bec4-380a-404d-a9a0-7327a68491e3.png)


### <img src="https://img.icons8.com/pastel-glyph/40/000000/planned-path.png"/> Un objeto que controlará las transiciones

Ahora debemos crear un objeto que controle los tres momentos de una animación de transición: el inicio o initial, la animación entre un estado y otro, aquí llamada animate y, luego, la animación de la salida, que solemos llamar exit.

Estos parámetros de la pageTransition serán también los parámetros que colocaremos en cada una de las rutas que queremos que tengan la transición deseada. 

  ![image](https://user-images.githubusercontent.com/72580574/194802289-d4c496ff-986f-4c79-beb3-89507876526a.png)

 ### <img src="https://img.icons8.com/pastel-glyph/40/000000/planned-path.png"/>  Anidar nuestras rutas
 
Debemos anidar nuestras rutas primero con AnimatePresence, el cual detectará los componentes que son desmontados para aplicar las transiciones necesarias y luego, anidamos cada ruta dentro de motion.div donde indicaremos cuál animación se ocupará en cada uno de los momentos initial > animate > exit.


![image](https://user-images.githubusercontent.com/72580574/194802331-609dfbea-a285-484e-b2a5-e9eaed4e9662.png)


### <img src="https://img.icons8.com/external-soft-fill-juicy-fish/40/000000/external-redirect-crisis-management-soft-fill-soft-fill-juicy-fish.png"/> Redirigir del login al inicio

Si bien esto no está relacionado estrictamente con la animación entre rutas, al loguearnos es muy probable que necesitemos redirigir al inicio de nuestro sitio y queramos hacerlo con una animación.

Para la redirección debemos importar useNavigate y crear una constante a la cual asignarle ese hooks, en este caso es navigate. 

En nuestro ejemplo, al ser exitoso el login, es cuando realizamos la redirección con navigate, pasándole el parámetro de la url hacia dónde iremos. 

![image](https://user-images.githubusercontent.com/72580574/194802361-8357426c-4279-46bd-ab6f-fd8589b44c09.png)


---

## 10.5  Lazy Import y suspense

## <img src="https://img.icons8.com/office/16/000000/spinner-frame-5.png"/> ¿Por qué usar lazy loading?

Una aplicación React tendrá sus archivos empaquetados en un bundle, lo que significa tener los archivos importados y fusionados en un único archivo. 

A medida que la aplicación crezca, el bundle también crecerá y para evitar terminar con un bundle grande, es bueno dividirlo para que se cargue de forma dinámica durante la ejecución de la aplicación. 

Dividir el código puede ayudarte a cargar solo lo necesario en cada momento y así mejorar el rendimiento, al reducir la cantidad de código durante la carga inicial.

Los componentes que queremos que se carguen solo cuando lo vamos a utilizar, los reemplazamos de esta forma en vez de la línea de importación.

![image](https://user-images.githubusercontent.com/72580574/194802390-11a10a64-236e-4697-a895-f6f5e3b9499b.png)

Y luego, en el lugar donde lo utilicemos, lo envolvemos con suspense que cargará algo mientras se carga nuestro componente. 

![image](https://user-images.githubusercontent.com/72580574/194802403-979bc16b-c856-4a44-b3e7-569bc9364dc2.png)


### <img src="https://img.icons8.com/office/16/000000/spinner-frame-5.png"/>  ¿Cuándo conviene utilizar lazy?

La utilización o no de esta herramienta dependerá de la estrategia que queramos implementar, aunque una buena opción es utilizarlo en aquellos componentes que son muy grandes o también los que no solemos utilizar mucho, indistintamente de su tamaño.

---

## :star: UNIDAD 11 * ADAPTANDO A MOBILE FIRST

---

## <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/40/000000/external-head-anatomy-flaticons-lineal-color-flat-icons-6.png"/> 11.1 Header


La etiqueta <header> contiene al encabezado del sitio, donde se colocan habitualmente los vínculos de navegación, los formularios de búsqueda, los logos, etc. En muchos casos, los contenidos del encabezado son iguales a lo largo de la navegación del sitio.

Si bien se recomienda utilizar la etiqueta header para el contenido que será el header en nuestro sitio, podríamos utilizar una etiqueta <div> dándole la misma utilidad. 

Este podría ser un ejemplo de esta etiqueta: 
 
 ![image](https://user-images.githubusercontent.com/72580574/194802708-549183c1-bcd5-4e4e-a898-c518097e6743.png)

 En este archivo de header, el usuario solo visualizará dos elementos, un logo y una x para cerrar la sesión. 

La x al ser apretada ejecutará handleLogout que, por un lado, borrará el ítem logged y luego, redirigirá al usuario al componente login. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194802730-fe1fba87-47d3-4bb8-b733-142f94672b24.png)

 
 Si bien ya ocupamos en ejemplos anteriores el elemento Navigate, no lo ocupamos en este componente, por lo que debemos importar el hook para ocuparlo: 
 
 ![image](https://user-images.githubusercontent.com/72580574/194802819-2e4a15a8-42da-4160-97dd-bcf7ea447222.png)

 Aquí podremos ver con más claridad el esquema de funcionamiento básico de nuestro header: 
 
 ![image](https://user-images.githubusercontent.com/72580574/194802844-0c21f2eb-585d-4d03-ace6-ee9d9354cd8a.png)

 ## <img src="https://img.icons8.com/external-bearicons-flat-bearicons/40/000000/external-colors-graphic-design-bearicons-flat-bearicons.png"/> El CSS
 
 Y, por último, para dar a nuestro header el estilo mostrado arriba, deberíamos aplicar los siguientes estilos a la hoja CSS enlazada a nuestro componente. 

Para importar el CSS a nuestro componente header debemos ejecutar: 

```JSX
import "./Header.style.css";
```
 
y aquí la hoja de estilos que dará forma al HTML.
 
 ![image](https://user-images.githubusercontent.com/72580574/194802935-f8eda365-ca2c-4e55-903f-9f4a2a9a38c6.png)

 En nuestro CSS para dar el efecto de separación entre el logo y la x utilizamos Flexbox, una herramienta de diseño en CSS que podrás ampliar yendo a los enlaces recomendados. 
 
 ---
 
 ## 11.2 CSS Global y estilos en login
 
 ### <img src="https://img.icons8.com/external-bearicons-flat-bearicons/40/000000/external-colors-graphic-design-bearicons-flat-bearicons.png"/> Variables globales en CSS
 
Tenemos varias formas de darle estilos a nuestra aplicación por medio de las hojas de estilo: podemos hacer que cada componente tenga su propia hoja de estilo, que exista una única hoja de estilos para toda la aplicación o ambas, distinguiendo qué colocamos en cada una. 

La forma más utilizada, que además utilizaremos en los ejemplos, es que exista una hoja global, donde colocaremos las variables globales para que puedan ser llamadas desde las hojas de estilos particulares de cada componente. 
 
### Las variables globales

 De esta forma declaramos las variables globales, en la hoja de estilo que es importada por el componente padre de todos los componentes.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803023-c388e34f-2eec-48ac-9994-b7f44051961a.png)

 ### Llamada a las variables globales 
 
Las llamadas a las variables globales desde los archivos CSS de componente se realiza de la siguiente forma: 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803048-7ce758a7-a78e-4ce0-8888-fde69c1838e1.png)

 
 ###  <img src="https://img.icons8.com/external-bearicons-flat-bearicons/40/000000/external-colors-graphic-design-bearicons-flat-bearicons.png"/> ¿Por qué usar !important en una propiedad CSS?
 
Muchas veces podemos tener situaciones en donde una propiedad sobrescribe otra y para indicar cuál está por encima de otra indicamos important. En el ejemplo que tenemos a continuación, la propiedad padding inicial está por encima de la segunda vez que lo declaramos.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803079-2b3b4010-6fff-4ebe-b4a2-64a381d46e40.png)

 Para priorizar una propiedad podemos hacerlo escribiendo !important al final de la declaración y antes del punto y coma. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803093-794f58d3-32a0-41a8-a5c4-4f7ca77909df.png)

 
 ###  Importar google fonts
 
Para importar una fuente desde fonts.google.com, debemos buscar la fuente que necesitamos y agregarla. 
 
![image](https://user-images.githubusercontent.com/72580574/194803106-8221e71d-c48e-4ddf-b09c-0d4f13db911a.png)

 En nuestro ejemplo utilizamos la función import para vincular la fuente con nuestro proyecto: 
 
![image](https://user-images.githubusercontent.com/72580574/194803117-c2771f10-5f37-44a3-8534-9837978ad996.png)

 El @import debemos ubicarlo en nuestro archivo CSS y después indicar dónde aplicaremos la fuente, que en este caso se encuentra de forma global con el *.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803140-5269cebe-6c92-48d2-9999-51818d190068.png)

 También podemos enlazar la fuente a nuestro proyecto con la etiqueta link y colocar el código que nos proporciona Google fonts, en el <head> de nuestro HTML principal y en el CSS aplicaríamos la propiedad CSS font-family, tal y como nos la proporciona Google fonts.
 
 ---
 
 ## <img src="https://img.icons8.com/color/40/000000/todo-list.png"/> 11.3 Lista de tareas Mobile First
 
 El listado que realizamos en nuestro desarrollo de ejemplo cuenta con un componente de tareas donde las mismas deben listarse. 

En nuestro caso, cada una de las tareas es un div de clase “list” que se repetirá según la cantidad de tareas que mostremos.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803213-5b07d792-39bf-4a35-90f0-836cca3feb46.png)

 El código de cada uno de los bloques pertenecientes a las tareas es
 
 ![image](https://user-images.githubusercontent.com/72580574/194803223-84ffb35f-d518-4fdb-8828-d5cae9aea1a6.png)

 Lo que permitirá una vista similar a esta
 
 ![image](https://user-images.githubusercontent.com/72580574/194803239-2ec7ffd8-064a-4bad-806a-71ae442875f6.png)

 Hasta acá es donde nos es posible llegar con nuestra explicación sobre los estilos volcados en los archivos CSS. Para continuar profundizando con el tema, pueden estudiar el repositorio del proyecto.
 
 ---
 
 ## 11.4 Listados en escritorio y utilidades
 
 ## <img src="https://img.icons8.com/dotty/40/000000/mac-book-pro-m1.png"/> Renderizado condicional según el ancho de la pantalla
 
Para lograr esto lo que debemos hacer es que el componente sepa cuál es el tamaño de la pantalla y, según esto, renderice los componentes que solicitamos para cada tamaño de pantalla. 
 
 
  ##<img src="https://img.icons8.com/dotty/40/000000/mac-book-pro-m1.png"/>  ¿Cómo saber si estamos en un teléfono o una laptop?
 
Utilizando useState podremos crear una constante que exista si el ancho de la pantalla es inferior a un tamaño que consideremos como el ancho de un teléfono o, caso contrario, consideraremos que el ancho es el de una computadora. 

Cuando el componente se renderiza, se chequea cuál es el ancho de la pantalla y si es inferior a 900 px. isPhone es true. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803301-30c09cf0-321f-4329-a7c7-d57e20fd4af8.png)

 Con esta constante que modifica su valor de verdad dependiendo del tamaño de la pantalla ya podemos colocar un renderizado condicional en nuestro componente, es decir, que aparezca una parte u otra dependiendo de si una constante es verdadera o falsa. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803313-f451e918-246a-4c15-ad29-5fb3680368d2.png)

 En este punto logramos que nuestra aplicación se renderice cada vez que se carga según el tamaño de la pantalla. Sin embargo, necesitamos que se haga de forma automatizada, por lo que para lograrlo utilizaremos useEffect que en este caso ejecutará handleResize() cada vez que se modifique el tamaño de la pantalla. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803328-4275defe-fb79-422d-a01e-e191f531039a.png)

 En el objeto windows llamamos a addEventListener, un escuchador de eventos que en este caso lo pondremos para que detecte el resize del objeto windows, es decir que “escuche” cada vez que se modifica el tamaño de la pantalla y pueda ejecutar handleResize() y luego de hacerlo, lo removemos. 
 
Aquí está handleResize, que simplemente modifica el valor de verdad de isPhone. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803340-d4b10d31-3ed1-454a-808c-a64f85087356.png)

 
 ##  Limitar las cadenas de caracteres
 
Cuando tenemos algún elemento donde la cantidad de caracteres que puede tener superará lo que esperamos, rompiendo el diseño o impidiendo una experiencia del usuario aceptable, podemos limitar la cantidad de caracteres de ese elemento. 

Para ello utilizaremos una función llamada slice(0, tamaño_que_queremos) que al ejecutar sobre un string podemos hacer que esa función devuelva la cantidad de caracteres que necesitemos. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803358-05041121-67fb-40e2-827a-570b9074f819.png)

 En la siguiente función, recibimos un string y analizamos por medio de un if si es mayor a 370 caracteres. De ser así lo recorta en 367 más los “...” y además agrega un elemento botón (addButton).
 
 ---
 
 ## 11.5 Refactorizaciones
 
 ### Implementar un custom hook
 
Un custom hook es una función común y corriente de JavaScript cuyo nombre comienza con ”use” y que puede llamar a otros hooks.

Para implementar nuestros propios hooks, debemos implementar un componente al que nombraremos con el prefijo use.

Su estructura interna dependerá de la solución que debemos implementar. En nuestro ejemplo desarrollaremos un hook que resuelva el problema de analizar el tamaño del dispositivo. 

En nuestro hook distinguiremos tres partes fundamentales: la importación, el desarrollo que resolverá el problema y el retorno de los elementos. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803406-bbf007d4-999c-42d9-81d2-b901a083c5c9.png)

 ### Refactorizar el componente listado
 
Ahora veremos cómo al incluir un componente dentro de otro componente, podemos pasarle datos y utilizarlo de forma repetitiva con un map. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803427-0e89ed6f-3a89-4764-9027-711a85a1951c.png)

 Lo que hace map aquí es construir una iteración de componentes Card, a los cuales les pasa los datos proporcionados por cardsData para cada uno de sus elementos. 

Distinguiremos dos elementos fundamentales en esta estructura: El key y el data que tendrá todos los datos sacados del archivo que ocuparemos para colocar la información. 

 ![image](https://user-images.githubusercontent.com/72580574/194803441-c657af42-7aba-426c-a434-0f3099056287.png)

 
 ---

 ## :star: UNIDAD 12 * TRABAJANDO CON FORMIK
 
 ---
 
 ### 12.1. Creación con Formik
 
 Este componente es un formulario que permitirá el ingreso de datos para la creación de cada una de las tareas. 

Lo crearemos y lo importamos al inicio del componente Tasks
 
 ![image](https://user-images.githubusercontent.com/72580574/194803630-1c80f77d-468a-4d91-953f-856d76b1218a.png)

 Este formulario debe tener todos los campos que sean necesarios ingresar por el usuario, y no los datos como, por ejemplo, el del nombre del usuario, que se podrá automáticamente o las id. 

 ---
 
 ## 12.2. Validación con Yup
 
 ### ¿Qué es Yup?
 
Es un generador de esquemas para la validación de valores, es decir, que nos permitirá validar los datos de nuestros formularios. 
 
### Instalar Yup
 
 ![image](https://user-images.githubusercontent.com/72580574/194803679-4f09d17d-4930-495e-8b77-43b3a76c9f71.png)

 
 ###  Importar Yup
 
Yup tiene una forma particular de ser importado a diferencia de otros elementos importados que estuvimos viendo. Pero seguiremos por este camino, ya que Yup es considerada por los desarrolladores de Formik como un gran complemento para trabajar en conjunto. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803696-682e4100-74e7-443c-a24b-8a0d11d101db.png)

 
 ###  El objeto Yup para validar
 
Aquí desarrollamos el objeto que validará al formulario. Este objeto tendrá como elemento a cada uno de los campos de nuestro formulario que queramos validar.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803706-c984c672-d0e4-4561-bb05-5602eb4e08c7.png)
 
 
- **.min(6, "mensaje")** podemos ponerlo para que de error si el input tiene menos caracteres del que ingresamos.
 
- **.required(required)** podemos ponerlo para que nos indique que el campo es obligatorio

Este nuevo objeto validationSchema, se suma a lo que habíamos aprendido de formik como un parámetro.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803765-922a3d4f-93e6-4b97-8da7-0e91c28f742a.png)

 
 ### Objeto validation Schema
 
 ![image](https://user-images.githubusercontent.com/72580574/194803785-c39b9db2-2cec-40da-9570-47f3b1b22a4a.png)

 
 Y así será como colocaremos en el HTML, donde errors.title nos mostrará los errores que devolverá yup.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803804-41286627-1a46-4b6b-8ae8-aea16b19a471.png)

 Es importante tener en cuenta que si no colocamos un mensaje personalizado en .min aparecerá el mensaje por defecto en inglés. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803823-ea543156-e63e-4788-8365-e0e3f786a7c3.png)
 
 Si nuestro mensaje para campo requerido será igual en todos los campos, podríamos utilizar una constante a la que llamemos en cada uno de los elementos del objeto validationSchema.
 
 ![image](https://user-images.githubusercontent.com/72580574/194803832-ce12851b-554d-47db-8736-fd419cad3c11.png)

 
 ---
 
 ## 12.3 OnBlur en Formik y UXp
 
### La propiedad touched

 Esta propiedad de formik, que se suma a las aprendidas, nos permitirá saber si un campo fue visitado. 

 ![image](https://user-images.githubusercontent.com/72580574/194803883-f36f42c0-1ba4-4a55-be1f-dd626df1bcfd.png)
 *Propiedad touched*
 

 Al sumarlo al HTML nos avisará que tendremos, aparte de los errores que ya indicamos, una validación más que es: si lo visitamos y no lo valoramos correctamente. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803906-c21b0149-f0ae-4e60-a832-e02b28bff6f0.png)
 *Validación de valoración*
 
 Además, sumaremos al input un elemento onBlur que disparará el handleBlur cada vez que se deja ese input. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803920-9b053f18-0f97-4996-9ba8-41a089fe72e8.png)

Y sumaremos a las validaciones de Formik.

 ![image](https://user-images.githubusercontent.com/72580574/194803932-a51bfb90-209f-428a-9c1b-d0888c5183b0.png)

 
 ![image](https://user-images.githubusercontent.com/72580574/194803939-de95341a-a07c-4f2b-afff-980ca32ca0f1.png)

Para este punto logramos dos tipos de validaciones, por un lado, la validación cada vez que apretamos el botón, validando el formulario en general y, por el otro, cada vez que abandonamos el campo.
 
### Mejorando el aviso de error

 Para mejorar el aviso de error podríamos colocar una clase a nuestro input que se active al presentarse la validación incorrecta. 

La línea que contiene la className agrega la clase error en caso de presentarse el error de validación. 
 
 ![image](https://user-images.githubusercontent.com/72580574/194803976-fa582e8b-2075-49a5-8a53-41546d491074.png)

 Este recurso también podríamos ocuparlos en otras partes del formulario, como, por ejemplo, en el mensaje de error:
 
 ![image](https://user-images.githubusercontent.com/72580574/194803995-eeda79b8-4629-495d-8209-94dffa34d397.png)

 
 ---
 
 ## Para profundizar
 
 Si quieres profundizar tu conocimiento respecto a lo dado en esta unidad, te recomendamos que visites los siguientes enlaces: 
 
- [Herramientas de desarrollo de Chrome para revisar etiquetas](https://support.google.com/campaignmanager/answer/2828688?hl=es)
 
- [Herramientas para desarrolladores en Mozilla Firefox](https://developer.mozilla.org/es/docs/Learn/Common_questions/What_are_browser_developer_tools)
 
- [CSS media queries](https://developer.mozilla.org/es/docs/Web/CSS/Media_Queries/Using_media_queries)
 
- [Fragments](https://es.reactjs.org/docs/fragments.html)
 
- [Todo sobre JSX](https://es.reactjs.org/docs/introducing-jsx.html)
 
- [Variables de Estado](https://es.reactjs.org/docs/hooks-state.html#declaring-a-state-variable)
 
- [Preguntas frecuentes sobre Hooks](https://es.reactjs.org/docs/hooks-faq.html)
 
- [Documentación de Formik](https://formik.org/)
 
- [Renderizado Condicional](https://es.reactjs.org/docs/conditional-rendering.html)
 
- [Documentación de React Router DOM](https://reactrouter.com/en/main)
 
- [Framer Motion](https://www.framer.com/)
 
- [División de Código con React](https://es.reactjs.org/docs/code-splitting.html)
 
- [Conceptos básicos de Flexbox](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
 
- [Google Web Fonts](https://fonts.google.com/)
 
- [Todo lo que hay que saber de String](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String)

 - [Construyendo tus propios Hooks](https://es.reactjs.org/docs/hooks-custom.html)
 
- [Yup en NPM](https://www.npmjs.com/package/yup)
 
 
