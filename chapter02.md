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

# Capítulo II: Requirements Elicitation & Analysis
## 2.1. Competidores
Para esta sección analizaremos y compararemos a diversos competidores que pudimos llegar a encontrar para así transferir conocimiento detectando las mejores opciones y prácticas que aplicar para nuestra aplicación.

-   Los competidores se pueden dividir en varios tipos, como los que hacen exactamente lo mismo que nosotros, los que no hacen lo mismo pero pueden llegar a solucionarlo, los de mayor rango que serían los que consideramos que estamos muy lejos de alcanzarlos, etc.
    

En este caso solo nos quedaremos con 3 que pensamos que serían los más óptimos observar:

-   Plataforma Web “Reizen”
    
-   Plataforma Web “SnappCar”
    
-   Aplicación “InDrive”
    

A continuación realizaremos el análisis necesario para ver qué estrategias podemos tomar para sobresalir entre ellos

|Categorias| **Moveo**|**Reizen**|**SnappCar**| InDrive|
|--------|-------|-------|--------|------|
|**Overview**|App open source que conecta a trabajadores y dueños de autos para alquiler autónomo sin intermediarios humanos|Plataforma peer-to-peer para alquiler de autos, yates y alojamientos|Plataforma europea peer-to-peer de alquiler de autos privados con apertura remota y seguro incluido|App de transporte bajo modelo C2C, donde conductor y usuario negocian el precio directamente|
|**Ventaja competitiva  <br>¿Qué valor ofrece a los clientes?**|Open source: flexibilidad y adaptación local; sin intermediarios físicos; integración de mapas y puntos de entrega|Comunidad local consolidada, confianza social basada en reviews y cercanía geográfica|Tecnología avanzada: apertura remota, seguro integrado, fuerte presencia en Europa|Precios negociados, baja comisión, red de usuarios grande y activa, crecimiento exponencial en LATAM|
 |**Mercado objetivo**|Trabajadores urbanos y dueños de autos subutilizados en LATAM|Usuarios en Colombia interesados en movilidad ocasional y propietarios buscando ingresos extra|Europeos en ciudades con alta cultura de carsharing|Usuarios que buscan transporte flexible en LATAM y otras regiones emergentes|
|**Estrategias de marketing**|Crecimiento orgánico a través de la comunidad Open Source, partnerships con estacionamientos y empresas|Publicidad en redes sociales locales, confianza de usuarios vía testimonios|Inversión en marketing digital y acuerdos con aseguradoras locales|Modelo viral de boca a boca y crecimiento por recomendaciones; marketing en apps|
|**Productos & Servicios**| Alquiler de autos peer-to-peer, apertura remota, elección de punto de entrega personalizado en la app|Alquiler peer-to-peer de autos, yates y propiedades|Alquiler peer-to-peer de autos privados, seguro, servicio sin contacto humano|Transporte urbano: usuarios y conductores fijan tarifas en tiempo real|
|**Precios & Costos**| - 25-40 USD/día promedio (dependiendo del modelo y zona) |20-45 USD/día promedio (varía según vehículo y ciudad)|30-60 USD/día promedio + seguro (obligatorio)|Tarifas por trayecto negociadas directamente; media en LATAM: 2-7 USD por trayecto|
|**Canales de distribución (Web y/o Móvil)**|App móvil y sitio web.|App móvil y sitio web.|-App móvil y sitio web|App móvil (Android / iOS) y crecimiento viral por referidos|
|**Fortalezas**|Open Source (adaptabilidad y comunidad), modelo autónomo sin personal intermediario, flexibilidad para proveedores y usuarios|Modelo probado en LATAM, marca local conocida, confianza comunitaria fuerte|Tecnología avanzada, seguro incluido, base de usuarios estable|Red de usuarios global, precios competitivos, crecimiento orgánico en LATAM|
|**Debilidades**|Requiere una masa crítica de autos y usuarios para funcionar; dependencia de proveedores locales|Limitado a Colombia; poca escalabilidad fuera de su mercado de origen|Fuerte enfoque en Europa, alta barrera de entrada en otros mercados| - No ofrece alquiler de autos, solo transporte personal <br> - Suele demorar mucho y los precios son elevados en ciertos puntos|
|**Oportunidades**|Asociaciones con empresas y estacionamientos; modelo replicable en ciudades emergentes|Expandir a otros países; diversificar más allá de autos (ya incluye yates y alojamiento)|Expansión a otros continentes, integración con plataformas de movilidad smart city|Ampliar servicios a carsharing o alquiler de autos autónomos|
|**Amenazas**|Alta competencia, proveedores limitados en fases iniciales, cambios regulatorios|Nuevos entrantes y modelos de negocio Open Source como Moveo|Competencia local y competencia externa fuerte|Cambios regulatorios en transporte urbano; competencia de apps como Uber y Lyft|

