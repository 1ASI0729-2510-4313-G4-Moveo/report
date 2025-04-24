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

<img src="./assets/chapter5/gitflow.png" />

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

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

### 5.1.4. Software Deployment Configuration
Para la realizacion del despliegue debemos seguir los siguientes pasos:
  1. Primero, creamos un nuevo [repositorio en GitHub](https://github.com/1ASI0729-2510-4313-G4-Moveo/Landing-Page). Después, subimos los archivos del  proyecto a ese repositorio.
  2. Una vez que se haya subido todo, nos dirigimos a la configuración del repositorio. Allí, buscamos la sección de **"Pages"**, que aparece en la barra lateral izquierda.
  3. Luego, se vera una opción que permite seleccionar la rama desde la cual quieres hacer el despliegue. Normalmente, se elige **main**.
  4. Después de esto, GitHub generará automáticamente una URL para tu sitio.
<br>
<img src="./assets/chapter5/landing-deployment.png" />

## 5.2. Landing Page, Services & Applications Implementation
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1
#### 5.2.1.2. Aspect Leaders and Collaborators
#### 5.2.1.3. Sprint Backlog 1
#### 5.2.1.4. Development Evidence for Sprint Review
#### 5.2.1.5. Execution Evidence for Sprint Review
#### 5.2.1.6. Services Documentation Evidence for Sprint Review
Para el Sprint 1, no se ha trabajado en la documentación de los servicios de la aplicación, ya que el enfoque principal ha sido la creación del Landing Page. No obstante, se tiene previsto desarrollar la documentación de los servicios en los próximos sprints. Sin embargo, se adjunta la url del repositorio que contenera los servicios.

URL del repositorio de Web Services: https://github.com/1ASI0729-2510-4313-G4-Moveo/backend

#### 5.2.1.7. Software Deployment Evidence for Sprint Review
Se inicio con la creación de la organización en github. 

<img src="./assets/chapter5/software-deployment-organization.png" />

Posteriormente, se asocio a los integrantes del equipo para poder colaborar en los repositorios de la organización.

<img src="./assets/chapter5/software-deployment-organization-members.png" />

Luego, se crearon los repositorios del reporte, Landing Page, Frontend y Backend para organizar los productos entregables.

<img src="./assets/chapter5/software-deployment-repositories.png" />

Finalmente, se configuro y desplegó la versión inicial del Landing Page en **GitHub Pages** desde la sección "Pages" seleccionando la rama **main**.

<img src="./assets/chapter5/landing-deployment.png" />

#### 5.2.1.8. Team Collaboration Insights during Sprint
## 5.3. Validation Interviews
### 5.3.1. Diseño de Entrevistas
### 5.3.2. Registro de Entrevistas
### 5.3.3. Evaluaciones según heurísticas
## 5.4. Video About-the-Product

## Conclusiones
## Referencias bibliográficas
## Anexos
