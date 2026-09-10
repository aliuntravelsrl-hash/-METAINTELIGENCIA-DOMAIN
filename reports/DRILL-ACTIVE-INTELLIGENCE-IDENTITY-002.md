# DRILL — ACTIVE INTELLIGENCE IDENTITY 002

**Fecha:** 2026-09-10
**Modo:** READ-ONLY / EVIDENCE-BOUND

## Objetivo
Determinar si las referencias activas de `INTELLIGENCE-BASELINE-000` pueden derivarse objetivamente de las superficies existentes.

## Evidencia principal
`atlas_state` contiene estado persistente real y referencias a COS, memoria, KBP, OVR, capabilities y sesiones. Sin embargo, el contenido está acumulado dentro de estructuras históricas/narrativas y no constituye un snapshot determinista de composición activa.

La propia evidencia institucional registra anteriormente `STATE LOSS` y `NARRATIVE DRIFT` como problemas de reconstrucción: una afirmación persistida puede existir sin que su vigencia, fuente y relación temporal permitan resolverla de forma determinista.

Por tanto, `atlas_state` no puede utilizarse como selector soberano automático de referencias activas.

## Reconciliación de superficies

| Dimensión | Superficie existente | ¿Demuestra pertenencia al Active Intelligence? |
|---|---|---|
| COS | `atlas-cos-v1` | Sí como autoridad canónica; no como snapshot de composición |
| Knowledge | `kbp_events`, `agent_persistent_memory` | Demuestran conocimiento/estado; no composición global |
| Capability | `capability_catalog`, `capability_resolver_map` | Demuestran catálogo/resolución; no conjunto activo autorizado |
| Integrity | KBP/domain integrity mechanisms | Demuestran estados de integridad; no composición |
| Supersession | genealogy/CEND/state records | Demuestran relaciones temporales; no selector determinista |
| Baseline | `INTELLIGENCE-BASELINE-000` en Metaintelligence | Identifica baseline conceptual; no sus referencias completas |

## Hallazgo

El conjunto de referencias activas **no es actualmente derivable de una única superficie existente sin introducir inferencia**.

Esto confirma que el problema restante no es simplemente "calcular un hash".

El mínimo requisito TO-BE es una **fuente derivada y reproducible que registre explícitamente las referencias que constituyen un Intelligence Baseline**, después de que esas referencias hayan sido determinadas por reglas gobernadas.

## Clasificación

`ACTIVE REFERENCES` → **DELTA/GAP real**

`MANIFEST` → **TRANSFORMACIÓN del conjunto de referencias**, no una nueva fuente de verdad.

`HASH` → **TRANSFORMACIÓN determinista**, posterior al Manifest.

## Secuencia resultante

`BASELINE → RULES OF INCLUSION → ACTIVE REFERENCES → MANIFEST → HASH → INTELLIGENCE VERSION`

No se justifica todavía implementar tabla, RPC ni nuevo protocolo. Primero debe quedar definida la regla de inclusión y su autoridad.

## Próximo Drill
Determinar si las reglas de inclusión pueden reutilizar mecanismos existentes (KBP, governance, baseline, supersession, capability lifecycle) o si existe un vacío real de gobierno que requiera EVO.

**OVR global:** 45% — sin modificación.
**V Edad investigación:** 40% — sin modificación.
