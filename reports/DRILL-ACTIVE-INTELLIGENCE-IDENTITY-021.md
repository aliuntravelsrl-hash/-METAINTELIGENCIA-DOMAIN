# DRILL — ACTIVE INTELLIGENCE IDENTITY 021

**Fecha:** 10 Sep 2026  
**Scope:** GLOBAL / METAINTELIGENCIA  
**Modo:** READ-ONLY / EVIDENCE-BOUND  
**OVR global:** 45% — sin modificación  
**V Edad research bar:** 40% — sin modificación

## Objetivo

Determinar si el estado físico existente permite seleccionar capacidades ACTIVE sin inventar un nuevo estado.

## Evidencia física

`capability_catalog` contiene 34 capacidades: 29 `canonical` y 5 `experimental`.

Las 29 capacidades `canonical` tienen `architecture_decisions` correspondientes con `estado='activo'` y `aprobado_por='director'`. Esto demuestra una relación física entre capacidad registrada y decisión arquitectónica activa/aprobada.

Sin embargo, `capability_catalog` no contiene columnas de `scope`, `ambito` o `domain`. La búsqueda equivalente en las tablas de governance inspeccionadas tampoco encontró un campo de scope para `capability_catalog`, `capability_requests`, `architecture_decisions` o `certification_records`. `kernel_entities` sí posee `domain`, pero el registro actual no proporciona una composición transversal de capacidades que permita asignar objetivamente cada CAP a un scope de inteligencia.

`deployed_at` permanece NULL en las capacidades inspeccionadas. Esto no invalida la identidad gobernada: materialización/operabilidad debe seguir separada de identidad.

## Hallazgo

Se corrige una parte de la hipótesis anterior:

```text
CANONICAL
+
ADR ACTIVO
+
APROBADO POR DIRECTOR
        ↓
GOVERNED CURRENT CAPABILITY
```

Por tanto, **sí existe un selector parcial físicamente demostrable** para el estado gobernado de Capability.

Pero todavía no existe evidencia suficiente para afirmar:

```text
GOVERNED CURRENT CAPABILITY
        ↓
AUTHORIZED SCOPE
        ↓
ACTIVE CAPABILITY REFERENCE
```

La ausencia real no es un nuevo mecanismo de Capability ni un nuevo Resolver. Es la falta de una regla física/determinista que establezca la pertenencia de una capacidad al scope de la inteligencia que se está versionando.

## Resultado

El gap se reduce desde:

`ACTIVE CAPABILITY SELECTION`

hasta:

`CAPABILITY → INTELLIGENCE SCOPE BINDING`

Clasificación: **TRANSFORM** si puede expresarse mediante componentes existentes; **DELTA/GAP** solo si la evidencia demuestra que ningún componente existente puede materializar esa relación.

## Regla de continuidad

No volver a investigar canonical/approved/deployed como sustitutos de scope. El siguiente Drill debe comprobar si la relación `capability → domain/scope` ya puede rescatarse de manifests, kernel entities, capability resolver map u otra fuente existente antes de proponer cualquier materialización nueva.

## Gobernanza

No se modifica Constitución, CEND, OVR, EVO, Supabase schema ni runtime. QA permanece fuera del camino estructural.
