# Incarico editoriale — Tecnico Informatico (NLD concorsi)

## Committente
Redazione **NLD concorsi** (rif. Camilla). Email "Proposta editoriale: Tecnico
Informatico" del **2026-06-15**.

## Oggetto
Elaborazione **ex novo** di alcune trattazioni in materia di **informatica di
base e avanzata**, come integrazione ai volumi NLD.

## Lavoro richiesto (due fasi)
1. **Gap analysis** — confronto tra l'indice del **volume competitor**
   (limitatamente alle **Parti I e II**) e gli indici di **due volumi NLD**, per
   individuare **contenuti mancanti o meritevoli di approfondimento**.
2. **Integrazioni** — redazione dei contenuti per colmare i gap individuati.

## Scadenze (dall'email del 2026-06-15)
- Indicazione contenuti mancanti/da approfondire: **entro 2-3 giorni** (≈ 18 giu).
- Trasmissione integrazioni: **entro fine settimana** (≈ 21 giu).
- ⚠️ Oggi è 2026-06-21: entrambe le scadenze sono **in scadenza/scadute** →
  priorità alta.

## Fonti (in `research/sources/`, testo in `research/extracted/`)

### 1. Competitor — *Concorsi per Informatici nella P.A.* (Simone 328/5, 2024)
`competitor-index.pdf` · 25 pp · estrazione testo OK.
**Ambito del confronto = solo Parti I e II:**
- **Parte I — Informatica avanzata** (10 capitoli): 1) Sistemi elaborativi e
  architetture; 2) Trasmissione dati; 3) Sistemi operativi (MS-DOS, Windows,
  Linux); 4) Principi di programmazione (C++, Python, Java, JavaScript, API REST);
  5) Comunicazione in rete (stack, HTTP/FTP/DNS, TCP/UDP, IP4/IP6, routing); 6)
  Algoritmi e strutture dati (complessità O/Ω/Θ, sorting, liste/code/pile/array/
  grafi/alberi); 7) Ingegneria del software (ciclo di vita, UML, pattern, V&V,
  Agile, Linee Guida AgID); 8) Strutture informative e Database (modello
  relazionale, E-R, SQL DDL/DML/DCL, 3-tier, LAMP); 9) Big Data (5V, Hadoop,
  Spark, NoSQL/MongoDB, Data Science, GDPR); 10) Cybersecurity (network/software/
  system security, crittografia, malware, BC/DR).
- **Parte II — Office automation** (5 capitoli): 1) Word; 2) Excel; 3)
  Presentazioni; 4) Posta elettronica (Outlook/Gmail); 5) Database (Access).
- (Parti III-VIII = diritto/questionari → **fuori ambito**.)

### 2. NLD — *Informatica per tutti i concorsi* (2026, 432 pp) — curato da Alessandro
`nld-informatica-tutti-concorsi-index.pdf` · 16 pp · estrazione testo OK (lievi
lacune da watermark, vedi `.txt`).
Volume interamente informatico: **Parte I — Fondamenti e sviluppi dell'informatica**
(17 capitoli) + **Parte II** (17 capitoli, versione sintetica/operativa). Copre
hardware/software, SO, Office (Word/Excel/PowerPoint), database, reti, comunicare/
collaborare in rete, sicurezza informatica, cittadinanza digitale, e ISMS/governance
IT (ISO 27000, framework). Taglio **base/divulgativo**.

### 3. NLD — *RIPAM 583 Informatici* (800 pp) — volume concorsuale approfondito
`nld-ripam-583-index.pdf` · 34 pp · **testo NON estraibile** (font custom) →
indice ricostruito via vision in `research/extracted/nld-ripam-583-index.md`.
Volume ampio (Parti I-XXI: diritto, logica, ecc.). **Nucleo informatico = Parti
V-XIV**: V) CAD/amministrazione digitale; VI) hardware/software/architetture/SO;
VII) sviluppo web client/server; VIII) database relazionali (fino a transazioni/
ottimizzazione/sicurezza); IX) reti e crittografia; X) sicurezza sistemi/reti;
XI) project & service management (PMI/COBIT/PRINCE2/ITIL/CMMI); XII) Agile; XIII)
metodologie di sviluppo e test; XIV) ISMS/ISO 27000-20000. Taglio **avanzato**.

## Approccio alla gap analysis (proposto)
Mappare ogni voce di **Competitor Parte I-II** sui due volumi NLD:
- **Coperto** (presente in NLD ≥ pari livello) → nessuna azione.
- **Mancante** (assente in entrambi i NLD) → candidato a integrazione ex novo.
- **Da approfondire** (presente ma più superficiale del competitor) → candidato
  ad ampliamento.
Output fase 1: tabella di copertura competitor→NLD con classificazione e note.
Output fase 2: trattazioni redatte per le voci mancanti/da approfondire.

## Stato
- [x] Fonti ingestite e mappate (file + memoria).
- [ ] Gap analysis (fase 1) — da avviare.
- [ ] Integrazioni (fase 2).
