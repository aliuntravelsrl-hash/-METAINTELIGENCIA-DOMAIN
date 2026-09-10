# DRILL — ACTIVE INTELLIGENCE IDENTITY — 012

**Scope:** METAINTELIGENCIA DOMAIN  
**Mode:** TO-BE / evidence-bound / reuse-first  
**Date:** 2026-09-10

## Question

Can the six required reference classes be deterministically composed into an Intelligence Manifest without creating a new authority or duplicating existing state?

## Physical evidence

Supabase currently demonstrates separate governed state surfaces:

- KBP records a validated knowledge state: `KBP-v1`, COS `3.5`, integrity `100`, status `ready`.
- KBP records currently have `manifest_hash = NULL`.
- `capability_resolver_map` provides capability-to-repository/path resolution, but does not select the active capability set.
- `capability_catalog` distinguishes lifecycle states but does not expose one deterministic transversal active set.
- `certification_records` provides certification lineage and supersession references.
- `runtime_registry` and workflow registry describe operational materialization separately.
- `atlas_state` stores historical/session state and is not a demonstrated active-intelligence selector.

## Finding

The six reference classes are not six missing mechanisms. Their underlying mechanisms already exist and should be reused:

1. COS / doctrine reference → REUSE
2. Knowledge reference → REUSE
3. Capability reference → REUSE + TRANSFORM
4. Integrity reference → REUSE
5. Supersession reference → REUSE
6. Baseline reference → REUSE + TRANSFORM

The unresolved element is the **composition function** that selects the current governed reference for each class and serializes only those references deterministically.

## Minimal TO-BE

```text
GOVERNED CURRENT STATES
        ↓
REFERENCE SELECTION RULE
        ↓
ACTIVE REFERENCES
        ↓
CANONICAL ORDER + DETERMINISTIC SERIALIZATION
        ↓
ACTIVE INTELLIGENCE MANIFEST
        ↓
HASH
        ↓
INTELLIGENCE VERSION
```

The Manifest is a derived identity artifact. It does not replace COS, KBP, OVR, capability governance, supersession, or baseline authority.

## Critical separation

```text
IDENTITY
  = what governed intelligence is active

OPERABILITY
  = whether its referenced mechanisms are materially available

EVIDENCE
  = what was actually demonstrated
```

A runtime failure therefore does not silently mutate the Intelligence Version.

## Classification

**TRANSFORM:** transversal composition and deterministic serialization.  
**No new authority.**  
**No new architecture.**  
**No QA dependency in this path.**

## Frontier

GAP-META-01 is now reduced to one materialization problem:

> Create a reproducible, canonical composition of existing governed references into an Active Intelligence Manifest and derive its hash.

This is narrower than creating a new intelligence-state system.

## Bars

- Global OVR: **45% — unchanged**
- V Edad research bar: **40% — unchanged**

## Next Drill

Determine the minimum canonical selection predicate for each reference class and verify that the resulting composition is reproducible without inference or duplicated state.
