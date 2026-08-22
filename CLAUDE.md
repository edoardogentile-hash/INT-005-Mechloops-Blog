# INT-005 — Mechloops Blog

Blog pubblico Mechloops costruito con Astro e distribuito sotto
`https://mechloops.com/blog`.

## Runtime

- `codice/src/` — pagine, layout, componenti, stili e contenuti Markdown.
- `codice/public/` — asset statici, favicon e robots.
- `codice/astro.config.mjs` — sito canonico, base `/blog`, Tailwind e sitemap.
- `codice/vercel.json` — contratto di build Vercel.
- `codice/package.json`, `codice/package-lock.json`, `codice/tsconfig.json` — toolchain Node.
- `codice/.vscode/` — configurazione editor per Astro.

Questi percorsi formano un unico sito e restano nella repo madre dentro la
cartella dinamica controllata `codice/`.
`dist/`, `.astro/` e `node_modules/` sono generati e ignorati.

## Stato editoriale

Il contenuto pubblicato vive in `codice/src/content/blog/`. Ogni articolo deve
rispettare lo schema in `codice/src/content.config.ts`; le route derivano dallo slug.
Non cambiare `site` o `base` senza verificare URL canonici, sitemap, link e
configurazione di hosting.

## Verifica

```bash
cd codice
npm ci
npm run build
```

Vercel deve usare `codice` come Root Directory. L'anteprima locale usa
normalmente la porta 4321. Dopo cambi di percorso o
configurazione va riavviata e controllata su `/blog/` e su una pagina articolo.

Decisioni durevoli: `LOG-DECISIONI.md`. Stato e prossimi controlli:
`RIPRESA.md`.
