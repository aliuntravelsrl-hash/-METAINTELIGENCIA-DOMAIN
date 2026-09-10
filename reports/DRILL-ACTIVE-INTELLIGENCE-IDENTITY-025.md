# DRILL — ACTIVE INTELLIGENCE IDENTITY 025

**Fecha:** 10 Sep 2026
**Scope:** GLOBAL / METAINTELIGENCIA
**Modo:** READ-ONLY / EVIDENCE-BOUND
**OVR global:** 45% — sin modificación
**V Edad research bar:** 40% — sin modificación

## Objetivo
Determinar si existe una fuente física que permita seleccionar el conjunto ACTIVE de capabilities para el scope global, sin inferencia.

## Evidencia

`capability_catalog` contiene 34 capacidades: 29 canonical y 5 experimental. Sus campos permiten identificar código, versión, lifecycle, owner, ADR, repositorio y materialización declarada, pero no exponen un selector `active_scope` o equivalente.

`architecture_decisions` registra decisiones y aprobación directorial, pero no existe una relación física demostrada que convierta ese conjunto de decisiones en un conjunto ACTIVE de capabilities para un scope de inteligencia.

`certification_records` aporta evidencia de certificación y genealogía mediante `supersedes_certification_id`, pero no constituye por sí mismo un selector ACTIVE transversal.

`capability_resolver_map` resuelve capabilities ya identificadas hacia repo/ruta; no selecciona el conjunto ACTIVE.

`atlas_state` consultado para baseline/version/intelligence/manifest/knowledge/capability/integrity/supersession solo mostró estado histórico/operacional de sesiones, no una composición ACTIVE global.

## Resultado

No se encontró una fuente física inequívoca para:

```text
GLOBAL INTELLIGENCE SCOPE
        ↓
ACTIVE CAPABILITY SET
```

Por tanto, el residuo permanece como una función de selección, no como ausencia de catalogación, resolución, autorización o hashing.

## Clasificación

- capability_catalog → REUSE
- architecture_decisions → REUSE
- certification_records → REUSE
- capability_resolver_map → REUSE + TRANSFORM
- atlas_state → REUSE como estado histórico/operacional
- ACTIVE CAPABILITY SELECTION → TRANSFORM / GAP funcional mínimo

## Conclusión

La investigación no justifica crear otra arquitectura ni otra tabla de capabilities.

El siguiente punto debe definir únicamente la semántica mínima de selección:

```text
CURRENT + AUTHORIZED + NOT SUPERSEDED + SCOPE
                    ↓
          ACTIVE CAPABILITY REF
```

Pero esta expresión sigue siendo una **recomendación TO-BE**, no una regla vigente del COS, hasta que Director la autorice y sea materializada/verificada.

Una vez autorizado, podrá probarse si los seis references pueden ensamblarse sin inferencia.

## Gobernanza

No se modifica Constitución, CEND, EVO, OVR global, V Edad, Supabase schema ni runtime. QA permanece fuera de este camino.
