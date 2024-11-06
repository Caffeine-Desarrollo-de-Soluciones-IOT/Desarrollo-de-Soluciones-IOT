# Report Iot

![logo](src/images/logo.webp)

Carrera: Ingeniería de Software

Nombre del curso: Desarrollo de Soluciones IOT

Sección: WV71

Nombre del profesor: Velasquez Nuñez, Angel Augusto

"Informe de TB2"

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

### 1.2.1 Antecedentes y problemática

### 1.2.2 Lean UX Process

#### 1.2.2.1 Lean UX Problem Statements

#### 1.2.2.2 Lean UX Assumptions

#### 1.2.2.3 Lean UX Hypothesis Statements

#### 1.2.2.4 Lean UX Canvas

## 1.3 Segmentos objetivo

### Segmento objetivo 1: Dueños de Inmuebles

# CAPÍTULO II: REQUIREMENTS ELICITATION & ANALYSIS

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

## 3.2. User Stories

## 3.3. Impact Mapping

## 3.4. Product Backlog

# CAPÍTULO IV: SOLUTION SOFTWARE DESIGN

## 4.1. Strategic-Level Domain-Driven Design

En esta sección, presentamos el proceso realizado para las decisiones estratégicas de diseño aplicando Domain-Driven
Design (DDD). Se decidió utilizar DDD debido a su capacidad para estructurar el sistema en dominios claramente
definidos, lo que facilita el manejo de complejidades y promueve la alineación con los objetivos de negocio de
FalconShield. A través de DDD, el equipo puede dividir el sistema en componentes manejables (Bounded Contexts), cada uno
representando áreas críticas del negocio. Esto asegura que las funcionalidades clave se desarrollen de manera coherente
y escalable.

### 4.1.1. EventStorming

Es una técnica colaborativa que nos permite explorar a fondo el dominio de nuestra aplicación de FalconShield, para
realizar el proceso, se llevó a cabo diversas reuniones y con apoyo de la herramienta Miro se pudo desarrollar todo el
flujo y los pasos. Para el primer paso se analizaron diversas opiniones sobre los posibles eventos del dominio y se fue
clasificando según criterios, tales como frecuencia, relevancia, etc.

1. **Primer paso: Unstructured Exploration**

   El primer paso consistió en realizar una exploración sin estructura para identificar posibles eventos en el dominio
   de FalconShield. Durante esta etapa, se analizaron criterios como la frecuencia y relevancia de eventos,
   identificando una variedad de situaciones que los usuarios pueden experimentar, tales como "User registered", "
   Subscription purchased" y "Notification enabled"

   ![event](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-1.png)

2. **Segundo paso: Timelines**

   Posteriormente, organizamos los eventos en una línea de tiempo para visualizar el flujo de interacciones y secuencias
   entre eventos. Esta organización temporal facilita la comprensión de dependencias y secuencias críticas, permitiendo
   un diseño más coherente.

   ![timeline](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-2.png)

3. **Tercer paso: Pain Points**

   En el tercer paso, identificamos "Pain Points" o cuellos de botella en el flujo de eventos. Por ejemplo, nos
   cuestionamos sobre cómo verificar a nuevos usuarios y comparar precios de suscripciones. Estos puntos críticos nos
   permitieron prever posibles problemas y diseñar soluciones adecuadas.

   ![pain](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-3.png)

4. **Cuarto paso: Pivotal Points**

   Identificamos los "Pivotal Points" o eventos cruciales, tales como la configuración de sensores y la aceptación de
   pagos. Estos puntos son esenciales para el flujo del sistema, y su correcta implementación asegura un funcionamiento
   fluido.

   ![pivotal](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-4.png)

5. **Quinto paso: Commands**

   Finalmente, definimos los comandos que los diferentes roles pueden ejecutar en el sistema. Roles como "Security User"
   y "Admin" tienen permisos específicos, lo cual asegura que cada usuario tenga un acceso adecuado a sus funciones.

   ![commands](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-5.png)

El proceso de EventStorming fue realizado con la herramienta Miro y tuvo una duración de aproximadamente 1.45 horas,
alineándose con la recomendación de 1 a 2 horas. Durante este tiempo, el equipo exploró el dominio de FalconShield,
identificando eventos clave, puntos de pivote, y comandos que guían la funcionalidad del sistema.

#### 4.1.1.1 Candidate Context Discovery

Una vez identificados los eventos clave, se procedió a seguir los otros pasos para finalmente agruparlos en contextos
delimitados, que representan áreas de interés o responsabilidades dentro del sistema. Estos contextos se definen en
función de la cohesión de los eventos y las reglas de negocio asociadas. Para descubrir los contextos candidatos,
aplicamos una combinación de análisis de eventos clave y puntos de pivote dentro del EventStorm. Esto permitió una
identificación estructurada de los Bounded Contexts al analizar aquellos eventos con mayor relevancia para el negocio (
look-for-pivotal-events). Así, el equipo fue capaz de definir contextos delimitados en función de la cohesión de eventos
y reglas de negocio compartidas.

1. **Sexto paso: Policies**

   Durante este paso, se establecieron políticas específicas, como "Payment Policies" y "Service Policies," para
   gestionar la interacción entre diferentes componentes del sistema. Estas políticas ayudan a mantener la integridad
   del sistema y minimizan riesgos operativos.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-6.png)

2. **Séptimo paso: Read Models**

   Se definieron modelos de lectura como "Device calibration" y "User Profile," que capturan el estado actual del
   sistema. Estos modelos permiten a los usuarios consultar información actualizada, facilitando la toma de decisiones.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-7.png)

3. **Octavo paso: External Systems**

   Identificamos sistemas externos que interactúan con nuestro sistema, como "Payment Gateway" y "Subscription Manager."
   Estos sistemas son fundamentales para ciertas operaciones, y se han implementado mecanismos para gestionar las
   dependencias.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-8.png)

4. **Noveno paso: Aggregates**

   Los agregados, como "User Profile," "Devices Manager," y "Notification Manager," agrupan entidades relacionadas de
   manera lógica, manteniendo la coherencia y modularidad del sistema.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-9.png)

5. **Décimo paso: Bounded Contexts**

   Finalmente, delimitamos los Bounded Contexts, incluyendo "Identity and Access Management," "Notification Management,"
   y "Events Management." Cada contexto tiene responsabilidades específicas, lo que facilita el mantenimiento y la
   alineación con los objetivos del negocio.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/event-10.png)

Enlace a los diagramas de
EventStorming: [EventStorming](https://miro.com/app/board/uXjVKjBJwpE=/?share_link_id=833719450756)

#### 4.1.1.2 Domain Message Flows Modeling

Para el modelado de los flujos de mensajes del dominio, se utilizó la técnica de EventStorming para identificar los
eventos clave y las interacciones entre ellos. A partir de estos eventos, se crearon diagramas de flujo de mensajes que
representan cómo se comunican los distintos componentes del sistema para lograr los objetivos del negocio. A
continuación, se presentan los diagramas de flujo de mensajes para los contextos identificados en el paso anterior.

1. Sincronización del sistema de seguridad:
   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/message-flow-1.png)

2. Alerta y notificación de eventos:
   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/message-flow-2.png)

3. Alerta y notificación de eventos:
   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/message-flow-3.png)

4. Respuesta a la activación de la alarma:
   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/message-flow-4.png)

#### 4.1.1.3 Bounded Context Canvases

En esta sección se detallan los bounded contexts siguiendo un proceso iterativo recomendado para el Bounded Context
Canvas. A continuación se describe el proceso de diseño de cada contexto, incluyendo la definición del contexto, las
reglas de negocio, el lenguaje ubicuo, y el análisis de capacidades.

### Proceso de Diseño Iterativo

1. **Context Overview Definition**: Se definieron los límites de cada contexto con base en las áreas funcionales
   principales, asegurando que cada contexto mantuviera una cohesión en términos de propósito y función. Los contextos
   incluyen **Events Management**, **Notification Management**, **IoT Asset Management**, **Software Update**, *
   *Identity and Access Management**, **Subscription and Payment**.

