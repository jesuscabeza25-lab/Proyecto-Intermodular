# Memoria del Proyecto Intermodular: PayClear

* Asignatura: Proyecto Intermodular
* Curso: 2º Desarrollo de Aplicaciones Multiplataforma (DAM)
  
---

# 1. INTRODUCCIÓN
## 1.1. Contexto del Proyecto
Hoy en día, la gestión de gastos compartidos es una necesidad habitual: ya sea para administrar las cuentas de un piso de estudiantes, organizar un viaje o planificar un evento en grupo. Aunque este tipo de situaciones cotidianas se ha digitalizado casi por completo, las herramientas actuales sigue presentando retos operativos para los usuarios.

Aprovechando esta realidad, y dentro del marco del ciclo de 2º de Desarrollo de Aplicaciones Multiplataforma (DAM), surge este proyecto intermodular. El objetivo es integrar de forma práctica los conocimiento0s adquiridos en las distintas asignaturas (Desarrollo de Interfaces, Programación Multimedia, Acceso a Datos) para construir una solución de software propia y eficiente. Para ello, el proyecto plantea una evolución tecnológica escalonada: partiendo de una primera versión funcional de escritorio, para culminar en el desarrollo de una aplicación móvil multiplataforma completa.

### ​1.3. Propuesta de solución

​Para solucionar todo este lío, proponemos **PayClear**. Nuestra idea es crear una aplicación para gestionar deudas que vaya directa al grano, sin rodeos. Lo vamos a conseguir basándonos en estos puntos clave:

-   ​**100% Offline y privada (Local-First):** La app funciona en tu propio dispositivo. No necesitas internet, ni crearte un perfil, ni iniciar sesión. Abres la app y listo, los datos se quedan en tu móvil.
-   ​**Rápida y directa (Cero fricción):** Hemos diseñado la interfaz para que nadie se pierda. En un máximo de 2 clics tienes que poder registrar un ticket o ver cómo están las cuentas.
-   ​**Las cuentas claras de un vistazo:** Vamos a usar un sistema de colores muy visual. Si tu tarjeta sale en **verde**, te deben dinero; si sale en **rojo**, te toca pagar; y si sale en **gris**, estás a cero.
-   ​**Algoritmo inteligente de deudas:** Hemos programado un sistema (un algoritmo __Greedy__) que hace la "magia" matemática para que el grupo tenga que hacerse el menor número de Bizums o transferencias posibles para quedar en paz.
-   ​**Evolución del proyecto:** Empezaremos construyendo el programa para ordenador usando Java Swing (con su interfaz visual), y el objetivo final será migrarlo y lanzarlo como una aplicación móvil con Flutter.

# 1.4. Objetivos del proyecto.

## 1.4.1. Objetivo general

> Desarrollar una solución que sea multiplataforma y diseñada para poder eliminar la fricción y el desgaste diario al compartir gastos en pisos compartidos, viajes o simplemente quedadas en bares, permitiendo así registrar movimientos, desglosar compras y simplificar deudas pendientes de forma transparente, equitativa y sobretodo rápidamente.

Tenemos 4 pilares fundamentales:

* **Eliminación de los conflictos sociales:** Queremos quitar las tensiones y malentendidos económicos habituales que surgen al convivir en grupo, mediante una visualización limpia de los balances, sustituyendo los cálculos manuales y las conversaciones incómodas por una liquidación matemática clara.

* **Privacidad y autonomía total (*Local-First*):** Queremos dar una herramienta totalmente funcional offline, donde los datos financieros residan exclusivamente en el dispositivo del usuario, sin registros obligatorios, servidores intermedios ni monetización invasiva y la posibilidad de bloquear la aplicación con contraseña o datos biométricos.

* **Compensación inteligente de deudas:** Queremos introducir algoritmos optimizados que resuelvan saldos cruzados reduciendo drásticamente el número de transferencias o bizums necesarios, transformando así repartos complejos en pagos sencillos y faciles.

* **Experiencia de usuario accesible y directa:** Queremos crear interfaz limpia e intuitiva que permita registrar un apunte o consultar la posición deudora en dos pasos, que cualquiera pueda utilizar la aplicación.

# 1.4. Objetivos del proyecto.

## 1.4.1. Objetivo general

> Desarrollar una solución que sea multiplataforma y diseñada para poder eliminar la fricción y el desgaste diario al compartir gastos en pisos compartidos, viajes o simplemente quedadas en bares, permitiendo así registrar movimientos, desglosar compras y simplificar deudas pendientes de forma transparente, equitativa y sobretodo rápidamente.

Tenemos 4 pilares fundamentales:

* **Eliminación de los conflictos sociales:** Queremos quitar las tensiones y malentendidos económicos habituales que surgen al convivir en grupo, mediante una visualización limpia de los balances, sustituyendo los cálculos manuales y las conversaciones incómodas por una liquidación matemática clara.

