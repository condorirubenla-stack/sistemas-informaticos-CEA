# Sistemas Informáticos CEA - Plataforma Académica

Plataforma educativa para el Centro de Educación Alternativa, nivel Técnico Medio.

## Estructura
El proyecto está unificado en un solo repositorio y cuenta con dos componentes principales:

1. **`/backend`**: API en FastAPI (Python) con PostgreSQL.
2. **`/frontend`**: Interfaz de usuario PWA basada en HTML, CSS y JS puro.

## Despliegue en Railway
### Backend
1. Crea un proyecto en Railway y conecta el repositorio.
2. Crea una base de datos PostgreSQL en Railway.
3. En las variables de entorno (`Variables`) del servicio backend, agrega:
   - `DATABASE_URL` (Usa el Internal Database URL de PostgreSQL).
   - `SECRET_KEY` (Una clave segura para JWT).
   - `RENDER=false`
4. Railway usará el archivo `Procfile` automáticamente.

### Frontend
1. En Railway, crea un nuevo servicio conectado al mismo repositorio.
2. Selecciona la carpeta `/frontend`.
3. Actualiza el archivo `/frontend/js/api.js` con el dominio del backend generado por Railway.

## Malla Curricular
- **Nivel Básico:** 1er Semestre
- **Nivel Auxiliar:** 2do Semestre
- **Nivel Medio I:** 3er Semestre
- **Nivel Medio II:** 4to Semestre

## Usuario Administrador por Defecto
Al iniciar el backend y ejecutar `/cargar-datos`, se creará automáticamente:
- **Usuario:** `admin@sistemas.com`
- **Contraseña:** `admin123`