2. **Business Rules Distillation & Ubiquitous Language Capture**: Cada contexto fue documentado con las reglas de
   negocio y el lenguaje ubicuo específico. Por ejemplo, en el contexto de **Notification Management**, se definieron
   términos como "activación de notificación" y "confirmación de registro", mientras que en el contexto de *
   *Subscription and Payment**, se capturaron términos como "procesamiento de pago" y "estado de suscripción".

3. **Capability Analysis**: Se analizaron las capacidades requeridas de cada contexto, enfocándose en cómo cada uno
   contribuye al sistema en su conjunto. Esto incluyó el análisis de **Notification Management** para enviar alertas a
   los usuarios y **Events Management** para gestionar y centralizar eventos críticos.

4. **Capability Layering (si aplica)**: No se aplicó una segmentación por capas en cada contexto, ya que la complejidad
   de las interacciones no requería una subdivisión adicional en este caso.

5. **Dependencies Capture**: Se identificaron las dependencias entre contextos. Por ejemplo, el contexto **Notification
   Management** depende de **Events Management** para recibir los eventos a notificar, y **Software Update** depende de
   **IoT Asset Management** para aplicar actualizaciones en los dispositivos.

6. **Design Critique**: Se evaluaron las decisiones de diseño mediante sesiones de revisión en equipo, asegurando que
   cada contexto fuera lo suficientemente autónomo y que las interdependencias estuvieran justificadas. Además, se
   analizó si el diseño optimizaba la flexibilidad y mantenibilidad de la solución.

### Ejemplos de Bounded Contexts

A continuación, se presentan ejemplos de los bounded contexts con los patrones de relación entre ellos:

- **Events Management Context - Notification Management Context (Customer/Supplier)**: La relación entre estos dos
  bounded contexts sigue el patrón Customer/Supplier. El Events Management Context es el proveedor que genera eventos
  críticos como alertas de seguridad o cambios en el estado de los dispositivos IoT. El Notification Management Context,
  como cliente, consume estos eventos y se encarga de enviar notificaciones al usuario a través de distintos canales (
  correo, SMS, etc.).

- **IoT Asset Management Context - Software Update Context (Conformist)**: El IoT Asset Management Context, encargado de
  gestionar los dispositivos IoT, depende del Software Update Context para implementar actualizaciones y parches. En
  este caso, el primero actúa como un Conformist, ya que debe adherirse a las reglas y servicios proporcionados por el
  Software Update Context sin imponer sus propias reglas, asegurando que las actualizaciones se apliquen de manera
  consistente.

- **Security Shield Management System Context - Identity and Access Management Context (Shared Kernel)**: Ambos bounded
  contexts comparten un núcleo común (Shared Kernel), ya que el Security Shield Management System necesita autenticar y
  autorizar a los usuarios y dispositivos, lo cual está estrechamente ligado con las políticas y mecanismos del Identity
  and Access Management Context. Debido a la naturaleza crítica de la seguridad, estas dos áreas deben compartir
  información sensible y estar completamente sincronizadas en términos de datos y lógicas de negocio relacionadas con la
  identidad.

- **Subscription and Payment Context - Notification Management Context (Anti-Corruption Layer)**: La relación entre
  estos dos bounded contexts se beneficia de un Anti-Corruption Layer para traducir y aislar los modelos de dominio. El
  Subscription and Payment Context maneja información financiera y suscripciones, mientras que el Notification
  Management Context envía alertas sobre el estado de las suscripciones o pagos. Para evitar que las complejidades del
  modelo de pagos interfieran con la simplicidad del sistema de notificaciones, se utiliza una capa anticorrupción que
  actúa como interfaz entre ambos contexts.

### 4.1.2. Context Mapping

Para la elaboración de los context maps, se consideraron diferentes alternativas y se realizaron preguntas exploratorias
para optimizar el diseño de la arquitectura. Este proceso incluyó analizar cómo cambiarían las relaciones y las
responsabilidades si se modificaran las capacidades o se reestructuraran los bounded contexts.

1. **Events Management Context - Notification Management Context (Customer/Supplier):**
   La relación entre estos dos bounded contexts sigue el patrón Customer/Supplier. El Events Management Context es el
   proveedor que genera eventos críticos como alertas de seguridad o cambios en el estado de los dispositivos IoT. El
   Notification Management Context, como cliente, consume estos eventos y se encarga de enviar notificaciones al usuario
   a través de distintos canales (correo, SMS, etc.).

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/412-1.jpg)

2. **IoT Asset Management Context - Software Update Context (Conformist):**
   El IoT Asset Management Context, encargado de gestionar los dispositivos IoT, depende del Software Update Context
   para implementar actualizaciones y parches. En este caso, el primero actúa como un Conformist, ya que debe adherirse
   a las reglas y servicios proporcionados por el Software Update Context sin imponer sus propias reglas, asegurando que
   las actualizaciones se apliquen de manera consistente.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/412-2.jpg)

3. **Security Shield Management System Context - Identity and Access Management Context (Shared Kernel):**
   Ambos bounded contexts comparten un núcleo común (Shared Kernel), ya que el Security Shield Management System
   necesita autenticar y autorizar a los usuarios y dispositivos, lo cual está estrechamente ligado con las políticas y
   mecanismos del Identity and Access Management Context. Debido a la naturaleza crítica de la seguridad, estas dos
   áreas deben compartir información sensible y estar completamente sincronizadas en términos de datos y lógicas de
   negocio relacionadas con la identidad.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/412-3.jpg)

4. **Subscription and Payment Context - Notification Management Context (Anti-Corruption Layer):**
   La relación entre estos dos bounded contexts se beneficia de un Anti-Corruption Layer para traducir y aislar los
   modelos de dominio. El Subscription and Payment Context maneja información financiera y suscripciones, mientras que
   el Notification Management Context envía alertas sobre el estado de las suscripciones o pagos. Para evitar que las
   complejidades del modelo de pagos interfieran con la simplicidad del sistema de notificaciones, se utiliza una capa
   anticorrupción que actúa como interfaz entre ambos contexts.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/412-4.jpg)

### Análisis de Alternativas en Context Mapping

- **Pregunta 1:** ¿Qué pasaría si movemos la capacidad de notificaciones al contexto de **Events Management**?
    - **Respuesta:** Esto simplificaría el flujo de notificaciones, pero reduciría la flexibilidad de enviar alertas
      personalizadas. Mantener **Notification Management** como un contexto separado asegura que las notificaciones sean
      adaptables y personalizables sin afectar la lógica central de eventos.

- **Pregunta 2:** ¿Qué pasaría si dividimos el **IoT Asset Management Context** en dos contextos: uno para gestión de
  dispositivos y otro para actualizaciones?
    - **Respuesta:** Dividir este contexto podría mejorar la especialización en cada área, pero también introduciría más
      complejidad en la coordinación. Se decidió mantenerlo como un solo contexto para evitar interdependencias
      innecesarias y facilitar la gestión centralizada de los dispositivos.

- **Pregunta 3:** ¿Qué pasaría si duplicamos la funcionalidad de verificación de usuarios entre **Identity and Access
  Management** y **Security Shield Management System**?
    - **Respuesta:** La duplicación de esta funcionalidad podría reducir el tiempo de respuesta en cada contexto, pero
      llevaría a una inconsistencia en la autenticación. Se optó por utilizar un núcleo compartido (Shared Kernel) para
      asegurar que ambas áreas accedan a una única fuente de autenticación y autorización.

Con base en el análisis, se implementaron los siguientes patrones de relación entre contextos:

- **Customer/Supplier** entre **Events Management** y **Notification Management**.
- **Conformist** entre **IoT Asset Management** y **Software Update**.
- **Shared Kernel** entre **Security Shield Management System** e **Identity and Access Management**.
- **Anti-Corruption Layer** entre **Subscription and Payment** y **Notification Management**.

### 4.1.3. Software Architecture

Se presenta la representación de la Arquitectura de Software para la solución utilizando el modelo C4, el cual
proporciona una visión clara de cómo se organiza y se comunica cada componente del sistema.

