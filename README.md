# Nearyx — Frontend

Plataforma web que conecta estudiantes con expertos cercanos en Medellín: mapa, feed, chat y reservas.

## Despliegue
| | Link |
|---|---|
| Sitio | https://TU-FRONT.vercel.app |
| API | https://TU-GATEWAY.onrender.com |
| Repositorio backend | https://github.com/TU-USUARIO/TU-BACKEND |

## Capturas
Guarda las imágenes en `docs/screenshots/`.

| Landing | Login |
|---|---|
| ![Landing](docs/screenshots/landing.png) | ![Login](docs/screenshots/login.png) |

| Explorar (mapa) | Administración |
|---|---|
| ![Explorar](docs/screenshots/explore.png) | ![Admin](docs/screenshots/admin.png) |

## Stack
Next.js 16 (App Router) · React 19 · TypeScript · Tailwind 4 · shadcn/ui · TanStack Query · Mapbox GL

## Instalación
```bash
git clone https://github.com/TU-USUARIO/TU-FRONT.git
cd TU-FRONT
cp .env.example .env.local   # completa los valores
npm install
npm run dev                  # http://localhost:3000
```

## Variables de entorno
| Variable | Descripción |
|---|---|
| `NEXT_PUBLIC_API_URL` | URL pública del gateway (sin barra final) |
| `INTERNAL_API_URL` | Misma URL, para las rutas `/api/*` del servidor |
| `NEXT_PUBLIC_WS_URL` | Host del WebSocket del chat |
| `NEXT_PUBLIC_MAPBOX_TOKEN` | Token público de Mapbox |

## Rutas protegidas
Sin sesión, `/dashboard`, `/explore`, `/bookings`, `/messages`, `/profile`, `/tutor` y `/admin` redirigen a `/login`. `/admin` además exige rol `admin`. Con sesión activa, `/login` y `/register` redirigen al inicio.

## Credenciales de prueba
| Rol | Correo | Contraseña |
|---|---|---|
| admin | admin@nearyx.dev | Admin12345! |
| student | estudiante@nearyx.dev | Estudiante12345! |
| tutor | experto@nearyx.dev | Experto12345! |

## Reparto del trabajo
| Integrante | Qué construyó |
|---|---|
| Nombre 1 | Landing, login y registro |
| Nombre 2 | Explorar, mapa, perfiles |
| Nombre 3 | Chat, reservas, administración |
