# Report Iot

![logo](src/images/logo.webp)

Carrera: Ingeniería de Software

Nombre del curso: Desarrollo de Soluciones IOT

Sección: WV71

Nombre del profesor: Velasquez Nuñez, Angel Augusto

"Informe de TB1"

Nombre del startup: VerySafe

Nombre del producto: FalconShield

Relación de integrantes:

- Gabriela Soledad Nomberto Ramos
- Dennis Piero Quevedo Yucra
- Max Dayson Sabino Arostegui
- Elvia Guadalupe Arteaga Cruz
- Jamutaq Piero Ortega Vélez

Mes y año: Agosto 2024

Ciclo: 2024-2

## Registro de Versiones del Informe
# Student Outcome
# CAPÍTULO I: INTRODUCTION
## 1.1 Startup Profile
### 1.1.1 Descripción de la Startup
### 1.1.2 Perfiles de integrantes del equipo
## 1.2 Solution Profile
### 1.2.1  Antecedentes y problemática
### 1.2.2 Lean UX Process
#### 1.2.2.1 Lean UX Problem Statements
#### 1.2.2.2 Lean UX Assumptions
#### 1.2.2.3 Lean UX Hypothesis Statements
#### 1.2.2.4 Lean UX Canvas
## 1.3 Segmentos objetivo

# CAPÍTULO II: REQUERIMENTS ELICITATION & ANALYSIS
## 2.1 Competidores
### 2.1.1. Análisis competitivo
## 2.2 Entrevistas
### 2.2.1. Diseño de entrevistas
### 2.2.2. Registro de entrevistas
### 2.2.3. Análisis de entrevistas
## 2.3 Needfinding
### 2.3.1. User Personas
### 2.3.2. User Task Matrix
### 2.3.3. User Journey Mapping
### 2.3.4. Empathy Mapping
### 2.3.5. As-Is Scenario Mapping
## 2.4. Ubiquitous Language

# CAPÍTULO III: REQUIREMENTS SPECIFICATION
## 3.1. To-Be Scenario Mapping.
## 3.2. User Stories.
## 3.3. Impact Mapping.
## 3.4. Product Backlog.

# CAPÍTULO IV: SOLUTION SOFTWARE DESIGN
## 4.1. Strategic-Level Domain-Driven Design
### 4.1.1. EventStorming
#### 4.1.1.1 Candidate Context Discovery
#### 4.1.1.2 Domain Message Flows Modeling
#### 4.1.1.3 Bounded Context Canvases
### 4.1.2. Context Mapping
### 4.1.3. Software Architecture
#### 4.1.3.1. Software Architecture System Landscape Diagram
#### 4.1.3.2. Software Architecture Context Level Diagrams
#### 4.1.3.2. Software Architecture Container Level Diagrams
#### 4.1.3.3. Software Architecture Deployment Diagrams
## 4.2. Tactical-Level Domain-Driven Design
### 4.2.X. Bounded Context: <Bounded Context Name>
#### 4.2.X.1. Domain Layer
#### 4.2.X.2. Interface Layer
#### 4.2.X.3. Application Layer
#### 4.2.X.4. Infrastructure Layer
#### 4.2.X.5. Bounded Context Software Architecture Component Level Diagrams
#### 4.2.X.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.X.6.1. Bounded Context Domain Layer Class Diagrams
##### 4.2.X.6.2. Bounded Context Database Design Diagram

# CAPÍTULO V: SOLUTION UI/UX DESIGN
## 5.1. Style Guidelines
### 5.1.1. General Style Guidelines
### 5.1.2. Web, Mobile and IoT Style Guidelines
## 5.2. Information Architecture
### 5.2.1. Organization Systems
### 5.2.2. Labeling Systems
### 5.2.3. SEO Tags and Meta Tags
### 5.2.4. Searching Systems
### 5.2.5. Navigation Systems
## 5.3. Landing Page UI Design
### 5.3.1. Landing Page Wireframe
### 5.3.2. Landing Page Mock-up
## 5.4. Applications UX/UI Design
### 5.4.1. Applications Wireframes
### 5.4.2. Applications Wireflow Diagrams
### 5.4.2. Applications Mock-ups
### 5.4.3. Applications User Flow Diagrams
## 5.5. Applications Prototyping