#### 4.1.3.1. Software Architecture System Landscape Diagram

El diagrama de landscape ofrece una visión general de cómo los usuarios interactúan con los sistemas externos. Este
diagrama centraliza el sistema y lo rodea con los usuarios (como el **Property User** y el **Security User**) y sistemas
externos (como **AWS SNS**) para dar una perspectiva completa de las interacciones.

![landscape](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/landscape%20diagram.jpg)

#### 4.1.3.2. Software Architecture Context Level Diagrams

En este diagrama se muestra cómo el sistema interactúa con elementos externos. Los usuarios principales son *
*Consumidores o Negocios**, quienes se conectan con la aplicación para gestionar la seguridad de sus inmuebles. La
aplicación también se conecta con **AWS SNS** para el envío de notificaciones.

![contexto](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/contexto.jpg)

En nuestro diagrama mostramos a los usuarios que son los consumidores de inmuebles o negocios que buscan mantener
mejorar la seguridad de su inmueble, este está conectado con la aplicación para que el usuario pueda interactuar y
finalmente se conecta con un servicio externo que utilizamos para el envío de notificaciones.

#### 4.1.3.2. Software Architecture Container Level Diagrams

Son representaciones visuales de la arquitectura de software a nivel de contenedores, que muestran cómo se agrupan y se
comunican los distintos componentes y servicios dentro de un sistema o aplicación. Estos diagramas proporcionan una
vista detallada de la organización de los contenedores de software, lo que ayuda a entender la estructura y las
interacciones en la arquitectura general.

![container](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/container.png)

Para el diagrama de contenedores desglosamos a nuestros usuarios que son el propietario de inmuebles y el usuario de
seguridad, cada uno interactúa con nuestras aplicaciones en este caso el propietario interactúa con nuestro Single Page
Application, Web Application y Mobile Application dado que podrá manejar un sistema más integral. Asimismo el usuario de
seguridad tendrá su tipo de acceso en el Web Application y Mobile Application para el monitoreo de las alarmas de
seguridad.
Pasando con las aplicaciones propuestas, tenemos que el Single Page Application que es una primera vista de nuestra
propuesta de solución se conecta con el Web Application.
Para el Web Application tenemos que se conecta con la API de la aplicación y esta misma API va a una base de datos de la
aplicación.
Para lo que es el Mobile Application tiene conexión a su misma base de datos y conexión con la API principal de nuestra
aplicación.
Asi también tenemos nuestro dispositivo IoT, el cual se conecta con el edge API y este a su vez a su base de datos con
la API general de todo la aplicación.
Finalmente, la API principal lo conectamos con nuestro servicio externo de mensajería AWS SNS.

#### 4.1.3.3. Software Architecture Deployment Diagrams

El diagrama de despliegue ilustra cómo los componentes de software se distribuyen en el entorno de producción,
incluyendo detalles de la infraestructura y la comunicación entre servicios. Cada componente, como la base de datos y
las API, está desplegado en un entorno específico que garantiza la seguridad y escalabilidad del sistema.

![deployment](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/deployment.jpg)

## 4.2. Tactical-Level Domain-Driven Design

### 4.2.1. Bounded Context: Subscription & Payments context

El Subscription and Payment Context abarca todos los procesos y funciones relacionados con la gestión de suscripciones y
pagos dentro de nuestro sistema. Este contexto es responsable de manejar la creación, modificación y cancelación de
suscripciones, así como de procesar pagos y gestionar el estado de los mismos. Incluye la administración de detalles
relacionados con los clientes, el seguimiento de las facturas y el estado de cada pago, y la sincronización con sistemas
externos como Stripe. Asegura que las suscripciones y pagos se gestionen de manera eficiente y precisa, proporcionando
una experiencia de servicio continua y sin interrupciones para los usuarios. A continuación, se detallan las clases
identificadas en este contexto:

#### Clases Identificadas

1. **Clase `Customer`**
    - **Propósito:** Representa a un cliente del sistema.
    - **Atributos:**
        - `id: string` - Identificador único del cliente.
        - `name: string` - Nombre del cliente.
        - `email: string` - Correo electrónico del cliente.
        - `stripeCustomerId: string` - Identificador del cliente en Stripe.
    - **Métodos:**
        - `getCustomerDetails(): CustomerDetails` - Retorna un objeto `CustomerDetails` con la información básica del
          cliente.
        - `registerCustomer(): void` - Registra al cliente en el sistema de pagos de Stripe.
    - **Relaciones:** Relación `1...n` con `Subscription`, ya que un cliente puede tener múltiples suscripciones.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/customer-class.png)

2. **Clase `Subscription`**
    - Propósito: La clase Subscription gestiona las suscripciones de un cliente a un servicio específico. Mantiene los
      detalles esenciales, como el estado de la suscripción y las fechas de inicio y finalización. Los detalles más
      complejos de la suscripción son manejados por Stripe.
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

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscription-class.png)

3. **Clase `Payment`**
    - Propósito: Esta clase almacena la información de los pagos realizados por un cliente en relación con una
      suscripción. Aunque Stripe gestiona el procesamiento de pagos, esta clase registra información relevante
      localmente, como el estado y monto del pago.
    - Atributos:
        - `id: string` - Identificador único del pago
        - `amount: double` - Monto del pago
        - `currency: string` - Moneda en la que se realizó el pago (ejm: USD, EUR)
        - `paymentDate: Date` - Fecha en la que se procesó el pago
        - `status: string` - Estado actual del pago (ejm: SUCCEEDED, FAILED)
        - `stripePaymentId: string` - Identificador del pago en el sistema de Stripe
    - Métodos:
        - `getPaymentDetails(): PaymentDetails` - Proporciona información detallada del pago.
    - Relaciones:
        - `n...1` con Subscription, un pago pertenece a una suscripción.
        - `1...n` con Invoice, un pago puede tener varias facturas asociadas.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/payment-class.png)

4. **Clase `Invoice`**
    - Propósito: Esta clase representa una factura generada por un pago. Aunque Stripe emite las facturas, esta clase
      localiza la información esencial de las mismas, como el monto total y la fecha de emisión.
    - Atributos:
        - `id: string` - Identificador único de la factura
        - `invoiceDate: Date` - Fecha de emisión de la factura
        - `totalAmount: double` - Monto total de la factura
        - `stripeInvoiceId: string` - Identificador de la factura en Stripe
    - Métodos:
        - `getInvoiceDetails(): InvoiceDetails` - Proporciona detalles de la factura.
    - Relaciones:
        - `n...1` con Payment, una factura pertenece a un pago.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/invoice-class.png)

#### 4.2.1.1. Domain Layer

En esta sección se presenta la capa de Dominio del contexto de **Suscripción y Pagos** dentro del sistema. La capa de
Dominio es el núcleo de la aplicación, donde se representan las reglas de negocio y la lógica fundamental del sistema.
En el contexto de **Suscripción y Pagos**, esta capa incluye Entidades, Objetos de Valor, Agregados y Servicios de
Dominio que soportan los procesos de administración de suscripciones y procesamiento de pagos.

## Clases Core de la Aplicación

### Entities

Las siguientes entidades representan los elementos fundamentales del contexto de **Suscripción y Pagos**:

1. **Customer**
    - **Propósito**: Representa a un usuario de la aplicación móvil que se suscribe a servicios IoT de seguridad.
    - **Atributos**:
        - `id: string` - Identificador único del cliente.
        - `name: string` - Nombre del cliente.
        - `email: string` - Correo electrónico del cliente.
        - `stripeCustomerId: string` - Identificador del cliente en el sistema de Stripe.
    - **Métodos**:
        - `getCustomerDetails(): CustomerDetails` - Retorna los detalles básicos del cliente.
        - `registerStripeCustomer(): void` - Registra al cliente en Stripe.
    - **Relaciones**:
        - `1...n` con **Subscription**, ya que un cliente puede tener varias suscripciones activas.
          ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/customer-class-entity.png)

