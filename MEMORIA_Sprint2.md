# 2.1. SECTOR PROFESIONAL Y PERFIL DE USUARIOS**

**2.1.1. Caracterización del sector profesional**
PayClear se sitúa en el sector FinTech (Financial Technology), dentro de la vertical de Gestión de Finanzas Personales (PFM) y sistemas de liquidación P2P no bancarios.   El sector evoluciona impulsado por la desafección hacia las aplicaciones SaaS comerciales tradicionales (Splitwise, Tricount), debido a sus muros de pago (paywalls), cuotas de registro y publicidad invasiva. En respuesta, PayClear adopta un modelo Local-First, que garantiza la operatividad sin conexión a Internet y cumple de forma nativa con el principio de privacidad por diseño.


**Tabla descriptiva del sector y modelo de negocio**
| Criterio | Sector SaaS Comercial (Splitwise, Tricount) | Modelo *Local-First* (PayClear) |
| :--- | :--- | :--- |
| **Ámbito** | Finanzas Personales en la Nube (Cloud PFM) | PFM Local-First y Optimización Algorítmica P2P |
| **Persistencia** | Servidores remotos de terceros | Almacenamiento local en el equipo (JSON) |
| **Conexión** | Conexión obligatoria a Internet | Operatividad 100% offline |
| **Modelo** | Suscripción Premium y banners publicitarios | Gratuito sin anuncios / Licencia Marca Blanca B2B |
| **Privacidad** | Registro de email/teléfono obligatorio | Minimización de datos: cero datos personales (RGPD) |



**2.1.2. Segmentación de perfiles de usuario (User Personas)**

Ficha 1: Carlos Gómez – Tesorero del Piso (Perfil Gestor / Escritorio)
- Rol y Entorno: Estudiante (23 años). Administra facturas de un piso compartido desde un ordenador portátil/escritorio.
- Competencias Digitales: Avanzadas (uso habitual de hojas de cálculo, gestión de ficheros y atajos de teclado).
- Objetivos: Introducir facturas rápidamente, visualizar balances globales con alta densidad de datos y exportar respaldos.
- Impacto en UI/UX: Interfaz en ventana única en Java Swing, navegación 100% por teclado (Tab/Enter) y exportación directa a JSON.

Ficha 2: Sofía Martínez – Conviviente Ocasional (Perfil Usuario / Móvil)
- Rol y Entorno: Estudiante (20 años). Añade tickets puntuales desde el smartphone (Android/iOS), frecuentemente en movimiento o sin cobertura.
- Competencias Digitales: Medias (nativa digital orientada a interfaces táctiles e intuitivas).
- Objetivos: Anotar un gasto en segundos y comprobar de un vistazo su estado de deuda.
- Impacto en UI/UX: Componente TarjetaSaldoParticipante con semáforo cromático (verde/rojo/gris) con contraste accesible (WCAG 2.1 AA) y ventana modal de calculadora rápida.

Ficha 3: Javier Ruiz – Gestor de Co-Living (Buyer Persona B2B)
- Rol y Entorno: Responsable de operaciones (38 años) en una residencia universitaria o complejo de co-living
- Competencias Digitales: Medias-Altas (usuario de software de gestión de empresas).
- Objetivos: Ofrecer una solución a los residentes para evitar conflictos de gastos sin asumir costes de infraestructura ni riesgos legales sobre datos personales.
- Impacto en UI/UX: Modelo de Marca Blanca B2B de coste $0 en servidores gracias a la arquitectura Local-First.



# 2.4. Partes interesadas

| Rol | Tipo | Categoría | Expectativas Principales | Nivel de Influencia | Estrategia de Comunicación Recomendada |
| :--- | :---: | :---: | :--- | :---: | :--- |
| **Equipo Scrum** | Interno | Primario | Claridad en los requisitos, reparto tareas y cumplimiento de plazos sin sobrecarga. | **Alto**<br>*(Gestionar el proyecto)* | *Daily Scrums* de 15 min, gestión en tiempo real mediante tablero Kanban y *Sprint Retrospectives*. |
| **Tribunal Evaluador** | Interno | Primario | Cumplimiento de los criterios de los RA, analizar documentación en Git, calidad técnica del código y demostrar la viabilidad del proyecto. | **Alto**<br>*(Gestionar de cerca)* | Presentaciones formales en cada *Sprint Review*, entrega puntual de capítulos en Markdown y seguimiento en tutorías. |
| **Usuarios Finales** | Externo | Primario | Aplicación gratuita, sin anuncios ni registros obligatorios, aplicación *offline* y que liquidación de deudas rápidas. | **Alto**<br>*(Mantener informados)* | Encuestas de validación, pruebas de usabilidad con prototipos interactivos y changelogs. |
| **Organismos Reguladores (AEPD, UE - RGPD / UNE)** | Externo | Secundario | Cumplimiento de privacidad, derechos de autor y accesibilidad WCAG 2.1 AA. | **Medio**<br>*(Mantener satisfechos)* | Auditoría interna de cumplimiento legal en la Memoria Técnica y redacción de políticas de privacidad y licencias en el repositorio. |
| **Proveedores Tecnológicos (GitHub, Flutter, Oracle...)** | Externo | Secundario | Respeto a las licencias de software libre y uso de sus APIs y librerías. | **Bajo**<br>*(Monitorizar)* | Control de licencias en la documentación técnica y seguimiento de *releases* oficiales en repositorios. |
| **Competidores(Splitwise, Tricount, Settle Up)** | Externo | Secundario | Mantener su mercado y rentabilizar sus modelos de suscripción. | **Bajo**<br>*(Monitorizar)* | Análisis de *benchmarking* periódico para vigilar cambios en sus métodos de monetización y mantener la ventaja competitiva de PayClear. |
