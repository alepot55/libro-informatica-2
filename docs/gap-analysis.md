# Gap analysis — Competitor (Simone 328/5, Parti I-II) vs volumi NLD

**Data:** 2026-06-21 · **Fase 1 dell'incarico** (vedi `incarico-editoriale.md`).

## Metodologia
Ogni voce dell'indice **competitor** (Simone 328/5 — *Concorsi per Informatici
nella P.A.*, ed. 2024), limitatamente a **Parte I (Informatica avanzata)** e
**Parte II (Office automation)**, è mappata sui due volumi NLD:
- **NLD-Info** = *Informatica per tutti i concorsi* (2026, taglio base/ampio).
- **NLD-RIPAM** = *RIPAM 583 Informatici* (800 pp, taglio avanzato; nucleo
  informatico nelle Parti V-XIV).

### Legenda verdetto
- **✅ Coperto** — presente in almeno un volume NLD a livello ≥ competitor.
- **🟡 Da approfondire** — presente ma più superficiale del competitor.
- **🔴 Mancante** — assente in entrambi i volumi NLD.

### Sintesi
Il competitor 2024 è un manuale tecnico "informatica avanzata"; i volumi NLD 2026
sono più ampi e aggiornati (coprono AI/ML, blockchain, quantum, IoT, cloud, OSI,
ITIL/COBIT/ISO 27000, Agile/Scrum, ecc.) e in molte aree **superano** il
competitor. I gap si concentrano quindi in **pochi temi tecnici classici** della
Parte I del competitor. **La Parte II (Office) è interamente coperta** (NLD è più
ricco). Tutti i gap rilevanti sono nella Parte I.

---

## PARTE I — Informatica avanzata

### Cap. 1 — Sistemi elaborativi e architetture
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Von Neumann, CPU (CU/ALU/registri), clock | Cap 2 | Parte VI Cap 2 | ✅ |
| Memorie (gerarchia, RAM/ROM, cache, massa) | Cap 2 | Parte VI Cap 2 | ✅ |
| Bus, interfacce, slot, porte, connettori | Cap 2 | Parte VI Cap 2 | ✅ |
| Periferiche (monitor, stampanti, modem) | Cap 2 | Parte VI Cap 2 | ✅ |
| Indicatori di prestazioni | Cap 2 (cenni) | Parte VI | ✅ |
| Architetture RISC/CISC | Cap 2 (3.5) | Parte VI | ✅ |
| **Linguaggio macchina e assembly** | — | — | 🟡 (NLD: solo cenni) |
| **Tassonomia di Flynn (SISD/SIMD/MISD/MIMD)** | — | — | 🟡 |
| **Classificazione sistemi (mainframe, mini, super, workstation)** | Cap 2 §7 (sistemi moderni) | Parte VI | 🟡 (NLD privilegia i sistemi moderni; classificazione classica più leggera) |

### Cap. 2 — Trasmissione dati
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Informazione e codifica, analogico/digitale | Cap 1 | Parte VI Cap 1 | ✅ |
| **Misura dell'informazione** | — | — | 🟡 |
| **Conversione A/D (campionamento, quantizzazione)** | Cap 1 (cenni) | — | 🟡 |
| Mezzi di trasmissione (guidati/non guidati, onde EM) | Cap 9 (1.4) | Parte IX | ✅ |
| **Modalità: seriale/parallela, sincrona/asincrona** | — | — | 🟡 |
| **Rilevazione errori (controllo di parità, CRC/redundancy check)** | — | — | 🔴 |
| **Tecniche di commutazione (circuito vs pacchetto)** | Cap 9 (analogia pacchetti) | Parte IX | 🟡 (manca la trattazione formale) |
| **Frame relay, ATM, ADSL** | — | — | 🔴 |
| Topologie di rete | Cap 9 (1.3) | Parte IX | ✅ |
| Architetture P2P e client-server | Cap 9 / Parte VII | Parte VII/IX | ✅ |

### Cap. 3 — Sistemi operativi
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| SO come gestore risorse, file system, multitasking | Cap 3-4 | Parte VI Cap 4 (online) | ✅ |
| GUI, gestione file/cartelle, Windows | Cap 4 | — | ✅ |
| Virtualizzazione | Cap 4 (10) | Parte VI | ✅ |
| **Processi/thread, interrupt ed eccezioni, programmazione concorrente** | Cap 3-4 (processi/multitasking, cenni) | — | 🟡 (manca interrupt/eccezioni/concorrenza formali) |
| **MS-DOS / riga di comando** | — | — | 🔴 |
| **Linux: distribuzioni, shell BASH, permessi file/directory, comandi** | — | Parte VI Cap 4 (online, da verificare) | 🔴 (assente in NLD-Info; in NLD-RIPAM online non confermato) |
| **Gestione utenti, sudo, comandi di rete (CLI)** | — | — | 🔴 |

