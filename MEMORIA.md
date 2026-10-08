# Memoria del Proyecto Intermodular: PayClear

* Asignatura: Proyecto Intermodular
* Curso: 2º Desarrollo de Aplicaciones Multiplataforma (DAM)
  
COEVALUACIÓN SPRINT 1:

| Integrante | Nota (%) |
| :--- | :--- |
| Guillermo Eugui | 100% |
| Jesús Cabeza | 100% | 
| JoseLuís Segura | 95% |

---

# 1. INTRODUCCIÓN
## 1.1. Contexto del proyecto
En la actualidad, la gestión compartida de gastos en entornos cotidianos —como el reparto de facturas en un piso de estudiantes, el saldo de cuentas durante un viaje o la organización de un evento grupal— constituye una necesidad recurrente en la sociedad digitalizada. Sin embargo, el panorama tecnológico actual presenta una fuerte dicotomía en las empresas del sector fintech y de software de productividad personal:

* **Empresas SaaS Corporativas / Modelos Freemium (ej. Splitwise, Tricount / Topptip, Revolut Group Split):** Son organizaciones consolidadas orientadas al beneficio masivo. Su infraestructura depende de servidores centralizados en la nube, lo que genera elevados costes fijos de mantenimiento. Para sostener su estructura organizativa, estas empresas recurren a la monetización agresiva mediante muros de pago (paywalls), restricciones artificiales en el número de registros diarios de gastos, bombardeo publicitario en la interfaz y la recopilación de datos de comportamiento del usuario para la venta de perfiles publicitarios.

* **Soluciones Open Source / Utilidades Privadas (ej. IHavePaid, Bitcharge):** Son desarrollos independientes o de comunidades reducidas centrados en la privacidad. Aunque eliminan los costes de servidores y la publicidad, suelen carecer de una experiencia de usuario (UX) cuidada, ofrecen interfaces arcaicas y carecen de soporte multiplataforma estructurado.

En este marco surge PayClear, un proyecto desarrollado en el ciclo formativo de grado superior en Desarrollo de Aplicaciones Multiplataforma (DAM). PayClear se posiciona en el espacio intermedio del sector: un software con arquitectura Local-First (local por diseño) que elimina los costes de infraestructura en la nube y los intermediarios corporativos, combinando la usabilidad de las aplicaciones comerciales de primer nivel con la privacidad, gratuidad e inmediatez del software libre.

## 1.2. Problema o necesidad detectada
A pesar de la popularidad de las herramientas comerciales para la gestión de deudas, el modelo de negocio de estas plataformas ha terminado por degradar la experiencia de uso. Con el fin de validar científicamente esta problemática antes de iniciar el desarrollo técnico, el equipo realizó un estudio de mercado mediante una encuesta pública a un total de 14 usuarios del perfil objetivo (estudiantes, compañeros de piso y colectivos habituales).

### Datos empíricos extraídos del estudio de mercado:

-   **Frecuencia de necesidad:** El **57,1%** de los encuestados comparte gastos grupales varias veces por semana y un **21,4%** lo hace de forma puntual en viajes o eventos, confirmando la alta recurrencia del problema.
-   **Abandono de apps comerciales:** Un abrumador **92,9%** de los usuarios recurre a la memoria o a transferencias directas por Bizum y el **21,4%** utiliza notas de móvil o WhatsApp debido a la fricción de las apps actuales. Ningún usuario encuestado utiliza Splitwise como herramienta principal.
-   **Grado de frustración con las limitaciones:** El **50%** de los usuarios expresa una molestia alta o extrema (puntuaciones de 4 y 5 sobre 5) respecto a los límites diarios de gastos, la publicidad abusiva y las suscripciones de pago.
-   **Factores determinantes para la adopción:** El **78,6%** exige una aplicación 100% gratuita y sin límites de registro; el **42,9%** rechaza obligatoriamente tener que registrarse con correo o crear cuenta; el **42,9%** demanda una calculadora rápida para desglosar tickets; y el **28,6%** valora de forma prioritaria el funcionamiento 100% offline.
-   **Preferencia de plataforma:** El **42,9%** prefiere una solución híbrida (móvil pero con versión de escritorio para gestionar cuentas complejas con comodidad) y un **35,7%** prefiere únicamente móvil.
-   **Demandas cualitativas de los usuarios:** Rapidez de uso, privacidad total sin control externo sobre pequeños gastos cotidianos y un reparto justo sin micropagos invasivos.

  

### Análisis de la problemática según la estructura organizativa de las soluciones actuales:

Los hallazgos del formulario reflejan deficiencias estructurales en las distintas áreas operativas de las empresas del sector:

