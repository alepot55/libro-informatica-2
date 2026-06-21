---
name: project-overview
description: "Stato e identità del progetto libro-informatica-2 — incarico editoriale NLD: gap analysis competitor vs 2 volumi NLD + integrazioni informatica."
metadata: 
  node_type: memory
  type: project
  originSessionId: c9c4f352-b32a-41f7-97eb-9edd829e2198
---

**`libro-informatica-2`** è un **incarico editoriale** per la redazione NLD
concorsi: gap analysis tra l'indice del competitor (Parti I-II) e due volumi NLD,
poi redazione delle integrazioni di informatica. Dettaglio in [[incarico-editoriale]]
e [[fonti]]. **Non** è la scrittura di un libro da zero.

Stato al 2026-06-21:
- Fonti ingestite e mappate (3 indici in `research/`); brief in `docs/`.
- Prossimo: **gap analysis (fase 1)**, in scadenza. Vedi [[task-queue]].
- Harness configurato: project `CLAUDE.md`, `.claude/settings.json`, scheletro
  cartelle (`book/`, `research/`, `docs/`).
- **Memoria in-repo + sincronizzata**: `memory/` dentro il repo, auto-gestita,
  versionata e pushata su `origin`. Config in `.claude/settings.local.json`.
  Vedi [[harness-architecture]].
- **Permessi: l'utente ha scelto il BYPASS TOTALE** via
  `claude --dangerously-skip-permissions` (deciso il 2026-06-21). È un flag di
  avvio: nessun prompt di permessi, nessun guardrail, per tutta la sessione.
  Va lanciato dall'utente (l'agente non può auto-concederselo: il classifier
  auto-mode blocca il self-widening). `.claude/settings.json` mantiene comunque
  un allowlist esteso (git completo, rg/ls/cat/wc/mkdir/tree; deny su `rm` e
  force/mirror push) come fallback per le sessioni avviate SENZA il flag.

Modello operativo: on-demand, nessuna schedulazione. Vedi [[harness-architecture]].
Lavoro tracciato in [[task-queue]]. Convenzioni in [[style-conventions]].
