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
* **Segmento 1: Dueños de inmuebles**
   
2. **Entrevista N°2:** Diana Gomez Oré
 - Edad: 25 años
 - Distrito: Chorrillos
 - Timing: 9:35
 - Duración: 5:22
 - Link: <a href="https://upcedupe-my.sharepoint.com/:v:/g/personal/u202113876_upc_edu_pe/EXHqrhK5ujRBmGwX9MkluJUBF2d1Zprer7bJl0F41fEX1g?e=Hh8QaG&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifSwicGxheWJhY2tPcHRpb25zIjp7InN0YXJ0VGltZUluU2Vjb25kcyI6NTc0Ljc0fX0%3D" target="_blank"> Entrevista 2 </a>

![Interview 2](/src/images/interview-2.png)

Antes de la entrevista, Diana me comentó que se acaba de mudar sola hace aproximadamente 6 meses, por lo que el tema de seguridad es algo que le preocupa, debido a que deja su hogar solo cuando se va al trabajo. Además me comentó que ha investigado un poco sobre algunas opciones de empresas de seguridad, pero aún no se decide por alguna de ellas.

Durante la entrevista, Diana mencionó que no ha tenido problemas de seguridad aún, pero que toda la seguridad que tiene en su hogar es colocar llave al cerrar la puerta. Es por ello que le parece interesante y ve como opción a futuro el adquirir un sistema de seguridad. Para ella es muy importante que la empresa de seguridad le brinde la confianza y seguridad que requiere un servicio de esta índole, además de que se realicen mantenimientos cada cierto tiempo y que la atención al cliente en caso de dudas o fallos sea rápida. Ella considera que los dispositivos más importantes serían cámaras, sensores y un pinpad. Además, mencionó que ella preferiría ser alertada de algún intruso mediante una llamada, ya que la atendería con mayor rapidez que un mensaje o notificación. Sin embargo, dijo que no le molestaría recibir notificaciones referentes a la seguridad de su hogar. Por último, mencionó que ella prefiere gestionar el sistema de seguridd de su hogar mediante una aplicación, ya que de esa manera podría visualizar sus cámaras y estar al tanto de la situación de su hogar en todo momento.

También pude notar que Diana utiliza un celular con android y una laptop con Windows. Además, sus canales de comunicación son principalmente WhatsApp e Instagram. Su relación con la tecnología es bastante buena, debido a que en su trabajo están en constante capacitación, sobretodo para el uso de pc. Asimismo, está acostumbrada a utilizar browsers basados en chromium, tales como Chrome y Brave.

### 2.2.3. Análisis de entrevistas
## 2.3 Needfinding
### 2.3.1. User Personas
Las personas que se presentan a continuación son una representación de los segmentos de usuarios definidos, se han tomado en cuenta las características más relevantes de las entrevistas realizadas y el análisis de la competencia las cuales incluyen: edad, distrito, dispositivos tecnológicos que utilizan, canales de comunicación, relación con la tecnología, necesidades y preferencias.

- **Segmento 1: Dueños de inmuebles**
![user persona seg 1](/src/images/user-persona-seg1.png)

- **Segmento 2: Empresas de seguridad**
![user persona seg 2](/src/images/user-persona-empresa.png)

### 2.3.2. User Task Matrix

Los User Personas que se han definido son Seele Vollerei el cual representa al primer segmento, dueño de inmueble y José Ramirez para el segundo segmento, empresa de seguridad. A continuación, se presenta la matriz de tareas de los User Personas.

<table border="1">
  <thead>
    <tr>
      <th rowspan="2">Task</th>
      <th colspan="2">Seele Vollerei <br> (Dueño de inmueble)</th>
      <th colspan="2">José Ramirez <br> (Empresa de seguridad)</th>
    </tr>
    <tr>
      <th>Frecuencia</th>
      <th>Importancia</th>
      <th>Frecuencia</th>
      <th>Importancia</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Monitorización de cámaras en tiempo real</td>
      <td>Casi siempre</td>
      <td>Alta</td>
      <td>Siempre</td>
      <td>Alta</td>
    </tr>
    <tr>
      <td>Revisión de grabaciones de las cámaras</td>
      <td>A veces</td>
      <td>Media alta</td>
      <td>Siempre</td>
      <td>Alta</td>
    </tr>
    <tr>
      <td>Recepción de alertas en tiempo real</td>
      <td>Siempre</td>
      <td>Alta</td>
      <td>Siempre</td>
      <td>Alta</td>
    </tr>
    <tr>
      <td>Respuesta ante incidentes</td>
      <td>Rara vez</td>
      <td>Alta</td>
      <td>Siempre</td>
      <td>Alta</td>
    </tr>
    <tr>
      <td>Análisis de patrones de seguridad</td>
      <td>Pocas veces</td>
      <td>Alta</td>
      <td>Siempre</td>
      <td>Alta</td>
    </tr>
    <tr>
      <td>Realización de informes de actividad</td>
      <td>Casi nunca</td>
      <td>Baja</td>
      <td>Siempre</td>
      <td>Alta</td>
    </tr>
    <tr>
      <td>Instalación de nuevas cámaras y/o dispositivos IoT</td>
      <td>A veces</td>
      <td>Alta</td>
      <td>Rara vez (no es su rubro)</td>
      <td>Baja</td>
    </tr>
    <tr>
      <td>Configuración y mantenimiento de los dispositivos IoT y cámaras</td>
      <td>Casi siempre</td>
      <td>Alta</td>
      <td>Casi nunca</td>
      <td>Baja</td>
    </tr>
  </tbody>
</table>

Las tareas que se realizan con mayor frecuencia e importancia por parte de los User Personas son la monitorización de cámaras en tiempo real, la recepción de alertas en tiempo real y la revisión de las grabaciones. En cuanto a las diferencias, se puede observar que Seele Vollerei realiza la instalación de nuevas cámaras y/o dispositivos IoT, mientras que José Ramirez no lo hace, ya que no es su rubro. Por otro lado, las demás tareas coinciden en su importancia y frecuencia, aunque José Ramirez realiza la mayoría de tareas con mayor frecuencia que Seele Vollerei debido a que es su trabajo.

### 2.3.3. User Journey Mapping
### 2.3.4. Empathy Mapping
### 2.3.5. As-Is Scenario Mapping
## 2.4. Ubiquitous Language
