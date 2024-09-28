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

### **Web Application**
La plataforma web será un punto de control principal para los usuarios, tanto propietarios de inmuebles como empresas de seguridad, que gestionarán sus sistemas de seguridad de manera remota. El diseño web será completamente responsive, adaptándose a cualquier tamaño de pantalla sin comprometer la claridad de la información ni la facilidad de uso. Se tendrá en cuenta una variedad de resoluciones, asegurando que tanto en dispositivos móviles como en pantallas de escritorio, los elementos clave sean accesibles y fáciles de interactuar.

#### **Patrón de Diseño**
Utilizaremos el patrón Z, ya que este patrón guía naturalmente la vista del usuario de izquierda a derecha y luego en diagonal, formando un trayecto en "Z". Este recorrido visual es ideal para resaltar la información más importante. 

#### **Estructura del Contenido**
- **Logo y Menú**: El logo de la empresa en la esquina superior izquierda y el menú de navegación en la parte superior derecha garantizan un acceso rápido a las secciones más importantes.
- **Panel de Control**: Justo debajo del menú, se mostrará el panel de control principal, donde el usuario podrá visualizar el estado general del sistema en tiempo real.
- **Uso de Espacios**: Los espacios serán generosos entre secciones para evitar la saturación de información, y los gráficos e íconos ayudarán a los usuarios a navegar de manera intuitiva.
- **Color y Tipografía**: Se utilizarán colores neutros con acentos en colores vivos para destacar elementos importantes (verde para seguridad, rojo para alertas). La tipografía será clara y legible, priorizando la simplicidad.

#### **Interacciones y Feedback**
- Los botones y formularios proporcionarán un feedback visual claro mediante cambios de color o animaciones sutiles, de modo que el usuario sepa que su acción fue reconocida.
- **Microinteracciones** como notificaciones emergentes se mostrarán cuando se detecten eventos importantes, como alertas de seguridad.
![web-guidelines](src/images/web-guidelines.png)

### **Mobile Application**
La app móvil se diseñará para ofrecer a los usuarios la capacidad de gestionar y monitorear sus sistemas de seguridad de manera eficiente desde cualquier lugar, con un enfoque en la accesibilidad y facilidad de uso en pantallas más pequeñas.

#### **Diseño Responsive**
El diseño de la app seguirá el patrón Z para guiar intuitivamente la atención del usuario. Los elementos más importantes, como el estado del sistema y las alertas, se mostrarán en la parte superior, mientras que el menú principal se encontrará en la parte inferior, facilitando la navegación con el pulgar.

#### **Interfaz de Usuario**
- **Pantalla de inicio**: Presentará un resumen visual del estado actual de los dispositivos (cámaras, sensores, alarmas) con íconos grandes e interactivos.
- **Gestión de cámaras**: Al seleccionar una cámara, se abrirá la transmisión en vivo y se ofrecerán botones destacados para revisar el historial o capturar imágenes.
- **Alertas**: Las alertas y notificaciones se mostrarán en tiempo real y serán accesibles mediante deslizamientos, con la posibilidad de personalizar las notificaciones push.

#### **Interacciones**
- Los gestos de deslizamiento permitirán a los usuarios navegar entre cámaras y alertas con facilidad.
- Botones flotantes estarán presentes para activar o desactivar funciones clave como alarmas o tomar capturas rápidas desde las cámaras.
![web-guidelines](src/images/patron-z.png)

### **IoT Device**
Los dispositivos IoT, como las cámaras y sensores, son fundamentales para la experiencia del usuario. Las interfaces de estos dispositivos deben ser claras, minimalistas y fácilmente accesibles tanto para profesionales como para usuarios novatos.

#### **Diseño de la Pantalla del Dispositivo IoT**
- **Prioridad en los datos críticos**: Los datos más importantes, como el estado de las cámaras, la batería de los sensores y las alertas activas, se mostrarán de manera prominente en la pantalla principal del dispositivo IoT.
  
- **Interfaz minimalista**: El diseño de la pantalla será simple y sin distracciones, mostrando solo la información esencial con opciones para acceder a más detalles si es necesario.

