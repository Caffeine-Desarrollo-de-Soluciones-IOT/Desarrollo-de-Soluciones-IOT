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
## 3.1. To-Be Scenario Mapping
* **Segmento 1: Dueños de inmuebles**

El To Be Scenario Mapping para los dueños de inmuebles tiene como objetivo visualizar el recorrido ideal que experimentarán estos usuarios al interactuar con un sistema de seguridad IoT. Al identificar cada paso que estos propietarios realizan, desde la investigación hasta el uso diario y mantenimiento del sistema, se puede comprender mejor cómo proporcionar una experiencia fluida y satisfactoria.

Este mapeo se centra en las acciones, pensamientos y emociones de los dueños de inmuebles en cada fase de interacción con el sistema. De este modo, se busca diseñar una solución que no solo sea eficiente y segura, sino también intuitiva y alineada con las expectativas y necesidades específicas de los usuarios. A través de este proceso, el objetivo es garantizar que los usuarios experimenten confianza, tranquilidad y satisfacción durante todo el ciclo de vida de su sistema de seguridad.

![To Be Property Owners](/src/images/to-be-1.jpg)

* **Segmento 2: Empresa de seguridad**

El To Be Scenario Mapping para las empresas de seguridad ofrece una representación detallada de cómo estas organizaciones interactúan con los sistemas de seguridad IoT y los clientes a lo largo de todo el proceso de respuesta a incidentes. Desde la recepción de una alerta hasta la mejora continua de los protocolos y sistemas, este mapeo busca optimizar cada paso crítico para garantizar un servicio eficiente, preciso y confiable.

El enfoque está en los desafíos que enfrentan las empresas de seguridad al validar alertas, coordinar respuestas y asegurar que sus equipos y procedimientos estén siempre actualizados y preparados para incidentes futuros. A través de este mapeo, se pretende crear una experiencia integrada, en la que la tecnología y la comunicación con los clientes se alineen para ofrecer una respuesta rápida y efectiva, manteniendo la confianza y satisfacción de los usuarios.

![To Be Security Company](/src/images/to-be-2.jpg)

## 3.2. User Stories

En esta sección se presentan las historias de usuario correspondientes a nuestra aplicación móvil, sitio web estático y dispositivos edge. Estas historias describen las características necesarias para nuestros dos segmentos objetivo. Además, se especifican los criterios de aceptación que nos permitirán verificar si las funcionalidades cumplen con las necesidades de los usuarios.

