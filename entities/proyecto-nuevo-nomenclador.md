---
title: Proyecto Nuevo Nomenclador
created: 2026-07-09
updated: 2026-07-09
type: entity
tags: [nomenclador, motor-reglas]
sources: [raw/notion/prestaciones.md, notion_export/Prestaciones (la revancha del regreso recargado)]
confidence: high
---

# Proyecto Nuevo Nomenclador

Proyecto para reemplazar el sistema fragmentado de nomencladores de SanCor Salud por un maestro prestacional único, normalizado y gobernado: [[nomenclador-prestaciones]].

## Diagnóstico

- El sistema actual está fragmentado en **~25 nomencladores distintos** (médico, odontológico, medicamentos, insumos/prótesis, descartables y otros creados ad hoc) con más de **35.000 códigos**, generados sin gobernanza a lo largo del tiempo.
- Ambigüedad dual: existen múltiples códigos para una misma práctica, y a la vez códigos genéricos que agrupan prácticas muy distintas.
- No hay un dueño claro del catálogo, lo que genera desconexión entre autorización, realización y liquidación, y variabilidad en cómo cada prestador homologa la misma prestación.
- Se identificaron vicios concretos: códigos que mezclan práctica médica con negociación comercial (materiales, prótesis, módulos), y códigos duplicados por convenio (N, NBU, NB) en lugar de por práctica.

## Objetivo y principios

- Crear un único código por práctica médica, independiente del convenio o forma de pago — separando la codificación clínica de la lista de precios.
- Prueba de concepto con el capítulo de urología (2 días de trabajo) usando SNOMED + nomenclador nacional + nomenclador de la Sociedad Argentina de Urología como fuentes, limpiando duplicados y prácticas obsoletas.
- Principio de creación de código: se justifica un código nuevo cuando hay necesidad de uso diferencial (metodología, parte del cuerpo, insumos, efectividad, indicación clínica) — el precio no es criterio suficiente por sí solo.
- Invertir la lógica de homologación: en vez de adaptar el nomenclador de Sancor al de cada prestador, el prestador homologa contra el nomenclador único de Sancor.

## Metodología (3 fases + homologación regional)

1. **Trabajo interno**: unificar nomenclador Sancor actual + nomenclador de la especialidad + nomenclador nacional en una "radiografía" que cubra el 100% de los procedimientos existentes.
2. **Trabajo con especialistas** (vía consultora externa): revisión código por código, identificación de obsoletos y faltantes.
3. **Revisión y validación** interna (liderada por Maxi).
4. **Homologación regional**: ajuste de particularidades por zona con prestadores (ej. cirugía endoscópica de fosas nasales varía según disponibilidad de endoscopios por región).

## Selección de consultora

- Se evaluó a IECS (Ezequiel García Lorio) para tercerizar la búsqueda y coordinación de especialistas médicos por especialidad — no la definición de criterios, que queda en el equipo interno.
- Plan B explorado en paralelo: conseguir nomencladores de referencia (Hospital Alemán, Hospital Italiano, San Juan, OSDE) y evaluar proveedores alternativos (Easy Salud/New Leasing, Global Action).
- A julio 2026 (20260708): en proceso de selección de consultora — tres empresas presentaron propuestas con estimaciones mínimas de **6 meses de trabajo**.

## Alcance

- **Incluido**: prestaciones médicas por especialidad.
- **Excluido inicialmente**: laboratorio clínico, imágenes diagnósticas, medicamentos (vademécum), prótesis.
- No incluye en esta etapa la definición de la herramienta tecnológica ni integraciones — el foco es el maestro prestacional conceptual. Se descartó construirlo sobre S400 (no hay control sobre esa tecnología, no se pueden generar tablas en DB2).

## Relación con Autorizaciones Inteligentes / Auditor AI

- Existe un proyecto paralelo de **Autorizaciones Inteligentes**: reemplazar con IA el trabajo hoy manual de +20 personas de Prácticas Médicas Ambulatorias, que interpretan el pedido médico y determinan el código de prestación correcto antes de cargarlo en [[integra]].
- El nomenclador es insumo clave para ese proyecto (y para [[auditor-ai]]): su metadata y sinonimias determinan la calidad de identificación de códigos. Pero no lo bloquea — Autorizaciones Inteligentes avanza con un "set de reglas" interim sobre el nomenclador actual mientras se construye el maestro prestacional.
- Una vez identificado el código correcto, la homologación con el prestador queda mayormente resuelta por el sistema de convenios existente.

## Relaciones

- Objeto del proyecto: [[nomenclador-prestaciones]]
- Insumo para [[auditor-ai]] e [[integra]]
- Vinculado a [[reglas]] (motor de reglas) y a la revisión de altas de prestaciones en convenios nuevos
