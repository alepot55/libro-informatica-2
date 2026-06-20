# libro-informatica-2

Progetto di authoring di un **libro di informatica in italiano**, scritto in modo
semi-autonomo con Claude Code.

> Specifica del libro (scope, pubblico, indice) **da definire**. Vedi
> `CLAUDE.md` per il modello operativo e `docs/` per la spec quando disponibile.

## Struttura

| Cartella | Contenuto |
|----------|-----------|
| `book/` | Il manoscritto: un file Markdown per capitolo/sezione. |
| `research/` | Fonti, appunti e materiale di riferimento (input). |
| `docs/` | Specifica del libro, indice/outline, decisioni di stile. |
| `.claude/` | Configurazione harness (permessi, comportamento). |

## Come si lavora

Authoring on-demand: l'utente lancia i task, Claude esegue il ciclo
draft → review → revisione mantenendo lo stato nella memoria persistente.
Dettagli in [`CLAUDE.md`](./CLAUDE.md).
