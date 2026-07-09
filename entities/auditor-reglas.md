---
title: Auditor de Reglas y Procesos Prestacionales
created: 2026-07-09
updated: 2026-07-09
type: entity
tags: [reglas, auditoria, controles]
sources: [raw/notion/mitigacion-de-riesgos-smr.md, notion_export/Definir perfil de persona para Auditoria de reglas]
confidence: high
---

# Auditor de Reglas y Procesos Prestacionales

Nuevo rol (jefatura) definido formalmente por Martín en marzo-abril de 2026 (tarea "Definir perfil de persona para Auditoría de reglas", deadline 06/04/2026, estado: Terminado), transversal — no exclusivo del sector de [[mitigacion-riesgos]] (Riesgos Prestacionales). Reporta al Jefe de Control Prestacional.

## Propósito

Supervisar, auditar y optimizar el ciclo de vida de las reglas prestacionales (motor de reglas, autorizador, Íntegra/procesos asociados), asegurando que sean eficaces, consistentes, trazables y sostenibles. Hoy no existe un proceso sistemático de evaluación posterior a la implementación de una regla — se detecta desvío recién cuando alguien lo reporta.

Se definieron dos versiones posibles del rol:

### Versión 1 — Auditoría de performance (control)
- Medir desempeño por regla/punto de control: volumen, tasa de disparo, tasa de intervención correcta, falsos positivos, excepciones, derivaciones, tiempo de ciclo.
- Detectar "reglas zombie" (vigentes sin impacto) y "reglas tóxicas" (alto daño operativo o mala experiencia del asociado/prestador).
- Controlar alineación entre política/criterio, documentación, configuración real en sistemas y evidencia de testing.
- Diseñar tableros de control: top reglas por fricción, top reglas por ahorro, deuda de documentación/tests, desalineación política vs. implementación.

### Versión 2 — Auditoría + diseño de mejoras (prevención y evolución)
- Explorar datos (consumos, historial, autorizaciones, facturación) para detectar patrones de uso atípico y oportunidades de control temprano.
- Redactar especificaciones de reglas nuevas (condiciones, acciones, excepciones, precedencias, test cases) y participar en su estabilización post-release.
- Mantener un catálogo navegable de reglas/puntos de control auditados: estado, riesgos, aprendizajes, métricas.

## Interacciones clave

- Auditoría Médica, [[auditoria-medica-facturacion]], Analítica/Costeo, IT/Motor de Reglas, Procesos/Transformación Digital.

## Perfil requerido

- Formación: Ingeniería (Industrial/Sistemas/Organización), Administración, Economía, Actuaría o afines con sesgo analítico.
- 3+ años en análisis de procesos, control de gestión, auditoría de sistemas/datos o BI (ideal: salud/seguros).
- Excel avanzado excluyente + Power BI/Tableau; SQL básico deseable.

## KPIs sugeridos

- Hit rate / precisión (intervenciones correctas / disparos), falsos positivos, tasa de excepciones.
- Ahorro real validado vs. ahorro proyectado.
- % de fugas detectadas convertidas en reglas/procesos implementados.
- Tiempo de ciclo hallazgo → especificación → producción.

## Estado de avance

- Tarea relacionada: "Definir puesto de Diseño de Reglas Prestacionales" (rol de diseño, distinto de este de auditoría).
- A julio 2026 el perfil está definido formalmente, pero la persona para el puesto todavía no está asignada.

## Relaciones

- Impulsado desde [[mitigacion-riesgos]]
- Supervisaría a [[reglas]]
- Relacionado con [[autorizador]] y [[politicas-cobertura]]
- Vinculado a [[control-prestacional]]
