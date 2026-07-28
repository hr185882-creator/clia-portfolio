# The Epstein Record — Sanitized Public Reference

[![Quality checks](https://github.com/hr185882-creator/clia-portfolio/actions/workflows/quality.yml/badge.svg)](https://github.com/hr185882-creator/clia-portfolio/actions/workflows/quality.yml)

A public-safe reference architecture for a source-first research product that distinguishes what records establish from what they merely suggest, repeat, or fail to prove.

- Live product: https://the-epstein-record.vercel.app/
- Portfolio: https://github.com/hr185882-creator
- Creator: Hasan Raza Kazmi

## Why this sanitized repository exists

The production product incorporates large public-record collections, reviewed research notes, privacy decisions, and publication controls that should not be copied wholesale into an open repository. This kit exposes the analytical and technical design without publishing sensitive records, private-person information, victim-identifying material, credentials, or unsupported allegations.

This is a reference implementation and documentation package, not a byte-for-byte copy of the production deployment.

## Demonstrated capabilities

- claim-level evidence classification;
- source provenance and source-chain separation;
- association-versus-culpability safeguards;
- adjudicated, alleged, disputed, unresolved, and not-established states;
- privacy and public-interest review boundaries;
- corrections, retractions, and revision history;
- sanitized record schemas and deterministic validation;
- public-facing research-product architecture.

## Repository map

- `docs/ARCHITECTURE.md` — system boundaries, data flow, and release gates
- `docs/PRIVACY_AND_CORRECTIONS.md` — privacy, corrections, and contested-claim controls
- `data/example-claim-ledger.json` — fictional public-safe schema examples
- `.github/workflows/quality.yml` — ready-to-copy content and build validation

## Evidence states

| State | Meaning |
|---|---|
| `adjudicated` | Established through a controlling legal disposition or equivalent official record |
| `verified_record` | Directly supported by an authenticated primary record |
| `supported_reporting` | Reliably reported but not independently established by this project |
| `alleged` | Attributed allegation with clear sourcing and no claim of adjudication |
| `disputed` | Materially contested by credible evidence or a named response |
| `unresolved` | Consequential claim for which the available record is insufficient |
| `not_established` | The reviewed record does not support the proposition |

## Non-negotiable analytical rules

1. Appearance in a contact book, calendar, photograph, address record, or flight record is not proof of criminal conduct.
2. Association is not culpability.
3. Allegations must remain attributed and labeled.
4. Legal outcomes and official records take precedence over repetition volume.
5. Privacy harm must be weighed independently from public curiosity.
6. Material corrections must preserve a visible revision record.
7. Fictional examples in this repository are not factual claims about real people.

## Authorship and AI assistance

Hasan Raza Kazmi directs the research questions, evidence standards, analytical framework, product architecture, editorial judgment, QA, and publication decisions. AI systems may assist with coding, synthesis, formatting, or production, but do not replace source verification or final human judgment.

## Security and responsible disclosure

Do not submit credentials, private personal information, victim-identifying material, sealed records, or illegal content through public issues. Report security concerns through the security process described in the parent portfolio repository.

## License boundary

The reference documentation, fictional schemas, and original example records may be reused with attribution. Underlying court records, government documents, journalism, photographs, and third-party materials retain their original rights and restrictions. No third-party corpus is redistributed here.
