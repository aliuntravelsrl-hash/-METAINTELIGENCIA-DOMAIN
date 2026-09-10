# DRILL — ACTIVE INTELLIGENCE IDENTITY 009

## Objective
Determine the minimum deterministic predicate for selecting ACTIVE capabilities from existing governed state.

## Physical evidence
The current `capability_catalog` schema exposes `codigo`, `version`, `owner`, `lifecycle`, `adr_codigo`, `deployed_at`, and timestamps. Current records are either `canonical` or `experimental`; `deployed_at` is null across the inspected catalog.

`capability_requests` currently contains 5 `approved`, 7 `in_review`, 16 `pending`, and 2 `archived` requests.

`architecture_decisions` and `certification_records` provide governance evidence, but the current physical model does not expose a deterministic binding equivalent to `capability → authorized active scope → current state`.

## Finding

No existing field or combination inspected can truthfully serve as the transversal `ACTIVE` selector.

Therefore the minimum predicate must be a derived rule, not a new authority:

```text
CAPABILITY
  + VALIDATED/CURRENT GOVERNANCE STATE
  + AUTHORIZED SCOPE
  + NOT SUPERSEDED
  + MATERIALIZATION / AVAILABILITY EVIDENCE
        ↓
     ACTIVE
```

Important: `canonical` alone is insufficient; `approved` request alone is insufficient; resolver-map presence alone is insufficient.

## Classification

- Existing capability catalog → REUSE.
- Existing resolver map → REUSE.
- Existing authorization / decision evidence → REUSE.
- Existing certification evidence → REUSE.
- Active selector predicate → TRANSFORM / GAP.
- New authority → NO.
- New resolver → NO.
- QA → outside this path.

## Architectural consequence

The selector belongs to the composition function used by Metaintelligence. It must reference existing governance state rather than become a new governance authority.

The Intelligence Manifest can then reference the resulting active set without embedding the selection logic as authority.

## Bars

- Global OVR: 45% — unchanged.
- V Edad research bar: 40% — unchanged.
- Metaintelligence baseline: `INTELLIGENCE-BASELINE-000 / BASELINE-PENDING`.

## Next frontier

Resolve the remaining ambiguity: whether `ACTIVE` requires proof of runtime materialization or whether authorized/current capability state alone defines active intelligence identity, with runtime evidence serving only verification.
