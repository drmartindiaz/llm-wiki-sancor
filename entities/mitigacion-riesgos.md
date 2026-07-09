---
title: Mitigación de Riesgos (SMR)
created: 2026-07-08
updated: 2026-07-09
type: entity
tags: [mitigacion-riesgos, fraude, controles]
sources: [raw/notion/mitigacion-de-riesgos-smr.md, notion_export/Mitigación de Riesgos (SMR)]
confidence: high
---

# Mitigación de Riesgos (SMR)

Sector de Control Prestacional enfocado en detectar y prevenir fraude, abuso y desperdicio en las prestaciones. En abril de 2026 se discutió renombrarlo (se descartó "Vigilancia de Riesgos Prestacionales" y quedó como **"Riesgos Prestacionales"**, quitando la palabra "mitigación" que limitaba la percepción de su alcance) — el nombre no está aún consolidado en toda la organización.

Equipo actual (2026): Caro (analista), Diego (analista), y una vacante que se buscó cubrir con perfil operativo/administrativo (se descartó reforzar el perfil legal tras la salida de Meli/Lucía).

## Origen: célula de fraude

- Se creó a partir de un caso en Entre Ríos (2023): un asociado adulteró facturas de kinesiología y recibió reintegros por ~900 sesiones, sin que existiera punto de control que limitara la cantidad reintegrable. Conectividad alertó por consumos extraordinarios.
- De ahí surgió la "marca de reintegro sospechoso": los asociados marcados no son fidelizables (no se les ofrecen bonificaciones ni retención).
- Los casos llegan desde múltiples fuentes (reintegros, legales, auditoría médica, ADP) al correo institucional de mitigación de riesgo, y se informan a la célula de fraude (que se reúne cada 15 días o ante casos graves).
- Resultado citado: asociados marcados pasaron de un costo de salud ~900% superior al normal a un costo contenido.

## Evolución del enfoque (2025-2026)

- **Reactivo → proactivo**: el trabajo histórico es reactivo (responder denuncias). Desde 2026 se buscó pasar a un enfoque proactivo: monitoreo sistemático de prestaciones (ej. ecografías, ecodoppler), detección de patrones de "mapeo" (múltiples prestaciones el mismo día al mismo paciente), y scoring de riesgo estilo seguros (auto/hogar), inspirado en casos como predicción de fraude aduanero.
- Casos de referencia: fonoaudióloga de Santa Fe que facturaba a su propio grupo familiar; dermatólogas de Tucumán con fraude estimado en ~50M$/año; caso de desconocimiento de medicamentos en Tucumán.
- **Proceso de "desconocimiento de consumos"** (marzo-noviembre 2025): 38 casos evaluados, ahorro total de solo $64.000 — el equipo concluyó que el ahorro no justificaba el trabajo invertido y se discutió directamente eliminarlo o rediseñarlo.
- **Bajo volumen de casos**: 23 casos procesados en el último año (~2/mes). Diagnóstico: el problema no es capacidad sino falta de *input* — la organización no conoce bien qué hace el área ni cómo derivarle casos. Se decidió trabajar en comunicación interna ("marketing" del área) usando el lenguaje fraude / abuso / desperdicio.

## Herramientas de seguimiento

- Evolución: planilla propia del sector → "Padre" (herramienta unificada con otros sectores desde 2024, perdió adherencia) → propuesta de nueva matriz (2026) con campos de ID, usuario informante, hallazgo, riesgo, nomenclador, prioridad, acción, estado e impacto.
- Se evaluó migrar el seguimiento a Salesforce/CRM en lugar de Excel o Jira.

## Rol nuevo: Auditor de Reglas

- Propuesto por Martín como rol transversal (no exclusivo de este sector) para monitorear sistemáticamente el impacto de reglas y puntos de control ya implementados — hoy no existe ese seguimiento post-implementación.
- Ver [[auditor-reglas]] para el detalle del rol.

## Relaciones

- Reporta a [[control-prestacional]]
- Colabora con [[auditoria-medica-facturacion]]
- Colabora con [[puntos-de-control]]
- Distinto de, pero relacionado con [[gestion-de-riesgos]] (área corporativa de riesgos, gerencia de Bettina Corbalá — la célula de fraude coordinaba antes con Lucía, que pasó a Riesgo de Compliance bajo esa gerencia)
- Da origen al rol [[auditor-reglas]]
- Interactúa con [[conectividad]] (alertas de consumo) y [[experiencia]] (comunicación con asociados)
