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
El To-Be Scenario Mapping es una herramienta clave para visualizar el recorrido ideal de los usuarios al interactuar con un sistema de seguridad IoT. Este enfoque permite identificar y optimizar cada fase del proceso, asegurando que las soluciones se alineen con las necesidades y expectativas de los usuarios.

A través de este mapeo, se busca mejorar la eficiencia y la experiencia del usuario, fomentando la confianza y tranquilidad tanto de los propietarios de inmuebles como de las empresas de seguridad. A continuación, se presentan los To-Be Scenario Mapping para cada segmento.

* **Segmento 1: Dueños de inmuebles**

El To Be Scenario Mapping para los dueños de inmuebles tiene como objetivo visualizar el recorrido ideal que experimentarán estos usuarios al interactuar con un sistema de seguridad IoT. Al identificar cada paso que estos propietarios realizan, desde la investigación hasta el uso diario y mantenimiento del sistema, se puede comprender mejor cómo proporcionar una experiencia fluida y satisfactoria.

Este mapeo se centra en las acciones, pensamientos y emociones de los dueños de inmuebles en cada fase de interacción con el sistema. De este modo, se busca diseñar una solución que no solo sea eficiente y segura, sino también intuitiva y alineada con las expectativas y necesidades específicas de los usuarios. A través de este proceso, el objetivo es garantizar que los usuarios experimenten confianza, tranquilidad y satisfacción durante todo el ciclo de vida de su sistema de seguridad.

![To Be Property Owners](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/to-be-1.jpg)

* **Segmento 2: Empresa de seguridad**

El To Be Scenario Mapping para las empresas de seguridad ofrece una representación detallada de cómo estas organizaciones interactúan con los sistemas de seguridad IoT y los clientes a lo largo de todo el proceso de respuesta a incidentes. Desde la recepción de una alerta hasta la mejora continua de los protocolos y sistemas, este mapeo busca optimizar cada paso crítico para garantizar un servicio eficiente, preciso y confiable.

El enfoque está en los desafíos que enfrentan las empresas de seguridad al validar alertas, coordinar respuestas y asegurar que sus equipos y procedimientos estén siempre actualizados y preparados para incidentes futuros. A través de este mapeo, se pretende crear una experiencia integrada, en la que la tecnología y la comunicación con los clientes se alineen para ofrecer una respuesta rápida y efectiva, manteniendo la confianza y satisfacción de los usuarios.

![To Be Security Company](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/to-be-2.jpg)

## 3.2. User Stories

En esta sección se presentan las historias de usuario correspondientes a nuestra aplicación móvil, sitio web estático y dispositivos edge. Estas historias describen las características necesarias para nuestros dos segmentos objetivo. Además, se especifican los criterios de aceptación que nos permitirán verificar si las funcionalidades cumplen con las necesidades de los usuarios.

