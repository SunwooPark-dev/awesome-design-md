# Awesome DESIGN.md adapter for Codex App

Use this file as a Codex-first operating contract when reusing the imported
`awesome-design-md` fork for design-guided UI work.

## Purpose

Preserve the repository's reusable design value — a curated catalog of
`DESIGN.md` references and AI-agent-friendly visual system descriptions —
while making the workflow explicit for Codex App and Codex CLI.

## Core operating rules

1. **Think before acting.** Read the relevant design entry and the target
   product context before changing UI code.
2. **Minimum viable implementation first.** Apply the smallest visual change
   that proves the selected design direction.
3. **Only modify what is necessary.** Keep edits scoped to the component,
   page, or design artifact being adapted.
4. **No unnecessary refactors.** Do not restructure unrelated UI code while
   applying a design reference.
5. **Ask when uncertainty materially affects correctness.** If the selected
   brand reference, target surface, or fidelity level is ambiguous, pause and
   resolve it.
6. **Verification before completion.** Capture screenshots, run available UI
   checks, or otherwise verify the visual result before claiming success.

## Codex reuse workflow

1. Identify the target design inspiration in `design-md/<brand>/README.md`.
2. Follow the linked `getdesign.md/<brand>/design-md` source if the local entry
   only points to the hosted design document.
3. Translate the design document into a project-local `DESIGN.md` or concise
   implementation brief.
4. Apply the design to the smallest useful UI slice.
5. Verify visually:
   - screenshot
   - browser preview
   - layout check
   - contrast / spacing check where relevant

## Codex-specific replacement notes

- Treat hosted `getdesign.md` pages as design references, not as executable
  tooling.
- Prefer project-local `DESIGN.md` files when starting a design pass.
- If the target repo already has a visual system, adapt selectively instead of
  blindly copying another brand.
- Avoid copyright or trademark overreach: use inspiration and tokens as a
  starting point, not impersonation.

## Recommended completion report

Always report:

- design reference used
- files changed
- visual verification performed
- screenshots or preview path when available
- remaining fidelity risks
