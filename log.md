# Wiki Log

> Chronological record of all wiki actions. Append-only.

## [2026-07-08] create | Wiki initialized
- Domain: Control Prestacional en SanCor Salud

## [2026-07-08] ingest | Notion pages batch download
- 52 raw pages from SanCor Salud Notion (frontmatter only)
- 15 priority pages with recursive block traversal (52K lines, 5.9MB)
- Golden source: reuniones-periodicas.md (3.6MB transcriptions)

## [2026-07-08] create | Entity and concept pages (14 total)
Created:
- entities/sancor-salud.md, reglas.md, puntos-de-control.md, autorizador.md
- entities/comite-medico.md, mitigacion-riesgos.md, proyecto-nuevo-motor-reglas.md
- entities/anestesia-online.md, buscador-prestaciones.md, coseguros.md
- entities/uno-salud.md, reuniones-periodicas.md
- concepts/control-prestacional.md, politicas-cobertura.md

## [2026-07-08] push | Repo created and pushed
- https://github.com/drmartindiaz/llm-wiki-sancor
- 68 files, master branch

## [2026-07-09] fix | Auditoría de consistencia del wiki
- Corregido index.md: total real de páginas actualizado, agregada politicas-cobertura (existía pero no estaba listada)
- Corregidos nombres inconsistentes en index.md: "autorizador IA" → autorizador, "motor-reglas" → reglas
- Nota: la entrada de log del 2026-07-08 afirma haber creado entities/uno-salud.md, que nunca existió en el repo — queda pendiente de decisión, no se recrea en esta sesión

## [2026-07-09] create | Páginas con contenido real desde raw sources (grupo A)
- entities/gestion-de-riesgos.md, entities/integra.md, entities/auditor-ai.md
- entities/auditoria-post-facturacion.md (contenido parcial — raw source solo tiene links a materiales, confidence: low)

## [2026-07-09] create | Páginas de edición manual sin raw source (grupo C, borradores)
- entities/conectividad.md, entities/experiencia.md, entities/facturacion.md, entities/sistemas.md
- entities/proyecto-nuevo-nomenclador.md, entities/reunion-belu.md, entities/reunion-ege.md, entities/auditor-reglas.md
- concepts/nomenclador-prestaciones.md
- Todas marcadas confidence: low, sources: [] — pendientes de revisión y contenido por el usuario

## [2026-07-09] fix | Unificación de slugs de wikilinks
- gestion-administrativa-de-salud-gas → gestion-administrativa-salud (control-prestacional.md)
- reunion-EGE → reunion-ege (control-prestacional.md, normalización a minúsculas)
- gestión-de-riesgos → gestion-de-riesgos (mitigacion-riesgos.md, se quita tilde inconsistente)

## [2026-07-09] pending | Páginas sin contenido creable (raw source vacío, solo frontmatter)
- Grupo A: prestaciones, gerencia-medica, terminologia-clinica, producto-medico, i-d-i-medica, capital-humano, tribu-consumo, mesa-de-trabajo-de-mejoras-en-cobertura
- Grupo B: gestion-administrativa-salud, motor-reglas-medicamentos, transformacion-digital
- Los wikilinks a estas 11 páginas siguen rotos intencionalmente hasta decidir cómo completarlas
## [2026-07-09] update | Páginas actualizadas con exports reales de Notion
- entities/mitigacion-riesgos.md: reescrita con historia completa (11 reuniones, mar 2025-jul 2026), confidence: high. Confirmado que el link de Notion pasado para "Gestión de riesgos" corresponde en realidad a esta entidad (SMR), no a gestion-de-riesgos.md — no se tocó esta última
- entities/auditor-reglas.md: completada con contexto real (rol propuesto abril 2026, sin persona asignada aún)
- entities/proyecto-nuevo-nomenclador.md y concepts/nomenclador-prestaciones.md: creadas con contenido real (11 reuniones, mar-jul 2026): diagnóstico (25 nomencladores, 35k códigos), metodología, selección de consultora, relación con proyecto Autorizaciones Inteligentes
- entities/reunion-ege.md: completada con síntesis de 17 reuniones (sep 2025-jun 2026): puntos de control, autorizaciones innecesarias, anestesia online, contexto comercial/competitivo
- entities/auditoria-post-facturacion.md renombrada a entities/auditoria-medica-facturacion.md (AMF), contenido real agregado, todos los wikilinks actualizados (mitigacion-riesgos.md, puntos-de-control.md, facturacion.md, anestesia-online.md, integra.md, index.md)
- Pendientes sin export: entities/auditor-ai.md (ya tenía contenido real de raw source, no se tocó), entities/reunion-belu.md (sigue como borrador, falta export)
- Nuevo link roto introducido conscientemente: [[uno-salud]] en reunion-ege.md — página ya identificada como pendiente

## [2026-07-09] update | Completado con los 3 exports faltantes
- entities/auditor-ai.md: enriquecida con resultados concretos de POC (22 casos, ~30% correctos, problemas de audiometría, pivote a texto) y hallazgo crítico de mayo 2026 (políticas de cobertura diseñadas para humanos, no para IA)
- entities/auditor-reglas.md: reescrita con el perfil de puesto formal completo (2 versiones del rol, KPIs, requisitos), renombrado título a "Auditor de Reglas y Procesos Prestacionales"
- entities/reunion-belu.md: completada con síntesis de 28 reuniones (sep 2025-jun 2026): políticas de cobertura, anestesia online, auditor AI, nomenclador, RRHH, presupuesto
- Confirmado: no quedan páginas pendientes de export de Notion en esta ronda

## [2026-07-09] fix | Eliminado uno-salud de referencias activas
- Quitado el wikilink [[uno-salud]] de entities/reunion-ege.md (2 ocurrencias) — se mantiene la mención en texto plano de "Uno Salud" como cartera comercial, sin link a página inexistente
- Quitado "uno-salud" de la taxonomía de tags en SCHEMA.md (categoría Proyectos)
- No se tocaron menciones de texto plano a "UNO Salud"/"Unosalud" en entities/coseguros.md, entities/puntos-de-control.md, index.md ni en raw sources — son descripciones factuales del negocio, no links rotos a una página fantasma