#### **Interacciones**
- **Iconografía intuitiva**: Se utilizarán íconos claros y reconocibles para representar el estado del sistema. Por ejemplo, un ícono de cámara indicará el estado de videovigilancia, un triángulo de advertencia mostrará alertas activas, y un candado indicará el estado de las alarmas.
  
- **Controles táctiles**: Los dispositivos tendrán botones físicos y táctiles para facilitar su uso, y permitirán la interacción remota mediante la aplicación móvil o web.

#### **Color**
- Los colores seguirán un esquema similar a las interfaces web y móvil, con colores brillantes para alertas importantes (rojo, amarillo).
![web-guidelines](src/images/iot-devices.png)

## 5.2. Information Architecture
### 5.2.1. Organization Systems
**1. Dueños de inmuebles**

**2. Empresas de seguridad**
**Jerarquía Visual:** Se utilizará para resaltar herramientas y reportes críticos en tiempo real. Las alertas, notificaciones y opciones de respuesta rápida serán el foco principal.
**Organización Matricial:** Para las tareas complejas como la coordinación de respuestas ante incidentes, se utilizará una organización matricial que permita acceder a diferentes funciones y recursos de manera rápida y paralela, manteniendo la flexibilidad en la navegación.
**Esquemas de Categorización:**
 - **Cronológico:** Las alertas y eventos de seguridad se organizarán cronológicamente, permitiendo un monitoreo eficaz de situaciones en curso y el acceso a históricos de incidentes.
 - **Por Audiencia:** Diferentes tipos de usuarios dentro de las empresas de seguridad, como operadores o técnicos de campo, tendrán acceso a contenidos específicos según sus roles.

### 5.2.2. Labeling Systems
### 5.2.3. SEO Tags and Meta Tags
### 5.2.4. Searching Systems
### 5.2.5. Navigation Systems
**1. Propietarios de inmuebles**
- **Navegación Basada en Menús Desplegables:** La Landing Page incluirá un menú principal en la parte superior, con opciones desplegables que permitirán a los usuarios acceder a categorías de productos (cámaras, sensores, alarmas) y servicios (instalación, mantenimiento). Esto simplificará la búsqueda y permitirá que encuentren fácilmente lo que necesitan.
 - **CTA (Call to Action):** Botones de CTA destacados visualmente guiarán a los usuarios a realizar acciones clave como “Solicitar una Cotización”, “Programar Instalación” o “Ver Ofertas Especiales”. Estos botones estarán distribuidos estratégicamente en toda la página para incentivar la interacción.
 - **Breadcrumbs:** Para garantizar que los usuarios nunca se sientan perdidos, se incluirán breadcrumbs o "migas de pan" en páginas internas. Estos indicarán la ruta de navegación y permitirán volver a secciones anteriores sin dificultad.
 - **Search Bar:** La barra de búsqueda estará disponible en la parte superior de la página, permitiendo a los usuarios realizar búsquedas rápidas y específicas sobre productos y servicios.

**2. Empresas de seguridad**
 - **Panel de Control Personalizado:** En las aplicaciones, las empresas de seguridad tendrán acceso a un panel de control principal, diseñado como un centro de operaciones. Desde aquí, podrán acceder a alertas recientes, coordinar respuestas y gestionar equipos. Este panel funcionará como el punto central de navegación.
 - **Navegación por Filtros:** Las alertas de seguridad podrán filtrarse por fecha, gravedad o tipo de incidente, ayudando a los operadores a priorizar las respuestas. Esto optimizará la navegación, especialmente en situaciones de alto volumen de alertas.
 - **Navegación Secuencial:** Durante la coordinación de una respuesta a un incidente, el sistema guiará a los usuarios paso a paso, desde la recepción de la alerta hasta la resolución, asegurando que cada fase del proceso sea clara y fácil de seguir.

## 5.3. Landing Page UI Design

Para esta parte como grupo explicaremos nuestro diseño de Landing page, donde hemos utilizado buenas prácticas de diseño. Asimismo, utilizamos Figma como herramienta principal para el diseño de nuestros wireframes y mockups.

### 5.3.1. Landing Page Wireframe

