# AGENTS.md

## What this is
ReadMe.com docs source for Where The Trail Ends. Markdown/MDX only, no build step.

## Commands
- Lint (the only check):  npx -y @readme/cli lint
- Full CLI:               npx @readme/cli --help

## Layout
- docs/<Category>/<slug>.md      guide pages (MDX: <Callout>, <Cards>, <Card> allowed)
- reference/ReadMeConfig/*.md    ReadMe api_config stubs — frontmatter only, do not add body text
- */_order.yaml                  sidebar order; add every new slug or it will not render in order

## Conventions
- Filename == slug == entry in _order.yaml (kebab-case).
- Frontmatter: title (required), excerpt, hidden, icon. New pages start hidden: true until reviewed.
- Default branch is v1.0. Open PRs against v1.0, not main.
- Run lint before committing. Never edit reference/ReadMeConfig/* bodies.
