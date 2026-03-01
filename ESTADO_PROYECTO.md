# Estado del Proyecto - MVP Plataforma Textil

> Última actualización: 28 de Febrero 2026

---

## Resumen Ejecutivo

**Proyecto:** Plataforma Digital Textil para OIT/UNTREF
**Presupuesto:** $20,000 USD (DEC-001)
**Timeline:** 5 meses (2 desarrollo + 3 piloto) (DEC-006)
**Stack:** Next.js 16 + TypeScript + Tailwind v4 + Prisma 6 + PostgreSQL (Supabase) + NextAuth v5 + Vercel
**Estado:** Sprint 1 completado. App desplegada en https://pdt-nine.vercel.app

---

## Lo que está listo

### Documentación Completa

| Archivo | Contenido | Estado |
|---------|-----------|--------|
| `docs/01_CONTEXTO.md` | Diagnóstico del sector | ✅ |
| `docs/02_FUNCIONES.md` | Funcionalidades del MVP | ✅ |
| `docs/03_CASOS_USO.md` | Casos de uso por actor | ✅ |
| `docs/04_HOJA_RUTA.md` | Cronograma 36 días | ✅ |
| `docs/05_ARQUITECTURA.md` | Stack técnico, modelo datos | ✅ |
| `docs/06_INTEGRACIONES.md` | AFIP, WhatsApp, Email | ✅ |
| `docs/07_COMUNICACION.md` | - | ✅ |
| `docs/08_PLAN_DESARROLLO_TECNICO.md` | **Plan técnico detallado fase por fase** | ✅ NUEVO |
| `PROPUESTA_OIT_REESTRUCTURADA.md` | Propuesta formal completa | ✅ |

### Diseño UI/UX

| Archivo | Contenido | Estado |
|---------|-----------|--------|
| `design/PANTALLAS_MVP.md` | **70 pantallas + 6 modales** con wireframes ASCII | ✅ |
| `design/DESIGN_SYSTEM.md` | Colores, tipografía, componentes | ✅ |
| `design/components/` | Componentes React de ejemplo | ✅ |

### Recursos para Cursos

| Archivo | Contenido | Estado |
|---------|-----------|--------|
| `planteos_scrape/docs/RECURSOS_CURSOS.md` | Links INTI, INET, OIT, Fundar + estructura de 5 cursos | ✅ NUEVO |

---

## Estado de Desarrollo

### Sprint 1 - COMPLETADO (2026-02-25)
- Seguridad API (auth + ownership en todos los endpoints)
- Password reset completo (API + email + página)
- Wizard perfil taller conectado a BD
- Upload de documentos con Supabase Storage
- Motor de cálculo de nivel BRONCE/PLATA/ORO
- Admin detalle taller con aprobación/rechazo de documentos

### Próximo: Sprint 2 - Integraciones core
Ver `docs/CHECKLIST.md` para detalle completo de estado y sprints.

---

## Estructura de Archivos del Proyecto

```
/MVP_DESARROLLO
├── docs/
│   ├── 01_CONTEXTO.md
│   ├── 02_FUNCIONES.md
│   ├── 03_CASOS_USO.md
│   ├── 04_HOJA_RUTA.md
│   ├── 05_ARQUITECTURA.md
│   ├── 06_INTEGRACIONES.md
│   ├── 07_COMUNICACION.md
│   └── 08_PLAN_DESARROLLO_TECNICO.md    ← Plan técnico detallado
├── planteos_scrape/
│   ├── design/
│   │   ├── PANTALLAS_MVP.md              ← 70 pantallas con wireframes
│   │   ├── DESIGN_SYSTEM.md
│   │   └── components/                   ← Componentes React ejemplo
│   └── docs/
│       └── RECURSOS_CURSOS.md            ← Material para Academia
├── prototipo/                            ← Maqueta HTML existente
├── PROPUESTA_OIT_REESTRUCTURADA.md
├── ESTADO_PROYECTO.md                    ← ESTE ARCHIVO
└── README.md
```

---

## Decisiones Técnicas Confirmadas

| Aspecto | Decisión |
|---------|----------|
| Frontend + Backend | Next.js 16 (App Router) |
| Base de datos | PostgreSQL via Supabase |
| Auth | NextAuth.js |
| Deploy | Vercel Pro ($20/mes) |
| Verificación CUIT | Afip SDK |
| Email | SendGrid |
| WhatsApp | Click-to-chat (wa.me) |
| IA en desarrollo | Claude (pagado por devs) |

---

## Pantallas Diseñadas (70 + 6 modales)

### Por Sección

| Sección | Cantidad |
|---------|----------|
| Autenticación | 5 |
| Taller | 5 |
| Marca | 2 |
| Estado | 2 |
| Públicas | 5 |
| Sistema | 4 |
| Onboarding | 1 |
| Admin | 34 |
| **Wizard Perfil Productivo** | **12** |
| **TOTAL** | **70 + 6 modales** |

### Wizard Perfil Productivo (nuevo)

Pantallas 59-70 con flujo pedagógico para que talleres carguen:
- Maquinaria
- Equipo (cantidad, experiencia)
- Organización del trabajo
- Espacio físico
- SAM (tiempos por prenda)
- Eficiencia
- Gestión
- Score final con comparativa

---

## Recursos Investigados para Cursos

| Fuente | Material |
|--------|----------|
| INTI | Guías 5S, Kaizen, Buenas Prácticas |
| INET | Perfiles profesionales (PDFs) |
| OIT | Campaña #Formalicemos, Proyecto EvA |
| Fundar | Plan de Acción Textil 2024 |

**5 cursos sugeridos:**
1. Organizá tu Taller (5S)
2. Competencias del Confeccionista
3. Medí tu Eficiencia
4. Camino a la Formalización
5. Certificaciones y Valor Agregado

---

## Para Continuar

1. **Leer** `docs/DECISIONES.md` - registro de todas las decisiones confirmadas
2. **Leer** `docs/CHECKLIST.md` - estado detallado de cada pantalla y API
3. **Ver** la app desplegada en https://pdt-nine.vercel.app

### Repositorios

| Repo | Contenido |
|------|-----------|
| `GIDs/textil-mvp` | Documentación y planificación |
| `GIDs/Textil_mvp` | Código Next.js (app desplegada) |

---

## Contacto Proyecto

- **Coordinación:** Matías Crespo (OIT/UNTREF)
- **Desarrollo:** Sergio Rodriguez, Gerardo Breard