Para nuestra base de Landing Page utilizamos el diseño Wireframe que nos da una visión mejor de cómo queremos que quede nuestro diseño, esto a su vez es diseñado tanto para un sitio web de escritorio y móvil. Además, hemos utilizado los principios, elementos de diseño, diseño inclusivo y arquitecturas de informacipon que se han planteado anteriormente.

Primero explicaremos cada parte de nuestra landing page:

**a. Landing Page Wireframe**
Como encabezado tendremos nuestro nombre y logo de la Empresa, así como Call to Action que nos dirigirán tanto a la aplicación web de nuestra empresa o que nos ayudará a desplazarnos dentro de la Landing Page. Asimismo contaremos con una frase de valor *"We provide protection in every corner, so that growth is your only concern" ("Brindamos protección en cada rincón, para que el crecimiento sea tu única preocupación")*. Para la parte de móvil, tendrá un call to action que nos redirigirá a la parte para descargar la aplicación móvil.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/1.%20web%20.jpg) | ![primera parte mov](src/images/1.%20app.jpg) |

Luego, ponemos nuestras soluciones que tenemos que son las cámaras de seguridad, sensores y alarmas. Aquí explicaremos brevemente las soluciones que brindamos al usuario.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/2.web.jpg) | ![primera parte mov](src/images/2.app.jpg) |

Seguidamente, presentamos nuestros planes en este caso solo tendremos 3; el básico, el premium y el gold que le ofrecemos al usuario y asimismo a un precio cómodo.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/3.web.jpg) | ![primera parte mov](src/images/3.app.jpg) |

Luego, tenemos nustra sección en donde presentamos el equipo de trabajo, aquí se pondrá una fotografía de cada uno esto nos ayudará a generar confianza con nuestros nuevos usuarios o con los usuarios que ya tenemos.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/4.web.jpg) | ![primera parte mov](src/images/4.app.jpg) |

Asimismo, tendremos una sección con los comentarios de los usuarios y además para lo que es el Landing Page Web una sección adicional en donde encontrarán nuestro App Móvil

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/5.web.jpg) | ![primera parte mov](src/images/5.app.jpg) |

Por último tendremos nuestra sección donde hablamos más sobre la aplicación mediante un video y nuestro footer.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/6.web.jpg) | ![primera parte mov](src/images/6.app.jpg) |

Luego de explicar cada sección, mostramos nuestros wireframe completo tanto para la parte del escritorio como para el mobile.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/LandingPageWebWireframe.png) | ![primera parte mov](src/images/LandingPagemobileWireframe.png) |

### 5.3.2. Landing Page Mock-up

Para nuestro diseño final de Landing Page utilizamos el diseño Mock-up que nos da una visión final de como queremos que quede nuestro diseño, esto a su vez es diseñado tanto para un sitio web de escritorio y móvil. Además, hemos utilizado los principios, elementos de diseño, diseño inclusivo y arquitecturas de informacipon que se han planteado anteriormente.

Primero explicaremos cada parte de nuestra landing page:

**a. Landing Page Mock-up**
Como encabezado tendremos nuestro nombre y logo de la Empresa, así como Call to Action que nos dirigirán tanto a la aplicación web como para registrarse o iniciar sesión si ya es usuario de nuestra empresa o que nos ayudará a desplazarnos dentro de la Landing Page. Asimismo contaremos con una frase de valor *"We provide protection in every corner, so that growth is your only concern" ("Brindamos protección en cada rincón, para que el crecimiento sea tu única preocupación")*. Para la parte de móvil, tendrá un call to action que nos redirigirá a la parte para descargar la aplicación móvil.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/web1.jpg) | ![primera parte mov](src/images/app1.jpg) |

Luego, ponemos nuestras soluciones que tenemos que son las cámaras de seguridad, sensores y alarmas. Aquí explicaremos con una descripción corta las soluciones que brindamos al usuario.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/web2.jpg) | ![primera parte mov](src/images/app2.jpg) |

Seguidamente, presentamos nuestros planes en este caso solo tendremos 3; el básico, el premium y el gold que le ofrecemos al usuario y asimismo a un precio cómodo.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/web3.jpg) | ![primera parte mov](src/images/app3.jpg) |

