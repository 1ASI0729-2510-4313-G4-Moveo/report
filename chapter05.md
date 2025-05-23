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

# **Capítulo V: Product Implementation, Validation & Deployment**
## 5.1. Software Configuration Management
### 5.1.1. Software Development Environment Configuration

Esta sección establece el listado oficial del software, herramientas y plataformas que los miembros del equipo de la startup usaron para garantizar coherencia, colaboración y eficiencia en la construcción y mantenimiento de la web application.

| **Actividad**             | **Producto**        | **Propósito**                                                            | **Ruta de referencia**                             |
|---------------------------|---------------------|--------------------------------------------------------------------------|--------------------------------------------------|
| **Project Management**     | Jira                | Planificación, seguimiento y gestión de tareas ágiles. (Sprints, Product Backlog, etc.) | [Jira](https://moveo-upc.atlassian.net/)          |
| **Product UX/UI Design**   | Figma               | Diseño de interfaces de usuario, landing page y prototipado               | [Figma](https://figma.com)                       |
| **Software Development**   | Visual Studio Code  | Edición y desarrollo de código para interfaces web y móvil               | [Visual Studio Code](https://code.visualstudio.com/) |
| **Software Deployment**    | Github Pages        | Despliegue de la landing Page                                             | [Github Pages](https://pages.github.com/)        |
| **Software Documentation** | Markdown + StackEdit.io | Redacción y despliegue de documentación técnica.                          | [StackEdit.io](https://stackedit.io)             |
| **Version Control**        | GIT (Github)        | Control de versiones y revisiones de código                               | [Github](https://github.com)                     |

### 5.1.2. Source Code Management

En nuestro proyecto, utilizamos **GitHub** como plataforma para gestionar el código fuente, manteniendo los siguientes repositorios:

- Report: https://github.com/1ASI0729-2510-4313-G4-Moveo/report
- Landing page: https://github.com/1ASI0729-2510-4313-G4-Moveo/Landing-Page
- Frontend: https://github.com/1ASI0729-2510-4313-G4-Moveo/frontend
- Backend: https://github.com/1ASI0729-2510-4313-G4-Moveo/backend

#### GitFlow Workflow
Se implementa el modelo de **GitFlow** para gestionar las ramas en nuestros repositorios. A continuación, se detallan las ramas principales:

##### Para el Reporte:

- **master**: Contiene las versiones estables del reporte.
- **develop**: Se utiliza para integrar las nuevas características antes de publicarlas en la rama master.
- **feature/\<número de capítulo>**: Rama creada para el desarrollo de funcionalidades del capítulo.

##### Para el Landing, Frontend y Backend:

- **main**: Contiene las versiones estables del reporte.
- **develop**: Se utiliza para integrar las nuevas características antes de publicarlas en la rama release/\<versión>.
- **hotfix**: Se utiliza para integrar caracteristicas urgentes que afectan el funcionamiento de la aplicación.
- **realease/\<Versión>**: Se utiliza para integrar las nuevas características antes de publicarlas en la rama main.
- **feature/\<nombre de funcionalidad>**: Rama creada para el desarrollo de funcionalidades específicas según el nombre. Las ramas se nombran en minúsculas siguiendo un esquema uniforme para mayor consistencia.

<img src="./assets/chapter05/gitflow.png" />

#### Conventional Commits
Se emplea para los mensajes de commmits el estándar de **Conventional Commits** con las siguientes etiquetas:

- **feat**: Nuevas características.
- **fix**: Corrección de errores.
- **docs**: Documentación.
- **style**: Modificaciones de estilos.
- **refactor**: Cambio de código que no corrige un error ni añade una característica.
- **perf**: Modificaciones que mejoran el rendimiento.
- **test**: Modificacciones en testing.
- **build**: Cambios que afectan al sistema de compilación o a dependencias externas.
- **ci**: Cambios en nuestros archivos y scripts de configuración CI.
- **chore**: Otros cambios que no modifican ficheros src o test
- **revert**: Revierte un commit anterior

### 5.1.3. Source Code Style Guide & Conventions


Usaremos buenas prácticas para que el código sea coherente, entendible y sostenible a lo largo del tiempo.

### General

- Todo el código y sus elementos estarán escritos en **inglés**.
- La codificación será en **UTF-8**: `<meta charset="UTF-8">`.
- Convenciones en nombres:
  - **lowercase** para etiquetas HTML.
  - **kebab-case** para clases CSS.
  - **camelCase** para IDs, variables y funciones en JavaScript.
  - **PascalCase** para clases en C#.
- Indentación uniforme: 2 o 4 espacios (según el proyecto).
- Comentarios claros y en inglés, explicando el *por qué*, no solo el *qué*.

### HTML

- Todas las etiquetas deben cerrarse correctamente (`<img />`, `<input />`).
- Incluir la extensión en las referencias a archivos (.css, .js, .png, etc.).
- Se utilizó una estructura semántica clara:

| Etiqueta | Uso |
|---------|-----|
| `<header>` | Contiene elementos introductorios como la barra de búsqueda. |
| `<nav>` | Define la navegación principal del sitio. |
| `<div>` | Contenedor general para aplicar estilos y organizar el layout. |
| `<img />` | Inserta imágenes en distintas secciones. |
| `<ul>` | Define listas desordenadas (ej. menú de navegación). |
| `<li>` | Elementos dentro de listas, como en la barra de navegación o en el blog. |
| `<a>` | Crea hipervínculos para navegar entre secciones. |
| `<p>` | Define párrafos de texto. |
| `<button>` | Botones para acciones específicas del usuario. |
| `<h1>` - `<h4>` | Títulos y subtítulos jerárquicos. |

### CSS

- El `body` tendrá `width: 100%`.
- Clases en `kebab-case` según su propósito: `.header`, `.main-container`, `.cta-button`.
- No se deben usar nombres genéricos como `.red`, `.big` o `.centered`.
- Reinicio global de márgenes y padding:

```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

### 5.1.4. Software Deployment Configuration
Para la realizacion del despliegue debemos seguir los siguientes pasos:
  1. Primero, creamos un nuevo [repositorio en GitHub](https://github.com/1ASI0729-2510-4313-G4-Moveo/Landing-Page). Después, subimos los archivos del  proyecto a ese repositorio.
  2. Una vez que se haya subido todo, nos dirigimos a la configuración del repositorio. Allí, buscamos la sección de **"Pages"**, que aparece en la barra lateral izquierda.
  3. Luego, se vera una opción que permite seleccionar la rama desde la cual quieres hacer el despliegue. Normalmente, se elige **main**.
  4. Después de esto, GitHub generará automáticamente una URL para tu sitio.
<br>
<img src="./assets/chapter05/landing-deployment.png" />

## 5.2. Landing Page, Services & Applications Implementation
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1

**Sprint Planning Background**
<table>
  <tr>
    <th>Criterio</th>
    <th>Detalle</th>
  </tr>
  <tr>
    <td>Date</td>
    <td>2025-18-04</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>12:00pm</td>
  </tr>
  <tr>
    <td>Location</td>
    <td>Reunión Virtual en Virtual google meet</td>
  </tr>
  <tr>
    <td>Prepared By</td>
    <td>Giancarlo Castañeda</td>
  </tr>
  <tr>
    <td>Attendees (to planning meeting)</td>
    <td>Carlos Gonzales, Fernando Lizano, Javier Nikaido, Anghel Trillo</td>
  </tr>
  <tr>
    <td>Sprint 1 Review Summary</td>
    <td>Se realizó la landing page implementada con CSS y HTML, a raíz de los mockups y wireframes del diseño del landing page.</td>
  </tr>
  <tr>
    <td>Sprint 1 Retrospective Summary</td>
    <td>Mejorar la puntualidad en la entrega de artefactos.</td>
  </tr>
</table>


**Sprint Goal & User Stories** 

| Criterio  | Detalle   |
| :-------------- | -------------------- |
| Sprint 1 Goal  | Nuestro enfoque para este sprint es implementar la landing page de nuestro producto. Creemos que esto brindará una correcta presentación de nuestro producto hacia los visitantes. Esto se confirmará cuando todas las secciones de nuestra página web sean visitadas por cada visitante.  |
| Sprint 1 Velocity            | Para este sprint nuestro equipo puende aceptar hasta 25 story points       |
| **Sum of Story Points**      | Para este sprint haremos 23 story points                                |

#### 5.2.1.2. Aspect Leaders and Collaborators

| Team Member (Last Name, First Name)  | GitHub Username | Aspect Diseño UX/UI y Prototipado (L/C) | Aspect Programación de la Landing Page (L/C) | Aspect Arquitectura de Información y Sistemas de Organización/Navegación (L/C) |
| ------------------------------------ | --------------- | --------------------------------------- | -------------------------------------------- | --------------------------------------------------------------------------------------------- |
| Castañeda Guimas, Giancarlo Santiago | Darksens01      | L                                       | L                                            | C                                                                                             |
| Gonzales Valverde, Carlos Matthew    | Carlos12324     | C                                       | L                                            | L                                                                                             |
| Nikaido Vargas, Javier Nikaido       | MassiFlip       | L                                       | C                                            | C                                                                                             |
| Lizano Coll Cardenas, Fernando Jesus | GuardianDeity   | L                                       | C                                            | L                                                                                             |
| Trillo Hernandez, Anghel Melanie     | AM27TH          | C                                       | C                                            | L                                                                                             |

#### 5.2.1.3. Sprint Backlog 1
| User Story | Work-Item/Task | Id | Title | Description | Estimation (Hrs) | Assigned To | Status |
|:---|:---|:---|:---|:---|:---|:---|:---|
| us-6 | T6 | T6.1 | Implementación de Call to Action | Colocar botones de acción clara para facilitar la navegación. | 5 | Fernando Lizano | DONE |
| us-7 | T7 | T7.1 | Creación de Footer Informativo | Crear un pie de página con información de contacto y redes sociales. | 4 | Fernando Lizano | DONE |
| us-8 | T8 | T8.1 | Sección de Testimonios de Usuarios | Mostrar opiniones de usuarios anteriores para generar confianza. | 6 | Fernando Lizano | DONE |
| us-9 | T9 | T9.1 | Sección de Preguntas Frecuentes (FAQ) | Implementar una sección con respuestas a dudas comunes. | 5 | Fernando Lizano | DONE |
| us-10 | T10 | T10.1 | Visualización de estacionamientos en el mapa | Mostrar los estacionamientos disponibles para entrega/recogida. | 5 | Fernando Lizano | DONE |
| us-13 | T13 | T13.1 | Visualizar precios y tarifas | Mostrar los precios y tarifas de los autos disponibles. | 5 | Fernando Lizano |DONE |
| us-14 | T14 | T14.1 | Visualizar principales funciones | Mostrar en la web las funciones principales de Moveo. | 4 |  Fernando Lizano| DONE |
| us-15 | T15 | T15.1 | Ver el nombre, logo y eslogan de la aplicación | Mostrar claramente el logo, nombre y eslogan de Moveo. | 4 | Fernando Lizano | DONE |
| us-16 | T16 | T16.1 | Visualizar el nombre del equipo | Mostrar el nombre del equipo creador en la página. | 4 | Fernando Lizano, Javier Nikaido, Carlos Gonzales, Giancarlos Castañeda, Anghel Trillo| DONE |
| us-17 | T17 | T17.1 | Sección de contacto | Crear un formulario de contacto para dudas o soporte. | 5 | Fernando Lizano | DONE |
| us-18 | T18 | T18.1 | Landing Page Responsive | Adaptar la landing page para dispositivos móviles y escritorio. | 5 | Fernando Lizano | DONE |
#### 5.2.1.4. Development Evidence for Sprint Review
A continuación se muestran los commits realizados por los integrantes del equipo, se obviaron los merges y commits incorrectos por razones de mejor visualización acerca de los commits correctamente desarrollados e implementados:

| Repository  | Branch  | Commit Id  | Commit Message  | Commit Message Body  | Commited on (Date) |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-customers | 3e6d460 | feat(index): add scroll top function and content | \* No aplica  | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-customers| a04bacf | feat(index): add map area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-customers | d4b4511 | feat(index): add contact area content | \* No aplica  | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-customers| 3ccab7e | style: add styles for contact and map area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-customers | 40ba33d | style: add styles for testimonial area content | \* No aplica  | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-hero | df0b9f4 | style: add styles for features area content  | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-hero | 48b0f4b | feat(index): add features area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-hero | 4bf4b47 | feat: add me.svg into assets\images\somethings | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-hero | 26468c9 | feat: add main.svg into assets\images\somethings | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-hero | 804fd1f | style: add styles for hero area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-services | 06d709e | style: add styles for pricing area content  | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-services | f00f946 | feat: add pricing area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-services | 86704c7 | feat: add styles for services area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-services | 465a3f8 | feat: add services area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-services | 29d38ab | Merge branch 'feature-hero' into develop | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-team | 14db7cb | style: add styles for team area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-team | 9ebbce7 | feat(index): add team area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-team | 90b0bf7 | style: add styles for video area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-team | 0bbb3c9 | feat(index): add video area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-team | f00f946 | feat: add pricing area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-headersandfooter   | ede3143 | style: add footer area style content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-headersandfooter   | c755442 | feat(index): add footer area content | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-headersandfooter   | 556aeea | feat: add moveo_icon_white.svg into assets\images\logo | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-headersandfooter   | 61214ea | feat: add moveo_icon_color.svg into assets\images\logo | \* No aplica | 20/04/2025 |
| 1ASI0729-2510-4313-G4-Moveo landing\_page | feature-headersandfooter   | ff76265 | style: add content for normalize and titles from css | \* No aplica | 20/04/2025 |

#### 5.2.1.5. Execution Evidence for Sprint Review

<img src="./assets/chapter05/evidence/evidence.PNG" />

<img src="./assets/chapter05/evidence/evidence2.PNG" />

<img src="./assets/chapter05/evidence/evidence3.PNG" />

<img src="./assets/chapter05/evidence/tabla.PNG" />

<img src="./assets/chapter05/evidence/tabla2.PNG" />

<img src="./assets/chapter05/evidence/tabla3.PNG" />

#### 5.2.1.6. Services Documentation Evidence for Sprint Review
Para el Sprint 1, no se ha trabajado en la documentación de los servicios de la aplicación, ya que el enfoque principal ha sido la creación del Landing Page. No obstante, se tiene previsto desarrollar la documentación de los servicios en los próximos sprints. Sin embargo, se adjunta la url del repositorio que contenera los servicios.

URL del repositorio de Web Services: https://github.com/1ASI0729-2510-4313-G4-Moveo/backend

#### 5.2.1.7. Software Deployment Evidence for Sprint Review
Se inicio con la creación de la organización en github. 

<img src="./assets/chapter05/software-deployment-organization.png" />

Posteriormente, se asocio a los integrantes del equipo para poder colaborar en los repositorios de la organización.

<img src="./assets/chapter05/software-deployment-organization-members.png" />

Luego, se crearon los repositorios del reporte, Landing Page, Frontend y Backend para organizar los productos entregables.

<img src="./assets/chapter05/software-deployment-repositories.png" />

Finalmente, se configuro y desplegó la versión inicial del Landing Page en **GitHub Pages** desde la sección "Pages" seleccionando la rama **main**.

<img src="./assets/chapter05/landing-deployment.png" />

#### 5.2.1.8. Team Collaboration Insights during Sprint

| Participante | Actividades de implementación |
| :---- | :---- |
| Lizano Coll Cardenas, Fernando Jesus | Nav bar, About us section, Our Services, Pricing & Plans, Watch our video, Meet our team, Our Testimonials, FAQ, Contact Us, Footer|
| Gonzales Valverde | Images adaptation, Traduction en-es |
| Castañeda Guimas, Giancarlo Santiago, Trillo Hernandez, Anghel Melanie, Nikaido Vargas, Javier Masaru  | Organization fixes |

<img src="./assets/chapter05/insights/insights.PNG" />

<img src="./assets/chapter05/insights/insights2.PNG" />

### 5.2.2. Sprint 2
#### 5.2.2.1. Sprint Planning 2

**Sprint Planning Background**
<table>
  <tr>
    <th>Criterio</th>
    <th>Detalle</th>
  </tr>
  <tr>
    <td>Date</td>
    <td>2025-13-05</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>12:00pm</td>
  </tr>
  <tr>
    <td>Location</td>
    <td>Reunión Virtual en Virtual google meet</td>
  </tr>
  <tr>
    <td>Prepared By</td>
    <td>Giancarlo Castañeda</td>
  </tr>
  <tr>
    <td>Attendees (to planning meeting)</td>
    <td>Carlos Gonzales, Fernando Lizano, Javier Nikaido, Anghel Trillo</td>
  </tr>
  <tr>
    <td>Sprint 2 Review Summary</td>
    <td>Se realizó la app web, integrandole las funcionalidades core y desarrollando el diseño de esta. Para ello </td>
  </tr>
  <tr>
    <td>Sprint 2 Retrospective Summary</td>
    <td>Mejorar la puntualidad en la entrega de artefactos, optimizar la entrega de trabajos.</td>
  </tr>

**Sprint Goal & User Stories** 

| Criterio  | Detalle   |
| :-------------- | -------------------- |
| Sprint 2 Goal  | Nuestro enfoque para este sprint es implementar la landing page de nuestro producto. Creemos que esto brindará una correcta presentación de nuestro producto hacia los visitantes. Esto se confirmará cuando todas las secciones de nuestra página web sean visitadas por cada visitante.  |
| Sprint 2 Velocity            | Para este sprint nuestro equipo puende aceptar hasta 25 story points       |
| **Sum of Story Points**      | Para este sprint haremos 23 story points                                |

#### 5.2.1.2. Aspect Leaders and Collaborators

| Team Member (Last Name, First Name)  | GitHub Username | Aspect Diseño UX/UI y Prototipado (L/C) | Aspect Programación de la app web (L/C)      | Aspect Arquitectura de Información y Sistemas de Organización/Navegación (L/C) |
| ------------------------------------ | --------------- | --------------------------------------- | -------------------------------------------- | --------------------------------------------------------------------------------------------- |
| Castañeda Guimas, Giancarlo Santiago | Darksens01      | L                                       | C                                            | C                                                                                             |
| Gonzales Valverde, Carlos Matthew    | Carlos12324     | L                                       | L                                            | L                                                                                             |
| Nikaido Vargas, Javier Nikaido       | MassiFlip       | L                                       | C                                            | C                                                                                             |
| Lizano Coll Cardenas, Fernando Jesus | GuardianDeity   | L                                       | L                                            | L                                                                                             |
| Trillo Hernandez, Anghel Melanie     | AM27TH          | L                                       | L                                            | L                                                                                             |

#### 5.2.2.3. Sprint Backlog 2
| User Story | Work-Item/Task | Id | Title | Description | Estimation (Hrs) | Assigned To | Status |
|:---|:---|:---|:---|:---|:---|:---|:---|
| US01 | T1 | T1-1 | Registro de nuevos usuarios | Crear pantalla de registro de usuarios | 4 | Carlos Matthew | DONE |
| US02 | T2 | T2-1 | Inicio de sesión seguro | Creación y almacenamiento de usuarios para la pantalla inicio de sesión  | 4 | Carlos Matthew |DONE|
| US23 | T23 | T23-1 | Visualizar historial de uso | Creación y codificación de el historial de uso de los usuarios | 5 | Carlos Matthew, Javier Masaru | DONE |
| US24 | T24 | T24-1 | Visualizar y editar metodos de pago | Creación, edició y eliminación de los metodos de pago | 6 | Carlos Matthew, Javier Masaru  | DONE |
| TS01 | T6 | T6-1 | Diseño adaptable (responsive) | Realizar diseño responsive a la app web | 6 | Carlos Matthew | DONE |
| TS04 | T7 | T7-1 | Funcionalidad CRUD en la interfaz | Agregar funcionalidades CRUD a la app web  | 5 | Carlos Matthew |DONE |
| TS05 | T8 | T8-1 | Despliegue de la aplicación | Desplegar la aplicación en un entorno seguro | 5 | Carlos Matthew | DONE |
| TS06 | T9 | T9-1 | Configuración de las rutas principales | Asignar rutas para mejorar la fluidez de la app | 6 | Carlos Matthew | DONE |

#### 5.2.2.4. Development Evidence for Sprint Review
A continuación se muestran los commits realizados por los integrantes del equipo, se obviaron los merges y commits incorrectos por razones de mejor visualización acerca de los commits correctamente desarrollados e implementados:

<img src="./assets/chapter05/insights3.webp" />

#### 5.2.2.5. Execution Evidence for Sprint Review

<img src="./assets/chapter05/evidence1.webp" />

<img src="./assets/chapter05/evidence2.webp" />

<img src="./assets/chapter05/evidence3.webp" />


#### 5.2.2.6. Services Documentation Evidence for Sprint Review
Para el Sprint 2, no se ha trabajado en la documentación de los servicios de la aplicación, ya que el enfoque principal ha sido la creación del Landing Page. No obstante, se tiene previsto desarrollar la documentación de los servicios en los próximos sprints. Sin embargo, se adjunta la url del repositorio que contenera los servicios.

URL del repositorio de Web Services: https://github.com/1ASI0729-2510-4313-G4-Moveo/backend

#### 5.2.2.7. Software Deployment Evidence for Sprint Review
Para esta entrega no pudimos realizar el deploy, intentaremos realizarlo para la siguiente entrega

#### 5.2.2.8. Team Collaboration Insights during Sprint

<img src="./assets/chapter05/insights1.webp" />

<img src="./assets/chapter05/insights2.webp" />


| Participante | Actividades de implementación |
| :---- | :---- |
| Castañeda Guimas, Giancarlo Santiago, Trillo Hernandez, Anghel Melanie, Nikaido Vargas, Javier Masaru | Organization fixes |
| Carlos Matthew | Creación de la app web |

## Conclusiones

- **Solución a una necesidad real:**
<br>Moveo logra cubrir la necesidad de movilidad flexible para trabajadores y turistas, ofreciendo una alternativa económica y conveniente frente al transporte público o taxis tradicionales.

- **Segmentación clara y efectiva:**
<br>Definir segmentos específicos (trabajadores y proveedores) permitió construir funcionalidades enfocadas que mejoran la experiencia de usuario de cada grupo.

- **Importancia de la experiencia de usuario:**
<br>El diseño UX/UI planteado en Figma priorizó la facilidad de uso, logrando flujos de navegación intuitivos y rápidos que favorecen el registro, reserva y provisión de autos.

- **Gestión técnica sólida:**
<br>La arquitectura propuesta en Structurizr permitió visualizar una estructura robusta de servicios, incluyendo pagos, historial de viajes y calificaciones, lo que garantiza escalabilidad para futuros crecimientos.

- **Trabajo colaborativo fundamental:**
<br>La construcción del proyecto demostró que una buena comunicación y división de tareas entre diseño, análisis y desarrollo es clave para avanzar de forma ágil y ordenada.

- **Futuro prometedor para Moveo:**
<br>El modelo de negocio y la plataforma tecnológica sentada en este proyecto tienen potencial para expandirse y consolidarse como un servicio de movilidad urbana relevante en el mercado.

## Recomendaciones
- **Fortalecer el trabajo en equipo:**
<br>Es importante mantener reuniones frecuentes y retrospectivas para revisar avances, identificar bloqueos y distribuir tareas de manera equitativa y estratégica.

- **Documentar todo el proceso:**
<br>Para proyectos futuros, registrar decisiones, cambios y justificaciones técnicas facilitará nuevas incorporaciones de miembros al equipo y reducirá la curva de aprendizaje.

- **Validación temprana con usuarios reales:**
<br>Antes de lanzar completamente, realizar pruebas piloto o MVP con usuarios reales permitirá ajustar funcionalidades, precios y flujos de manera basada en evidencia.

- **Actualización constante de la infraestructura:**
<br>Planificar actualizaciones periódicas en la API, seguridad de pagos y bases de datos asegurará que Moveo se mantenga competitivo y protegido frente a nuevas amenazas tecnológicas.

- **Ampliar la cultura de feedback:**
<br>Promover una cultura donde todos los miembros puedan dar y recibir feedback sincero, respetuoso y enfocado en mejorar el producto, ayuda a fortalecer la calidad final del trabajo.

- **Explorar futuras integraciones:**
<br>A largo plazo, considerar integrar Moveo con servicios externos como mapas inteligentes, seguros de viaje automáticos o asociaciones con parkings privados podría ampliar las fuentes de ingreso y la propuesta de valor.

## Referencias bibliográficas
- Ries, E. (2011). The Lean Startup: How Today's Entrepreneurs Use Continuous Innovation to Create Radically Successful Businesses. Crown Business.
https://www.amazon.com/Lean-Startup-Entrepreneurs-Continuous-Innovation/dp/0307887898

- Brown, T. (2009). Change by Design: How Design Thinking Creates New Alternatives for Business and Society. Harvard Business Press.
https://www.amazon.com/Change-Design-Creates-Alternatives-Business/dp/1422177807

- Katzenbach, J., & Smith, D.(1993). The Wisdom of Teams: Creating the High-Performance Organization. Harvard Business Review Press.
https://www.amazon.com/Wisdom-Teams-Creating-High-Performance-Organization/dp/0875843670

- Gehl, J. (2010). Cities for People. Island Press.
https://islandpress.org/books/cities-people

- Norman, D. A. (2013). The Design of Everyday Things: Revised and Expanded Edition. Basic Books.
https://www.basicbooks.com/titles/don-norman/the-design-of-everyday-things/9780465050659/
## Anexos

## Anexo A: Diseño y Landing: 

### Figma
- [Figmas diseño UX]()

### Landing Page
- [Landing Page desplegada](https://1asi0729-2510-4313-g4-moveo.github.io/Landing-Page/)

### Domain-Driven Software Architecture / C4 Diagrams
- [Link a Structurizr](https://structurizr.com/share/93082/63f18b90-16d9-4bde-8f03-5c4cea943181)

### Flujos y Prototype

- [link a wireflow diagrams](https://lucid.app/lucidchart/9cdef739-cc7e-4c87-bd8e-6bffdbcd0134/edit?view_items=BhmasF0meFeN&invitationId=inv_5f89d871-f295-4b3e-9348-cf5af6ab0940)

- [link a userflow diagrams Parte 1](https://lucid.app/lucidchart/41a45b15-a31f-4d40-8b54-ae29cbfd528a/edit?viewport_loc=-23%2C72%2C2237%2C1109%2CbLmanzMPT3G7&invitationId=inv_e3d6bee7-388c-4adb-afaa-053ebb2be412)

- [link a userflow diagrams Parte 2](https://lucid.app/lucidchart/cdc929f2-25ef-4684-b019-5a526f18bb35/edit?viewport_loc=-1550%2C-1351%2C5798%2C3748%2C0_0&invitationId=inv_b19dc14a-c643-4ee4-901c-78e25fad7cd7)

- [link a prototype](https://www.figma.com/proto/nrxEj7WzMbOci6Qe0h9zGO/Untitled?node-id=1-49&t=OV9Jld3INRoD278N-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A49)

<div style="page-break-after: always; break-after: page;"></div>

## Anexo B: Videos de exposiciones: 
- [Link a video de exposición de TB1 en Microsoft Stream]()
