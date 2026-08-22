# Ripresa — Mechloops Blog

Aggiornato: 2026-08-22

## Stato

Il sito contiene una home blog e un articolo pubblico. La build genera pagine,
sitemap e asset sotto la base `/blog`.

L'audit del 22-08-2026 è sceso da nove a tre advisory con gli aggiornamenti
non-breaking. Le due advisory alte residue richiedono il salto maggiore da
Astro 6 ad Astro 7: aggiornarlo e collaudarlo separatamente, senza
`npm audit fix --force` durante la migrazione strutturale.

Non risultano interventi di codice aperti in questa repo. La crescita del
catalogo editoriale va coordinata con il Marketing Center e verificata contro
lo schema di `src/content.config.ts`.

## Controllo prima della pubblicazione

1. Eseguire `npm run build` senza warning bloccanti.
2. Aprire `/blog/` e almeno una route articolo nell'anteprima locale.
3. Verificare canonical URL, sitemap, metadata e link esterni.
4. Controllare che `dist/`, `.astro/` e `node_modules/` non siano tracciati.

Il server locale sulla porta 4321 va riavviato nel collaudo finale del
workspace.
