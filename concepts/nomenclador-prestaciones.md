---
title: Nomenclador de Prestaciones
created: 2026-07-09
updated: 2026-07-09
type: concept
tags: [nomenclador]
sources: [raw/notion/prestaciones.md, notion_export/Prestaciones (la revancha del regreso recargado)]
confidence: high
---

# Nomenclador de Prestaciones

Catálogo de códigos que identifica cada práctica médica en SanCor Salud. Es el objeto/resultado esperado del [[proyecto-nuevo-nomenclador]]: hoy está fragmentado en ~25 nomencladores distintos (35.000+ códigos) sin gobernanza; el proyecto busca convertirlo en un **maestro prestacional único, normalizado y gobernado**.

## Definiciones clave

- **Maestro prestacional**: nomenclador único con un código por cada práctica médica, independiente del convenio o forma de pago — separa la codificación clínica de la lista de precios.
- **Criterio de nomenclatura**: estructura estandarizada para nombrar prestaciones, definiendo el nivel de especificidad necesario según la especialidad (ej. práctica + vía de abordaje en cirugía; práctica + parte anatómica en traumatología).
- **Homologación vs. codificación**: separar qué es una práctica médica (codificación/nomenclatura) de cómo se negocia comercialmente con cada prestador (homologación, valores, materiales, módulos).

## Problemas del estado actual

- Multiplicidad de códigos para la misma práctica, y códigos genéricos que agrupan prácticas distintas (ambigüedad dual).
- Códigos que mezclan práctica clínica con negociación comercial.
- Sin dueño claro del catálogo → falta de gobernanza, homologaciones inconsistentes entre prestadores.
- Dependencia de tecnología legacy (S400) que limita el control sobre la estructura de datos.

## Uso como referencia

- Referenciado también en discusiones de [[auditor-ai]] sobre la dificultad de que una misma cirugía tenga múltiples códigos asociados, lo que complica buscar casos históricos.
- Es insumo clave del proyecto de Autorizaciones Inteligentes (identificación automática del código correcto a partir del texto libre de un pedido médico).

## Relaciones

- Impulsado por [[proyecto-nuevo-nomenclador]]
- Relevante para [[auditor-ai]] e [[integra]]
