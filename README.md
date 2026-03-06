# infra-clima 🌦️

Infraestructura Docker para levantar el proyecto **frontend-clima**.

---

## Requisitos previos

- [Docker](https://www.docker.com/) ≥ 24
- [Docker Compose](https://docs.docker.com/compose/) ≥ 2.20 (viene incluido con Docker Desktop)

---

## Configuración de variables de entorno

1. Copia el archivo de ejemplo y renómbralo como `.env`:

   ```bash
   cp .env.example .env
   ```

2. Abre `.env` y llena tu API key de OpenWeatherMap:

   ```env
   OWM_API_KEY=tu_api_key_real_aqui
   OWM_BASE_URL=https://api.openweathermap.org/data/2.5
   OWM_CITY=Tuxtla Gutierrez,MX
   ```

> **Nota:** Puedes obtener tu API key gratuita en [openweathermap.org](https://openweathermap.org/api).

---

## Levantar el proyecto

Desde la carpeta `infra-clima`, ejecuta:

```bash
docker compose up --build
```

La aplicación estará disponible en: **[http://localhost:3000](http://localhost:3000)**

---


## Estructura del proyecto

```
ej.APIs_Terceros_Clima/
├── frontend-clima/    # Código fuente de la app Next.js
│   └── Dockerfile     # Imagen Docker multi-etapa
└── infra-clima/       # ← Estás aquí
    ├── docker-compose.yml
    ├── .env.example
    └── README.md
```

---
