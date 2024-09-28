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
Es una técnica colaborativa que nos permite explorar a fondo el dominio de nuestra aplicación de FalconShield, para realizar el proceso, se llevó a cabo diversas reuniones y con apoyo de la herramienta Miro se pudo desarrollar todo el flujo y los pasos. Para el primer paso se analizaron diversas opiniones sobre los posibles eventos del dominio y se fue clasificando según criterios, tales como frecuencia, relevancia, etc.

1. **Primer paso: Unstructured Exploration**

    Para este paso se analizaron diversas opiniones sobre los posibles eventos del dominio y se fue clasificando según criterios, tales como frecuencia, relevancia, etc.
    
    ![event](src/images/event-1.png)

2. **Segundo paso: Timelines**
   
    En este paso se procedió a ordenar los eventos en una línea de tiempo, para poder visualizar mejor el flujo de los eventos y las interacciones entre ellos.
    
    ![timeline](src/images/event-2.png)

3. **Tercer paso: Pain Points**
   
    En este paso se identifaron posibles cuellos de botella o problemas en el flujo de eventos, para poder abordarlos y solucionarlos de manera efectiva.
    
    ![pain](src/images/event-3.png)

4. **Cuarto paso: Pivotal Points**
   
    En este paso se identificaron puntos o eventos importantes que pueden ser cruciales para el funcionamiento del sistema, y que deben ser considerados con especial atención.

    ![pivotal](src/images/event-4.png)

5. **Quinto paso: Commands**
    Aquí se identificaron los comandos que se pueden ejecutar en el sistema, y que generan eventos en el dominio.
    
    ![commands](src/images/event-5.png)

#### 4.1.1.1 Candidate Context Discovery
Una vez identificados los eventos clave, se procedió a seguir los otros pasos para finalmente agruparlos en contextos delimitados, que representan áreas de interés o responsabilidades dentro del sistema. Estos contextos se definen en función de la cohesión de los eventos y las reglas de negocio asociadas.

1. **Sexto paso: Policies**
   
    En este paso se identificaron los eventos que deberían ser ejecutados de forma automática por el sistema, sin intervención del usuario o si se requiere de alguna política de negocio para su ejecución.

    ![alt text](src/images/event-6.png)

2. **Séptimo paso: Read Models**
   
    En este paso se identificaron los eventos que generan información que debe ser almacenada y consultada posteriormente, para poder visualizar el estado actual del sistema.

    ![alt text](src/images/event-7.png)

3. **Octavo paso: External Systems**
   
    En este paso se identificaron los eventos que interactúan con sistemas externos, como APIs de terceros, bases de datos, etc.

    ![alt text](src/images/event-8.png)

4. **Noveno paso: Aggregates**
   
    En este paso se identificaron los eventos que están relacionados entre sí y que pueden ser agrupados en un agregado, para poder gestionarlos de forma coherente.

    ![alt text](src/images/event-9.png)

5. **Décimo paso: Bounded Contexts**
   
    En este paso se agruparon los eventos en contextos delimitados, que representan áreas de interés o responsabilidades dentro del sistema. Estos contextos se definen en función de la cohesión de los eventos y las reglas de negocio asociadas.

    ![alt text](src/images/event-10.png)

