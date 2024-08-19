# CAPÍTULO I: INTRODUCTION
## 1.1 Startup Profile
### 1.1.1 Descripción de la Startup
### 1.1.2 Perfiles de integrantes del equipo
- **Elvia Guadalupe Arteaga Cruz:** Soy una estudiante de la carrera de ingeniería de software. Ingresé a la universidad para estudiar ingeniería mecatrónica, pero el mundo de la programación siempre me gustó más, es por ello que decidí cambiarme de carrera. Me gusta mucho la tecnología y las grandes cosas que se pueden hacer con ella. Tengo la ilusión de crear productos y servicios que ayuden a facilitar la vida de las personas y que nos ayuden a crecer como sociedad.
## 1.2 Solution Profile
### 1.2.1  Antecedentes y problemática
### 1.2.2 Lean UX Process
#### 1.2.2.1 Lean UX Problem Statements
**Domain:** Seguridad IoT para el hogar

**Customer Segments:**

1. **Usuarios Residenciales:** Personas que buscan proteger sus viviendas mediante sistemas de seguridad.
2. **Empresas de Seguridad:** Compañías encargadas de responder a emergencias activadas por alarmas de seguridad.
3. **Empresas de Instalación y Mantenimiento:** Proveedores que instalan, mantienen y gestionan dispositivos de seguridad en viviendas.

**Pain Points:**

**1. Usuarios Residenciales:**

- **Acceso Limitado a Información:** Dificultad para obtener datos en tiempo real sobre el estado de los dispositivos y acceder a imágenes en vivo o grabaciones pasadas.
- **Falta de Control Centralizado:** Necesidad de gestionar múltiples dispositivos y aplicaciones, lo que resulta en una experiencia de usuario fragmentada.
- **Respuesta Lenta en Emergencias:** La integración con las empresas de seguridad puede ser lenta, afectando la rapidez en la gestión de incidentes.

**2. Empresas de Seguridad:**

- **Falta de Información en Tiempo Real:** Limitaciones para acceder a datos cruciales durante emergencias, afectando la toma de decisiones.
- **Coordinación Ineficiente:** Dificultades para coordinarse con los usuarios en la gestión de alertas y respuesta a incidentes.

**3. Empresas de Instalación y Mantenimiento:**

- **Gestión del Mantenimiento:** Dificultad para rastrear el estado de los dispositivos y coordinar las tareas de mantenimiento preventivo y correctivo.
- **Notificación de Fallos:** Falta de un sistema efectivo para recibir alertas sobre fallos en los dispositivos o necesidades de instalación.

**Gap:**

Actualmente, los sistemas de seguridad disponibles no integran eficazmente la gestión de dispositivos, la respuesta a emergencias y la administración del mantenimiento en una plataforma unificada. Además, la principal empresa competidora no tiene una alianza con una empresa de seguridad y solo llama a la policía nacional en caso de alertas, lo que puede resultar en una respuesta menos especializada y menos eficiente en comparación con un equipo de seguridad propio o aliado. Esto representa una oportunidad para ofrecer una solución más completa y eficiente.

**Visión/Estrategia:**

Desarrollar una solución de seguridad IoT innovadora que integre dispositivos de seguridad con una interfaz unificada y fácil de usar, mejorando la gestión en tiempo real, la coordinación en emergencias y la eficiencia en el mantenimiento. La estrategia incluye formar alianzas con empresas de seguridad para proporcionar una respuesta más eficaz y especializada, y ofrecer una plataforma que permita a los usuarios residenciales, empresas de seguridad y empresas de mantenimiento operar de manera más eficiente.

**Initial Segment:**

El segmento inicial será ***Usuarios Residenciales***, ya que estos son los clientes finales que utilizarán el sistema de seguridad de manera directa. Su experiencia y satisfacción con la plataforma serán fundamentales para establecer la aceptación y adopción del producto. La solución debe abordar sus necesidades de acceso a información en tiempo real, gestión centralizada de dispositivos y respuesta rápida a incidentes, destacando la ventaja competitiva de contar con una alianza con empresas de seguridad.

#### 1.2.2.2 Lean UX Assumptions
**Suposiciones sobre los Usuarios y sus Necesidades:**

- Los usuarios residenciales valoran un sistema de seguridad intuitivo que les permita monitorear y controlar dispositivos desde cualquier lugar.
- Las empresas de seguridad necesitan acceso instantáneo a datos relevantes para responder eficazmente a emergencias.
- Las empresas de mantenimiento requieren notificaciones automáticas sobre fallos y necesidades de mantenimiento para gestionar el mantenimiento de forma proactiva.

**Suposiciones sobre el Comportamiento de los Dispositivos:**

- Los dispositivos de seguridad funcionarán de manera confiable con conectividad Wi-Fi.
- Las actualizaciones de firmware podrán realizarse de forma automática y remota sin interrumpir el servicio.
- Las baterías de respaldo serán adecuadas para mantener el funcionamiento durante cortes de energía.

**Suposiciones sobre la Tecnología Utilizada:**

- Wi-Fi proporcionará una conectividad adecuada y estable entre los dispositivos y las aplicaciones.
- AWS ofrecerá una solución segura y escalable para el almacenamiento en la nube.
- La arquitectura basada en microservicios permitirá escalar el sistema de manera eficiente.

