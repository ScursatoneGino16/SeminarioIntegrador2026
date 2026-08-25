# Descripcion Del Dominio

Una plataforma web desea brindar a usuarios de Steam la posibilidad de consultar información sobre videojuegos y compartir sus opiniones mediante reseñas. El acceso a la plataforma se encuentra destinado exclusivamente a personas que posean una cuenta de Steam, utilizando dicha cuenta para identificarse dentro del sistema.

Una vez autenticado, el usuario podrá consultar información relacionada con los videojuegos disponibles en el catálogo de la plataforma y, cuando corresponda, acceder a información sobre los juegos pertenecientes a su biblioteca de Steam y las horas de juego registradas para cada uno de ellos.

Los videojuegos se encuentran identificados mediante un código único utilizado por Steam denominado AppID. Para cada videojuego se dispone de información descriptiva como su nombre, descripción y portada, además de las categorías y etiquetas asociadas al mismo. Esta información permitirá realizar consultas y aplicar diferentes filtros dentro del catálogo. La portada del videojuego será utilizada como referencia visual dentro de la aplicación.

La plataforma permitirá a los usuarios publicar reseñas asociadas a los videojuegos. Cada reseña estará vinculada a un único usuario y a un único videojuego, y contendrá una valoración de entre una y cinco estrellas, un comentario y la fecha en que fue realizada. Al momento de publicar una reseña también se registrará la cantidad de horas de juego que posee el usuario sobre dicho videojuego, con el objetivo de contextualizar su opinión de acuerdo con su experiencia real.

Los usuarios podrán consultar las reseñas realizadas por otros usuarios desde la ficha correspondiente a cada videojuego. Asimismo, podrán administrar sus propias reseñas, pudiendo crearlas, modificarlas y eliminarlas.

La plataforma permitirá consultar perfiles de otros usuarios y visualizar el historial de reseñas que hayan publicado. Esta consulta será únicamente informativa, sin contemplar mecanismos de interacción directa entre usuarios.

El catálogo de videojuegos permitirá realizar búsquedas y consultas mediante diferentes criterios, incluyendo el nombre del videojuego, sus categorías y sus etiquetas. Un videojuego puede estar asociado a múltiples categorías y etiquetas, y una misma categoría o etiqueta puede estar asociada a múltiples videojuegos.

La información descriptiva de los videojuegos, sus categorías y sus etiquetas será obtenida a partir de un conjunto de datos utilizado para alimentar el catálogo de la aplicación. Las relaciones entre videojuegos, categorías y etiquetas serán gestionadas internamente por el sistema para permitir la consulta y filtrado del catálogo.

La información relacionada con la biblioteca y la actividad de juego de los usuarios será obtenida desde Steam. La información proveniente de Steam y la información gestionada por la propia plataforma se relacionarán mediante el identificador AppID de cada videojuego.

### Consideraciones sobre el dominio

Para simplificar el problema y acotar el alcance del proyecto, no se tendrán en cuenta:

- La integración con plataformas de distribución de videojuegos distintas de 
- Steam.
    
- La compra, venta, descarga o instalación de videojuegos.
    
- La gestión de información propia del funcionamiento interno de los videojuegos.
    
- La administración de galerías de imágenes o capturas de pantalla de los videojuegos.
	
- Los sistemas de amigos, seguidores o contactos entre usuarios.
    
- La mensajería privada y el chat entre usuarios.
    
- Las notificaciones sociales.
    
- La publicación de contenido diferente de las reseñas de videojuegos.
    
- Los sistemas de recomendación personalizados.
    
- La gestión de comunidades o foros.
    
- La modificación de la información descriptiva de los videojuegos por parte de los usuarios.
    
- La modificación manual de categorías y etiquetas por parte de los usuarios.

# Objetivo del Producto

Gestionar la consulta y publicación de reseñas de videojuegos pertenecientes a Steam, permitiendo a los usuarios autenticarse mediante su cuenta de Steam, consultar información sobre videojuegos, conocer las opiniones de otros usuarios y registrar sus propias valoraciones junto con información sobre su experiencia de juego.

# Alcances

- **Administrar Videojuegos**
	
- **Gestionar Usuarios**
    
- **Gestionar Biblioteca**
    
- **Gestionar Reseñas**
    
- **Gestionar Catálogo**
    
- **Gestionar Reseñas**
    
- **Gestionar Perfiles**

## No contempla

- Registro de usuarios mediante usuario y contraseña propios de la aplicación.
    
- Integración con plataformas diferentes de Steam.
    
- Compra o venta de videojuegos.
    
