# Claim Schema

## Required top-level fields

| Field | Type | Requirement |
|---|---|---|
| `record_id` | string | Stable unique identifier |
| `version` | string | Semantic or controlled record version |
| `decision_question` | string | Precise question the record addresses |
| `horizon` | string or null | Time boundary for forecasts; null for non-forecast records |
| `claims` | array | One or more atomic claim objects |
| `hypotheses` | array | Competing explanations or outcomes |
| `constraints` | array | Binding limits and gate conditions |
| `assessment` | object | Resolved judgment, confidence, and action state |
| `review` | object | Reviewer, approval state, and timestamp |
| `revision_conditions` | array | Evidence or events that would change the record |

## Claim object

Each claim should include:

- `claim_id` — stable identifier;
- `text` — one atomic proposition;
- `type` — `fact`, `inference`, `forecast`, `speculation`, or `unverified_claim`;
- `state` — `supported`, `plausible`, `not_proven`, `contradicted`, or `verified`;
- `source_ids` — references to source-registry entries;
- `contradictions` — material evidence against the proposition;
- `assumptions` — dependencies not directly established;
- `evidence_ceiling` — the strongest wording justified by the record;
- `independence_notes` — whether apparent corroboration derives from independent evidence;
- `privacy_status` — `public`, `restricted`, `withhold`, or `not_applicable`.

## Source object

A source entry should include:

- `source_id`;
- `title`;
- `issuer_or_author`;
- `published_at`;
- `accessed_at`;
- `source_class`;
- `url_or_locator`;
- `independence_group`;
- `integrity_notes`;
- `rights_or_handling`.

## Hypothesis object

A hypothesis should include:

- `hypothesis_id`;
- `statement`;
- `supporting_claim_ids`;
- `contradicting_claim_ids`;
- `discriminating_indicators`;
- `status`.

## Assessment object

The assessment should include:

- `judgment` — concise resolved conclusion;
- `confidence` — `directional`, `high_confidence`, or `verified`;
- `confidence_basis` — explanation tied to evidence quality and alternatives;
- `strongest_counterargument`;
- `falsifier`;
- `action_state` — for example `monitor`, `wait`, `reject`, `investigate`, `hedge`, `publish`, `escalate`, or `prepare`;
- `action_rationale`.

## Validation rules

1. Every source identifier must resolve to one source-registry entry.
2. A claim marked `fact` cannot rely only on an `unverified` source class.
3. A claim marked `verified` must identify the controlling record.
4. Confidence cannot be `verified` when material contradictions remain unresolved.
5. Every forecast requires a horizon and revision conditions.
6. Every published record requires a strongest counterargument and falsifier.
7. Restricted or withheld claims must not enter the public export.
8. Material edits require a version increment and revision note.
