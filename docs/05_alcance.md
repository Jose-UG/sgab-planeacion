# Definición del Alcance

Definir el alcance del proyecto es fundamental para establecer los límites y objetivos claros, lo que facilita la planificación y ejecución efectiva.

---

## Funcionalidades Incluidas

- Registro y gestión de usuarios.
- Gestión de materias.
- Registro de alumnos.
- Registro y consulta de calificaciones.
- Generación de reportes académicos.
- Autenticación y control de acceso basado en roles.
- Interfaz web intuitiva y responsiva.

---

## Funcionalidades Excluidas

- Integración con sistemas externos.
- Pagos en línea o gestión financiera.
- Aplicación móvil nativa.
- Reportes avanzados o personalizados.

---

## Suposiciones

- La institución no requiere integración con otros sistemas.
- El número de usuarios simultáneos será manejable con la infraestructura propuesta.
- El sistema se usará únicamente vía web, sin necesidad de aplicaciones móviles nativas.

---

## Ejemplo de Cambio y su Impacto

Si se solicita agregar generación automática de boletas en PDF, esto implicaría:

- Requerir una nueva funcionalidad de generación de documentos.
- Aumentar el tiempo de desarrollo y pruebas.
- Incrementar la complejidad del sistema.
- Ajuste en la base de datos para almacenar información adicional.

---

## Ejemplo de Scope Creep

Durante el desarrollo del sistema, el cliente solicita agregar una aplicación móvil para que los alumnos puedan consultar sus calificaciones desde sus teléfonos.

Aunque la funcionalidad parece relacionada con el sistema original, esta solicitud representa un cambio significativo en el alcance del proyecto, ya que implica:

- Desarrollo de una nueva plataforma (móvil). 
- Diseño de una interfaz diferente.
- Pruebas adicionales para asegurar compatibilidad con diferentes dispositivos.
- Incremento considerable en el tiempo y costo del proyecto.
- Posible contratación de recursos adicionales.

Este tipo de solicitud representa un caso clase de *scope creep*, ya que amplía el proyecto sin una revisión formal del alcance, lo que puede afectar negativamente la planificación y ejecución del proyecto.

### Esquema de Scope Creep

Alcance Original:
[ SGAB Web ]

Solicitud de Cambio:
[ SGAB Web + App Móvil ]

Impacto:
Tiempo de desarrollo aumenta.
Costo aumenta.
Complejidad aumenta.