2. **Subscription**
    - **Propósito**: Representa una suscripción de un cliente a un plan específico.
    - **Atributos**:
        - `id: string` - Identificador único de la suscripción.
        - `status: SubscriptionStatus` - Estado actual de la suscripción.
        - `startDate: Date` - Fecha de inicio de la suscripción.
        - `endDate: Date` - Fecha de finalización de la suscripción.
        - `stripeSubscriptionId: string` - Identificador de la suscripción en Stripe.
    - **Métodos**:
        - `getSubscriptionDetails(): SubscriptionDetails` - Retorna los detalles de la suscripción.
        - `cancelSubscription(): void` - Cancela la suscripción.
    - **Relaciones**:
        - `n...1` con **Customer**.
        - `1...n` con **Payment**.
          ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscription-class-entity.png)

3. **Payment**
    - **Propósito**: Esta entidad representa un pago asociado a una suscripción, aunque Stripe procesa los pagos, esta
      entidad almacena localmente la información esencial del pago.
    - **Atributos**:
        - `id: string` - Identificador único del pago.
        - `amount: Money` - Monto del pago.
        - `paymentDate: Date` - Fecha del pago.
        - `status: PaymentStatus` - Estado del pago.
        - `stripePaymentId: string` - Identificador del pago en Stripe.
    - **Métodos**:
        - `getPaymentDetails(): PaymentDetails` - Retorna los detalles del pago.
    - **Relaciones**:
        - `n...1` con **Subscription**.
        - `1...n` con **Invoice**.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/payment-class-entity.png)

4. **Invoice**
    - **Propósito**: Representa una factura generada por un pago.
    - **Atributos**:
        - `id: string` - Identificador único de la factura.
        - `invoiceDate: Date` - Fecha de emisión de la factura.
        - `totalAmount: Money` - Monto total de la factura.
        - `stripeInvoiceId: string` - Identificador de la factura en Stripe.
    - **Métodos**:
        - `getInvoiceDetails(): InvoiceDetails` - Retorna los detalles de la factura.
    - **Relaciones**:
        - `n...1` con **Payment**.

   ![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/invoice-class-entity.png)

### Value Objects

Los siguientes objetos de valor encapsulan conceptos de negocio que se utilizan en varias clases de la aplicación:

1. **SubscriptionPlan**
    - **Propósito**: Encapsula detalles de un plan de suscripción, como el nombre, el precio y la duración.
    - **Atributos**:
        - `name: string` - Nombre del plan.
        - `price: Money` - Precio del plan.
        - `durationInMonths: int` - Duración en meses.
    - ![SubscriptionPlan Class](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscriptionplan-class-vo.png)

2. **Money**
    - **Propósito**: Encapsula el concepto de dinero, incluyendo el monto y la moneda.
    - **Atributos**:
        - `amount: double` - Monto de dinero.
        - `currency: Currency` - Moneda en la que se realiza el pago.
    - ![Money Class](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/money-class-vo.png)

3. **Currency (Enumeration)**
    - **Propósito**: Define las monedas permitidas en la aplicación.
    - **Valores**:
        - `USD`, `PEN`, `EUR`
    - ![Currency Enumeration](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/currency-enum.png)

4. **SubscriptionStatus (Enumeration)**
    - **Propósito**: Define los posibles estados de una suscripción.
    - **Valores**:
        - `ACTIVE`, `CANCELED`, `PAST_DUE`, `INCOMPLETE`, `UNPAID`
    - ![SubscriptionStatus Enumeration](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscriptionstatus-enum.png)

5. **PaymentStatus (Enumeration)**
    - **Propósito**: Define los posibles estados de un pago.
    - **Valores**:
        - `SUCCEEDED`, `FAILED`, `PENDING`, `CANCELED`
    - ![PaymentStatus Enumeration](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/paymentstatus-enum.png)

### Aggregates

El agregado **CustomerAggregate** encapsula la lógica de negocio relacionada con los clientes y sus suscripciones,
permitiendo gestionar las operaciones de manera transaccional y coherente.

1. **CustomerAggregate**
    - **Propósito**: Coordina la lógica de negocio relacionada con los clientes, sus suscripciones y pagos.
    - **Atributos**:
        - `customerData: Customer` - Datos del cliente.
        - `subscription: Subscription` - Datos de suscripción.
    - **Métodos**:
        - `getAccount()`
        - `cancelSubscription()`
        - `viewPayments()`
        - `createCustomerPortal()`
    - ![CustomerAggregate Class](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/customeraggregate.png)

### Domain Services

El **SubscriptionService** contiene la lógica de negocio relacionada con la gestión de suscripciones, incluyendo la
creación, cancelación y renovación de las mismas.

1. **SubscriptionService**
    - **Propósito**: Coordina las operaciones relacionadas con las suscripciones de manera eficiente.
    - **Métodos**:
        - `createSubscription()`
        - `cancelSubscription()`
        - `renewSubscription()`
    - ![SubscriptionService](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscriptionservice.png)

## Reglas de Negocio

Las reglas de negocio que gobiernan el comportamiento de las entidades y objetos en el contexto de **Suscripción y Pagos
** son las siguientes:

- **Renovación Automática**: Las suscripciones se renuevan automáticamente a menos que se cancelen antes de la fecha de
  renovación.
- **Cancelación de Suscripciones**: Una suscripción con pagos pendientes no puede ser cancelada.
- **Procesamiento de Pagos**: Los pagos deben ser procesados de forma segura y reflejarse en el estado correspondiente
  de la suscripción.
- **Manejo de Pagos Fallidos**: Los pagos fallidos deben ser gestionados adecuadamente para evitar interrupciones en el
  servicio.
- **Generación de Facturas**: Las facturas deben generarse automáticamente después de cada pago exitoso.
- **Actualización de Información del Cliente**: La información del cliente, como el correo electrónico, debe estar
  siempre sincronizada con Stripe.

Esta capa de dominio define claramente las entidades, objetos de valor, agregados y servicios que componen el núcleo de
la aplicación. Cumple con los criterios de diseño, siguiendo los principios de Domain-Driven Design para representar de
manera fiel las reglas y la lógica del dominio específico de **Suscripción y Pagos**.

#### 4.2.1.2. Interface Layer

En esta sección, se detallan las clases que forman parte de la capa de presentación o capa de interfaz para el contexto
de "Subscription & Payments". Estas clases permiten la interacción entre los usuarios y el sistema, manejando las
solicitudes HTTP y devolviendo respuestas adecuadas a través de controladores RESTful. Los controladores presentados se
encargan de gestionar clientes, suscripciones y planes de suscripción, y están diseñados para interactuar con la capa de
dominio de manera eficaz y segura.

- **CustomerController**: expone las operaciones relacionadas con los clientes de la aplicación. Permite la creación,
  actualización y consulta de los clientes, así como la gestión de su relación con Stripe. Al crear un cliente, se
  genera un identificador (stripeCustomerId) que es guardado en la entidad local y se sincroniza con el sistema de
  Stripe.
    - **Métodos**:
        - `createCustomer(CreateCustomerDto request): ResponseEntity` - Crea un nuevo cliente en el sistema y lo
          registra en Stripe.
        - `getCustomer(String customerId): CustomerDto` - Recupera los detalles de un cliente específico.
        - `updateCustomer(String customerId, UpdateCustomerDto req): ResponseEntity` - Actualiza la información de un
          cliente en el sistema y en Stripe.
        - `deleteCustomer(String customerId): ResponseEntity` - Elimina un cliente del sistema y de Stripe.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/customer-controller.png)

- **SubscriptionController**: gestiona las operaciones relacionadas con las suscripciones de los clientes. Este
  controlador
  permite crear nuevas suscripciones, actualizar el estado de las mismas y cancelarlas, todo esto interactuando con los
  servicios de Stripe.
    - **Métodos**:
        - `createSubscription(String customerId, CreateSubscriptionDto request): SubscriptionDto` - Crea una nueva
          suscripción para un cliente.
        - `getSubscription(String customerId): List<SubscriptionDto>` - Recupera la lista de suscripciones activas de un
          cliente.
        - `cancelSubscription(String subscriptionId): ResponseEntity` - Cancela una suscripción específica.
        - `renewSubscription(String customerId): ResponseEntity` - Renueva una suscripción para el cliente.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscription-controller.png)

