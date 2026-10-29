# Domain Docs

How the engineering skills should consume the domain documentation when exploring this repo.

## Before exploring, read these

- **`GLOSSARY.md`** at this repo's root: the generator's own vocabulary.
- **`docs/adr/`** in this repo: decisions inside the generator. Read the ones that touch the area you're about to work in.
- **The parent repo's ADR-0001, ADR-0002 and ADR-0016** (`youmadeit/docs/adr/`): why the generator exists and what its first consumer needs from it. This clone sits in the parent's `generator/` folder, and a worktree sits deeper inside it, so walk up to the first folder that holds `docs/adr/0016-*.md`. On GitHub: <https://github.com/DannyFestor/youmadeit/tree/main/docs/adr>.

If any of these files don't exist, **proceed silently**. Don't flag their absence; don't suggest creating them upfront. The `/domain-modeling` skill creates them lazily when terms or decisions actually get resolved.

## Stay product-neutral

The generator is a generic Laravel package (ADR-0016). Read the parent's ADRs as one consumer's requirements, not as vocabulary: no You Made It terms in code, docs, issues or the glossary here.

## ADR numbers

One number names one decision across all the You Made It repos. Each repo counts in its own block: parent below 0100, app 0100, iOS 0200, Android 0300, api-docs 0400, generator 0500. New ADRs in this repo number from 0500, so a number alone tells you which repo holds it.

## Use the glossary's vocabulary

When your output names a domain concept (in an issue title, a refactor proposal, a hypothesis, a test name), use the term as defined in `GLOSSARY.md`. Don't drift to synonyms the glossary explicitly avoids.

If the concept you need isn't in the glossary yet, that's a signal: either you're inventing language the project doesn't use (reconsider) or there's a real gap (note it for `/domain-modeling`).

## Flag ADR conflicts

If your output contradicts an existing ADR, surface it explicitly rather than silently overriding:

> _Contradicts ADR-0016 (standalone contract generator), but worth reopening because…_
