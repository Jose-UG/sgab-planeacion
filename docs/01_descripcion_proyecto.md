# Descripcion del Proyecto

## Objetivo del Sistema

El Sistema de Gestion Académica Básico (SGAB) es una aplicación web diseñada para administrar la información académica de una institución educativa. El propósito principal es centralizar la gestión de alumnos, materias, calificaciones y usuarios en una plataforma accesible y estructurada.

El sistema busca ayudar y mejorar el control administrativo, reducir errores manuales y facilitar el acceso a la información académica en timepo real.

---

## Usuarios Principales

Los usuarios identificados en el sistema son:

-**Administrador**: Gestiona los usuarios, materias y la configuración general del sistema.
-**Docente**: Registra y consulta calificaciones de alumnos.
-**Alumno**: Consulta sus materias y sus calificaciones.

Para este sistema, a cada usuario le corresponde un rol, el cual tendrá permisos dentro del sistema según su nivel de rol.

---

## Problema que Resuelve

Actualmente, la mayoría de las instituciones educativas recurren a la gestión de información académica mediante hojas de cálculos o procesos manuales, esto genera:

- Errores en la captura de datos.
- Pérdidas de información.
- Dificultad en generación de reportes.

El SGAB resuelve estos problemas mediante una plataforma web bien estructurada, segura y centralizada.

---

## Suposiciones Iniciales

- El sistema será usado por una institución educativa grande o mediana o chica.
- El acceso a este sistema será por el navegador web.
- Existirá la conexión a internet estable.
- El número estimado de usuarios simultáneos será menor a 100.
- La institución tendrá la manera de separar e identificar a los estudiantes.

## Diagrama de Contexto

                              +---------------------+
                              |     Administrador   |
                              | (Gestiona usuarios) |
                              +---------------------+
                                        |
                                        |
                                        v
+-----------------+        +-------------------------+        +-----------------+
|   Alumno        | -----> |   SGAB (Sistema Web)    | <----- |   Docente       |
| (Consulta       |        |    Gestión Académica    |        | (Registra       |
| calificaciones) |        |                         |        | calificaciones) |
+-----------------+        +-------------------------+        +-----------------+

Este SGAB funciona como un sistema centralizado que interactúa con tres tipos de usuarios (mencionados en Usuarios Principales), intercambian informacion con el sistema según el rol y permisos de cada uno.