- **PlanController**: gestiona los planes de suscripción disponibles en la aplicación. Los usuarios pueden consultar los
  planes disponibles, sus características y precios.
    - **Métodos**:
        - `getAvailablePlans(): List<PlanDto>` - Recupera una lista de todos los planes de suscripción disponibles.
        - `getPlanDetails(String planId): PlanDto` - Muestra los detalles de un plan específico de suscripción.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/plan-controller.png)

### Conclusión

Las clases de la capa de interfaz implementadas cumplen con el objetivo de manejar la comunicación entre la capa de
presentación y la capa de dominio. Los controladores están diseñados para permitir la gestión eficiente y segura de los
clientes, suscripciones y planes de suscripción, asegurando una interacción fluida y organizada entre el usuario final y
el sistema.

#### 4.2.1.3. Application Layer

Esta capa, para el Subscription and Payment Context, se definen los flujos de negocios a través de clases de tipo
Command Handlers y Event Handlers, asegurando que los procesos de suscripción, pago y gestión de eventos externos (como
los webhooks de Stripe) se manejen correctamente. Estos handlers permiten que el sistema sea reactivo, eficiente y
mantenga la consistencia entre las operaciones internas y los eventos externos. A continuación, se presentan los
handlers y eventos identificados para este contexto:

#### Command Handlers:

1. **CreateSubscriptionCommandHandler**
    - **Descripción**: Maneja el proceso de creación de una nueva suscripción para un cliente. Este handler se encarga
      de validar los datos de entrada y crear la suscripción tanto en el sistema como en Stripe.
    - **Atributos**:
        - `subscriptionService: SubscriptionService` - Servicio para gestionar suscripciones.
    - **Métodos**:
        - `handle(CreateSubscriptionCommand command): SubscriptionDto` - Ejecuta la creación de suscripción.
    - **Diagrama**:

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/createsubscription-ch.png)

2. **ProcessPaymentCommandHandler**
    - **Descripción**: Registra el pago procesado por Stripe en la base de datos y mantiene la consistencia entre el
      estado del pago y la suscripción asociada.
    - **Atributos**:
        - `paymentService: PaymentService` - Servicio para procesar pagos.
    - **Métodos**:
        - `handle(ProcessPaymentCommand command): PaymentDto` - Procesa y guarda el pago.
    - **Diagrama**:
      ![ProcessPaymentCommandHandler](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/processpayment-ch.png)

3. **CancelSubscriptionCommandHandler**
    - **Descripción**: Gestiona la cancelación de una suscripción existente, verificando si puede ser cancelada,
      actualizando su estado y notificando a Stripe.
    - **Atributos**:
        - `subscriptionService: SubscriptionService` - Servicio para gestionar suscripciones.
    - **Métodos**:
        - `handle(CancelSubscriptionCommand command): void` - Ejecuta la cancelación de la suscripción.
    - **Diagrama**:
      ![CancelSubscriptionCommandHandler](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/cancelsubscription-ch.png)

#### Event Handlers

1. **StripeWebhookEventHandler**
    - **Descripción**: Maneja los eventos provenientes de Stripe a través de webhooks. Asegura el procesamiento adecuado
      de eventos de facturación, pagos fallidos, renovaciones de suscripciones, etc.
    - **Atributos**:
        - `subscriptionService: SubscriptionService` - Servicio para gestionar suscripciones.
    - **Métodos**:
        - `handle(StripeEvent event): void` - Procesa los eventos de Stripe.
    - **Diagrama**:
      ![StripeWebhookEventHandler](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/stripewebhook-eh.png)

2. **SubscriptionExpiredEventHandler**
    - **Descripción**: Reacciona cuando una suscripción llega a su fecha de finalización sin ser renovada, gestionando
      la lógica de expiración, como notificación al cliente y desactivación de servicios.
    - **Atributos**:
        - `subscriptionService: SubscriptionService` - Servicio para gestionar suscripciones.
    - **Métodos**:
        - `handle(SubscriptionExpiredEvent event): void` - Ejecuta las acciones necesarias ante la expiración de la
          suscripción.
    - **Diagrama**:
      ![SubscriptionExpiredEventHandler](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscriptionexpired-eh.png)

3. **PaymentFailedEventHandler**
    - **Descripción**: Reacciona a eventos de pagos fallidos, generados por el dominio o recibidos de Stripe,
      notificando al cliente, reintentando el pago y, si es necesario, cancelando la suscripción.
    - **Atributos**:
        - `paymentService: PaymentService` - Servicio para gestionar pagos.
    - **Métodos**:
        - `handle(PaymentFailedEvent event): void` - Ejecuta la lógica ante el fallo de un pago.
    - **Diagrama**:
      ![PaymentFailedEventHandler](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/paymentfailed-eh.png)

#### Capabilities Cubiertos

Las clases de la Application Layer están diseñadas para cubrir los siguientes capabilities del sistema:

1. **Gestión de Suscripciones**: A través de los Command Handlers como `CreateSubscriptionCommandHandler` y
   `CancelSubscriptionCommandHandler`, el sistema permite a los clientes gestionar sus suscripciones, incluyendo
   creación, cancelación y renovación.

2. **Procesamiento de Pagos**: Mediante `ProcessPaymentCommandHandler` y event handlers como
   `PaymentFailedEventHandler`, el sistema registra los pagos, integrándose con Stripe y gestionando pagos fallidos.

3. **Manejo de Eventos Externos (Stripe Webhooks)**: `StripeWebhookEventHandler` garantiza que el sistema reaccione
   adecuadamente a eventos de Stripe, sincronizando estados de suscripciones y pagos entre la plataforma y el sistema.

4. **Manejo de Expiración de Suscripciones**: `SubscriptionExpiredEventHandler` asegura que, cuando una suscripción
   expire, se tomen las acciones necesarias, como notificar al cliente y desactivar servicios asociados.

#### Recomendaciones

- Asegurar la implementación de pruebas unitarias para cada Command y Event Handler, validando que los flujos de negocio
  se ejecutan correctamente.
- Documentar la integración con Stripe y cualquier servicio externo, detallando cómo cada handler interactúa con estos
  servicios.
- Verificar que cada handler gestione adecuadamente los posibles errores para garantizar la robustez del sistema.

#### 4.2.1.4. Infrastructure Layer

Esta capa es responsable de proporcionar la implementación de las operaciones que interactúan con recursos externos,
como bases de datos, servicios de terceros (por ejemplo, Stripe), sistemas de mensajería y otros. En esta capa, también
se implementan los Repositories definidos en la Domain Layer, que permiten la persistencia de las entidades del sistema.
A continuación, se presentan las clases clave de esta capa, con una breve descripción de su función en el contexto del
sistema:

1. **StripePaymentGateway**: Es la clase encargada de la integración con el sistema de pagos de Stripe. Implementa las
   operaciones necesarias para gestionar pagos, suscripciones y facturación a través de la API de Stripe.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/stripepaymentgateway.png)

2. **NotificationService**: Se encarga de enviar notificaciones a los usuarios, ya sea por correo electrónico, SMS o
   cualquier otro medio configurado. Es utilizada para notificar eventos importantes, como pagos fallidos, renovaciones
   de suscripción o vencimientos.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/notificationservice.png)

3. **StripeWebhookService**: Se encarga de procesar las notificaciones recibidas desde Stripe a través de webhooks. Esta
   clase recibe los eventos de Stripe y los transforma en eventos internos del dominio que los Event Handlers procesan.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/stripewebhookservice.png)

4. **PaymentRepository**: Esta clase maneja las operaciones de almacenamiento y recuperación de información relacionada
   con
   los pagos realizados por los clientes.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/payment-repo.png)

5. **SubscriptionRepository**: Esta clase se encarga de manejar las operaciones de persistencia de las suscripciones en
   la
   base de datos.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/subscription-repo.png)

6. **CustomerRepository**: Se encarga de gestionar la persistencia de la información de los clientes, incluyendo la
   sincronización con el sistema de Stripe.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/customer-repo.png)

#### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams

En esta sección, se presenta el diagrama de componentes para el Bounded Context **Subscription & Payments**, mostrando
la estructura interna de los contenedores y sus interacciones principales. Este diagrama, creado siguiendo el modelo C4,
descompone cada contenedor en componentes específicos, explicando sus responsabilidades y las tecnologías utilizadas.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/c4-component-bc-subscriptions.png)

##### Componentes Identificados

1. **Single-Page Application**
    - **Descripción**: Proporciona la interfaz web para los usuarios de la aplicación Falcon Shield. Permite la gestión
      de suscripciones, pagos y acceso a las funcionalidades de seguridad.
    - **Interacción**: Realiza llamadas API (JSON/HTTP) al backend para operar con los datos y gestionar las
      suscripciones.

2. **Mobile Application**
    - **Descripción**: Interfaz móvil para Falcon Shield, diseñada para dispositivos Android y iOS. Ofrece
      funcionalidades similares a la interfaz web, optimizadas para dispositivos móviles.
    - **Interacción**: Comunica con el backend mediante llamadas API para sincronizar datos de suscripciones y pagos.

3. **Subscription Controller**
    - **Responsabilidad**: Exponer una interfaz para las operaciones de pago y suscripción, gestionando las
      interacciones entre la aplicación y el sistema de pagos de Stripe.
    - **Interacción**: Utiliza el **Stripe Payment Gateway** para la integración directa con Stripe y delega las
      operaciones de almacenamiento al **Subscription Repository**.

4. **Stripe Payment Gateway**
    - **Responsabilidad**: Implementa la SDK de Stripe para la gestión de pagos y suscripciones. Encargado de conectar y
      gestionar la comunicación con la API de Stripe.
    - **Interacción**: Procesa los pagos y envía eventos de notificación a **Stripe Webhook Service** para mantener el
      sistema sincronizado.

5. **Stripe Webhook Service**
    - **Responsabilidad**: Gestiona los eventos de Stripe recibidos a través de webhooks, como pagos exitosos o
      fallidos, y envía actualizaciones al sistema interno.
    - **Interacción**: Utiliza el **Subscription Service** para actualizar el estado de las suscripciones basándose en
      los eventos de Stripe.

6. **Subscription Service**
    - **Responsabilidad**: Administrar el estado y la persistencia de las suscripciones en el sistema, incluyendo la
      creación, cancelación y actualización de suscripciones.
    - **Interacción**: Depende de **Subscription Repository** para realizar operaciones de almacenamiento en la base de
      datos.

7. **Subscription Repository**
    - **Responsabilidad**: Manejar las operaciones de almacenamiento de suscripciones, garantizando la persistencia de
      los datos en la base de datos PostgreSQL.
    - **Interacción**: Realiza operaciones de lectura/escritura en el contenedor **Database**.

8. **Payment Repository**
    - **Responsabilidad**: Gestionar la persistencia y recuperación de la información de pagos realizados por los
      clientes.
    - **Interacción**: Interactúa con el **Database** para almacenar y acceder a los datos de pagos, asegurando
      consistencia en el estado de los pagos.

9. **Database**
    - **Descripción**: Almacena todas las operaciones relacionadas con suscripciones y pagos, proporcionando un
      repositorio confiable y persistente de datos.
    - **Interacción**: Es accedido por los componentes **Subscription Repository** y **Payment Repository** para la
      lectura/escritura de datos.

#### Tecnologías y Detalles de Implementación

- **Backend**: Implementado en Spring Service, que facilita la integración con Stripe y permite la organización
  estructural de componentes.
- **Base de Datos**: PostgreSQL, elegido por su robustez y soporte para operaciones complejas de transacción.
- **Frontends**: Angular y Flutter para proporcionar aplicaciones web y móviles de alto rendimiento y accesibles para el
  usuario.

#### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams

El diagrama de clases UML para el contexto delimitado de "Subscription & Payments" muestra las principales entidades y
relaciones de la capa de dominio. Este diagrama incluye las clases `Customer`, `Subscription`, `Payment` e `Invoice`,
junto con los objetos de valor `Money` y `Currency`, y otros elementos como enumeraciones y agregados que definen el
comportamiento y estado de las suscripciones y pagos en el sistema. Además, el diagrama detalla los atributos, métodos y
visibilidad (privado, público) de cada clase, cumpliendo con los criterios establecidos.

**Componentes principales:**

- **Entities**:
    - `Customer`: Representa a un cliente de la aplicación, contiene información como el nombre, correo electrónico e
      identificador de Stripe.
    - `Subscription`: Representa una suscripción de un cliente a un plan, incluye el estado y fechas de la suscripción.
    - `Payment`: Encapsula los detalles de un pago realizado por el cliente, como el monto y el estado.
    - `Invoice`: Representa una factura generada por un pago exitoso.

- **Value Objects**:
    - `Money`: Maneja el concepto de dinero en diferentes monedas.
    - `Currency`: Enumera las monedas soportadas.

- **Enumerations**:
    - `SubscriptionStatus`: Define los posibles estados de una suscripción, como `ACTIVE` y `CANCELED`.
    - `PaymentStatus`: Enumera los estados posibles de un pago, incluyendo `SUCCEEDED` y `FAILED`.

- **Aggregate**:
    - `CustomerAggregate`: Encapsula la lógica de negocio y asegura la consistencia de las operaciones de los clientes y
      suscripciones.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/class-diagram-subs.png)

##### 4.2.1.6.2. Bounded Context Database Design Diagram

El diseño de la base de datos para el contexto de "Subscription & Payments" incluye las entidades principales en forma
de tablas relacionales y sus respectivas relaciones. El diagrama de la base de datos presenta los atributos, tipos de
datos, claves primarias y foráneas, asegurando la integridad referencial entre las tablas. Esto permite una persistencia
de los datos necesaria para soportar las operaciones relacionadas con las suscripciones y pagos.

**Descripción de Tablas Principales:**

- **subscription_plans**: Contiene los planes de suscripción con sus características únicas.
- **subscriptions**: Almacena información de las suscripciones activas, incluyendo referencias a los clientes y planes.
- **payments**: Gestiona los pagos realizados por cada suscripción, con referencias a métodos de pago y estados.

**Claves Primarias y Foráneas**:

- Cada tabla incluye claves primarias (`PK`) para identificar de manera única cada registro.
- Las relaciones entre las tablas están representadas mediante claves foráneas (`FK`) para asegurar la integridad
  referencial entre suscripciones, planes y pagos.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/database-design-subs.png)

### 4.2.2. Bounded Context: Device

#### 4.2.2.1 Domain Layer

- **Entidades de dominio**:
    - **Device**: Representa un dispositivo IoT instalado en el inmueble, incluyendo sus características y estado.
    - **Installation**: Representa la instalación de un dispositivo en un inmueble, incluyendo la fecha de instalación y
      el estado de la instalación.
    - **Property**: Representa la propiedad (inmueble) donde los dispositivos están instalados, incluyendo detalles
      sobre la ubicación y características.

- **Objetos de valor**:
    - **DeviceConfiguration**: Contiene la configuración específica de cada dispositivo, como el tipo de dispositivo,
      configuraciones de red y parámetros operativos.
    - **InstallationDetails**: Información sobre la instalación del dispositivo, como la ubicación exacta y el método de
      instalación.

- **Repositorios**:
    - **DeviceRepository**: Maneja la persistencia de los dispositivos.
    - **InstallationRepository**: Maneja la persistencia de las instalaciones de dispositivos.
    - **PropertyRepository**: Maneja la persistencia de las propiedades donde se instalan los dispositivos.

#### 4.2.2.2 Interface Layer

- **DeviceController**: Gestiona la configuración y visualización de dispositivos IoT. Permite a los usuarios ver,
  agregar y actualizar la información de los dispositivos instalados, así como revisar el estado y configuraciones de
  cada dispositivo.

- **InstallationController**: Maneja la gestión de la instalación de dispositivos. Permite a los usuarios iniciar nuevas
  instalaciones, actualizar el estado de las instalaciones y visualizar el historial de instalaciones.

