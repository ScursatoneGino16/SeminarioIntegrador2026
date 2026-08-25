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

- El registro de usuarios mediante credenciales propias de la aplicación, ya que la autenticación se realizará exclusivamente mediante cuentas de Steam
	
- La integración con plataformas de distribución de videojuegos diferentes de Steam
	
- La compra, venta, descarga o instalación de videojuegos
	
- La gestión de pagos relacionados con la compra de videojuegos o cualquier otro servicio
	
- La gestión de información relacionada con el funcionamiento interno de los videojuegos
	
- La gestión o registro de componentes de hardware de los usuarios
	
- La administración de galerías de imágenes, capturas de pantalla o contenido audiovisual propio
	
- La reproducción o almacenamiento de videos dentro de la aplicación
	
- La gestión de amigos, seguidores o contactos entre usuarios
	
- La mensajería privada y el chat entre usuarios
	
- La implementación de notificaciones de carácter social
	
- La publicación de contenido diferente de las reseñas de videojuegos
	
- La edición o modificación de reseñas pertenecientes a otros usuarios
	
- La modificación por parte de los usuarios de la información descriptiva de los videojuegos
	
- La modificación manual de categorías y etiquetas por parte de los usuarios
	
- La implementación de sistemas de recomendación personalizados
	
- La gestión de comunidades, foros o espacios de discusión

# Objetivo del Producto

Gestionar la consulta y publicación de reseñas de videojuegos pertenecientes a Steam, permitiendo a los usuarios autenticarse mediante su cuenta de Steam, consultar información sobre videojuegos, conocer las opiniones de otros usuarios y registrar sus propias valoraciones junto con información sobre su experiencia de juego.

# Alcances Generales

- Administrar Videojuego
	
- Administrar Reseñas
	
- Administrar Usuario
	
- Administrar Categoria
	
- Administrar Etiqueta
	
- Gestionar autenticación de usuarios mediante Steam
	
- Gestionar consulta de videojuegos
	
- Gestionar búsqueda y filtrado de videojuegos
	
- Gestionar biblioteca y actividad de juego
	
- Gestionar reseñas de videojuegos
	
- Gestionar consulta de perfiles e historial de reseñas
	
- Gestionar integración con Steam

# Alcances Detallados

* **Administrar Videojuego**
	- Consultar [AppID, NombreVideojuego, Descripción]
* **Administrar Reseñas**
	* Registrar [Usuario, Videojuego, Valoración, Comentario, Fecha, Horas de juego]
	- Modificar [Valoración, Comentario]
	- Eliminar [*]
	- Consultar [Usuario, Videojuego, Valoración, Comentario, Fecha, Horas de juego]
* **Administrar Usuario**
	* Consultar [SteamID, NombreUsuario]
* **Administrar Categoria**
	* Consultar [NombreCategoria]
* **Administrar Etiqueta**
	* Consultar [NombreEtiqueta]
* **Gestionar autenticación de usuarios mediante Steam**
	* Iniciar sesión mediante una cuenta de Steam
	- Verificar identidad del usuario
	- Identificar usuario mediante Steam
	- Permitir acceso a la plataforma
* **Gestionar consulta de videojuegos**
	* Buscar videojuegos por nombre
	- Consultar información del videojuego
	- Consultar información mediante AppID
	- Visualizar nombre
	- Visualizar descripción
	- Visualizar categorías
	- Visualizar etiquetas
* **Gestionar búsqueda y filtrado de videojuegos**
	* Ingresar nombre del videojuego
	- Seleccionar categoría
	- Seleccionar etiqueta
	- Aplicar criterios de búsqueda
	- Visualizar videojuegos que coincidan con los criterios seleccionados
* **Gestionar biblioteca y actividad de juego**
	* Consultar biblioteca de Steam
	- Consultar videojuegos pertenecientes a la biblioteca
	- Consultar horas de juego
	- Obtener información de actividad de juego desde Steam
	- Relacionar información mediante AppID
* **Gestionar reseñas de videojuegos**
	* Seleccionar videojuego
	- Ingresar valoración
	- Ingresar comentario
	- Registrar horas de juego
	- Registrar fecha de publicación
	- Publicar reseña
	- Consultar reseñas de un videojuego
	- Modificar reseña propia
	- Eliminar reseña propia
