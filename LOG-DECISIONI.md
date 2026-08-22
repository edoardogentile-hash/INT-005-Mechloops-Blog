# Log decisioni

## 2026-04 — prima versione

- Astro statico con contenuti Markdown tipizzati.
- Tailwind CSS per lo stile e sitemap generata in build.
- Pubblicazione sotto il prefisso `/blog` del dominio Mechloops.
- Vercel usa `npm run build` e pubblica `dist/`.
- Il primo articolo è una guida pillar sull'AI nelle PMI italiane.

## 2026-08-22 — standard repository

- Il sito resta un'unica unità nella madre; non serve una sottorepo ulteriore.
- Configurazioni Astro, Node, TypeScript e Vercel restano in radice perché la
  piattaforma le rileva lì.
- Il README generico dello starter Astro è stato archiviato: non descriveva il
  sistema reale.
