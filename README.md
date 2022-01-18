## Práctica: AR (Realidad Aumentada)

Nombre: Aram Pérez Dios  
Correo: alu0101244488@ull.edu.es  
Universidad: Universidad de La Laguna 
Asignatura: Interfaces Inteligentes
Grupo: PE102  

### Vuforia

Lo primero para empezar con el desarrollo de la aplicación es crearse una cuenta en Vuforia [https://developer.vuforia.com/](https://developer.vuforia.com/).

El siguiente paso es crear por una parte una licencia y por otro crear la base de datos de nuestros markers.

Para crear la licencia, nos colocamos en el apartado develop y License Manager. Aquí creamos una licencia con losvalores por defecto, y le damos un nombre.

![](https://github.com/alu0101244488/Interfaces-Inteligentes-AR/blob/main/img/lcencias.png?raw=true)

El siguiente paso es colocarse en el apartado de Target Manager donde primero creamos una base de datos y luego introducimos las imagenes que vamos a emplear como targets. Podemos buscamos unos markers. En este caso se hace uso de algunos que se encuentran como ejemplo en OpenCV:
[https://docs.opencv.org/3.4/d5/dae/tutorial_aruco_detection.html](https://docs.opencv.org/3.4/d5/dae/tutorial_aruco_detection.html)

![](https://github.com/alu0101244488/Interfaces-Inteligentes-AR/blob/main/img/basededatos.png?raw=true)

Hay que tener en cuenta que los markers deben de encontrarse porque si no puede darnos el siguiente error.

![error]()

Una vez procesados nos dirá cual es la calidad de nuestro marker.

Después de esto descargamos la base de datos y la importamos a unity de la misma manera que importamos vuforia.



### Entorno Unity

En este caso se emplea la versión 2019.4.32f1 de Unity y Vuforia 9.8.11. Lo primero es descargar vuforia desde la página web (habiendose creado una cuenta previamente) y lo importamos a unity como un custom package (Assests > import package > custom packages).

Una vez importado, eliminamos la cámara de la escena y colocamos la ARcamera. Podemos tambien añadir el image target como hijo de ARcamera. Ahora dentro la ARcamera, en el campo de licencia colocamos el código que obtenemos de la licencia que hemos creado.

Luego nos dirigimos a image target y elegimos la base de datos para nuestros targes.


El último paso es importar algún modelo 3d y colocarlo como hijo de image target en la escena.

Una vez hecho estos pasos, cambiamos la plataforma de desarrollo a android y pulsamos en build para generar la apk y poder así instalar la apk en nuestro dispositivo.

![entorno]()

### Ejecución en dispositivo móvil

![ejecucion]()



