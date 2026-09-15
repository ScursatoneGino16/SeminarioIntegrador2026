# Introducción
## Descripción del dominio

La plataforma consiste en una aplicación web orientada a la consulta y publicación de reseñas sobre videojuegos pertenecientes a Steam. El acceso está destinado exclusivamente a usuarios que posean una cuenta de Steam, la cual será utilizada para identificar a cada persona dentro de la plataforma mediante el mecanismo de autenticación proporcionado por Steam. A partir de esta autenticación, el sistema obtiene el identificador único del usuario, denominado SteamID, que permite reconocerlo dentro de la aplicación y asociar a su cuenta la información y las acciones que realice en la plataforma.

Una vez autenticado, el usuario podrá consultar el catálogo de videojuegos disponible en la plataforma y acceder a información descriptiva de cada uno de ellos, incluyendo su nombre, descripción, portada, categorías y etiquetas. Los videojuegos se encuentran identificados mediante el AppID, identificador único utilizado por Steam, que permite relacionar la información de los videojuegos gestionada por la plataforma con la información obtenida desde Steam.

La plataforma permitirá a los usuarios registrar reseñas para videojuegos que forman parte de su biblioteca de Steam y consultar reseñas de otros usuarios pertenecientes o no a videojuegos de su pertenencia. Como información adicional se puede conocer la cantidad de horas de juego registradas para cada videojuego. Para acceder a esta información, el usuario deberá mantener pública su biblioteca de Steam. Los datos correspondientes a la biblioteca y actividad de juego serán obtenidos desde Steam y relacionados con los videojuegos del catálogo mediante su AppID.

El objetivo principal de la plataforma será permitir que los usuarios compartan sus opiniones sobre los videojuegos mediante la publicación de reseñas. Cada reseña estará asociada a un único usuario y a un único videojuego, y contendrá una valoración de entre una y cinco estrellas, un comentario de hasta 1.200 caracteres y la fecha de publicación. Al momento de registrar una reseña, el sistema obtendrá automáticamente desde Steam la cantidad de horas de juego que el usuario posea sobre el videojuego y almacenará dicho valor correspondiente al momento de publicación de la reseña, con el propósito de brindar contexto sobre la experiencia del usuario.

Los usuarios podrán crear, modificar y eliminar sus propias reseñas, mientras que las reseñas publicadas por otros usuarios podrán ser consultadas desde la página correspondiente a cada videojuego. El contenido de las reseñas será de libre expresión y la plataforma no contempla mecanismos de censura, moderación automática ni filtrado del contenido textual publicado por los usuarios. El límite de 1.200 caracteres constituye únicamente una restricción de extensión del contenido.

La plataforma permitirá a los usuarios expresar su valoración sobre las reseñas publicadas por otros mediante las opciones de "Me gusta" y "No me gusta". Asimismo, los usuarios podrán utilizar diferentes reacciones mediante emojis para expresar distintas opiniones o reacciones frente al contenido de una reseña. Estas interacciones están asociadas al usuario y a la reseña correspondiente.

La cantidad de "Me gusta" recibidos por cada reseña será utilizada para determinar su posición dentro de la página del videojuego. Las reseñas serán ordenadas de forma descendente según la cantidad de "Me gusta" obtenidos, permitiendo que aquellas que hayan sido mejor valoradas por la comunidad tengan mayor visibilidad.

La plataforma también permitirá consultar los perfiles de otros usuarios y visualizar el historial de reseñas que hayan publicado. Esta consulta tendrá carácter informativo y no contemplará mecanismos de comunicación directa entre usuarios, como sistemas de amigos, seguidores, mensajería privada o chat.

El catálogo de videojuegos permitirá realizar búsquedas y aplicar filtros mediante diferentes criterios, incluyendo el nombre del videojuego, sus categorías y sus etiquetas. Un videojuego podrá estar asociado a múltiples categorías y etiquetas, mientras que una misma categoría o etiqueta podrá estar asociada a múltiples videojuegos.

La información descriptiva de los videojuegos, sus categorías y sus etiquetas será obtenida a partir de un conjunto de datos utilizado para alimentar el catálogo de la aplicación. Las relaciones entre videojuegos, categorías y etiquetas serán gestionadas internamente por el sistema para permitir la consulta y el filtrado de los videojuegos.

