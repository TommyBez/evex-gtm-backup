# SEO

Direttiva, gate, GSC, e ciò che è già live.
Parte del grafo gtm: indice in [../STATE.md](../STATE.md).
Vedi anche: [regole](regole.md), [agenti](agenti.md), [directory e backlinks](directory-backlinks.md), [strumenti](strumenti.md).

## Direttiva

**300 impression organiche medie al giorno entro il 2026-09-27** (Tommy, 28/08).

Gate:

- 3 settembre: ≥40/giorno e inspect ≠ unknown su hub `/agents`, GIM, DKA, `/learn`
- 10 settembre: ≥80/giorno

Search Counsel è consulente, non un posto fisso. PMM resta owner del play.

Piano a 30 giorni (Search Counsel, 28/08). Stretch dichiarato: 26/giorno → 300 è circa 11×. Non esiste una query testa. Non pSEO grid. Non Indexing API. Non click UI GSC.

Aim: eve agent framework; install Eve agent; @evex/{name}; github issue Eve agent; docs knowledge Eve agent; mcp server for Eve agents.
Reject: eve harlow / night agent; eve white literary; eve online; bare shadcn registry; bare evex finché la SERP non è nostra.

Ordine (URL esistenti prima) e stato:
1. `/agents` come pagina eve agent framework, H1 unico, inventario crawlable — SHIPPED (#70 + nav #68).
2. Title pass job-intent su `/agents/*` già in sitemap — SHIPPED (#70).
3. noindex (o canonical) sui filtri `/?category=*` e `q` — SHIPPED (#71).
4. Espandere i due Learn già esistenti, niente sezione nuova — SHIPPED (#71/#72), Learn in header (#73).
5. Nuove URL Learn solo su near-miss GSC (≥150 impr, pos 5–20, niente URL dedicata). Default: iterare, non spawnare.

Cancelli (7d trailing daily avg, service account + URL Inspection):
- 3/09: inspect ≠ unknown su `/`, `/agents`, GIM, DKA, Learn. Media ≥40/giorno. Se hub ancora unknown, Soft Eng verifica link crawlable, non request indexing.
- 10/09: ≥80. Se <60, stop nuove URL, solo titoli + internal link, dire a Tommy che 300 è off-track.
- 17/09: ≥150. Kill se <100.
- 24/09: ≥250.
- 27/09: media 7d vs 300. Reportare il numero, non spostare i pali su click o AIO.

Inspect lunedì 1/09 è il primo check di quel piano, non un freeze.

## GSC (agg. 30/08 ~21:25)

Proprietà `sc-domain:evex.sh`. Ricetta in [strumenti.md](strumenti.md).

- Ultimo giorno completo: **2026-08-28** 1 click / 27 impression
- 7 giorni 22–28 agosto: **4 click / 181 impression** (~26/giorno)
- 29–30 agosto: non ancora in API
- Inspect **bloccato fino a lunedì 1 settembre**. Non ispezionare prima. L'inspect del lunedì è un check, non un freeze.

## Shipped

Storia PR per PR non sta in STATE. Qui il set live:

- `/agents` 200 — #66 + nav #68
- Job-intent titles — #70
- noindex filtri — #71
- `/learn` Eve agent guides — #72
- Learn in header — #73 mergiata 29/08 14:28 CEST
- Sitemap: 33 loc

Packs:

- Audit 11/08: [../packs/seo-audit-2026-08-11.md](../packs/seo-audit-2026-08-11.md)
- AI-SEO 13/08 (#58 #59): [../packs/ai-seo-proposal-2026-08-12.md](../packs/ai-seo-proposal-2026-08-12.md) e copy PR-B in `packs/`

## Lezioni

- **Non ispezionare prima di lunedì 1 settembre.**
- **Non aggiungere un URL nuovo il giorno dopo un batch live** (lezione island).
