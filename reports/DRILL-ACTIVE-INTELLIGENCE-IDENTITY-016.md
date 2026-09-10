# DRILL — ACTIVE INTELLIGENCE IDENTITY 016

**Date:** 2026-09-10  
**Scope:** GLOBAL / METAINTELIGENCIA  
**Mode:** TO-BE / evidence-bound  
**OVR global:** 45% — unchanged  
**V Edad research bar:** 40% — unchanged

## Question

Can existing governance + certification + supersession evidence select the ACTIVE CAPABILITY reference without creating a new authority?

## Physical evidence

`capability_catalog` contains 34 records: 29 `canonical` and 5 `experimental`. `capability_requests` contains 30 requests, of which 5 are `approved`.

`architecture_decisions` contains active decisions explicitly approved by `director`.

`certification_records` currently contains only `DRAFT_PREPARED` and `REJECTED` acts in the inspected physical state. The rejected record has a concrete blocking reason. No inspected certification record establishes a current active capability composition.

The existing `supersedes_certification_id` field provides lineage between certification records, but does not itself select the active capability set.

## Finding

Governance and certification provide necessary evidence, but the inspected physical state does not expose a deterministic transversal selector equivalent to `hotel_knowledge.activo = true` + `verificado = true`.

Therefore the minimum selector remains a TO-BE composition rule:

```text
CAPABILITY
  + CURRENT GOVERNANCE
  + AUTHORIZED SCOPE
  + NOT SUPERSEDED
        ↓
ACTIVE CAPABILITY REFERENCE
```

This is **TRANSFORM**, not a new capability resolver and not a new authority.

## Important separation

`CERTIFIED` is not automatically equivalent to `ACTIVE`.

`CANONICAL` is not automatically equivalent to `ACTIVE`.

`APPROVED` is not automatically equivalent to `ACTIVE`.

The selector must be explicit and reproducible.

## Consequence for Manifest

The Active Intelligence Manifest cannot yet truthfully contain a Capability reference derived from the current database without an explicit selection rule. The gap is therefore narrowed to the **active capability selection predicate**.

No table, RPC, or new architecture is created by this drill.

## Classification

- Existing capability catalog → REUSE
- Existing capability requests → REUSE
- Existing architecture decisions → REUSE
- Existing certification → REUSE
- Existing supersession lineage → REUSE
- Active capability selection rule → TRANSFORM
- New authority → NO
- New architecture → NO
- QA → OUTSIDE CURRENT PATH

## Next frontier

Define the smallest evidence-bound predicate for ACTIVE CAPABILITY and test whether it can be expressed entirely from existing governed fields before declaring any DELTA/GAP.
