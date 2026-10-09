# Analisi critica: software gestionale per le Comunità Energetiche Rinnovabili (CER)

_Data: 9 ottobre 2026 · Obiettivo: dare una forma precisa all'idea, smontarla e vedere cosa resta in piedi._

**L'idea proposta:** software "chiavi in mano" per gestire le CER: onboarding dei membri, trasparenza sui dati energetici, calcolo e ripartizione degli incentivi GSE tra condomini, PMI e comuni.

---

## 0. In una pagina

- **Il problema esiste**, ma **non è quello descritto.** La parte "difficile da calcolare" (l'energia condivisa e l'incentivo) **la calcola già il GSE**, che paga il referente. Il dolore vero è **amministrativo**: pagamenti del GSE che arrivano dopo più di un anno, dati poco leggibili, PEC, aggiornamento delle configurazioni, fiscalità, soci che entrano ed escono, assemblee.
- **Il mercato è piccolo per costruzione.** Una CER media ha **~10 membri e ~85 kW** e incassa circa **6-8.000 € l'anno** di incentivi. Per tutti i costi di gestione (consulenza compresa) può spendere realisticamente **500-1.000 € l'anno**. Con ~4.800 CER, **l'intero mercato del software vale pochi milioni di euro l'anno.**
- **È già affollato**, e le grandi utility **regalano** la gestione per vendere energia e impianti: Plenitude, Iren, A2A, Enel X, più almeno 7 piattaforme specializzate e uno strumento pubblico gratuito di ENEA.
- **Ha una scadenza.** Le nuove CER possono accedere all'incentivo **entro il 31/12/2027** (o al raggiungimento dei 5 GW). La proroga al 2030 è stata chiesta ma **non è approvata**.
- **Verdetto: 🔴 nella forma proposta.** 🟡 solo in una forma diversa: **"back office in outsourcing" per chi gestisce molte CER**, oppure come porta d'ingresso verso servizi a più valore (sez. 5). Secondo me è più debole della "Permitting Intelligence" che abbiamo scartato.

---

## 1. Dare forma all'idea: come funziona una CER e dove sono i soldi

### Il meccanismo
```
 Impianti FV (≤1 MW ciascuno)          Consumatori (case, PMI, comune)
          │  immettono energia                    │  prelevano energia
          ▼                                        ▼
        ┌──────────────── Rete pubblica (stessa cabina primaria) ───────────────┐
        │  "Energia condivisa" = minimo tra immessa e consumata, ora per ora    │
        └──────────────────────────────┬────────────────────────────────────────┘
                                       ▼
          GSE: calcola l'energia condivisa con i dati dei contatori
          e paga al REFERENTE della CER:
            • tariffa premio: 60-120 €/MWh per 20 anni
            • restituzione delle componenti tariffarie ARERA (~8-9 €/MWh)
                                       ▼
          Il REFERENTE ripartisce tra i membri secondo il regolamento interno
          (con un'eventuale trattenuta per i costi, es. 15%)
```

### Dimensioni reali del mercato (dati GSE 2026)
| Dato | Valore |
|---|---|
| Configurazioni in esercizio (30/6/2026) | **3.630**, 302,9 MW, 37.821 clienti |
| Con contratto attivo o in finalizzazione (31/8/2026) | **>4.800**, ~400 MW, >51.000 punti di connessione |
| Crescita | Da 1.805 (fine 2025) a 3.630 (metà 2026): **raddoppiate in 6 mesi** |
| CER media | **~10 membri, ~85 kW** |
| Obiettivo PNRR | 1.730 MW: siamo a meno di un quarto |
| Contingente dell'incentivo | 5 GW: siamo all'**~8%** |
| Scadenza per accedere | **31/12/2027** (proroga al 2030 richiesta, non approvata) |
| Fondo perduto PNRR (40%) | **Chiuso** alle nuove domande; fine lavori spostata al 31/12/2027 |

