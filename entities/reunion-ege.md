---
title: Reunión EGE
created: 2026-07-09
updated: 2026-07-09
type: entity
tags: [reunion, seguimiento]
sources: [raw/notion/reunion-ege.md, notion_export/Reunión EGE]
confidence: high
---

# Reunión EGE

Reunión periódica del Equipo de Gerencia Estratégica de Salud (participantes recurrentes: Belén, Martín, Fer, Ana, Jimena, Tomy/Tommy, entre otros). Es una de las [[reuniones-periodicas]] de seguimiento del equipo, y funciona como el ámbito donde se toman o validan decisiones operativas de control prestacional: ajuste de puntos de control, priorización de proyectos, y seguimiento de indicadores comerciales/competitivos.

> El raw source tiene 17 reuniones documentadas (septiembre 2025 → junio 2026) con un volumen muy grande de detalle operativo. Esta página resume los temas más recurrentes y su relación con el resto del wiki; para el detalle completo de una reunión puntual, conviene consultar el export.

## Formato

- Desde enero 2026 el formato cambió: de presentaciones narrativas a preguntas concretas basadas en indicadores de la plataforma.
- Cadencia semanal, con reuniones presenciales periódicas (ej. off-site en Rosario, abril 2026) para revisar objetivos anuales y organigrama.

## Temas recurrentes

### Ajuste de puntos de control y autorizaciones innecesarias
- Análisis recurrente de por qué ciertos códigos generan autorización (F4) innecesaria: distinción entre "molestado premeditadamente" (referencia 14 por decisión médica), "molestado por punto de control" (límite mal configurado) y "molestado por comportamiento del prestador" (el prestador deriva a autorización cuando no corresponde).
- Ejemplo trabajado en detalle: de 38.500 personas que solicitaron autorización en un período, 30.300 fueron F4 ambulatorio, 7.000 F6 (internación), 3.800 F8 (odontología). Se armó un análisis jerárquico completo (embudo/Sankey) desde el total de consumidores hasta el resultado de cada autorización, para identificar dónde actuar primero.
- Casos puntuales: se decidió eliminar la referencia 14 de videoendoscopía digestiva baja (19% rechazo, mayoría con criterio de cobertura correcto) y pasarla a validación online con [[auditoria-medica-facturacion]] posterior; se propuso subir el punto de control anual de inmunoglobulina E de 1 a 16 controles/año.
- Esto conecta directamente con [[puntos-de-control]] y con el trabajo de [[reglas]] (motor de reglas).

### Proyecto Anestesia Online
- Tema recurrente con idas y vueltas: en una reunión hubo "posiciones encontradas" sobre si avanzar, pendiente de decisión de Belén; en la reunión siguiente se decidió avanzar. Ver [[anestesia-online]].

### Estrategia comercial y contexto competitivo
- Seguimiento de bajas de asociados y caída en venta de cápitas (de 20.000 a 18.000/mes), atribuido a una nueva resolución que permite cambiar de prepaga antes del año, y a competencia más agresiva (Swiss Medical, Medifé).
- Seguimiento de medidas comerciales con impacto directo en costo prestacional: compra de cartera de Uno Salud en Comodoro Rivadavia (+$79M/mes por mayor patología de la esperada), incorporación de odontólogos, nuevas prestaciones del Plan GEN (impacto de gasto de $889M/mes, con rentabilidad recién esperada desde el sexto mes).

### Estructura, capacitación y clima
- Seguimiento de encuesta de clima organizacional y definición de objetivos anuales por líder (ESER).
- Cambios de estructura y reporting (ej. salida de Ine de su posición, redistribución de gerencias regionales).
- Coordinación con [[capital-humano]] para readaptaciones de equipo.

### Automatización y herramientas
- Evaluación comparativa de herramientas de IA para distintos usos internos (documentos, onboarding de prestadores).
- Menciones a RPA para contactar automáticamente al asociado cuando un prestador deriva a autorización innecesariamente.

## Relaciones

- Parte de [[reuniones-periodicas]]
- Relacionada con [[reunion-belu]]
- Vinculada a [[puntos-de-control]], [[reglas]], [[anestesia-online]], [[capital-humano]]
