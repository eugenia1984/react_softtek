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