1.  **Departamento de Producto y UI/UX:** Prioriza los intereses de monetización sobre la usabilidad, saturando la pantalla de banners publicitarios y obligando al usuario a realizar múltiples clics o pasar por pantallas de registro antes de anotar un simple gasto.
2.  **Departamento de Infraestructura y Sistemas (Backend):** La insistencia en centralizar las bases de datos en la nube genera una dependencia absoluta de la conexión a internet y obliga a repercutir costes de mantenimiento al usuario mediante suscripciones *Pro*.
3.  **Departamento Legal y de Protección de Datos:** La exigencia de correos electrónicos, números de teléfono y la monitorización de hábitos de consumo vulnera el principio de minimización de datos del RGPD, generando desconfianza en los usuarios sobre el tratamiento de sus finanzas personales.


## 1.3. Propuesta de solución

PayClear responde a las necesidades detectadas mediante una aplicación de gestión de gastos compartidos centrada en la eficiencia, la privacidad y la agilidad de uso.

Los principales pilares de la solución son:

-   **Arquitectura Local-First y privacidad:** en la fase inicial, los datos se almacenarán localmente en el dispositivo mediante ficheros JSON, permitiendo el funcionamiento sin conexión a Internet y reduciendo la exposición de información personal a servicios externos.
-   **Cero fricción en la UI/UX:** se plantea una interfaz de ventana única que facilite el registro de gastos y la consulta del estado global del grupo con el menor número posible de pasos.
-   **Calculadora de reparto rápido:** se incorpora una funcionalidad específica para dividir tickets y compras colectivas entre varios participantes de forma rápida, tanto a partes iguales como mediante cantidades personalizadas.
-   **Simplificación de la liquidación:** se utilizará un algoritmo de liquidación basado en una estrategia voraz para reducir el número de transferencias necesarias entre acreedores y deudores.
-   **Evolución tecnológica escalonada:** la primera implementación prevista será una aplicación de escritorio en Java Swing siguiendo el patrón MVC, dejando preparada la arquitectura para una futura extensión móvil mediante Flutter.

### Oportunidades de negocio previsibles

Aunque el proyecto se plantea inicialmente como una solución gratuita de uso personal, se identifican posibles vías futuras de explotación, entre ellas:

-   Adaptaciones de marca blanca para organizaciones que gestionen grupos de usuarios.
-   Servicios opcionales de respaldo o sincronización respetando los requisitos de privacidad.
-   Servicios de soporte, mantenimiento o financiación mediante aportaciones de usuarios y organizaciones.

### Tipo de proyecto requerido

Para responder a las necesidades detectadas se requiere un proyecto de software multiplataforma con una arquitectura desacoplada, orientada al funcionamiento local, la persistencia sin conexión y una experiencia de usuario sencilla e inmediata.


# 1.4. Objetivos del proyecto.

## 1.4.1. Objetivo general

> Desarrollar una aplicación de software movil y de escritorio orientada a la gestión y liquidación eficaz de los gastos compartidos en grupos cotidianos (pisos compartidos, viajes y eventos sociales... etc), eliminando la fricción y los conflictos económicos que se generan entre convivientes mediante un sistema *Local-First* privado, rapido y respaldado por una optimización algorítmica que simplifica al máximo las transferencias necesarias para saldar las cuentas.

## 1.4.2. Objetivos específicos

| Área de Trabajo | Objetivo Específico |
| :--- | :--- |
| **Diseño y Usabilidad (UI/UX)** | Diseñar una interfaz en ventana única orientada a tareas que integre el componente reutilizable `TarjetaSaldoParticipante` con semáforo cromático automático (verde para acreedor, rojo para deudor y gris para saldado). |
| **Lógica Contable y Algoritmia** | Centralizar los balances en una única fuente  (`Grupo`) e integrar algoritmo que simplifique la liquidación de deudas en un máximo de n - 1 transferencias directas. |
| **Arquitectura de Software (MVC)** | Implementar el patrón Modelo-Vista-Controlador (MVC) en Java Swing, desacoplando la representación gráfica de las reglas contables y centralizando los eventos en `ControladorPrincipal`. |
| **Persistencia y Seguridad (Local-First)** | Garantizar operatividad 100% offline y privacidad total mediante almacenamiento en local, acceso protegido por contraseña (SHA-256) y copias de seguridad portables en JSON. |
| **Multiplataforma y Metodología** | Desarrollar la versión de escritorio en Java Swing como base desacoplada para la futura extensión móvil con Flutter, gestionando el ciclo con Scrum y Sprints. |

---

