---
name: harness-architecture
description: "Decisione architetturale dell'harness di authoring — memoria a due livelli, agent on-demand, nessun cron."
metadata: 
  node_type: memory
  type: project
  originSessionId: c9c4f352-b32a-41f7-97eb-9edd829e2198
---

Harness di authoring per libro-informatica-2 (scelto con l'utente il 2026-06-21).

**Esecuzione**: autonoma **on-demand**. Niente cron / scheduled task — l'utente
lancia i task in sessione; Claude esegue il ciclo draft → review → revisione.

**Memoria in-repo, automatica, sincronizzata (aggiornato 2026-06-21)**:
- Memoria durevole in `<repo>/memory/` — **dentro il repository**, versionata e
  pushata su `origin` insieme al contenuto. Indicizzata da `memory/MEMORY.md`.
  Auto-gestita: `autoMemoryEnabled` + `autoMemoryDirectory` (= path repo) +
  `autoDreamEnabled` in `.claude/settings.local.json` (locale, git-ignored
  perché contiene path assoluti).
- `.remember/` nel repo: buffer di sessione effimero, **locale/non
  sincronizzato**; a fine sessione si distilla in `memory/`.
- Motivo del cambio: l'utente vuole la memoria tutta dentro la repo e
  sincronizzata con GitHub, gestita automaticamente.

**Comportamento**: definito in project `CLAUDE.md` (precedenza sul CLAUDE.md
workstation genitore) + `.claude/settings.json` (permessi). L'utente ha chiesto
**permessi liberi**; il classifier auto-mode dell'harness ha però bloccato
l'auto-concessione di un allowlist blanket (self-widening) — la scelta di
allargare i permessi resta all'utente (vedi nota in [[project-overview]]).

**Agent**: usati on-demand per review (`code-reviewer` per esempi di codice;
review editoriale per il testo). Nessun agent in background.

**Perché**: il libro è il deliverable; lo stato deve sopravvivere ai confini di
sessione tramite memory, mentre l'esecuzione resta sotto controllo dell'utente.
Vedi [[project-overview]].
