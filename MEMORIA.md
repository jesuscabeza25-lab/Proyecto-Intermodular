# Memoria del Proyecto Intermodular: PayClear

* Asignatura: Proyecto Intermodular
* Curso: 2º Desarrollo de Aplicaciones Multiplataforma (DAM)
  
---

# 1. INTRODUCCIÓN
## 1.1. Contexto del Proyecto
Hoy en día, la gestión de gastos compartidos es una necesidad habitual: ya sea para administrar las cuentas de un piso de estudiantes, organizar un viaje o planificar un evento en grupo. Aunque este tipo de situaciones cotidianas se ha digitalizado casi por completo, las herramientas actuales sigue presentando retos operativos para los usuarios.

Aprovechando esta realidad, y dentro del marco del ciclo de 2º de Desarrollo de Aplicaciones Multiplataforma (DAM), surge este proyecto intermodular. El objetivo es integrar de forma práctica los conocimiento0s adquiridos en las distintas asignaturas (Desarrollo de Interfaces, Programación Multimedia, Acceso a Datos) para construir una solución de software propia y eficiente. Para ello, el proyecto plantea una evolución tecnológica escalonada: partiendo de una primera versión funcional de escritorio, para culminar en el desarrollo de una aplicación móvil multiplataforma completa.

## 1.2. Problema o necesidad detectada
​Aunque ya existen aplicaciones muy famosas para dividir gastos (seguro que os suenan Splitwise o Tricount), la realidad es que usarlas se ha vuelto un poco desesperante últimamente. Nos hemos dado cuenta de que tienen varios problemas que frustran bastante al usuario:

* **Pérdida de tiempo y registros obligatorios:** Para anotar un simple gasto del supermercado tienes que crearte una cuenta, dar tu correo o tu teléfono. Corta mucho el rollo cuando solo quieres apuntar algo rápido.
* **Si no hay internet, no hay app:** La mayoría dependen de la nube. Si te vas de viaje rural o a un festival y la cobertura falla, no puedes usar la aplicación.
* **Publicidad y funciones de pago:** Las apps actuales te bombardean con anuncios molestos y te bloquean opciones básicas (como añadir más de "X" gastos al día) para obligarte a pagar una suscripción.
* **Lo que nos dijo la gente:** (METER AQUI DATOS DEL FORMULARIO)
* **Ejemplo:** "De hecho, en la encuesta que pasamos a numerosas personas, nos sorprendió ver que la queja principal era la publicidad y lo lentas que son para simplemente apuntar un gasto...."

### ​1.3. Propuesta de solución

​Para solucionar todo este lío, proponemos **PayClear**. Nuestra idea es crear una aplicación para gestionar deudas que vaya directa al grano, sin rodeos. Lo vamos a conseguir basándonos en estos puntos clave:

-   ​**100% Offline y privada (Local-First):** La app funciona en tu propio dispositivo. No necesitas internet, ni crearte un perfil, ni iniciar sesión. Abres la app y listo, los datos se quedan en tu móvil.
-   ​**Rápida y directa (Cero fricción):** Hemos diseñado la interfaz para que nadie se pierda. En un máximo de 2 clics tienes que poder registrar un ticket o ver cómo están las cuentas.
-   ​**Las cuentas claras de un vistazo:** Vamos a usar un sistema de colores muy visual. Si tu tarjeta sale en **verde**, te deben dinero; si sale en **rojo**, te toca pagar; y si sale en **gris**, estás a cero.
-   ​**Algoritmo inteligente de deudas:** Hemos programado un sistema (un algoritmo __Greedy__) que hace la "magia" matemática para que el grupo tenga que hacerse el menor número de Bizums o transferencias posibles para quedar en paz.
-   ​**Evolución del proyecto:** Empezaremos construyendo el programa para ordenador usando Java Swing (con su interfaz visual), y el objetivo final será migrarlo y lanzarlo como una aplicación móvil con Flutter.

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
