# DRILL — ACTIVE INTELLIGENCE IDENTITY 011

## Objective
Resolve the distinction between integrity, supersession, baseline, and execution evidence in the identity of active intelligence.

## Physical evidence
KBP physically records `knowledge_version`, `cos_version`, `integrity`, and `status`. The latest daily checks report `KBP-v1`, COS `3.5`, integrity `100`, and `ready`, while `manifest_hash` remains null. This proves an existing integrity/knowledge validation mechanism but not a composite intelligence identity.

`certification_records` contains an explicit `supersedes_certification_id`, demonstrating an existing genealogy/supersession relation. This is reusable temporal validity evidence.

`atlas_state` contains session and operational state, but no dedicated global key selecting an active intelligence baseline, so it must not be treated as the identity selector.

## Finding

The six reference classes remain valid, but they have different semantic roles:

```text
COS / DOCTRINE       = governing reference
KNOWLEDGE            = content reference
CAPABILITY           = executable potential/reference
INTEGRITY            = validity evidence/state
SUPERSESSION         = temporal validity relation
BASELINE             = current intelligence reference
```

Execution telemetry and runtime availability remain verification evidence, not identity.

## Critical conclusion

The Manifest should reference the **current governed states**, not require a separate runtime proof to define identity.

Runtime evidence answers:

`¿Está funcionando/materializado?`

The intelligence identity answers:

`¿Qué composición gobernada estaba activa/autorizada?`

Therefore:

```text
CURRENT + AUTHORIZED + NOT SUPERSEDED
              ↓
ACTIVE INTELLIGENCE IDENTITY
              ↓
MANIFEST / HASH
              ↓
INTELLIGENCE VERSION
              ↓
RUNTIME VERIFICATION
```

This preserves the distinction between identity and execution evidence without creating a new authority.

## Classification

- Integrity mechanism → REUSE.
- Supersession relation → REUSE.
- Baseline mechanism → REUSE + TRANSFORM.
- Execution/runtime evidence → REUSE as verification.
- Identity composition rule → TRANSFORM.
- New architecture → NO.
- New authority → NO.
- QA → outside this path.

## Bars

- Global OVR: 45% — unchanged.
- V Edad research bar: 40% — unchanged.
- Metaintelligence baseline: `INTELLIGENCE-BASELINE-000 / BASELINE-PENDING`.

## Next frontier

The remaining problem is now narrowed to the deterministic representation of the selected current references: define how the active set is serialized so equal governed state always produces equal identity, without embedding authority inside the Manifest.