# CAPÍTULO VI: PRODUCT IMPLEMENTATION, VALIDATION & DEPLOYMENT
## 6.1. Software Configuration Management
### 6.1.1. Software Development Environment Configuration
### 6.1.2. Source Code Management
### 6.1.3. Source Code Style Guide & Conventions
Aquí el equipo explica e indica las referencias que adoptará para nombrar elementos y programar en los lenguajes que se utilizan en la solución (en este caso HTML, CSS, JavaScript, TypeScript, Java, C#, Kotlin, Swift, u otros según los contraints del proyecto; así como Gherkin para los archivos .feature). Para todos los lenguajes debe aplicar la nomenclatura en inglés. Adicionalmente, adopte convenciones estándares para coding (Vea por ejemplo “HTML Style Guide and Coding Conventions”, “Google HTML/CSS Style Guide”, “Gherkin Conventions for Readable Specifications”, “Angular coding style guide”, “Google Java Style Guide”, “Google TypeScript Style Guide” y “Spring Boot Features” en la sección de Referencias).

A continuación, se darán a conocer las convenciones, formatos, estilos y entre otras propiedades de los lenguajes trabajados en la presente solución las cuales son: HTML, JavaScript/TypeScript, Java y CSS. Además, por el lado de las pruebas de aceptación también se darán a conocer dichos temas para el lenguaje Gherkin.

**HTML:** Se hará uso de la guía “HTML Style Guide and Coding” de la página W3Schools, la cual menciona las convenciones y estándares de este lenguaje de etiquetas. Hemos considerado las siguientes como las más importantes:

- _Declarar siempre el tipo documento:_ Es decir, colocar siempre la etiqueta \<!DOCTYPE html\> en la primera línea del código.
- _Utilizar el nombre de las etiquetas y sus atributos en minúscula:_ Por un tema de estética y orden del código para que este se vea más limpio y sea más fácil de escribir.
- _Cerrar todas las etiquetas:_ Esto evita futuros problemas o errores de sintaxis.
- _Siempre coloca comillas para los valores de los atributos de las etiquetas:_ De esta forma los valores son más fáciles de leer y se deben utilizar obligatoriamente si este contiene espacios.
- _Especificar siempre los atributos alt, width y height para las imágenes:_ Es importante en caso de que la imagen no se pueda mostrar por algún motivo y también ayuda con el tema de la accesibilidad de los usuarios.
- _No omitir la etiqueta \<title\> ni los metadatos (\<meta\>):_ Estas etiquetas son importantes para la optimización de motores de búsqueda (SEO).

**CSS:** Se siguió la guía “Google HTML/CSS Style Guide” donde se indican las convenciones, reglas y buenas prácticas para este lenguaje. Hemos considerado las siguientes recomendaciones como las más destacadas:

- _Nombre de clases:_ Se recomienda usar nombres generales para las clases, no deben ser específicas por la razón de que deben comportarse como padres.
- _Usar nombres de clase cortos:_ Se recomienda utilizar nombres de clase que sean cortos y descriptivos, para transmitir la idea de lo que representa de manera concisa.
- _Usar delimitadores de nombres de clase adecuados:_ Se debe de separar las palabras en los nombres de clase con solo guiones.
- _Evitar los selectores de ID:_ No se recomienda implementar este tipo de selectores, por la razón de que estos deben ser únicos en toda la página y en proyectos grandes que tengan muchos componentes es difícil de garantizar esa unicidad, es preferible usar selectores de clase.
- _Usar propiedades abreviadas:_ Es muy recomendable usar propiedades que soporten ser declarados de forma abreviada (por ejemplo, la propiedad padding, margin, border, etc.) por la razón de que reduce de forma significativa la cantidad de líneas de código, y es más legible para el programador o diseñador.

**JavaScript:** Se consideró importante seguir una guía de buenas prácticas para un mejor desarrollo del código, para este caso se eligió la guía de la wiki “JavaScript best practices“ del World Wide Web (W3C). Lo cual se destaca lo siguiente:

- _Usar nombres cortos y fáciles de leer:_ Es recomendable nombrar adecuadamente las variables, clases, funciones y otros elementos para que sea más sencillo de leer y comprender.
- _Evitar el uso de variables globales (keyword “var”):_ No se recomienda el uso de este tipo de variables en un proyecto, porque pueden generar muchos errores a medida que el proyecto crece y estas pueden sobrescribirse fácilmente afectando el valor y se pueden declarar otros elementos como funciones con el mismo nombre de la variable y generar errores.
- _Comentar y documentar lo necesario:_ Se recomienda comentar líneas de código que son complejos de entender a simple vista explicando o dejando mensajes para que otros programadores lo entiendan.
- _Usar notaciones sencillas de entender:_ Javascript cuenta con diversas notaciones y operadores para crear o modificar ciertas estructuras de datos como objetos, arrays, selectivas, etc.

**TypeScript:** Se siguieron las convenciones y guías de estilo de código de “TypeScript Style Guide” de Google. Lo cual se destaca lo siguiente: 

- _PascalCase para Clases y Tipos:_ Los nombres de clases y tipos deben usar PascalCase, donde cada palabra comienza con una letra mayúscula. Ejemplo: MiClase. 
- _camelCase para Variables y Funciones:_ Los nombres de variables y funciones deben usar camelCase, donde la primera palabra comienza con minúscula y las siguientes con mayúscula. Ejemplo: miVariable. 
- _UPPER_CASE para Constantes:_ Los nombres de constantes se escriben completamente en mayúsculas y se separan con guiones bajos. Ejemplo: MI_CONSTANTE. 
- _Evitar el tipo Any:_ Se debe evitar el uso de any en TypeScript y, en su lugar, se deben declarar tipos explícitos para variables y parámetros de función siempre que sea posible. 
- _Interfaces para Estructuras de Datos:_ Utilizar interfaces para definir la estructura de datos de objetos y clases.  
- _Uso de Tipos Genéricos:_ Utilizar tipos genéricos para crear componentes y funciones reutilizables que funcionen con varios tipos de datos. 
- _Uso de Modificadores de Acceso:_ Utilizar modificadores de acceso como public, private y protected para controlar la visibilidad y el acceso a propiedades y métodos de una clase. 
- _Nombrar Funciones según su Propósito:_ Dar nombres descriptivos a las funciones que reflejen su propósito y su acción. 

**Angular:** Se siguieron las convenciones y guías de estilo de código de “Angular coding style guide” de la página oficial de Angular.io. Lo cual se destaca lo siguiente: 

- _Nombres de Archivos en kebab-case:_ Los nombres de los archivos de componentes, módulos y servicios deben usar la convención kebab-case, donde las palabras se separan con guiones. Ejemplo: mi-componente.component.ts. 
- _Uso de Decoradores:_ Utilizar decoradores como @Component y @Injectable para anotar componentes, servicios y otros elementos de Angular. 
- _Convención de Carpetas:_ Organizar los archivos de Angular en carpetas según su tipo, como componentes, servicios, módulos, etc. 
- _Uso de Módulos:_ Utilizar módulos para organizar y encapsular funcionalidades relacionadas en la aplicación. 
- _Uso de RxJS:_ Emplear RxJS para gestionar flujos de datos asíncronos y observables en la aplicación. 
- _Uso de Directivas Personalizadas:_ Crear directivas personalizadas cuando sea necesario para agregar funcionalidad específica a elementos del DOM. 
- _Uso de Servicios:_ Separar la lógica de negocio y la comunicación con el servidor en servicios reutilizables. 
- _Evitar Lógica en Plantillas:_ Evitar lógica compleja en las plantillas de componentes y, en su lugar, moverla a los métodos del componente. 
- _Gestión de Rutas:_ Utilizar el enrutamiento de Angular para gestionar las rutas y la navegación entre páginas de la aplicación. 

**Spring:** Se siguieron las convenciones y guías de estilo de código de la documentación oficial de Spring Boot y se destaca lo siguiente: 

- _Uso de Anotaciones:_ Utilizar anotaciones como @Controller, @Service, @Repository y @Component para marcar clases y componentes específicos de Spring. 
- _Convención de Paquetes:_ Organizar los archivos y clases en carpetas que representen la estructura lógica de la aplicación, como controladores, servicios, repositorios, etc. 
- _Convención de Nombres en Bases de Datos:_ Utilizar la convención de nombres en bases de datos como snake_case para nombres de tablas y columnas. Spring Boot se encargará de mapear estos nombres a objetos Java. 
- _Uso de Spring Data JPA:_ Emplear Spring Data JPA para simplificar la interacción con la capa de persistencia y bases de datos. 
- _Uso de Inyección de Dependencias:_ Aplicar la inyección de dependencias utilizando el constructor de las clases. 
- _Configuración Externa:_ Utilizar archivos de configuración externos (como application.properties o application.yml) para configurar propiedades de la aplicación. 
- _Uso de @RestController:_ Usar la anotación @RestController para marcar controladores que devuelven datos en formato JSON. 
- _Manejo de Excepciones:_ Implementar el manejo de excepciones de manera consistente, utilizando las anotaciones @ExceptionHandler y @ControllerAdvice. 
- _Logging con SLF4J:_ Realizar el registro de eventos y seguimiento de la aplicación utilizando la interfaz SLF4J (Simple Logging Facade for Java). 
- _Seguridad con Spring Security:_ Implementar la seguridad en la aplicación utilizando Spring Security para autenticación y autorización. 

**Java:** Se siguieron las convenciones y guías de estilo de código de " Java Style Guide” de Google y se destaca lo siguiente: 

- _Nombres de Clases en CamelCase:_ Los nombres de clases en Java deben seguir la convención CamelCase, donde cada palabra comienza con mayúscula. Ejemplo: MiClase. 
- _Nombres de Paquetes en minúsculas:_ Los nombres de paquetes en Java se escriben en minúsculas y generalmente reflejan la estructura del proyecto. Ejemplo: com.miproyecto. 
- _Nombres de Métodos Descriptivos:_ Dar nombres descriptivos a los métodos que reflejen su propósito y acción, utilizando camelCase. Ejemplo: calcularTotal. 
- _Nombres de Variables en camelCase:_ Los nombres de variables en Java se escriben en camelCase, donde la primera letra comienza con minúscula. Ejemplo: miVariable. 
- _Uso de Comentarios Javadoc:_ Documentar las clases y métodos utilizando comentarios Javadoc para proporcionar una descripción clara y legible de su funcionalidad. 
- _Convención de Nombres para Getters y Setters:_ Los métodos de acceso (getters) y modificación (setters) para propiedades deben seguir la convención getPropiedad y setPropiedad. Ejemplo: getNombre y setNombre. 
- _Uso de Interfaces:_ Utilizar interfaces para definir contratos y proporcionar una forma de implementación común en clases diferentes. 
- _Convención para Manejo de Excepciones:_ Manejar las excepciones de manera adecuada, preferiblemente utilizando bloques try-catch, y proporcionar mensajes descriptivos en las excepciones personalizadas. 
- _Convención de Nombres para Enumeraciones:_ Los nombres de enumeraciones se escriben en mayúsculas y suelen representar valores constantes. Ejemplo: DíasDeLaSemana. 
- _Evitar el Uso de Caracteres Especiales en Nombres:_ Evitar caracteres especiales, espacios y acentos en los nombres de clases, métodos y variables. 

**Gherkin:** Se consideró conveniente usar la guía y convenciones que se mencionan en “Gherkin Conventions for Readable Specifications” para una correcta realización de las pruebas. A continuación, se mencionan los puntos que consideramos más importantes para nuestro trabajo:

- _Los bloques “Give-When-Then” deben ser diferenciados:_ Se recomienda usar una correcta indentación de esos bloques para identificar mejor las secciones de la prueba y también añadiendo la keyword “And” para añadir otra línea en los pasos y otro bloque.
- _Usar tablas para los pasos:_ Si uno de los pasos requiere de más información es recomendable - usar tablas para organizar dicha información y tenga un aspecto más ordenado.
- _Usar comillas simples para los parámetros:_ Se recomienda esta práctica para una mejor legibilidad de los parámetros en un paso y tener una sintaxis más simple.
- _Separar los escenarios con comentarios:_ Si se da el caso de tener muchos escenarios en una prueba, es usar los comentarios como separadores para que visualmente sea más organizado, fácil de leer y distinguir mejor.

### 6.1.4. Software Deployment Configuration
## 6.2. Landing Page, Services & Applications Implementation
### 6.2.1. Sprint 1
#### 6.2.1.1. Sprint Planning n
#### 6.2.1.2. Sprint Backlog n
#### 6.2.1.3. Development Evidence for Sprint Review
#### 6.2.1.4. Testing Suite Evidence for Sprint Review
#### 6.2.1.5. Execution Evidence for Sprint Review
#### 6.2.1.6. Services Documentation Evidence for Sprint Review
#### 6.2.1.7. Software Deployment Evidence for Sprint Review
#### 6.2.1.8. Team Collaboration Insights during Sprint