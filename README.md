<div align="center">

  <img src="img/logo-payClear.png" alt="PayClear Logo" width="180" />

  # PayClear

  > **Gestor ágil de gastos compartidos y liquidación de deudas en local**

  [![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](#)
  [![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](#)
  [![Swing](https://img.shields.io/badge/GUI-Swing%20%2F%20Matisse-4E82B4?style=for-the-badge&logo=java&logoColor=white)](#)
  [![Arquitectura](https://img.shields.io/badge/Arquitectura-MVC-2EA44F?style=for-the-badge)](#)
  [![Licencia: MIT](https://img.shields.io/badge/Licencia-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 1. Descripcion General

PayClear es una solucion de escritorio disenada para simplificar la division de gastos grupales y la liquidacion eficiente de saldos en comunidades cerradas (pisos compartidos, viajes y tesoreria de colectivos).

Nace como respuesta directa frente a soluciones comerciales privativas (Splitwise, Tricount), suprimiendo los muros de pago recurrentes, los limites artificiales de registro diario y la recopilacion indebida de informacion personal.

### Principios Fundamentales
* **Acceso Inmediato:** Cero registros obligatorios, correos o contrasenas.
* **Privacidad Estricta (Local-First):** La base de datos reside de forma exclusiva en el almacenamiento local del equipo.
* **Optimizacion de Pagos:** Implementacion de un algoritmo voraz (*greedy algorithm*) que minimiza el numero total de transferencias necesarias para liquidar balances a cero.

---

## 2. Arquitectura del Proyecto (Patron MVC)

El proyecto esta organizado bajo una separacion estricta de responsabilidades:

```text
src/main/java/com/payclear/
|-- AplicacionPayClear.java
|-- componente/
|   `-- TarjetaSaldoParticipante.java
|-- controlador/
|   `-- ControladorPrincipal.java
|-- modelo/
|   |-- Gasto.java
|   `-- Participante.java
`-- vista/
    |-- DialogoDivisionRapida.form
    |-- DialogoDivisionRapida.java
    |-- VistaPrincipal.form
    `-- VistaPrincipal.java
    
 ````

 ## 4. Requisitos y Compilacion

### Requisitos de Entorno

* **Java Development Kit (JDK):** Version 17 o superior.
* **Entorno de Desarrollo (IDE):** Apache NetBeans 17 o superior.
* **Gestor de Construccion:** Apache Ant o Maven.


## 5. Equipo de Desarrollo

* Guillermo Eugui Sanchez
* Jesus Cabeza
* Jose Luis Fernandez
