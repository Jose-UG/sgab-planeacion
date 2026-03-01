# Definición de Requisitos Funcionales para Endpoints
Sistema de Gestión Académica Básico (SGAB)

---

## 1. Introducción

En este documento traducimos cada requisito funcional definido previamente en endpoints.

Se establece la relación:

Requisito Funcional -> Método HTTP -> Endpoint -> Reglas de negocio

---

## 2. Módulo Students (Alumnos)

### RF-04: Registrar, modificar y eliminar alumnos

#### POST /students
Descripción: Crear un nuevo alumno.

Body esperado:
{
  "matricula": "string",
  "nombre": "string",
  "carrera": "string"
}

Reglas:
- Matricula única.
- Campos obligatorios.
- Status inicial = active.

Respuesta:
201 created

---

#### GET /students
Descripción: Listar alumnos.

Consulta opcional:
GET /students?page=1&limit=10

Respuesta:
{
  "items": [],
  "total": number
}

---

#### GET /students/:id
Descripción: Consultar alumno por ID.

Reglas:
- El alumno debe existir.
- Si no existe → 404 Not Found.

---

#### PATCH /students/:id
Descripción: Actualizar información del alumno.

Body parcial:
{
  "nombre": "string?",
  "carrera": "string?",
  "status": "string?"
}

Reglas:
- Validar cambios.
- Verificar unicidad si cambia matrícula.

---

#### DELETE /students/:id
Descripción: Eliminación lógica del alumno.

Regla:
- Cambiar status a inactive.
- Respuesta: 204 No Content.

---

## 3. Módulo Subjects (Materias)

### RF-05: Gestionar materias

#### POST /subjects
Crear materia.

Body:
{
  "clave": "string",
  "nombre": "string",
  "semestre": number
}

Reglas:
- Clave única.
- Campos obligatorios.

---

#### GET /subjects
Listar materias.

#### GET /subjects/:id
Consultar materia específica.

#### PATCH /subjects/:id
Actualizar materia.

#### DELETE /subjects/:id
Eliminar materia.

---

## 4. Módulo Grades (Calificaciones)

### RF-06 y RF-07: Registrar y consultar calificaciones

#### POST /grades
Registrar calificación.

Body:
{
  "studentId": "string",
  "subjectId": "string",
  "value": number
}

Reglas:
- El alumno debe existir.
- La materia debe existir.
- value entre 0 y 100.

Respuesta:
201 Created

---

#### GET /grades
Listar calificaciones.

#### GET /grades/:id
Consultar calificación específica.

#### PATCH /grades/:id
Actualizar calificación.

#### DELETE /grades/:id
Eliminar calificación.

---

## 5. Módulo Users (Usuarios)

### RF-01 y RF-02: Gestión de usuarios

#### POST /users
Crear usuario.

Body:
{
  "nombre": "string",
  "email": "string",
  "password": "string",
  "role": "admin | teacher | student"
}

Reglas:
- Email único.
- Password obligatoria.

---

#### POST /auth/login
Autenticación.

Body:
{
  "email": "string",
  "password": "string"
}

Respuesta:
200 OK + token

---

## Conclusión

Cada requisito funcional ha sido traducido a un endpoint específico con su método HTTP correspondiente, reglas de negocio claras y formatos de request/response definidos. Esto servirá como base para el desarrollo del backend del SGAB.
