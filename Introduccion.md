# Descripcion Del Dominio

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
### Consideraciones sobre el dominio

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
# Objetivo del Producto

Gestionar la consulta y publicación de reseñas de videojuegos pertenecientes a Steam, permitiendo a los usuarios autenticarse mediante su cuenta de Steam, consultar información sobre videojuegos, conocer las opiniones de otros usuarios y registrar sus propias valoraciones junto con información sobre su experiencia de juego.
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

- Consultas a Steam: El tiempo de sincronización con la API de Steam para obtener la biblioteca y horas de juego del usuario no debe superar los 5 segundos
    
- Autenticación externa: El inicio de sesión debe realizarse exclusivamente a través del protocolo oficial de autenticación de Steam (OpenID), sin almacenar contraseñas de usuarios en la base de datos propia.
    
- Control de inactividad: Las sesiones de usuario autenticadas deben expirar automáticamente tras 30 minutos de inactividad.
    
- Carga e Ingesta de Datos: El diseño de la base de datos debe permitir actualizar o alimentar el catálogo desde el conjunto de datos de videojuegos de forma eficiente sin requerir la detención del servicio.
    
- Compatibilidad de navegadores: La plataforma debe ser compatible con las dos últimas versiones estables de los principales navegadores (Chrome, Firefox, Edge, Safari).
    
- Tolerancia a fallos (API de Steam): Si la API externa de Steam no se encuentra disponible o excede el tiempo de respuesta el sistema debe permitir al usuario seguir navegando por el catálogo y las reseñas locales, presentando un mensaje sobre la indisponibilidad de la biblioteca
    
- Diseño responsivo: La interfaz debe adaptar su maquetación automáticamente identificando la resolución de la pantalla de dispositivos móviles, tablets y computadoras de escritorio
# Reglas de Negocio

| N.º de RN | Regla de Negocio                             | Descripción                                                                                                                                                                                          |
| --------- | -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RN01**  | **Identificación mediante Steam**            | Para poder acceder a la plataforma, el usuario deberá poseer una cuenta válida de Steam y deberá identificarse mediante ella                                                                         |
| **RN02**  | **Identificación y relación de videojuegos** | Para poder gestionar y relacionar la información de los videojuegos con la información proveniente de Steam, se deberá utilizar el AppID único correspondiente a cada videojuego                     |
| **RN03**  | **Valoración de las reseñas**                | Para poder publicar una reseña, el usuario deberá ingresar una valoración comprendida entre una y cinco estrellas                                                                                    |
| **RN04**  | **Asociación de las reseñas**                | Cada reseña deberá estar asociada a un único usuario y a un único videojuego                                                                                                                         |
| **RN05**  | **Información obligatoria de las reseñas**   | Para poder publicar una reseña, el usuario deberá ingresar un comentario y el sistema deberá registrar la fecha en que fue realizada                                                                 |
| **RN06**  | **Registro de horas de juego**               | Para poder publicar una reseña, el sistema deberá registrar la cantidad de horas de juego que posea el usuario sobre el videojuego reseñado                                                          |
| **RN07**  | **Reseña única por videojuego**              | Para poder publicar una reseña sobre un videojuego, el usuario no deberá poseer otra reseña activa asociada al mismo videojuego                                                                      |
| **RN08**  | **Administración de reseñas propias**        | Para poder modificar o eliminar una reseña, el usuario deberá ser propietario de la misma                                                                                                            |
| **RN09**  | **Consulta de perfiles de usuarios**         | Los perfiles y el historial de reseñas de otros usuarios deberán poder consultarse únicamente con fines informativos, sin permitir la modificación de sus datos o reseñas                            |
| **RN10**  | **Relación entre videojuegos y categorías**  | Un videojuego podrá estar asociado a múltiples categorías y una misma categoría podrá estar asociada a múltiples videojuegos                                                                         |
| **RN11**  | **Relación entre videojuegos y etiquetas**   | Un videojuego podrá estar asociado a múltiples etiquetas y una misma etiqueta podrá estar asociada a múltiples videojuegos                                                                           |
| **RN12**  | **Información del catálogo**                 | La información descriptiva, las categorías y las etiquetas de los videojuegos deberán obtenerse de la fuente de datos utilizada para alimentar el catálogo                                           |
| **RN13**  | **Inmutabilidad de categorías y etiquetas**  | Los usuarios no podrán modificar manualmente las categorías ni las etiquetas asociadas a los videojuegos                                                                                             |
| **RN14**  | **Inmutabilidad de información descriptiva** | Los usuarios no podrán modificar la información descriptiva de los videojuegos                                                                                                                       |
| **RN15**  | **Posesión de videojuego**                   | Para poder publicar una reseña sobre un videojuego, el usuario deberá contar con una copia del mismo en la su biblioteca de Steam y poseer un tiempo de juego igual o mayor a 0.1 horas registradas. |
|           |                                              |                                                                                                                                                                                                      |
