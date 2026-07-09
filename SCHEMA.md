# Wiki Schema

## Domain
Control Prestacional en SanCor Salud — gestión estratégica de prestaciones médicas, políticas de cobertura, auditoría, reglas, autorizaciones, y proyectos de transformación digital en una empresa de medicina prepaga/obra social en Argentina.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `politicas-cobertura.md`)
- Every wiki page starts with YAML frontmatter (see below)
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/notion/page-name.md]
confidence: high | medium | low
---
```

## Tag Taxonomy
- **Estructura**: equipo, organigrama, puesto, area, direccion, gerencia
- **Procesos**: politica-cobertura, autorizacion, auditoria, facturacion, debitos, reglas, controles
- **Proyectos**: motor-reglas, anestesia-online, buscador-prestaciones, coseguros, nomenclador, integra
- **Sistemas**: as400, motor, autogestor, crm, tablero, microstrategy
- **Prestaciones**: consultas, cirugia, medicamentos, laboratorio, imagenes, salud-mental, internacion
- **Stakeholders**: comercial, gerencia-medica, sistemas, proveedores, asociados
- **Meta**: reunion, seguimiento, planificacion, indicadores, objetivos

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources or is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions, minor details, or things outside the domain
- **Split a page** when it exceeds ~200 lines

## Update Policy
When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark `contested: true` in frontmatter
4. Flag for user review
