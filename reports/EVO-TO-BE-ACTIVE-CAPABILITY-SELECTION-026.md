# EVO / TO-BE — ACTIVE CAPABILITY SELECTION 026

**Fecha:** 10 Sep 2026  
**Scope:** GLOBAL / METAINTELIGENCIA  
**Modo:** RECOMMENDATION / NOT AUTHORIZED FOR MATERIALIZATION  
**OVR global:** 45% — sin modificación  
**V Edad research bar:** 40% — sin modificación

## Punto de partida

La arqueología y la clasificación agotaron las fuentes relevantes para el selector de Capability.

El COS ya dispone de:

- capability_catalog
- capability_requests
- architecture_decisions
- certification_records
- capability_resolver_map
- manifests con `requires` y `domain_requires`
- reglas de current / supersession / authorization

Ningún componente existente demuestra por sí solo la selección transversal de un conjunto ACTIVE para una instancia de Intelligence.

## EVO signal

El objeto no necesita una nueva arquitectura de capacidades. Necesita una función de selección que consuma estados gobernados existentes.

## TO-BE recomendado

Para un `scope` determinado, una Capability puede ser considerada referencia ACTIVE únicamente cuando exista evidencia gobernada de:

```text
CURRENT
+
AUTHORIZED
+
NOT SUPERSEDED
+
SCOPE COMPATIBLE
        ↓
ACTIVE CAPABILITY REFERENCE
```

La selección debe producir referencias a capacidades existentes, nunca duplicar el catálogo ni sustituir la autoridad de `atlas-cos-v1`.

## Relación con Manifest

```text
GOVERNED CAPABILITY STATES
        ↓
ACTIVE-SELECTION RULE
        ↓
ACTIVE CAPABILITY REFERENCES
        ↓
ACTIVE INTELLIGENCE REFERENCES
        ↓
DETERMINISTIC SERIALIZATION
        ↓
HASH
        ↓
INTELLIGENCE VERSION
```

La regla es un mecanismo de composición/selección. El Manifest continúa siendo una representación derivada de estado; no se convierte en autoridad.

## Macro / Micro

La misma función puede operar en:

```text
GLOBAL SCOPE
   ↓
GLOBAL ACTIVE CAPABILITY REFERENCES
```

ó:

```text
DOMAIN SCOPE
   ↓
DOMAIN ACTIVE CAPABILITY REFERENCES
```

No se crean dos mecanismos. Cambia únicamente el scope.

## Gobernanza

Este documento es **TO-BE / RECOMENDACIÓN EVO**.

No autoriza:
- nueva tabla
- nueva RPC
- modificación de capability_catalog
- modificación de atlas-cos-v1
- cambio de OVR
- cambio de CEND
- cambio de EVO

La secuencia constitucional permanece:

```text
OUTCOME SIGNAL
      ↓
DOMAIN / META LEARNING
      ↓
FUTURE RELEVANCE / META-EVO
      ↓
EVO
      ↓
TO-BE
      ↓
DIRECTOR
      ↓
AUTHORIZATION
      ↓
EXECUTION
      ↓
VALIDATION
      ↓
ADOPTION
      ↓
NEW BASELINE
```

## Próxima prueba

No implementar todavía.

El siguiente Drill debe comprobar si esta regla mínima puede seleccionar un conjunto ACTIVE usando exclusivamente evidencia existente, sin añadir una nueva fuente de autoridad.

Si la respuesta es sí, el siguiente paso será materialización mínima. Si no, se registra el delta exacto.