Luego, tenemos nustra sección en donde presentamos el equipo de trabajo, aquí se pondrá una fotografía de cada uno esto nos ayudará a generar confianza con nuestros nuevos usuarios o con los usuarios que ya tenemos.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/web4.jpg) | ![primera parte mov](src/images/app4.jpg) |

Asimismo, tendremos una sección con los comentarios de los usuarios y además para lo que es el Landing Page Web una sección adicional en donde encontrarán nuestro App Móvil

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/web5.jpg) | ![primera parte mov](src/images/app5.jpg) |

Por último tendremos nuestra sección donde hablamos más sobre la aplicación mediante un video y nuestro footer.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/web6.jpg) | ![primera parte mov](src/images/app6.jpg) |

Luego de explicar cada sección, mostramos nuestros wireframe completo tanto para la parte del escritorio como para el mobile.

| Wireframe para Desktop | Wireframe para Mobile |
| -- |-- |
| ![primera parte web](src/images/LandingPageWebMockup.png) | ![primera parte mov](src/images/LandingPagemobileMockup.png) |

## 5.4. Applications UX/UI Design

Para esta parte como grupo explicaremos nuestro diseños Wireframes y Mock-ups de nuestra aplicación móvil y aplicación web de nuestro producto FalconShield

### 5.4.1. Applications Wireframes

**MOBILE APPLICATION WIREFRAMES**

Presentaremos nuestro diseño visual en el formato de wireframe que nos da una visión de bajo nivel al diseño que quisieramos lograr. Tengamos en cuenta que la aplicación móvil solo va dirigida a un segmento objetivo que es el Dueño de Inmueble.

Tenemos nuestras pantallas generales como el inicio de sesión y el registro del usuario, asi como las pantallas de registro o inicio de sesión exitoso.

| Wireframe | Descripción |
|-- | -- |
|![inicio de sesion app movil](src/images/inicioapp.png) | **Inicio de Sesión:** En esta pantalla le mostamos al usuario los campos que tiene que llenar para que ingrese a nuestra aplicación. |
| ![inicio exitoso app movil](src/images/inicioexapp.png) | **Inicio de sesión exitoso:**  En esta pantalla le mostramos al usuario que pudo acceder de forma exitosa dado que ingreso correctamente sus credenciales. |
| ![registro de usuario](src/images/registerapp.png) | **Registrar una cuenta:** En esta pantalla le mostamos al usuario los campos que tiene que llenar para poder crearse una cuenta. |
| ![registro exitoso](src/images/registerexitapp.png) | **Registro exitoso:** En esta pantalla le mostramos al usuario que pudo crear correctamente su nueva cuenta. |

Asimismo contamos dentro de la aplicación con la pantalla principal Home:

| Wireframe | Descripción |
| -- | -- |
| ![pantalla inicial app](src/images/Home%20Screenapp.png) | **Pantalla de Incio:** En esta pantalla le mostramos al usuario sus dispositivos que ha solicitado asimismo en que ambientes se han instalado. Tener en cuenta que esta pantalla sera de tipo scroll. |

Tenemos tambiens nuestra pantalla donde el usuario podrá ver su información personal.
| Wireframe | Descripción |
| -- | -- |
| ![profile](src/images/Profile.png) | **Perfil del usuario:** En esta pantalla el usuario podrá ver su información asi como otras funciones adicionales. |

Tenemos tambien nuestras pantallas para que el usuario agregue los dispositivos luego de ser instalados.

