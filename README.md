# 🎬 TMDB Clone — Movies ADA06

Recreación simplificada de las vistas y catálogo de **The Movie Database (TMDB)** ([themoviedb.org](https://www.themoviedb.org/?language=es)) con arquitectura Frontend y Backend (REST API).

---

## 📋 Descripción del Proyecto

Este proyecto implementa las vistas principales de TMDB para exploración y consulta de películas:
- **Navbar / Encabezado TMDB**: Navegación por categorías, menú desplegable, branding oficial y búsqueda.
- **Hero Banner interactivo**: Buscador en tiempo real de títulos y sinopsis.
- **Filtro por Géneros**: Chips interactivos para filtrar el catálogo (Acción, Animación, Aventura, Ciencia Ficción, Comedia, Drama, Terror, etc.).
- **Carruseles de Categorías**:
  - *Tendencias* (Hoy / Esta semana).
  - *Lo más popular* (En streaming / En cines).
  - *Mejor valoradas* (Aclamadas por la crítica).
- **Insignias circulares de calificación**: Círculo de porcentaje SVG estilo TMDB con gradiente de color según la nota de usuario.
- **Vista detallada / Modal de Película**:
  - Banner backdrop y póster en alta resolución.
  - Título, año, clasificación por edades, duración, géneros y lema.
  - Sinopsis completa ("Vista general").
  - Reparto principal con fotografías de actores y personajes.
  - Reproductor integrado de tráiler oficial en YouTube.

---

## 📂 Estructura del Repositorio

```text
Movies-ADA06/
├── AI_USAGE_LOG.md           # Registro de uso de Inteligencia Artificial (plantilla requerida)
├── README.md                 # Documentación del proyecto
├── .gitignore                # Archivos y dependencias ignoradas por Git
├── package.json              # Configuración y scripts raíz
├── backend/                  # Servidor y API REST
│   ├── package.json
│   ├── server.js             # API Express con endpoints de películas y servicio estático
│   └── data/
│       └── movies.json       # Base de datos con películas, pósters e información detallada
└── frontend/                 # Interfaz de usuario (Vistas TMDB)
    ├── index.html            # Estructura de vistas, componentes y modales
    ├── styles.css            # Hoja de estilos con diseño fiel a TMDB
    └── app.js                # Lógica del cliente, consumo de API y renderizado dinámico
```

---

## 🚀 Puesta en Marcha

### Prerrequisitos
- Node.js (versión 18 o superior)
- npm

### Ejecución Rápida (Recomendada)
Desde la raíz del proyecto, ejecuta:

```bash
# 1. Instalar dependencias del backend
npm run install:all

# 2. Iniciar servidor (sirve tanto la API como el frontend)
npm start
```

Abre tu navegador en:  
👉 **[http://localhost:5000](http://localhost:5000)**

---

## 📡 Endpoints del Backend (API REST)

| Método | Endpoint | Descripción | Parámetros de consulta |
|---|---|---|---|
| `GET` | `/api/movies` | Lista todas las películas | `?category=popular\|trending\|top_rated\|upcoming`, `?search=texto`, `?genre=genero` |
| `GET` | `/api/movies/:id` | Detalle completo de una película | Parámetro en ruta `:id` |
| `GET` | `/api/categories` | Lista de categorías disponibles | Ninguno |
| `GET` | `/api/genres` | Lista de todos los géneros únicos | Ninguno |
| `GET` | `/api/health` | Estado del servicio | Ninguno |

---

## 🔑 Prerrequisito: Fine-grained Personal Access Token (Solo Lectura)

Para dar acceso de solo lectura al evaluador/profesor sobre este repositorio mediante un **Fine-grained Personal Access Token**:

1. En GitHub, ve a **Settings** → **Developer Settings** → **Personal Access Tokens** → **Fine-grained tokens**.
2. Haz clic en **Generate new token**.
3. Configura:
   - **Token name**: `Evaluacion-Movies-ADA06`
   - **Expiration**: Según la duración del curso (ej. 30 o 60 días).
   - **Repository access**: Selecciona **Only select repositories** y elige `RubenPerez55/Movies-ADA06`.
   - **Permissions** → **Repository permissions**:
     - *Contents*: `Read-only`
     - *Issues*: `Read-only`
     - *Pull requests*: `Read-only`
     - *Metadata*: `Read-only` (asignado automáticamente)
4. Haz clic en **Generate token** y copia el token para entregarlo al profesor.

---

## 📝 Registro de IA

El archivo `AI_USAGE_LOG.md` se encuentra disponible en la raíz del repositorio listo para ser completado durante el desarrollo de las tareas correspondientes.
