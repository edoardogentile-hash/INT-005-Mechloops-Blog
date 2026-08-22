# INT-005 — Mechloops Blog

Blog pubblico Mechloops costruito con Astro e distribuito sotto
`https://mechloops.com/blog`.

## Runtime

- `src/` — pagine, layout, componenti, stili e contenuti Markdown.
- `public/` — asset statici, favicon e robots.
- `astro.config.mjs` — sito canonico, base `/blog`, Tailwind e sitemap.
- `vercel.json` — contratto di build Vercel.
- `package.json`, `package-lock.json`, `tsconfig.json` — toolchain Node.
- `.vscode/` — configurazione editor per Astro.

Questi percorsi formano un unico sito e restano nella repo madre. I file di
configurazione in radice sono eccezioni tecniche necessarie alla build.
`dist/`, `.astro/` e `node_modules/` sono generati e ignorati.

## Stato editoriale

Il contenuto pubblicato vive in `src/content/blog/`. Ogni articolo deve
rispettare lo schema in `src/content.config.ts`; le route derivano dallo slug.
Non cambiare `site` o `base` senza verificare URL canonici, sitemap, link e
configurazione di hosting.

## Verifica

```bash
npm ci
npm run build
```

L'anteprima locale usa normalmente la porta 4321. Dopo cambi di percorso o
configurazione va riavviata e controllata su `/blog/` e su una pagina articolo.

Decisioni durevoli: `LOG-DECISIONI.md`. Stato e prossimi controlli:
`RIPRESA.md`.