| **ID**  | **Título**                                                        | **Descripción**                                                                                                   | **Criterios de Aceptación**                                                                                                                                          | **Relacionado con (Epic ID)** |
|---------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| **HU-01** | Ver historial de eventos                                          | Como propietario de un inmueble, quiero poder ver el historial de los eventos para revisar incidentes pasados. | **Given** que el propietario está en la página Events **When** selecciona el evento **Then** puede ver todas las notificaciones en base al evento. <br><br> **Given** que no hay notificaciones en el evento seleccionado **When** selecciona la fila **Then** se muestra un mensaje indicando que no hay notificaciones para ese evento.           | Epic 1                        |
| **HU-02** | Configurar notificaciones personalizadas                          | Como empresa de seguridad, quiero configurar las alertas para recibir notificaciones específicas según los tipos de eventos en cada propiedad. | **Given** que el usuario está en la sección de configuraciones **When** crea una nueva alerta personalizada **Then** recibe notificaciones solo para los eventos configurados. <br><br> **Given** que hay varias alertas personalizadas creadas **When** elimina una alerta personalizada **Then** la alerta se elimina y ya no recibe notificaciones de ese tipo.            | Epic 1                        |
| **HU-03** | Controlar dispositivos de seguridad                               | Como propietario de un inmueble, quiero controlar mis dispositivos de seguridad desde la aplicación web para armar o desarmar la alarma. | **Given** que el propietario está en el panel de control de dispositivos **When** selecciona un dispositivo y una acción (armar/desarmar) **Then** el dispositivo realiza la acción y se muestra una notificación de confirmación. <br><br> **Given** que un dispositivo no responde **When** intenta armar o desarmar el dispositivo **Then** se muestra un mensaje de error indicando que no se pudo completar la acción. | Epic 2                        |
| **HU-04** | Resumen de eventos                                               | Como usuario, quiero un resumen de todos los eventos desde una única interfaz para gestionar los dispositivos de manera eficiente. | **Given** que el usuario está en el dashboard **When** selecciona una propiedad **Then** puede ver un resumen en tiempo real de todos los dispositivos y alertas de esa propiedad. <br><br> **Given** que hay una alerta activa en una propiedad **When** selecciona la propiedad **Then** se muestra la alerta en la parte superior del resumen con opciones para gestionarla.       | Epic 2                        |
| **HU-05** | Reportar un incidente                                             | Como propietario de un inmueble, quiero reportar un incidente directamente desde la aplicación web para que la empresa de seguridad lo gestione. | **Given** que el propietario está en la sección de reportes **When** llena el formulario de incidente y lo envía **Then** la empresa de seguridad recibe una notificación con los detalles del reporte. <br><br> **Given** que el formulario de reporte tiene campos obligatorios vacíos **When** intenta enviarlo **Then** se muestra un mensaje de error indicando que debe completar los campos obligatorios. | Epic 3                        |
| **HU-06** | Recibir notificaciones en tiempo real                             | Como propietario de un inmueble, quiero recibir notificaciones en tiempo real en mi móvil sobre cualquier alerta de seguridad para tomar acciones inmediatas. | **Given** que el propietario tiene la aplicación móvil instalada **When** se activa una alerta **Then** recibe una notificación push con la descripción del evento. <br><br> **Given** que la alerta no ha sido atendida en 5 minutos **When** la aplicación verifica el tiempo transcurrido **Then** envía una notificación de recordatorio al propietario. | Epic 4                        |
| **HU-07** | Acceso remoto a cámaras                                          | Como empresa de seguridad, quiero acceder a las cámaras de las propiedades desde mi dispositivo móvil para verificar en tiempo real cualquier alerta. | **Given** que la empresa de seguridad tiene acceso a la propiedad en la aplicación **When** selecciona la opción de cámaras **Then** puede ver las imágenes en vivo de todas las cámaras instaladas. <br><br> **Given** que una cámara está fuera de servicio **When** intenta acceder a las imágenes **Then** se muestra un mensaje indicando que la cámara no está disponible. | Epic 4                        |
| **HU-08** | Control de acceso remoto                                         | Como propietario de un inmueble, quiero controlar el acceso a mi propiedad desde mi móvil para abrir o cerrar puertas de manera remota. | **Given** que el propietario tiene la aplicación instalada **When** selecciona la opción de control de acceso **Then** puede abrir o cerrar puertas conectadas con un solo clic. <br><br> **Given** que una puerta está bloqueada **When** el propietario intenta abrirla desde la app **Then** se muestra un mensaje de error indicando que no se puede completar la acción. | Epic 5                      |
| **HU-09** | Crear y gestionar alertas desde la app                          | Como empresa de seguridad, quiero poder crear y gestionar alertas desde mi móvil para estar siempre en control, incluso cuando no estoy en la oficina. | **Given** que la empresa de seguridad está en la aplicación **When** crea una nueva alerta personalizada **Then** esta se activa y puede recibir notificaciones basadas en esa configuración. <br><br> **Given** que la empresa desea modificar una alerta activa **When** edita los parámetros de la alerta **Then** los cambios se reflejan de inmediato en la app. | Epic 5                       |
| **HU-10** | Ver grabaciones de seguridad                                      | Como propietario de un inmueble, quiero ver las grabaciones de seguridad desde mi móvil para revisar eventos pasados mientras estoy fuera de casa. | **Given** que el propietario está en la app **When** selecciona una fecha y hora **Then** puede ver la grabación correspondiente directamente desde su dispositivo móvil. <br><br> **Given** que no hay grabaciones disponibles para la fecha seleccionada **When** el propietario intenta visualizarla **Then** se muestra un mensaje indicando que no hay grabaciones para ese periodo. | Epic 6                       |
| **HU-11** | Gestión de usuarios                                              | Como administrador, quiero poder gestionar todos los usuarios desde el backend para controlar el acceso y los permisos de la plataforma. | **Given** que el administrador está en el panel de administración **When** agrega, edita o elimina un usuario **Then** los cambios se reflejan en la aplicación web y móvil. <br><br> **Given** que un usuario ha sido eliminado **When** el administrador revisa la lista de usuarios **Then** el usuario eliminado ya no aparece en la lista. | Epic 7                        |
| **HU-12** | Gestión de dispositivos conectados                                 | Como administrador, quiero poder gestionar todos los dispositivos conectados para monitorear su estado y funcionamiento. | **Given** que el administrador está en el panel de administración **When** visualiza el listado de dispositivos **Then** puede actualizar su estado, ver logs y desconectar dispositivos si es necesario. <br><br> **Given** que un dispositivo no responde **When** el administrador intenta actualizar su estado **Then** se muestra un mensaje de error indicando que el dispositivo está desconectado. | Epic 7                        |
| **HU-13** | Integración con sistemas de terceros                               | Como administrador, quiero integrar la plataforma con sistemas de seguridad de terceros para ampliar las capacidades del sistema. | **Given** que el administrador está en el panel de integraciones **When** configura una integración nueva **Then** los dispositivos y datos del sistema de terceros se sincronizan con la plataforma. <br><br> **Given** que la integración ha fallado **When** el administrador revisa los logs de la integración **Then** se muestra el motivo del fallo y las posibles soluciones. | Epic 7                        |
| **HU-14** | Gestión de logs y auditoría                                       | Como administrador, quiero poder acceder a los logs y realizar auditorías para monitorear la actividad del sistema y detectar anomalías. | **Given** que el administrador está en la sección de logs **When** selecciona un rango de fechas **Then** puede ver todas las actividades registradas en ese periodo. <br><br> **Given** que el administrador necesita exportar los logs **When** selecciona la opción de exportación **Then** los logs se descargan en un archivo CSV. | Epic 8                        |
| **HU-15** | Configuración de políticas de seguridad                            | Como administrador, quiero poder configurar políticas de seguridad para asegurar que todos los dispositivos y datos cumplan con los estándares requeridos. | **Given** que el administrador está en la sección de políticas **When** establece una nueva política de seguridad **Then** se aplica a todos los dispositivos y usuarios de la plataforma. <br><br> **Given** que una política de seguridad no cumple con los estándares **When** el administrador intenta guardarla **Then** se muestra un mensaje de advertencia y la política no se guarda. | Epic 8                        |
| **HU-16** | Detección de anomalías en tiempo real                             | Como propietario de un inmueble, quiero que los dispositivos en el edge detecten anomalías en tiempo real para reaccionar de inmediato ante posibles amenazas. | **Given** que tengo dispositivos edge instalados **When** ocurre una anomalía **Then** el dispositivo envía una alerta inmediata a la app móvil y web. <br><br> **Given** que la anomalía se ha solucionado **When** el dispositivo envía un informe de la resolución **Then** se notifica al propietario. | Epic 9                       |
| **HU-17** | Actualización remota de firmware                                    | Como administrador, quiero poder actualizar remotamente el firmware de los dispositivos en el edge para asegurar su correcto funcionamiento y seguridad. | **Given** que estoy en el panel de dispositivos **When** selecciono actualizar el firmware de un dispositivo **Then** el dispositivo se actualiza automáticamente y se reinicia. <br><br> **Given** que la actualización falla **When** el sistema intenta de nuevo **Then** se envía una notificación al administrador sobre el error. | Epic 9                       |
| **HU-18** | Autonomía operativa de dispositivos edge                           | Como empresa de seguridad, quiero que los dispositivos en el edge funcionen de manera autónoma si pierden conexión con el servidor para asegurar la continuidad del servicio. | **Given** que un dispositivo edge pierde conexión **When** continúa operando de manera autónoma **Then** las alertas y registros se guardan localmente hasta que se restablezca la conexión. <br><br> **Given** que la conexión se restablece **When** se sincronizan los datos almacenados **Then** el servidor muestra el historial completo de alertas. | Epic 9                       |
| **HU-19** | Monitoreo de alertas en dispositivos edge                          | Como propietario de un inmueble, quiero monitorear las alertas de mis dispositivos edge.                              | **Given** que estoy en el dashboard de alertas **When** le doy click a un dispositivo **Then** puedo ver un historial de alertas del dispositivo y recibir sugerencias de optimización. <br><br> **Given** que un dispositivo ha tenido múltiples alertas **When** reviso el historial **Then** se muestran estadísticas de frecuencia y tipo de alertas. | Epic 10                       |
| **HU-20** | Reinicio remoto de dispositivos edge                               | Como administrador, quiero poder reiniciar remotamente los dispositivos en el edge para solucionar problemas de manera eficiente. | **Given** que estoy en el panel de dispositivos **When** selecciono la opción de reinicio **Then** el dispositivo se reinicia automáticamente y notifica al usuario. <br><br> **Given** que el dispositivo no responde **When** intento reiniciarlo **Then** se envía una alerta al administrador indicando que el dispositivo está inoperativo. | Epic 10                      |
| **HU-21** | Control de luces inteligentes                                       | Como propietario de un inmueble, quiero controlar las luces inteligentes de mi propiedad desde la app para encender o apagar según necesidad. | **Given** que estoy en la app móvil **When** selecciono una luz que quiero modificar **Then** puedo encenderla, apagarla o ajustar la intensidad. <br><br> **Given** que la luz está encendida **When** la apago **Then** se refleja el cambio en la app inmediatamente. | Epic 11                       |
| **HU-22** | Monitoreo de sensores de movimiento                                 | Como empresa de seguridad, quiero monitorear en tiempo real los sensores de movimiento de los dispositivos IoT para detectar intrusos. | **Given** que estoy en el dashboard de sensores **When** un sensor detecta movimiento **Then** recibo una alerta inmediata en la app. <br><br> **Given** que la alerta se activa **When** reviso el registro de eventos **Then** se muestra la hora y la ubicación del movimiento detectado. | Epic 11                       |
| **HU-23** | Monitorización de baterías en dispositivos IoT                      | Como empresa de seguridad, quiero monitorear el nivel de batería de los dispositivos IoT para asegurar que siempre estén operativos. | **Given** que estoy en el dashboard de energía **When** el nivel de batería es bajo **Then** recibo una alerta para reemplazar o recargar el dispositivo. <br><br> **Given** que el nivel de batería se ha recuperado **When** recargo el dispositivo **Then** se notifica el estado actualizado de la batería. | Epic 12                       |
| **HU-24** | Automatización de escenarios                                        | Como propietario de un inmueble, quiero crear escenarios automatizados en mi app para que los dispositivos IoT actúen en conjunto según la hora o eventos específicos. | **Given** que estoy en la app **When** configuro un escenario **Then** los dispositivos correspondientes se activan o desactivan automáticamente según lo programado. <br><br> **Given** que un escenario está activo **When** ocurre el evento programado **Then** se notifica al usuario de la acción realizada. | Epic 12                       |
| **HU-25** | Respuesta automatizada ante amenazas                                 | Como empresa de seguridad, quiero que el sistema responda automáticamente ante amenazas identificadas por los dispositivos de seguridad para minimizar el tiempo de reacción. | **Given** que una amenaza es detectada **When** el sistema la confirma **Then** se activan las medidas de seguridad preconfiguradas (alarma, bloqueo de puertas, notificación a autoridades). <br><br> **Given** que las medidas de seguridad están activadas **When** se recibe una nueva alerta **Then** el sistema registra la acción y notifica a los usuarios autorizados. | Epic 13                       |
| **HU-26** | Uso compartido de dispositivos                                       | Como propietario de un inmueble, quiero compartir el control de ciertos dispositivos con otros usuarios desde la app para que también puedan manejarlos. | **Given** que estoy en la sección de dispositivos **When** configuro el uso compartido **Then** el otro usuario tiene acceso limitado o completo según lo configurado. <br><br> **Given** que el acceso está compartido **When** el otro usuario intenta acceder **Then** se registra la actividad y se notifica al propietario. | Epic 14                       |
| **HU-27** | Alertas de mantenimiento preventivo                                  | Como propietario de un inmueble, quiero recibir alertas de mantenimiento preventivo de los dispositivos para evitar fallos y asegurar su operación continua. | **Given** que tengo dispositivos operando **When** alguno necesita mantenimiento **Then** recibo una alerta en la app y el email con los pasos a seguir para realizar el mantenimiento. <br><br> **Given** que he realizado el mantenimiento **When** actualizo el estado en la app **Then** se registra la acción y se confirma la operación continua del dispositivo. | Epic 15                       |
| **HU-28** | Sección de "Hero" con slogan y mensaje de bienvenida               | Como visitante, quiero ver una sección de "Hero" con un slogan atractivo y un mensaje de bienvenida al acceder a la landing page. | **Given** que el usuario accede a la landing page **When** se muestra la sección de "Hero" **Then** debe incluir un slogan y un mensaje de bienvenida visualmente atractivos. | Epic 16                       |
| **HU-29** | Sección de "Solutions" para mostrar tecnologías y beneficios       | Como visitante, quiero ver una sección de "Solutions" que muestre las tecnologías y beneficios del sistema. | **Given** que el usuario está en la landing page **When** accede a la sección de "Solutions" **Then** debe ver las tecnologías y beneficios destacados de manera clara y concisa. | Epic 16                        |
| **HU-30** | Sección de "Followers" con experiencias positivas de usuarios      | Como visitante, quiero ver una sección de "Followers" que presente experiencias positivas de usuarios previos. | **Given** que el usuario está en la landing page **When** accede a la sección de "Followers" **Then** debe visualizar testimonios o experiencias positivas de usuarios. | Epic 16                        |
| **HU-31** | Sección de "Learn more about us" con explicación visual del sistema | Como visitante, quiero ver una sección que explique visualmente el sistema y sus características. | **Given** que el usuario está en la landing page **When** accede a la sección "Learn more about us" **Then** debe encontrar una explicación visual clara del sistema. | Epic 17                        |
| **HU-32** | Sección de "Política de Privacidad" o "Protección de Datos"      | Como visitante, quiero acceder a la sección de "Política de Privacidad" para entender cómo se protegen mis datos. | **Given** que el usuario está en la landing page **When** accede a la sección de "Política de Privacidad" **Then** debe visualizar la información relevante sobre la protección de datos. | Epic 1                        |
| **HU-33** | Sección de "Llamada a la Acción" para descarga en Google Play/App Store | Como visitante, quiero ver una sección de "Llamada a la Acción" que me invite a descargar la aplicación. | **Given** que el usuario está en la landing page **When** accede a la sección de "Llamada a la Acción" **Then** debe ver los botones para descargar en Google Play y App Store. | Epic 17                        |
| **HU-34** | Sección de "Subscription Plans" con diferentes opciones de planes  | Como visitante, quiero ver una sección de "Subscription Plans" que muestre las diferentes opciones de suscripción. | **Given** que el usuario está en la landing page **When** accede a la sección de "Subscription Plans" **Then** debe visualizar las diferentes opciones de planes y precios. | Epic 17                        |
| **HU-35** | Diseño responsivo para usuarios móviles                             | Como usuario móvil, quiero que la landing page se vea bien en mi dispositivo para una mejor experiencia de usuario. | **Given** que un usuario accede a la landing page desde un dispositivo móvil **When** carga la página **Then** debe mostrarse un diseño responsivo y optimizado para móviles. | Epic 18                        |
| **HU-36** | Cambio de idioma en la landing page                            | Como visitante, quiero poder seleccionar mi idioma en el sitio web para comprender toda la información y navegar de manera más efectiva | **Given** que el usuario está en la landing page **When** selecciona un idioma de la opción de idiomas disponible **Then** el contenido de la página se actualiza al idioma seleccionado. <br><br> **Given** que el usuario cambia el idioma **When** navega a diferentes secciones de la página **Then** el contenido se muestra en el idioma elegido en todas las secciones. | Epic 18                        |
| **HU-37**| Monitoreo y almacenamiento de datos de sensores de movimiento | Como usuario, quiero que el sistema detecte movimientos dentro de mi propiedad y registre estos eventos para monitorear posibles intrusos. | **Given** que un sensor de movimiento se activa **When** el sistema recibe la señal **Then** se almacenan los datos en el backend con fecha, hora y ubicación. <br><br> **Given** que se detecta movimiento inusual **When** el sistema lo verifica **Then** se envía una notificación inmediata al usuario.                                              | Epic 19                        |
| **HU-38**| Detección de humo y alerta de emergencia               | Como usuario, quiero que el sistema detecte la presencia de humo en mi propiedad y me alerte inmediatamente para poder tomar acción. | **Given** que el detector de humo activa **When** el sistema recibe la señal **Then** se envía una alerta de emergencia al dispositivo del usuario. <br><br> **Given** que se detecta humo **When** el sistema activa la alarma **Then** se registra el evento en el historial.                                                                 | Epic 19                        |
| **HU-39**| Alerta por cambios de temperatura inesperados           | Como usuario, quiero que el sistema monitoree la temperatura de mi propiedad y me notifique en caso de cambios bruscos, para poder identificar riesgos como incendios. | **Given** que el sistema recibe una lectura de temperatura **When** verifica que está fuera de rango **Then** activa una alerta para el usuario. <br><br> **Given** que se registra un cambio brusco de temperatura **When** el sistema guarda la información **Then** se incluye fecha, hora y temperatura exacta en el registro.                              | Epic 19                        |
| **HU-40**| Activación y desactivación de alarmas                  | Como usuario, quiero poder activar o desactivar la alarma desde la aplicación para tener control sobre la seguridad de mi propiedad. | **Given** que el usuario está en la aplicación **When** activa o desactiva la alarma **Then** el estado se actualiza en el backend en tiempo real. <br><br> **Given** que se intenta desactivar la alarma sin autorización **When** el sistema lo bloquea **Then** se envía una notificación de intento no autorizado.                                        | Epic 19                        |
| **HU-41**| Historial de eventos de seguridad                       | Como usuario, quiero poder acceder al historial de eventos de seguridad para revisar la actividad en mi propiedad.  | **Given** que el usuario accede al historial **When** solicita ver eventos de seguridad **Then** se muestra un registro detallado de activaciones y cambios. <br><br> **Given** que el usuario desea filtrar el historial **When** selecciona las opciones de filtro **Then** se muestran los eventos según los criterios seleccionados.                       | Epic 20                        |
| **HU-42**| Configuración de notificaciones personalizadas          | Como usuario, quiero configurar qué tipo de notificaciones recibir para que el sistema me alerte solo en situaciones específicas. | **Given** que el usuario está en la sección de configuraciones **When** activa o desactiva notificaciones por tipo de sensor **Then** los cambios se aplican en tiempo real. <br><br> **Given** que el usuario guarda sus preferencias **When** el sistema envía notificaciones según la configuración establecida **Then** se registra el tipo de notificación. | Epic 20                        |
| **HU-43**| Pruebas periódicas de dispositivos                      | Como usuario, quiero recibir notificaciones para realizar pruebas periódicas de los dispositivos IoT para asegurar que funcionan correctamente. | **Given** que el backend genera un recordatorio **When** el usuario recibe una notificación para realizar una prueba **Then** se registra la fecha y hora de la prueba en el sistema. <br><br> **Given** que un dispositivo falla durante la prueba **When** el sistema envía una notificación **Then** se recomienda realizar una revisión del dispositivo. | Epic 20                        |
| **HU-44**| Integración con servicios de emergencia                 | Como usuario, quiero que el sistema notifique a los servicios de emergencia automáticamente en caso de eventos críticos para una respuesta rápida. | **Given** que se detecta un evento crítico **When** el sistema está configurado para alertar a servicios de emergencia **Then** se envían los datos específicos del evento y la ubicación. <br><br> **Given** que la notificación se ha enviado **When** el sistema registra la hora del envío **Then** se confirma la acción en el registro.                        | Epic 20                       |