### Cap. 4 — Principi di programmazione
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Ciclo di sviluppo, paradigmi, programmazione strutturata | Cap 1 (9), Cap 3 | Parte VII/XIII | ✅ |
| Linguaggi (panoramica), compilatori/interpreti | Cap 1 (9) | Parte VI/VII | ✅ |
| Linguaggi per il web (HTML/CSS/JS) | Cap 1 (9.6) | Parte VII | ✅ |
| API / API REST | Cap 1 (9.7) | Parte VII | ✅ |
| **Elementi del linguaggio e classi di istruzioni (I/O, calcolo, trasferimento, logiche)** | — | — | 🟡 |
| **Fondamenti pratici con esempi di codice (variabili, tipi, operatori, I/O) — es. Python/JavaScript** | Cap 1 (panoramica) | Parte VII (concettuale) | 🟡 (NLD resta a livello descrittivo, niente primer pratico) |
| **Assembly (linguaggio)** | — | — | 🟡 |

### Cap. 5 — Comunicazione in rete
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Internet, stack a livelli, modello OSI/TCP-IP | Cap 9 | Parte IX | ✅ (NLD più ricco: OSI 7 livelli) |
| Livello applicativo (WWW, HTTP, FTP, DNS, posta) | Cap 9-10 | Parte VII/IX | ✅ |
| Livello trasporto (TCP, UDP, mux/demux) | Cap 9 (3) | Parte IX | ✅ |
| Livello rete (IPv4/IPv6, indirizzamento, NAT) | Cap 9 (3.3) | Parte IX | ✅ |
| **Instradamento/routing, ICMP** | — | Parte IX | 🟡 |
| **VLAN** | — | — | 🟡 |

### Cap. 6 — Algoritmi e strutture dati  ⚠️ AREA DI GAP PRINCIPALE
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Concetto di algoritmo, proprietà, flowchart | Cap 1 (7) | Parte VI Cap 1 | ✅ |
| **Analisi di complessità e notazione asintotica O, Ω, Θ** | — | — | 🔴 |
| **Algoritmi di ordinamento (insertion sort, merge sort, …)** | — | — | 🔴 |
| **Strutture dati astratte (lista, coda, pila, array, tabella hash, grafo, albero)** | — | — | 🔴 |
| **Strutture dati concrete** | — | — | 🔴 |

> Entrambi i volumi NLD trattano *il concetto* di algoritmo (e la logica
> booleana) ma **non** la complessità computazionale, gli algoritmi di
> ordinamento, né le strutture dati. È il **gap più ampio**.

### Cap. 7 — Ingegneria del software
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Ciclo di vita del software | Cap 3 (5.6) | Parte XIII | ✅ |
| Metodologie Agili (Scrum, XP, Lean, Kanban) | Cap 3 (6-9) | Parte XII | ✅ (NLD molto ricco) |
| Verifica e validazione, testing | Cap 3 / Cap 11 | Parte XIII Cap 2 | ✅ |
| Qualità del software, manutenzione | Cap 3 | Parte XI/XIII | ✅ |
| Linee Guida AgID | Cap 12 | Parte V | ✅ |
| **UML (use case, class, sequence, state chart, activity diagram)** | — | — | 🔴 |
| **Analisi e specifica dei requisiti** | — | Parte XIII (cenni) | 🟡 |
| **Design Patterns (architetturali e GoF)** | — | Parte XIII (MDD/DDD/Microservices) | 🟡 (manca il catalogo dei pattern GoF) |

### Cap. 8 — Strutture informative e database
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Modello relazionale, chiavi, integrità referenziale | Cap 8 | Parte VIII | ✅ |
| Progettazione (E-R, logica, fisica), normalizzazione | Cap 8 | Parte VIII | ✅ |
| SQL (DDL/DML/DCL), join, aggregazione | Cap 8 | Parte VIII Cap 4-5 | ✅ |
| Transazioni/ACID, indici, NoSQL | Cap 8 | Parte VIII Cap 7-8 | ✅ |
| **Operatori dell'algebra relazionale (formale)** | Cap 8 (cenni) | Parte VIII | 🟡 |
| **Architettura 3-tier; stack LAMP/WAMP/XAMPP** | — | Parte VII (cenni) | 🟡 |
| **Strumenti CASE per la progettazione** | — | — | 🟡 |

### Cap. 9 — Gestione dei Big Data
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Concetto di Big Data, le 5V | Cap 1 (9.7, cenni) | Parte XIII | 🟡 |
| Dati strutturati/semi/non strutturati, IoT e Big Data | Cap 1 / Cap 9 | Parte XIII | ✅ |
| NoSQL, MongoDB | Cap 8 (4.4) | Parte VIII | ✅ |
| **Ecosistema Apache Hadoop (moduli) e Apache Spark** | — | — | 🔴 |
| **Data Science e Data Analytics (pipeline, metodi)** | Cap 1 (cenni AI) | Parte XIII (sistemi conoscitivi, ML) | 🟡 |
| Big Data e GDPR | Cap 12 | Parte V | ✅ |