| **ID**  | **Título**                | **Descripción**                                                                                                   | **Criterios de Aceptación (Cucumber)**                                                                                                                                          | **Relacionado con (Epic ID)** |
|---------|---------------------------|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| **HU-01**| Ver historial de eventos  | Como propietario de un inmueble, quiero poder ver el historial de los eventos para revisar incidentes pasados. | **Given** que el propietario está en la página Events **When** selecciona el evento **Then** puede ver todas las notificaciones en base al evento. <br><br> **Given** que no hay notificaciones en el evento seleccionado **When** selecciona la fila **Then** se muestra un mensaje indicando que no notificaciones para ese evento.           | Epic 1                        |
| **HU-02**| Configurar notificaciones personalizadas | Como empresa de seguridad, quiero configurar las alertas para recibir notificaciones específicas según los tipos de eventos en cada propiedad. | **Given** que el usuario está en la sección de configuraciones **When** crea una nueva alerta personalizada **Then** recibe notificaciones solo para los eventos configurados. <br><br> **Given** que hay varias alertas personalizadas creadas **When** elimina una alerta personalizada **Then** la alerta se elimina y ya no recibe notificaciones de ese tipo.            | Epic 1                        |
| **HU-03**| Controlar dispositivos de seguridad | Como propietario de un inmueble, quiero controlar mis dispositivos de seguridad desde la aplicación web para armar o desarmar la alarma. | **Given** que el propietario está en el panel de control de dispositivos **When** selecciona un dispositivo y una acción (armar/desarmar) **Then** el dispositivo realiza la acción y se muestra una notificación de confirmación. <br><br> **Given** que un dispositivo no responde **When** intenta armar o desarmar el dispositivo **Then** se muestra un mensaje de error indicando que no se pudo completar la acción. | Epic 2                        |
| **HU-04**| Resumen de eventos  | Como usuario, quiero un resumen de todos los eventos desde una única interfaz para gestionar los dispositivos de manera eficiente. | **Given** que el usuario está en el dashboard **When** selecciona una propiedad **Then** puede ver un resumen en tiempo real de todos los dispositivos y alertas de esa propiedad. <br><br> **Given** que hay una alerta activa en una propiedad **When** selecciona la propiedad **Then** se muestra la alerta en la parte superior del resumen con opciones para gestionarla.       | Epic 2                        |
| **HU-05**| Reportar un incidente      | Como propietario de un inmueble, quiero reportar un incidente directamente desde la aplicación web para que la empresa de seguridad lo gestione. | **Given** que el propietario está en la sección de reportes **When** llena el formulario de incidente y lo envía **Then** la empresa de seguridad recibe una notificación con los detalles del reporte. <br><br> **Given** que el formulario de reporte tiene campos obligatorios vacíos **When** intenta enviarlo **Then** se muestra un mensaje de error indicando que debe completar los campos obligatorios. | Epic 3                        || 
| **HU-06**| Recibir notificaciones en tiempo real | Como propietario de un inmueble, quiero recibir notificaciones en tiempo real en mi móvil sobre cualquier alerta de seguridad para tomar acciones inmediatas. | **Given** que el propietario tiene la aplicación móvil instalada **When** se activa una alerta **Then** recibe una notificación push con la descripción del evento. <br><br> **Given** que la alerta no ha sido atendida en 5 minutos **When** la aplicación verifica el tiempo transcurrido **Then** envía una notificación de recordatorio al propietario. | Epic 4                        |
| **HU-07**| Acceso remoto a cámaras            | Como empresa de seguridad, quiero acceder a las cámaras de las propiedades desde mi dispositivo móvil para verificar en tiempo real cualquier alerta. | **Given** que la empresa de seguridad tiene acceso a la propiedad en la aplicación **When** selecciona la opción de cámaras **Then** puede ver las imágenes en vivo de todas las cámaras instaladas. <br><br> **Given** que una cámara está fuera de servicio **When** intenta acceder a las imágenes **Then** se muestra un mensaje indicando que la cámara no está disponible. | Epic 4                        |
| **HU-08**| Control de acceso remoto           | Como propietario de un inmueble, quiero controlar el acceso a mi propiedad desde mi móvil para abrir o cerrar puertas de manera remota. | **Given** que el propietario tiene la aplicación instalada **When** selecciona la opción de control de acceso **Then** puede abrir o cerrar puertas conectadas con un solo clic. <br><br> **Given** que una puerta está bloqueada **When** el propietario intenta abrirla desde la app **Then** se muestra un mensaje de error indicando que no se puede completar la acción. | Epic 5                      |
| **HU-09**| Crear y gestionar alertas desde la app | Como empresa de seguridad, quiero poder crear y gestionar alertas desde mi móvil para estar siempre en control, incluso cuando no estoy en la oficina. | **Given** que la empresa de seguridad está en la aplicación **When** crea una nueva alerta personalizada **Then** esta se activa y puede recibir notificaciones basadas en esa configuración. <br><br> **Given** que la empresa desea modificar una alerta activa **When** edita los parámetros de la alerta **Then** los cambios se reflejan de inmediato en la app. | Epic 5                       |
| **HU-10**| Ver grabaciones de seguridad       | Como propietario de un inmueble, quiero ver las grabaciones de seguridad desde mi móvil para revisar eventos pasados mientras estoy fuera de casa. | **Given** que el propietario está en la app **When** selecciona una fecha y hora **Then** puede ver la grabación correspondiente directamente desde su dispositivo móvil. <br><br> **Given** que no hay grabaciones disponibles para la fecha seleccionada **When** el propietario intenta visualizarla **Then** se muestra un mensaje indicando que no hay grabaciones para ese periodo. | Epic 6                       ||
| **HU-11**| Gestión de usuarios               | Como administrador, quiero poder gestionar todos los usuarios desde el backend para controlar el acceso y los permisos de la plataforma. | **Given** que el administrador está en el panel de administración **When** agrega, edita o elimina un usuario **Then** los cambios se reflejan en la aplicación web y móvil. <br><br> **Given** que un usuario ha sido eliminado **When** el administrador revisa la lista de usuarios **Then** el usuario eliminado ya no aparece en la lista. | Epic 7                        |
| **HU-12**| Gestión de dispositivos conectados| Como administrador, quiero poder gestionar todos los dispositivos conectados para monitorear su estado y funcionamiento. | **Given** que el administrador está en el panel de administración **When** visualiza el listado de dispositivos **Then** puede actualizar su estado, ver logs y desconectar dispositivos si es necesario. <br><br> **Given** que un dispositivo no responde **When** el administrador intenta actualizar su estado **Then** se muestra un mensaje de error indicando que el dispositivo está desconectado. | Epic 7                        |
| **HU-13**| Integración con sistemas de terceros | Como administrador, quiero integrar la plataforma con sistemas de seguridad de terceros para ampliar las capacidades del sistema. | **Given** que el administrador está en el panel de integraciones **When** configura una integración nueva **Then** los dispositivos y datos del sistema de terceros se sincronizan con la plataforma. <br><br> **Given** que la integración ha fallado **When** el administrador revisa los logs de la integración **Then** se muestra el motivo del fallo y las posibles soluciones. | Epic 7                        |
| **HU-14**| Gestión de logs y auditoría       | Como administrador, quiero poder acceder a los logs y realizar auditorías para monitorear la actividad del sistema y detectar anomalías. | **Given** que el administrador está en la sección de logs **When** selecciona un rango de fechas **Then** puede ver todas las actividades registradas en ese periodo. <br><br> **Given** que el administrador necesita exportar los logs **When** selecciona la opción de exportación **Then** los logs se descargan en un archivo CSV. | Epic 8                        |
| **HU-15**| Configuración de políticas de seguridad | Como administrador, quiero poder configurar políticas de seguridad para asegurar que todos los dispositivos y datos cumplan con los estándares requeridos. | **Given** que el administrador está en la sección de políticas **When** establece una nueva política de seguridad **Then** se aplica a todos los dispositivos y usuarios de la plataforma. <br><br> **Given** que una política de seguridad no cumple con los estándares **When** el administrador intenta guardarla **Then** se muestra un mensaje de advertencia y la política no se guarda. | Epic 8                        ||
| **HU-16**| Detección de anomalías en tiempo real    | Como propietario de un inmueble, quiero que los dispositivos en el edge detecten anomalías en tiempo real para reaccionar de inmediato ante posibles amenazas. | **Given** que tengo dispositivos edge instalados **When** ocurre una anomalía **Then** el dispositivo envía una alerta inmediata a la app móvil y web. <br><br> **Given** que la anomalía se ha solucionado **When** el dispositivo envía un informe de la resolución **Then** se notifica al propietario. | Epic 9                       |
| **HU-17**| Actualización remota de firmware         | Como administrador, quiero poder actualizar remotamente el firmware de los dispositivos en el edge para asegurar su correcto funcionamiento y seguridad. | **Given** que estoy en el panel de dispositivos **When** selecciono actualizar el firmware de un dispositivo **Then** el dispositivo se actualiza automáticamente y se reinicia. <br><br> **Given** que la actualización falla **When** el sistema intenta de nuevo **Then** se envía una notificación al administrador sobre el error. | Epic 9                       |
| **HU-18**| Autonomía operativa de dispositivos edge  | Como empresa de seguridad, quiero que los dispositivos en el edge funcionen de manera autónoma si pierden conexión con el servidor para asegurar la continuidad del servicio. | **Given** que un dispositivo edge pierde conexión **When** continúa operando de manera autónoma **Then** las alertas y registros se guardan localmente hasta que se restablezca la conexión. <br><br> **Given** que la conexión se restablece **When** se sincronizan los datos almacenados **Then** el servidor muestra el historial completo de alertas. | Epic 9                       |
| **HU-19**| Monitoreo de alertas en dispositivos edge | Como propietario de un inmueble, quiero monitorear las alertas de mis dispositivos edge.                              | **Given** que estoy en el dashboard de alertas **When** le doy click a un dispositivo **Then** puedo ver un historial de alertas del dispositivo y recibir sugerencias de optimización. <br><br> **Given** que un dispositivo ha tenido múltiples alertas **When** reviso el historial **Then** se muestran estadísticas de frecuencia y tipo de alertas. | Epic 10                       |
| **HU-20**| Reinicio remoto de dispositivos edge      | Como administrador, quiero poder reiniciar remotamente los dispositivos en el edge para solucionar problemas de manera eficiente. | **Given** que estoy en el panel de dispositivos **When** selecciono la opción de reinicio **Then** el dispositivo se reinicia automáticamente y notifica al usuario. <br><br> **Given** que el dispositivo no responde **When** intento reiniciarlo **Then** se envía una alerta al administrador indicando que el dispositivo está inoperativo. | Epic 10                      ||
| **HU-21**| Control de luces inteligentes              | Como propietario de un inmueble, quiero controlar las luces inteligentes de mi propiedad desde la app para encender o apagar según necesidad. | **Given** que estoy en la app móvil **When** selecciono una luz que quiero modificar **Then** puedo encenderla, apagarla o ajustar la intensidad. <br><br> **Given** que la luz está encendida **When** la apago **Then** se refleja el cambio en la app inmediatamente. | Epic 11                       |
| **HU-22**| Monitoreo de sensores de movimiento        | Como empresa de seguridad, quiero monitorear en tiempo real los sensores de movimiento de los dispositivos IoT para detectar intrusos. | **Given** que estoy en el dashboard de sensores **When** un sensor detecta movimiento **Then** recibo una alerta inmediata en la app. <br><br> **Given** que la alerta se activa **When** reviso el registro de eventos **Then** se muestra la hora y la ubicación del movimiento detectado. | Epic 11                       |
| **HU-23**| Monitorización de baterías en dispositivos IoT | Como empresa de seguridad, quiero monitorear el nivel de batería de los dispositivos IoT para asegurar que siempre estén operativos. | **Given** que estoy en el dashboard de energía **When** el nivel de batería es bajo **Then** recibo una alerta para reemplazar o recargar el dispositivo. <br><br> **Given** que el nivel de batería se ha recuperado **When** recargo el dispositivo **Then** se notifica el estado actualizado de la batería. | Epic 12                       |
| **HU-24**| Automatización de escenarios               | Como propietario de un inmueble, quiero crear escenarios automatizados en mi app para que los dispositivos IoT actúen en conjunto según la hora o eventos específicos. | **Given** que estoy en la app **When** configuro un escenario **Then** los dispositivos correspondientes se activan o desactivan automáticamente según lo programado. <br><br> **Given** que un escenario está activo **When** ocurre el evento programado **Then** se notifica el usuario de la acción realizada. | Epic 12                       |
| **HU-25**| Respuesta automatizada ante amenazas      | Como empresa de seguridad, quiero que el sistema responda automáticamente ante amenazas identificadas por los dispositivos de seguridad para minimizar el tiempo de reacción. | **Given** que una amenaza es detectada **When** el sistema la confirma **Then** se activan las medidas de seguridad preconfiguradas (alarma, bloqueo de puertas, notificación a autoridades). <br><br> **Given** que las medidas de seguridad están activadas **When** se recibe una nueva alerta **Then** el sistema registra la acción y notifica a los usuarios autorizados. | Epic 13                       |
| **HU-26**| Uso compartido de dispositivos              | Como propietario de un inmueble, quiero compartir el control de ciertos dispositivos con otros usuarios desde la app para que también puedan manejarlos. | **Given** que estoy en la sección de dispositivos **When** configuro el uso compartido **Then** el otro usuario tiene acceso limitado o completo según lo configurado. <br><br> **Given** que el acceso está compartido **When** el otro usuario intenta acceder **Then** se registra la actividad y se notifica al propietario. | Epic 14                       |
| **HU-27**| Alertas de mantenimiento preventivo        | Como propietario de un inmueble, quiero recibir alertas de mantenimiento preventivo de los dispositivos para evitar fallos y asegurar su operación continua. | **Given** que tengo dispositivos operando **When** alguno necesita mantenimiento **Then** recibo una alerta en la app y el email con los pasos a seguir para realizar el mantenimiento. <br><br> **Given** que he realizado el mantenimiento **When** actualizo el estado en la app **Then** se registra la acción y se confirma la operación continua del dispositivo. | Epic 15                       |