- Gestión de pagos.
    
- Descarga o instalación de videojuegos.
    
- Gestión de amigos o seguidores.
    
- Mensajería privada o chat.
    
- Sistema de notificaciones sociales.
    
- Publicación de contenido diferente de las reseñas.
    
- Edición de reseñas pertenecientes a otros usuarios.
    
- Modificación por parte de los usuarios de la información descriptiva de los videojuegos.
    
- Administración de galerías de imágenes o capturas de pantalla.
    
- Reproducción o almacenamiento de videos dentro de la aplicación.
    
- Gestión de contenido audiovisual propio.
    
- Sistemas de recomendación personalizados.
    
- Gestión de comunidades o foros.
    
- Registro de componentes de hardware

# Reglas de Negocio

|Nº|Nombre|Regla de Negocio – Descripción|
|--:|---|---|
|1|Identificación del Usuario|Para acceder a las funcionalidades de la plataforma, el usuario debe autenticarse mediante una cuenta válida de Steam.|
|2|Identificación del Videojuego|Cada videojuego se identifica mediante un AppID único correspondiente al identificador utilizado por Steam.|
|3|Biblioteca del Usuario|La biblioteca de videojuegos y las horas de juego del usuario son obtenidas a partir de la información disponible en Steam.|
|4|Publicación de Reseñas|Una reseña debe estar asociada a un único usuario y a un único videojuego.|
|5|Valoración de la Reseña|Toda reseña debe contener una valoración comprendida entre una y cinco estrellas.|
|6|Experiencia de Juego|Al momento de publicar una reseña se debe registrar la cantidad de horas de juego que posee el usuario sobre el videojuego reseñado.|
|7|Reseña por Videojuego|Un usuario puede poseer como máximo una reseña activa por videojuego. Dicha reseña puede ser modificada posteriormente por su autor.|
|8|Modificación de Reseñas|Un usuario únicamente puede modificar las reseñas que le pertenecen.|
|9|Eliminación de Reseñas|Un usuario únicamente puede eliminar las reseñas que le pertenecen.|
|10|Consulta de Reseñas|Las reseñas publicadas pueden ser consultadas por los usuarios desde la información correspondiente al videojuego.|
|11|Perfil de Usuario|Los perfiles de otros usuarios pueden ser consultados únicamente en modo de lectura, sin posibilidad de modificar sus datos o reseñas.|
|12|Catálogo de Videojuegos|Los videojuegos disponibles para consulta pertenecen al catálogo administrado por la plataforma y se identifican mediante su AppID.|
|13|Categorías y Etiquetas|Un videojuego puede estar asociado a múltiples categorías y etiquetas, y una misma categoría o etiqueta puede estar asociada a múltiples videojuegos.|
|14|Información del Catálogo|La información descriptiva, categorías y etiquetas de los videojuegos se obtiene de la fuente de datos utilizada para alimentar el catálogo y no puede ser modificada por los usuarios.|
|15|Portada del Videojuego|Cada videojuego posee una referencia a su portada, utilizada como representación visual dentro de la aplicación. No se contempla la gestión de galerías de imágenes.|
|16|Contenido Audiovisual|El sistema no almacena ni administra contenido audiovisual de los videojuegos. Cuando corresponda, el usuario podrá acceder a contenido externo mediante plataformas como YouTube.|
|17|Información de Steam|La información obtenida desde Steam sobre la actividad del usuario no puede ser modificada directamente desde la aplicación.|
|18|Contexto de la Reseña|La cantidad de horas de juego registrada en una reseña corresponde a las horas que poseía el usuario en el momento de su publicación y no debe actualizarse automáticamente con el paso del tiempo.|
## Requerimientos No Funcionales
- **Consultas a Steam:** El tiempo de sincronización con la API de Steam para obtener la biblioteca y horas de juego del usuario no debe superar los 5 segundos
- **Autenticación externa:** El inicio de sesión debe realizarse exclusivamente a través del protocolo oficial de autenticación de Steam (OpenID), sin almacenar contraseñas de usuarios en la base de datos propia.
- **Control de inactividad:** Las sesiones de usuario autenticadas deben expirar automáticamente tras 30 minutos de inactividad.
- **Carga e Ingesta de Datos:** El diseño de la base de datos debe permitir actualizar o alimentar el catálogo desde el conjunto de datos de videojuegos de forma eficiente sin requerir la detención del servicio.
- **Compatibilidad de navegadores:** La plataforma debe ser compatible con las dos últimas versiones estables de los principales navegadores (Chrome, Firefox, Edge, Safari).