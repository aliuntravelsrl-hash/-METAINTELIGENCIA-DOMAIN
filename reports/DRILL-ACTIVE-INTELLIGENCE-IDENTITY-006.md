# DRILL — ACTIVE INTELLIGENCE IDENTITY 006

## Objective
Determine the minimum mandatory active references for one intelligence scope using existing authoritative mechanisms, without inference.

## Evidence boundary
The Metaintelligence domain defines Intelligence Baseline as a governed state and requires evidence before a new baseline is established. The domain also explicitly states that existing components must be reused before new materialization.

## Finding
The minimum identity cannot be a copy of all COS state. It must contain only references necessary to identify the intelligence composition for a declared scope.

For the GLOBAL scope, the mandatory reference classes are:

1. Constitutional / doctrinal reference — identifies the governing COS baseline.
2. Knowledge reference — identifies the validated knowledge state required for the scope.
3. Capability reference — identifies the authorized active capability composition available to the intelligence.
4. Integrity reference — identifies the validity state of the referenced intelligence inputs.
5. Supersession reference — identifies which referenced material remains current versus superseded.
6. Intelligence baseline reference — identifies the currently authorized intelligence baseline.

These are reference classes, not new sources of authority.

## Important distinction

`EVIDENCE`, `EXECUTION`, `SESSION MEMORY`, and `TELEMETRY` are not mandatory identity components. They may prove or measure the state, but they are not themselves the identity of the active intelligence composition.

## Minimal TO-BE

```text
DECLARED SCOPE
      ↓
COS / DOCTRINE REF
      ↓
KNOWLEDGE REF
      ↓
CAPABILITY REF
      ↓
INTEGRITY REF
      ↓
SUPERSESSION REF
      ↓
BASELINE REF
      ↓
ACTIVE REFERENCES
      ↓
DETERMINISTIC SERIALIZATION
      ↓
MANIFEST / HASH
      ↓
INTELLIGENCE VERSION
```

## Architectural classification

- Existing authority and state mechanisms: REUSE.
- Scope-specific selection of mandatory references: TRANSFORM.
- Deterministic composition: TRANSFORM.
- No new authority identified.
- No new architecture identified.
- QA remains outside this research path.

## Unresolved boundary

The reference classes are now sufficiently defined conceptually, but the physical source for each active reference must be resolved without assuming that a table, file, or current value is authoritative merely because it exists.

## Bars

- Global OVR: 45% — unchanged.
- V Edad genealogical research bar: 40% — unchanged.
- Metaintelligence baseline: `INTELLIGENCE-BASELINE-000 / FOUNDATIONAL / BASELINE-PENDING`.

## Next frontier

Resolve the authoritative physical source and deterministic selector for each mandatory reference class, beginning with the COS reference and knowledge reference.