- **PropertyController**: Gestiona la información de las propiedades donde los dispositivos están instalados. Permite a
  los usuarios ver detalles sobre las propiedades y asociar dispositivos con propiedades específicas.

#### 4.2.2.3. Application Layer

- **Command Handlers**:
    - **RegisterDeviceCommandHandler**: Procesa la solicitud para registrar un nuevo dispositivo IoT en el sistema. Este
      handler maneja la creación de registros para nuevos dispositivos y su configuración inicial.
    - **UpdateDeviceConfigurationCommandHandler**: Maneja las actualizaciones en la configuración de un dispositivo
      existente.
    - **InstallDeviceCommandHandler**: Procesa la solicitud para instalar un dispositivo en una propiedad. Maneja la
      asociación del dispositivo con la propiedad y actualiza el estado de la instalación.
    - **UninstallDeviceCommandHandler**: Maneja la solicitud para desinstalar un dispositivo, actualizando el estado del
      dispositivo y la propiedad asociada.

- **Event Handlers**:
    - **DeviceRegisteredEventHandler**: Responde a eventos que confirman la creación y registro exitoso de un
      dispositivo. Actualiza el estado del dispositivo en la base de datos y emite eventos relacionados.
    - **DeviceConfigurationUpdatedEventHandler**: Maneja eventos que indican que la configuración de un dispositivo ha
      sido actualizada. Actualiza la base de datos y notifica a los usuarios correspondientes.
    - **DeviceInstalledEventHandler**: Maneja eventos de instalación exitosa de un dispositivo. Actualiza el estado de
      la instalación y emite notificaciones.
    - **DeviceUninstalledEventHandler**: Responde a eventos que indican que un dispositivo ha sido desinstalado.
      Actualiza el estado en la base de datos y emite notificaciones relacionadas.

#### 4.2.2.5. Bounded Context Software Architecture Component Level Diagrams

Este diagrama proporciona una vista de la estructura de la arquitectura y cómo los diferentes componentes interactúan
dentro del aggregate Devices.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/c4-devices.png)

#### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams

El diagrama UML del bounded context "Devices" ilustra las clases Property, Devices, Installation y DeviceConfigurations
con sus respectivos atributos y métodos. Las clases también contienen métodos para crear, actualizar, validar y eliminar
instancias.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/devices-diagram.png)

#### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams

Este diagrama de base de datos representa las tablas y las relaciones dentro del bounded context "Devices". Se define la
entidad devices, que almacena información sobre ek tipo y la descripción del dispositivo de seguridad. La entidad
devices_type almacena el tipo de dispositivo.

![alt text](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/devices-db.png)

<!-- TODO -->

### 4.2.3. Bounded Context: Area

#### 4.2.3.1. Domain Layer

- Entities:
    - Área: Representa un área específica en la que se colocan los dispositivos.
        - Atributos: id, name, icon, color.
    - Property: Representa una propiedad que puede tener múltiples áreas.
        - Atributos: id, name, image_url, address.

- Value Objects:
    - AreaId: Identificador único de un área.
    - PropertyId: Identificador único de una propiedad.

- Aggregates:
    - AreaAggregate: Agregado raíz que encapsula las operaciones relacionadas con las áreas, incluyendo la creación,
      actualización y eliminación de áreas.
    - PropertyAggregate: Agregado raíz que encapsula las operaciones relacionadas con las propiedades, incluyendo la
      asociación con áreas.

- Domain Services:
    - AreaService: Define las operaciones de negocio relacionadas con las áreas, como la creación, actualización y
      eliminación de áreas.
    - PropertyService: Define las operaciones de negocio relacionadas con las propiedades, como la gestión de áreas
      asociadas.

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
    - AreaController: Controlador que gestiona las operaciones relacionadas con las áreas, como la creación,
      actualización y eliminación de áreas.
    - PropertyController: Controlador que gestiona las operaciones relacionadas con las propiedades, como la creación,
      actualización y eliminación de propiedades.

#### 4.2.3.3. Application Layer

- Application Services:
    - AreaApplicationService: Servicio de aplicación que coordina las operaciones relacionadas con las áreas, como la
      creación, actualización y eliminación de áreas.
    - PropertyApplicationService: Servicio de aplicación que gestiona las operaciones relacionadas con las propiedades,
      como la creación, actualización y eliminación de propiedades.

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
    - AreaRepositoryImpl: Implementación concreta del repositorio de áreas que se encarga de la persistencia de las
      áreas en la base de datos.
    - PropertyRepositoryImpl: Implementación concreta del repositorio de propiedades que se encarga de la persistencia
      de las propiedades en la base de datos.

- External Services:
    - En este contexto, no se han identificado servicios externos específicos para las áreas y propiedades, pero podrían
      incluir servicios de almacenamiento de imágenes o integraciones con sistemas de mapeo si se requieren en el
      futuro.

#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams

Este diagrama proporciona una vista de la estructura de la arquitectura y cómo los diferentes componentes interactúan
dentro del aggregate Areas.
![Bounded Context C4 Areas](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/bc-c4-areas.jpeg)

#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams

#### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams

El diagrama UML del bounded context "Areas" ilustra las clases Area y Property con sus respectivos atributos y métodos.
En este contexto, Area representa las distintas áreas dentro de una propiedad, mientras que Property representa el
conjunto completo de estas áreas. Cada clase tiene atributos básicos como identificadores, nombres, y otras
características relevantes. Las clases también contienen métodos para crear, actualizar y eliminar instancias. La
relación entre Property y Area está representada mediante una composición, donde una propiedad contiene múltiples áreas,
lo que refuerza la relación de uno a muchos entre ambas clases.

ssss
![Bounded Context UML Areas](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/bc-uml-areas.png)

#### 4.2.3.6.2. Bounded Context Database Design Diagram

Este diagrama de base de datos representa las tablas y las relaciones dentro del bounded context "Areas". Se define la
tabla area, que almacena información sobre las áreas específicas donde se colocan dispositivos de seguridad, y la tabla
property, que representa una propiedad, la cual puede contener múltiples áreas. La relación entre estas dos entidades es
de uno a muchos, donde una propiedad puede tener varias áreas asociadas. Los atributos principales incluyen
identificadores únicos para cada entidad, nombres descriptivos, y detalles adicionales como iconos y colores para las
áreas, y direcciones para las propiedades.

![Bounded Context Database Areas](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/bc-db-areas.jpg)

### 4.2.4. Bounded Context: User context

El User Context abarca los procesos y funciones relacionados con la gestión del usuario y el rol que desempeña cada uno
dentro de nuestro sistema. Aquí podemos manejar la creación, modificación o eliminación del usuario de nuestro sistema,
asimismo podemos gestionar la asignación de roles.

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
    * Propósito: Representa los distintos roles que los usuarios puedan tener dentro del sistema para que determine los
      permisos y acciones que puedan realizar.
    * Atributos:
        * `id: string`: Identificador único del rol
        * `type: string`: Tipo del rol que podría desempeñar el usuario.
    * Relaciones:
        * `1...n` con User dado que un rol puede tener varios usuarios.

#### 4.2.4.1. Domain Layer

En la capa de dominio encontramos nuestras clases centrales como núcleo de nuestro sistema y las reglas de negocio que
incluyen lo siguiente:

* Entities:
    * User: Representa a un usuario del sistema y debe de ser único.
        * Atributos: id, firstname, lastname, email, password,phone, dni
    * Role: Representa el rol que desempeña el usuario dentro de la aplicación.
        * Atributos: id, type.

* Value Objects:
    * UserId: Identificador único de cada usuario
    * RoleId: Identificador único de cada rol asignado a un usuario
    * Password: Objeto de valor para manejar contraseñas seguras y encriptadas.
    * Email: Objeto de valor para manejar correos únicos por cada usuario.

* Aggregates:
    * UserAggregate: Es un agregado que incluye la entidad de usuario y los roles relacionados con ella. Además,
      encapsula a las reglas y lógica de negocio.

