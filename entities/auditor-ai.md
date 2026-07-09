---
title: Auditor AI
created: 2026-07-09
updated: 2026-07-09
type: entity
tags: [autorizador-ia, auditoria, autorizacion]
sources: [raw/notion/auditor-ai.md, notion_export/Auditor AI]
confidence: high
---

# Auditor AI

Proyecto de agente de IA que procesa casos de autorización después del motor de reglas ([[reglas]]) y antes del auditor humano, para casos que hoy se autorizan siempre.

## Contexto

- 81-85% de los socios consumen sin requerir autorización. Del 15-19% que sí tramita, solo al 15% se le niega (85% se aprueba).
- SLA actual: 24h carga inicial + 48h auditoría médica = 3 días totales, percibido como excesivo por los socios aunque se cumpla.

## Problemas identificados

- Velocidad de respuesta percibida como lenta pese a cumplir SLA.
- Falta de gestión activa del "no" con prestadores que insisten en prácticas no autorizables.
- Carga administrativa de los auditores médicos, con poco tiempo para discusión médica real con prestadores.

## Solución propuesta

- Agente IA que lee documentos adjuntos (resúmenes de historia clínica, informes PDF) y decide en modo binario: **autoriza** o **deriva al auditor humano** (nunca rechaza directamente).
- Objetivo: automatizar al menos el 50% del 85% de casos que hoy siempre se autorizan, con meta de concordancia >95% respecto al criterio del auditor.
- Arranca con 10 prácticas seleccionadas por Gastón (más frecuentes / más automatizables).
- Modelo usado en las pruebas: Gemini 2.5 (Google, por costo/disponibilidad frente a versiones más nuevas), con capacidad de interpretación de imágenes.

## Resultados de las primeras corridas (POC)

- Primera corrida: 22 casos procesados, solo ~30% (o menos) con resultado correcto.
- **Inconsistencia**: el mismo caso ejecutado 3 veces dio resultados distintos (aprobado vs. pendiente) a pesar de usar temperatura cero.
- **Problema técnico principal**: interpretación de audiometrías. Desfasajes de 20-30 decibeles entre valores detectados por la IA y los gráficos reales; dificultad marcada cuando vía aérea y vía ósea se superponen en el mismo gráfico (círculos, X y cruces solapados).
- Solución de preprocesamiento desarrollada: recortar cada estudio individualmente y hacer una llamada separada por estudio/lateralidad (6 prompts específicos), en vez de mandar el archivo completo — mejoró la consistencia pero exige más mantenimiento.
- **Cambio de enfoque**: el equipo decidió pivotar de interpretación de imágenes a interpretación de texto/informes, ya que la mayoría de los casos de auditoría se basan en informes textuales y no en lectura directa de gráficos.
- Segunda corrida (con política de septumplastia más flexible): la corrida anterior había rechazado casi todos los casos porque la política escrita era más estricta de lo que los prestadores documentan en la práctica real (ej. exigir la palabra "severa" en la deformidad, o especificar tratamiento conservador previo — cosas que rara vez se documentan así). Se decidió que la política debe reflejar lo que el auditor humano realmente usa, sin adaptarse a documentación faltante del prestador (eso se resuelve educando al prestador, no flexibilizando la IA).

## Actualización crítica (mayo 2026)

- Incluso llevando la política de cobertura al mínimo de exigencia posible, el agente seguía sin funcionar bien.
- **Diagnóstico de fondo**: las políticas de cobertura están escritas para que las apliquen humanos, con criterio y flexibilidad contextual — no para una IA que no pondera múltiples factores simultáneamente.
- Se evaluó reducir el piloto a una prestación con menos requisitos. Lectura pesimista que surgió en el equipo: el enfoque podría servir para autorización pero no necesariamente para auditoría propiamente dicha.

## Extensión: Autorizaciones AI / OCR de recetas

- Proyecto hermano ("Autorizaciones AI") que usa OCR (GLM) para leer recetas médicas y extraer la prestación solicitada — conecta directamente con el trabajo de identificación de código correcto del [[proyecto-nuevo-nomenclador]] (Autorizaciones Inteligentes).

## Desafíos técnicos

- Integración con Salesforce: los casos de auditoría (Query Case) guardan archivos distinto que los casos de servicio; hubo casos de muestra mezclados por error (autorización vs. auditoría, con archivos en el objeto padre vs. hijo).
- Nomenclador: una misma cirugía puede tener múltiples códigos, lo que complica la búsqueda de casos históricos.
- Tipificación de archivos poco confiable (mal etiquetados o con múltiples tipos de documento en un solo archivo).
- Calidad de imagen muy variable (escaneos, fotos de tickets térmicos).

## Relaciones

- Depende de políticas definidas en [[politicas-cobertura]]
- Sucede después de [[reglas]] y antes del auditor humano
- Impulsado por [[control-prestacional]]
- Relacionado con [[proyecto-nuevo-nomenclador]] (identificación de códigos) e [[integra]] (origen de los casos en Salesforce)
