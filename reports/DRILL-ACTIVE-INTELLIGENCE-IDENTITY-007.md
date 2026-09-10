# DRILL — ACTIVE INTELLIGENCE IDENTITY 007

## Objective
Determine whether the existing capability registry/resolver provides a sufficient objective reference for active capability composition.

## Physical evidence
The active Supabase project contains `capability_resolver_map` with 18 mappings. Each mapping resolves a capability code to a repository and concrete path. This confirms a real reusable resolution mechanism.

`capability_catalog` contains 34 records, with 29 marked `canonical` and 5 `experimental`. No record has `deployed_at` populated in the current query. Therefore the catalog does not, by itself, prove which capability set is currently active in production.

`architecture_decisions` contains active decisions approved by `director`, including recent ADRs. These decisions establish authorized architectural state, but the queried fields do not establish a deterministic active-capability set.

## Finding

The existing resolver is sufficient for:

```text
CAPABILITY IDENTIFIED
        ↓
RESOLVER MAP
        ↓
REPOSITORY + PATH
```

It is NOT sufficient for:

```text
GLOBAL ACTIVE INTELLIGENCE
        ↓
ACTIVE CAPABILITY SET
```

The missing element is therefore not another resolver. It is the objective selection/reference of the capabilities that constitute the active intelligence for a declared scope.

## Classification

- `capability_resolver_map` → REUSE.
- `capability_catalog` → REUSE + TRANSFORM.
- `architecture_decisions` → REUSE as authorization evidence.
- Active capability-set selection/reference → TRANSFORM / unresolved.
- New resolver architecture → NO.
- New authority → NO.
- QA → outside this path.

## Reduced GAP

```text
AUTHORIZED / VALIDATED CAPABILITIES
        ↓
ACTIVE CAPABILITY REFERENCE
        ↓
ACTIVE REFERENCES
```

The selector must be deterministic and scope-aware. It must not infer activity merely from catalog presence, canonical lifecycle, or historical deployment fields.

## Bars

- Global OVR: 45% — unchanged.
- V Edad research bar: 40% — unchanged.

## Next frontier

Determine whether existing authorization/certification/state evidence can objectively select the active capability set, or whether a minimal selection rule is the only remaining TRANSFORM gap.