* Domain Services:
    * AuthenticationService: Puede ser incluido un servicio de dominio encargado de la autenticación del usuario

* Repositories:
    * UserRepository: Define los métodos para almacenar, modificar, eliminar y recuperar información de los usuarios en
      la base de datos
    * RoleRepository: Define los métodos para gestionar la persistencia de roles.

#### 4.2.4.2. Interface Layer

Aquí manejamos las interacciones y solicitudes entre el sistema y los usuarios y consigo devolviendo respuestas óptimas.
Para el Bounded Context de User tenemos lo siguiente:

* Controllers:
    * UserController: Se expone las operaciones relacionadas con el usuario como la creación, actualización, consulta y
      eliminación del usuario. Al crearse un usuario, este a su vez se le asigna un rol.
    * RoleController: Gestiona las peticiones relacionadas con la administración de roles, como la creación de nuevos
      roles o la modificación de roles existentes.

#### 4.2.4.3. Application Layer

Para esta capa definimos los flujos de negocios a través de clases de tipo Command Handlers y Event Handlers, asegurando
asi el manejo de las clases correctamente.

* Command Handlers:
    * CreateUserCommandHandler: Maneja la lógica de creación de nuevos usuarios, asegurándose que cada uno cumpla con
      todas las reglas de negocio, como validar el correo único y el cifrado de contraseñas
    * AssignRoleToUserCommandHandler: Gestiona la asignación de roles a los usuarios
* Event Handlers:
    * UserRegisteredEventHandler: Este handler puede enviar una notificación cuando un nuevo usuario es registrado
      exitosamente en el sistema

#### 4.2.4.4. Infrastructure Layer

En esta capa veremos las relaciones de nuestras clases con las conexiones a los servicios externos como las bases de
datos

**Repositories:**

* UserRepository: Implementación de la interfaz de repositorio para acceder a la base de datos que almacena la
  información de los usuarios.
* RoleRepository: Implementación de la interfaz de repositorio para gestionar la persistencia de roles a través de la
  base de datos.

**External Service:**

* MessageService: Servicio externo que se utiliza para enviar notificaciones a los usuarios en caso haya cambios en la
  aplicación móvil o una gestión de alarmas.

#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams

En esta parte presentaremos el Diagrama de componentes en el modelo C4, mostraremos la descomposición del container en
componentes y sus interacciones

#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams

##### 4.2.4.6.2. Bounded Context Database Design Diagram

En el diagrama de base de datos de usuario podemos ver la relación existente de las tablas dentro del bounded context "
User". Aquí definimos la tabla usuario, en el cual almacenamos información importante del usuario para que pueda
registrarse en la aplicación que a su vez está relacionada con un rol de usuario el cual asigna los permisos al sistema
dependiendo el rol que desempeñen dentro de nuestra aplicación dando conocer asi que un rol lo puede desempeñar varios
usuarios, pero un usuario tiene un único rol. Los atributos los cuales manejamos incluyen identificadores unicos para
cada entidad asi como detalles principales que debemos tener para la aplicación.

![Bounded Context Database User](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/database-user.png)

### 4.2.5. Bounded Context: Events context

El Event Context abarca los procesos y funciones relacionados con la gestión de los eventos y/o sucesos que puedan
ocurrir a través de nuestro sistema de alarma. Podemos manejar la creación o modificación de las alarmas según el
usuario lo crea conveniente.

1. Clase Events
    * Propósito: La clase Events representa a los eventos que puedan suceder por las alarmas puestas en nuestros.
    * Atributos:
        * `id: string`: Identificador único del evento
        * `title: string`: Título del suceso
        * `description: string`: Descripción del evento sucedido
        * `timestamp: string`: Hora en el cual sucedió el evento
    * Métodos:
        * `getEventDetails(): void` - Retorna los detalles importantes del evento para el registro correspondiente.
        * `registerEvent(): void` - Registro de un nuevo evento en el sistema
    * Relaciones:
        * `1...1` con Tipo de Evento, ya que un tipo de evento puede tener un evento que sucedió

2. Clase Events_type
    * Propósito: Representa los distintos roles que los usuarios puedan tener dentro del sistema para que determine los
      permisos y acciones que puedan realizar.
    * Atributos:
        * `id: string`: Identificador único del rol
        * `type: string`: Tipo del rol que podría desempeñar el usuario.
    * Relaciones:
        * `1...1` con Type dado que un evento puede tener un tipo de evento.

#### 4.2.4.1. Domain Layer

En la capa de dominio encontramos nuestras clases centrales como núcleo de nuestro sistema y las reglas de negocio que
incluyen lo siguiente:

* Entities:
    * Events: Representa a un evento que pudo ocurrir y capto nuestro sistema de seguridad.
        * Atributos: id, title, description, timestamp.
    * EventsType: Representa el tipo de evento que desempeña el evento dentro de la aplicación.
        * Atributos: id, type.

* Value Objects:
    * EventId: Identificador único de cada usuario
    * TypeEventId: Identificador único de cada rol asignado a un usuario.

* Aggregates:
    * EventsAggregate: Es un agregado que incluye la entidad de usuario y los roles relacionados con ella. Además,
      encapsula a las reglas y lógica de negocio.

* Domain Services:
    * MessageService: Puede ser incluido un servicio de dominio encargado de la notificación al usuario de un evento
      ocurrido.

* Repositories:
    * EventRepository: Define los métodos para almacenar, modificar, eliminar y recuperar información de los usuarios en
      la base de datos
    * EventTypeRepository: Define los métodos para gestionar la persistencia de roles.

#### 4.2.4.2. Interface Layer

Aquí manejamos las interacciones y solicitudes entre el sistema y los usuarios y consigo devolviendo respuestas óptimas.
Para el Bounded Context de Event tenemos lo siguiente:

* Controllers:
    * EventController: Se expone las operaciones relacionadas con el evento como la creación, actualización y consulta
      del evento. Al crearse un evento, este a su vez.
    * EventTypeController: Gestiona las peticiones relacionadas con la administración de tipos de eventos, como la
      creación de nuevos eventos o la modificación de eventos existentes.

#### 4.2.4.3. Application Layer

Para esta capa definimos los flujos de negocios a través de clases de tipo Command Handlers y Event Handlers, asegurando
asi el manejo de las clases correctamente.

* Command Handlers:
    * CreateEventCommandHandler: Maneja la lógica de creación de nuevos eventos, asegurándose que cada uno cumpla con
      todas las reglas de negocio.
    * AssignTypeToEventCommandHandler: Gestiona la asignación de tipos de eventos a los eventos
* Event Handlers:
    * EventRegisteredEventHandler: Este handler puede enviar una notificación cuando un nuevo evento está sucediendo.

#### 4.2.4.4. Infrastructure Layer

En esta capa veremos las relaciones de nuestras clases con las conexiones a los servicios externos como las bases de
datos

**Repositories:**

* EventRepository: Implementación de la interfaz de repositorio para acceder a la base de datos que almacena la
  información de los eventos.
* EvenTypeRepository: Implementación de la interfaz de repositorio para gestionar el tipo de evento a través de la base
  de datos.

**External Service:**

* MessageService: Servicio externo que se utiliza para enviar notificaciones a los usuarios en caso haya cambios en la
  gestión de alarmas.

#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams

En esta parte presentaremos el Diagrama de componentes en el modelo C4, mostraremos la descomposición del container en
componentes y sus interacciones

#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams

##### 4.2.4.6.2. Bounded Context Database Design Diagram

En el diagrama de base de datos de usuario podemos ver la relación existente de las tablas dentro del bounded context "
Event". Aquí definimos la tabla event, en el cual almacenamos información importante del evento o suceso que suceda en
el momento que pueda activarse una alarma, además esta está relacionado con un tipo de evento para una mejor gestión al
momento de registrar el evento ocurrido. Los atributos los cuales manejamos incluyen identificadores unicos para cada
entidad asi como detalles principales que debemos tener para la aplicación.

![Bounded Context Event](https://pub-9734af8385734c25a466d683cb2e6c2f.r2.dev/database%20event.png)

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