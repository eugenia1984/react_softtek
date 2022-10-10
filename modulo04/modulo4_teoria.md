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

## :star: UNIDAD 9