| Wireframe | Descripción |
| -- | -- |
| ![pantalla inicial de dispositivos](src/images/ADD%20DEVICE.png) | **Pantalla principal de los Dispositivos:** En esta pantalla le presentaremos al usuario los dispositivos adquiridos, asi como un boton que puede agregar luego de obtener más|
| ![seleccion de conexion](src/images/AD%203.png) | **Selección tipo de conexión con el dispositivo nuevo:** En esta pantalla el usuario podrá elegir el tipo de conexión con su nuevo dispositivo en este caso Bluetooth |
| ![tipo de nuevo dispositivo](src/images/AD%204.png) | **Selección del nuevo dispositivo:** En esta pantalla el usuario podrá seleccionar el nuevo dispositivo adquirido para poder agregarlo. |
| ![seleccion de ambiente](src/images/AD%205.png) | **Selección de ambiente:** En esta pantalla el usuario podrá elegir en que ambiente de su inmueble fue colocado el nuevo dispositivo |
| ![nombre de dispositivo](src/images/AD%206.png) | **Ingreso de nombre del dispositivo nuevo:** En esta pantalla el usuario podrá ingresar como quiere que se llame su nuevo dispositivo. |
| ![dispositivo nuevo agregado exitoso](src/images/AD%207.png) | **Registro de dispositivo nuevo exitoso:** En esta pantala el usuario podrá ver que agrego su dispositivo nuevo de forma exitosa en la aplicación |
| ![nuevo dispositvo](src/images/AD%208.png) | **Ver nuevo dispositivo:** En esta pantalla el usuario podrá verificar el nuevo dispositivo que ha agregado. |
| ![detalles del dispositivo](src/images/Device%20Especification.png) | **Detalles del dispositivo:** En esta pantalla el usuario verá los detalles del dispositivo ya sea su descripcióm, el tipo de dispositvo, etc. |

Tenemos tambien nuestras pantallas para que el usuario agregue los nuevos ambientes que desea un dispositivo.

| Wireframe | Descripción |
| -- | -- |
| ![pantalla incial de ambientes](src/images/CREATE%20ROOM.png) | **Pantalla principal de los ambientes:** En esta pantalla el usuario podrá visualizar los ambientes en los cuales tiene un dispositivo de seguridad |
| ![ingreso de nombre del nuevo ambiente](src/images/CR%201.png) | **Ingreso del nombre del nuevo ambiente:** En esta pantalla el usuario podrá ingresar el nombre del nuevo ambiente que quiera crear |
| ![selección del ambiente](src/images/CR%202.png) | **Selección del nuevo ambiente:** En esta pantalla el usuario podrá elegir el nuevo ambiente que va a tener un dispositivo de seguridad |
| ![ambiente agregado exitoso](src/images/CR%203.png) | **Ambiente agregado de forma exitosa:** En esta pantalla el usuario verá que su ambiente se ha agregado exitosamente |
| ![visualizacion del nuevo ambiente](src/images/CR%204.png) | **Nuevo ambiente visualizado:** En esta pantalla el usuario verá que se agrego el ambiente en la aplicación móvil. |
| ![especificaciones del nuevo ambiente](src/images/Room%20Especification.png) | **Detalles del ambiente:** En esta pantalla el usuario verá que dispositivos se encuentran en el ambiente seleccionado. |

### 5.4.2. Applications Wireflow Diagrams
### 5.4.2. Applications Mock-ups

**MOBILE APPLICATION MOCK-UP**

Presentaremos nuestro diseño visual en el formato de Mockup que nos da una visión de alto nivel del diseño de nuestra aplicación. Tengamos en cuenta que la aplicación móvil solo va dirigida a un segmento objetivo que es el Dueño de Inmueble.

Tenemos nuestras pantallas generales como el inicio de sesión y el registro del usuario, asi como las pantallas de registro o inicio de sesión exitoso.

| Wireframe | Descripción |
|-- | -- |
|![inicio de sesion app movil](src/images/minicioapp.png) | **Inicio de Sesión:** En esta pantalla le mostamos al usuario los campos que tiene que llenar para que ingrese a nuestra aplicación. Utilizamos botones para que el usuario pueda diferenciar |
| ![inicio exitoso app movil](src/images/minicioexapp.png) | **Inicio de sesión exitoso:**  En esta pantalla le mostramos al usuario que pudo acceder de forma exitosa dado que ingreso correctamente sus credenciales. |
| ![registro de usuario](src/images/mregisterapp.png) | **Registrar una cuenta:** En esta pantalla le mostamos al usuario los campos que tiene que llenar para poder crearse una cuenta. |
| ![registro exitoso](src/images/mregisterexitapp.png) | **Registro exitoso:** En esta pantalla le mostramos al usuario que pudo crear correctamente su nueva cuenta. |

Asimismo contamos dentro de la aplicación con la pantalla principal Home:

