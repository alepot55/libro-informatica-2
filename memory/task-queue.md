---
name: task-queue
description: Coda persistente dell'incarico editoriale — gap analysis competitor vs NLD e redazione integrazioni. Fonte di verità del lavoro.
metadata:
  node_type: memory
  type: project
  originSessionId: c9c4f352-b32a-41f7-97eb-9edd829e2198
---

Coda di lavoro per l'incarico NLD (vedi [[incarico-editoriale]], [[fonti]]).
Stato voci: `todo` → `in corso` → `done`.

## Completati
- [x] Ingestione e organizzazione fonti (`research/sources/` + `research/extracted/`).
- [x] Ricostruzione indice RIPAM (testo non estraibile) → `research/extracted/nld-ripam-583-index.md`.
- [x] Brief incarico → `docs/incarico-editoriale.md`; mappatura in memoria.

## In corso
_(nessuno)_

## Backlog — FASE 1: Gap analysis (priorità ALTA, in scadenza)
- [ ] Tabella di copertura: ogni voce di **Competitor Parte I** mappata su
      NLD-informatica + NLD-RIPAM, con classificazione Coperto / Mancante /
      Da approfondire + note di livello.
- [ ] Idem per **Competitor Parte II** (Office automation).
- [ ] Sintesi: elenco ordinato dei gap (mancanti + da approfondire) → output
      fase 1 per la redazione. Salvare in `docs/gap-analysis.md`.

## Backlog — FASE 2: Integrazioni
- [ ] Per ogni gap confermato, redigere la trattazione ex novo in `book/`
      (italiano, taglio coerente col volume NLD di destinazione).
- [ ] Review (tecnica + editoriale) e verifica esempi di codice.

## Decisioni aperte (da confermare con utente/redazione)
- A quale dei due volumi NLD è destinata ciascuna integrazione (base vs avanzato)?
- Formato/lunghezza attesa delle integrazioni.