### Quanto incassa una CER tipica (stima)
| Voce | Calcolo | Valore |
|---|---|---|
| Produzione annua | 85 kW × ~1.300 h | ~110 MWh |
| Energia condivisa | ipotesi 50-70% | ~55-75 MWh |
| Incentivo + restituzione ARERA | × ~100-120 €/MWh | **~6.000-9.000 €/anno** |
| Budget per tutta la gestione | trattenuta del 10-15% | **~600-1.300 €/anno** |
| ...di cui disponibile per il software | | **~200-600 €/anno** (ipotesi) |

### Dimensione del mercato del software
| Scenario | CER | × €/anno | Mercato annuo |
|---|---|---|---|
| Oggi | ~4.800 | 400 € | **~2 M€** |
| Fine 2027, se la crescita continua | ~10-12.000 | 400 € | **~4-5 M€** |
| Teorico, con i 5 GW pieni (improbabile entro il 2027) | ~60.000 | 400 € | ~24 M€ |

> **Il punto chiave:** anche nello scenario più ottimistico è un mercato piccolo, frammentato in migliaia di clienti minuscoli, ognuno con poche centinaia di euro da spendere. Per vincere bisognerebbe conquistarne una quota enorme.

---

## 2. Smontare l'idea: le obiezioni più forti

| # | Obiezione | Evidenza | Gravità | Si può rispondere? |
|---|---|---|---|---|
| 1 | **Il "calcolo difficile" lo fa già il GSE** | Il GSE calcola l'energia condivisa con i dati dei contatori e paga il referente. La ripartizione interna segue un regolamento: per una CER di 10 membri basta un foglio Excel | 🔴 Alta | Solo in parte: il valore non sta nel calcolo ma nella **gestione amministrativa** (sez. 3) |
| 2 | **Clienti minuscoli** | CER media di ~10 membri e ~7.000 €/anno di incentivi. Costo di acquisizione di ogni cliente alto rispetto a quanto può pagare | 🔴 Alta | Sì, ma solo vendendo a **chi gestisce tante CER** (installatori, ESCo, diocesi, unioni di comuni), non alla singola CER |
| 3 | **Mercato affollato** | HexErgy, ROSE Energy Community (Maps Energy), Alpinvision, CER Italia, E-360 (CER Builder e CER Manager), MACS CER, Regalgrid (con Intesa Sanpaolo), ENEA (gratuito, per la progettazione) | 🔴 Alta | Difficile: le funzioni sono già standard |
| 4 | **Le utility regalano la gestione** | Plenitude, Iren e A2A offrono la CER "dalla costituzione alla gestione" per vendere energia e impianti. Il software per loro è un costo di marketing | 🔴 Alta | No: non si compete contro "gratis" su un prodotto standard |
| 5 | **Scadenza di accesso al 31/12/2027** | Dopo quella data niente nuove CER incentivate, salvo proroga | 🟠 Media-alta | **Doppia lettura:** le CER esistenti ricevono l'incentivo per **20 anni** e vanno gestite fino al 2047. Ma la crescita di nuovi clienti si fermerebbe |
| 6 | **Dipendenza dalle regole del GSE** | Portale, formati e regole operative cambiano; ritardi e dati poco leggibili | 🟠 Media | È anche il motivo per cui serve aiuto, ma rende il prodotto fragile |
| 7 | **Barriera bassa** | Nessun dato proprietario, nessun effetto rete forte: chiunque con un team di sviluppo può copiarlo | 🟠 Media | Si costruisce un vantaggio solo con **scala e relazioni**, non con la tecnologia |
| 8 | **Il founder non ha competenze tecniche** | Un software da costruire in un mercato a bassi margini | 🟠 Media | Più fattibile come **servizio** che come software |

**Conclusione dello smontaggio:** come "software gestionale chiavi in mano" venduto alle CER, **l'idea cade.** Il cliente è troppo piccolo, il prodotto è già standard, i giganti lo regalano e la parte più complessa la fa il GSE.

---

## 3. Dov'è il dolore vero

