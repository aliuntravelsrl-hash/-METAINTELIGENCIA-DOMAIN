# DRILL — ACTIVE INTELLIGENCE IDENTITY 008

## Objective
Determine whether existing authorization and certification state can objectively select the active capability set.

## Physical evidence
`capability_resolver_map` contains 18 mappings, but its rows identify resolvable capabilities and repository paths; they do not contain an active/authorized state.

`capability_catalog` contains 34 records: 29 `canonical` and 5 `experimental`. The current physical query shows no `deployed_at` values. Therefore `lifecycle=canonical` cannot be used as a production-active selector.

`architecture_decisions` contains active decisions approved by `director`, but the current schema/query does not provide a deterministic many-to-many binding from those decisions to the active capability set.

`certification_records` currently contains three records, with observed acts `DRAFT_PREPARED` and `REJECTED`; no observed certification record establishes a current active capability composition.

`ovr_instances` has validated/dispatched records, but the observed capability field is null in the queried validated/dispatched instances. Therefore OVR currently does not provide the missing transversal selector either.

## Finding

Existing authorization and certification mechanisms are reusable as evidence and governance state, but they do not currently expose a deterministic `ACTIVE CAPABILITY SET`.

The unresolved element is therefore a **selection/reference rule** that consumes existing governed states.

```text
AUTHORIZED / VALIDATED STATE
          ↓
SELECTION RULE
          ↓
ACTIVE CAPABILITY REFERENCE
          ↓
ACTIVE REFERENCES
```

This is TRANSFORM. It is not a new resolver and not a new authority.

## Architectural consequence

The Intelligence Manifest must reference a selected capability state; it must not decide which capabilities are authorized. Authorization remains external to the identity artifact.

## Bars

- Global OVR: 45% — unchanged.
- V Edad research bar: 40% — unchanged.
- Metaintelligence baseline: INTELLIGENCE-BASELINE-000 / BASELINE-PENDING.

## Next frontier

Determine the minimum deterministic selection predicate that can distinguish `ACTIVE` from `CANONICAL`, `EXPERIMENTAL`, `HISTORICAL`, and `SUPERSEDED` without creating a new authority.