**Suposiciones sobre la Experiencia del Usuario:**

- Los usuarios prefieren una interfaz simple y directa para la gestión de dispositivos.
- Las notificaciones push y alertas automáticas serán eficaces para mantener a los usuarios informados sobre eventos importantes.
- La integración de funcionalidades en una única aplicación mejorará la experiencia del usuario.

#### 1.2.2.3 Lean UX Hypothesis Statements

1. **Facilidad de Uso:**
- ***Hipótesis:*** Creemos que si la interfaz de usuario es intuitiva y fácil de usar, entonces los usuarios residenciales estarán más satisfechos y serán más propensos a adoptar y utilizar el sistema de manera continua.
- **Validación:** Sabremos que estamos en lo correcto cuando veamos la siguiente retroalimentación del mercado:
  - *Retroalimentación Cualitativa:* Comentarios positivos de los usuarios sobre la facilidad de navegación y la gestión de dispositivos durante las pruebas de usabilidad.
  - *Retroalimentación Cuantitativa:* Altas tasas de adopción de usuarios y bajas tasas de deserción en las métricas de participación de usuarios.
  - *Cambio en el Indicador Clave de Rendimiento:* Mejora en los puntajes de satisfacción del usuario y una disminución en las solicitudes de soporte relacionadas con problemas de usabilidad.

2. **Acceso a Datos en Tiempo Real:**

- ***Hipótesis:*** Creemos que si las empresas de seguridad tienen acceso inmediato a datos relevantes como imágenes de cámaras y alertas, entonces su eficacia para responder a emergencias mejorará significativamente.
- ***Validación:*** Sabremos que estamos en lo correcto cuando veamos la siguiente retroalimentación del mercado:
  - *Retroalimentación Cualitativa:* Comentarios positivos de las empresas de seguridad sobre la mejora en la toma de decisiones y en los tiempos de respuesta.
  - *Retroalimentación Cuantitativa:* Reducción en los tiempos de respuesta a incidentes en comparación con sistemas que no tienen acceso a datos en tiempo real.
  -  *Cambio en el Indicador Clave de Rendimiento:* Mejora en los métricas de eficacia en la respuesta a emergencias y tiempos de resolución más rápidos.

3. **Notificaciones y Alertas Automáticas:**

- ***Hipótesis:*** Creemos que si las empresas de instalación y mantenimiento reciben notificaciones automáticas sobre fallos en los dispositivos y necesidades de mantenimiento, entonces podrán gestionar el mantenimiento de manera más proactiva y eficiente.
- ***Validación:*** Sabremos que estamos en lo correcto cuando veamos la siguiente retroalimentación del mercado:
  - *Retroalimentación Cualitativa:* Comentarios positivos de las empresas de mantenimiento sobre la eficiencia y la puntualidad en la programación del mantenimiento y la resolución de problemas.
  - *Retroalimentación Cuantitativa:* Disminución en los tiempos de respuesta a problemas de mantenimiento y mayor tasa de acciones proactivas de mantenimiento.
  - *Cambio en el Indicador Clave de Rendimiento:* Aumento en la efectividad de las operaciones de mantenimiento y reducción en el tiempo de inactividad de los dispositivos.

4. **Wi-Fi como Tecnología:**

- ***Hipótesis:*** Creemos que si el sistema utiliza Wi-Fi como tecnología de comunicación, entonces la confiabilidad del sistema dependerá de la calidad y estabilidad de la red Wi-Fi, lo que afectará la experiencia del usuario.
- ***Validación:*** Sabremos que estamos en lo correcto cuando veamos la siguiente retroalimentación del mercado:
  - *Retroalimentación Cualitativa:* Comentarios de los usuarios sobre problemas de conectividad o satisfacción con el rendimiento del sistema basado en la calidad del Wi-Fi.
  - *Retroalimentación Cuantitativa:* Frecuencia de problemas de conectividad reportados por los usuarios.
  - *Cambio en el Indicador Clave de Rendimiento:* Mejora en las métricas de confiabilidad del sistema y en los puntajes de satisfacción del usuario relacionados con la conectividad.

5. **Almacenamiento en AWS:**

- ***Hipótesis:*** Creemos que usar AWS para el almacenamiento en la nube de datos de video garantizará una alta seguridad y disponibilidad de los datos debido a las características avanzadas de seguridad e infraestructura confiable de AWS.
- ***Validación:*** Sabremos que estamos en lo correcto cuando veamos la siguiente retroalimentación del mercado:
  - *Retroalimentación Cualitativa:* Comentarios positivos sobre la seguridad y disponibilidad de los datos por parte de los usuarios.
  - *Retroalimentación Cuantitativa:* Baja incidencia de pérdida de datos o problemas de acceso reportados.
  - *Cambio en el Indicador Clave de Rendimiento:* Altas tasas de disponibilidad y sólidos resultados en auditorías de seguridad.

#### 1.2.2.4 Lean UX Canvas
![Lean UX Canvas](/images/lean-ux-canvas.jpg)
## 1.3 Segmentos objetivo
# CAPÍTULO II: REQUERIMENTS ELICITATION & ANALYSIS
# CAPÍTULO III: REQUERIMENTS SPECIFICATION
# CAPÍTULO IV: SOLUTION SOFTWARE DESIGN