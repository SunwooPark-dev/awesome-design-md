# Import Decision — VoltAgent/awesome-design-md

Date: 2026-04-23
Source repository: `https://github.com/VoltAgent/awesome-design-md`
Owning account: `https://github.com/SunwooPark-dev`

## Import decision

- **Overall verdict:** `partial_migration_needed`
- **Recommended import strategy:** `fork + clone`

## Why the repo was imported

This repository is valuable because it is a curated catalog of `DESIGN.md`
references intended for AI agents that generate UI. It is directly aligned
with the ecosystem need for better design guidance across Codex, Antigravity,
and Gemini workflows.

The repository is not fully `directly_usable` as a standalone local asset
because many local entries are pointer pages that direct users to hosted
`getdesign.md/<brand>/design-md` references rather than storing full
`DESIGN.md` content in the GitHub tree. The reusable value survives, but target
adapters need to explain how to use the catalog safely and when to fetch hosted
design references.

## Core value classification

- **Primary core value:** documentation / design-reference catalog
- **Code value:** minimal
- **Workflow value:** moderate, because the intended use is “copy/use a
  DESIGN.md, then ask an AI agent to generate matching UI”

## What reusable value was preserved

Preserved value:

- curated list of design inspirations
- `design-md/<brand>/README.md` entrypoints
- MIT-licensed repository structure
- platform-neutral concept of `DESIGN.md`
- design-first workflow for AI coding agents

## Claude-specific elements removed or replaced

The repository is not structurally Claude-specific. Some hosted pages and copy
mention Claude design usage, but that is peripheral.

Replacements used for this import:

- **Codex App** → `adapters/codex/AGENTS.md`
- **Antigravity App** → `adapters/antigravity/ANTIGRAVITY_PROMPT.md`
- **Gemini terminal workflow** → `adapters/gemini/GEMINI_PROMPT.md`

## Compatibility review summary

### Codex App

**Status:** reusable with light adaptation

Codex-friendly parts:

- design reference catalog
- local `design-md/<brand>/README.md` entrypoints
- Markdown-first design instructions
- UI implementation workflow using project-local `DESIGN.md`

Codex caveat:

- hosted design detail may need to be fetched from `getdesign.md`

### Antigravity App

**Status:** reusable with light adaptation

Antigravity-friendly parts:

- design-first references
- screenshot-friendly UI verification workflow
- platform-neutral markdown descriptions

Antigravity caveat:

- needs a prompt contract to avoid literal brand copying or overbroad UI
  rewrites

### Gemini terminal workflow

**Status:** reusable with light adaptation

Gemini-friendly parts:

- terminal-readable Markdown
- hosted design pages can be fetched and summarized
- design references can be converted into project-local `DESIGN.md`

Gemini caveat:

- terminal-only flows must explicitly call out screenshot/browser verification
  gaps

## What is shared across all 3 targets

- choose a design reference
- convert reference into a project-local design brief or `DESIGN.md`
- apply the smallest useful visual change
- verify with screenshots / previews when possible
- avoid literal brand impersonation

## What is target-specific

### Only valid in one environment

None of the core repository content is exclusive to one target environment.
Target-specific behavior lives only in the adapter files added by this import.

### Assets to preserve unchanged

- `README.md`
- `CONTRIBUTING.md`
- `LICENSE`
- `design-md/**`

### Assets to adapt

- target adapter prompts
- local usage notes
- downstream project-local `DESIGN.md` files derived from selected references

### Assets to exclude

- any interpretation that copies a brand identity wholesale
- any hosted design content redistribution without checking the source terms

## Migration plan

Because the verdict is `partial_migration_needed`, the import proceeds with a
minimal additive adapter strategy.

### Core reusable assets

- `design-md/**`
- README collection taxonomy
- hosted `getdesign.md` references

### Assets to preserve unchanged

- upstream history
- upstream catalog structure
- MIT license and contribution docs

### Assets to adapt

- `adapters/codex/AGENTS.md`
- `adapters/antigravity/ANTIGRAVITY_PROMPT.md`
- `adapters/gemini/GEMINI_PROMPT.md`
- this migration decision record

### Target-specific replacements

- generic “AI agent” usage → Codex / Antigravity / Gemini operating contracts
- hosted design references → target-local workflow for fetching, summarizing,
  and applying references
- raw brand inspiration → guarded design translation with visual verification

### Minimal additive adapter strategy

1. Keep upstream catalog unchanged.
2. Add target adapters under `adapters/**`.
3. Add migration decision under `docs/migration/**`.
4. Do not copy hosted design pages into the repo on first import.

### Verification checklist before commit

- fork exists under `SunwooPark-dev`
- clone exists locally
- `origin` points to the fork
- `upstream` points to `VoltAgent/awesome-design-md`
- working branch is isolated from `main`
- required adapter files exist
- required adapter phrases are present
- `git diff --check` is clean

## How to use the repo in each target

### Codex App

1. Start from `adapters/codex/AGENTS.md`
2. Pick a design reference from `design-md/<brand>/README.md`
3. Fetch the hosted design reference if needed
4. Create or update a project-local `DESIGN.md`
5. Implement the smallest visual slice and verify with screenshot evidence

### Antigravity App

1. Start from `adapters/antigravity/ANTIGRAVITY_PROMPT.md`
2. Select a design reference
3. State fidelity and brand-borrowing assumptions
4. Apply the design to the smallest UI surface
5. Verify visually before completion

### Gemini terminal workflow

1. Start from `adapters/gemini/GEMINI_PROMPT.md`
2. Inspect local entrypoint and fetch hosted reference if needed
3. Convert it into a concise terminal-friendly design brief
4. Apply minimal UI changes
5. Report screenshot/browser verification gaps if not directly verifiable
