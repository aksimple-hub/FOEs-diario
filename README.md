# FOEs-diario
---

# Diario de Trabajo: Proyecto Gestión de Personal Docente

**Periodo:** 02/03/2026 - 10/03/2026

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

* **Configuración del Entorno Docker:** * Modificación de archivos `docker-compose.yml` y `.env` para adaptar el sistema a un entorno de pruebas controlado.
* Levantamiento del servidor web (PHP 8.4/Nginx) y de la base de datos (MySQL 8.0).


* **Resolución de errores de acceso:** * Solución del fallo de autenticación mediante la generación de la `APP_KEY` y configuración de los *Guards* de Laravel.
* **Desarrollo de las Tareas A, B y C:**
* Implementación del alta de docentes con validación de DNI (estandarización a mayúsculas) y correos electrónicos.
* Corrección de errores de integridad referencial (Error 1452) y campos obligatorios (Error 1364) en la base de datos.



### Martes 10/03/2026 (Hoy)

* **Implementación de la Tarea D (Bajas y Reactivaciones):**
* Creación de un sistema de "Soft Delete" para marcar docentes como inactivos mediante el campo `de_baja`.
* Integración de botones dinámicos en la interfaz para dar de baja o reactivar docentes con un solo clic.


* **Optimización de la Tarea G (Sanitización de Datos):**
* Desarrollo del método `normalizarNombreYApellido` utilizando `str_replace` para eliminar símbolos (º, .) y aplicar formato `Title Case`.


* **Mejoras de UX y Lógica de Negocio:**
* Integración de **Alpine.js** para el filtrado de tablas en tiempo real sin recarga de página.
* Aplicación de filtros en los selectores de docencia para excluir automáticamente a los docentes que están de baja.


* **Documentación Técnica:**
* Redacción del archivo `README.md` detallando la infraestructura, comandos de arranque y soluciones a retos técnicos encontrados durante la semana.



---
