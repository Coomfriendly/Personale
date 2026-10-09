# Analisi critica: software per aree idonee e autorizzazioni FER

_Data: 9 ottobre 2026 · Obiettivo: dare una forma precisa all'idea, smontarla e vedere cosa resta in piedi._

---

## 0. In una pagina

- **L'idea nella forma iniziale** ("report e software di idoneità del sito per gli sviluppatori") **è più debole di come l'avevo presentata.** Ha tre problemi seri:
  1. **Non tocca il vero collo di bottiglia.** I 150 GW sono fermi per la capacità della PA, i pareri del Ministero della Cultura e la politica, non perché agli sviluppatori mancano informazioni.
  2. **Il flusso di nuovi progetti si sta riducendo**: i nuovi progetti in VIA sono calati del 75% nel 2025 e le richieste di connessione sono in calo.
  3. **Lo strato "mappa + vincoli" si sta trasformando in una commodity**: c'è la PAI pubblica del GSE, i geoportali regionali sono gratuiti, e **Glint Solar** (Norvegia, 8 M$ di Series A, clienti come TotalEnergies, E.ON e Statkraft) **sta assumendo un team commerciale in Italia**.
- ⚠️ **Correzione rispetto al report precedente:** avevo scritto "nessun leader in Italia". Sullo strato di mappatura **un concorrente europeo ben finanziato sta entrando adesso.**
- **Cosa sopravvive:** il valore specificamente italiano non sta nella mappa. Sta nel **capire come decide la PA**: quali progetti vengono approvati o bocciati, da chi, perché e in quanto tempo. Le forme più solide sono due:
  - **B. Rischio autorizzativo per chi compra progetti** (investitori, utility, fondi);
  - **C. Strumenti per chi fa le istruttorie** (PA).
- **Verdetto: 🟡 da riformulare, non da abbandonare.** La forma da studiare è quella che chiamo **"Permitting Intelligence"** (sez. 4). Prima di investirci tempo va verificata con le ipotesi critiche della sez. 5.

---

## 1. Dare forma all'idea: dove sta il valore

### La vita di un progetto FER (fotovoltaico a terra / agrivoltaico)

```
 1. Scelta del sito ──► 2. Diritti sul terreno ──► 3. Connessione (STMG Terna/distributore)
          │                                                │
          ▼                                                ▼
 4. Progettazione + studi ──► 5. Autorizzazione (PAS / AU / VIA / PAUR) ──► 6. RTB ──► 7. Vendita o costruzione
     (SIA, relazioni)              ⏳ 18-30+ mesi, il collo di bottiglia        │
                                                                              ▼
                                                     Valore: 72.000-166.000 €/MWp (2026)
```

### I numeri che contano
| Dato | Valore | Cosa implica |
|---|---|---|
| Prezzo di un progetto **RTB** (autorizzato) | **72-166k €/MWp**, media ~123k nel 2º trimestre 2026 | Un progetto da 30 MW autorizzato vale **~2-5 M€**. L'autorizzazione è dove si crea il valore |
| Costo di costruzione | 0,7-1,2 M€/MW | |
| Spese legali e autorizzative | ~10-15k €/MW (dato di 2 anni fa) | Su 30 MW: 300-450k € di sviluppo. **La verifica iniziale del sito è una frazione minima** |
| Richieste di connessione FV | 3.531 richieste, ~140 GW | Pipeline enorme... |
| Progetti FV RTB | **224 progetti, ~10 GW** | ...ma solo il ~7% arriva al traguardo. **La scarsità di RTB tiene alti i prezzi** |
| Accumuli | 290 GW richiesti, ~10 GW autorizzati | Stesso schema, ancora più estremo |
| Pareri VIA della Commissione | 308 nei primi 8 mesi del 2026 (+40%) | La PA sta accelerando (anche perché arrivano meno progetti nuovi) |
| Nuovi progetti entrati in VIA nel 2025 | **-75%** rispetto al 2024 | **Il mercato greenfield si sta contraendo** |

**Il valore economico sta nel passaggio "da progetto in coda a progetto autorizzato".** Lì si passa da quasi zero a 100k+ €/MW. Qualunque prodotto deve aumentare la **probabilità** o la **velocità** di quel passaggio, oppure aiutare chi **compra** a capire quanto è probabile.