* **Gestionar consulta de perfiles e historial de reseñas**
	* Consultar perfil de usuario
	- Consultar historial de reseñas
	- Consultar reseñas publicadas por un usuario
	- Visualizar información de las reseñas
* **Gestionar integración con Steam**
	* Obtener información de la biblioteca del usuario
	- Obtener información sobre las horas de juego
	- Relacionar información de Steam con los videojuegos mediante AppID

# Reglas de Negocio

| N.º de RN | Regla de Negocio                             | Descripción                                                                                                                                                                      |
| --------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RN01**  | **Identificación mediante Steam**            | Para poder acceder a la plataforma, el usuario deberá poseer una cuenta válida de Steam y deberá identificarse mediante ella                                                     |
| **RN02**  | **Identificación y relación de videojuegos** | Para poder gestionar y relacionar la información de los videojuegos con la información proveniente de Steam, se deberá utilizar el AppID único correspondiente a cada videojuego |
| **RN03**  | **Valoración de las reseñas**                | Para poder publicar una reseña, el usuario deberá ingresar una valoración comprendida entre una y cinco estrellas                                                                |
| **RN04**  | **Asociación de las reseñas**                | Cada reseña deberá estar asociada a un único usuario y a un único videojuego                                                                                                     |
| **RN05**  | **Información obligatoria de las reseñas**   | Para poder publicar una reseña, el usuario deberá ingresar un comentario y el sistema deberá registrar la fecha en que fue realizada                                             |
| **RN06**  | **Registro de horas de juego**               | Para poder publicar una reseña, el sistema deberá registrar la cantidad de horas de juego que posea el usuario sobre el videojuego reseñado                                      |
| **RN07**  | **Reseña única por videojuego**              | Para poder publicar una reseña sobre un videojuego, el usuario no deberá poseer otra reseña activa asociada al mismo videojuego                                                  |
| **RN08**  | **Administración de reseñas propias**        | Para poder modificar o eliminar una reseña, el usuario deberá ser propietario de la misma                                                                                        |
| **RN09**  | **Consulta de perfiles de usuarios**         | Los perfiles y el historial de reseñas de otros usuarios deberán poder consultarse únicamente con fines informativos, sin permitir la modificación de sus datos o reseñas        |
| **RN10**  | **Relación entre videojuegos y categorías**  | Un videojuego podrá estar asociado a múltiples categorías y una misma categoría podrá estar asociada a múltiples videojuegos                                                     |
| **RN11**  | **Relación entre videojuegos y etiquetas**   | Un videojuego podrá estar asociado a múltiples etiquetas y una misma etiqueta podrá estar asociada a múltiples videojuegos                                                       |
| **RN12**  | **Información del catálogo**                 | La información descriptiva, las categorías y las etiquetas de los videojuegos deberán obtenerse de la fuente de datos utilizada para alimentar el catálogo                       |
| **RN13**  | **Inmutabilidad de categorías y etiquetas**  | Los usuarios no podrán modificar manualmente las categorías ni las etiquetas asociadas a los videojuegos                                                                         |
| **RN14**  | **Inmutabilidad de información descriptiva** | Los usuarios no podrán modificar la información descriptiva de los videojuegos                                                                                                   |
## Requerimientos No Funcionales
- **Consultas a Steam:** El tiempo de sincronización con la API de Steam para obtener la biblioteca y horas de juego del usuario no debe superar los 5 segundos
- **Autenticación externa:** El inicio de sesión debe realizarse exclusivamente a través del protocolo oficial de autenticación de Steam (OpenID), sin almacenar contraseñas de usuarios en la base de datos propia.
- **Control de inactividad:** Las sesiones de usuario autenticadas deben expirar automáticamente tras 30 minutos de inactividad.
- **Carga e Ingesta de Datos:** El diseño de la base de datos debe permitir actualizar o alimentar el catálogo desde el conjunto de datos de videojuegos de forma eficiente sin requerir la detención del servicio.
- **Compatibilidad de navegadores:** La plataforma debe ser compatible con las dos últimas versiones estables de los principales navegadores (Chrome, Firefox, Edge, Safari).