Le lamentele documentate delle CER (coordinamento delle CER del Lazio, presidenti di CER, associazioni) **non riguardano gli algoritmi** ma la burocrazia:

| Dolore | Fonte |
|---|---|
| **Bonifici del GSE dopo più di un anno**, con dati difficili da leggere che obbligano a ricostruzioni contabili per ripartire le somme | Presidenti di CER citati da QualEnergia |
| "Adempimenti ridicoli e ritardi cronici" | Presidente di una CER |
| Tempi incerti per aggiornare le configurazioni (soci che entrano ed escono) | Coordinamento CER Lazio |
| PEC, dati di potenza degli impianti, tempi di connessione | Coordinamento CER Lazio |
| **Fiscalità**: trattamento delle trattenute (risposta dell'Agenzia delle Entrate n. 22/2026), enti non commerciali, ripartizioni | Fiscal Focus, Ecnews |
| **Liquidità iniziale** (l'anticipo PNRR è stato portato dal 10% al 30% per questo motivo) | Rete Agevolazioni |
| Incertezza sulla scadenza del 2027 | Edilportale |

> **Chi soffre davvero è il referente o il promotore** (sindaco, parroco, presidente di un'associazione, amministratore di condominio). Spesso è un volontario che si ritrova a fare il **contabile, il fiscalista e lo sportello GSE** di una piccola comunità. Il suo problema non è "mi manca un software", ma "**non ho tempo né competenze per fare tutto questo**".

---

## 4. Forme alternative a confronto

| | **A. Software gestionale per singole CER** (forma proposta) | **B. Back office in outsourcing** ("il commercialista delle CER") | **C. Piattaforma white label per chi gestisce molte CER** | **D. CER come piattaforma di servizi** (flessibilità, efficienza, povertà energetica) |
|---|---|---|---|---|
| Cosa fa | Onboarding, dashboard, ripartizione | Si prende in carico tutta la burocrazia: pratiche GSE, aggiornamenti, ripartizione, fiscalità, comunicazione ai soci | Strumento per installatori, ESCo, diocesi e unioni di comuni che seguono decine o centinaia di CER | Usa la CER come canale per vendere altri servizi: batterie, flessibilità, efficienza, fondi per la povertà energetica |
| Chi paga | La singola CER | La CER (in percentuale sull'incentivo) | L'operatore che gestisce le CER | Membri, utility, enti pubblici |
| Ricavo per cliente | Molto basso | Basso-medio (10-15% dell'incentivo, ~1.000 €/anno) | Medio-alto | Potenzialmente alto, ma incerto |
| Concorrenza | 🔴 Altissima | 🟡 Media (commercialisti, consulenti locali, utility) | 🟠 Alta (ROSE / Maps Energy, Regalgrid) | 🟢 Bassa, perché il mercato non esiste ancora |
| Adatto a te | ❌ | ✅ **Sì**: è un servizio, si parte con processi + AI + un commercialista partner | ⚠️ Serve un team tecnico | ❌ Troppo speculativo |
| Scalabilità | Bassa | **Bassa-media**: azienda di servizi, non startup VC | Media | Alta, se si materializza |
| **Valutazione** | 🔴 | 🟡 **Piccola azienda redditizia, non una startup** | 🟡 | 🟡 Interessante ma prematura |

### Il calcolo della forma B (la più realistica)
- Ricavo: ~1.000 € per CER all'anno (10-15% dell'incentivo).
- **Per 500.000 € di fatturato servono 500 CER**, cioè il ~10% di tutte le CER italiane di oggi.
- Con un buon livello di automazione (AI per leggere i dati GSE, ripartire, generare documenti) una persona potrebbe seguirne forse 100-200.
- **Risultato:** un'attività di servizi sostenibile per 2-5 persone, con ricavi ricorrenti per 20 anni (la durata dell'incentivo). **Non una startup ad alta crescita.**

---

## 5. Ipotesi critiche (se false, l'idea muore anche nella forma B)

| # | Ipotesi | Perché potrebbe essere falsa |
|---|---|---|
| H1 | I referenti **pagherebbero il 10-15%** dell'incentivo per delegare tutto | Molti sono volontari che preferiscono arrangiarsi; le utility lo offrono gratis |
| H2 | **Proroga dell'accesso agli incentivi oltre il 2027** | Senza proroga, il numero di nuovi clienti si ferma tra un anno |
| H3 | La burocrazia si può **automatizzare** abbastanza da rendere il margine sostenibile | Se ogni CER richiede ore di lavoro manuale ogni mese, i conti non tornano |
| H4 | Esistono **aggregatori** (installatori, diocesi, unioni di comuni) che vogliono esternalizzare | Potrebbero preferire farlo in casa o affidarsi a un'utility |
| H5 | **Le utility non chiudono il mercato** | Se le grandi utility gestiscono la maggior parte delle nuove CER, lo spazio per gli indipendenti si riduce |

---

## 6. Prospettiva: cosa potrebbe cambiare le carte in tavola

- **Energy sharing europeo:** la riforma europea del mercato elettrico introduce un diritto alla condivisione dell'energia in tutti gli Stati membri. L'esperienza italiana sulle CER potrebbe diventare esportabile (_da verificare: tempi di recepimento e regole nei singoli paesi_).
- **Fondo Sociale per il Clima** (Piano Sociale per il Clima, 9,3 miliardi contro l'impatto dell'ETS2): le CER "solidali" potrebbero diventare uno strumento finanziato contro la povertà energetica.
- **CER e flessibilità:** aggregare piccoli impianti e batterie delle CER per i servizi di rete (il collegamento con l'idea di Demand Response). Interessante, ma richiede regole e competenze che oggi non ci sono.

Sono scenari, **non mercati esistenti**: non bastano a giustificare l'idea oggi.

---

## 7. Verdetto

| Domanda | Risposta |
|---|---|
| L'idea così com'è funziona? | **No.** Software standard per clienti minuscoli, in un mercato affollato dove i giganti lo regalano e il calcolo lo fa già il GSE |
| C'è qualcosa sotto? | **Sì, un'attività di servizi** (back office delle CER), concreta ma piccola |
| È una startup? | **No**, salvo che si materializzino gli scenari della sez. 6 |
| È adatta a te? | La forma B sì, perché è un servizio e non richiede di costruire tecnologia complessa. Ma non soddisfa il tuo obiettivo di **costruire una startup** |
| Giudizio | 🔴 **forma proposta** · 🟡 **forma B come piccola azienda** · nel complesso **più debole della "Permitting Intelligence"** |

---

## Fonti

- [Smart Building Italia: oltre 3.600 CER attive, nuova pagina GSE](https://www.smartbuildingitalia.it/news/energia-rinnovabili/comunita-energetiche-oltre-3-600-cer-attive-il-gse-lancia-una-nuova-pagina-con-dati-e-strumenti-di-monitoraggio/)
- [Sky TG24: CER in Italia, la Vetrina del GSE](https://tg24.sky.it/economia/2026/09/08/cer-italia-sito-gse)
- [LavoriPubblici: Vetrina CER GSE](https://www.lavoripubblici.it/news/vetrina-cer-gse-comunita-energetiche-38675)
- [Next EU: raddoppiate le comunità energetiche, sono 3.630](https://www.nexteu.it/raddoppiate-le-comunita-energetiche-in-italia-sono-3-630-di-davide-stasi/)
- [Salentolive24: CER raddoppiate, al Sud diffusione disomogenea](https://www.salentolive24.com/2026/07/27/comunita-energetiche-raddoppiate-al-sud-piu-diffusione-disomogenea/amp=1)
- [Osservatorio CER: numeri e scenari verso il 2026](https://www.osservatoriocer.it/comunita-energetiche-rinnovabili-2025-numeri-mappe-e-scenari-verso-il-2026/)
- [Osservatorio CER: migliori software per le CER nel 2026](https://www.osservatoriocer.it/migliori-software-comunita-energetiche-2026/)
- [Social Impact Agenda: oltre l'incentivo](https://www.socialimpactagenda.it/2026/02/25/oltre-lincentivo-rifondare-le-comunita-energetiche-come-infrastrutture-sociali-misurabili-e-finanziabili/)
- [MASE: regole operative CACER](https://www.mase.gov.it/portale/documents/d/guest/allegato-1-regole-operative-cacer-def-pdf)
- [Rete Agevolazioni: tariffa incentivante CER 2026-2027](https://www.reteagevolazioni.it/comunita-energetiche-rinnovabli-incentivi/)
- [Solare Industriale: incentivi CER fino a 120 €/MWh](https://www.solareindustriale.it/incentivi/incentivi-cer-energia-condivisa)
- [Strategie Amministrative: il decreto CACER, la tariffa incentivante](https://www.strategieamministrative.it/dettaglio-news/20246211217-il-decreto-cacer-in-breve-la-tariffa-incentivante/)
- [Edilportale: incentivi CER, chiesta la proroga al 2030](https://www.edilportale.com/news/2026/09/risparmio-energetico/incentivi-cer-chiesta-la-proroga-dell-accesso-al-2030_112061_27.html)
- [Mr. Kilowatt: fondo CER chiuso](https://www.mrkilowatt.it/news/aggiornamento-incentivi/incentivi-fotovoltaico-2026-torna-il-fondo-perduto-per-cer-e-autoconsumo/)
- [QualEnergia: le CER scontente chiedono spiegazioni al GSE](https://www.qualenergia.it/articoli/cer-scontente-chiedono-spiegazioni-gse/)
- [QualEnergia: dopo il GSE, le CER solidali puntano al MASE](https://www.qualenergia.it/articoli/dopo-gse-cer-solidali-puntano-mase/)
- [Fiscal Focus: trattenute degli incentivi GSE fuori campo IVA](https://www.fiscal-focus.it/news-24/ore-08-04-cer-e-incentivi-gse-trattenute-per-i-costi-di-gestione-senza-commercialita-e-fuori-campo-iva,3,181607)
- [Ecnews: ripartizione dei contributi GSE negli enti non commerciali](https://www.ecnews.it/fiscale/?p=18795)
- [QualEnergia: gli incentivi distribuiti ai membri non costituiscono utili](https://www.qualenergia.it/articoli/incentivi-distribuiti-cer-membri-non-costituiscono-utili/)
- [Reonic: CER per installatori, prezzi indicativi](https://reonic.com/it-it/blog/come-aderire-comunita-energetica-guida/)
- [E-360: software CER](https://www.e-360.it/software-cer/)
- [MACS CER](https://macscer.com/)
- [CER Italia: servizi](https://cer-italia.energy/servizi/)
- [AziendaBanca: Intesa Sanpaolo e Regalgrid per le CER](https://www.aziendabanca.it/notizie/banche/intesa-sanpaolo-regalgrid-cer)
- [Plenitude: comunità energetiche](https://eniplenitude.com/comunita-energetiche)
- [Iren: comunità energetiche](https://www.irenlucegas.it/casa/comunita-energetiche)
- [EconomyUp: i CVC delle utility puntano sulle piattaforme di trading energetico](https://www.economyup.it/fintech/comunita-energetiche-rinnovabili-i-cvc-delle-utility-puntano-sulle-piattaforme-di-trading-energetico/)
- [Infobuildenergia: CER di area vasta e Piano Sociale per il Clima](https://www.infobuildenergia.it/approfondimenti/comunita-energetica-di-area-vasta-vantaggi-per-i-piccoli-comuni/)

_Nota: le stime su incassi, budget e mercato sono calcoli indicativi basati su medie (~85 kW e ~10 membri per CER, 50-70% di energia condivisa). Le cifre ufficiali sul contingente dei 5 GW non erano disponibili._
