# Hiraeth Legal Pages

Public legal documents for the **Hiraeth** Discord bot (a project developed by Necel).
Hosted with GitHub Pages. These pages are the canonical source for the Terms of Service
and Privacy Policy URLs configured in the Discord Developer Portal.

## Pages

| Document | URL |
| --- | --- |
| Privacy Policy (ES + EN) | https://lucianonecel.github.io/hiraeth-legal/privacy-policy.html |
| Terms of Service (ES + EN) | https://lucianonecel.github.io/hiraeth-legal/terms-of-service.html |

## Layout

- `index.html` — simple landing page linking both documents.
- `privacy-policy.html` — bilingual policy; Spanish section (`#es`) first, English section (`#en`) second.
- `terms-of-service.html` — bilingual terms, same structure.
- `.nojekyll` — serves files verbatim (no Jekyll processing).

Each page is fully self-contained (inline CSS, no external resources, no build step).

## How to update

1. Edit the HTML file directly (keep the ES and EN sections in sync — they must always say the same thing).
2. Bump the "Last updated / Última actualización" date and the version in the footer.
3. Commit and push to `main`; GitHub Pages republishes automatically within a minute.
4. If the document was materially changed, verify the effective date is correct — the Discord
   Developer Portal links themselves do not need to change unless the URLs change.

## Content accuracy rule

The Privacy Policy must reflect **actual bot behavior** (what is stored, sent to third parties,
and retained). It was drafted from a verified audit of the bot's data models and external API
calls (2026-09-01). Whenever the bot starts storing new user data, calling a new third-party
API, or changes retention (TTLs), update `privacy-policy.html` in the same release cycle.

## Future: custom domain

To move to a personal domain later without breaking the Discord portal links:

1. Add a `CNAME` file with the domain (e.g. `legal.midominio.com`).
2. Configure the DNS `CNAME` record pointing to `lucianonecel.github.io`.
3. Enable HTTPS in the Pages settings.
4. Optionally update the URLs in the Discord Developer Portal → General Information.

## Disclaimer

These documents are written in plain language for bot users and are not formal legal advice.
If the project ever charges money, adds real-money features, or expands to regions beyond
Argentina, have them reviewed by a lawyer.