La información relacionada con la identidad, biblioteca y actividad de juego de los usuarios será obtenida desde Steam. La información proveniente de Steam y la información gestionada por la propia plataforma se relacionarán mediante los identificadores proporcionados por Steam, principalmente el SteamID para identificar a los usuarios y el AppID para identificar los videojuegos.

## Objetivos del Proyecto

Gestionar la consulta y publicación de reseñas de videojuegos pertenecientes a Steam, permitiendo a los usuarios autenticarse mediante su cuenta de Steam, consultar información sobre videojuegos, conocer las opiniones de otros usuarios y registrar sus propias valoraciones junto con información sobre su experiencia de juego.

## Alcances del Proyecto

Para simplificar el problema y acotar el alcance del proyecto, no se tendrán en cuenta:

- El registro de usuarios mediante credenciales propias de la aplicación, ya que la autenticación se realizará exclusivamente mediante cuentas de Steam.
    
- La integración con plataformas de distribución de videojuegos diferentes de Steam.
    
- La compra, venta, descarga o instalación de videojuegos.
    
- La gestión de pagos relacionados con la compra de videojuegos o cualquier otro servicio.
    
- La gestión de información relacionada con el funcionamiento interno de los videojuegos.
    
- La gestión o registro de componentes de hardware de los usuarios.
    
- La administración de galerías de imágenes, capturas de pantalla o contenido audiovisual propio.
    
- La reproducción o almacenamiento de videos dentro de la aplicación.
    
- La gestión de amigos, seguidores o contactos entre usuarios.
    
- La mensajería privada y el chat entre usuarios.
    
- La implementación de notificaciones de carácter social.
    
- La publicación de contenido diferente de las reseñas de videojuegos.
    
- La edición o modificación de reseñas pertenecientes a otros usuarios.
    
- La modificación por parte de los usuarios de la información descriptiva de los videojuegos.
    
- La modificación manual de categorías y etiquetas por parte de los usuarios.
    
- La implementación de sistemas de recomendación personalizados.
    
- La gestión de comunidades, foros o espacios de discusión.
    
- La implementación de mecanismos de moderación, censura o filtrado automático del contenido publicado en las reseñas.

# Requerimientos

## Requerimientos Funcionales


- El sistema debe permitir el ingreso mediante la verificación de credenciales utilizando el mecanismo de autentificación de steam con el respectivo SteamID del usuario.  
	- Iniciar sesión mediante cuenta de Steam
	    
	- Consultar e identificar usuario mediante SteamID
	    
	- Consultar biblioteca de videojuegos del usuario desde Steam
	    
	- Consultar horas de juego por videojuego desde Steam
	    
	- Validar privacidad pública de la biblioteca del usuario en Steam

- El sistema debe permitir crear, ver, actualizar y eliminar una  reseña asociada a un videojuego a los usuarios.
	- Registrar Reseña
	    
	- Modificar Reseña
	    
	- Consultar Reseña
	    
	- Eliminar Reseña
	    
	- Organizar Reseña

- El sistema debe permitir crear, consultar, actualizar y eliminar una categoría
	- Consultar Categorías.

- El sistema deberá permitir consultar las etiquetas
	- Consultar Etiquetas.

- El sistema contempla consultar videojuegos mediante la AppID y permitir consultar un listado de los mismos
	- Consultar información de videojuego por AppID
	    
	- Consultar listado de videojuegos

## Requerimientos No Funcionales

