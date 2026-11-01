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

## Privacy / Integritet

Inga privata uppgifter får committas, och de får inte stå i PR-text (titel, beskrivning eller kommentar). Det gäller:

- personlig e-post — använd GitHubs noreply-adress i stället
- telefonnummer
- postadresser och hemadresser
- namn på privatpersoner
- interna IP-adresser
- Tailscale-värdnamn
- användarnamn i sökvägar
- nycklar och tokens
- innehåll i `.env`

Kör `pre-commit install` lokalt så att gitleaks granskar staged ändringar mot `.gitleaks.toml` före varje commit.

Agenter som hittar privata uppgifter maskerar dem med platshållare och skriver aldrig ut själva värdet i en commit, en pull request eller en logg. Använd till exempel `<email>`, `<user>`, `192.168.x.y`, `10.x.y.z`, `100.64.0.x` och `<host>.ts.net`.
