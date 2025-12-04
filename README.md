# Control Escolar DESIT – Proyecto Final

Aplicaciones Web (DESIT) – Otoño 2025  
Facultad de Ciencias de la Computación – BUAP  
Profesor: M.C. Luis Yael Méndez Sánchez

---

# Descripción del Proyecto

Control Escolar DESIT es una aplicación web completa desarrollada con **Angular (frontend)** y **Django REST Framework (backend)** que permite gestionar usuarios (administradores, maestros y alumnos) y realizar el **CRUD completo de materias**, cumpliendo todas las validaciones y requerimientos establecidos en el proyecto.

El sistema incluye autenticación, roles, servicios HTTP, tablas dinámicas, gráficas y validaciones estrictas para los formularios.

---

## Funcionalidades Principales

### Módulo de Usuarios
- Login con autenticación.
- Roles: Administrador, Maestro y Alumno.
- Contenido dinámico por permisos.

### RUD de Materias (solo Administrador)
- Crear, listar, editar y eliminar materias.
- Validaciones estrictas:
  - NRC único y numérico.
  - Nombre sin números ni caracteres especiales.
  - Sección numérica.
  - Selección obligatoria de días.
  - Validación de horarios (inicio < fin).
  - Créditos numéricos.
  - Selección de salón, carrera y profesor asignado.

### abla dinámica (Angular Material)
- Paginación.
- Filtrado (NRC y nombre).
- Ordenamiento.
- Acciones dinámicas por rol.

### Gráficas dinámicas (Chart.js)
- Histograma.
- Barras.
- Pastel.
- Dona.
- Datos reales desde la base de datos (usuarios registrados).

---

## Tecnologías utilizadas

### Frontend
- Angular 17+
- Angular Material
- SCSS
- RxJS
- Chart.js

### Backend
- Django 4+
- Django REST Framework
- MariaDB / MySQL
- JWT Authentication

---

---

## Cómo ejecutar el proyecto

### Backend (Django)

cd control_escolar_desit_api
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

### Frontend (Angular)

cd control-escolar-desit-webapp
npm install
ng serve -o