## 3.3. Impact Mapping
La herramienta denominada Impact Mapping consiste en una forma visual de representar las metas que nos plasmamos para llegar a cada sector de nuestro público. Por esta razón, el equipo utilizó este artefacto con el fin de definir nuestro camino para alcanzar a los segmentos objetivos. De este modo, al final del mapa mental identificamos las acciones y funcionalidades que debemos llevar a cabo para formar el proyecto de manera eficiente.

### User: Dueño de Inmuebles

A continuación, se presenta el Impact Map en el usuario, dueño de inmuebles; para la cual nos basamos en las User Stories de nuestro proyecto, brindando las alternativas con las que dispone los aplicativos para solucionar y satisfacer las necesidades del usuario.
![](/src/images/impact-map-dueño-inmueble.png)

### User: Empresa de seguridad
Este mapa de impacto incluye los objetivos empresariales, los efectos deseados en la organización de seguridad y las historias de usuario relacionadas. El enfoque es en mejorar la eficiencia operativa y la satisfacción del cliente mediante el uso de tecnología IoT para vigilancia en tiempo real y respuestas automatizadas a amenazas.
![](/src/images/impact-map-seguridad.png)

## 3.4. Product Backlog

Una vez que todas las User Stories están redactadas, es necesario priorizarlas. El Product Backlog se encarga de establecer un orden de relevancia entre todas las historias de usuario. Además, se incluirán los Story Points asignados a cada historia, que representan el esfuerzo requerido para completar exitosamente la User Story correspondiente.


