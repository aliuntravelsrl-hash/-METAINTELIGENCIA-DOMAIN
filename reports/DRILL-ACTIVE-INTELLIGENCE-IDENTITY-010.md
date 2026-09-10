# DRILL — ACTIVE INTELLIGENCE IDENTITY 010

## Objective
Resolve whether runtime materialization is part of Intelligence Identity or a separate verification state.

## Physical evidence
The current capability catalog exposes `lifecycle`, `repositorio`, `adr_codigo`, and `deployed_at`; the inspected catalog has `deployed_at = NULL` across its records. `runtime_registry` separately exposes runtime identity and `estado`, including runtime path, repository, branch, health check and operational fields. `wf_registry` separately exposes workflow `estado`, lifecycle, execution timestamps and repository linkage.

This establishes a structural separation between capability definition/governance and runtime materialization/operational state.

## Finding
Runtime materialization should NOT be embedded as the identity criterion of Intelligence itself.

The intelligence identity answers:

```text
WHAT GOVERNED INTELLIGENCE IS ACTIVE?
```

Runtime verification answers:

```text
CAN THE REFERENCED CAPABILITIES / MECHANISMS BE OBSERVED AS MATERIALIZED AND OPERABLE?
```

Therefore:

```text
AUTHORIZED + CURRENT + NOT SUPERSEDED
        ↓
ACTIVE INTELLIGENCE IDENTITY
        ↓
MANIFEST / HASH

ACTIVE INTELLIGENCE IDENTITY
        ↓
RUNTIME MATERIALIZATION
        ↓
VERIFICATION / EVIDENCE
```

A runtime outage must not silently rewrite the intelligence identity. Conversely, an identity reference must not be considered physically executable merely because it is authorized.

## Classification

- Capability governance state → REUSE.
- Runtime registry → REUSE.
- Workflow registry → REUSE.
- Runtime verification → REUSE + TRANSFORM.
- Separation between identity and operability → TRANSFORM of existing state relationships.
- New architecture → NO.
- New authority → NO.
- QA → outside this path.

## Reduced composition rule

For identity selection, the minimum capability predicate is:

```text
CURRENT + AUTHORIZED + NOT SUPERSEDED
        ↓
ACTIVE CAPABILITY REFERENCE
```

Materialization/availability is verified downstream and must be evidenced, not conflated with identity.

## Bars

- Global OVR: 45% — unchanged.
- V Edad research bar: 40% — unchanged.
- Metaintelligence baseline: `INTELLIGENCE-BASELINE-000 / BASELINE-PENDING`.

## Next frontier

Apply the same separation to Integrity, Supersession and Baseline references, then determine whether the six reference classes can be composed into one deterministic manifest without introducing another state authority.
