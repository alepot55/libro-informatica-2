# CLAUDE.md — libro-informatica-2

Guida operativa per Claude Code in questo repository.

> **Questo NON è l'ambiente-workstation** descritto nel `CLAUDE.md` della home
> (`/home/alepot55/CLAUDE.md`, hardware/sysadmin). Quello è un genitore ereditato:
> ignora il suo contesto "non è un repository" — **questo è un progetto di
> authoring di un libro** e ha la precedenza per ogni decisione che riguarda
> questo repo.

## 1. Identità del progetto

`libro-informatica-2` è un **incarico editoriale** per la redazione **NLD
concorsi**: confrontare l'indice di un volume **competitor** (solo Parti I-II)
con due volumi **NLD**, individuare i **gap** (contenuti mancanti o da
approfondire) e redigere **ex novo le integrazioni** di informatica.
Brief completo: `docs/incarico-editoriale.md`. Memoria: vedi `memory/`.

- **Lingua dei contenuti**: italiano. Tutte le integrazioni (testo, esercizi,
  esempi) sono in italiano.
- **Lingua di lavoro / config / git**: inglese per commit e nomi file; italiano
  nella comunicazione con l'utente.
- **Fonti** in `research/sources/` (PDF) e `research/extracted/` (testo).
  ⚠️ L'indice **RIPAM non è estraibile** come testo → usare
  `research/extracted/nld-ripam-583-index.md` (ricostruito via vision).

## 2. Modello operativo

Authoring **autonomo on-demand**: nessuna schedulazione/cron. L'utente lancia i
task; Claude esegue draft → review → revisione usando gli agent, mantenendo lo
stato nella memoria persistente.

Principi (dai rules globali in `~/.claude/rules/`):
- Task piccoli/chiari → agisci. Decisioni di contenuto/struttura impattanti →
  proponi prima.
- File piccoli e focalizzati. Un capitolo/sezione per file. Markdown.
- Self-review prima di consegnare; per revisioni sostanziali usa gli agent.
- Commit quando qualcosa funziona o prima di modifiche rischiose. Inglese,
  conciso, niente attribuzione AI.

## 3. Protocollo di memoria (LEGGERE A INIZIO SESSIONE)

La memoria è **in-repo, automatica e sincronizzata con GitHub**: vive dentro il
repository, è gestita automaticamente da Claude Code e viene committata/pushata
su `origin` insieme al contenuto.

| Sistema | Path | Scopo |
|---------|------|-------|
| Memoria durevole (auto-memory) | `<repo>/memory/` | Fatti stabili: stato progetto, decisioni, **task queue**, convenzioni. Indice in `memory/MEMORY.md`. **Versionata e pushata.** Auto-gestita via `autoMemoryEnabled` + `autoMemoryDirectory` + `autoDreamEnabled` in `.claude/settings.local.json`. |
| Buffer di sessione | `<repo>/.remember/` | Scratch/handoff effimero (`remember.md`), log. **Locale, NON sincronizzato.** A fine sessione distilla ciò che conta dentro `memory/`. |

Regole:
1. A inizio sessione l'indice `memory/MEMORY.md` è caricato automaticamente.
   Consultalo.
2. La **coda dei task** è in `memory/task-queue.md` — fonte di verità del lavoro.
   Aggiornala man mano.
3. Salva in `memory/`: decisioni su struttura/stile, stato dei capitoli
   (draft/review/done), feedback dell'utente.
4. Una memoria = un file con frontmatter; aggiorna il file esistente invece di
   duplicare; collega le memorie con `[[nome]]`.
5. **Committa e pusha la memoria** insieme al contenuto: fa parte del repo.

## 4. Layout del repository

```
libro-informatica-2/
├── CLAUDE.md            # questo file
├── README.md           # overview del progetto
├── .claude/
│   ├── settings.json        # comportamento harness (versionato)
│   └── settings.local.json  # auto-memory + config locale (git-ignored)
├── memory/             # memoria durevole auto-gestita (versionata, pushata)
├── research/
│   ├── sources/        # PDF originali degli indici (3 fonti)
│   └── extracted/      # testo estratto + indice RIPAM ricostruito (.md)
├── docs/               # brief incarico, gap-analysis (output fase 1)
├── book/               # integrazioni redatte ex novo (output fase 2)
└── .remember/          # buffer/handoff di sessione (locale, git-ignored)
```

## 5. Workflow dell'incarico (due fasi, on-demand)

**Fase 1 — Gap analysis** (in scadenza):
1. Mappa ogni voce di **Competitor Parte I-II** sui due volumi NLD.
2. Classifica: Coperto / Mancante / Da approfondire (+ note di livello).
3. Output → `docs/gap-analysis.md`; aggiorna `memory/task-queue.md`.

**Fase 2 — Integrazioni**:
1. Per ogni gap confermato, redigi la trattazione ex novo in `book/<...>.md`,
   italiano, taglio coerente col volume NLD di destinazione.
2. **Review** — agent `code-reviewer` per gli esempi di codice (devono essere
   corretti e testabili), review editoriale per il testo.
3. **Revise** + aggiorna `task-queue.md`. **Commit** quando stabile.

Esempi di codice nel libro: devono essere **corretti e testabili**. Verifica il
codice (eseguilo quando possibile) prima di includerlo.

## 6. Convenzioni di stile (placeholder)

Da consolidare quando arriva la specifica del libro. Default ragionevoli:
- Markdown, intestazioni gerarchiche, code fence con linguaggio esplicitato.
- Terminologia tecnica: forma originale (es. `array`, `compiler`), spiegata alla
  prima occorrenza.
- Una nuova convenzione concordata → registrala in `memory/` e qui.

## 7. Vincoli di sistema (dalla workstation)

8 GB RAM, no GPU, no npm/pip globali. Per tool/script preferisci Python di
sistema o C/C++. Vedi `~/.claude/CLAUDE.md` per i dettagli hardware.
