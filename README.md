# diogonmoura.com

Personal site of Diogo N. Moura — strategy operator for scale-up founders. Porto, Portugal.

Hosted at **https://diogonmoura.com**.

## Stack

Static HTML + CSS. No build, no framework, no JavaScript dependencies beyond a small inline `<script>` for the dark-mode toggle. Fonts loaded from [Bunny Fonts](https://fonts.bunny.net/) (privacy-friendly, no Google Fonts).

## Run locally

Any static server. Two one-liners:

```bash
# Python (no install needed)
python3 -m http.server 8000

# Or Node
npx serve .
```

Then open http://localhost:8000.

## Deploy

Connected to **Cloudflare Pages** — every push to `main` re-deploys automatically.

- Build command: *(none)*
- Output directory: `/` (repo root)
- Production branch: `main`

To deploy manually via Wrangler:
```bash
npx wrangler pages deploy . --project-name=diogonmoura --branch=main
```

## Languages

- **English** — public.
- **Portuguese** — present at `/pt/` but `noindex,nofollow` and not linked from any EN page. Pending content review before going public. To unhide later: remove `<meta name="robots" content="noindex, nofollow">` from `pt/index.html`, restore the EN→PT toggles in the topbar/footer of EN pages, restore hreflang alternates, re-add `/pt/` to `sitemap.xml`.

## Structure

```
/                       EN home (single-page sections)
/legal/                 EN legal notice
/privacy/               EN privacy policy
/pt/                    PT mirror — currently hidden
/pt/aviso-legal/        PT — hidden
/pt/privacidade/        PT — hidden
/robots.txt             crawl directives (explicit AI-bot allow)
/sitemap.xml
/llms.txt               AI answer-engine summary
/favicon.svg            32×32 monogram
/og.svg + og.png        OpenGraph card (1200×630)
/_headers               Cloudflare Pages headers (HSTS, cache)
/styles.css
```

## Theme

Auto-respects `prefers-color-scheme` on first visit. Manual toggle (sun/moon) in the topbar overrides and persists in localStorage. URL param `?theme=dark` or `?theme=light` overrides both — useful for sharing a themed link.

## License

All content © Diogo N. Moura. Not licensed for reuse.
