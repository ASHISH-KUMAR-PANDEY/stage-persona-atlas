# STAGE · Persona Atlas

A single-page, presentation-ready microsite for the 8 user personas derived from
4,727 real STAGE character-bot users across the full lifecycle (3-day → 15+ days).

## Structure

```
stage-personas-site/
├── index.html        # the report (self-contained)
├── assets/
│   └── styles.css    # dark-theme stylesheet
├── .nojekyll         # tells GitHub Pages to serve assets as-is
└── README.md         # this file
```

## Local preview

```bash
cd stage-personas-site
python3 -m http.server 8000
# open http://localhost:8000
```

Any static server works — no build step.

## Deploy to GitHub Pages

```bash
# from this directory
git init
git add .
git commit -m "Add Persona Atlas site"
git branch -M main
git remote add origin git@github.com:<your-username>/<repo>.git
git push -u origin main

# then in GitHub repo settings:
# Settings → Pages → Source: Deploy from a branch → main → / (root)
```

The site will be available at `https://<your-username>.github.io/<repo>/`.

If you want to host it alongside the existing `chat-analysis-report-1774618336`
repo, just commit this folder into that repo and link it from the index.

## What's inside

- **Hero + stats** — corpus shape at a glance
- **Methodology** — the 4-step derivation process and the cohort × bucket table
- **8 persona dossiers** — each with verbatim quote, inferred portrait, behavioural
  fingerprint, top characters, intent mix, stay/leave/comeback levers, risk flag,
  anchor user IDs, and product implications
- **Comparison matrix** — all 8 personas side by side
- **Lifecycle map** — how personas move (or don't) from 3-day to 15+
- **Next steps** — three directions for follow-on work

## Data provenance

All quotes, user IDs, intent percentages, and behavioural metrics are derived
from the STAGE chat-analysis-report-1774618336 corpus. Persona names, ages,
towns, and occupations are explicitly labelled as inferred from chat evidence
(dialect, register, topics) — they are hypotheses for the team to validate,
not demographic facts.
