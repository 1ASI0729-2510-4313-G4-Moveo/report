<style>
  body {
    font-family: 'Times New Roman', sans-serif;
    text-align: justify;
    font-size: 12px;
    margin-left: 2em;
    margin-right: 2em;
    line-height: 2;
  }
  
  p {
    text-indent: 2em; /* Sangría en el primer renglón de cada párrafo */
  }

  h1 {
    margin-left: 0; /* No aplica sangría para el título principal */
  }

  h2 {
    margin-left: 0; /* No aplica sangría para subtítulos de nivel 2 */
  }

  h3 {
    margin-left: 2em; /* Aplica una sangría de 2em para subtítulos de nivel 3 */
  }

  h4 {
    margin-left: 4em; /* Aplica una sangría de 4em para subtítulos de nivel 4 */
  }
</style>

# Capítulo III: Requirements Specification
## 3.1. To-Be Scenario Mapping

- **Segmento 1: Trabajador urbano**

<p align="center">
  <a>
    <img src="assets/chapter03/to-be/To-Be%20Trabajador.png" style="width:1000px; height:auto;" alt="">
  </a>
</p>


- **Segmento 2: Proveedor de auto**
<p align="center">
  <a>
    <img src="assets/chapter03/to-be/To-Be%20Proveedor.png" style="width:1000px; height:auto;" alt="">
  </a>
</p>