| Wireframe | Descripción |
| -- | -- |
| ![pantalla inicial app](src/images/MHome%20Screen.png) | **Pantalla de Incio:** En esta pantalla le mostramos al usuario sus dispositivos que ha solicitado asimismo en que ambientes se han instalado. Tener en cuenta que esta pantalla sera de tipo scroll. |

Tenemos tambiens nuestra pantalla donde el usuario podrá ver su información personal.
| Wireframe | Descripción |
| -- | -- |
| ![profile](src/images/mProfile.png) | **Perfil del usuario:** En esta pantalla el usuario podrá ver su información asi como otras funciones adicionales. |

Tenemos tambien nuestras pantallas para que el usuario agregue los dispositivos luego de ser instalados.

| Wireframe | Descripción |
| -- | -- |
| ![pantalla inicial de dispositivos](src/images/MADD%20DEVICE}.png) | **Pantalla principal de los Dispositivos:** En esta pantalla le presentaremos al usuario los dispositivos adquiridos, asi como un boton que puede agregar luego de obtener más|
| ![seleccion de conexion](src/images/MAD%203.png) | **Selección tipo de conexión con el dispositivo nuevo:** En esta pantalla el usuario podrá elegir el tipo de conexión con su nuevo dispositivo en este caso Bluetooth |
| ![tipo de nuevo dispositivo](src/images/MAD%204.png) | **Selección del nuevo dispositivo:** En esta pantalla el usuario podrá seleccionar el nuevo dispositivo adquirido para poder agregarlo. |
| ![seleccion de ambiente](src/images/MAD%205.png) | **Selección de ambiente:** En esta pantalla el usuario podrá elegir en que ambiente de su inmueble fue colocado el nuevo dispositivo |
| ![nombre de dispositivo](src/images/MAD%206.png) | **Ingreso de nombre del dispositivo nuevo:** En esta pantalla el usuario podrá ingresar como quiere que se llame su nuevo dispositivo. |
| ![dispositivo nuevo agregado exitoso](src/images/MAD%207.png) | **Registro de dispositivo nuevo exitoso:** En esta pantala el usuario podrá ver que agrego su dispositivo nuevo de forma exitosa en la aplicación |
| ![nuevo dispositvo](src/images/MAD%208.png) | **Ver nuevo dispositivo:** En esta pantalla el usuario podrá verificar el nuevo dispositivo que ha agregado. |
| ![detalles del dispositivo](src/images/MA%202.png) | **Detalles del dispositivo:** En esta pantalla el usuario verá los detalles del dispositivo ya sea su descripcióm, el tipo de dispositvo, etc. |

Tenemos tambien nuestras pantallas para que el usuario agregue los nuevos ambientes que desea un dispositivo.

| Wireframe | Descripción |
| -- | -- |
| ![pantalla incial de ambientes](src/images/MCREATE%20ROOM.png) | **Pantalla principal de los ambientes:** En esta pantalla el usuario podrá visualizar los ambientes en los cuales tiene un dispositivo de seguridad |
| ![ingreso de nombre del nuevo ambiente](src/images/MCR%201.png) | **Ingreso del nombre del nuevo ambiente:** En esta pantalla el usuario podrá ingresar el nombre del nuevo ambiente que quiera crear |
| ![selección del ambiente](src/images/MCR%202.png) | **Selección del nuevo ambiente:** En esta pantalla el usuario podrá elegir el nuevo ambiente que va a tener un dispositivo de seguridad |
| ![ambiente agregado exitoso](src/images/MCR%203.png) | **Ambiente agregado de forma exitosa:** En esta pantalla el usuario verá que su ambiente se ha agregado exitosamente |
| ![visualizacion del nuevo ambiente](src/images/MCR%204.png) | **Nuevo ambiente visualizado:** En esta pantalla el usuario verá que se agrego el ambiente en la aplicación móvil. |
| ![especificaciones del nuevo ambiente](src/images/Living%20Room.png) | **Detalles del ambiente:** En esta pantalla el usuario verá que dispositivos se encuentran en el ambiente seleccionado. |

### 5.4.3. Applications User Flow Diagrams
## 5.5. Applications Prototyping