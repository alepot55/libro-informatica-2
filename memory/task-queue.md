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
- [x] Ricostruzione indici via vision (RIPAM + NLD-Info TOC completa).
- [x] Brief incarico → `docs/incarico-editoriale.md`; mappatura in memoria.
- [x] **FASE 1 — Gap analysis completa** → `docs/gap-analysis.md`. Risultati in
      [[gap-analysis-findings]]. Parte II del competitor = interamente coperta;
      gap concentrati nella Parte I.

## In corso
_(nessuno)_

## Backlog — FASE 2: Integrazioni (in attesa di conferma redazione)
Ordine di priorità (gap 🔴 mancanti prima):
- [ ] 1. Algoritmi e strutture dati (complessità O/Ω/Θ, sorting, strutture dati).
- [ ] 2. UML (use case, class, sequence, state chart, activity).
- [ ] 3. Trasmissione dati: rilevazione errori (parità/CRC), commutazione, ATM/frame relay/ADSL.
- [ ] 4. SO da riga di comando: MS-DOS/CLI, Linux (BASH, permessi, comandi, sudo).
- [ ] 5. Big Data: ecosistema Hadoop/Spark.
- [ ] 6. Software security: buffer overflow, vulnerabilità di memoria.
- [ ] 7-13. Voci 🟡 "da approfondire" (vedi `docs/gap-analysis.md`).
- [ ] Review (tecnica + editoriale) e verifica esempi di codice per ogni integrazione.

## Decisioni aperte (da confermare con utente/redazione)
- A quale volume NLD destinare ciascuna integrazione (base = NLD-Info vs avanzato = RIPAM)?
- Formato/lunghezza attesa delle integrazioni.
- Verificare i capitoli RIPAM **online** (Parte VI Cap 4 SO; Parte VII Cap 5 sicurezza web)
  prima di confermare i gap su Linux/CLI e sicurezza applicativa.
