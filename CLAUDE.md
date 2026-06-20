# CLAUDE.md — libro-informatica-2

Guida operativa per Claude Code in questo repository.

> **Questo NON è l'ambiente-workstation** descritto nel `CLAUDE.md` della home
> (`/home/alepot55/CLAUDE.md`, hardware/sysadmin). Quello è un genitore ereditato:
> ignora il suo contesto "non è un repository" — **questo è un progetto di
> authoring di un libro** e ha la precedenza per ogni decisione che riguarda
> questo repo.

## 1. Identità del progetto

`libro-informatica-2` è un progetto di **scrittura di un libro di informatica in
italiano**, condotto in modo semi-autonomo con Claude Code.

- **Lingua del libro**: italiano. Tutto il contenuto del libro (capitoli,
  esercizi, esempi) è in italiano.
- **Lingua di lavoro / config / git**: inglese per messaggi di commit e nomi
  file; italiano nella comunicazione con l'utente.
- **Specifica del libro (scope, pubblico, indice): DA DEFINIRE.** L'utente
  fornirà i dettagli (tipo di libro, livello, struttura) in un secondo momento.
  Finché non arrivano, NON inventare contenuti né struttura dei capitoli:
  registra ciò che è noto in memory e chiedi quando serve una decisione di
  contenuto.

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

Lo stato del progetto vive in **due** sistemi complementari:

| Sistema | Path | Scopo |
|---------|------|-------|
| Built-in memory | `~/.claude/projects/-home-alepot55-project-libro-informatica-2/memory/` | Fatti stabili: stato progetto, decisioni, **task queue**, preferenze. Indice in `MEMORY.md`. |
| `.remember/` | `<repo>/.remember/` | Buffer di sessione / handoff (`remember.md`), log giornalieri. Git-ignored. |

Regole:
1. A inizio sessione, l'indice `MEMORY.md` è caricato in contesto. Consultalo.
2. La **coda dei task** del libro è in `memory/task-queue.md` — è la fonte di
   verità su cosa scrivere/rivedere. Aggiornala man mano.
3. Salva in memory: decisioni su struttura del libro, convenzioni di stile
   emerse, stato dei capitoli (draft/review/done), feedback dell'utente.
4. Scrivi l'handoff di fine sessione in `.remember/remember.md`.
5. Una memoria = un file con frontmatter; aggiorna il file esistente invece di
   duplicare.

## 4. Layout del repository

```
libro-informatica-2/
├── CLAUDE.md            # questo file
├── README.md           # overview del progetto
├── .claude/
│   └── settings.json   # permessi + comportamento harness
├── book/               # il manoscritto: un file .md per capitolo/sezione
├── research/           # fonti, appunti, materiale di riferimento (input)
├── docs/               # spec del libro, indice/outline, decisioni
└── .remember/          # buffer/handoff di sessione (git-ignored)
```

(`book/`, `research/`, `docs/` partono vuoti — la struttura interna segue la
specifica del libro quando arriva.)

## 5. Workflow di authoring (on-demand)

Quando l'utente chiede di scrivere/rivedere:

1. **Outline first** — se la sezione non è in `task-queue.md`, definisci scopo,
   prerequisiti, obiettivi didattici prima di scrivere.
2. **Draft** — scrivi il contenuto in `book/<...>.md`, italiano, didattico.
3. **Review** — usa un agent (`code-reviewer` per esempi di codice;
   review editoriale per il testo) per coerenza, accuratezza tecnica, livello.
4. **Revise** — applica i fix; aggiorna lo stato in `task-queue.md`.
5. **Commit** quando la sezione è stabile.

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