* **Privacidad y autonomía total (*Local-First*):** Queremos dar una herramienta totalmente funcional offline, donde los datos financieros residan exclusivamente en el dispositivo del usuario, sin registros obligatorios, servidores intermedios ni monetización invasiva y la posibilidad de bloquear la aplicación con contraseña o datos biométricos.

* **Compensación inteligente de deudas:** Queremos introducir algoritmos optimizados que resuelvan saldos cruzados reduciendo drásticamente el número de transferencias o bizums necesarios, transformando así repartos complejos en pagos sencillos y faciles.

* **Experiencia de usuario accesible y directa:** Queremos crear interfaz limpia e intuitiva que permita registrar un apunte o consultar la posición deudora en dos pasos, que cualquiera pueda utilizar la aplicación.

## 1.4.2. Objetivos específicos

| Área de Trabajo | Objetivos Específicos |
| :--- | :--- |
| **Diseño y Usabilidad (UI/UX)** | • Diseñar una interfaz orientada a tareas en el paradigma de una ventana única, permitiendo registrar gastos o consultar balances en un flujo directo de dos pasos.<br><br>• Desarrollar el componente modular reutilizable `TarjetaSaldoParticipante` con señalización cromática automática según el balance contable (verde `#11734F` acreedor, rojo `#B53C3C` deudor y gris `#59665E` saldado).<br><br>• Diseñar un diálogo modal unificado (`DialogoGasto`) para captura ágil de compras con soporte simultáneo para reparto equitativo y asignaciones asimétricas individuales. |
| **Lógica Contable y Algoritmia** | • Establecer una única fuente de verdad contable en la entidad agregada `Grupo`, recalculando los saldos dinámicamente a partir de los apuntes registrados.<br><br>• Diseñar e integrar una heurística voraz que liquide las obligaciones cruzadas en como máximo 1 transferencias directas, eliminando transacciones redundantes entre los participantes.<br><br>• Implementar control de precisión numérica mediante márgenes de tolerancia de redondeo para evitar inconsistencias por imprecisión en aritmética de punto flotante. |
| **Arquitectura de Software (MVC)** | • Implementar el patrón arquitectónico **Modelo-Vista-Controlador (MVC)**, desacoplando el dominio contable de los componentes gráficos de Java Swing y de la gestión de eventos de usuario.<br><br>• Modelar la estructura formal de clases del sistema (`Participante`, `Gasto`, `Grupo`, `Transferencia`, `AlgoritmoLiquidacion`, `ServicioBoveda`) garantizando alta cohesión y bajo acoplamiento.<br><br>• Centralizar el flujo de interacción en el `ControladorPrincipal` (`ActionListener`), procesando las entradas de la Vista para mutar el Modelo y coordinando el refresco visual del estado consolidado. |
| **Seguridad y Persistencia Local-First** | • Construir un motor de almacenamiento estrictamente local y 100% fuera de línea (*offline*), asegurando que los registros financieros residan exclusivamente en el equipo del usuario sin depender de servidores externos.<br><br>• Proteger el acceso a la bóveda de datos local mediante un mecanismo de validación de contraseñas basado en funciones hash SHA-256.<br><br>• Incorporar mecanismos de respaldo mediante exportación e importación manual de copias de seguridad portables en formato estructurado JSON. |
| **Evolución Multiplataforma y Metodología** | • Desarrollar el cliente de escritorio en Java Swing cumpliendo la especificación de componentes JavaBeans y maquetación con NetBeans Matisse.<br><br>• Diseñar los modelos de datos y la arquitectura visual con vistas a su posterior traslación hacia una aplicación móvil reactiva desarrollada con Flutter.<br><br>• Gestionar el ciclo de desarrollo bajo el marco ágil Scrum, organizando el trabajo mediante historias de usuario, estimación relativa por *Story Points* y tableros visuales de seguimiento. |

## 1.5. Alcance del proyecto

El alcance global de PayClear contempla el ciclo de vida completo de esta aplicacion, cubriendo tanto sus funcionalidades como los objetivos para este primer sprint.

* **Registro inmediato de los gastos:** Entrada rapida de los datos, indicando concepto, importe y quien paga en la menor cantidad de clics posibles.
* **Pantalla de balances:** Pantalla donde ver en tiempo real el estado de cada cuenta individualmente mediante un sistema de señalizacion con colores (verde/rojo/gris) e historial de movimientos.
* **Liquidación multilateral optimizada:** Integracion de un algoritmo que simplifica las deudas al mínimo numero de transferencias directas entre integrantes.
* **Calculadora de reparto rapido:** Overlay para dividir cenas, compras, peajes... De manera equitativa y personalizada sin abandonar la pantalla principal.

---

> **Enfoque específico del Sprint 1:**  
> Ideación, análisis de mercado (benchmarking), prototipado de alta fidelidad navegable en Figma, definición del Backlog y especificación técnica de la arquitectura de clases y componentes.
