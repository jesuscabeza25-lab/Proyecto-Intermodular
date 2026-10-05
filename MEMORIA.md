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
| **Lógica Contable y Algoritmia** | Centralizar los balances en una única fuente  (`Grupo`) e integrar algoritmo que simplifique la liquidación de deudas en un máximo de 1 transferencias directas. |
| **Arquitectura de Software (MVC)** | Implementar el patrón Modelo-Vista-Controlador (MVC) en Java Swing, desacoplando la representación gráfica de las reglas contables y centralizando los eventos en `ControladorPrincipal`. |
| **Persistencia y Seguridad (Local-First)** | Garantizar operatividad 100% offline y privacidad total mediante almacenamiento en local, acceso protegido por contraseña (SHA-256) y copias de seguridad portables en JSON. |
| **Multiplataforma y Metodología** | Desarrollar la versión de escritorio en Java Swing como base desacoplada para la futura extensión móvil con Flutter, gestionando el ciclo con Scrum y Sprints. |

## 1.5. Alcance del proyecto

El alcance global de PayClear contempla el ciclo de vida completo de esta aplicacion, cubriendo tanto sus funcionalidades como los objetivos para este primer sprint.

* **Registro inmediato de los gastos:** Entrada rapida de los datos, indicando concepto, importe y quien paga en la menor cantidad de clics posibles.
* **Pantalla de balances:** Pantalla donde ver en tiempo real el estado de cada cuenta individualmente mediante un sistema de señalizacion con colores (verde/rojo/gris) e historial de movimientos.
* **Liquidación multilateral optimizada:** Integracion de un algoritmo que simplifica las deudas al mínimo numero de transferencias directas entre integrantes.
* **Calculadora de reparto rapido:** Overlay para dividir cenas, compras, peajes... De manera equitativa y personalizada sin abandonar la pantalla principal.

---

> **Enfoque específico del Sprint 1:**  
> Ideación, análisis de mercado (benchmarking), prototipado de alta fidelidad navegable en Figma, definición del Backlog y especificación técnica de la arquitectura de clases y componentes.