## 3.3. Impact Mapping
La herramienta denominada Impact Mapping consiste en una forma visual de representar las metas que nos plasmamos para llegar a cada sector de nuestro público. Por esta razón, el equipo utilizó este artefacto con el fin de definir nuestro camino para alcanzar a los segmentos objetivos. De este modo, al final del mapa mental identificamos las acciones y funcionalidades que debemos llevar a cabo para formar el proyecto de manera eficiente.

### User: Dueño de Inmuebles

A continuación, se presenta el Impact Map en el usuario, dueño de inmuebles; para la cual nos basamos en las User Stories de nuestro proyecto, brindando las alternativas con las que dispone los aplicativos para solucionar y satisfacer las necesidades del usuario.
![Impact Mapping Owner](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/impact-map-dueño-inmueble.png)

### User: Empresa de seguridad
Este mapa de impacto incluye los objetivos empresariales, los efectos deseados en la organización de seguridad y las historias de usuario relacionadas. El enfoque es en mejorar la eficiencia operativa y la satisfacción del cliente mediante el uso de tecnología IoT para vigilancia en tiempo real y respuestas automatizadas a amenazas.
![Impact Mapping Business](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/impact-map-seguridad.png)

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
#### 4.1.3.3. Software Architecture Container Level Diagrams
#### 4.1.3.4. Software Architecture Deployment Diagrams
## 4.2. Tactical-Level Domain-Driven Design
### 4.2.1. Bounded Context: Subscription & Payments context
#### 4.2.1.1. Domain Layer
#### 4.2.1.2. Interface Layer
#### 4.2.1.3. Application Layer
#### 4.2.1.4. Infrastructure Layer
#### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams
#### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams
##### 4.2.1.6.2. Bounded Context Database Design Diagram
### 4.2.2. Bounded Context: Device
#### 4.2.2.1 Domain Layer
#### 4.2.2.2 Interface Layer
#### 4.2.2.3. Application Layer
#### 4.2.3.4. Infrastructure Layer
#### 4.2.2.5. Bounded Context Software Architecture Component Level Diagrams
#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams
#### 4.2.2.6.2. Bounded Context Domain Layer Class Diagrams
### 4.2.3. Bounded Context: Area
#### 4.2.3.1. Domain Layer
#### 4.2.3.2. Interface Layer
#### 4.2.3.3. Application Layer
#### 4.2.3.4. Infrastructure Layer
#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams
#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams
#### 4.2.3.6.2. Bounded Context Database Design Diagram
### 4.2.4. Bounded Context: User context
#### 4.2.4.1. Domain Layer
#### 4.2.4.2. Interface Layer
#### 4.2.4.3. Application Layer
#### 4.2.4.4. Infrastructure Layer
#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams
#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams
##### 4.2.4.6.2. Bounded Context Database Design Diagram
### 4.2.5. Bounded Context: Events context
#### 4.2.5.1. Domain Layer
#### 4.2.5.2. Interface Layer
#### 4.2.5.3. Application Layer
#### 4.2.5.4. Infrastructure Layer
#### 4.2.5.5. Bounded Context Software Architecture Component Level Diagrams
#### 4.2.5.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.5.6.1. Bounded Context Domain Layer Class Diagrams
##### 4.2.5.6.2. Bounded Context Database Design Diagram

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
### 5.4.3. Applications Mock-ups
### 5.4.4. Applications User Flow Diagrams
## 5.5. Applications Prototyping

# CAPÍTULO VI: PRODUCT IMPLEMENTATION, VALIDATION & DEPLOYMENT
## 6.1. Software Configuration Management
### 6.1.1. Software Development Environment Configuration
### 6.1.2. Source Code Management
### 6.1.3. Source Code Style Guide & Conventions
### 6.1.4. Software Deployment Configuration
## 6.2. Landing Page, Services & Applications Implementation
### 6.2.1. Sprint 1
#### 6.2.1.1. Sprint Planning 1
#### 6.2.1.2. Sprint Backlog 1
#### 6.2.1.3. Development Evidence for Sprint Review
#### 6.2.1.4. Testing Suite Evidence for Sprint Review
#### 6.2.1.5. Execution Evidence for Sprint Review
#### 6.2.1.6. Software Deployment Evidence for Sprint Review
#### 6.2.1.7. Team Collaboration Insights during Sprint