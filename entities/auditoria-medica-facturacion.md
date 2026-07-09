---
title: Auditoría Médica de Facturación (AMF)
created: 2026-07-09
updated: 2026-07-09
type: entity
tags: [auditoria, facturacion, controles]
sources: [raw/notion/auditoria-post-facturacion.md, notion_export/Jornada auditoría médica de facturación - AMF (Contrataciones y GE)]
confidence: medium
---

# Auditoría Médica de Facturación (AMF)

Auditoría que se realiza sobre la facturación de prestaciones, después de la liquidación (a diferencia de la auditoría previa a la autorización). Antes dependía de DAF; la liquidación de prestaciones pasó a Subgerencia Operativa, que genera el CP (cursograma de pagos) para que AMF audite.

> Nota: renombrada desde "Auditoría post facturación" — mismo concepto, nombre alineado al usado en la jornada de trabajo de Contrataciones y GE.

## Proceso

- El prestador tiene por ley hasta 2 años para presentar la factura. SanCor Salud decidió no imponer un límite más corto (por riesgo de impericia) para priorizar la carga.
- Flujo: liquidación de prestaciones → genera CP → AMF audita.
- Consultas no se auditan; odontología e internación domiciliaria hoy tampoco pasan por AMF.
- T46: listado ponderado de prestadores por facturación — identifica el 95% que más factura para priorizar foco de auditoría.

## Problemas identificados

- **Formato de recepción de detalles de facturación**: es lo que más tiempo consume del proceso. Stefi asumió como nueva referente en este tema.
- **ODM (bandeja) de medicamentos y descartables**: requiere cuentas manuales para verificar necesidad.
- **Recepción de facturas**: no se controla documentación respaldatoria ni desfasajes de montos (tema pendiente con Seba y Franco). La documentación respaldatoria no es digital — se está explorando un digitalizador vía SAP.
- Preguntas abiertas: qué se puede automatizar y qué no; complementariedad entre ECP y AMF para auditar solo lo que no se pueda automatizar; cuánto tiempo se invierte en analizar vs. en impactar la información (pregunta de Belu).
- Cómo alimentar la variable de origen de débito: médico, administrativo, manual o automático.

## Relaciones

- Vinculado a [[puntos-de-control]]
- Colabora con [[mitigacion-riesgos]]
- Requerido por [[anestesia-online]]
- Relacionado con [[integra]] (cierre de casos hijos de auditoría)
