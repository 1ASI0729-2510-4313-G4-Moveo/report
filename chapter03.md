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

| Epic ID | Título                                   | Descripción                                                                                                      |
|---------|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| EP01    | Landing Page Informativa                  | **Como** visitante (trabajador o proveedor) **quiero** entender qué es Moveo, cómo funciona y qué beneficios me ofrece, **para** decidir registrarme en la plataforma. |
| EP02    | Gestión y Registro de Usuarios            | **Como** usuario (trabajador o proveedor) **quiero** poder registrarme y autenticarme fácilmente en la plataforma **para** acceder de forma segura a las funcionalidades de Moveo según mi perfil. |
| EP03    | Gestión de Vehículos para Proveedores     | **Como** usuario proveedor **quiero** registrar, listar y administrar mis autos disponibles **para** alquiler de forma flexible y automatizada, y generar ingresos cuando no los utilizo. |
| EP04    | Solicitud y Reserva de Vehículos          | **Como** usuario trabajador **quiero** poder buscar, reservar y acceder a vehículos cercanos desde la aplicación **para** movilizarme libremente sin necesidad de comprar un auto. |
| EP05    | Visualización y Selección de Estacionamientos | **Como** usuario trabajador **quiero** visualizar en un mapa los estacionamientos disponibles **para** recoger y dejar el vehículo en el punto que más me convenga. |
| EP06    | Manejo de la app web | **Como** desarrollador **quiero** manejar fácilmente la información de la aplicación **para** saber si todo está fluyendo de forma satisfactoria. |

### User Stories

| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
| ----- | ----- | ----- | ----- | ----- |
| US01 | Registro de nuevos usuarios | **Como** visitante de ambos segmentos, **quiero** registrarme **para** acceder al servicio de la aplicación. | **Escenario 1:** <br>**Dado** que deseo alquilar un auto <br>**Cuando** completo el formulario de registro correctamente <br>**Entonces** la plataforma crea mi cuenta y me notifica que el registro fue exitoso.  <br>**Escenario 2:**<br>  **Dado** que soy un visitante del segmento trabajadores y no completo todos los campos obligatorios <br>**Cuando** intentó finalizar el registro **Entonces** la plataforma me muestra mensajes indicando los campos faltantes. | EP02 |
| US02 | Inicio de sesión seguro | **Como** usuario, **quiero** iniciar sesión de manera segura **para** usar la plataforma. | **Escenario 1:** <br> **Dado** que soy usuario registrado  <br> **Cuando** ingreso mis credenciales correctas **Entonces** puedo acceder a la plataforma  <br>**Escenario 2:** <br> **Dado** que ingresó credenciales incorrecta **Cuando** intento iniciar sesión <br> **Entonces** recibo un mensaje de error indicando que los datos no son válidos. | EP02 |
| US03 | Registro de autos por proveedor |**Como** usuario, **quiero** registrar mis autos **para** ponerlos en alquiler. | **Escenario 1:** <br>**Dado** que soy usuario y tengo un auto disponible <br> **Cuando** completo los datos del vehículo y los envío<br> **Entonces** el auto queda disponible en la plataforma. <br> **Escenario 2:** <br>**Dado** que soy usuario y omito datos obligatorios <br> **Cuando** intento registrar el auto <br> **Entonces** el sistema me alerta sobre los campos incompletos. | EP03 |
| US04 | Visualización de autos disponibles | **Como** usuario, **quiero** visualizar los autos disponibles en un mapa **para** tener un mejor acercamiento a los centros cerca mio. | **Escenario 1:** <br> **Dado** que soy usuario autenticado <br> **Cuando** accedo a la sección de mapa <br> **Entonces** puedo visualizar los autos disponibles en tiempo real. <br> **Escenario 2:** <br> **Dado** que me encuentro en una zona sin autos disponibles <br> **Cuando** ingreso al mapa <br> **Entonces** la plataforma me notifica que no hay disponibilidad en esa ubicación. | EP04 |
| US05 | Reserva de auto | **Como** usuario, **quiero** reservar un auto **para** asegurar su disponibilidad. | **Escenario 1:** <br> **Dado** que soy un usuario y encuentro un auto disponible <br> **Cuando** realizo la reserva **Entonces** recibo confirmación de que el auto ha sido apartado  <br> **Escenario 2:** <br>  **Dado** que otro usuario ya reservó el auto antes que yo <br> **Cuando** intento hacer la reserva <br> **Entonces** recibo una notificación indicando que el auto ya no está disponible. | EP05 |
| US06 | Implementación de Call to Action | **Como** visitante de ambos segmentos, **quiero** encontrar botones de acción clara **para** facilitar la interacción. | **Escenario 1:** <br> **Dado** que accede a la Landing Page <br> **Cuando** visualizo las secciones principales <br> **Entonces** encuentro al menos un Call to Action en cada sección clave. <br> **Escenario 2:** <br>  **Dado** que accede a la Landing Page desde un dispositivo móvil <br> **Cuando** navego hacia abajo <br> **Entonces** los Call to Action deben ser claramente visibles y accesibles sin interferir con la navegación. | EP01 |
| US07 | Creación de Footer Informativo | **Como** visitante de ambos segmentos, **quiero** encontrar en el footer información sobre contacto, términos y condiciones y enlaces sociales. **para** sentir confianza y poder comunicarme fácilmente con la plataforma si lo necesito. | **Escenario 1:** <br> **Dado** que estoy en cualquier sección de la web <br> **Cuando** hago scroll hasta abajo <br> **Entonces** encuentro un footer con datos de contacto y enlaces legales. <br> **Escenario 2:** <br> **Dado** que visualizo el footer en distintos dispositivos <br> **Cuando** cambio de escritorio a móvil <br> **Entonces** la información sigue siendo legible y funcional (responsive). | EP01 |
| US08 | Sección de Testimonios de Usuarios | **Como** visitante de ambos segmentos, **quiero** visualizar opiniones y experiencias de otros usuarios **para** confiar en el servicio antes de usarlo. | **Escenario 1:**  <br> **Dado** que accedo a la sección de testimonios <br> **Cuando** navego por las opiniones <br> **Entonces** visualizo testimonios reales con nombre y calificación. **Escenario 2:** <br> **Dado** que revisó varios testimonios <br> **Cuando** regresó en otro momento <br> **Entonces** el orden de testimonios puede variar (rotación aleatoria o según relevancia). | EP01 |
| US09 | Sección de Preguntas Frecuentes (FAQ) | **Como** visitante de ambos segmentos, **quiero** consultar una sección de preguntas frecuentes **para** resolver mis dudas sin contacto humano. | **Escenario 1:** <br> **Dado** que accedo a la Landing Page <br> **Cuando** ingresó a la sección de FAQ <br> **Entonces** puedo visualizar y expandir preguntas y respuestas claras.  <br> **Escenario 2:** <br> **Dado** que realizó una búsqueda en la FAQ <br> **Cuando** escribo palabras clave en el buscador <br> **Entonces** se filtran las preguntas relacionadas de forma automática. | EP01 |
| US10 | Visualización de estacionamientos en el mapa | **Como** usuario, **quiero** ver en el mapa los estacionamientos disponibles cercanos **para** poder elegir uno al recibir el auto | **Escenario 1:**  **Dado** que el invitado ha iniciado sesión <br> **Cuando** accede al mapa de estacionamientos <br> **Entonces** el sistema muestra marcadores de ubicación con disponibilidad.  <br> **Escenario 2:** <br> **Dado** que el invitado selecciona un estacionamiento <br> **Cuando** confirma la reserva <br> **Entonces** el sistema le asigna el punto de entrega y lo bloquea para otros usuarios. | EP03 |
| US11 | Desbloqueo del auto mediante la app | **Como** usuario, **quiero** desbloquear el auto desde la aplicación **para** no necesitar contacto físico o intermediarios | **Escenario 1:**  <br> **Dado** que el usuario ha llegado al estacionamiento correcto <br> **Cuando** abre la app y confirma la ubicación <br> **Entonces** el sistema habilita el botón de desbloqueo.  <br> **Escenario 2:** <br>  **Dado** que el invitado pulsa el botón de desbloqueo **Cuando** el sistema valida la reserva **Entonces** se libera el seguro electrónico y se habilita el acceso al vehículo. | EP04 |
| US12 | Verificación de mantenimiento del vehículo | **Como** usuario, **quiero** recibir notificaciones sobre cuándo es necesario realizar mantenimiento a mis vehículos en renta **para** asegurarme de que estén siempre en buen estado y ofrecer un servicio seguro y confiable. | **Escenario 1:** <br> **Dado** que el auto alcanza el kilometraje límite configurado <br> **Cuando** se registra en la plataforma <br> **Entonces** se envía una notificación automática al proveedor.  <br> **Escenario 2:** <br>  **Dado** que el proveedor recibe la notificación de mantenimiento <br> **Cuando** accede a la app **Entonces** puede marcar como "mantenimiento programado" para que el auto sea retirado de la disponibilidad temporalmente. | EP05 |
| US13 | Visualizar precios y tarifas | **Como** visitante del segmento objetivo trabajadores **quiero** poder visualizar los precios y tarifas que ofrece la aplicación **para** saber si me conviene comprar sus servicios | **Escenario 1:** <br> **Dado** que el visitante del segmento trabajadores accede a la landing page <br> **Cuando** navega a la sección de precios <br> **Entonces** puede visualizar la lista actualizada de tarifas y modalidades disponibles. <br> **Escenario 2:** <br> **Dado** que el visitante del segmento trabajadores accede desde un dispositivo móvil <br> **Cuando** carga la sección de precios <br> **Entonces** la información se muestra legible y correctamente adaptada. | EP01 |
| US14 | Visualizar principales funciones | **Como** visitante de ambos segmentos, **quiero** poder ver las funcionalidades que ofrece la aplicación **para** saber qué beneficio puedo tener | **Escenario 1:** <br> **Dado** que accedo a la landing page <br> **Cuando** llega a la sección de funcionalidades <br> **Entonces** visualiza una lista clara y breve de las funciones principales de la aplicación <br> **Escenario 2:** <br> **Dado** que la lista de funciones es extensa <br> **Cuando** el visitante navega <br> **Entonces** puede acceder a detalles ampliados mediante enlaces o botones informativos. | EP01 |
| US15 | Visualización de datos de la empresa de la aplicación | **Como** visitante de ambos segmentos, **quiero** poder visualizar el nombre y eslogan de la aplicación **para** saber de qué se trata a primera vista   | **Escenario 1:** <br> **Dado** que el visitante accede a la landing page <br> **Cuando** la página carga correctamente **Entonces** puede visualizar el nombre, logo y eslogan de la aplicación en la cabecera. <br> **Escenario 2:** <br> **Dado** que el visitante accede desde un dispositivo móvil <br> **Cuando** visualiza la cabecera <br> **Entonces** el nombre, logo y eslogan se adaptan y siguen siendo claramente legibles. | EP01 |
| US16 | Visualizar el nombre del equipo |**Como** visitante de ambos segmentos, **quiero** poder visualizar el nombre del equipo que diseñó la aplicación **para** saber quién la creó y darle mis respetos | **Escenario 1:** <br> **Dado** que el visitante accede al pie de página de la landing page <br> **Cuando** la sección "Acerca del equipo" está disponible <br> **Entonces** puede visualizar el nombre del equipo responsable de la aplicación.  **Escenario 2:** <br> **Dado** que el visitante quiere conocer más sobre el equipo <br> **Cuando** hace clic sobre el nombre del equipo <br> **Entonces** es redirigido a una página de presentación o sección con detalles adicionales. | EP01 |
| US17 | Sección de contacto | **Como** visitante de ambos segmentos **quiero** poder contactar a la startup creadora de la app **para** notificar si hay algun error o si simplemente quiero hablar con ellos | **Escenario 1:** <br> **Dado** que el visitante accede a la sección de contacto <br> **Cuando** completa el formulario con sus datos y mensaje <br> **Entonces** recibe una confirmación visual de que su mensaje ha sido enviado correctamente. <br> **Escenario 2:** <br> **Dado** que el visitante deja campos obligatorios vacíos en el formulario de contacto <br> **Cuando** intenta enviarlo <br> **Entonces** el sistema muestra un mensaje de error solicitando completar la información. | EP01 |
| US19 | Editar información de un vehículo | **Como** usuario, **quiero** actualizar datos de un vehículo (tarifa, descripción) **para** mantener la información al día. | **Escenario 1:** <br> **Dado** que el usuario selecciona "Editar" en uno de sus vehículos <br> **Cuando** modifica la tarifa y guarda los cambios <br> **Entonces** el sistema actualiza la información y muestra un mensaje de éxito. <br> **Escenario 2:** <br> **Dado** que intenta guardar con una tarifa no válida (por ejemplo, negativa) **Cuando** presiona "Guardar" **Entonces** el sistema muestra la validación de error en el campo de tarifa. | EP03 |
| US20 | Desactivar vehículo de la plataforma | **Como** usuario, **quiero** desactivar un vehículo **para** que deje de aparecer disponible en Moveo. | **Escenario 1:** <br>  **Dado** que el invitado desea pausar un vehículo <br> **Cuando** hace clic en "Desactivar" <br> **Entonces** el sistema cambia su estado a "no disponible" y confirma la acción.  <br> **Escenario 2:** <br> **Dado** que el vehículo está reservado para una futura fecha <br> **Cuando** intenta desactivarlo <br> **Entonces** el sistema muestra un mensaje que impide la desactivación hasta que se cumpla la reserva. | EP03 |
| US21 | Subir fotos al listado de vehículo | **Como** usuario, **quiero** agregar o eliminar fotos de mis vehículos **para** mostrarlos mejor a los arrendatarios. | **Escenario 1:**  <br> **Dado** que accede a la galería de un vehículo <br> **Cuando** sube imágenes en formatos válidos (jpg/png) <br> **Entonces** las fotos se guardan y aparecen en la galería.  <br> **Escenario 2:** <br> **Dado** que intenta subir un archivo de formato no soportado (por ejemplo, .exe) <br> **Cuando** lo selecciona <br> **Entonces** recibe un mensaje de error indicando formatos permitidos. | EP03 |
| US22 | Visualizar reservas de mis vehículos | **Como** usuario, **quiero** consultar un historial y estado de reservas realizadas a mis vehículos **para** llevar un control eficiente de su uso y disponibilidad. | **Escenario 1:** <br> **Dado** que hay reservas activas o pasadas <br> **Cuando** accede a la sección "Reservas de mis vehículos" <br> **Entonces** ve una lista con cada reserva, fechas y estado. <br> **Escenario 2:** <br> **Dado** que no hay reservas registradas <br> **Cuando** ingresa a esa sección <br> **Entonces** ve un mensaje "Aún no tienes reservas". | EP03 |
| US23 | Visualizar historial de uso  | **Como** usuario, **quiero** consultar un historial de carros que eh usado en un pasado **para** llevar un control eficiente de uso y gasto en la aplicación. | **Escenario 1:** <br> **Dado** que hay un historial guardado sobre carros usados <br> **Cuando** accede a la sección "Record" <br> **Entonces** ve una lista del historial de carros usados. <br> **Escenario 2:** <br> **Dado** que no hay un historial registrado <br> **Cuando** ingresa a esa sección <br> **Entonces** ve un mensaje "Aún no tiene historial". | EP02 |
| US24 | Visualizar y editar metodos de pago | **Como** usuario, **quiero** editar el metodo de pago **para** cambiar de tarjeta a una donde si tengo fondos | **Escenario 1:** <br> **Dado** que el usuario quiera cambiar de metodo de pago <br> **Cuando** accede a la sección "payments" <br> **Entonces** ve el metodo de pago actual mas la opción de editarlo <br> **Escenario 2:** <br> **Dado** que el usuario quiera eliminar el metodo de pago <br> **Cuando** ingresa a esa sección <br> **Entonces** presiona eliminar metodo de pago. | EP03 |
| TS01 | Diseño adaptable (responsive) | **Como** developer  **quiero** asegurar que la aplicación web se adapte a cualquier tamaño de pantalla, **para** garantizar una experiencia accesible desde móviles y computadoras | **Escenario 1:** <br> **Dado** que se visualiza en un smartphone <br> **Cuando** se accede a la interfaz principal <br> **Entonces** todos los elementos deben ajustarse sin desbordarse. <br> **Escenario 2:** <br> **Dado** que se accede desde una laptop o pantalla grande <br> **Cuando** se cargan las vistas  **Entonces** la disposición debe ocupar eficientemente el espacio disponible. | EP06 |
| TS02 | Integración del mapa con geolocalización | **Como** desarrollador, **quiero** integrar una API de mapas con soporte de geolocalización, **para** mostrar la ubicación de autos y estacionamientos en tiempo real | **Escenario 1:** <br> **Dado** que el mapa está visible <br> **Cuando** el usuario accede a la app <br> **Entonces** debe mostrarse su ubicación actual con un marcador. <br> **Escenario 2:** <br> **Dado** que existen autos disponibles, **Cuando** el mapa se carga <br> **Entonces** deben mostrarse sus ubicaciones como pines interactivos. | EP06 |
| TS03 | Implementación de sistema de calificación de autos | **Como** desarrollador, **quiero** permitir que los usuarios califiquen los autos después de un viaje, **para** mantener control sobre la calidad del servicio | **Escenario 1:** <br> **Dado** que el usuario ha completado un viaje <br> **Cuando** accede a su historial <br> **Entonces** debe visualizar una opción para calificar el auto utilizado. <br> **Escenario 2:** <br>  **Dado** que el usuario ingresa una calificación <br> **Cuando** la envía <br> **Entonces** debe guardarse correctamente en la base de datos con la referencia al auto y al viaje. <br> **Escenario 3:** <br>  **Dado** que múltiples usuarios han calificado el mismo auto <br> **Cuando** se consulta la ficha del auto <br> **Entonces** debe mostrarse el promedio de calificaciones actualizado. | EP06 |
| TS04 | Funcionalidad CRUD en la interfaz | Como developer quiero implementar funcionalidades CRUD (Crear, leer, actualizar, eliminar)  en la interfaz para gestionar los recursos de manera dinamica desde el frontend | **Escenario 1:**<br>Dado que el developer prueba la sección de users<br>Cuando crea un nueva renta<br>Entonces inmediatamente se debe crear y mostrar los detalles sin necesidad de recargar la página <br>**Escenario 2:**<br>Dado que el developer sigue realizando pruebas y decide eliminar o editar la renta realizada<br>Cuando presiona el botón eliminar o editar<br>Entonces los cambios realizados se deben mostrar en la interfaz y el estado de la  aplicación | EP06 |
| TS05 | Despliegue de la aplicación | Como developer quiero desplegar la aplicación en un entorno accesible públicamente para que otros usuarios puedan probar su funcionamiento |*Escenario 1:**<br>Dado que el repositorio principal contiene la última versión estable del proyecto<br>Cuando se ejecuta el proceso de despliegue<br>Entonces la aplicación debe estar disponible en una URL pública sin errores <br>**Escenario 2:**<br>Dado que el entorno de producción está activo Cuando un usuario accede a la aplicación<br>Entonces la carga debe completarse en un tiempo optimo | EP06 |
| TS06 | Configuración de las rutas principales | Como developer, quiero configurar las rutas principales de la aplicación para permitir la navegación entre las diferentes vistas de forma fluida  | **Escenario 1:**<br>Dado que el usuario accede a la ruta principal<br>Cuando la URL es ingresada o se hace clic en un enlace<br>Entonces debe cargarse la vista principal sin recargar la página<br>**Escenario 2:**<br>Dado que el usuario accede a una ruta no definida como /xyz Cuando se produce un error en las rutas de navegación Entonces debe mostrarse una página 404 personalizada.  | EP06 |

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
|---------|--------------|--------|-------------|--------------|
| 1 | US06 | Implementación de Call to Action | **Como** visitante de ambos segmentos, **quiero** encontrar botones de acción clara **para** facilitar la interacción. | 2 |
| 2 | US07 | Creación de Footer Informativo | **Como** visitante de ambos segmentos, **quiero** encontrar en el footer información sobre contacto, términos y condiciones y enlaces sociales **para** sentir confianza y poder comunicarme fácilmente con la plataforma si lo necesito. | 1 |
| 3 | US08 | Sección de Testimonios de Usuarios | **Como** visitante de ambos segmentos, **quiero** visualizar opiniones y experiencias de otros usuarios **para** confiar en el servicio antes de usarlo. | 2 |
| 4 | US09 | Sección de Preguntas Frecuentes (FAQ) | **Como** visitante de ambos segmentos, **quiero** consultar una sección de preguntas frecuentes **para** resolver mis dudas sin contacto humano. | 3 |
| 5 | US13 | Visualizar precios y tarifas | **Como** visitante del segmento objetivo trabajadores, **quiero** poder visualizar los precios y tarifas que ofrece la aplicación **para** saber si me conviene comprar sus servicios. | 2 |
| 6 | US14 | Visualizar principales funciones | **Como** visitante de ambos segmentos, **quiero** poder ver las funcionalidades que ofrece la aplicación **para** saber qué beneficio puedo tener. | 1 |
| 7 | US15 | Visualización de datos de la empresa de la aplicación | **Como** visitante de ambos segmentos, **quiero** poder visualizar el nombre y eslogan de la aplicación **para** saber de qué se trata a primera vista. | 1 |
| 8 | US16 | Visualizar el nombre del equipo | **Como** visitante de ambos segmentos, **quiero** poder visualizar el nombre del equipo que diseñó la aplicación **para** saber quién la creó y darle mis respetos. | 1 |
| 9 | US17 | Sección de contacto | **Como** visitante de ambos segmentos, **quiero** poder contactar a la startup creadora de la app **para** notificar si hay algún error o si simplemente quiero hablar con ellos. | 3 |
| 10 | US01 | Registro de nuevos usuarios | **Como** visitante de ambos segmentos, **quiero** registrarme **para** acceder al servicio de la aplicación. | 5 |
| 11 | US02 | Inicio de sesión seguro | **Como** usuario, **quiero** iniciar sesión de manera segura **para** usar la plataforma. | 3 |
| 12 | US03 | Registro de autos por proveedor | **Como** usuario, **quiero** registrar mis autos **para** ponerlos en alquiler. | 5 |
| 13 | US10 | Visualización de estacionamientos en el mapa | **Como** usuario, **quiero** ver en el mapa los estacionamientos disponibles cercanos **para** poder elegir uno al recibir el auto. | 3 |
| 14 | US19 | Editar información de un vehículo | **Como** usuario, **quiero** actualizar datos de un vehículo (tarifa, descripción) **para** mantener la información al día. | 2 |
| 15 | US20 | Desactivar vehículo de la plataforma | **Como** usuario, **quiero** desactivar un vehículo **para** que deje de aparecer disponible en Moveo. | 2 |
| 16 | US21 | Subir fotos al listado de vehículo | **Como** usuario, **quiero** agregar o eliminar fotos de mis vehículos **para** mostrarlos mejor a los arrendatarios. | 3 |
| 17 | US22 | Visualizar reservas de mis vehículos | **Como** usuario, **quiero** consultar un historial y estado de reservas realizadas a mis vehículos **para** llevar un control eficiente de su uso y disponibilidad. | 2 |
| 18 | US04 | Visualización de autos disponibles | **Como** usuario, **quiero** visualizar los autos disponibles en un mapa **para** tener un mejor acercamiento a los centros cerca mío. | 5 |
| 19 | US11 | Desbloqueo del auto mediante la app | **Como** usuario, **quiero** desbloquear el auto desde la aplicación **para** no necesitar contacto físico o intermediarios. | 5 |
| 20 | US05 | Reserva de auto | **Como** usuario, **quiero** reservar un auto **para** asegurar su disponibilidad. | 5 |
| 21 | US12 | Verificación de mantenimiento del vehículo | **Como** usuario, **quiero** recibir notificaciones sobre cuándo es necesario realizar mantenimiento a mis vehículos en renta **para** asegurarme de que estén siempre en buen estado y ofrecer un servicio seguro y confiable. | 3 |
| 22 | US23 | Visualizar historial de uso |  **Como** usuario, **quiero** consultar un historial de carros que eh usado en un pasado **para** llevar un control eficiente de uso y gasto en la aplicación.| 5 |
| 23 | US24 | Visualizar y editar metodos de pago | **Como** usuario, **quiero** editar el metodo de pago **para** cambiar de tarjeta a una donde si tengo fondos  | 3 |
| 24 | TS01 | Diseño adaptable (responsive) | **Como** developer, **quiero** asegurar que la aplicación web se adapte a cualquier tamaño de pantalla, **para** garantizar una experiencia accesible desde móviles y computadoras. | 5 |
| 25 | TS02 | Integración del mapa con geolocalización | **Como** desarrollador, **quiero** integrar una API de mapas con soporte de geolocalización, **para** mostrar la ubicación de autos y estacionamientos en tiempo real. | 8 |
| 26 | TS03 | Implementación de sistema de calificación de autos | **Como** desarrollador, **quiero** permitir que los usuarios califiquen los autos después de un viaje, **para** mantener control sobre la calidad del servicio. | 3 |
| 27 | TS04 | Funcionalidad CRUD en la interfaz | Como developer quiero implementar funcionalidades CRUD (Crear, leer, actualizar, eliminar)  en la interfaz para gestionar los recursos de manera dinamica desde el frontend | 5 |
| 28 | TS05 | Despliegue de la aplicación | Como developer quiero desplegar la aplicación en un entorno accesible públicamente para que otros usuarios puedan probar su funcionamiento | 3 |
| 29 | TS06 | Configuración de las rutas principales | Como developer, quiero configurar las rutas principales de la aplicación para permitir la navegación entre las diferentes vistas de forma fluida | 3 |

<p align="center">
  <a>
    <img src="assets/chapter03/product%20backlog/backlog.png" style="width:1000px; height:auto;" alt="">
  </a>
</p>
