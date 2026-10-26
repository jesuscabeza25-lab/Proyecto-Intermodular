## **2.1. SECTOR PROFESIONAL Y PERFIL DE USUARIOS**

### **2.1.1. Caracterización del sector profesional**
PayClear pertenece al sector FinTech (Financial Technology), dentro de la línea de Gestión de Finanzas Personales y de los sistemas de pago P2P no bancarios. El sector se mueve impulsado por la frustración con las aplicaciones SaaS tradicionales (Splitwise, Tricount) por sus barreras de pago (paywalls), cuotas de registro y publicidad invasiva. Como respuesta, PayClear adopta un modelo Local-First, que garantiza la operatividad sin conexión a Internet y respeta de forma nativa el principio de privacidad por diseño.



**Tabla descriptiva del sector y modelo de negocio**
| Criterio | Sector SaaS Comercial (Splitwise, Tricount) | Modelo *Local-First* (PayClear) |
| :--- | :--- | :--- |
| **Ámbito** | Finanzas Personales en la Nube (Cloud PFM) | PFM Local-First y Optimización Algorítmica P2P |
| **Persistencia** | Servidores remotos de terceros | Almacenamiento local en el equipo (JSON) |
| **Conexión** | Conexión obligatoria a Internet | Operatividad 100% offline |
| **Modelo** | Suscripción Premium y banners publicitarios | Gratuito sin anuncios / Licencia Marca Blanca B2B |
| **Privacidad** | Registro de email/teléfono obligatorio | Minimización de datos: cero datos personales |

### **2.1.2. Segmentación de perfiles de usuario (User Personas)**

**Ficha 1: Carlos Gómez – El tesorero del piso (Perfil Gestor / Ordenador)** 

Carlos tiene 23 años, estudia y vive en un piso compartido. Es la persona organizada de la casa que se encarga de llevar al día las facturas de la luz, el agua y el alquiler desde su ordenador portátil. 

-   **Nivel tecnológico:** Maneja bien los ordenadores. Le gusta usar la hoja de cálculo (Excel) y prefiere usar atajos de teclado antes que estar haciendo clic con el ratón para ir más rápido. 
-   **¿Qué necesita?:** Apuntar los gastos de forma rápida, ver en una sola pantalla todos los números claros del piso sin dar vueltas por menús complicados y guardar una copia de seguridad de las cuentas por si acaso. 
-   **¿Cómo responde PayClear en la pantalla?:**
    -   Toda la información del piso se muestra en una única ventana fácil de entender.
    -   Se puede mover por los campos de texto usando solo la tecla Tabulador y confirmar con Enter, sin necesidad de tocar el ratón.
    -   Permite guardar las cuentas directamente como un archivo en su propio ordenador para tenerlo siempre a salvo.

**Ficha 2: Sofía Martínez – La compañera de piso (Perfil Usuario / Móvil)**

Sofía tiene 20 años y comparte piso con Carlos. Usa la aplicación desde su teléfono móvil sobre la marcha (al salir del supermercado o en la cafetería), muchas veces sin internet o sin cobertura.

-   **Nivel tecnológico:** Normal. Usa el móvil a diario para redes sociales y mensajería, por lo que busca cosas visuales, sencillas y directas.
-   **¿Qué necesita?:** Apuntar un ticket de la compra en un par de segundos y saber de un vistazo rápido si le deben dinero o si le toca pagar a ella.
-   **¿Cómo responde PayClear en la pantalla?:**
    -   Usa tarjetas de colores muy claras y fáciles de leer para cualquier persona:
        -   **Verde:** Le deben dinero a ella.
        -   **Rojo:** Ella debe dinero a sus compañeros.
        -   **Gris:** Las cuentas están a cero (saldadas).
    -   Incluye un botón sencillo para abrir una calculadora rápida que divide el ticket en partes iguales o personalizadas sin complicaciones.

**Ficha 3: Javier Ruiz – El gestor del edificio de alquiler (Buyer Persona / Cliente Empresa)**

Javier tiene 38 años y trabaja gestionando una residencia de estudiantes o un edificio con varios pisos compartidos.

-   **Nivel tecnológico:** Medio-alto. Usa programas de gestión en su trabajo diario.
-   **¿Qué necesita?:** Recomendar a los inquilinos una herramienta para que gestionen sus gastos sin pelearse, pero sin que su empresa tenga que pagar cuotas mensuales de servidores ni responsabilizarse de guardar datos personales (correos, teléfonos o tarjetas de crédito) de los jóvenes.
-   **¿Cómo responde PayClear en la pantalla?:**
    -   Al no guardar datos en internet ni en la nube (todo se guarda dentro del móvil u ordenador de los propios usuarios), la empresa de Javier no gasta dinero en servidores ni se expone a problemas con las leyes de protección de datos.
    -   Permite personalizar la aplicación con la marca o logo del edificio si la empresa quiere ofrecerla como un servicio extra a sus inquilinos.



# 2.4. Partes interesadas

| Rol | Tipo | Categoría | Expectativas Principales | Nivel de Influencia | Estrategia de Comunicación Recomendada |
| :--- | :---: | :---: | :--- | :---: | :--- |
| **Equipo Scrum** | Interno | Primario | Claridad en los requisitos, reparto tareas y cumplimiento de plazos sin sobrecarga. | **Alto**<br>*(Gestionar el proyecto)* | *Daily Scrums* de 15 min, gestión en tiempo real mediante tablero Kanban y *Sprint Retrospectives*. |
| **Tribunal Evaluador** | Interno | Primario | Cumplimiento de los criterios de los RA, analizar documentación en Git, calidad técnica del código y demostrar la viabilidad del proyecto. | **Alto**<br>*(Gestionar de cerca)* | Presentaciones formales en cada *Sprint Review*, entrega puntual de capítulos en Markdown y seguimiento en tutorías. |
| **Usuarios Finales** | Externo | Primario | Aplicación gratuita, sin anuncios ni registros obligatorios, aplicación *offline* y que liquidación de deudas rápidas. | **Alto**<br>*(Mantener informados)* | Encuestas de validación, pruebas de usabilidad con prototipos interactivos y changelogs. |
| **Organismos Reguladores (AEPD, UE - RGPD / UNE)** | Externo | Secundario | Cumplimiento de privacidad, derechos de autor y accesibilidad WCAG 2.1 AA. | **Medio**<br>*(Mantener satisfechos)* | Auditoría interna de cumplimiento legal en la Memoria Técnica y redacción de políticas de privacidad y licencias en el repositorio. |
| **Proveedores Tecnológicos (GitHub, Flutter, Oracle...)** | Externo | Secundario | Respeto a las licencias de software libre y uso de sus APIs y librerías. | **Bajo**<br>*(Monitorizar)* | Control de licencias en la documentación técnica y seguimiento de *releases* oficiales en repositorios. |
| **Competidores(Splitwise, Tricount, Settle Up)** | Externo | Secundario | Mantener su mercado y rentabilizar sus modelos de suscripción. | **Bajo**<br>*(Monitorizar)* | Análisis de *benchmarking* periódico para vigilar cambios en sus métodos de monetización y mantener la ventaja competitiva de PayClear. |
