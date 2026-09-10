# DRILL — ACTIVE INTELLIGENCE IDENTITY — 014

**Fecha:** 10 Sep 2026  
**Estado:** COMPLETADO / EVIDENCE-BOUND  
**Alcance:** Metainteligencia — identidad de inteligencia activa  
**OVR global:** 45% — sin modificación  
**V Edad:** 40% — sin modificación

## Pregunta

¿Pueden los seis tipos de referencia definidos para la identidad activa producir ya un Manifest reproducible, sin introducir autoridad nueva ni inferencia?

## Evidencia

### 1. Integridad

El proyecto Supabase activo tiene `pgcrypto` instalado en el esquema `extensions`, versión 1.3. Por tanto, existe capacidad criptográfica física disponible para materializar un hash. Esto resuelve la disponibilidad del mecanismo criptográfico, pero no define qué debe entrar en el hash.

Los eventos recientes de KBP muestran `knowledge_version=KBP-v1`, `cos_version=3.5`, `integrity=100`, `required_loaded=6/6` y `status=ready`; sin embargo, `manifest_hash` permanece NULL en los eventos inspeccionados.

**Clasificación:** REUSE.

### 2. Knowledge reference

`KBP-v1` es una referencia de conocimiento validado y físicamente observada. No constituye por sí sola una identidad transversal de todo el conocimiento activo.

**Clasificación:** REUSE + TRANSFORM.

### 3. Capability reference

`capability_resolver_map` existe físicamente y contiene mappings reales. Sin embargo, el catálogo de capacidades no expone una selección transversal inequívoca de capacidades activas/autorizadas. Por tanto, el resolver puede reutilizarse, pero todavía no proporciona por sí solo el `CAPABILITY_REF` global.

**Clasificación:** REUSE + TRANSFORM.

### 4. Supersession reference

La genealogía y los mecanismos de certificación ya permiten representar relaciones de supersession. No existe evidencia suficiente de un único selector transversal que responda automáticamente cuál es el conjunto vigente para el Manifest global.

**Clasificación:** REUSE + TRANSFORM.

### 5. Baseline reference

`INTELLIGENCE-BASELINE-000` está establecido como baseline fundacional en el dominio Metainteligencia. La propia VERSION.md establece que una nueva baseline requiere evidencia de evolución autorizada y verificable.

**Clasificación:** REUSE.

### 6. COS reference

`atlas-cos-v1` permanece como fuente constitucional/doctrinal soberana. La referencia puede ser identificada por su fuente canónica y, cuando corresponda, por un commit SHA verificable.

**Clasificación:** REUSE.

## Resultado

El mecanismo de hashing ya está disponible físicamente, pero **todavía no existe evidencia de que los seis inputs puedan seleccionarse automáticamente sin inferencia**.

Por tanto, no se materializa todavía un Manifest real.

La frontera se reduce a:

```text
GOVERNED SOURCES
      ↓
ACTIVE-SELECTION RULE
      ↓
6 CANONICAL REFERENCES
      ↓
DETERMINISTIC SERIALIZATION
      ↓
MANIFEST
      ↓
SHA-256
      ↓
INTELLIGENCE VERSION
```

La ausencia restante no es criptográfica. Es la **regla objetiva de selección de referencias activas**.

## Clasificación global

| Elemento | Clasificación |
|---|---|
| COS reference | REUSE |
| Knowledge reference | REUSE + TRANSFORM |
| Capability reference | REUSE + TRANSFORM |
| Integrity reference | REUSE |
| Supersession reference | REUSE + TRANSFORM |
| Baseline reference | REUSE |
| Hash mechanism | REUSE |
| Active-selection rule | TRANSFORM / GAP candidate |
| New authority | NO |
| New architecture | NO |
| QA | FUERA DEL CAMINO |

## Conclusión

`GAP-META-01` queda reducido a una única necesidad funcional: **seleccionar de forma objetiva y reproducible las referencias activas que ya gobierna el COS**.

No corresponde crear todavía una tabla, RPC, Manifest ni nueva arquitectura. Primero debe demostrarse que la regla de selección puede reutilizar estados existentes y producir el mismo conjunto de referencias ante la misma realidad gobernada.

El siguiente Drill debe comprobar esa regla de selección, comenzando por `Knowledge` y `Capability`, donde la evidencia actual muestra mayor dispersión.
