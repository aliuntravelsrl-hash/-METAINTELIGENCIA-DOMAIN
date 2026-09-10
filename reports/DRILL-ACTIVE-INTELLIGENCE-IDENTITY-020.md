# DRILL — ACTIVE INTELLIGENCE IDENTITY 020

**Fecha:** 10 Sep 2026  
**Scope:** GLOBAL / METAINTELIGENCIA  
**Modo:** READ-ONLY / EVIDENCE-BOUND  
**OVR global:** 45% — sin modificación  
**V Edad research bar:** 40% — sin modificación

## Objetivo

Probar si las seis clases mínimas de referencia pueden seleccionarse hoy de forma objetiva, sin reconstrucción inferida, para formar una identidad de inteligencia activa.

## Evidencia física

### 1. COS / DOCTRINA
`atlas-cos-v1` continúa siendo la fuente constitucional y doctrinal soberana. La referencia es determinable por fuente canónica, no por actividad operacional.

**Clasificación:** REUSE.

### 2. KNOWLEDGE
Supabase `hotel_knowledge` tiene 150 registros. La regla física previamente demostrada es `activo = true` + `verificado = true`; el conjunto observado fue 150/150.

**Clasificación:** REUSE.

### 3. CAPABILITY
`capability_catalog` contiene 34 capacidades: 29 `canonical` y 5 `experimental`. `capability_resolver_map` contiene 18 resoluciones CAP → repo/ruta.

No existe todavía un selector físico inequívoco que determine cuál conjunto de capacidades está ACTIVE para el scope global. `canonical`, `approved`, `certified` y `not superseded` no son equivalentes a ACTIVE.

**Clasificación:** TRANSFORM.

### 4. INTEGRITY
Existe evidencia física de integridad dentro de KBP: eventos recientes muestran `knowledge_version=KBP-v1`, `cos_version=3.5`, `integrity=100`, `required_loaded=6/6` y `status=ready`. `manifest_hash` sigue NULL en esos eventos recientes.

La integridad puede ser referenciada como estado gobernado; el score no debe confundirse con la identidad completa.

**Clasificación:** REUSE.

### 5. SUPERSESSION
Existe mecanismo físico de genealogía mediante `certification_records.supersedes_certification_id`, y la doctrina de supersession ya está establecida como mecanismo transversal de vigencia temporal.

La referencia debe representar el estado de vigencia relevante, no copiar toda la historia de supersession.

**Clasificación:** REUSE + TRANSFORM.

### 6. BASELINE
`-METAINTELIGENCIA-DOMAIN/VERSION.md` establece `INTELLIGENCE-BASELINE-000` como baseline actual y exige evidencia + autorización para una nueva baseline. La baseline existe como referencia doctrinal persistida.

**Clasificación:** REUSE.

## Resultado del Drill

Cinco clases pueden obtener una referencia gobernada/reutilizable sin crear arquitectura nueva. La sexta, CAPABILITY, sigue sin selector ACTIVE transversal demostrado.

Por tanto, la asamblea completa todavía NO puede declararse determinísticamente cerrada.

```text
COS REF              → SELECTABLE
KNOWLEDGE REF        → SELECTABLE
CAPABILITY REF       → NOT YET SELECTABLE
INTEGRITY REF        → SELECTABLE
SUPERSESSION REF     → SELECTABLE
BASELINE REF         → SELECTABLE
                         ↓
                 ACTIVE REFERENCES
                         ↓
                  MANIFEST / HASH
                         ↓
                 INTELLIGENCE VERSION
```

## Gap mínimo actual

El gap no es Manifest, SHA256, KBP, Integrity, Supersession, Baseline ni Resolver.

El gap mínimo sigue siendo:

```text
GOVERNED CAPABILITY STATE
        ↓
ACTIVE CAPABILITY SELECTION RULE
        ↓
CAPABILITY REFERENCE
```

Una vez resuelto ese selector, debe repetirse únicamente la prueba de ensamblaje de las seis referencias y comprobar si la serialización determinista produce una identidad reproducible. No se justifica todavía crear tabla, RPC o nuevo mecanismo constitucional.

## Regla de continuidad

No volver a hacer arqueología sobre los cinco componentes ya resueltos. El siguiente Drill debe atacar exclusivamente la selección ACTIVE de Capability y su relación con scope/authorization/current/not-superseded.

## Gobernanza

No se modifica Constitución, CEND, OVR global, EVO, Supabase schema ni runtime. QA permanece fuera de este camino estructural.
