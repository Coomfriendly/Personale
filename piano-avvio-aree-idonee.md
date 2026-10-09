# Piano di avvio: software per aree idonee e autorizzazioni

_Data: 9 ottobre 2026 · Segue: [validazione-idee-energia.md](validazione-idee-energia.md)_

---

## 1. Partire senza competenze tecniche: si può, ma con un metodo

Molte startup B2B sono state fondate da chi **non** era esperto del settore. Ha funzionato perché il founder ha fatto tre cose:

1. **Ha parlato con i clienti più di chiunque altro.** Per questo non servono competenze: servono curiosità e costanza.
2. **Ha trovato in fretta cofondatori o partner** che avevano le competenze mancanti.
3. **Ha imparato le basi** quanto bastava per fare le domande giuste. Non per diventare un esperto.

### Il tuo ruolo: CEO / Business
| Fai tu | Lo delegano o lo fanno i cofondatori |
|---|---|
| Interviste ai clienti, vendita, partnership | Analisi GIS e dati territoriali |
| Capire il problema meglio di tutti | Interpretazione delle norme e delle sentenze |
| Raccolta fondi (bandi, investitori) | Costruzione del software |
| Coordinamento, prezzi, priorità | Firma tecnica dei report (se necessaria) |

### Il team che ti serve
| Ruolo | Profilo | Quando | Come (all'inizio) |
|---|---|---|---|
| **Esperto di dominio** ⭐ | Ingegnere ambientale, geologo, pianificatore territoriale o avvocato dell'energia, con 3+ anni in progetti FER | **Subito** (settimane 1-4) | Cofondatore con quote, oppure consulente pagato a report |
| **Tecnico GIS / dati** | Esperto di QGIS, PostGIS, Python, dati geografici | Mesi 1-3 | Cofondatore con quote, o freelance per il prototipo |
| **Sviluppatore software** | Full-stack (mappe web, backend) | Mesi 3-6 | Può coincidere con il profilo GIS |

> **Regola pratica:** l'esperto di dominio è il più importante. Senza di lui i report non sono credibili. Il software all'inizio si sostituisce con lavoro manuale e AI, l'esperto no.

### Dove trovare i cofondatori
- **LinkedIn:** cerca "ingegnere ambientale fotovoltaico", "geologo rinnovabili", "GIS analyst energia", "permitting rinnovabili". Molti lavorano da dipendenti negli sviluppatori o negli studi e vorrebbero mettersi in proprio.
- **Università:** Politecnici e corsi di ingegneria ambientale, pianificazione territoriale, geologia, master GIS. Neolaureati e dottorandi.
- **Eventi di settore:** fiera **KEY di Rimini** (marzo), eventi di **Italia Solare** ed **Elettricità Futura**, meetup GIS e open data.
- **Piattaforme di matching:** YC Co-Founder Matching, community di startup italiane, incubatori universitari.
- **Le tue interviste:** spesso il cofondatore giusto è una delle persone che intervisti.

### Come proporre la collaborazione
- **Fase di prova (1-2 mesi):** lavorate insieme sui primi report, pagati a prestazione o per ora.
- **Poi le quote:** se funziona, divisione delle quote con **vesting di 4 anni e cliff di 1 anno** (le quote si maturano nel tempo; chi lascia presto perde la parte non maturata).
- Mettilo per iscritto subito, anche in un semplice accordo tra fondatori.

---

## 2. Cosa imparare (30 giorni, circa 1 ora al giorno)

Non devi diventare un esperto. Devi **capire il linguaggio** dei tuoi clienti.

| Settimana | Argomento | Cosa sapere alla fine |
|---|---|---|
| 1 | **Come nasce un impianto FER** | Le fasi: scelta del sito → diritti sul terreno → richiesta di connessione a Terna o al distributore → autorizzazione → costruzione → esercizio. Chi sono gli sviluppatori e come guadagnano (vendita dei progetti autorizzati "ready to build", PPA) |
| 2 | **Regimi autorizzativi** | Testo Unico FER (d.lgs. 190/2024): **attività libera, PAS, Autorizzazione Unica**. Cosa sono **VIA e PAUR**. Cosa sono le **aree idonee** e le **zone di accelerazione** |
| 3 | **I vincoli** | Paesaggistici (Soprintendenza), idrogeologici (PAI), Rete Natura 2000, aree agricole e agrivoltaico, distanze. Cos'è la **PAI del GSE** e come si consulta |
| 4 | **La tua regione** | La legge regionale sulle aree idonee, le ultime sentenze TAR, quali sviluppatori sono attivi |

**Come studiare:**
- Leggi le guide di BibLus, Infobuildenergia e QualEnergia sul Testo Unico FER e sulle aree idonee.
- Leggi il rapporto Legambiente *Scacco matto alle rinnovabili 2026* per capire i blocchi.
- Apri la Piattaforma Aree Idonee del GSE e "gioca" con la mappa.
- Usa Claude come tutor: incolla una norma o una sentenza e chiedi "spiegamela come se fossi un principiante" e "quali conseguenze ha per uno sviluppatore".
- **La fonte migliore restano le interviste:** ogni sviluppatore ti insegnerà qualcosa.

---

## 3. Regione e tecnologia di partenza

| Opzione | Pro | Contro |
|---|---|---|
| **Puglia o Sicilia, FV a terra e agrivoltaico** ⭐ | Tanti progetti e tanti sviluppatori; molti contenziosi, quindi alto bisogno di chiarezza | Mercato più competitivo tra consulenti locali |
| **Lazio, agrivoltaico** | Molti progetti, sentenze TAR recenti (11395/2026) | |
| **Lombardia o Emilia-Romagna** | Leggi regionali nuove (2026), quindi tutti devono ricapire le regole | Meno progetti di grandi dimensioni |
| **Accumuli (BESS), in tutta Italia** | Boom di richieste (290 GW richiesti, solo ~10 GW autorizzati): grande bisogno | Più tecnico |

**Consiglio:** se non hai legami con un territorio, parti da **FV a terra e agrivoltaico in Puglia o Sicilia**, dove si concentra la domanda. Se vivi in una di queste regioni, o hai contatti lì, ancora meglio.

---

## 4. Script per le interviste (20-30 minuti)

**Obiettivo:** capire il problema, **non** vendere. Parla poco, ascolta molto, chiedi esempi concreti.

### Apertura (2 min)
> "Grazie del tempo. Sto studiando come gli sviluppatori di rinnovabili scelgono i siti e gestiscono le autorizzazioni, per capire dove si perde più tempo. Non ti vendo niente: mi interessa la tua esperienza. Posso prendere appunti?"

### Contesto (3 min)
1. Di cosa ti occupi e che tipo di progetti seguite (tecnologia, taglia, regioni)?
2. Quanti progetti avete in sviluppo in questo momento?

### Scelta dei siti (7 min)
3. Raccontami **l'ultima volta** che avete valutato un nuovo terreno. Come avete fatto, passo per passo?
4. Chi se ne occupa? Quanto tempo ci vuole? Quanto costa (persone, consulenti)?
5. Che strumenti usate? (GIS, PAI del GSE, consulenti, Excel...)
6. Vi è capitato di scoprire **tardi** un vincolo che ha bloccato un progetto? Cos'è successo e quanto vi è costato?

### Autorizzazioni (7 min)
7. Qual è la parte più lenta o frustrante dell'iter autorizzativo?
8. Come tenete traccia delle **nuove leggi regionali e delle sentenze**? Chi lo fa?
9. Quanti progetti avete fermi in autorizzazione? Da quanto tempo?
10. Se aveste **una bacchetta magica**, cosa cambiereste di questo processo?

### Soldi e soluzioni attuali (5 min)
11. Quanto spendete in un anno per consulenze tecniche, ambientali e legali sulle autorizzazioni?
12. Avete provato software o servizi per questo? Cosa non funzionava?
13. Se esistesse un report che in 24-48 ore vi dice se un terreno è idoneo, con quali vincoli, quale regime autorizzativo e quali rischi, vi sarebbe utile? Cosa dovrebbe contenere per fidarvi?

### Chiusura (2 min)
14. Posso ricontattarti quando avrò un primo prototipo? Ti andrebbe di **provare gratis** un report su un vostro terreno?
15. C'è qualcun altro con cui dovrei parlare?

**Dopo ogni intervista**, segna in un foglio: nome, azienda, tipo, dolore principale, spesa attuale, interesse per il report (sì/no) e chi ti ha suggerito di sentire.

---

## 5. Messaggi di contatto

### A. Sviluppatori e studi tecnici (LinkedIn o email)
> Ciao [Nome],
> sto studiando come gli sviluppatori di rinnovabili gestiscono scelta dei siti e autorizzazioni, soprattutto ora che con il Testo Unico FER e le nuove leggi regionali sulle aree idonee le regole cambiano di continuo.
>
> Non vendo nulla: sto parlando con chi lavora sul campo per capire dove si perde più tempo. Avresti 20 minuti per una chiamata la prossima settimana? In cambio condivido volentieri cosa sto imparando dalle altre interviste.
>
> Grazie,
> [Il tuo nome]

### B. Possibili cofondatori (esperto di dominio)
> Ciao [Nome],
> ho visto che lavori su [autorizzazioni / VIA / GIS] per progetti rinnovabili. Sto avviando un progetto per rendere molto più veloce la verifica di idoneità dei siti e l'iter autorizzativo, combinando dati pubblici (PAI GSE, vincoli), leggi regionali, sentenze e AI.
>
> Sto parlando con sviluppatori per validare il problema e cerco una persona esperta con cui costruirlo, prima come collaborazione e poi eventualmente come socio. Ti andrebbe un caffè o una call di 30 minuti per raccontarti l'idea e sentire la tua opinione?
>
> [Il tuo nome]

### C. Follow-up (dopo 5-7 giorni senza risposta)
> Ciao [Nome], ti riscrivo nel caso il messaggio si fosse perso. Bastano 15-20 minuti, quando ti è comodo. Grazie!

**Obiettivo:** 50 contatti → 10-15 risposte → 10-15 interviste.

---

## 6. Calendario delle prossime 6 settimane

| Settimana | Business (tu) | Team | Studio |
|---|---|---|---|
| **1** | Lista di 50 sviluppatori e studi; 20 messaggi | Lista di 15 possibili esperti di dominio; 5 messaggi | Fasi di un impianto FER |
| **2** | 30 messaggi + follow-up; prime 5 interviste | 2-3 chiamate con candidati | Regimi autorizzativi |
| **3** | Altre 5-10 interviste; sintesi dei risultati | Scegli l'esperto; accordo di prova | Vincoli e PAI GSE |
| **4** | Con l'esperto: 3-5 report gratuiti su siti reali | Cerca un profilo GIS | Legge regionale e sentenze |
| **5** | Consegna dei report, raccolta feedback, proposta di **pilota a pagamento** | | |
| **6** | **Decisione:** avanti, aggiusta o cambia (metriche nel report di validazione) | Accordo tra fondatori, se si procede | |

### Budget iniziale indicativo
| Voce | Costo |
|---|---|
| LinkedIn Premium / Sales Navigator (1-2 mesi) | ~100-200 € |
| Esperto di dominio pagato a report, per 3-5 report pilota | ~500-1.500 € (se non entra subito come socio) |
| Strumenti (QGIS è gratuito, dati pubblici, Claude) | ~20-50 €/mese |
| **Totale** | **~1.000-2.000 €** |

### Finanziamenti per dopo la validazione
- **Smart&Start Italia** (Invitalia): finanziamento agevolato per startup innovative (fino a 1,5 M€ nel 2026, da verificare).
- **Incubatori e acceleratori** specializzati in energia e climate tech.
- **Pre-seed** da business angel e fondi climate (Paces, REplace e Nyxium hanno raccolto da 2 a 11 milioni nella stessa nicchia).

---

## 7. Prossimo passo concreto

1. Dimmi la **regione** (la mia proposta: Puglia o Sicilia, FV e agrivoltaico).
2. Ti preparo la **lista dei primi sviluppatori e studi** da contattare in quella regione, cercando nelle fonti pubbliche.
3. Ti preparo un **report di esempio** (mockup) da mostrare nelle interviste e ai potenziali cofondatori.
