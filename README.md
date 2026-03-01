# Plataforma Textil OIT-UNTREF - MVP

**Repositorio de documentacion del MVP** | [Repositorio de codigo](https://github.com/GIDs/Textil_mvp)

## Vision

Plataforma sociotecnica para el sector textil argentino que busca:
- Formalizar talleres y cooperativas textiles
- Conectar marcas con proveedores verificados
- Garantizar trazabilidad y transparencia
- Facilitar la fiscalizacion del Estado
- Combatir el trabajo informal y el dumping social

## Estado Actual

- **App desplegada:** [pdt-nine.vercel.app](https://pdt-nine.vercel.app)
- **Sprint 1:** Completado (fundacion, auth, layout, navegacion base)
- **Prototipo original:** [gbreard.github.io/textil](https://gbreard.github.io/textil/) (21 pantallas HTML)
- **Documentacion:** Completa (ver `/docs`)
- **Decisiones confirmadas:** [DECISIONES.md](docs/04_operacional/DECISIONES.md)

## Metricas del MVP

| Metrica | Objetivo |
|---------|----------|
| Talleres registrados | 20 |
| Marcas registradas | 10 |
| Pedidos iniciados | 30 |
| Pedidos completados | 15 |
| Presupuesto | $20,000 USD |
| Timeline | 2 meses dev + 3 meses piloto |
| Pantallas | 70 + 6 modales |

## Las 5 Funciones del MVP

1. **REGISTRAR** - Alta y verificacion de talleres, marcas y trabajadores
2. **ENCONTRAR** - Matching talleres <-> marcas por capacidad, ubicacion y certificacion
3. **APRENDER** - Capacitacion contextual para formalizacion y buenas practicas
4. **ACOMPANAR** - Checklist guiado de formalizacion (ex COMPLIANCE)
5. **FISCALIZAR** - Priorizacion de inspecciones con datos de la plataforma

## Stack Tecnologico

| Capa | Tecnologia |
|------|------------|
| Framework | Next.js 16 |
| Lenguaje | TypeScript |
| Estilos | Tailwind CSS v4 |
| ORM | Prisma 6 |
| Base de datos | PostgreSQL (Supabase) |
| Autenticacion | NextAuth v5 |
| Deploy | Vercel |
| WhatsApp | wa.me click-to-chat (sin API) |

**Integraciones estatales:**
- AFIP/ARCA (Web Services)
- ANSES

## Estructura del Proyecto

```
MVP_DESARROLLO/
├── README.md
├── docs/
│   ├── 01_estrategia/              # Capa 1: Por que
│   │   └── 01_CONTEXTO.md          # Problema, actores, barreras
│   ├── 02_funcional/               # Capa 2: Que
│   │   ├── 02_FUNCIONES.md         # Las 5 funciones del MVP
│   │   ├── 03_CASOS_USO.md         # Casos de uso prioritarios
│   │   ├── 07_COMUNICACION.md      # Canales y notificaciones
│   │   └── PANTALLAS_MVP.md        # 70 wireframes ASCII con specs
│   ├── 03_tecnico/                 # Capa 3: Como
│   │   ├── 05_ARQUITECTURA.md      # Stack y modelo de datos
│   │   ├── 06_INTEGRACIONES.md     # AFIP/ARCA, ANSES
│   │   ├── 08_PLAN_DESARROLLO.md   # Plan tecnico fase por fase
│   │   └── DESIGN_SYSTEM.md        # Tokens, tipografia, colores
│   ├── 04_operacional/             # Capa 4: Donde estamos
│   │   ├── CHECKLIST.md            # Estado real (fuente de verdad)
│   │   ├── DECISIONES.md           # Decisiones confirmadas
│   │   └── 04_HOJA_RUTA.md         # Cronograma y presupuesto
│   └── auditoria/                  # Diagnostico tecnico
│       ├── AS_IS_MAP.md            # Estado actual del codigo
│       ├── TO_BE_MAP.md            # Estado objetivo
│       ├── GAP_MATRIX.md           # Brechas AS-IS vs TO-BE
│       └── ROADMAP_REMEDIACION.md  # Plan de remediacion
├── prototipo/                      # Prototipo HTML original
└── planteos_scrape/                # Scraping de planteos textiles
```

## Documentacion por Capa

### Capa 1 - Estrategia (Por que)
| Documento | Descripcion |
|-----------|-------------|
| [01_CONTEXTO](docs/01_estrategia/01_CONTEXTO.md) | Problema, 8 actores, 7 barreras |

### Capa 2 - Funcional (Que)
| Documento | Descripcion |
|-----------|-------------|
| [02_FUNCIONES](docs/02_funcional/02_FUNCIONES.md) | Las 5 funciones del MVP |
| [03_CASOS_USO](docs/02_funcional/03_CASOS_USO.md) | 10 casos de uso prioritarios |
| [07_COMUNICACION](docs/02_funcional/07_COMUNICACION.md) | Canales, WhatsApp, notificaciones |
| [PANTALLAS_MVP](docs/02_funcional/PANTALLAS_MVP.md) | 70 wireframes ASCII con specs |

### Capa 3 - Tecnica (Como)
| Documento | Descripcion |
|-----------|-------------|
| [05_ARQUITECTURA](docs/03_tecnico/05_ARQUITECTURA.md) | Stack y modelo de datos |
| [06_INTEGRACIONES](docs/03_tecnico/06_INTEGRACIONES.md) | AFIP/ARCA, ANSES |
| [08_PLAN_DESARROLLO](docs/03_tecnico/08_PLAN_DESARROLLO_TECNICO.md) | Plan tecnico fase por fase |
| [DESIGN_SYSTEM](docs/03_tecnico/DESIGN_SYSTEM.md) | Tokens, tipografia, colores |

### Capa 4 - Operacional (Donde estamos)
| Documento | Descripcion |
|-----------|-------------|
| [CHECKLIST](docs/04_operacional/CHECKLIST.md) | Estado real de cada pantalla/API |
| [DECISIONES](docs/04_operacional/DECISIONES.md) | Registro de decisiones confirmadas |
| [04_HOJA_RUTA](docs/04_operacional/04_HOJA_RUTA.md) | Cronograma y presupuesto |

## Los 8 Actores

1. Talleres y Cooperativas
2. Marcas de Indumentaria
3. Trabajadores Textiles
4. Federaciones (FACTA)
5. Sindicatos (SOIVA)
6. Estado (MTEySS, AFIP, ANSES)
7. Certificadores (Vestir Conciencia)
8. Consumidores Finales

## Las 7 Barreras que Resuelve

| # | Barrera | Solucion |
|---|---------|----------|
| B1 | Falta de Trazabilidad | Registro verificable en tiempo real |
| B2 | Desconfianza entre Actores | Reputacion transparente y publica |
| B3 | Formalizacion Compleja | Checklist automatizado con ayuda |
| B4 | Falta de Articulacion | Dashboard compartido entre actores |
| B5 | Estado Ausente | Datos e IA amplifican fiscalizacion |
| B6 | Bajas Capacidades | Cursos contextuales gratuitos |
| B7 | Dumping Social | Transparencia nivela la cancha |

## Repositorios

| Repo | Contenido |
|------|-----------|
| [gbreard/textil-mvp](https://github.com/gbreard/textil-mvp) | Documentacion y especificaciones |
| [GIDs/Textil_mvp](https://github.com/GIDs/Textil_mvp) | Codigo fuente de la aplicacion |

## Como Contribuir

1. Revisar [DECISIONES.md](docs/04_operacional/DECISIONES.md) antes de cualquier cambio
2. Revisar documentacion en `/docs` (organizada en 4 capas)
3. Ver app desplegada en [pdt-nine.vercel.app](https://pdt-nine.vercel.app)
4. Proponer cambios via Pull Request

## Licencia

Por definir (probablemente Open Source)
