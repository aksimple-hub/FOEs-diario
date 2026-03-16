# FOEs-diario
---


# Diario de Trabajo: Proyecto Gestión de Personal Docente

**Periodo:** 02/03/2026 - 12/03/2026

**Proyecto:** Gestión de Prácticas Docentes - FP Virtual

---

## Semana 1: Introducción y Toma de Contacto

### Lunes 02/03/2026

* **Presentación del equipo:** Conocimiento de los responsables del proyecto y compañeros de departamento.
* **Recorrido por las instalaciones:** Visita guiada por el edificio y asignación del puesto de trabajo.
* **Inducción inicial:** Jornada ligera de adaptación a la cultura de la empresa y flujos de trabajo internos.

### Martes 03/03/2026

* **Asignación al proyecto:** Inicio formal en el proyecto de **Prácticas Docentes**.
* **Análisis preliminar:** Revisión de la documentación existente y primera toma de contacto con la estructura del repositorio.

### Miércoles 04/03/2026

* **Exploración técnica:** Análisis del stack tecnológico (Laravel, Docker, MySQL).
* **Revisión de requisitos:** Identificación de las tareas pendientes dentro de la gestión de centros y docentes.

### Jueves 05/03/2026 - Viernes 06/03/2026

* **Festivo:** Días no laborables por festividades.

---

## Semana 2: Desarrollo y Resolución de Problemas

### Lunes 09/03/2026

* **Configuración del Entorno Docker:** * Ajuste de los archivos `docker-compose.yml` y `.env` para crear una base de datos llamada **instituto** con usuario y contraseña **alumno/alumno**.
* Configuración del puerto **23306** para poder conectar mi ordenador directamente con la base de datos de Docker.


* **Solución de problemas de acceso:** * Se identificó que el problema al entrar al panel no era de programación, sino de credenciales. Se revisaron los **seeders** para usar los correos y contraseñas de prueba correctos.
* **Desarrollo de Altas:**
* Implementación del registro de docentes asegurando que el DNI se guarde siempre en mayúsculas.
* Corrección de errores en la base de datos para que el sistema guarde primero al profesor y luego lo vincule a su centro.



### Martes 10/03/2026

* **Gestión de Bajas y Reactivaciones:**
* Creación de un sistema que permite dar de baja a un docente sin borrar sus datos, solo marcándolo como inactivo.
* Se añadieron botones que cambian según el estado: si el profesor está de baja, aparece un botón verde para reactivarlo; si está activo, aparece el botón rojo para darle de baja.


* **Limpieza de datos:**
* Creación de un filtro automático que elimina puntos o símbolos (º, .) de los nombres y pone la primera letra en mayúscula.


* **Buscador en tiempo real:**
* Integración de **Alpine.js** para que la lista de profesores se filtre al instante mientras escribimos el nombre o el DNI.



### Miércoles 11/03/2026

* **Organización de rutas y limpieza de código:**
* Se reestructuró el archivo de rutas (`web.php`) para organizar mejor las funciones de los centros y las del administrador.
* Se sacó la función de "Reactivar docente" del grupo de administración para que los usuarios de los centros puedan usarla directamente.


* **Mejora en la gestión de acciones:**
* Se actualizaron los formularios de la tabla de docentes para que utilicen rutas más sencillas y seguras, mejorando la respuesta del sistema al pulsar los botones de baja.



### Jueves 12/03/2026 (Hoy)

* **Optimización de listas de selección:**
* Se modificó el sistema de asignación de clases para que los profesores que están de baja ya no aparezcan en los menús desplegables.


* **Ajuste de mensajes de aviso:**
* Se corrigió una alerta que avisaba de "módulo duplicado" por error. Ahora el sistema es capaz de ignorar a los profesores inactivos al hacer el recuento de personal.


* **Finalización de documentación técnica:**
* Redacción del manual **README.md** explicando de forma sencilla cómo arrancar el proyecto, la configuración del puerto 23306 y las soluciones aplicadas a los problemas de estos días.

### Viernes 13/03/2026 
* **Pruebas de Integración (Flujo completo):

* Hice un testeo real: di de alta a un profesor, comprobé que aparecía en "Establecer Docencia", luego le di de baja y verifiqué que desaparecía del desplegable automáticamente.

* Probé a reactivarlo para confirmar que el botón verde funcionaba y el mensaje de éxito era claro.

* **Revisión de Mensajes de Feedback (Alertas):

* Me aseguré de que cuando el sistema redirige tras una acción (como la de reactivar), el mensaje de "El docente ha sido reactivado correctamente" se viera bien en pantalla para que el usuario sepa qué ha pasado.

* ** Limpieza de código muerto:

* Aproveché para borrar ese trozo de código de los ciclos/módulos que no estábamos usando en la pantalla de alta, dejando el controlador mucho más limpio y fácil de explicar.

---
