# DRILL-ACTIVE-INTELLIGENCE-IDENTITY-015

**Scope:** Knowledge + Capability active-reference selection  
**Mode:** COLD ENTRY / READ-ONLY / EVIDENCE-BOUND  
**Date:** 2026-09-10

## Evidence

### Knowledge
`public.hotel_knowledge` currently contains **150/150 active and verified** records. This demonstrates that an existing domain knowledge surface exposes an explicit active predicate (`activo=true`) and verification state (`verificado=true`).

### Capability
`public.capability_catalog` contains **29 canonical** and **5 experimental** records. The catalog exposes lifecycle, version, repository and deployment fields, but no explicit transversal `active` selector. `capability_requests` has **5 approved** requests among 30 total. Therefore `approved` is governance evidence, not by itself an active capability-set selector.

### Existing resolver
`capability_resolver_map` remains reusable for resolving an already identified capability to repository/path. It does not select the active set.

## Finding

Knowledge already has a physically expressible active predicate. Capability does not yet expose an equivalent deterministic transversal predicate.

Therefore the frontier is narrowed to one reusable transformation:

```text
GOVERNED CAPABILITY STATE
        ↓
CURRENT + AUTHORIZED + NOT SUPERSEDED
        ↓
ACTIVE CAPABILITY REFERENCE
```

No new resolver, authority, knowledge store, or runtime mechanism is justified.

## Classification

- Hotel Knowledge active/verified state → REUSE
- Capability Catalog → REUSE
- Capability Requests approval → REUSE as governance evidence
- Capability Resolver Map → REUSE
- Active Capability selection rule → TRANSFORM
- New architecture → NO
- New authority → NO
- QA → OUTSIDE CURRENT PATH

## Consequence for Intelligence Identity

The six-reference composition is still valid. Knowledge can supply a concrete active reference today; Capability requires a selection rule that consumes existing governed state without duplicating it.

```text
COS_REF
KNOWLEDGE_REF
CAPABILITY_REF   ← current unresolved selection rule
INTEGRITY_REF
SUPERSESSION_REF
BASELINE_REF
        ↓
DETERMINISTIC MANIFEST
        ↓
HASH
        ↓
INTELLIGENCE VERSION
```

**Global OVR:** 45% — unchanged.  
**V Edad research bar:** 40% — unchanged.

## Next frontier

Determine whether the missing capability predicate can be derived from an existing combination of governance + certification + supersession evidence, or whether a minimal new selection field/rule is actually required.