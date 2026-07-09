---
title: Integra
created: 2026-07-09
updated: 2026-07-09
type: entity
tags: [integra, autorizacion, auditoria, crm]
sources: [raw/notion/integra.md]
confidence: medium
---

# Integra

Sistema construido sobre Salesforce que reemplaza a Fluir para la gestión de autorizaciones y auditoría médica de prestaciones ambulatorias (F4).

## Estado de implementación

- Cobertura actual: 85% de casos ambulatorios (F4) implementados en Integra.
- Vías de ingreso: 85% vía equipo administrativo de autorizaciones (Dirección de Operaciones), 15% vía equipo de experiencia en los CARs, 1% remanente sigue en Fluir (excepciones fuera de alcance).
- Cobertura esperada completa (ambulatorio + internación): febrero.
- Casos que permanecen en Fluir: trasplantes, bariátrica, medicamentos de autorización previa, excepciones.

## Estructura (dos procesos principales)

- **Autorizaciones**: liderado por Vicky Costa Maña (Dirección de Operaciones). Gestión migrada de Fluir a Salesforce, incluye autorización automática por [[reglas]]. Genera caso padre.
- **Auditoría médica**: liderado por Fernando. Casos que requieren auditoría generan caso hijo automáticamente. Antes no existía reportería propia de auditoría.

## Mejoras implementadas

- Diagnósticos: búsqueda vía servidor de terminología SNOMED con vinculación automática a CIE-10, validación obligatoria del auditor médico antes de cerrar el caso.
- Solicitud de documentación al asociado directamente desde el sistema (mail automático, seguimiento 48h + 24h adicionales, cierre automático si no se recibe documentación — todavía mejorable).
- Trazabilidad de solicitante (obligatorio) y actuante (no obligatorio, tema de proceso más que de sistema).

## Problemas de calidad de datos (Tablero Operativo Ambulatorio)

- Datos hasta nov/dic vienen de sistemas viejos.
- Ranking de acreedores y prescribientes con alto porcentaje de datos faltantes o mal cargados (códigos genéricos como P9999, P0, "no definido en origen"). Mejora observada en enero pero el tablero necesita revisión para capturar bien los datos de Integra.
- Proceso de "sujeto a auditoría posterior" está roto/informal: no hay vinculación caso a caso con auditoría de facturación, solo una sugerencia de débito que se deriva por fuera del CRM. Falta definir criterio formal de cuándo auditoría de autorización debe derivar a auditoría de facturación.

## Relaciones

- Genera datos para [[control-prestacional]]
- Autorización automática vía [[reglas]]
- Relacionado con [[puntos-de-control]] y [[auditoria-medica-facturacion]]