| **Orden** | **User Story ID** | **Título**                                          | **Descripción**                                                                                         | **Story Points** |
|-----------|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------|
| 1         | HU-25             | Respuesta automatizada ante amenazas                | Como empresa de seguridad, quiero que el sistema responda automáticamente ante amenazas identificadas por los dispositivos de seguridad para minimizar el tiempo de reacción. | 5                |
| 2         | HU-6              | Recibir notificaciones en tiempo real               | Como propietario de un inmueble, quiero recibir notificaciones en tiempo real en mi móvil sobre cualquier alerta de seguridad para tomar acciones inmediatas. | 3                |
| 3         | HU-4              | Configurar notificaciones personalizadas            | Como empresa de seguridad, quiero configurar las alertas para recibir notificaciones específicas según los tipos de eventos en cada propiedad. | 3                |
| 4         | HU-2              | Controlar dispositivos de seguridad                 | Como propietario de un inmueble, quiero controlar mis dispositivos de seguridad desde la aplicación web para armar o desarmar la alarma. | 3                |
| 5         | HU-8              | Control de acceso remoto                            | Como propietario de un inmueble, quiero controlar el acceso a mi propiedad desde mi móvil para abrir o cerrar puertas de manera remota. | 3                |
| 6         | HU-7              | Acceso remoto a cámaras                             | Como empresa de seguridad, quiero acceder a las cámaras de las propiedades desde mi dispositivo móvil para verificar en tiempo real cualquier alerta. | 5                |
| 7         | HU-10             | Ver grabaciones de seguridad                        | Como propietario de un inmueble, quiero ver las grabaciones de seguridad desde mi móvil para revisar eventos pasados mientras estoy fuera de casa. | 5                |
| 8         | HU-5              | Reportar un incidente                               | Como propietario de un inmueble, quiero reportar un incidente directamente desde la aplicación web para que la empresa de seguridad lo gestione. | 3                |
| 9         | HU-1              | Ver historial de eventos                            | Como propietario de un inmueble, quiero poder ver el historial de los eventos para revisar incidentes pasados. | 2                |
| 10        | HU-3              | Resumen de eventos                                  | Como usuario, quiero un resumen de todos los eventos desde una única interfaz para gestionar los dispositivos de manera eficiente. | 3                |
| 11        | HU-26             | Uso compartido de dispositivos                      | Como propietario de un inmueble, quiero compartir el control de ciertos dispositivos con otros usuarios desde la app para que también puedan manejarlos. | 2                |
| 12        | HU-27             | Alertas de mantenimiento preventivo                 | Como propietario de un inmueble, quiero recibir alertas de mantenimiento preventivo de los dispositivos para evitar fallos y asegurar su operación continua. | 3                |
| 13        | HU-12             | Gestión de dispositivos conectados                  | Como administrador, quiero poder gestionar todos los dispositivos conectados para monitorear su estado y funcionamiento. | 3                |
| 14        | HU-11             | Gestión de usuarios                                 | Como administrador, quiero poder gestionar todos los usuarios desde el backend para controlar el acceso y los permisos de la plataforma. | 3                |
| 15        | HU-14             | Gestión de logs y auditoría                         | Como administrador, quiero poder acceder a los logs y realizar auditorías para monitorear la actividad del sistema y detectar anomalías. | 3                |
| 16        | HU-9              | Crear y gestionar alertas desde la app             | Como empresa de seguridad, quiero poder crear y gestionar alertas desde mi móvil para estar siempre en control, incluso cuando no estoy en la oficina. | 3                |
| 17        | HU-19             | Monitoreo de alertas en dispositivos edge          | Como propietario de un inmueble, quiero monitorear las alertas de mis dispositivos edge. | 3                |
| 18        | HU-22             | Monitoreo de sensores de movimiento                 | Como empresa de seguridad, quiero monitorear en tiempo real los sensores de movimiento de los dispositivos IoT para detectar intrusos. | 3                |
| 19        | HU-23             | Monitorización de baterías en dispositivos IoT      | Como empresa de seguridad, quiero monitorear el nivel de batería de los dispositivos IoT para asegurar que siempre estén operativos. | 2                |
| 20        | HU-24             | Automatización de escenarios                         | Como propietario de un inmueble, quiero crear escenarios automatizados en mi app para que los dispositivos IoT actúen en conjunto según la hora o eventos específicos. | 5                |
| 21        | HU-13             | Integración con sistemas de terceros                | Como administrador, quiero integrar la plataforma con sistemas de seguridad de terceros para ampliar las capacidades del sistema. | 3                |
| 22        | HU-20             | Reinicio remoto de dispositivos edge                 | Como administrador, quiero poder reiniciar remotamente los dispositivos en el edge para solucionar problemas de manera eficiente. | 2                |
| 23        | HU-16             | Detección de anomalías en tiempo real               | Como propietario de un inmueble, quiero que los dispositivos en el edge detecten anomalías en tiempo real para reaccionar de inmediato ante posibles amenazas. | 5                |
| 24        | HU-18             | Autonomía operativa de dispositivos edge            | Como empresa de seguridad, quiero que los dispositivos en el edge funcionen de manera autónoma si pierden conexión con el servidor para asegurar la continuidad del servicio. | 5                |
| 25        | HU-17             | Actualización remota de firmware                    | Como administrador, quiero poder actualizar remotamente el firmware de los dispositivos en el edge para asegurar su correcto funcionamiento y seguridad. | 3                |
| 26        | HU-21             | Control de luces inteligentes                        | Como propietario de un inmueble, quiero controlar las luces inteligentes de mi propiedad desde la app para encender o apagar según necesidad. | 3                |
| 27        | HU-15             | Configuración de políticas de seguridad              | Como administrador, quiero poder configurar políticas de seguridad para asegurar que todos los dispositivos y datos cumplan con los estándares requeridos. | 3                |