### 2.1.2. Estrategias y tácticas frente a competidores
-   Se realizarán diversas entrevistas con nuestros segmentos objetivos para comprobar si nuestra idea les parece razonable y si estarían dispuestos a probarla.
    
-   Con base en los resultados de la investigación, implementaremos las ideas más innovadoras que saquemos e intentemos acoplarlos a nuestra aplicación.
    
-   Buscaremos una diferenciación clara con nuestros competidores, intentaremos destacar en la autonomia y libertad que puede ofrecer nuestro producto a la hora de desplazarse.
    
-   Los propietarios de autos que no usan sus vehiculos constantemente son un mercado muy poco atendido que creemos que podemos captar antes de que crezcan nuestros competidores
    
-   Cada vez más usuarios valoran la flexibilidad de tener un auto solo por horas o días sin asumir costos de propiedad, creemos que nuestra app podria ser de gusto para ellos

## 2.2. Entrevistas
### 2.2.1. Diseño de entrevistas
Para las preguntas decidimos antes de todo explicar de qué va nuestro tema, las entrevistas contarán con un tiempo de entre 10 a 15 minutos o la disposición del entrevistado el cual puede cancelar la entrevista en cualquier momento lo desee.

**Para segmento objetivo trabajadores urbanos**

1. Cuéntame cómo es tu rutina diaria cuando necesitas trasladarte de un lugar a otro. ¿Qué medios usas?

2. ¿En qué medio de transportes vas usualmente?

3. ¿En qué situaciones sientes que el transporte que usas no es suficiente o no cumple tus necesidades?

4. ¿Qué factores consideras antes de elegir cómo moverte a tu destino? (Ej. tiempo, costo, comodidad)

5. ¿Qué tan importante es para ti tener autonomía y flexibilidad en tus traslados diarios?

6. ¿Has tenido que pedir prestado un vehículo a amigos o familiares? Cuéntame cómo fue esa experiencia.

7. Cuando tu transporte habitual no está disponible, ¿cómo sueles resolverlo?

8. ¿Cómo te sientes cuando dependes de transporte público o de terceros para llegar a tiempo?

9. Imagina que tienes acceso a un vehículo solo cuando lo necesitas, ¿cómo crees que cambiaría tu día a día?

10. ¿Qué aspectos te harían confiar en una nueva solución de movilidad que te dé más independencia?

**Para segmento objetivo proveedor de autos**

1. En tu día a día, ¿con qué frecuencia utilizas tu auto? ¿Sientes que pasa mucho tiempo estacionado?

2. ¿Qué significa para ti tener un auto? ¿Lo ves más como una inversión, una herramienta o un metodo para tener más libertad?

3. Si tu auto pudiera generarte ingresos cuando no lo usas, ¿qué pensarías de esa posibilidad?

4. ¿Qué condiciones te harían sentir seguro al permitir que otras personas usen tu auto temporalmente?

5. ¿Alguna vez has pensado en formas de obtener ganancias adicionales a partir de las cosas que ya posees? ¿Cómo te ha ido?

6. ¿Conoces a alguien que haya logrado sacarle provecho a su auto aparte de la movilización? (Ejm. Uber, InDrive o rentandolo mismamente)

7. En otros países es común que las personas renten sus autos de forma flexible. ¿Te imaginas que eso pueda funcionar aquí?

8. ¿Qué sentirías si, en lugar de tener tu auto estacionado, pudiera ayudarte a cubrir parte de tus gastos mensuales?

9. ¿Qué características crees que debería tener una plataforma para que sientas que tu auto está protegido cuando lo usa otra persona?

10. ¿Cómo te sentirías al formar parte de una red donde los autos que no están siendo utilizados se ponen a disposición de personas que los necesitan?

