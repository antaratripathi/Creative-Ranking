# Creative Ranking Workflow — Use Case First

An intent-first redesign of the **Creative Ranking** setup flow ("See Which Creative Wins"). Instead of asking users to pick an asset format up front, the flow anchors on the user's **use case** first, then guides context, format, assets, and audience as a set of progressively unlocking steps.

## Files

| File | Description |
|------|-------------|
| [`index.html`](index.html) | The redesigned **5-step, intent-first** guided workflow — the main deliverable. |
| [`original.html`](original.html) | The original single-screen layout, kept for before/after comparison. |

Both are self-contained static HTML files — no build step, no dependencies.

## The flow (`index.html`)

A guided, progressively-unlocking sequence. Each step reveals only after the previous one is genuinely complete, and a completed step shows a green ✓.

1. **Select your use case** — search the full catalog ("Find the right one") or pick from a labeled shortlist ("Browse saved"). The choice tailors the rest of the setup.
2. **Set context** — upload a context brief (PDF/DOCX) or describe the brand direction and how it should come across.
3. **Select format** — Text / Image / Video, each with a description. The format matching the use case is pre-recommended, and a tone-aware tip confirms a good fit (green) or cautions against a mismatch (amber).
4. **Upload assets** — drag-and-drop or browse to add the creatives to rank, with thumbnail previews and per-file remove. Heading adapts to the chosen format ("Upload images" / "Upload videos" / "Upload text"). Needs ≥2 assets to proceed (it's a comparison).
5. **Select target audience** — reveal a list of audience segments and pick one. Completing this enables **Kick Off Research**.

State is honest throughout: clearing an input reverts the step's completion and re-locks everything downstream.

## Running locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Notes

- Pure HTML/CSS/vanilla JS. All interactivity is client-side; nothing is uploaded anywhere.
- This is a design prototype for stakeholder review, not production code.