## 3.2. User Stories
### Epics
| **Epic ID**|**Título**| **Descripción**|
|------------|---------|----------------|
|**EP01**|**Gestión y Registro de Usuarios**|**Como invitado trabajador, quiero poder registrarme y autenticarme en la plataforma para tener acceso seguro a las funcionalidades de Moveo.** |
|**EP02**|**Gestión de Autos para Proveedores**|**Como invitado proveedor, quiero poder registrar, listar y administrar mis autos disponibles para alquiler, para así generar ingresos cuando no los utilice.** |
| **EP03**|**Solicitud y Reserva de Vehículos**| **Como invitado trabajador, quiero poder buscar, reservar y desbloquear autos desde la aplicación, para movilizarme sin intermediarios.** |
|**EP04**|**Visualización y Selección de Estacionamientos**|**Como invitado trabajador, quiero visualizar en un mapa los estacionamientos disponibles para programar dónde recoger y dejar el vehículo de manera conveniente.** |
|**EP05**|**Creación de Landing Page**|**Como visitante trabajador, quiero conocer la propuesta de valor de Moveo, cómo funciona y qué beneficios me ofrece tanto como proveedor o como cliente, desde la web oficial** |
### User Stories
|**Epic / Story ID**|**Título**|**Descripción**|**Criterios de Aceptación**|**Relacionado con (Epic ID)**|
|--|-| --| --|-- |
|US01|Registro de nuevos usuarios|Como visitante del segmento del segmento trabajadores, quiero registrarme para acceder al servicio de alquiler de autos.|**Scenario 1:<br>Given** que soy un visitante del segmento y deseo alquilar un auto<br>**When** completo el formulario de registro correctamente<br>**Then** la plataforma crea mi cuenta y me notifica que el registro fue exitoso<br>**Scenario 2:<br>Given** que soy un visitante del segmento del segmento trabajadores y no completo todos los campos obligatorios<br>**When** intentó finalizar el registro<br>**Then** la plataforma me muestra mensajes indicando los campos faltantes.|EP01|
|US02|Inicio de sesión seguro|Como visitante del segmento trabajadores, quiero iniciar sesión de manera segura para usar la plataforma.|**Scenario 1<br>Given** que soy un visitante del segmento trabajadores registrado<br>**When** ingreso mis credenciales correctas<br>**Then** puedo acceder a la plataforma<br>**Scenario 2:<br>Given** que ingresó credenciales incorrectas<br>**When** intento iniciar sesión<br>**Then** recibo un mensaje de error indicando que los datos no son válidos.|EP01|
|US03|Registro de autos por proveedor|Como visitante del segmento de proveedores, quiero registrar mis autos para ponerlos en alquiler.|**Scenario 1:**<br>**Given** que soy un visitante del segmento proveedores y tengo un auto disponible<br>**When** completo los datos del vehículo y los envió<br>**Then** el auto queda disponible en la plataforma<br>**Scenario 2:**<br>**Given** que soy un visitante del segmento proveedoresy omito datos obligatorios<br>**When** intento registrar el auto<br>**Then** el sistema me alerta sobre los campos incompletos|EP02|
|US04|Visualización de autos disponibles|Como visitante del segmento trabajadores, quiero visualizar los autos disponibles en un mapa.|**Scenario 1:<br>Given** que soy un visitante del segmento trabajadores autenticado<br>**When** accedo a la sección de mapa<br>**Then** puedo visualizar los autos disponibles en tiempo real.<br>**Scenario 2:<br>Given** que me encuentro en una zona sin autos disponibles<br>**When** ingreso al mapa<br>**Then** la plataforma me notifica que no hay disponibilidad en esa ubicación.|EP03|
|US05|Reserva de auto|Como visitante del segmento trabajadores, quiero reservar un auto para asegurar su disponibilidad.|**Scenario 1:**<br>**Given** que soy un visitante del segmento trabajadores y encuentro un auto disponible<br>**When** realizó la reserva<br>**Then** recibo confirmación de que el auto ha sido apartado.<br>**Scenario 2:**<br>**Given** que otro invitado ya reservó el auto antes que yo<br>**When** intento hacer la reserva<br>**Then** recibo una notificación indicando que el auto ya no está disponible|EP04|
|US06|Implementación de Call to Action|Como visitante del segmento trabajadores, quiero encontrar botones de acción clara para facilitar la interacción.|**Scenario 1:**<br>**Given** accedo a la Landing Page<br>**When** visualizo las secciones principales<br>**Then** encuentro al menos un Call to Action en cada sección clave.<br>**Scenario 2:<br>Given** que accedo a la Landing Page desde un dispositivo móvil<br>**When** navego hacia abajo<br>**Then** los Call to Action deben ser claramente visibles y accesibles sin interferir con la navegación.</p>|EP05|
|US07|Creación de Footer Informativo|Como visitante del segmento (trabajadores), quiero encontrar en el footer información sobre contacto, términos y condiciones y enlaces sociales.|**Scenario 1:<br>Given** que estoy en cualquier sección de la web<br>**When** hago scroll hasta abajo<br>**Then** encuentro un footer con datos de contacto y enlaces legales<br>**Scenario 2:<br>Given** que visualizo el footer en distintos dispositivos<br>**When** cambio de escritorio a móvil<br>**Then** la información sigue siendo legible y funcional (responsive).|EP05|
|US08|Sección de Testimonios de Usuarios|Como visitante del segmento trabajadores, quiero visualizar opiniones y experiencias de otros usuarios para confiar en el servicio antes de usarlo.|**Scenario 1:**<br>**Given** que accedo a la sección de testimonios<br>**When** navego por las opiniones<br>**Then** visualizo testimonios reales con nombre y calificación.<br>**Scenario 2:**<br>**Given** que reviso varios testimonios<br>**When** regreso en otro momento<br>**Then** el orden de testimonios puede variar (rotación aleatoria o según relevancia)|EP05|
|US09|Sección de Preguntas Frecuentes (FAQ)|Como visitante del segmento trabajadores, quiero consultar una sección de preguntas frecuentes para resolver mis dudas sin contacto humano.|**Scenario 1:**<br>**Given** que accedo a la Landing Page<br>**When** ingreso a la sección de FAQ,<br>**Then** puedo visualizar y expandir preguntas y respuestas claras.<br>**Scenario 2:**<br>**Given** que realizo una búsqueda en la FAQ<br>**When** escribo palabras clave en el buscador<br>**Then** se filtran las preguntas relacionadas de forma automática|EP05|
|US10|Visualización de estacionamientos en el mapa|Como usuario, quiero ver en el mapa los estacionamientos disponibles cercanos para poder elegir uno al recibir el auto|**Scenario 1:** <br>**Given** que el invitado ha iniciado sesión<br>**When** accede al mapa de estacionamientos<br>**Then** el sistema muestra marcadores de ubicación con disponibilidad<br>**Scenario 2:** <br>**Given** que el invitado selecciona un estacionamiento<br>**When** confirma la reserva<br>**Then** el sistema le asigna el punto de entrega y lo bloquea para otros usuarios|EP02|
|US11|Desbloqueo del auto mediante la app|Como usuario, quiero desbloquear el auto desde la aplicación sin necesidad de contacto físico o intermediarios|**Scenario 1:**<br>**Given** que el invitado ha llegado al estacionamiento correcto<br>**When** abre la app y confirma la ubicación <br>**Then** el sistema habilita el botón de desbloqueo<br>**Scenario 2:**<br>**Given** que el invitado pulsa el botón de desbloqueo<br>**When** el sistema valida la reserva <br>**Then** se libera el seguro electrónico y se habilita el acceso al vehículo|EP03|
|US12|Verificación de mantenimiento del vehículo|Como usuario, quiero recibir notificaciones sobre cuándo es necesario realizar mantenimiento a mis vehículos en renta|**Scenario 1:** <br>**Given** que el auto alcanza el kilometraje límite configurado<br>**When** se registra en la plataforma<br>**Then** se envía una notificación automática al proveedor<br>**Scenario 2:** <br>**Given** que el proveedor recibe la notificación de mantenimiento<br>**When** accede a la app <br>**Then** puede marcar como "mantenimiento programado" para que el auto sea retirado de la disponibilidad temporalmente.|EP04|
|US13|Visualizar precios y tarifas|Como visitante del segmento objetivo trabajadores quisiera poder visualizar los precios y tarifas que ofrece la aplicación para saber si me conviene comprar sus servicios|**Scenario 1:** <br>**Given** que el visitante del segmento trabajadores accede a la landing page<br>**When** navega a la sección de precios<br>**Then** puede visualizar la lista actualizada de tarifas y modalidades disponibles<br>**Scenario 2:** <br>**Given** que el visitante del segmento trabajadores accede desde un dispositivo móvil<br>**When** carga la sección de precios<br>**Then** la información se muestra legible y correctamente adaptada|EP05|
|US14|Visualizar principales funciones|Como visitante del segmento objetivo de trabajadores y proveedores, quiero poder ver las funcionalidades que ofrece la aplicación para saber qué beneficio puedo tener|**Scenario 1:**<br>**Given** que el visitante del segmento trabajadores o proveedores accede a la landing page<br>**When** llega a la sección de funcionalidades<br>**Then** visualiza una lista clara y breve de las funciones principales de la aplicación<br>**Scenario 2:**<br>**Given** que la lista de funciones es extensa<br>**When** el visitante navega<br>**Then** puede acceder a detalles ampliados mediante enlaces o botones informativos|EP05|
|US15|Ver el nombre, logo y eslogan de la aplicación|Como visitante del segmento trabajadores y proveedores, quiero poder visualizar el nombre y eslogan de la aplicación para saber de qué se trata a primera vista |**Scenario 1:** <br>**Given** que el visitante accede a la landing page<br>**When** la página carga correctamente<br>**Then** puede visualizar el nombre, logo y eslogan de la aplicación en la cabecera<br>**Scenario 2:**<br>**Given** que el visitante accede desde un dispositivo móvil<br>**When** visualiza la cabecera<br>**Then** el nombre, logo y eslogan se adaptan y siguen siendo claramente legibles.</p>|EP05|
|US16|Visualizar el nombre del equipo |Como visitante del segmento trabajadores y proveedores, quiero poder visualizar el nombre del equipo que diseñó la aplicación para saber quién la creó y darle mis respetos|**Scenario 1:** <br>**Given** que el visitante accede al pie de página de la landing page<br>**When** la sección "Acerca del equipo" está disponible<br>**Then** puede visualizar el nombre del equipo responsable de la aplicación.<br>**Scenario 2:**<br>**Given** que el visitante quiere conocer más sobre el equipo<br>**When** hace clic sobre el nombre del equipo<br>**Then** es redirigido a una página de presentación o sección con detalles adicionales|EP05|
|US17|Sección de contacto|Como visitante del segmento trabajadores y proveedores, quiero poder contactar a la startup creadora de la app para notificar si hay algun error o si simplemente quiero hablar con ellos|**Scenario 1:**<br>**Given** que el visitante accede a la sección de contacto<br>**When** completa el formulario con sus datos y mensaje<br>**Then** recibe una confirmación visual de que su mensaje ha sido enviado correctamente<br>**Scenario 2:**<br>**Given** que el visitante deja campos obligatorios vacíos en el formulario de contacto<br>**When** intenta enviarlo <br>**Then** el sistema muestra un mensaje de error solicitando completar la información|EP05|
|US18|Landing Page Responsive|Como visitante del segmento trabajadores y proveedores, quiero entrar a la landing page desde mi movil y mi pc sin ningun problema para tener más flexibilidad al momento de registrarse|**Scenario 1:** <br>**Given** que el visitante accede desde un smartphone<br>**When** la landing page carga<br>**Then** la estructura y contenido se adaptan al tamaño de pantalla correctamente<br>**Scenario 2:**<br>**Given** que el visitante accede desde una computadora de escritorio<br>**When** la landing page se carga<br>**Then** todos los elementos visuales y botones se muestran correctamente alineados y accesibles|EP05|
|US19|Editar información de un vehículo|Como visitante del segmento proveedores, quiero actualizar datos de un vehículo (tarifa, descripción) para mantener la información al día.|**Scenario 1:**<br>**Given** que el invitado selecciona “Editar” en uno de sus vehículos<br>**When** modifica la tarifa y guarda los cambios<br>**Then** el sistema actualiza la información y muestra un mensaje de éxito<br>**Scenario 2:**<br>**Given** que intenta guardar con una tarifa no válida (p.ej. negativa)<br>**When** presiona “Guardar”<br>**Then** el sistema muestra validación de error en el campo de tarifa|EP02|
|US20|Desactivar vehículo de la plataforma|Como visitante del segmento proveedores, quiero desactivar un vehículo para que deje de aparecer disponible en Moveo.|**Scenario 1:**<br>**Given** que el invitado desea pausar un vehículo,<br>**When** hace clic en “Desactivar”<br>**Then** el sistema cambia su estado a “no disponible” y confirma la acción<br>**Scenario 2:**<br>**Given** que el vehículo está reservado para una futura fecha<br>**When** intenta desactivarlo<br>**Then** el sistema muestra un mensaje que impide la desactivación hasta que se cumpla la reserva|EP02|
|US21|Subir fotos al listado de vehículo|Como visitante del segmento proveedores, quiero agregar o eliminar fotos de mis vehículos para mostrarlos mejor a los arrendatarios.|**Scenario 1:**<<br>**Given** que accede a la galería de un vehículo<br>**When** sube imágenes en formatos válidos (jpg/png)<br>**Then** las fotos se guardan y aparecen en la galería<br>**Scenario 2:**<br>**Given** que intenta subir un archivo de formato no soportado (p.ej. .exe)<br>**When** lo selecciona<br>**Then** recibe un mensaje de error indicando formatos permitidos|EP02|
|US22|Visualizar reservas de mis vehículos|Como visitante del segmento proveedores, quiero consultar un historial y estado de reservas realizadas a mis vehículos|**Scenario 1:**<br>**Given** qué hay reservas activas o pasadas<br>**When** accede a la sección “Reservas de mis vehículos”<br>**Then** ve una lista con cada reserva, fechas y estado<br>**Scenario 2:**<br>**Given** que no hay reservas registradas<br>**When** ingresa a esa sección<br>**Then** ve un mensaje “Aún no tienes reservas”|EP02|

