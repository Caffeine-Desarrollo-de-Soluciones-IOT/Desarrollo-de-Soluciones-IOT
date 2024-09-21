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

# Capítulo IV: Solution Software Design
## 4.1. Strategic-Level Domain-Driven Design
### 4.1.1. EventStorming
#### 4.1.1.1 Candidate Context Discovery
#### 4.1.1.2 Domain Message Flows Modeling
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