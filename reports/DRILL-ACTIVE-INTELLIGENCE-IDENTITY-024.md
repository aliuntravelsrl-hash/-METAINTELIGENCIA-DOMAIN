# DRILL — ACTIVE INTELLIGENCE IDENTITY 024

**Fecha:** 10 Sep 2026  
**Scope:** GLOBAL / METAINTELIGENCIA  
**Modo:** READ-ONLY / EVIDENCE-BOUND  
**OVR global:** 45% — sin modificación  
**V Edad research bar:** 40% — sin modificación

## Objetivo

Probar si las seis referencias pueden ensamblarse hoy en una identidad determinista sin duplicar fuentes de verdad ni convertir estados históricos en activos.

## Evidencia física

La base actual demuestra:

- COS: `atlas-cos-v1` como fuente soberana.
- Knowledge: `KBP-v1`; último evento observado con `cos_version=3.5`, `integrity=100`, `status=ready`.
- Capability: 29 capacidades `canonical`, 5 `experimental`, 18 mappings en `capability_resolver_map`.
- Supersession: `certification_records` contiene genealogía mediante `supersedes_certification_id`.
- Baseline: `INTELLIGENCE-BASELINE-000` está definido por el dominio de Metainteligencia.
- Hashing: el mecanismo SHA-256/pgcrypto ya existe.

## Prueba de ensamblaje

Una serialización determinista mínima podría mantener únicamente referencias estables y no duplicar el contenido de sus fuentes:

```text
scope
cos_ref
knowledge_ref
capability_ref
integrity_ref
supersession_ref
baseline_ref
```

Sin embargo, la prueba no puede producir todavía una `capability_ref` global objetiva, porque el conjunto `29 canonical` describe lifecycle, no necesariamente el conjunto ACTIVE de inteligencia global. Los 18 mappings del resolver tampoco constituyen por sí mismos ese selector.

Por tanto, fabricar un hash ahora exigiría una inferencia sobre `capability_ref` y produciría una identidad aparentemente determinista pero epistemológicamente falsa.

## Hallazgo

La serialización determinista **sí es materialmente posible**.

El bloqueo no está en la serialización ni en SHA-256.

El bloqueo sigue siendo exclusivamente la semántica de selección de `CAPABILITY REF`.

```text
REFERENCIAS ESTABLES
        ↓
SERIALIZACIÓN DETERMINISTA   ← DISPONIBLE
        ↓
HASH SHA-256                 ← DISPONIBLE
        ↓
INTELLIGENCE VERSION         ← PENDIENTE DE REFERENCIA CAPABILITY
```

## Clasificación

- COS reference → REUSE
- Knowledge reference → REUSE
- Integrity reference → REUSE
- Supersession reference → REUSE + TRANSFORM
- Baseline reference → REUSE
- Deterministic serialization → TRANSFORM
- SHA-256 → REUSE
- Capability reference → TRANSFORM / unresolved selector

## Resultado

`GAP-META-01` queda reducido a una única cuestión semántica:

**¿Cuál es la fuente gobernada que permite identificar, sin inferencia, el conjunto de capacidades ACTIVE que debe entrar en la identidad de inteligencia para un scope determinado?**

No se justifica crear todavía Manifest, tabla, RPC ni nuevo mecanismo constitucional.

## Siguiente Drill

Buscar exclusivamente una fuente existente que pueda responder esa pregunta: manifiestos, authorization state, runtime/current state, o cualquier mecanismo de selección ya persistido. Si no existe, entonces declarar el mínimo TO-BE necesario.

## Gobernanza

No se modifica Constitución, CEND, OVR, EVO, Supabase schema ni runtime. QA permanece fuera del camino estructural.