## 1.5. Alcance del proyecto

El alcance global de PayClear cubre el ciclo de vida completo del producto y su desarrollo evolutivo por fases, delimitando de forma clara lo que se implementa en esta primera entrega frente a lo proyectado para el resto del curso.

### 1.5.1. Ciclo de vida y fases de evolución de la aplicación
La solución se desarrolla siguiendo un modelo incremental distribuido en tres fases tecnológicas:
1. **Fase 1: Prototipado, Ideación y Arquitectura (Fase actual - Sprint 1):** Análisis de mercado, prototipado navegable de alta fidelidad en Figma, definición de la arquitectura MVC y estructuración del backlog. En este ciclo no se escribira codigo fuente en Java.
2. **Fase 2: Versión de Escritorio (Java Swing):** Implementación del entorno de escritorio usando el diseñador visual de NetBeans, codificación de la lógica de la calculadora y organizacion del proyecto mediante "MVC".
3. **Fase 3: Expansión Móvil (Flutter):** Llevar lo hecho en escritorio a una aplicacion movil contando con el ya mencionado local-first sin servidores externos.

---

### 1.5.2. Contextualización de funcionalidades previstas y prototipo
Cada pantalla y función responde a una necesidad concreta detectada en las alternativas comerciales:

* **Pantalla principal y balances:**
  * *Por qué se hace y qué nos llevó a ella:* En herramientas como Splitwise los balances están escondidos tras varios menús. Hacía falta ver de golpe la situación económica del grupo.
  * *Función esperada:* Ventana única que lista los miembros y aplica un código de colores automático con el componente `TarjetaSaldoParticipante`: verde para quien cobra, rojo para quien debe y gris para saldo a cero.
  
  ![Pantalla de balances](https://github.com/jesuscabeza25-lab/Desarrollo-de-Interfaz/blob/main/img/pantalla%20de%20deudas%20pendientes%20y%20saldadas.png?raw=true)

* **Calculadora de reparto rápido (modal overlay):**
  * *Por qué se hace y qué nos llevó a ella:* Al pagar cuentas o compras conjuntas se pierde tiempo echando cálculos a mano o repartiendo picos sueltos.
  * *Función esperada:* Ventana modal emergente que permite meter el importe del ticket y elegir quiénes participan para repartir el gasto a partes iguales o personalizadas sin cerrar la pantalla principal.
  
  ![Calculadora Modal](https://github.com/jesuscabeza25-lab/Desarrollo-de-Interfaz/blob/main/img/Calculadora.png?raw=true)

* **Liquidación multilateral optimizada (Algoritmo Voraz):**
  * *Por qué se hace y qué nos llevó a ella:* En grupos con muchos gastos cruzados se generan multitud de micropagos cruzados entre amigos.
  * *Función esperada:* Un algoritmo voraz analiza los balances en el propio equipo y cruza las deudas directamente entre el mayor deudor y el mayor acreedor, liquidando el grupo en un máximo de $n - 1$ transferencias simples.

* **Acceso al grupo local:**
  * *Por qué se hace y qué nos llevó a ella:* Pedir usuario, contraseña o email es la principal molestia al usar apps comerciales.
  * *Función esperada:* Acceso directo para abrir o crear el archivo del grupo de gastos en el equipo sin necesidad de internet ni registro en servidores.
  
  ![Acceso al grupo local](https://github.com/jesuscabeza25-lab/Desarrollo-de-Interfaz/blob/main/img/Iniciar%20sesion.png?raw=true)

---

### 1.5.3. Delimitación específica del Sprint 1
En cumplimiento con los requerimientos del primer sprint para esta entrega:
* El alcance práctico se limita al diseño del prototipo interactivo en Figma con sus transiciones y modales.
* No se incluye codificación en Java Swing para este sprint.
* Se entrega la planificación en GitHub Projects (Product y Sprint Backlog) y la especificación conceptual de la arquitectura MVC.


---

## 1.6. Limitaciones y Marco Normativo

### 1.6.1. Limitaciones y exclusiones técnicas
* **Sin pasarelas de pago bancarias:** PayClear calcula y optimiza los repartos matemáticos, pero no procesa dinero real (no conecta con Bizum o bancos) para no requerir licencias financieras. Los pagos los realizan los usuarios por su cuenta.
* **Sin backend ni nube:** La app es 100% *Local-First*. Guarda todo en el equipo del usuario para que funcione sin internet y garantice la privacidad de los datos.
* **Moneda única inicial (Euro):** Operamos con el euro local para evitar consultar tipos de cambio mediante APIs externas que romperían el modo sin conexión.

---

### 1.6.2. Marco fiscal y laboral 
Ante un lanzamiento comercial en España, el proyecto se encuadra en la legislación laboral y tributaria vigente:

* **Obligaciones fiscales (Hacienda):**
  * **IAE (Epígrafe 763):** Código censal de Hacienda correspondiente a *Programadores y Analistas de Informática*, necesario para facturar desarrollo y licencias de software.
  * **IVA (Modelo 303 y 390):** Aplicación del 21% de IVA en la venta o servicios del software. Se liquida cada tres meses ante la Agencia Tributaria con el **Modelo 303** y se presenta su resumen anual con el **Modelo 390**.
* **Marco laboral (Convenio Colectivo):**
  * Aplicación del **Convenio Colectivo Estatal TIC** (Tecnologías de la Información y Consultoría), que establece los sueldos mínimos, las categorías del equipo (programador, diseñador UI/UX) y un límite máximo de jornada de 1.800 horas anuales.

---

### 1.6.3. Prevención de Riesgos Laborales - PRL 
* **Normativa (Real Decreto 488/1997):** Regula la salud laboral en puestos de trabajo frente a **Pantallas de Visualización de Datos (PVD)**.
* **Aplicación en el proyecto:**
  * *Fatiga visual:* Diseñar la interfaz con contrastes cromáticos legibles y adaptar el brillo en las pantallas de trabajo.
  * *Ergonomía física:* Uso de puestos de trabajo con soporte lumbar regulable, distancia de 40 a 70 cm a la pantalla y pausas activas para evitar lesiones por estar sentados.

---

### 1.6.4. Financiación y ayudas públicas 
Vías de apoyo público del Estado para sustentar el desarrollo técnico y la posterior versión móvil:
* **ENISA Jóvenes Emprendedores:** Préstamos del Ministerio de Industria dirigidos a proyectos tecnológicos impulsados por menores de 40 años, sin exigir avales personales.
* **Programa Kit Digital:** Subvenciones de los Fondos Europeos Next Generation para la implantación de herramientas digitales de gestión.
* **Neotec (CDTI):** Financiación a fondo perdido para empresas emergentes que creen tecnología e innovación algorítmica propia.ç

---

## 1.7. Estructura de la memoria

| Capítulo | Contenido Proyectado y Enfoque en PayClear |
| :--- | :--- |
| **1. Introducción y Contexto** | Justificación del proyecto, detección del problema en soluciones de mercado, propuesta de valor Local-First, objetivos (general y específicos), alcance y delimitación del Sprint 1. |
| **2. Planificación y Gestión Ágil** | Organización metodológica bajo Scrum: gestión de artefactos (Product Backlog y Sprint Backlog), roles del equipo y control de versiones en GitHub. |
| **3. Análisis de Requisitos y Viabilidad** | Estudio de viabilidad técnica y operativa, resultados de la validación empírica con usuarios, especificación de requisitos funcionales (casos de uso) y no funcionales (rendimiento *offline*, privacidad). |
| **4. Diseño del Sistema y Arquitectura** | Modelado arquitectónico bajo el patrón MVC, diseño del catálogo formal de clases y entidades (`Grupo`, `Participante`, `Gasto`), prototipado UI/UX en Figma y diseño modular de componentes Swing. |
| **5. Desarrollo e Implementación** | Codificación del núcleo de la aplicación: lógica contable en Java, integración de la heurística voraz de simplificación de deudas, desarrollo del componente visual `TarjetaSaldoParticipante` y motor de persistencia local en JSON con hash SHA-256. |
| **6. Pruebas y Control de Calidad (QA)** | Batería de pruebas unitarias con JUnit sobre el modelo de balances y el algoritmo de reparto, pruebas de interfaz gráfica y validación de escenarios límite (entradas erróneas y redondeos). |
| **7. Empaquetado y Despliegue** | Generación del ejecutable distribuible de escritorio (.jar) con sus dependencias y especificación de los requisitos de entorno para su ejecución multiplataforma. |
| **8. Manuales de Usuario y Técnico** | Guía visual de uso paso a paso para el usuario final y documentación técnica para desarrolladores (estructura del código, dependencias y ciclo de vida de los eventos). |
| **9. Evolución del Proyecto (Fase Móvil)** | Hoja de ruta para la traslación del modelo hacia dispositivos móviles: análisis de arquitectura reactiva en Flutter y reutilización de la lógica contable establecida en escritorio. |
| **10. Conclusiones y Líneas Futuras** | Balance global del proyecto, grado de consecución de objetivos, dificultades técnicas superadas y planificación de futuras extensiones. |