### Chi ha il dolore e quanto vale per lui
| Attore | Dolore | Vale per lui... |
|---|---|---|
| **Sviluppatore** (greenfield) | Scegliere siti che poi verranno bocciati; anni di attesa | Alto, ma la **verifica iniziale del sito costa poco** e la sa già fare (GIS interno o consulenti) |
| **Sviluppatore** (con progetti in coda) | Non sapere se e quando arriverà il titolo; integrazioni richieste dalla PA | Alto: ogni mese di ritardo costa (affitti dei terreni, opzioni, rischio di perdere la connessione) |
| **Acquirente di progetti** (utility, fondi, IPP: Iren, Enel, Met Group...) | Comprare progetti in coda senza sapere se arriveranno a RTB; due diligence lente | **Molto alto**: decidono il prezzo di un portafoglio in base alla probabilità di autorizzazione |
| **PA** (MASE, Commissione VIA, Regioni, Soprintendenze) | Montagne di pratiche, poco personale, contenziosi | Altissimo, ma **comprano lentamente e con gare** |
| **Comuni e territori** | Subiscono i progetti, poca capacità tecnica | Medio, budget minimo |

---

## 2. Smontare l'idea: le 9 obiezioni più forti

| # | Obiezione | Evidenza | Gravità | Si può rispondere? |
|---|---|---|---|---|
| 1 | **Non risolve il vero blocco.** I progetti sono fermi in Commissione, al MiC e alla Presidenza del Consiglio, non perché gli sviluppatori non conoscono i vincoli | Legambiente: 69% in attesa dell'istruttoria, 160 progetti in attesa della Presidenza del Consiglio, 88 del MiC, 81 con parere VIA positivo ma MiC negativo. Carenza cronica di personale | 🔴 Alta | Solo **in parte**: un prodotto per sviluppatori riduce le bocciature evitabili, ma non accorcia la coda. Per attaccare la coda bisogna lavorare **per la PA** (forma C) |
| 2 | **Il mercato dei nuovi siti si sta restringendo** | -75% di nuovi progetti in VIA nel 2025; connessioni FER in calo (da 326 a 314 GW); "saturazione virtuale" della rete e nuove regole (decreto MASE dell'8/9/2026) | 🔴 Alta | Sì, **spostando il focus**: dal greenfield ai progetti già in coda (gestirli, valutarli, comprarli) e agli accumuli |
| 3 | **La mappa dei vincoli diventa una commodity** | PAI del GSE gratuita; geoportali regionali (in Puglia il SIT con il piano paesaggistico PPTR) gratuiti; **Glint Solar** sta entrando in Italia | 🔴 Alta | Sì: **non competere sulla mappa.** Usarla come materia prima e competere su ciò che Glint non ha (decisioni della PA, sentenze, prassi locali) |
| 4 | **La verifica iniziale del sito vale poco** rispetto al progetto | Una pre-analisi GIS costa poche migliaia di euro, su sviluppi da centinaia di migliaia | 🟠 Media | In parte: vale molto **se evita una bocciatura** (anni persi). Ma lo sviluppatore deve crederci prima |
| 5 | **Gli sviluppatori sono pochi e si sovrappongono** | Molte Srl di progetto appartengono agli stessi gruppi; gli acquirenti sono poche decine | 🟠 Media | Mercato piccolo ma ricco: va bene per un'azienda redditizia, meno per una **startup da venture capital** solo in Italia |
| 6 | **Non scala all'estero** | Ogni paese ha regole, PA e giurisprudenza proprie. Paces lavora solo negli USA, Glint ha un livello GIS generico | 🟠 Media | Il vantaggio "regole locali" è un fossato in Italia ma un **limite di scala**. Possibile espansione verso paesi simili (Spagna, Grecia) con molto lavoro |
| 7 | **Le regole cambiano ogni mese** | TAR 2025, legge 4/2026, RED III, leggi regionali 2026, DL Ambiente bis (ottobre 2026), Corte costituzionale 144/2026 | 🟡 Doppia | È **sia il motivo d'esistere sia un costo enorme**: serve personale legale fisso per tenere aggiornato il prodotto. Se le regole si stabilizzano, il valore scende |
| 8 | **Responsabilità e fiducia** | Una valutazione sbagliata può costare milioni | 🟠 Media | Posizionarsi come **supporto decisionale**, non come parere legale; servono esperti con un nome nel settore |
| 9 | **Il founder non ha competenze di dominio né tecniche** | — | 🟠 Media | Questo è un mercato basato sulla fiducia e sull'esperienza: **senza un cofondatore senior di settore l'idea non regge**. Non è un dettaglio operativo, è parte della tesi |

**Conclusione dello smontaggio:** la forma "report e mappa di idoneità per sviluppatori" **cade** per le obiezioni 1, 2 e 3 messe insieme. Si rivolge al cliente sbagliato (chi il dolore ce l'ha, ma lo spende altrove), in un momento in cui il flusso cala, con un prodotto che sta diventando gratuito.

---

## 3. Tre forme alternative a confronto

| | **A. Site intelligence per sviluppatori** (forma originale) | **B. Rischio autorizzativo per acquirenti e sviluppatori** | **C. Strumenti per la PA** (GovTech) |
|---|---|---|---|
| Cosa fa | Trova i siti idonei e mostra i vincoli | Stima **probabilità e tempi** di autorizzazione di un progetto o di un portafoglio, sulla base dello storico delle decisioni | Aiuta la Commissione VIA, le Regioni e le Soprintendenze a fare le istruttorie più in fretta (verifica di completezza, controllo dei vincoli, bozze dei pareri) |
| Cliente | Sviluppatori | Utility, fondi, IPP che comprano progetti; sviluppatori con progetti in coda; banche che finanziano | MASE, Regioni, Province, Comuni |
| Attacca il vero blocco? | ❌ | ⚠️ Non lo riduce, ma **lo rende prezzabile** | ✅ **Sì, direttamente** |
| Disponibilità a pagare | Media-bassa | **Alta** (decisioni da milioni) | Alta in teoria, budget pubblici |
| Ciclo di vendita | Breve | Medio | **Molto lungo** (gare, MePA, politica) |
| Concorrenza | 🔴 Glint, PAI GSE, consulenti GIS | 🟢 Advisor tecnici e legali per le due diligence (manuali), nessun prodotto dati noto in Italia | 🟢 Grandi integratori IT della PA |
| Fossato | Basso | **Alto**: dataset strutturato delle decisioni VIA, MiC e TAR | Medio: relazione e integrazione con la PA |
| Adatto a un founder senza competenze | ❌ | ⚠️ Serve un cofondatore esperto, ma il prodotto è soprattutto **dati + analisi** | ❌ Serve conoscere bene la PA e il procurement |
| Rischio principale | Commodity | Le decisioni sono **troppo politiche per essere prevedibili** | Nessuno compra, oppure vince il grande integratore |
| **Valutazione** | 🔴 | 🟢 **La più solida** | 🟡 Interessante come seconda fase |

---

## 4. La forma che sopravvive: "Permitting Intelligence"

### L'intuizione
Ogni decisione autorizzativa in Italia lascia una **traccia pubblica**: pareri della Commissione VIA, pareri del MiC, decreti MASE, determine regionali (BURP), delibere del Consiglio dei ministri, sentenze TAR e del Consiglio di Stato. Sono **migliaia di documenti** su va.mite.gov.it, sui bollettini regionali e nella giustizia amministrativa. Oggi nessuno li legge in modo sistematico. Gli advisor ci arrivano a memoria e per esperienza.

**Con l'AI questi documenti diventano un dataset strutturato**: progetto, luogo, MW, tecnologia, vincoli, enti coinvolti, motivazioni, durata di ogni fase, esito, ricorsi.

### Cosa permette di dire
- "I progetti agrivoltaici **in questa zona e con queste caratteristiche** sono stati approvati nel **X%** dei casi; il motivo di bocciatura più frequente è **l'impatto cumulativo**."
- "Il tempo medio da presentazione a decreto per la VIA statale in Puglia è **N mesi**; questa Soprintendenza dà parere negativo nel **Y%** dei casi, ma la Presidenza del Consiglio lo supera nel **Z%**."
- "Questo **portafoglio di 12 progetti** ha un valore atteso di **€** dato il rischio di ogni progetto."
- "Il tuo progetto in coda è fermo da 14 mesi; i progetti simili hanno impiegato in media 11 mesi: **è in ritardo, ecco a che fase è e chi deve agire**."

### Per chi è
1. **Primo cliente: chi compra progetti in coda o RTB** (utility, fondi, IPP). Prezzano portafogli da decine di milioni con stime a occhio.
2. **Secondo: sviluppatori con molti progetti in coda**, per decidere su quali puntare, quali vendere e quali abbandonare.
3. **Terzo: banche e assicurazioni** che finanziano lo sviluppo.
4. **In prospettiva: la PA** (forma C), con lo stesso dataset rivolto a chi decide.

### Perché ha un fossato
- **Il dataset si accumula nel tempo** e diventa più prezioso ogni mese.
- **La complessità normativa italiana è un vantaggio** contro i concorrenti esteri: Glint mappa il terreno, questo prodotto capisce la PA.
- Usa la mappa GIS (PAI, geoportali) come **materia prima**, senza competere su di essa.

### Riferimento internazionale
Il prodotto principale di **Paces** (USA, Series A da 11 M$, Y Combinator) è proprio il **"Permitting Predictor"**: previsione del rischio autorizzativo a partire da dati su zonizzazione e permessi. **La tesi è già stata validata da investitori in un altro mercato.**

---

## 5. Smontare anche la nuova forma: le ipotesi critiche

Queste sono le ipotesi che, **se false, uccidono l'idea**. Vanno verificate prima di tutto il resto.

| # | Ipotesi | Perché potrebbe essere falsa | Come si capirebbe |
|---|---|---|---|
| H1 | **I documenti pubblici sono accessibili e utilizzabili in modo sistematico** | PDF scansionati, formati disomogenei, portali difficili da scaricare, eventuali limiti al riuso | Prendere 50 procedimenti pugliesi e provare a estrarne i dati |
| H2 | **Gli esiti sono abbastanza prevedibili** dai dati | Le decisioni potrebbero dipendere da fattori politici e personali che non stanno nei documenti | Su un campione storico: le variabili osservabili (zona, MW, vincoli, ente) spiegano gli esiti meglio del caso? |
| H3 | **Gli acquirenti di progetti pagherebbero** per questa informazione | Potrebbero fidarsi solo dei propri advisor, o ritenere di saperlo già | Conversazioni con 5-10 responsabili M&A o sviluppo di utility e fondi |
| H4 | **Il mercato è abbastanza grande** | Poche decine di acquirenti potrebbero non bastare per una startup | Contare gli acquirenti attivi e le transazioni annue di RTB in Italia |
| H5 | **Glint, Paces o un advisor grande non lo fanno prima** | Paces potrebbe arrivare in Europa; i grandi studi legali potrebbero costruire strumenti interni | Monitoraggio dei concorrenti; capire cosa offre Glint in Italia |
| H6 | **Il volume di decisioni resta alto** abbastanza a lungo | Se le riforme sbloccano tutto, o se il flusso crolla, il dataset perde valore | Trend dei pareri VIA e dei decreti nel 2026-2027 |

**Le più rischiose sono H2 e H3.** H1 è verificabile in fretta e senza nessuno, anche subito con l'AI su documenti pubblici.

---

## 6. Verdetto

| Domanda | Risposta |
|---|---|
| L'idea iniziale funziona? | **No, non così com'era.** Cliente sbagliato, flusso in calo, prodotto che diventa commodity |
| C'è qualcosa di valido sotto? | **Sì.** Il valore italiano sta nel prevedere e prezzare **le decisioni della PA**, non nella mappa |
| La forma migliore | **Permitting Intelligence** (forma B), con la forma C (PA) come evoluzione naturale |
| È una startup da venture capital? | **Forse.** Solo Italia: azienda di nicchia molto redditizia. Startup VC: solo se il modello si replica in altri paesi europei con PA complesse (Spagna, Grecia, Francia), da dimostrare |
| Va bene per te, senza competenze? | **Solo con un cofondatore esperto** di autorizzazioni FER. È parte della tesi, non un dettaglio |
| Giudizio complessivo | 🟡 **Promettente in forma B, da verificare su H1-H3 prima di innamorarsene** |

---

## 7. Domande aperte da approfondire insieme

1. **Quanto sono strutturati i documenti VIA e MiC?** Posso provare subito ad analizzare alcuni pareri pubblici per verificare H1.
2. **Quante transazioni di progetti FER ci sono in Italia ogni anno** e chi sono gli acquirenti? (H4)
3. **Cosa fa esattamente Glint in Italia** e cosa offrono gli advisor di due diligence? (H5)
4. **La forma C (PA) è davvero un mercato?** Esistono fondi PNRR o gare per digitalizzare le istruttorie VIA?
5. **Quali altri paesi europei** hanno lo stesso problema (PA lenta e giurisprudenza abbondante), per la scala?

---

## Fonti

- [pv magazine: progetti RTB, PV tra 72.000 e 150.000 €/MWp](https://www.pv-magazine.it/2026/04/13/progetti-rtb-nteaser-pv-tra-72-000-e-150-000-e-mwp-bess-tra-15-000-e-48-000-e-mw/)
- [Maysun Solar: notizie FV Italia, luglio 2026](https://www.maysunsolar.it/blog/notizie-fotovoltaico-italia-luglio-2026)
- [Maysun Solar: notizie FV Italia, agosto 2026](https://www.maysunsolar.it/blog/notizie-fotovoltaico-italia-agosto-2026)
- [TecnologiaPULITA: costo di un impianto da 1, 10 e 20 MW](https://tecnologiapulita.com/quanto-costa-impianto-fotovoltaico-1-10-20-mw/)
- [Energia Oltre: spese legali per il fotovoltaico, 15.000 €/MW](https://energiaoltre.it/esposito-cce-italia-spese-legali-per-fotovoltaico-15-000-e-mw-incentivi-non-servono/)
- [Legambiente: Scacco Matto alle Rinnovabili 2026](https://www.legambiente.it/wp-content/uploads/2026/03/ScaccoMatto-alle-Rinnovabili-2026.pdf)
- [greenMe: Scacco matto alle rinnovabili](https://www.greenme.it/?p=1367670)
- [ItaliaOggi: energie rinnovabili, pratiche a spron battuto](https://www.italiaoggi.it/settori/ambiente/energie-rinnovabili-pratiche-a-spron-battuto-mwzi50bn)
- [Il Sole 24 Ore: la Regione Siciliana certifica ritardi su 1.200 progetti](https://en.ilsole24ore.com/art/la-regione-siciliana-certifica-ritardi-1200-progetti-AEq2z18)
- [ANSA: 4mila progetti rinnovabili fermi (settembre 2026)](https://www.ansa.it/ansa2030/notizie/energia_energie/2026/09/20/elettricita-futura-4mila-progetti-rinnovabili-pronti-ma-fermi-per-burocrazia_8e11874b-e12b-41ce-b656-9479d752654b.html)
- [Energ Magazine: permitting e accumulo, solo 10 GW su 290](https://energmagazine.it/2026093025513/accumulo/case-study-accumulo/permitting-e-accumulo-solo-10-gw-su-290-gw-richiesti/)
- [QualEnergia: connessioni FER in calo](https://www.qualenergia.it/pro/articoli-pro/connessioni-fer-ancora-giu-domande-ready-to-build-11-gw/)
- [Advant Nctm: saturazione virtuale della rete e open season](https://www.advant-nctm.com/news-e-approfondimenti/saturazione-virtuale-della-rete-il-nuovo-modello-delle-open-season-e-gli-impatti-sulle-operazioni-ma-nel-settore-delle-rinnovabili)
- [TechCrunch: Glint Solar raccoglie 8 M$](https://techcrunch.com/2024/11/07/glint-solar-grabs-8m-to-help-accelerate-solar-energy-adoption-across-europe)
- [Jobgether: Glint Solar, Account Executive per il mercato italiano](https://jobgether.com/offer/6a50d7caac00a71a5a860963-account-executive---italian-market)
- [ESG Today: Paces raccoglie 11 M$](https://www.esgtoday.com/energy-infrastructure-software-startup-paces-raises-11-million-to-accelerate-green-energy-development/)
- [pv magazine USA: piattaforma GIS e dati da 11 M$](https://pv-magazine-usa.com/?p=13437)
- [MASE: portale Valutazioni Ambientali](https://va.mite.gov.it/it-IT/Oggetti/Info/8719)
- [QualEnergia: VIA al progetto record da 599 MWp (parere MiC negativo superato in area idonea)](https://www.qualenergia.it/articoli/fotovoltaico-via-progetto-record-599-mwp-puglia/)
- [Infobuildenergia: decreto aree idonee e sentenza del TAR](https://www.infobuildenergia.it/decreto-aree-idonee-sentenza-tar-regioni/)
- [QualEnergia: Piattaforma Aree Idonee del GSE](https://www.qualenergia.it/pro/articoli-pro/gse-lavora-piattaforma-digitale-aree-idonee/)

_Nota: prezzi RTB, costi e volumi vengono da operatori di mercato e stampa di settore. Le stime di mercato sono ipotesi. Questa analisi non è un parere legale o d'investimento._