### Cap. 10 — Cybersecurity
| Tema competitor | NLD-Info | NLD-RIPAM | Verdetto |
|---|---|---|---|
| Minacce, malware, phishing, ingegneria sociale | Cap 11 | Parte X | ✅ |
| Network security (firewall, IDS, wireless, VPN) | Cap 11 | Parte IX/X | ✅ |
| Crittografia | Cap 11 (3.3) | Parte IX | ✅ |
| Gestione del rischio, controllo accessi, BC/DR | Cap 11/13/14 | Parte XIV | ✅ |
| Incident response, digital forensics | Cap 11 (5.2) | Parte X | ✅ |
| Standard ISO 27000/27001, governance (COBIT/ITIL/NIST) | Cap 13-16 | Parte XIV | ✅ (NLD molto ricco) |
| **Software security: buffer overflow, vulnerabilità di memoria** | — | — | 🔴 |
| **Sicurezza delle applicazioni web (OWASP), fuzzing** | Cap 11 (sicurezza web, generale) | Parte VII Cap 5 (online), Parte XIII Cap 2 | 🟡 |
| **Secure SDLC (ciclo di sviluppo sicuro), analisi del malware** | Cap 11 (cenni) | Parte XIII | 🟡 |

---

## PARTE II — Office automation
**Verdetto complessivo: ✅ interamente coperto (NLD superiore al competitor).**

| Cap. competitor | Copertura NLD |
|---|---|
| 1. Word | NLD-Info Cap 5 (più ampio: stili, mail merge, sommario, master, macro, accessibilità, PA) |
| 2. Excel | NLD-Info Cap 6 (più ampio: pivot, XLOOKUP/CERCA.X, CONTA.SE/SOMMA.SE, validazione, macro, PA) |
| 3. Presentazioni | NLD-Info Cap 7 (più ampio: schema diapositiva, animazioni, accessibilità, PA) |
| 4. Posta elettronica | NLD-Info Cap 10 (email, PEC, VoIP, sicurezza) |
| 5. Database (Access) | NLD-Info Cap 8 + NLD-RIPAM Parte VIII |

**Nessuna integrazione necessaria per la Parte II.**

---

## Elenco consolidato dei GAP (output per la redazione)

### 🔴 Mancanti (assenti in entrambi i volumi NLD) — priorità ALTA
1. **Algoritmi e strutture dati** — complessità asintotica (O, Ω, Θ); algoritmi
   di ordinamento (insertion sort, merge sort, ecc.); strutture dati astratte e
   concrete (liste, code, pile, array, tabelle hash, alberi, grafi).
2. **UML** — diagrammi use case, class, sequence, state chart, activity.
3. **Trasmissione dati (livello fisico/data-link)** — rilevazione e correzione
   errori (parità, CRC); tecniche di commutazione (circuito vs pacchetto);
   frame relay, ATM, ADSL.
4. **Sistemi operativi — riga di comando** — MS-DOS/CLI; **Linux**: shell BASH,
   permessi su file/directory, comandi principali, gestione utenti/sudo.
5. **Big Data — ecosistema** — Apache Hadoop (moduli) e Apache Spark.
6. **Software security** — buffer overflow e vulnerabilità di memoria.

### 🟡 Da approfondire (presenti ma più superficiali del competitor) — priorità MEDIA
7. **Fondamenti pratici di programmazione** — elementi del linguaggio e classi di
   istruzioni; primer con esempi (variabili, tipi, operatori, I/O) in
   Python/JavaScript; Assembly; programmazione strutturata.
8. **Design Patterns** (architetturali e GoF) + analisi/specifica dei requisiti.
9. **Architetture HW classiche** — linguaggio macchina/assembly; tassonomia di
   Flynn; classificazione classica dei sistemi (mainframe/mini/super/workstation).
10. **Reti — livello di rete** — instradamento/routing, ICMP, VLAN.
11. **Database — formalismi** — algebra/operatori relazionali; architettura
    3-tier; stack LAMP/WAMP/XAMPP; strumenti CASE.
12. **Big Data — Data Science/Analytics** (pipeline e metodi) + le 5V in dettaglio.
13. **Sicurezza applicativa** — OWASP/sicurezza web in profondità, fuzzing,
    secure SDLC, analisi del malware; SO: interrupt/eccezioni/concorrenza.

---

## Raccomandazioni per la Fase 2 (integrazioni)
- **Destinazione consigliata**: i gap tecnici avanzati (1, 2, 5, 6, 8, 12, 13)
  sono coerenti col volume **RIPAM** (taglio avanzato); i fondamenti (3, 4, 7, 9)
  con **NLD-Info** (taglio base). **Da confermare con la redazione.**
- **Priorità di redazione** (per impatto e ampiezza del gap):
  1) Algoritmi e strutture dati · 2) UML · 3) Trasmissione dati ed errori ·
  4) Linux/CLI · 5) Big Data (Hadoop/Spark) · 6) Software security.
- **Verifiche aperte**: confermare il contenuto dei capitoli RIPAM **online**
  (es. Parte VI Cap 4 "Sistemi operativi", Parte VII Cap 5 "Sicurezza app web")
  prima di classificare definitivamente i punti 4 e 13.