### 2.2.2. Registro de entrevistas
| Segmento Objetivo | Trabajador Urbano |
| ----- | ----- |
| **Número de registro** | **Datos del entrevistado** |
| 01 | **Nombre:** Juan Diego <br>**Edad:** 19 <br>**Profesión:** Estudiante Universitario **Distrito:** Santiago de Surco <br>**Inicio \- Duración:** 0:00 \- 5:02 <br>**Enlace de la entrevista: [upc-pre-202510-1asi0730-4374-GPT4-needfinding-sprint-1.mp4](https://upcedupe-my.sharepoint.com/personal/u202310601_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202310601%5Fupc%5Fedu%5Fpe%2FDocuments%2FMoveo%20entrevista%202%20%28Trabajador%29%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2E58a1182c%2D9ba7%2D40ae%2D937b%2Dddd720ff42e0)** |
|  | **Resumen:** Juan Diego no posee auto propio y depende del transporte público para sus desplazamientos diarios, lo que considera una experiencia tediosa e insegura debido al tráfico, la informalidad y las rutas ineficientes. Valora altamente la autonomía y la flexibilidad que otorga conducir un vehículo propio, ya que permite controlar los tiempos de traslado. Ha tenido experiencias positivas alquilando autos en su familia y resalta su preferencia por no depender de terceros para movilizarse. Considera que una aplicación como Moveo podría cambiar su rutina, especialmente en situaciones de urgencia. Sin embargo, recalca que confiaría más en la plataforma si los autos ofrecidos cumplen con requisitos de seguridad como tener documentos en regla (SOAT, revisión técnica) y verificaciones legales.  |
| 02 | **Nombre:** Sebastian Hernandez <br>**Edad:** 20 <br>**Profesión:** Estudiante y desarrollador de aplicaciones <br>**Distrito:** San Juan de Lurigancho <br>**Inicio \- Duración:** 0:00 \- 3:12 <br>**Enlace de la entrevista: [upc-pre-202510-1asi0730-4374-GPT4-needfinding-sprint-2.mp4](https://upcedupe-my.sharepoint.com/personal/u202314130_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202314130%5Fupc%5Fedu%5Fpe%2FDocuments%2Fupc%2Dpre%2D202510%2D1asi0730%2D4374%2DGPT4%2Dneedfinding%2Dsprint%2D2%2Emkv&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Ef11b75c1%2D3ac6%2D4c49%2Da036%2D38e9203293af&isDarkMode=false)** |
|  | **Resumen:** Sebastián utiliza principalmente el tren y las combis como medios de transporte, pero reconoce que enfrentarse al tráfico y a la falta de comodidad es una constante en su rutina diaria. Al elegir un medio de transporte prioriza el costo, la comodidad y el tiempo de traslado. Destaca que la autonomía y la flexibilidad son muy importantes para él, ya que le permitirían optimizar sus rutas y tiempos. Actualmente no ha tenido que pedir prestado un vehículo, pero cuando su transporte habitual no está disponible, busca rutas alternativas o utiliza taxis. Considera que depender del transporte público es frustrante por la falta de fiabilidad y los problemas de aforo. Sebastián cree que tener acceso a un vehículo solo cuando lo necesite mejoraría significativamente su calidad de vida, y confiaría en una solución de movilidad que garantice eficiencia y seguridad.|
| 03 | **Nombre:**  Itzel Cortegana <br>**Edad:** 19 <br>**Profesión:** Administradora <br>**Distrito:** Chorrillos <br>**Inicio \- Duración:** 0:00 \- 3:54 <br>**Enlace de la entrevista: [upc-pre-202510-1asi0730-4374-GPT4-needfinding-sprint-3.mkv](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202314130_upc_edu_pe/EZOrUFB7B99PobtZuAQfQycBRLow34wk0y9zQZbjoXXg2A?e=xxRlhb&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)** |
|  | **Resumen:** Itzel utiliza principalmente el Metropolitano para trasladarse, considerando también combis y aplicaciones de taxi en ocasiones. Identifica como principales problemas el tráfico, la sobrecarga de pasajeros y la inseguridad cuando debe movilizarse de noche. Al elegir un medio de transporte prioriza el tiempo, el costo, la seguridad y la comodidad. La autonomía y la flexibilidad son muy importantes para ella, ya que desea moverse sin depender de horarios fijos ni congestión. Ha pedido vehículos prestados en ocasiones urgentes, pero considera que no es una solución permanente. Siente estrés y pérdida de tranquilidad al depender del transporte público. Itzel opina que una aplicación como Moveo mejoraría su calidad de vida, dándole independencia y seguridad, siempre que sea fácil de usar, accesible en su zona, que los vehículos estén en buen estado y que haya soporte rápido ante cualquier inconveniente.|
| **Segmento Objetivo** | **Proveedor de Auto** |
| **04** | **Nombre:** Christian Trillo <br>**Edad:** 45 <br>**Profesión:** Empresario <br>**Distrito:** Santiago de Surco <br>**Inicio \- Duración:** 0:00 - 5:13 <br>**Enlace de la entrevista: [upc-pre-202510-1asi0730-4374-GPT4-needfinding-sprint-4](https://upcedupe-my.sharepoint.com/personal/u201912401_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu201912401%5Fupc%5Fedu%5Fpe%2FDocuments%2FMoveo%20proveedor%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Ee3112f1d%2D3a22%2D4ddc%2D99e5%2Dff0745ff84ea)** |
|  | **Resumen:** Christian menciona que utiliza su auto, pero reconoce que pasa periodos estacionado sin ser aprovechado. Considera su vehículo una herramienta útil para movilizarse y ve positivamente la posibilidad de generar ingresos alquilándolo. Indica que para sentirse seguro permitiría el alquiler solo si se garantizan aspectos como un domicilio estable del arrendatario, garantías de buen uso, y la posibilidad de rastrear el vehículo mediante GPS. También conoce casos de conocidos que han alquilado autos, aunque con experiencias mixtas respecto al cuidado de los vehículos. Opina que el modelo de alquiler flexible podría funcionar en el país, sobre todo para optimizar tiempos libres y generar ingresos adicionales. Se mostró interesado en la propuesta de integrar su vehículo a una red de autos compartidos. |
| **05** | **Nombre:** Daniel Rodríguez <br>**Edad:** 19 <br>**Profesión:** Estudiante Universitario <br>**Distrito:** Santiago de Surco <br>**Inicio \- Duración:** 0:00 \- 7:19 <br>**Enlace de la entrevista: [upc-pre-202510-1asi0730-4374-GPT4-needfinding-sprint-5.mp4](https://upcedupe-my.sharepoint.com/personal/u202310601_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202310601%5Fupc%5Fedu%5Fpe%2FDocuments%2FEntrevista%201%20Moveo%20%28Proveedor%29%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2E9b52e82e%2D24a3%2D4187%2D942d%2Db0e766c58ba5)** |
|  | **Resumen:** Daniel es propietario de un auto que utiliza diariamente para movilizarse, principalmente a la universidad y actividades personales. Considera el auto una herramienta que proporciona comodidad y libertad, además de un lujo. Aunque no ha buscado anteriormente formas de obtener ingresos extra con sus posesiones, reconoce que un auto podría ser rentable, y comenta que tiene familiares que han trabajado como taxistas usando sus propios vehículos. Considera viable el modelo de alquiler flexible propuesto por Moveo, destacando la necesidad de contar con seguros que cubran daños externos e internos, además de medidas de seguridad contra robos y verificación de identidad de los arrendatarios. Señala que, si tuviera una flota de autos, definitivamente utilizaría una plataforma como Moveo para generar ingresos adicionales.  |
|**06**| **Nombre:** Luis Sebastian Ortiz <br>**Edad:** 19 <br>**Profesión:** Estudiante de Ingeniería de Software <br>**Distrito:** San Juan de Miraflores **Inicio \- Duración:** 0:00 \- 5:06 <br>**Enlace de la entrevista: [upc-pre-202510-1asi0730-4374-GPT4-needfinding-sprint-6.mp4](https://upcedupe-my.sharepoint.com/personal/u202310601_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202310601%5Fupc%5Fedu%5Fpe%2FDocuments%2FEntrevista%203%20Moveo%20%28Proveedor%29%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Edee3535a%2D73ab%2D41fb%2D93d1%2D07f527161fd2)** |
|  | **Resumen:** Sebastian es propietario de un vehículo que utiliza cuando necesita movilizarse. Considera que tener un auto representa libertad personal, además de ser un gusto propio. Ha considerado previamente la posibilidad de obtener ingresos extra prestando su vehículo, aunque también ha explorado otras formas de ingresos pasivos como prestar cuentas. Manifiesta que para sentirse seguro prestando su auto sería esencial que la empresa se responsabilice de cualquier daño ocasionado por los arrendatarios. Tambien sugiere que la plataforma incluya la ubicación en tiempo real del vehículo para mayor seguridad. Cree que si se garantiza la seguridad tanto del vehículo como del conductor, la aplicación Moveo tendría éxito en Perú. Si prestaria su auto en el futuro si se cumplen las condiciones de seguridad. |
### 2.2.3. Análisis de entrevistas
## 2.3. Need finding
### 2.3.1. User Person
#### Segmento 1: Trabajador urbano
<img src="assets/chapter2/User persona - Trabajador.png">

#### Segmento 2: Proveedor de auto
<img src="assets/chapter2/User persona - Proveedor.png">

### 2.3.2. User Task Matrix

#### Trabajador Urbano

Esta tabla resume las principales actividades que realiza un usuario trabajador urbano, quien necesita soluciones eficientes para sus desplazamientos cotidianos por la ciudad, especialmente hacia su trabajo.

----------
|Task|Importancia|Frecuencia|
|-----|--------------|---------|
|Buscar rutas eficientes para ir al trabajo|High|Daily|
|Comparar precios entre opciones de movilidad|High|Daily|
|Reservar transporte de manera rápida y segura|High|Many|
|Verificar el tiempo estimado de llegada y condiciones del tráfico|High|Many|
|Valorar o calificar el servicio recibido|Moderate|Rare|
|Guardar rutas favoritas|Low|Rare|
|Contactar al proveedor en caso de incidencias|Moderate|Rare|



#### Proveedor de Auto

Esta tabla resume las tareas que realiza un proveedor de auto (persona que ofrece su vehículo como opción de transporte), cuyo objetivo es monetizar su vehículo maximizando su uso.

------
|Task|Importancia|Frecuencia|
|-----|--------------|---------|
|Registrar el vehículo en la plataforma|High|Rare|
|Establecer horarios de disponibilidad|High|Weekly|
|Gestionar solicitudes y reservas de viajes|High|Many|
|Verificar datos del pasajero antes del viaje|Moderate|Many|
|Recibir pagos de manera segura|Moderate|Many|
|Consultar estadísticas de uso e ingresos|Moderate|Weekly|
|Calificar a los usuarios después del viaje|Low|Rare|
|Modificar la disponibilidad o condiciones del servicio|Moderate|Weekly|

### 2.3.3. User Journey Mapping
#### Segmento 1: Trabajador urbano
<img src="assets/chapter2/User journey map - trabajador.png">

#### Segmento 2: Proveedor de auto
<img src="assets/chapter2/User journey map - proveedor.png">

### 2.3.4. Empathy Mapping

#### Segmento 1: Trabajador urbano
<img src="assets/chapter2/Trabajador - Empathy map.png">

#### Segmento 2: Proveedor de auto
<img src="assets/chapter2/Proveedor - Empathy map.png">

### 2.3.5. As-is Scenario Mapping

#### Segmento 1: Trabajador urbano
<img src="assets/chapter2/As-Is Trabajador.png">

#### Segmento 2: Proveedor de auto
<img src="assets/chapter2/As-Is Proveedor.png">

## 2.4. Ubiquitous Language.
| **Término (Inglés)** |**Término (Español)** | **Definición** |
|-------------------------|--------------------------|-------------------|
|Vehicle Provider |Proveedor de Vehículo|Persona que ofrece su auto personal para ser alquilado mediante la aplicación Moveo|
|Renter|Arrendatario / Usuario|Persona que alquila un vehículo disponible mediante la plataforma para su transporte|
|Fixed Rate|Tarifa Fija|Monto económico predeterminado que un usuario paga por el uso del vehículo en un periodo|
|Delivery Point|Punto de Entrega|Lugar físico, mostrado en el mapa, donde el auto es dejado por el proveedor para el usuario|
|Parking Hub|Centro de Estacionamiento|Estacionamiento asociado al sistema donde se permite el intercambio o almacenamiento de autos|
|Remote Unlock|Desbloqueo Remoto|Funcionalidad que permite abrir y cerrar el vehículo usando la aplicación sin contacto físico|
|Available Vehicle|Vehículo Disponible|Auto que ha sido ofrecido por un proveedor y se encuentra visible para ser rentado en la aplicación|
