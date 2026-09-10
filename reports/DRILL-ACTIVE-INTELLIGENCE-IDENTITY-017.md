# DRILL — ACTIVE INTELLIGENCE IDENTITY 017

**Scope:** Knowledge + Capability
**Mode:** COLD ENTRY / READ-ONLY / EVIDENCE-BOUND

## Physical evidence

`hotel_knowledge` currently exposes an explicit active/valid state through `activo=true` and `verificado=true`. Current physical count observed: 150 total, 150 active and verified.

`capability_catalog` exposes lifecycle state. Current physical count observed: 34 total, 29 canonical and 5 experimental. Canonical status alone is not equivalent to active runtime intelligence.

Capability governance is represented separately through `architecture_decisions` and `capability_requests`; certification records also exist, but observed certification acts are `DRAFT_PREPARED` and `REJECTED`. Therefore certification cannot currently be treated as an active selector by itself.

## Finding

The same semantic predicate cannot be copied literally across Knowledge and Capability because their existing state models differ.

The reusable transversal rule is therefore functional rather than schema-identical:

```text
GOVERNED CURRENT STATE
        +
AUTHORIZED / VALIDATED STATE
        +
NOT SUPERSEDED
        ↓
ACTIVE REFERENCE
```

For Knowledge, the existing physical state can satisfy this directly.

For Capability, the required active selector remains a **TRANSFORM** over existing governance/lifecycle/supersession information. `canonical` is necessary evidence of catalog status but is insufficient to prove active intelligence membership.

## Consequence for Manifest

The Manifest should not embed the different domain predicates. It should consume their already-resolved active references:

```text
KNOWLEDGE STATE ──→ ACTIVE KNOWLEDGE REF
CAPABILITY STATE ─→ ACTIVE CAPABILITY REF
                         ↓
                  ACTIVE REFERENCES
                         ↓
                DETERMINISTIC MANIFEST
```

No new authority, parallel state model, or duplicated selector is justified.

## Classification

- Existing Knowledge state: **REUSE**
- Existing Capability governance/lifecycle: **REUSE**
- Shared semantic active-reference rule: **TRANSFORM**
- New architecture: **NO**
- New authority: **NO**
- QA: **OUTSIDE CURRENT PATH**

## Frontier

The remaining GAP-META-01 is now specifically the **materialization of the transversal active-reference composition**, not the creation of separate Knowledge or Capability state systems.

## Bars

- Global OVR: **45% — unchanged**
- V Edad research bar: **40% — unchanged**
