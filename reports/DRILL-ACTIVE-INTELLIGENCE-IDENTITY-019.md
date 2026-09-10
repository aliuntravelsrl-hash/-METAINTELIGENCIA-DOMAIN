# DRILL — ACTIVE INTELLIGENCE IDENTITY 019

## Objective
Determine whether the current capability corpus can yield an objective ACTIVE CAPABILITY reference for the Active Intelligence Manifest without creating a parallel authority.

## Physical evidence
- `capability_catalog`: 34 records.
- Lifecycle: 29 `canonical`, 5 `experimental`.
- `deployed_at`: 0 populated records in the inspected current catalog.
- `capability_requests`: approval status exists, but approval is not an active-set selector.
- `certification_records`: current inspected records are `DRAFT_PREPARED` / `REJECTED`; no demonstrated active capability composition.
- `capability_resolver_map`: existing resolver maps identified capabilities to repository/path; it does not select the active set.

## Finding
The existing physical structures do not provide a demonstrated deterministic predicate for `ACTIVE CAPABILITY`.

Therefore the following equivalences are explicitly rejected:

- CANONICAL != ACTIVE
- APPROVED != ACTIVE
- RESOLVED != ACTIVE
- CERTIFIED != ACTIVE
- DEPLOYED != IDENTITY

The missing function is a governed selection rule that consumes existing state rather than creating a new authority.

## Minimal TO-BE

```text
GOVERNED CAPABILITY STATE
        ↓
CURRENT + AUTHORIZED + NOT SUPERSEDED + SCOPE
        ↓
ACTIVE CAPABILITY REFERENCE
        ↓
ACTIVE INTELLIGENCE MANIFEST
```

Runtime materialization remains a separate verification layer and must not silently rewrite intelligence identity.

## Classification

- Existing capability catalog: REUSE
- Existing requests/authorization evidence: REUSE
- Existing certification: REUSE
- Existing supersession: REUSE
- Resolver map: REUSE + TRANSFORM
- Active capability selection rule: TRANSFORM
- New architecture: NO
- New authority: NO
- QA: outside this research path

## State
GAP-META-01 remains open only at the composition/selection function. No new table, RPC, runtime component, or constitutional mechanism is justified by this drill.

OVR global: 45% — unchanged.
V Edad research bar: 40% — unchanged.

## Next frontier
Test whether the same governed-selection abstraction can be expressed for all six reference classes and then deterministically serialized into one manifest, without duplicating their source state.