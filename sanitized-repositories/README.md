# Sanitized Public Repository Kits

These directories are public-safe reference implementations for two deployed products whose production corpora and internal build packages are not suitable for direct publication.

## Available kits

### [The Epstein Record](the-epstein-record/)

A source-first public-record research architecture demonstrating claim classification, provenance, association-versus-culpability controls, privacy boundaries, corrections handling, and public-safe example data.

Live product: https://the-epstein-record.vercel.app/

### [RECORD LOCK](record-lock/)

An auditable evidence-verification and dossier-publication architecture demonstrating immutable record identifiers, claim states, source lineage, competing hypotheses, confidence labels, falsifiers, and revision conditions.

Live product: https://record-lock-platform.vercel.app/

## Publication boundary

The kits intentionally exclude:

- production source corpora and licensed documents;
- victim-identifying or private-person information;
- unpublished research notes;
- credentials, tokens, internal paths, and deployment secrets;
- production-only moderation and security controls;
- claims about named people that are not already established in an appropriate public record.

The included records are fictional examples created solely to demonstrate schema design and analytical controls. They must not be interpreted as factual allegations.

## How to use these kits

Each directory is structured so its contents can become the root of a standalone GitHub repository. The included workflow performs deterministic content checks and dependency review. Before publishing a standalone repository, verify links, replace placeholder contact information where needed, and preserve the privacy and corrections policies.
