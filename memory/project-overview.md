---
name: project-overview
description: "Stato e identità del progetto libro-informatica-2 — libro di informatica in italiano, authoring autonomo on-demand, spec ancora da definire."
metadata: 
  node_type: memory
  type: project
  originSessionId: c9c4f352-b32a-41f7-97eb-9edd829e2198
---

**`libro-informatica-2`** è un progetto di authoring di un **libro di informatica
in italiano** condotto semi-autonomamente con Claude Code.

Stato al 2026-06-21:
- Repo inizializzato (vuoto a parte la configurazione harness). Nessun contenuto
  del libro ancora scritto.
- Harness configurato: project `CLAUDE.md`, `.claude/settings.json`, scheletro
  cartelle (`book/`, `research/`, `docs/`).
- **Memoria in-repo + sincronizzata**: `memory/` dentro il repo, auto-gestita,
  versionata e pushata su `origin`. Config in `.claude/settings.local.json`.
  Vedi [[harness-architecture]].
- **Permessi: l'utente vuole "permessi liberi"** ma il classifier auto-mode ha
  bloccato l'auto-concessione di un allowlist blanket (self-widening). Stato
  attuale: allowlist esteso (incl. git push/pull/fetch, mv/cp/python3), deny solo
  su `rm`. La decisione di passare a bypass totale spetta all'utente
  (`/config` → Permissions, oppure `--dangerously-skip-permissions`).
- **Specifica del libro DA DEFINIRE**: tipo (scuola superiore / universitario /
  guida pratica / volume 2 di una serie), pubblico, livello, indice. L'utente
  ha detto che fornirà le info in seguito. Finché non arrivano: non inventare
  contenuti o struttura dei capitoli.

Modello operativo: on-demand, nessuna schedulazione. Vedi [[harness-architecture]].
Lavoro tracciato in [[task-queue]]. Convenzioni in [[style-conventions]].
