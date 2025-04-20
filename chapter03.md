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
| **Epic / Story ID**|**Título**| **Descripción**|**Criterios de aceptación**|**Relacionado con (Epic ID)**|
|------------|---------|----------------|------|------|
|**US01**|**Registro de Usuario**|**Como invitado trabajador quiero registrarme para acceder a la plataforma.**|**Given** un usuario que accede al formulario de registro <br>**When** ingresa todos los datos válidos <br>**Then** su cuenta debe crearse correctamente|**EP01**|
|**US02**|**Inicio de Sesión Seguro**|**Como invitado proveedor quiero iniciar sesión para acceder a mi cuenta**|**Given** que el invitado ha ingresado su usuario y contraseña correctos <br>**When** presiona iniciar sesión <br>**Then** debe acceder a su panel personal|**EP01**|
|**US03**|**Registro de Autos por Proveedores**|**Como invitado proveedor quiero registrar mis autos disponibles para alquiler.**|**Given**  un proveedor autenticado<br>**When**  completa los datos del auto y presiona registrar<br>**Then** el auto debe estar disponible en la lista de autos para alquilar|**EP02**|
|**US04**|**Visualización de Vehículos Disponibles**|**Como invitado trabajador quiero ver los autos disponibles para alquilar.**|**Given** un invitado autenticado<br>**When** accede a la sección de búsqueda<br>**Then** debe mostrarse un listado filtrable de autos disponibles.**|**EP03**|
|**US05**|**Selección de Estacionamiento en el Mapa**|**Como invitado trabajador quiero seleccionar el punto de recogida y entrega en un mapa.**|**Given** que un invitado ha iniciado sesión<br>**When** visualiza el mapa<br>**Then** debe poder seleccionar un estacionamiento válido como punto de entrega/recogida|**EP04**|
|**US06**|**Implementación de Call to Action**|**Como visitante trabajador quiero encontrar botones de acción clara que me guíen a registrarse o alquilar, para facilitar la interacción**|**Given** que accedo a la Landing Page<br>**When** visualizo las secciones principales<br>**Then** encuentro Call to Action claros como “Regístrate” o “Alquila un vehículo”|**EP05**|
|**US07**|**Creación de Footer Informativo**|**Como visitante proveedor quiero encontrar en el footer información sobre contacto, términos y condiciones y enlaces sociales.**|**Given** que estoy en cualquier sección de la web<br>**When** hago scroll hasta abajo<br>**Then**encuentro un footer con datos de contacto, enlaces legales y redes sociales.**|**EP05**|
|**US08**|**Sección de Testimonios de Usuarios**|**Como visitante proveedor quiero visualizar opiniones y experiencias de otros usuarios, para confiar en el servicio antes de usarlo**|**Given** que accedo a la sección de testimonios<br>**When** navegó por las opiniones<br>**Then** debo poder leer diferentes experiencias validadas por otros clientes|**EP05**|
|**US09**|**Sección de Preguntas Frecuentes (FAQ)**|**Como visitante trabajador quiero consultar una sección de preguntas frecuentes para resolver mis dudas sin contacto humano**|**Given** que accedo a la Landing Page<br>**When** entro a la sección de preguntas frecuentes<br>**Then**  debo poder leer y entender respuestas claras a las dudas comunes.**|**EP05**|

## 3.3. Impact Mapping
## 3.4. Product Backlog