Enlace a los diagramas de EventStorming: [EventStorming](https://miro.com/app/board/uXjVKjBJwpE=/?share_link_id=833719450756)

#### 4.1.1.2 Domain Message Flows Modeling

Para el modelado de los flujos de mensajes del dominio, se utilizó la técnica de EventStorming para identificar los eventos clave y las interacciones entre ellos. A partir de estos eventos, se crearon diagramas de flujo de mensajes que representan cómo se comunican los distintos componentes del sistema para lograr los objetivos del negocio. A continuación, se presentan los diagramas de flujo de mensajes para los contextos identificados en el paso anterior.

1. Sincronización del sistema de seguridad:
![alt text](src/images/message-flow-1.png)

2. Alerta y notificación de eventos:
![alt text](src/images/message-flow-2.png)

3. Alerta y notificación de eventos:
![alt text](src/images/message-flow-3.png)

4. Respuesta a la activación de la alarma:
![alt text](src/images/message-flow-4.png)

#### 4.1.1.3 Bounded Context Canvases
### 4.1.2. Context Mapping

1. **Events Management Context - Notification Management Context (Customer/Supplier):**
  La relación entre estos dos bounded contexts sigue el patrón Customer/Supplier. El Events Management Context es el proveedor que genera eventos críticos como alertas de seguridad o cambios en el estado de los dispositivos IoT. El Notification Management Context, como cliente, consume estos eventos y se encarga de enviar notificaciones al usuario a través de distintos canales (correo, SMS, etc.).

    ![alt text](src/images/412-1.jpg)

2. **IoT Asset Management Context - Software Update Context (Conformist):**
  El IoT Asset Management Context, encargado de gestionar los dispositivos IoT, depende del Software Update Context para implementar actualizaciones y parches. En este caso, el primero actúa como un Conformist, ya que debe adherirse a las reglas y servicios proporcionados por el Software Update Context sin imponer sus propias reglas, asegurando que las actualizaciones se apliquen de manera consistente.

    ![alt text](src/images/412-2.jpg)

3.	**Security Shield Management System Context - Identity and Access Management Context (Shared Kernel):**
  Ambos bounded contexts comparten un núcleo común (Shared Kernel), ya que el Security Shield Management System necesita autenticar y autorizar a los usuarios y dispositivos, lo cual está estrechamente ligado con las políticas y mecanismos del Identity and Access Management Context. Debido a la naturaleza crítica de la seguridad, estas dos áreas deben compartir información sensible y estar completamente sincronizadas en términos de datos y lógicas de negocio relacionadas con la identidad.

    ![alt text](src/images/412-3.jpg)

4.	**Subscription and Payment Context - Notification Management Context (Anti-Corruption Layer):**
  La relación entre estos dos bounded contexts se beneficia de un Anti-Corruption Layer para traducir y aislar los modelos de dominio. El Subscription and Payment Context maneja información financiera y suscripciones, mientras que el Notification Management Context envía alertas sobre el estado de las suscripciones o pagos. Para evitar que las complejidades del modelo de pagos interfieran con la simplicidad del sistema de notificaciones, se utiliza una capa anti-corrupción que actúa como interfaz entre ambos contexts.

    ![alt text](src/images/412-4.jpg)

### 4.1.3. Software Architecture

En esta parte, mostraremos la representación de la Arquitectura de Software de la solución en base a los modelos C4 para poder obtener una mejor visión de nuestro sistema

#### 4.1.3.1. Software Architecture System Landscape Diagram

Este diagrama nos ofrece una visión mas general de como es la interacción de los usuarios con los sistemas externos, nos permite comprender la conexión de los componentes para contribuir al funcionamiento general de las aplicaciones.

![landscape](src/images/landscape%20diagram.jpg)

#### 4.1.3.2. Software Architecture Context Level Diagrams

En este tipo de diagramas, se muestra como nuestro sistema interactúa con elementos externos.

![contexto](src/images/contexto.jpg)

En nuestro diagrama mostramos a los usuarios que son los consumidores de inmuebles o negocios que buscan mantener mejorar la seguridad de su inmueble, este esta conectado con la aplicación para que el usuario pueda interactuar y finalmente se conecta con un servicio externo que utilizamos para el envío de notificaciones.

#### 4.1.3.2. Software Architecture Container Level Diagrams

Son representaciones visuales de la arquitectura de software a nivel de contenedores, que muestran cómo se agrupan y se comunican los distintos componentes y servicios dentro de un sistema o aplicación. Estos diagramas proporcionan una vista detallada de la organización de los contenedores de software, lo que ayuda a entender la estructura y las interacciones en la arquitectura general.

![container](src/images/container.png)

Para el diagrama de contenedores desglosamos a nuestros usuarios que son el propietario de inmuebles y el usuario de seguridad, cada uno interactua con nuestras aplicaciones en este caso el propietario interactua con nuestro Single Page Application, Web Application y Mobile Application dado que podra manejar un sistema más integral. Asimismo el usuario de seguridad tendra su tipo de acceso en el Web Application y Mobile Application para el monitoreo de las alarmas de seguridad.
Pasando con las aplicaciones propuestas, tenemos que el Single Page Application que es una primera vista de nuestra propuesta de solucion se conect con el Web Application.
Para el Web Application tenemos que se conecta con la API de la applicacion y esta misma API va a una base de datos de la aplicacion. 
Para lo que es el Mobile Application tiene conexion a su misma base de datos y conexion con el API principal de nuestra aplicacion. 
Asi tambien tenemos nuestros dispositivo IoT, el cual se conecta con el edge API y este a su vez a su base de datos con el API general de todo la aplicacion.
Finalmente, el API principal lo conectamos con nuestro servicio externo de mensajeria AWS SNS.

#### 4.1.3.3. Software Architecture Deployment Diagrams

Son representaciones gráficas que ilustran cómo se despliegan y ejecutan los componentes de software en la infraestructura de hardware o en un entorno de producción.

![deployment](src/images/deployment.jpg)

## 4.2. Tactical-Level Domain-Driven Design
### 4.2.1. Bounded Context: Subscription & Payments context
El Subscription and Payment Context abarca todos los procesos y funciones relacionados con la gestión de suscripciones y pagos dentro de nuestro sistema. Este contexto es responsable de manejar la creación, modificación y cancelación de suscripciones, así como de procesar pagos y gestionar el estado de los mismos. Incluye la administración de detalles relacionados con los clientes, el seguimiento de las facturas y el estado de cada pago, y la sincronización con sistemas externos como Stripe. Asegura que las suscripciones y pagos se gestionen de manera eficiente y precisa, proporcionando una experiencia de servicio continua y sin interrupciones para los usuarios. A continuación, se detallan las clases identificadas en este contexto:

1. Clase Customer
    - Propósito: La clase Customer representa a un cliente en el sistema. Contiene la información esencial del cliente, como su nombre y correo electrónico, y un identificador que enlaza con el sistema de Stripe para gestionar pagos y suscripciones
    - Atributos:
      - `id: string` - Identificador único del cliente
      - `name: String` - Nombre del cliente
      - `email: String` - Correo electrónico del cliente
      - `stripeCustomerId: String` - Identificador del cliente en el sistema de Stripe
    - Métodos:
      - `getCustomerDetails(): CustomerDetails` - Retorna los detalles básicos del cliente (nombre y correo electrónico)
      - `registerStripeCustomer(): void` - Registra al cliente en Stripe
   	- Relaciones:
     	- `1...n` con Subscription, ya que un cliente puede tener varias suscripciones activas.

    ![alt text](src/images/customer-class.png)

2. Clase Subscription
    - Propósito: La clase Subscription gestiona las suscripciones de un cliente a un servicio específico. Mantiene los detalles esenciales, como el estado de la suscripción y las fechas de inicio y finalización. Los detalles más complejos de la suscripción son manejados por Stripe.
    - Atributos:
      - `id: string` - Identificador único de la suscripción
      - `status: string` - Estado actual de la suscripción (ejm: ACTIVA, CANCELADA, etc.)
      - `planId: string` - Identificador del plan de suscripción
      - `status: string` - Estado actual de la suscripción (activo, inactivo, cancelado)
      - `startDate: Date` - Fecha de inicio de la suscripción
      - `endDate: Date` - Fecha de finalización de la suscripción
      - `stripeSubscriptionId: string` - Identificador de la suscripción en Stripe
    - Métodos:
      - `getSubscriptionDetails(): SubscriptionDetails` - Retorna los detalles de la suscripción
      - `cancelSubscription(): void` - Cancela la suscripción
    - Relaciones:
      - `n...1` con Customer, ya que una suscripción pertenece a un cliente.
      - `1...n` con Payment, una suscripción puede tener múltiples pagos.

    ![alt text](src/images/subscription-class.png)

3. Clase Payment
    - Propósito: Esta clase almacena la información de los pagos realizados por un cliente en relación con una suscripción. Aunque Stripe gestiona el procesamiento de pagos, esta clase registra información relevante localmente, como el estado y monto del pago.
    - Atributos:
      - `id: string` - Identificador único del pago
      - `amount: double` - Monto del pago
      - `currency: string` - Moneda en la que se realizó el pago (ejm: USD, EUR)
      - `paymentDate: Date` - Fecha en la que se procesó el pago
      - `status: string` - Estado actual del pago (ejm: SUCCEEDED, FAILED)
      - `stripePaymentId: string` - Identificador del pago en el sistema de Stripe
    - Métodos:
      - `getPaymentDetails(): PaymentDetails` - Retorna los detalles del pago
    - Relaciones:
      - `n...1` con Subscription, un pago pertenece a una suscripción.
      - `1...n` con Invoice, un pago puede tener varias facturas asociadas.

    ![alt text](src/images/payment-class.png)

4. Clase Invoice
    - Propósito: Esta clase representa una factura generada por un pago. Aunque Stripe emite las facturas, esta clase localiza la información esencial de las mismas, como el monto total y la fecha de emisión.
    - Atributos:
      - `id: string` - Identificador único de la factura
      - `invoiceDate: Date` - Fecha de emisión de la factura
      - `totalAmount: double` - Monto total de la factura
      - `stripeInvoiceId: string` - Identificador de la factura en Stripe
    - Métodos:
      - `getInvoiceDetails(): InvoiceDetails` - Retorna los detalles de la factura
    - Relaciones:
      - `n...1` con Payment, una factura pertenece a un pago.

    ![alt text](src/images/invoice-class.png)

#### 4.2.1.1. Domain Layer

- Clases Core de la aplicación:
  - Entities:
    1. Customer: Representa a un usuario de la aplicación móvil que se suscribe a servicios IoT de seguridad. Esta entidad contiene la información básica del cliente y está relacionada con las suscripciones que tiene activas.
    ![alt text](src/images/customer-class-entity.png)

    2. Subscription: Representa una suscripción de un cliente a un plan específico. Esta clase encapsula el estado y los detalles relevantes de la suscripción, como su duración y la integración con Stripe.
    ![alt text](src/images/subscription-class-entity.png)

    3. Payment: Esta entidad representa un pago asociado a una suscripción, aunque Stripe procesa los pagos, esta entidad almacena localmente la información esencial del pago.
    ![alt text](src/images/payment-class-entity.png)

    4. Invoice: La entidad Invoice representa una factura generada por un pago hecho por Stripe, esta entidad almacena localmente los detalles esenciales de la factura.
    ![alt text](src/images/invoice-class-entity.png)

  - Value Objects:
    1. SubscriptionPlan: Encapsula los detalles de un pago, como el monto, la moneda y la fecha de procesamiento. Este objeto se utiliza para transmitir información de pago entre las capas de la aplicación.

    ![alt text](src/images/subscriptionplan-class-vo.png)

    2. Money: Encapsula el concepto de dinero, incluyendo el monto y la moneda. Se utiliza en los pagos, planes de suscripción y otros.    

    ![alt text](src/images/money-class-vo.png)

    3. Currency: Este enumerado define los códigos de moneda estándar que se utilizan en la aplicación. Se utiliza para garantizar la consistencia en la representación de monedas en toda la aplicación.

    ![alt text](src/images/currency-enum.png)
    
    4. SubscriptionStatus: Este enumerado define los posibles estados de una suscripción, como activa, cancelada o pendiente, se utiliza para controlar el ciclo de vida de las suscripciones.

    ![alt text](src/images/subscriptionstatus-enum.png)

    5. PaymentStatus: Este enumerado define los estados posibles de un pago, como exitoso, fallido o pendiente. Se utiliza para rastrear el estado de los pagos.

    ![alt text](src/images/paymentstatus-enum.png)
  
  - Aggregates:
    1. CustomerAggregate: Eencapsula la lógica de negocio relacionada con los clientes y sus suscripciones. Esto permite gestionar de manera coherente y transaccional las operaciones relacionadas con los clientes.

    ![alt text](src/images/customeraggregate.png)
  
  - Domain Services:
    1. SubscriptionService: Este servicio contiene la lógica de negocio relacionada con la gestión de suscripciones, como la creación, cancelación y renovación de suscripciones. Este servicio se encarga de coordinar las operaciones de suscripción.

    ![alt text](src/images/subscriptionservice.png)

- Reglas de negocio:
  - Las suscripciones deben renovarse automáticamente a menos que se cancelen antes de la fecha de renovación.
  - No se puede cancelar una suscripción con pagos pendientes.
  - Los pagos deben procesarse de manera segura y reflejarse en el estado de la suscripción correspondiente.
  - Los pagos fallidos deben ser gestionados adecuadamente para evitar interrupciones en el servicio.
  - Las facturas deben generarse automáticamente después de cada pago exitoso.
  - La información del cliente, como su correo electrónico, debe estar siempre actualizada en Stripe.

#### 4.2.1.2. Interface Layer
En esta capa se presentan las clases que permiten la comunicación entre la capa de dominio y la capa de aplicación, manejando las solicitudes de los usuarios y devolviendo las respuestas adecuadas. Para el contexto de Subscription & Payments, se han identificado los siguientes controladores:

- CustomerController: expone las operaciones relacionadas con los clientes de la aplicación. Permite la creación, actualización y consulta de los clientes, así como la gestión de su relación con Stripe. Al crear un cliente, se genera un identificador (stripeCustomerId) que es guardado en la entidad local y se sincroniza con el sistema de Stripe.
- 
  ![alt text](src/images/customer-controller.png)

- SubscriptionController: gestiona las operaciones relacionadas con las suscripciones de los clientes. Este controlador permite crear nuevas suscripciones, actualizar el estado de las mismas y cancelarlas, todo esto interactuando con los servicios de Stripe.
- 
  ![alt text](src/images/subscription-controller.png)

- PlanController: gestiona los planes de suscripción disponibles en la aplicación. Los usuarios pueden consultar los planes disponibles, sus características y precios.
- 
  ![alt text](src/images/plan-controller.png)

#### 4.2.1.3. Application Layer
Esta capa, para el Subscription and Payment Context, se definen los flujos de negocio a través de clases de tipo Command Handlers y Event Handlers, asegurando que los procesos de suscripción, pago y gestión de eventos externos (como los webhooks de Stripe) se manejen correctamente. Estos handlers permiten que el sistema sea reactivo, eficiente y mantenga la consistencia entre las operaciones internas y los eventos externos. A continuación, se presentan los handlers y eventos identificados para este contexto:

- Command Handlers:
  1. CreateSubscriptionCommandHandler: Maneja el proceso de creación de una nueva suscripción para un cliente. Este handler se encarga de validar los datos de entrada y crea la suscripción tanto en el sistema como en Stripe.

  ![alt text](src/images/createsubscription-ch.png)

  2. ProcessPaymentCommandHandler: Se encarga de guardar el pago procesado por Stripe en la base de datos y mantener la consistencia entre el estado del pago y la suscripción asociada.

  ![alt text](src/images/processpayment-ch.png)

  3. CancelSubscriptionCommandHandler: Gestiona la cancelación de una suscripción existente. Este handler verifica si la suscripción puede ser cancelada, actualiza su estado y notifica a Stripe para reflejar el cambio.

  ![alt text](src/images/cancelsubscription-ch.png)

- Event Handlers:
  1. StripeWebhookEventHandler: Maneja los eventos provenientes de Stripe a través de webhooks. Se asegura de procesar adecuadamente los eventos de facturación, pagos fallidos, renovaciones de suscripciones, etc.

  ![alt text](src/images/stripewebhook-eh.png)

  2. SubscriptionExpiredEventHandler: Reacciona cuando una suscripción ha llegado a su fecha de finalización sin ser renovada. Gestiona la lógica relacionada con la expiración, como la notificación al cliente y la desactivación de servicios vinculados.

  ![alt text](src/images/subscriptionexpired-eh.png)

  3. PaymentFailedEventHandler: Este handler reacciona a eventos de pagos fallidos, ya sea generados por el dominio o recibidos de Stripe. Se encarga de notificar al cliente, reintentar el pago y, si es necesario, cancelar la suscripción.

  ![alt text](src/images/paymentfailed-eh.png)

- Capabilities Cubiertos: 
  
  Las clases de la Application Layer están diseñadas para cubrir los siguientes capabilities del sistema:

	1.	Gestión de Suscripciones: A través de los Command Handlers como CreateSubscriptionCommandHandler y CancelSubscriptionCommandHandler, el sistema permite a los clientes gestionar sus suscripciones, incluyendo su creación, cancelación y renovación.
	2.	Procesamiento de Pagos: Mediante ProcessPaymentCommandHandler y event handlers como PaymentFailedEventHandler, el sistema registra los pagos, incluyendo la integración con Stripe y manejo de pagos fallidos.
	3.	Manejo de Eventos Externos (Stripe Webhooks): StripeWebhookEventHandler garantiza que el sistema reaccione correctamente a los eventos provenientes de Stripe, sincronizando los estados de suscripciones y pagos entre la plataforma y el sistema.
	4.	Manejo de Expiración de Suscripciones: SubscriptionExpiredEventHandler asegura que, cuando una suscripción expire, se tomen las acciones adecuadas, como notificar al cliente y desactivar servicios asociados.

#### 4.2.1.4. Infrastructure Layer
Esta capa es responsable de proporcionar la implementación de las operaciones que interactúan con recursos externos, como bases de datos, servicios de terceros (por ejemplo, Stripe), sistemas de mensajería y otros. En esta capa, también se implementan los Repositories definidos en la Domain Layer, que permiten la persistencia de las entidades del sistema. A continuación, se presentan las clases clave de esta capa, con una breve descripción de su función en el contexto del sistema:

1. StripePaymentGateway: Es la clase encargada de la integración con el sistema de pagos de Stripe. Implementa las operaciones necesarias para gestionar pagos, suscripciones y facturación a través de la API de Stripe.

![alt text](src/images/stripepaymentgateway.png)

2. NotificationService: Se encarga de enviar notificaciones a los usuarios, ya sea por correo electrónico, SMS o cualquier otro medio configurado. Es utilizada para notificar eventos importantes, como pagos fallidos, renovaciones de suscripción o vencimientos.

![alt text](src/images/notificationservice.png)

3. StripeWebhookService: Se encarga de procesar las notificaciones recibidas desde Stripe a través de webhooks. Esta clase recibe los eventos de Stripe y los transforma en eventos internos del dominio que los Event Handlers procesan.

![alt text](src/images/stripewebhookservice.png)

4. PaymentRepository: Esta clase maneja las operaciones de almacenamiento y recuperación de información relacionada con los pagos realizados por los clientes.

![alt text](src/images/payment-repo.png)

5. SubscriptionRepository: Esta clase se encarga de manejar las operaciones de persistencia de las suscripciones en la base de datos.

![alt text](src/images/subscription-repo.png)

6. CustomerRepository: Se encarga de gestionar la persistencia de la información de los clientes, incluyendo la sincronización con el sistema de Stripe.

![alt text](src/images/customer-repo.png)

#### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams
En el caso del Bounded Context Subscription & Payments, se ha identificado los siguientes componentes y sus interacciones:

![alt text](src/images/c4-component-bc-subscriptions.png)

#### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams

El diagrama UML del bounded context Subscription & Payments muestra las clases y sus relaciones en la capa de dominio. Las entidades principales, como Customer, Subscription, Payment e Invoice, se relacionan entre sí para representar la lógica de negocio del contexto. Además, se incluyen los Value Objects y Aggregates que encapsulan la información y la lógica de negocio relacionada con las suscripciones y pagos.

![alt text](src/images/class-diagram-subs.png)

##### 4.2.1.6.2. Bounded Context Database Design Diagram

El diseño de la base de datos para el contexto Subscription & Payments refleja la estructura de las entidades y sus relaciones. Cada tabla representa una entidad del dominio, con sus atributos y claves primarias y foráneas. La base de datos se ha diseñado para garantizar la integridad de los datos y soportar las operaciones de gestión de suscripciones y pagos.

![alt text](src/images/database-design-subs.png)

### 4.2.2. Bounded Context: Device
#### 4.2.2.1 Domain Layer
- **Entidades de dominio**:
  - **Device**: Representa un dispositivo IoT instalado en el inmueble, incluyendo sus características y estado.
  - **Installation**: Representa la instalación de un dispositivo en un inmueble, incluyendo la fecha de instalación y el estado de la instalación.
  - **Property**: Representa la propiedad (inmueble) donde los dispositivos están instalados, incluyendo detalles sobre la ubicación y características.

- **Objetos de valor**:
  - **DeviceConfiguration**: Contiene la configuración específica de cada dispositivo, como el tipo de dispositivo, configuraciones de red y parámetros operativos.
  - **InstallationDetails**: Información sobre la instalación del dispositivo, como la ubicación exacta y el método de instalación.

- **Repositorios**:
  - **DeviceRepository**: Maneja la persistencia de los dispositivos.
  - **InstallationRepository**: Maneja la persistencia de las instalaciones de dispositivos.
  - **PropertyRepository**: Maneja la persistencia de las propiedades donde se instalan los dispositivos.

#### 4.2.2.2 Interface Layer
- **DeviceController**: Gestiona la configuración y visualización de dispositivos IoT. Permite a los usuarios ver, agregar y actualizar la información de los dispositivos instalados, así como revisar el estado y configuraciones de cada dispositivo.

- **InstallationController**: Maneja la gestión de la instalación de dispositivos. Permite a los usuarios iniciar nuevas instalaciones, actualizar el estado de las instalaciones y visualizar el historial de instalaciones.

- **PropertyController**: Gestiona la información de las propiedades donde los dispositivos están instalados. Permite a los usuarios ver detalles sobre las propiedades y asociar dispositivos con propiedades específicas.

#### 4.2.2.3. Application Layer
- **Command Handlers**:
  - **RegisterDeviceCommandHandler**: Procesa la solicitud para registrar un nuevo dispositivo IoT en el sistema. Este handler maneja la creación de registros para nuevos dispositivos y su configuración inicial.
  - **UpdateDeviceConfigurationCommandHandler**: Maneja las actualizaciones en la configuración de un dispositivo existente.
  - **InstallDeviceCommandHandler**: Procesa la solicitud para instalar un dispositivo en una propiedad. Maneja la asociación del dispositivo con la propiedad y actualiza el estado de la instalación.
  - **UninstallDeviceCommandHandler**: Maneja la solicitud para desinstalar un dispositivo, actualizando el estado del dispositivo y la propiedad asociada.

- **Event Handlers**:
  - **DeviceRegisteredEventHandler**: Responde a eventos que confirman la creación y registro exitoso de un dispositivo. Actualiza el estado del dispositivo en la base de datos y emite eventos relacionados.
  - **DeviceConfigurationUpdatedEventHandler**: Maneja eventos que indican que la configuración de un dispositivo ha sido actualizada. Actualiza la base de datos y notifica a los usuarios correspondientes.
  - **DeviceInstalledEventHandler**: Maneja eventos de instalación exitosa de un dispositivo. Actualiza el estado de la instalación y emite notificaciones.
  - **DeviceUninstalledEventHandler**: Responde a eventos que indican que un dispositivo ha sido desinstalado. Actualiza el estado en la base de datos y emite notificaciones relacionadas.

#### 4.2.2.5. Bounded Context Software Architecture Component Level Diagrams

Este diagrama proporciona una vista de la estructura de la arquitectura y cómo los diferentes componentes interactúan dentro del aggregate Devices.

![alt text](/src/images/c4-devices.png)

#### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams
El diagrama UML del bounded context "Devices" ilustra las clases Property, Devices, Installation y DeviceConfigurations con sus respectivos atributos y métodos. Las clases también contienen métodos para crear, actualizar, validar y eliminar instancias. 

![alt text](/src/images/devices-diagram.png)
#### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams
Este diagrama de base de datos representa las tablas y las relaciones dentro del bounded context "Devices". Se define la entidad devices, que almacena información sobre ek tipo y la descripción del dispositivo de seguridad.La entidad devices_type almacena el tipo de dispositivo.

![alt text](/src/images/devices-db.png)

<!-- TODO -->
### 4.2.3. Bounded Context: Area
#### 4.2.3.1. Domain Layer
- Entities:
  - Area: Representa un área específica en la que se colocan los dispositivos.
    - Atributos: id, name, icon, color.
  - Property: Representa una propiedad que puede tener múltiples áreas.
    - Atributos: id, name, image_url, address.

- Value Objects:
  - AreaId: Identificador único de un área.
  - PropertyId: Identificador único de una propiedad.

- Aggregates:
  - AreaAggregate: Agregado raíz que encapsula las operaciones relacionadas con las áreas, incluyendo la creación, actualización y eliminación de áreas.
  - PropertyAggregate: Agregado raíz que encapsula las operaciones relacionadas con las propiedades, incluyendo la asociación con áreas.

- Domain Services:
  - AreaService: Define las operaciones de negocio relacionadas con las áreas, como la creación, actualización y eliminación de áreas.
  - PropertyService: Define las operaciones de negocio relacionadas con las propiedades, como la gestión de áreas asociadas.

- Repositories:
  - AreaRepository: Interfaz que define las operaciones de persistencia relacionadas con las áreas.
  - PropertyRepository: Interfaz que define las operaciones de persistencia relacionadas con las propiedades.

#### 4.2.3.2. Interface Layer
- API Endpoints:
  - POST /areas: Crea una nueva área.
  - PUT /areas/{areaId}: Actualiza una área existente.
  - DELETE /areas/{areaId}: Elimina una área.
  - GET /areas/{areaId}: Obtiene los detalles de una área.
  - POST /properties: Crea una nueva propiedad.
  - PUT /properties/{propertyId}: Actualiza una propiedad existente.
  - DELETE /properties/{propertyId}: Elimina una propiedad.
  - GET /properties/{propertyId}: Obtiene los detalles de una propiedad.

- DTOs:
  - AreaDTO: Representa los datos de un área para ser enviados o recibidos a través de la API.
  - PropertyDTO: Representa los datos de una propiedad para ser enviados o recibidos a través de la API.

- Controllers:
  - AreaController: Controlador que gestiona las operaciones relacionadas con las áreas, como la creación, actualización y eliminación de áreas.
  - PropertyController: Controlador que gestiona las operaciones relacionadas con las propiedades, como la creación, actualización y eliminación de propiedades.

#### 4.2.3.3. Application Layer
- Application Services:
  - AreaApplicationService: Servicio de aplicación que coordina las operaciones relacionadas con las áreas, como la creación, actualización y eliminación de áreas.
  - PropertyApplicationService: Servicio de aplicación que gestiona las operaciones relacionadas con las propiedades, como la creación, actualización y eliminación de propiedades.

- Commands/Queries:
  - CreateAreaCommand: Comando para crear una nueva área.
  - UpdateAreaCommand: Comando para actualizar una área existente.
  - DeleteAreaCommand: Comando para eliminar una área.
  - GetAreaQuery: Consulta para obtener los detalles de una área.
  - CreatePropertyCommand: Comando para crear una nueva propiedad.
  - UpdatePropertyCommand: Comando para actualizar una propiedad existente.
  - DeletePropertyCommand: Comando para eliminar una propiedad.
  - GetPropertyQuery: Consulta para obtener los detalles de una propiedad.

- Events:
  - AreaCreatedEvent: Evento que se dispara cuando se crea una nueva área.
  - AreaUpdatedEvent: Evento que se dispara cuando se actualiza una área.
  - AreaDeletedEvent: Evento que se dispara cuando se elimina una área.
  - PropertyCreatedEvent: Evento que se dispara cuando se crea una nueva propiedad.
  - PropertyUpdatedEvent: Evento que se dispara cuando se actualiza una propiedad.
  - PropertyDeletedEvent: Evento que se dispara cuando se elimina una propiedad.

#### 4.2.3.4. Infrastructure Layer
- Repositories Implementations:
  - AreaRepositoryImpl: Implementación concreta del repositorio de áreas que se encarga de la persistencia de las áreas en la base de datos.
  - PropertyRepositoryImpl: Implementación concreta del repositorio de propiedades que se encarga de la persistencia de las propiedades en la base de datos.

- External Services:
  - En este contexto, no se han identificado servicios externos específicos para las áreas y propiedades, pero podrían incluir servicios de almacenamiento de imágenes o integraciones con sistemas de mapeo si se requieren en el futuro.

#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams
Este diagrama proporciona una vista de la estructura de la arquitectura y cómo los diferentes componentes interactúan dentro del aggregate Areas.
![Bounded Context C4 Areas](src/images/bc-c4-areas.jpeg)

#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams
#### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams
El diagrama UML del bounded context "Areas" ilustra las clases Area y Property con sus respectivos atributos y métodos. En este contexto, Area representa las distintas áreas dentro de una propiedad, mientras que Property representa el conjunto completo de estas áreas. Cada clase tiene atributos básicos como identificadores, nombres, y otras características relevantes. Las clases también contienen métodos para crear, actualizar y eliminar instancias. La relación entre Property y Area está representada mediante una composición, donde una propiedad contiene múltiples áreas, lo que refuerza la relación de uno a muchos entre ambas clases.

![Bounded Context UML Areas](src/images/bc-uml-areas.png)

#### 4.2.3.6.2. Bounded Context Database Design Diagram
Este diagrama de base de datos representa las tablas y las relaciones dentro del bounded context "Areas". Se define la tabla area, que almacena información sobre las áreas específicas donde se colocan dispositivos de seguridad, y la tabla property, que representa una propiedad, la cual puede contener múltiples áreas. La relación entre estas dos entidades es de uno a muchos, donde una propiedad puede tener varias áreas asociadas. Los atributos principales incluyen identificadores únicos para cada entidad, nombres descriptivos, y detalles adicionales como iconos y colores para las áreas, y direcciones para las propiedades.

![Bounded Context Database Areas](src/images/bc-db-areas.jpg)

### 4.2.4. Bounded Context: User context
El User Context abarca los procesos y funciones relacionados con la gestión del usuario y el rol que desempeña cada uno dentro de nuestro sistema. Aqui podemos manejar la creación, modificación o eliminación del usuario de nuestro sistema, asimismo podemos gestionar la asiganción de roles.

1. Clase User
   * Propósito: La clase User representa a los usuarios del sistema. Un usuario puede tener un rol asignado
   * Atributos:
     * `id: string`: Identificador único del usuario
     * `firstname: string`: Nombre del usuario
     * `lastname: string`: Apellido del usuario
     * `email: string`: Correo electrónico del usuario
     * `password: string`: Contraseña cifrada del usuario
     * `phone: number`: Número Telefónico del usuario
     * `dni: char(8)`: Documento Nacional de Identidad del usuario
     * `rols_id: int`: Identificador del rol asignado al usuario
   * Métodos:
     * `getUserDetails(): void` - Retorna los detalles importantes del usuario para el inicio de sesión.
     * `registerUser(): void` - Registro del usuario en el sistema
   * Relaciones:
     * `n...1` con Roles ya que un rol puede tener varios usuarios

2. Clase Roles
   * Propósito: Representa los distintos roles que los usuarios puedan tener dentor del sistema para que determine los permisos y acciones que puedan realizar.
   * Atributos:
     * `id: string`: Identificador único del rol
     * `type: string`: Tipo del rol que podría desempeñar el usuario.
   * Relaciones: 
     * `1...n` con User dado que un rol puede tener varios usuario.

#### 4.2.4.1. Domain Layer
En la capa de dominio encontramos nuestras clases centrales como núcleo de nuestro sistema y las reglas de negocio que incluyen lo siguiente:

* Entities:
  * User: Representa a un usuario del sistema y debe de ser único.
    * Atributos: id, firstname, lastname, email, password,phone, dni
  * Role: Representa el rol que desempeña el usuario dentro de la aplicacion.
    * Atributos: id, type.

* Value Objects:
  * UserId: Identificador único de cada usuario
  * RoleId: Identificador único de cada rol asignado a un usuario
  * Password: Objeto de valor para manejar contraseñas seguras y encriptadas.
  * Email: Objeto de valor para manejar correos únicos por cada usuario.
  
* Aggregates: 
  * UserAggregate: Es un agregado que incluye la entidad de usuario y los roles relacionados a ella. Además encapsula a las reglas y lógica de negocio.

* Domain Services: 
  * AuthenticationSerivce: Puede ser incluido un servicio de dominio encargado de la autenticación del usuario
  
* Repositories: 
  * UserRepository: Define los métodos para almacenar, modificar, eliminar y recuperar información de los usuarios en la base de datos
  * RoleRepository: Define los métofdos para gestionar la persistencia de roles.

#### 4.2.4.2. Interface Layer
Aquí manejamos las interacciones y solicitudes entre el sistema y los usuarios y consigo devolviendo respuestas optimas. Para el Bounded Context de User tenemos lo siguiente:

* Controllers:
  * UserController: Se expone las operaciones relacionadas con el usuario como la creción, actualización, consulta y eliminación del usuario. Al crearse un usuario, este a su vez se le asigna un rol.
  * RoleController: Gestiona las peticiones relacionadas con la administración de roles, como la creación de nuevos roles o la modificación de roles existentes.
  

#### 4.2.4.3. Application Layer
Para esta capa definimos los flujos de negocios a traves de clases de tipo Command  Handlers y Event Handlers, asegurando asi el manejor de las clases correctamente.

* Command Handlers:
  * CreateUserCommandHandler: Maneja la lógica de creación de nuevos usuarios, asegurándose que cada uno cumpla con todas las reglas de negocio, como validar el correo único y el cifrado de contraseñas
  * AssignRoleToUserCommandHandler: Gestiona la asiganción de roles a los usuarios
* Event Handlers:
  * UserRegisteredEventHandler: Este handler puede enviar una notificación cuando un nuevo usuario es registrado existosamente en el sistema

#### 4.2.4.4. Infrastructure Layer
En esta capa veremos las relaciones de nuestreas clases con las conexiones a los servicios externos como las bases de datos

**Repositories:**
  * UserRepository: Implementacion de la interfaz de repositorio para acceder a la base de datos que almacena la información de los usuarios.
  * RoleRepository: Implementacion de la interfaz de repositorio para gestionar la persistencia de roles a travez de la base de datos.

**External Service:**
* MessageService: Servicio externo que se utiliza para enviar notificaciones a los usuarios en caso haya cambios en la aplicación móvil o una gestión de alarmas.

#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams
En esta parte presentaremos el Diagrama de componentes en el modelo C4, mostraremos las descomposicion del container en componentes y sus interacciones

#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams
##### 4.2.4.6.2. Bounded Context Database Design Diagram
En el diagrama de base de datos de usuario podemos ver la relacion existente de las tablas dentro del bounded context "User". Aqui definimos la tabla usuario, en el cual almacenamos información importante del usuario para que pueda registrarse en la aplicacion que a su vez esta relacionada con un rol de usuario el cual asigna los permisos al sistema dependiendo el rol que desempeñen dentro de nuestra aplicación dando conocer asi que un rol lo puede desempeñar varios usuarios pero un usuario tiene un unico rol. Los atributos los cuales manejamos incluyen identificadores unicos para cada entidad asi como detalles principales que debemos tener para la aplicacion. 

![Bounded Context Database User](src/images/database-user.png)

### 4.2.5. Bounded Context: Events context
El Event Context abarca los procesos y funciones relacionados con la gestión de los eventos y/o sucesos que puedan ocurrir a traves de nuestro sistema de alarma. Podemos manejar la creación o modificación de las alarmas según el usuario lo crea conveniente.

1. Clase Events
   * Propósito: La clase Events representa a los eventos que puedan suceder por las alarmas puestas en nuestros.
   * Atributos:
     * `id: string`: Identificador único del evento
     * `title: string`: Título del suceso 
     * `description: string`: Descripción del evento sucedido
     * `timestamp: string`: Hora en el cual sucedio el evento
   * Métodos:
     * `getEventDetails(): void` - Retorna los detalles importantes del evento para el registro correspondiente.
     * `registerEvent(): void` - Registro de un nuevo evento en el sistema
   * Relaciones:
     * `1...1` con Tipo de Evento ya que un tipo de evento puede tener un evento que sucedió

2. Clase Events_type
   * Propósito: Representa los distintos roles que los usuarios puedan tener dentor del sistema para que determine los permisos y acciones que puedan realizar.
   * Atributos:
     * `id: string`: Identificador único del rol
     * `type: string`: Tipo del rol que podría desempeñar el usuario.
   * Relaciones: 
     * `1...1` con Type dado que un evento puede tener un tipo de evento.

#### 4.2.4.1. Domain Layer
En la capa de dominio encontramos nuestras clases centrales como núcleo de nuestro sistema y las reglas de negocio que incluyen lo siguiente:

* Entities:
  * Events: Representa a un evento que pudo ocurrir y capto nuestro sistema de seguridad.
    * Atributos: id, title, description, timestamp.
  * EventsType: Representa el tipo de evento que desempeña el evento dentro de la aplicacion.
    * Atributos: id, type.

* Value Objects:
  * EventId: Identificador único de cada usuario
  * TypeEventId: Identificador único de cada rol asignado a un usuario.
  
* Aggregates: 
  * EventsAggregate: Es un agregado que incluye la entidad de usuario y los roles relacionados a ella. Además encapsula a las reglas y lógica de negocio.

* Domain Services: 
  * MessageService: Puede ser incluido un servicio de dominio encargado de la notificación al usuario de un evento ocurrido.
  
* Repositories: 
  * EventRepository: Define los métodos para almacenar, modificar, eliminar y recuperar información de los usuarios en la base de datos
  * EventTypeRepository: Define los métofdos para gestionar la persistencia de roles.

#### 4.2.4.2. Interface Layer
Aquí manejamos las interacciones y solicitudes entre el sistema y los usuarios y consigo devolviendo respuestas optimas. Para el Bounded Context de Event tenemos lo siguiente:

* Controllers:
  * EventController: Se expone las operaciones relacionadas con el evento como la creción, actualización y consulta del evento. Al crearse un evento, este a su vez.
  * EventTypeController: Gestiona las peticiones relacionadas con la administración de tipos de eventos, como la creación de nuevos eventos o la modificación de eventos existentes.

#### 4.2.4.3. Application Layer
Para esta capa definimos los flujos de negocios a traves de clases de tipo Command  Handlers y Event Handlers, asegurando asi el manejor de las clases correctamente.

* Command Handlers:
  * CreateEventCommandHandler: Maneja la lógica de creación de nuevos eventos, asegurándose que cada uno cumpla con todas las reglas de negocio.
  * AssignTypeToEventCommandHandler: Gestiona la asiganción de tipos de eventos a los eventos
* Event Handlers:
  * EventRegisteredEventHandler: Este handler puede enviar una notificación cuando un nuevo evento esta sucediendo.

#### 4.2.4.4. Infrastructure Layer
En esta capa veremos las relaciones de nuestreas clases con las conexiones a los servicios externos como las bases de datos

**Repositories:**
  * EventRepository: Implementacion de la interfaz de repositorio para acceder a la base de datos que almacena la información de los eventos.
  * EvenTypeRepository: Implementacion de la interfaz de repositorio para gestionar el tipo de evento a travez de la base de datos.

**External Service:**
* MessageService: Servicio externo que se utiliza para enviar notificaciones a los usuarios en caso haya cambios en la gestión de alarmas.

#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams
En esta parte presentaremos el Diagrama de componentes en el modelo C4, mostraremos las descomposicion del container en componentes y sus interacciones

#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams
##### 4.2.4.6.2. Bounded Context Database Design Diagram
En el diagrama de base de datos de usuario podemos ver la relacion existente de las tablas dentro del bounded context "Event". Aqui definimos la tabla event, en el cual almacenamos información importante del evento o suceso que suceda en el momento que pueda activarse una alarma, además esta esta relacionado con un tipo de evento para una mejor gestión al momento de registrar el evento ocurrido. Los atributos los cuales manejamos incluyen identificadores unicos para cada entidad asi como detalles principales que debemos tener para la aplicacion. 

![Bounded Context Event](src/images/database%20event.png)
=======
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

Para esta sección, acordamos como equipo ciertos diseños, fuentes, colores, etc. para estar de acorde en todos nuestros diseños y en el momento de programación.

### 5.1.1. General Style Guidelines

Para esta parte mostraremos nuestra guía organizada de los estilos y herramientas que se estarán utilizando para la contrucción del diseño.

**Brand Overview**

La seguridad es una preocupación creciente en Lima, Perú, debido al aumento de robos e intrusiones en propiedades residenciales y comerciales. Los propietarios buscan soluciones efectivas que no solo sean accesibles, sino también confiables y tecnológicamente avanzadas para proteger lo que más valoran. Sin embargo, las soluciones de seguridad tradicionales tienden a ser costosas y, en muchos casos, ineficientes en ofrecer respuestas rápidas o integrarse con la tecnología moderna.

Nuestra solución, FalconShield, responde a esta necesidad crítica al ofrecer un ecosistema de seguridad IoT (Internet de las Cosas) que incluye sensores avanzados, cámaras inteligentes y sistemas de alarmas, todos integrados en una plataforma centralizada y fácil de usar. Este producto no solo permite monitorear y controlar el estado de seguridad en tiempo real, sino que también se asocia con empresas de seguridad para proporcionar una respuesta rápida y coordinada en caso de emergencias. VerySafe, nuestra empresa, se compromete a garantizar que la seguridad de nuestros usuarios sea accesible, eficaz y moderna.

**Brand Name**

El nombre de nuestra solución es FalconShield. Este surgió de la combinación de dos palabras que simbolizan nuestros valores fundamentales. Falcon, que representa agudeza y vigilancia, alude a la capacidad de nuestro sistema para detectar intrusiones y amenazas de manera precisa y rápida. Shield, que significa escudo, refuerza el concepto de protección y defensa contra cualquier peligro que pueda afectar las propiedades de nuestros usuarios.

Elegimos el nombre en inglés para que sea comercialmente atractivo a nivel global y fácil de recordar en el mercado local. Este enfoque hace que el producto sea accesible y entendible no solo en Perú, sino también para una posible expansión en el futuro. VerySafe, el nombre de nuestra empresa, refleja nuestro compromiso de brindar soluciones que vayan más allá de las expectativas, asegurando una protección "muy segura" para todos nuestros clientes.

A continuación, presentaremos nuestro logo: 

![logo](src/images/logo1.jpg)

**Typography**

La tipografía debe ser clara y fácilmente legible, reflejando profesionalismo y modernidad. Aquí algunas recomendaciones:

* **Fuente primaria:** Lato o Open Sans son excelentes opciones para reflejar tecnología avanzada y claridad. Son fuentes sans-serif modernas y versátiles.

![lato](src/images/lato.png)
![open sans](src/images/open%20sans.png)

* **Jerarquía de texto:**
* 
  * **Títulos y encabezados:** Deben estar en negrita y ser grandes para capturar la atención. Tamaños sugeridos: 24px para el encabezado principal, 20px para subtítulos.
  * **Cuerpo del texto:** Para mejorar la legibilidad en dispositivos móviles y de escritorio, el tamaño sugerido es entre 16px-18px.
Botones y CTA (Call to Action): El texto debe ser claro y conciso, con tamaños de entre 14px-16px.
    ![tipografia](src/images/Typpgraphy.png)


**Colors**

Los colores juegan un papel clave en el diseño de VerySafe y FalconShield, y deben reflejar seguridad, confianza y tecnología. Basado en el análisis, tenemos estos colores

**Color Primario : Verde**

El verde es el color primario de nuestra marca, seleccionado para reflejar varios valores clave:

* **Seguridad y protección:** El verde es un color que transmite estabilidad y confianza, características fundamentales para una marca de seguridad.
* **Tecnología avanzada:** También representa crecimiento y evolución, lo que refuerza el enfoque innovador de FalconShield en la utilización de tecnología IoT avanzada.
* **Sostenibilidad y modernidad:** El verde es un color que conecta con la idea de un futuro más seguro y sostenible, lo que encaja con nuestra visión de integrar soluciones que sean accesibles para todos.

![src](src/images/verde.jpg)

**Color Secundario: Azul Marino**

El azul marino es el color secundario de la marca, elegido por sus asociaciones con profesionalismo, tecnología avanzada y tranquilidad. El azul marino complementa al verde oscuro y agrega una capa de sofisticación y profundidad visual. Es ideal para utilizar en elementos como los fondos de secciones, textos secundarios y detalles gráficos.

![azul](src/images/azul.jpg)

**Color de estado: Error - Rojo**

Utilizamos el color rojo ya que siempre han estado como el error de algún proceso. Así que usaremos este color en caso el usuario realice una actividad errónea

![rojo](src/images/rojo.jpg)

**Colores Neutros: Gris Claro y Blanco**

Para equilibrar los colores primarios y secundarios, utilizamos el gris claro y el blanco como colores neutros. Estos colores ayudan a proporcionar claridad y simplicidad, lo que es esencial en una plataforma de seguridad donde la información debe ser clara y directa.

![gris](src/images/gris.jpg)

**Spacing**

El espaciado es crucial para mejorar la experiencia del usuario y mantener un diseño limpio y fácil de navegar.

* **Margen y relleno:** Mantén un margen consistente entre secciones principales (al menos 80px en desktop y 40px en móvil) para que el contenido no se vea apretado. Esto facilita la escaneabilidad de la página.
* **Espaciado entre elementos:** Usa un espaciado generoso entre los elementos de cada sección, por ejemplo, entre un título y un bloque de texto (al menos 20px en desktop, 15px en móvil) y entre tarjetas o bloques de información como los planes de suscripción.
  
![spacing](src/images/spaccing.png)

**Tono de Comunicación y Lenguaje**
Dado que el producto se dirige tanto a usuarios residenciales como a empresas de seguridad, el tono debe ser serio, profesional, y confiable, pero también accesible. Aquí te dejo una guía del tono:

* **Tono General:**
    * Serio y Formal, pero no distante. Los usuarios deben sentir que están en buenas manos, y la comunicación debe transmitir autoridad en seguridad, pero con un enfoque amigable y fácil de entender.
  
* **Aplicación del Tono:**
  * Botones y llamadas a la acción (CTA): Usa verbos claros y directos, como “Proteger mi hogar”, “Descargar App”, o “Ver más”.
  * Mensajes de bienvenida y testimonios: Puedes ser un poco más informal y cercano para crear un vínculo con el usuario. Por ejemplo: “Disfruta de la tranquilidad de saber que FalconShield cuida lo que más valoras.”
  * Instrucciones y mensajes operacionales: El tono debe ser respetuoso y profesional, evitando la jerga técnica innecesaria.

**Referencias y Principios de Diseño**
Las decisiones de diseño se basan en los principios de Diseño Responsivo y Diseño Inclusivo, asegurando que el contenido sea accesible en cualquier dispositivo y para usuarios con diferentes capacidades visuales. El uso de colores contrastantes, tipografías legibles y espaciados amplios contribuye a una experiencia de usuario óptima.

* Diseño Responsivo: El contenido debe ajustarse correctamente a pantallas de diferentes tamaños, asegurando que las columnas de soluciones y planes se apilen en dispositivos móviles.
* Accesibilidad: Aplicar una buena relación de contraste entre los colores del texto y el fondo. Añadir textos alternativos a las imágenes para aquellos que usen lectores de pantalla.

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

A continuación, el equipo mostrará el sistema de etiquetado que otorgará una descripción breve y clara de la información brindada por nuestra plataforma de seguridad IoT, tanto para la Landing Page como para las interfaces web y móvil.

### **Landing Page**

Presentamos los encabezados con los que contará esta página:

- **Inicio/Home**: Sección preseleccionada por defecto que brindará una visión general del sistema de seguridad IoT y sus principales características, incluyendo cámaras, sensores y alarmas.
- **Conócenos/About Us**: Sección que permitirá a los usuarios conocer más sobre la empresa, incluyendo nuestra misión, visión, valores y equipo.
- **Servicios/Services**: Sección que muestra los servicios disponibles, tales como monitoreo de cámaras, control de sensores, y gestión de alarmas, con detalles sobre los beneficios de cada uno.
- **Planes/Plans**: Sección donde se presentarán los distintos planes de servicio (Básico, Premium, Gold) con sus respectivas características y precios.
- **Contáctanos/Contact Us**: Sección donde se muestran los canales de comunicación para que los usuarios puedan contactarse con el equipo de soporte o realizar consultas.

### **Aplicación Web y Móvil**

Presentamos las etiquetas que se utilizarán en las interfaces web y móvil para que los usuarios puedan navegar fácilmente entre las funciones y características del sistema de seguridad IoT.

#### **Para propietarios de inmuebles:**

- **Inicio/Home**: Pantalla principal donde se muestra un resumen general del estado de seguridad de la propiedad, incluyendo alertas recientes, cámaras activas y el estado de los sensores.
- **Cámaras/Cameras**: Pantalla que permite a los usuarios ver la transmisión en vivo de las cámaras de seguridad, revisar grabaciones pasadas y gestionar la configuración de las cámaras.
- **Sensores/Sensors**: Pantalla que muestra el estado de los sensores instalados (como sensores de movimiento, de apertura de puertas, etc.) y el historial de activaciones.
- **Alarmas/Alarms**: Pantalla para gestionar el sistema de alarmas, incluyendo activar o desactivar las alarmas, y ver el historial de activaciones.
- **Historial/History**: Sección donde el usuario puede revisar el historial de eventos del sistema, como la activación de alarmas, movimientos detectados por los sensores, o cualquier evento relacionado con las cámaras.
- **Configuración/Settings**: Sección donde los usuarios pueden ajustar las configuraciones del sistema, agregar nuevos dispositivos, personalizar notificaciones y actualizar la información de la cuenta.

#### **Para empresas de seguridad:**

- **Panel de Control/Dashboard**: Pantalla que presenta un resumen de las propiedades que la empresa monitorea, mostrando las alertas más recientes, cámaras activas y sensores conectados.
- **Cámaras/Cameras**: Pantalla que permite acceder a la transmisión en vivo de las cámaras instaladas en las propiedades de los clientes, así como gestionar el almacenamiento de video y programar grabaciones.
- **Sensores/Sensors**: Pantalla que muestra el estado de los sensores instalados en todas las propiedades que monitorea la empresa, con la capacidad de activar o desactivar sensores específicos de manera remota.
- **Alarmas/Alarms**: Sección para controlar y gestionar las alarmas de todas las propiedades monitoreadas. Se puede configurar la respuesta ante alertas y coordinar con los equipos de emergencia.
- **Configuración/Settings**: Página donde los administradores pueden agregar nuevos dispositivos, gestionar usuarios y permisos, así como ajustar las configuraciones del sistema y personalizar alertas.

### **IoT Devices**

Para los dispositivos IoT que forman parte del sistema de seguridad (cámaras, sensores, alarmas), utilizaremos etiquetas simples que representen claramente su función:

- **Estado/Status**: Muestra el estado del dispositivo (Activo/Inactivo) y su conexión a la red.
- **Alertas/Alerts**: Muestra cualquier alerta relacionada con el dispositivo, como fallos, detecciones de movimiento o intentos de sabotaje.
- **Configuración/Settings**: Opción para ajustar la configuración del dispositivo, como la sensibilidad del sensor o la calidad de grabación de la cámara.
- **Historial/History**: Registra los eventos recientes capturados por el dispositivo, como activaciones de sensores o grabaciones de video.


### 5.2.3. SEO Tags and Meta Tags

Presentaremos las etiquetas que identificarán y diferenciarán a nuestro sitio web. Asimismo para el app movil incluiremos el ASO.

**Landing Page:**
1. Title (Título):
   1. Title: FalconShield - Seguridad Avanzada para tu Hogar y Negocio
   
2. Meta Tags:
   1. Meta Description: 
    `<meta name="description" content="FalconShield ofrece soluciones de seguridad avanzada para hogares y negocios. Con monitoreo en tiempo real, sensores, cámaras y alarmas IoT, garantizamos la protección de lo que más valoras.">`
    2. Meta Keywords:
      `<meta name="keywords" content="seguridad IoT, cámaras de seguridad, alarmas, sensores, protección de propiedades, seguridad en tiempo real, FalconShield, seguridad para el hogar, VerySafe">`
    3. Meta Author:
      `<meta name="author" content="Equipo FalconShield">`

3. Open Graph Tags:
   1. Open Graph Title
      `<meta property="og:title" content="FalconShield - Protección Inteligente para tu Propiedad">`
    2. Open Graph Description
      `<meta property="og:description" content="Con FalconShield, monitorea y protege tu hogar o negocio desde cualquier lugar con tecnología IoT avanzada. Cámaras, alarmas y sensores inteligentes a tu disposición.">`
    3. Open Graph Image
        `<meta property="og:image" content="https://tusitio.com/imagen_falconshield.jpg">`
    4. Open Graph URL
      `<meta property="og:url" content="https://tusitio.com">`

**Web Application:**

1. Title (Título):
   1. Title: FalconShield App - Controla la Seguridad de tu Propiedad desde Cualquier Lugar

2. Meta Tags:
   1. Meta Description:
      `<meta name="description" content="Gestiona tu sistema de seguridad con la app FalconShield. Monitoreo en tiempo real, alertas instantáneas y control total de tus dispositivos IoT desde una plataforma intuitiva.">`
   2. Meta Keywords:
      `<meta name="keywords" content="app de seguridad, control de seguridad IoT, monitoreo de cámaras, control de alarmas, FalconShield app, seguridad en tiempo real, VerySafe">`
   3.  Meta Author:
      `<meta name="author" content="Gaby Nomberto, Equipo FalconShield">`

1. Open Graph Tags:
   1. Open Graph Title:
      `<meta property="og:title" content="FalconShield App - Monitorea tu Seguridad en Tiempo Real">`
   2. Open Graph Description:
      `<meta property="og:description" content="Con la app FalconShield, protege tu hogar o negocio. Recibe alertas y controla tus dispositivos de seguridad desde tu teléfono.">`
   3. Open Graph Image:
    `<meta property="og:image" content="https://tusitio.com/app_falconshield.jpg">`
   4. Open Graph URL:
    `<meta property="og:url" content="https://tusitio.com/app">`

**ASO (App Store Optimization) para Aplicaciones Móviles:**

1. App Title:
   1. FalconShield: Seguridad Inteligente en Tiempo Real
2. App Subtitle: 
   1. Protege tu hogar y negocio con monitoreo avanzado IoT

3. App Keywords:
   1. seguridad IoT, cámaras de seguridad, alarmas, sensores, monitoreo en tiempo real, protección de propiedades, FalconShield, seguridad inteligente, VerySafe

4. App Description:
   1. FalconShield es una solución de seguridad inteligente que te permite proteger tu hogar y negocio con tecnología IoT avanzada. Desde la app puedes monitorear en tiempo real, controlar tus cámaras, alarmas y sensores, y recibir alertas instantáneas ante cualquier amenaza. Con una interfaz fácil de usar, FalconShield te brinda la tranquilidad que necesitas. Descárgala ahora y asegúrate de que lo que más valoras esté siempre protegido.

5. App Store Screenshots and Media:
   1. Asegúrate de incluir capturas de pantalla que muestren la interfaz de usuario, la funcionalidad de monitoreo en tiempo real, el control de dispositivos IoT, y las alertas en acción. Estas imágenes deben reflejar la facilidad de uso y el nivel avanzado de tecnología ofrecido.


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

**WEB APPLICATION WIREFRAMES**

Se presenta el diseño visual y de interacción en formato de wireframes de nuestro producto digital.

Tenemos las pantallas generales que vendrían a ser el inicio sesión y registro.

![alt text](src/images/webFrame.png)
Iniciar sesión: En esta pantalla le mostramos al usuario los campos a llenar para ingresas con su cuenta en nuestra plataforma,

![alt text](src/images/webFrame1.png)

Registrar cuenta: En esta pantalla le mostramos al usuario los campos a llenar para crearse una cuenta en nuestra plataforma. Se usaron elementos como formas, textos y colores.

![alt text](src/images/webFrame2.png)

Mis dispositivos: En esta parte el usuario podra visualizar los dispositivos asociados a su cuenta.

![alt text](src/images/webFrame3.png)

Dashboard: En esta pantalla se mostrará un resumen de los eventos de todos los dispositivos de manera grafica.

![alt text](src/images/webFrame4.png)

Asistencia: En esta parte el usuario podra contarse para recibir una asistencia tecnica cuando lo requiera.

![alt text](src/images/webFrame5.png)

Eventos: En esta pantalla el usuario visualiza los eventos registrados por los dispositivos.

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
En esta sección se presentará los flujos de navegación entre pantallas de nuestra aplicación que visualizará el usuario y la interacción que tendrá con los elementos que presenta cada sección.

**WEB APPLICATION WIREFLOWS:**

| **User Goal:** Como usuario, deseo iniciar sesión con mi cuenta previamente creada para ingresar a la aplicación. | ![alt text](src/images/flow.png) |
| --- | --- |
| **User Goal:** Como usuario, quiero controlar mis dispositivos de seguridad desde la aplicación web para armar o desarmar la alarma.. |![alt text](src/images/flow1.png)  |
| --- | --- |
| **User Goal:** Como usuario, quiero un resumen de todos los eventos desde una única interfaz para gestionar los dispositivos de manera eficiente. | ![alt text](src/images/flow2.png) |
| --- | --- |
| **User Goal:** Como usuario, quiero tener una asistencia tecnica para solucionar problemas con el dispositivo. | ![alt text](src/images/flow3.png)|
| --- | --- |
| **User Goal:** Como usuario, quiero ver las eventos registrados por los dispositivos. | ![alt text](src/images/flow4.png) |
| --- | --- |



**MOBILE APPLICATION WIREFLOWS:**

Segmento objetivo Dueños de Inmuebles

| **User Goal:** Como usuario, deseo crear una cuenta para registrarme dentro de la aplicación. | ![wireflow-register](src/images/w-register.png) |
| --- | --- |
| **User Goal:** Como usuario, deseo iniciar sesión con mi cuenta previamente creada para ingresar a la aplicación. | ![wireflow-login](src/images/w-login.png) |
| --- | --- |
| **User Goal:** Como usuario, deseo ingresar a mi perfil para visualizar los datos que presento en la aplicación. | ![wireflow-profile](src/images/w-profile.png) |
| --- | --- |
| **User Goal:** Como usuario, deseo agregar un nuevo dispositivo para que pueda tener control de otra area de mi inmueble. | ![wireflow-add-device](src/images/w-add-device.png) |
| --- | --- |
| **User Goal:** Como usuario, deseo agregar una nueva area para tener control con los dispositivos IoT. | ![wireflow-add-area](src/images/w-create-area.png) |
| --- | --- |
| **User Goal:** Como usuario, deseo ver los detalles de los dispositivos para conocer más acerca de sus capacidades e instalaciones en el inmueble. | ![wireflow-add-area](src/images/w-device.png) |
| --- | --- |

### 5.4.2. Applications Mock-ups

**WEB APPLICATION MOCK-UP**
| Wireframe | Descripción |
|-- | -- |
|![alt text](src/images/mweb1.png)| **Inicio de Sesión:** En esta pantalla le mostamos al usuario los campos que tiene que llenar para que ingrese a nuestra aplicación. Utilizamos botones para que el usuario pueda diferenciar |
| ![alt text](src/images/mweb2.png) | **Registrar una cuenta:** En esta pantalla le mostamos al usuario los campos que tiene que llenar para poder crearse una cuenta. |
|

| Wireframe | Descripción |
| -- | -- |
| ![alt text](src/images/mweb3.png) | **Pantalla Home:** En esta pantalla le mostramos al usuario sus dispositivos, alertas, pendientes y problemas tiene. |
| ![alt text](src/images/mweb4.png) | **Pantalla Asisstence:** En esta pantalla le mostramos al usuario un medio para que pueda tener asistencia tecnica. |
| ![alt text](src/images/mweb5.png) | **Pantalla My Devices:** En esta pantalla le mostramos al usuario los dispositivos asociados a su cuenta. |
| ![alt text](src/images/mweb6.png) | **Pantalla My Devices:** En esta pantalla le mostramos al usuario los dispositivos asociados a su cuenta. |


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
| ![profile](src/images/MProfile.png) | **Perfil del usuario:** En esta pantalla el usuario podrá ver su información asi como otras funciones adicionales. |

Tenemos tambien nuestras pantallas para que el usuario agregue los dispositivos luego de ser instalados.

| Wireframe | Descripción |
| -- | -- |
| ![pantalla inicial de dispositivos](src/images/MADD%20DEVICE.png) | **Pantalla principal de los Dispositivos:** En esta pantalla le presentaremos al usuario los dispositivos adquiridos, asi como un boton que puede agregar luego de obtener más|
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

**MOBILE APPLICATION USERFLOWS:**
Enlace para una mejor visualización: https://overflow.io/s/3C8AFWFU

| -- | -- |
| -- | -- |
| **USER GOAL:** Como usuario deseo crear una cuenta | ![flow1](src/images/userflow2.jpg) |
| **USER GOAL:** Como usuario deseo iniciar sesión con mi cuenta previamente creada | ![flow2](src/images/userflow1.jpg) |
| **USER GOAL:** Como usuario deseo poder visualizar mi perfil | ![flow3](src/images/FLOW3.jpg) |
| **USER GOAL:** Como usuario, deseo agregar un nuevo dispositivo para que pueda tener control de otra area de mi inmueble. | ![flow4](src/images/flow4.jpg) |
| **USER GOAL:** Como usuario, deseo agregar una nueva area para tener control con los dispositivos IoT. | ![flow5](src/images/folw5.jpg) |


## 5.5. Applications Prototyping
=======
## 5.5. Applications Prototyping

# CAPÍTULO VI: PRODUCT IMPLEMENTATION, VALIDATION & DEPLOYMENT
## 6.1. Software Configuration Management
### 6.1.1. Software Development Environment Configuration
En esta sección se presenta la configuración del entorno de desarrollo de software utilizado por el equipo en el proyecto de IoT. A continuación, se detallan las herramientas seleccionadas, junto con sus descripciones y propósitos específicos, así como los enlaces para acceder a cada una de ellas. Estas herramientas son fundamentales para colaborar eficazmente en las diversas etapas del ciclo de vida de los productos digitales, incluyendo la gestión de proyectos, la gestión de requisitos, el diseño UX/UI, el desarrollo de software, las pruebas, el despliegue y la documentación.

| Herramienta | Descripción y propósito | Enlace |
|-------------|-------------------------|--------|
| UX Pressia         | Herramienta para crear mapas de experiencia del usuario, permitiendo visualizar y documentar la experiencia del usuario en un formato colaborativo. Se utilizará para desarrollar y comunicar la experiencia del usuario en las soluciones de IoT.                                         | [https://uxpressia.com](https://uxpressia.com)     |
| Miro               | Pizarra colaborativa en línea ideal para la lluvia de ideas y la planificación de proyectos. Se utilizará para la colaboración en la definición de requisitos y la creación de diagramas de flujo que guiarán el desarrollo del software.                                                            | [https://miro.com](https://miro.com)                 |
| Figma              | Herramienta de diseño de interfaces y prototipado colaborativo que permite trabajar juntos en tiempo real. Se utilizará para diseñar la interfaz de usuario (UI) y crear prototipos interactivos que se validarán con los usuarios finales.                                                        | [https://www.figma.com](https://www.figma.com)      |
| Overflow           | Herramienta de diagramación de flujos de usuario que permite crear recorridos visuales de las interacciones del usuario. Se utilizará para ilustrar cómo los usuarios interactuarán con la solución de IoT.                                                                                     | [https://overflow.io](https://overflow.io)          |
| Structurizr        | Herramienta para crear diagramas de arquitectura de software utilizando el lenguaje C4. Se utilizará para definir y comunicar la arquitectura de la solución IoT.                                                                                                                                              | [https://structurizr.com](https://structurizr.com)  |
| LucidChart         | Herramienta de diagramación en línea que permite crear diagramas de flujo y organigramas. Se utilizará para documentar visualmente los procesos y flujos de trabajo asociados con el desarrollo de la solución de IoT.                                                                           | [https://www.lucidchart.com](https://www.lucidchart.com) |
| Vertabelo          | Herramienta de diseño de bases de datos que permite crear y documentar esquemas de bases de datos. Se utilizará para el modelado de datos en el proyecto, asegurando que la estructura de la base de datos se alinee con los requisitos del sistema IoT.                                             | [https://www.vertabelo.com](https://www.vertabelo.com) |
| HTML5              | Lenguaje de marcado estándar para crear páginas web. Se utilizará para estructurar el contenido de las aplicaciones web del proyecto, asegurando una base sólida para la interfaz de usuario.                                                                                                            | No dispone |
| CSS3               | Hoja de estilo utilizada para diseñar la presentación de las aplicaciones web. Se utilizará para estilizar las interfaces de usuario y garantizar una experiencia visual atractiva y coherente.                                                                                                         | No dispone   |
| JavaScript         | Lenguaje de programación utilizado para desarrollar aplicaciones web interactivas. Se utilizará para implementar la lógica de negocio y las interacciones en la aplicación de IoT.                                                                                                         | No dispone   |
| Angular Framework   | Framework de desarrollo web para construir aplicaciones web de una sola página. Se utilizará para crear la interfaz del usuario y gestionar el estado de la aplicación IoT.                                                                                                                        | [https://angular.io](https://angular.io)          |
| Angular Material    | Biblioteca de componentes de UI para Angular que sigue las pautas de diseño de Material Design. Se utilizará para implementar componentes de interfaz de usuario coherentes y responsivos en la aplicación.                                                                                 | [https://material.angular.io](https://material.angular.io)  |
| TypeScript         | Superset de JavaScript que añade tipado estático. Se utilizará en el proyecto para mejorar la calidad del código y facilitar el desarrollo al proporcionar herramientas de desarrollo más robustas.                                                                                                   | [https://www.typescriptlang.org](https://www.typescriptlang.org)  |
| Trello             | Herramienta de gestión de proyectos que utiliza tableros para organizar tareas y proyectos. Se utilizará para gestionar el progreso del proyecto, asignar tareas y hacer seguimiento del trabajo del equipo.                                                                                             | [https://trello.com](https://trello.com)           |
| GIT                | Sistema de control de versiones distribuido que permite gestionar el código fuente del proyecto. Se utilizará para llevar un seguimiento de los cambios en el código y colaborar eficientemente entre los miembros del equipo.                                                                               | [https://git-scm.com](https://git-scm.com)         |
| GitHub             | Plataforma de desarrollo colaborativo que permite almacenar y gestionar repositorios de código usando Git. Se utilizará para alojar el código del proyecto y facilitar la colaboración entre los miembros del equipo.                                                                                   | [https://github.com](https://github.com)           |
| GitFlow            | Flujo de trabajo para Git que define un modelo de ramificación para gestionar el desarrollo. Se utilizará para organizar el trabajo en el proyecto, facilitando la integración de nuevas características y la gestión de lanzamientos.                                                                     | No dispone |


### 6.1.2. Source Code Management
### 6.1.3. Source Code Style Guide & Conventions
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

En esta sección especificaremos los pasos necesarios para realizar el despliegue de los productos digitales actuales de la solución. En la fase inicial, se despliega la Landing Page utilizando GitHub Pages y la aplicación Web en Netlify.

**Landing Page - Despliegue en GitHub Pages**

**Pasos para el Despliegue:**
1. Preparación del Repositorio:
   * Asegúrate de tener el repositorio de GitHub creado para la Landing Page.
   * Todos los archivos de la Landing Page (HTML, CSS, JavaScript y activos estáticos) deben estar en el directorio raíz o en una carpeta llamada docs.
  
2. Configurar GitHub Pages:
   * Ve a la sección de Settings en tu repositorio de GitHub.
   * Desplázate hasta GitHub Pages y selecciona la rama desde la que deseas desplegar tu página (generalmente main o master).
   * Si los archivos de tu Landing Page están en una carpeta específica, como docs, selecciona esa carpeta en el desplegable.

3. Publicación:
     * Guarda los cambios. GitHub Pages generará automáticamente una URL donde tu Landing Page estará disponible.
     * Verifica que la Landing Page sea accesible desde la URL proporcionada por GitHub Pages.

4. Actualizaciones:
   * Para hacer cambios en la Landing Page, realiza commits y push en el repositorio. GitHub Pages actualizará automáticamente el sitio con los cambios subidos.

**Web Application - Despliegue en Netlify**
**Pasos para el Despliegue:**

1. Preparación del Proyecto:
  * Asegúrate de que el proyecto esté correctamente configurado en tu entorno local.
  * Genera una versión de producción del proyecto con el comando adecuado (ejemplo: npm run build si usas React).

2. Conexión con Netlify:
   * Inicia sesión en tu cuenta de Netlify.
   * En el panel de control, selecciona "New site from Git".
   * Conecta tu repositorio de GitHub donde está alojada la Web Application.

3. Configuración de Despliegue:
   * Selecciona la rama que deseas desplegar (generalmente main o master).
   * Especifica el comando de construcción (por ejemplo, npm run build) y la carpeta donde se encuentra la salida (build o dist, dependiendo de tu configuración).
  
4. Publicación:
   * Netlify construirá y desplegará automáticamente la aplicación. Una vez que el despliegue esté completo, recibirás una URL para acceder a la aplicación.
   * Puedes personalizar la URL o usar un dominio personalizado en la configuración de Netlify.
5. Actualizaciones:
   * Para actualizar la Web Application, realiza cambios en el código, haz commits y push. Netlify detectará automáticamente los cambios y reconstruirá el sitio.

**Deployment Diagram (C4 Model)**
Para esta parte como es una etapa inicial contamos unicamente con nuestra Landing Page y nuestra primera versión de la aplicación Web

![deployment C4 1er sprint](src/images/deploymentc4.jpg)

## 6.2. Landing Page, Services & Applications Implementation
### 6.2.1. Sprint 1
#### 6.2.1.1. Sprint Planning 1
<table align="center"  border="1" width="90%" style="text-align:center;">
    <tr align="left">
        <td>
            <b>Sprint #</b>
        </td>
        <td>
            <b>Sprint 1</b>           
        </td>
    </tr>
    <tr align="left">
        <td colspan="2">
            <b>Sprint Planning Background</b>
        </td>
    </tr>
    <tr align="left">
        <td>
            <b>Date</b>
        </td>
        <td>
            20/09/24         
        </td>
    </tr>
       <tr align="left">
        <td>
            <b>Time</b>
        </td>
        <td>
            16:00         
        </td>
    </tr>
       <tr align="left">
        <td>
            <b>Location</b>
        </td>
        <td>
            Canal de voz en Discord      
        </td>
    </tr>
     </tr>
       <tr align="left">
        <td>
            <b>Prepared By</b>
        </td>
        <td>
            Integrantes del equipo  
        </td>
    </tr>
    </tr>
       <tr align="left">
        <td>
            <b>Attendess (to planning meeting)</b>
        </td>
        <td>
            - Gabriela Soledad Nomberto Ramos <br/>
            - Dennis Piero Quevedo Yucra <br/>
            - Max Dayson Sabino Arostegui  <br/>
            - Elvia Guadalupe Arteaga Cruz <br/>    
            - Jamutaq Piero Ortega Vélez <br/> 
        </td>
    </tr>
      </tr>
       <tr align="left">
        <td>
            <b>Sprint n - 1</b>
            <b>Review Summary</b>
        </td>
        <td>
            Se definieron las bases del proyecto con historias de usuario centradas en el desarrollo del Landing Page y la lógica de negocio de la plataforma. Se desplegó el landing page de forma exitosa.
        </td>
    </tr>
    <tr align="left">
        <td>
            <b>Sprint n - 1</b>
            <b>Retrospective Summary</b>
        </td>
        <td>
        Se logró cumplir con los objetivos planteados en el Sprint 1, sin embargo, se identificaron oportunidades de mejora en la comunicación y coordinación del equipo.
        </td>
    </tr>
     <tr align="left">
        <td colspan="2">
            <b>Sprint Goal & User Stories</b>
        </td>
    </tr>
      <tr align="left">
        <td>
            <b>Sprint 1 Velocity</b>
        </td>
        <td>
            -
        </td>
    </tr>
       <tr align="left">
        <td>
            <b>Sum of Story Points</b>
        </td>
        <td>
            -
        </td>
    </tr>
</table> 

#### 6.2.1.2. Sprint Backlog 1
En esta sección se especifican los detalles del Sprint Backlog, que es una lista de tareas que se han realizado para completar el Sprint.

<table align="center" border="1" width="90%" style="text-align:center">
    <tr>
       <td colspan="1"><b>Sprint #</b></td>
       <td colspan="7"><b>Sprint 1</b></td>
     </tr>
     <tr>
       <td colspan="2"><b>User Story</b></td>
       <td colspan="6"><b>Work-Item / Task</b></td>
     </tr>
     <tr>
       <td><b>Id</b></td>
       <td><b>Title</b></td>
       <td><b>Id</b></td>
       <td><b>Title</b></td>
       <td><b>Description</b></td>
       <td><b>Estimation(Hours)</b></td>
       <td><b>Assigned To</b></td>
       <td><b>Status(To-do/ In-Process/ To-Review/ Done)</b></td>
     </tr>
     <tr>
       <td rowspan="3">HU-01	</td>
       <td rowspan="3">Ver historial de eventos</td>
       <td>T01</td>
       <td>Creación del componente</td>
       <td>Crear y tener los archivos de código fuente necesarios  </td>
       <td>0.1</td>
       <td>Jamutaq O.</td>
       <td>Done</td>
    </tr>
    <tr>
       <td>T02</td>
       <td>Estructuración del componente (UI)</td>
       <td>Implementar el código HTML necesario</td>
       <td>2</td>
       <td>Jamutaq O.</td>
       <td>Done</td>
    </tr>
    <tr>
       <td>T03</td>
       <td>Estilado del componente</td>
       <td>Agregar los estilos correspondientes (desde una archivo SCSS o de Angular Material)</td>
       <td>2</td>
       <td>Jamutaq O.</td>
       <td>Done</td>
    </tr>
    <tr>
    </tr>
   <tr>
       <td rowspan="3">HU-03	</td>
       <td rowspan="3">Controlar dispositivos de seguridad</td>
       <td>T04</td>
       <td>Creación de la vista</td>
       <td>Crear el componente para la vista y configurar su ruta</td>
       <td>0.5</td>
       <td>Elvia A.</td>
       <td>Done</td>
    </tr>
    <tr>
       <td>T05</td>
       <td>Creación de subcomponentes necesarios</td>
       <td>Crear o importar componentes como cards, botones y entre otros</td>
       <td>2</td>
       <td>Elvia A.</td>
       <td>Done</td>
    </tr>
    <tr>
       <td>T06</td>
       <td>Creación de los servicios</td>
       <td>Crear los servicios necesarios como llamadas a APIs</td>
       <td>2</td>
       <td>Elvia A.</td>
       <td>Done</td>
    </tr>
    <tr>
       <td rowspan="3">HU-12</td>
       <td rowspan="3">Gestión de dispositivos conectados	</td>
       <td>T07</td>
       <td>Creación de la vista</td>
       <td>Crear el componente para la vista y sus rutas</td>
       <td>1</td>
       <td>Max D.</td>
       <td>Done</td>
    </tr>
    <tr>
       <td>T08</td>
       <td>Creación de subcomponentes</td>
       <td>Crear o importar componentes necesarios</td>
       <td>2</td>
       <td>Max D.</td>
       <td>Done</td>
    </tr>
    <tr>
       <td>T09</td>
       <td>Creación de los servicios</td>
       <td>Crear kos servicios para obtener los datos</td>
       <td>2</td>
       <td>Max D.</td>
       <td>Done</td>
    </tr>
</table>

#### 6.2.1.3. Development Evidence for Sprint Review

Para el despliegue de la aplicación web utilizamos Netlify: 
Enlace de la aplicacion web: https://verysafe.netlify.app/

#### 6.2.1.4. Testing Suite Evidence for Sprint Review

Para evidenciar la colaboración de todos integrantes del equipo Caffeine en el desarrollo del presente sprint, mostramos a continuación la sección Insights del repositorio donde se encuentra almacenada nuestro iot device.

![team](src/images/team.jpg)

#### 6.2.1.5. Execution Evidence for Sprint Review

#### 6.2.1.6. Software Deployment Evidence for Sprint Review

Enlace de aplicacion web: https://verysafe.netlify.app/

#### 6.2.1.7. Team Collaboration Insights during Sprint
Las actividades de implementación se han desarrollado de acuerdo a lo planificado en el Sprint Planning, donde se han asignado tareas a cada miembro del equipo y se han realizado reuniones grupales para realizar el despliegue. A continuación, se presentan los analíticos de colaboración y commits en GitHub, realizados por los miembros del equipo durante el Sprint 1:

![network](src/images/network.jpg)
