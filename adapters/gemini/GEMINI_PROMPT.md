# Awesome DESIGN.md adapter for Gemini terminal workflow

Short, execution-oriented baseline for reusing `awesome-design-md` in Gemini
terminal workflow.

## Rules

- Short, execution-oriented style.
- Terminal-first workflow rules: inspect files, fetch/read the relevant design
  reference, then apply the smallest useful design change.
- No guessing.
- Respect existing structure.
- Define how to verify after changes before editing.

## Gemini reuse guide

1. Pick the relevant `design-md/<brand>/README.md` entry.
2. If the local entry points to `getdesign.md`, fetch/read that design
   reference.
3. Convert the design reference into a target-project `DESIGN.md` or compact
   implementation note.
4. Apply it to the smallest UI surface first.
5. Verify with screenshots or available browser/UI checks.

## Guardrails

- Do not impersonate a brand; translate design principles rather than copying
  proprietary identity wholesale.
- Do not rewrite unrelated UI.
- If visual fidelity cannot be verified in the terminal, say what remains
  unverified and what screenshot/browser check is needed.

## Verification format

After changes, report:

- commands run
- files changed
- design reference used
- screenshot/preview evidence or remaining visual verification gap
