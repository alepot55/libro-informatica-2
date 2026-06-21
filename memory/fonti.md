---
name: fonti
description: Le tre fonti dell'incarico (competitor + 2 volumi NLD), loro struttura e caveat di estrazione testo.
metadata:
  type: reference
---

Tre indici-sorgente, in `research/sources/` (PDF) e `research/extracted/` (testo).
Contesto in [[incarico-editoriale]].

1. **Competitor — Simone 328/5** *Concorsi per Informatici nella P.A.* (2024,
   25pp). `competitor-index.pdf` → `.txt` (estrazione OK).
   **Ambito confronto = Parti I-II**: Parte I *Informatica avanzata* (10 cap:
   architetture, trasmissione dati, SO, programmazione, reti, algoritmi/strutture
   dati, ingegneria del software, database, big data, cybersecurity); Parte II
   *Office automation* (Word, Excel, presentazioni, posta, Access). Parti III+ =
   diritto → fuori ambito.

2. **NLD — Informatica per tutti i concorsi** (2026, 432pp, curato da Alessandro).
   `nld-informatica-tutti-concorsi-index.pdf` → `.txt` (OK, lievi lacune
   watermark). Tutto informatico, taglio **base**: Parte I (17 cap) + Parte II
   (17 cap). HW/SW, SO, Office, database, reti, sicurezza, cittadinanza digitale,
   ISMS base.

3. **NLD — RIPAM 583 Informatici** (800pp). `nld-ripam-583-index.pdf`.
   ⚠️ **Testo NON estraibile** (font custom: pdftotext rende solo i puntini) →
   indice ricostruito via vision in `research/extracted/nld-ripam-583-index.md`
   (usare quello). Volume ampio (Parti I-XXI). **Nucleo informatico = Parti
   V-XIV** (CAD/digitale, HW/SW/SO, sviluppo web, database avanzati, reti+cripto,
   sicurezza, project/service mgmt, Agile, metodologie sviluppo/test, ISMS/ISO),
   taglio **avanzato**.

**Caveat operativo**: per dettaglio fine su RIPAM (e in caso di lacune sul NLD
informatica) usare la **lettura visiva del PDF**, non il testo estratto.
`tesseract` non è installato; `pdftotext`/`pdfinfo`/`gs` sì.