|  N° | Nombre                                   | Descripción                                                                                                                                                                                                              | Características |  SPA   | Prioridad | Explicación                                                                                                                                                                                                                               |
| --: | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------- | :----: | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   1 | Tiempo de respuesta de Steam             | Las consultas realizadas a los servicios de Steam para obtener la biblioteca y las horas de juego de un usuario no deberán superar los 5 segundos.                                                                       | Performance     | **SI** | Alta      | La arquitectura deberá contemplar mecanismos de comunicación con servicios externos y control del tiempo de espera de las consultas para evitar que una demora de Steam bloquee el funcionamiento del sistema.                            |
|   2 | Autenticación mediante Steam             | El acceso al sistema deberá realizarse exclusivamente mediante el mecanismo oficial de autenticación de Steam. El sistema no deberá almacenar contraseñas de Steam.                                                      | Seguridad       | **SI** | Alta      | La arquitectura deberá incorporar un componente de autenticación externa y separar la gestión de identidad del sistema de las credenciales administradas por Steam.                                                                       |
|   3 | Expiración de sesiones por inactividad   | Las sesiones de usuarios autenticados deberán expirar luego de 30 minutos de inactividad.                                                                                                                                | Seguridad       | **SI** | Media     | La arquitectura deberá contemplar un mecanismo de gestión del estado de sesión que permita controlar su expiración por inactividad.                                                                                                       |
|   4 | Actualización del catálogo               | La incorporación y actualización de los datos del catálogo de juegos deberá poder realizarse sin interrumpir el funcionamiento normal del sistema.                                                                       | Disponibilidad  | **SI** | Media     | La arquitectura deberá contemplar un mecanismo de carga o actualización de datos independiente de las consultas de los usuarios, evitando que la actualización del catálogo bloquee el servicio.                                          |
|   5 | Compatibilidad con navegadores           | El sistema deberá ser compatible con las últimas dos versiones estables de Google Chrome, Mozilla Firefox, Microsoft Edge y Safari.                                                                                      | Compatibilidad  | **NO** | No Aplica | La compatibilidad con determinados navegadores no requiere una modificación estructural de la arquitectura del sistema.                                                                                                                   |
|   6 | Tolerancia a fallos de Steam             | Si los servicios de Steam no se encuentran disponibles o superan el tiempo máximo de respuesta establecido, los usuarios deberán poder continuar consultando el catálogo de juegos y las reseñas almacenadas localmente. | Disponibilidad  | **SI** | Alta      | La arquitectura deberá desacoplar las funcionalidades que dependen de Steam de aquellas que utilizan información almacenada localmente, permitiendo que el sistema continúe funcionando parcialmente ante una falla del servicio externo. |
|   7 | Diseño responsivo                        | La interfaz deberá adaptarse automáticamente a dispositivos de escritorio, tablets y teléfonos inteligentes.                                                                                                             | Usabilidad      | **NO** | No Aplica | El diseño responsivo afecta principalmente la implementación de la interfaz de usuario y no requiere una modificación estructural de la arquitectura del sistema.                                                                         |
|   8 | Integridad y consistencia de los datos   | El sistema deberá garantizar la integridad y consistencia de la información almacenada, evitando registros duplicados o relaciones inválidas entre usuarios, juegos y reseñas.                                           | Integridad      | **SI** | Alta      | La arquitectura de persistencia deberá contemplar mecanismos de integridad referencial y restricciones de datos que garanticen la consistencia de la información almacenada.                                                              |
|   9 | Control de autorización                  | El sistema deberá garantizar que cada usuario pueda modificar o eliminar únicamente sus propias reseñas y que las operaciones restringidas sean verificadas en el servidor.                                              | Seguridad       | **SI** | Alta      | La arquitectura deberá incorporar mecanismos de autorización en el servidor para controlar el acceso a las operaciones según la identidad del usuario autenticado.                                                                        |
|  10 | Persistencia histórica de horas de juego | Al momento de publicar una reseña, el sistema deberá almacenar las horas de juego obtenidas desde Steam correspondientes a ese momento. Este valor no deberá depender de consultas posteriores a Steam.                  | Persistencia    | **SI** | Alta      | El modelo de datos deberá contemplar el almacenamiento del tiempo de juego como parte de la reseña, permitiendo conservar el valor histórico independientemente de futuras modificaciones en Steam.                                       |
|  11 | Validación de datos                      | El sistema deberá validar los datos ingresados en las reseñas, permitiendo una valoración entre 1 y 5 estrellas y comentarios de hasta 1200 caracteres.                                                                  | Integridad      | **NO** | No Aplica | Las restricciones de los datos pueden resolverse mediante validaciones en la lógica de negocio y en la interfaz, sin requerir una decisión arquitectónica específica.                                                                     |

## Modelo de Requerimientos
Casos de uso

# Diseño

## Arquitectura General

### Vista de Diseño Global con Microservicios

![[Pasted image 20260915172845.png]]

### Vista Arquitectónica

![[Pasted image 20260915172817.png]]

## Modelo de Datos
### DER
![[Pasted image 20260915172049.png]]

## Mockup o Wireframe

Por verse

## Tecnologías Elegidas

Por verse