## 3.3. Impact Mapping

- Segmento Objetivo: Proveedor de Autos

<p align="center">
  <img src="assets/chapter03/impact%20mapping/impact_trabajador.png"  style="width:650px; height:auto;" alt="">
</p>

- Segmento Objetivo: Trabajador Urbano

<p align="center">
  <img src="assets/chapter03/impact%20mapping/impact_provedor.png"  style="width:650px; height:auto;" alt="">
</p>

## 3.4. Product Backlog
|**# Orden**|**User Story Id**|**Título**|**Descripción**|**Story Points(1 / 2 / 3 / 5)**|
|--|-| --| --|-- |
|1|US01|Registro de nuevos usuarios|Como visitante del segmento del segmento trabajadores, quiero registrarme para acceder al servicio de alquiler de autos.|3|
|2|US02|Inicio de sesión seguro|Como visitante del segmento trabajadores, quiero iniciar sesión de manera segura para usar la plataforma.|2|
|3|US03|Registro de autos por proveedor|Como visitante del segmento de proveedores, quiero registrar mis autos para ponerlos en alquiler.|3|
|4|US04|Visualización de autos disponibles|Como visitante del segmento trabajadores, quiero visualizar los autos disponibles en un mapa.|3|
|5|US05|Reserva de auto|Como visitante del segmento trabajadores, quiero reservar un auto para asegurar su disponibilidad.|2|
|6|US06|Implementación de Call to Action|Como visitante del segmento trabajadores, quiero encontrar botones de acción clara para facilitar la interacción.|3|
|7|US07|Creación de Footer Informativo|Como visitante del segmento (trabajadores), quiero encontrar en el footer información sobre contacto, términos y condiciones y enlaces sociales.|1|
|8|US08|Sección de Testimonios de Usuarios|Como visitante del segmento trabajadores, quiero visualizar opiniones y experiencias de otros usuarios para confiar en el servicio antes de usarlo.|3|
|9|US09|Sección de Preguntas Frecuentes (FAQ)|Como visitante del segmento trabajadores, quiero consultar una sección de preguntas frecuentes para resolver mis dudas sin contacto humano.|2|
|10|US10|Visualización de estacionamientos en el mapa|Como usuario, quiero ver en el mapa los estacionamientos disponibles cercanos para poder elegir uno al recibir el auto|5|
|11|US11|Desbloqueo del auto mediante la app|Como usuario, quiero desbloquear el auto desde la aplicación sin necesidad de contacto físico o intermediarios|3|
|12|US12|Verificación de mantenimiento del vehículo|Como usuario, quiero recibir notificaciones sobre cuándo es necesario realizar mantenimiento a mis vehículos en renta|3|
|13|US13|Visualizar precios y tarifas|Como visitante del segmento objetivo trabajadores quisiera poder visualizar los precios y tarifas que ofrece la aplicación para saber si me conviene comprar sus servicios|2|
|14|US14|Visualizar principales funciones|Como visitante del segmento objetivo de trabajadores y proveedores, quiero poder ver las funcionalidades que ofrece la aplicación para saber qué beneficio puedo tener|3|
|15|US15|Ver el nombre, logo y eslogan de la aplicación|Como visitante del segmento trabajadores y proveedores, quiero poder visualizar el nombre y eslogan de la aplicación para saber de qué se trata a primera vista |1|
|16|US16|Visualizar el nombre del equipo |Como visitante del segmento trabajadores y proveedores, quiero poder visualizar el nombre del equipo que diseñó la aplicación para saber quién la creó y darle mis respetos|3|
|17|US17|Sección de contacto|Como visitante del segmento trabajadores y proveedores, quiero poder contactar a la startup creadora de la app para notificar si hay algun error o si simplemente quiero hablar con ellos|3|
|18|US18|Landing Page Responsive|Como visitante del segmento trabajadores y proveedores, quiero entrar a la landing page desde mi movil y mi pc sin ningun problema para tener más flexibilidad al momento de registrarse|2|
|19|US19|Editar información de un vehículo|Como visitante del segmento proveedores, quiero actualizar datos de un vehículo (tarifa, descripción) para mantener la información al día.|3|
|20|US20|Desactivar vehículo de la plataforma|Como visitante del segmento proveedores, quiero desactivar un vehículo para que deje de aparecer disponible en Moveo.|3|
|21|US21|Subir fotos al listado de vehículo|Como visitante del segmento proveedores, quiero agregar o eliminar fotos de mis vehículos para mostrarlos mejor a los arrendatarios.|5|
|22|US22|Visualizar reservas de mis vehículos|Como visitante del segmento proveedores, quiero consultar un historial y estado de reservas realizadas a mis vehículos|3|

<p align="center">
  <a>
    <img src="assets/chapter03/product%20backlog/backlog.png" style="width:1000px; height:auto;" alt="">
  </a>
</p>