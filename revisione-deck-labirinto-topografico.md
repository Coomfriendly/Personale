# Revisione critica del deck "Il Labirinto Topografico"

_Documento analizzato: "Il Labirinto Topografico: Sbloccare la Transizione Energetica in Italia", Società Italiana Transizione Energetica, novembre 2024, 15 slide (generato con Gemini Notebook)._
_Revisione: 9 ottobre 2026, confrontata con [analisi-critica-aree-idonee.md](analisi-critica-aree-idonee.md)._

---

## 1. Cosa sostiene il deck

1. **Problema** (slide 2-4): 341 GW richiesti, 80 GW necessari al 2030, oltre 2.100 progetti bloccati. Il collo di bottiglia è lo scontro tra decarbonizzazione e tutela del paesaggio, gestito con **valutazioni ex post, soggettive e discrezionali**.
2. **Soluzioni esistenti insufficienti** (slide 5-10): agrivoltaico avanzato e Testo Unico FER/SUER aiutano, ma la normativa è "ipertrofica" e frammentata per regione.
3. **Tesi** (slide 11-12): gli sviluppatori progettano **"al buio"** perché i vincoli vengono scoperti solo in conferenza dei servizi.
4. **Soluzione** (slide 13-14): **intelligenza spaziale e mappatura predittiva**, cioè simulazione preventiva dei vincoli, automazione delle aree idonee e dei buffer, integrazione con SUER. Processo in tre passi: scouting guidato dai dati, design conforme, autorizzazione "blindata".
5. **Promessa** (slide 15): "da anni a mesi". *"Non è un problema di energia, è un problema di geografia."*

---

## 2. Punti forti

| | |
|---|---|
| ✅ **Narrativa chiara** | Funnel 341 → 80 GW → 2.100 progetti, "Il punto cieco", "il territorio respinge": si capisce in 30 secondi |
| ✅ **Diagnosi corretta della discrezionalità** | La slide 3 coglie il vero nodo: le decisioni sono **incerte e discrezionali** |
| ✅ **Il "rovo" della slide 4** | Rende bene la complessità tra VIA, Soprintendenze, conferenza dei servizi ed enti locali |
| ✅ **Frammentazione regionale** | È un argomento vero e nel 2026 è ancora più forte (nuove leggi in Lombardia, Emilia-Romagna, Abruzzo, Umbria, Sicilia, Puglia) |
| ✅ **Doppio beneficio** (slide 15) | Sviluppatori **e** istituzioni: apre la strada alla forma GovTech |

---

## 3. Il problema strategico centrale: il deck si contraddice

> **Slide 3:** il blocco nasce da "valutazioni amministrative **incerte e discrezionali**".
> **Slide 15:** "È un problema di **geografia**. La nostra piattaforma offre **la mappa**."

**Le due cose non stanno insieme.** Se il vincolo è soggettivo e discrezionale, per definizione **non sta su una mappa**. Una mappa mostra i vincoli **oggettivi** (perimetri paesaggistici, aree protette, PAI idrogeologico), che:
- sono **già pubblici** (PAI del GSE, geoportali regionali come il SIT Puglia);
- sono **già mappati** da prodotti finanziati: **Glint Solar** (8 M$, in espansione in Italia) e i consulenti GIS;
- **non sono la causa principale dei blocchi.** Nel gennaio 2026 c'erano **81 progetti con VIA tecnica positiva e parere MiC negativo**, 160 in attesa della Presidenza del Consiglio, e il 69% dei progetti fermo per mancanza di istruttoria (Legambiente). Sono problemi di **capacità e discrezionalità della PA**, non di geografia.

**Cosa serve davvero per "prevedere il soggettivo":** la **memoria delle decisioni passate**, cioè come hanno deciso quella Soprintendenza, quella Commissione e quel TAR su progetti simili. È la forma **"Permitting Intelligence"** dell'analisi critica. Il deck ci va vicino (slide 14: "aree con alta probabilità di approvazione paesaggistica"), ma la attribuisce alla mappa invece che ai dati sulle decisioni.

**Suggerimento:** cambiare la frase finale in qualcosa come *"Non è un problema di geografia. È un problema di prevedibilità. Noi trasformiamo migliaia di decisioni pubbliche in probabilità."*

---

## 4. Errori, dati superati e affermazioni da verificare

| Slide | Affermazione | Problema | Gravità |
|---|---|---|---|
| 1 | Data **novembre 2024** | Quadro normativo superato: TAR Lazio 2025 sul decreto aree idonee, legge 4/2026 (aree idonee nel Testo Unico), RED III (d.lgs. 5/2026), leggi regionali 2026, DL Ambiente bis (ottobre 2026) | 🔴 |
| 2 | 341 GW / 5.930 richieste | Dato Terna superato: ~314 GW a luglio 2026, in calo | 🟡 |
| 2 | "Il mercato è pronto. Il capitale è pronto." | 341 GW contro 80 GW di fabbisogno significa che **gran parte delle richieste è speculativa** ("saturazione virtuale", decreto MASE dell'8/9/2026). Il mercato reale è molto più piccolo. Un investitore lo nota subito | 🟠 |
| 7 | Agrivoltaico avanzato: "piena eleggibilità (**D.M. 63/2024**)" | **Probabile errore.** Il 63/2024 è il **DL Agricoltura** (che limita il FV a terra in area agricola). Gli incentivi PNRR per l'agrivoltaico derivano dal **DM MASE 436/2023**. Da verificare | 🔴 |
| 7 | Nota a piè di pagina | **Testo senza senso** ("Il confronto diagnosti aoɪzmtato... scani a rigontibili matriz..."): è un artefatto della generazione AI. **Toglie molta credibilità** | 🔴 |
| 9 | Soglie del Testo Unico FER: attività libera < 5 MW, PAS 5-10 MW, AU > 10 MW; AU regionale < 300 MW, MASE > 300 MW | **Troppo semplificato.** Nel d.lgs. 190/2024 i regimi dipendono da **tecnologia, collocazione e tipo di intervento**, non solo dalla potenza, e sono stati modificati dai correttivi del 2025-2026. Da verificare sugli allegati del Testo Unico aggiornato | 🟠 |
| 10 | Emilia-Romagna: "limite del 10% di superficie occupata" | La **l.r. 5/2026** fissa un tetto dell'**1,5% della SAU regionale** | 🟠 |
| 10 | Puglia e Sicilia: "orientamento favorevole" | Nel 2026 la **Puglia** ha preso una **linea conservativa** (nuovo testo dell'8 ottobre 2026, tetti al suolo agricolo). La **Sicilia** ha approvato solo in parte la l.r. 21/2026 | 🟠 |
| 8, 13 | Integrazione con **SUER** "operativa dal 2024/2025"; "pre-compila i dati" | Non è chiaro se SUER esponga **interfacce (API)** a soggetti privati. Senza, l'integrazione è una promessa non verificata | 🟠 |
| 15 | "Da **anni a mesi**" | **Non dimostrato.** I tempi dipendono soprattutto dalla PA (istruttorie, MiC, Presidenza del Consiglio), che il software degli sviluppatori non controlla | 🔴 |
| 14 | "Autorizzazione **blindata** contro le contestazioni" | Promessa eccessiva e legalmente rischiosa: nessuno strumento può garantire l'esito di una valutazione discrezionale | 🟠 |
| 4, 12 | "Vincolo archeologico imprevisto", "vincoli invisibili" | Giusto, ma parte di questi vincoli **emerge solo con indagini sul campo** (es. archeologia preventiva), non da dati | 🟡 |

---

## 5. Cosa manca (per un investitore o un partner)

| Elemento | Stato nel deck |
|---|---|
| **Cliente preciso** (chi firma il contratto e quanto paga) | ❌ "Sviluppatori" e "istituzioni" in generale |
| **Modello di business** e prezzi | ❌ |
| **Dimensione del mercato** in euro | ❌ Ci sono solo GW, che non sono ricavi |
| **Concorrenza** (Glint Solar, PAI GSE, consulenti GIS, Paces come riferimento) | ❌ Totalmente assente: per un investitore è un campanello d'allarme |
| **Vantaggio difendibile** (perché non vi copiano) | ❌ |
| **Prova** (pilota, caso reale, dati su un progetto) | ❌ |
| **Team** | ❌ |
| **Perché adesso** | ⚠️ Implicito. Nel 2026 c'è un "perché adesso" fortissimo (leggi regionali nuove, sentenze) che il deck non usa perché è del 2024 |
| **Richiesta** (cosa chiedete: soldi, partner, pilota) | ❌ |

---

## 6. Come rimodellarlo (struttura proposta, 12 slide)

| # | Slide | Da dove |
|---|---|---|
| 1 | Titolo e frase chiave aggiornata ("problema di prevedibilità") | Nuovo |
| 2 | Il funnel, **con dati 2026** e il tasso reale di arrivo al RTB (~7%) | Slide 2 aggiornata |
| 3 | Il collo di bottiglia: **discrezionalità** (81 progetti con VIA positiva e MiC negativo) | Slide 3 + dati Legambiente 2026 |
| 4 | Il rovo autorizzativo | Slide 4 (ottima) |
| 5 | Frammentazione 2026: leggi regionali e sentenze | Slide 10 corretta |
| 6 | **Quanto costa l'incertezza**: un progetto autorizzato vale 72-166k €/MW; uno bocciato vale zero | Nuovo |
| 7 | **Soluzione**: mappa dei vincoli oggettivi (materia prima) + **memoria delle decisioni** (VIA, MiC, TAR) → probabilità e tempi | Slide 13 riscritta |
| 8 | Esempio concreto: un progetto o un portafoglio, prima e dopo | Nuovo |
| 9 | Clienti e modello: acquirenti di progetti, sviluppatori con pipeline, in prospettiva la PA | Slide 15 approfondita |
| 10 | Concorrenza e posizionamento (Glint = mappa; noi = decisioni) | Nuovo |
| 11 | Perché adesso e perché noi | Nuovo |
| 12 | Richiesta | Nuovo |

**Da eliminare o ridurre:** slide 5-7 (agrivoltaico, troppo spazio per un tema di contesto), slide 8-9 (normativa: basta una slide aggiornata), slide 11 (citazione: bella, ma è la quarta slide sullo stesso concetto).

---

## 7. Giudizio complessivo

| | Voto |
|---|---|
| Narrativa del problema | 8/10 |
| Accuratezza dei dati | 4/10 (superati al 2026, alcuni errori) |
| Solidità della soluzione | 4/10 (si contraddice con la propria diagnosi) |
| Completezza come pitch | 2/10 (mancano cliente, modello, concorrenza, team) |

**In sintesi:** il deck **racconta bene il problema** ma propone la **soluzione più debole e più affollata**, cioè la mappa. Inoltre usa dati del 2024 e contiene errori visibili, compreso il testo senza senso della slide 7. La sua stessa diagnosi (discrezionalità) porta naturalmente alla forma più forte: **prevedere le decisioni, non mappare il terreno.**

---

## Fonti usate per il confronto
- [Legambiente: Scacco Matto alle Rinnovabili 2026](https://www.legambiente.it/wp-content/uploads/2026/03/ScaccoMatto-alle-Rinnovabili-2026.pdf)
- [greenMe: Scacco matto alle rinnovabili (81 progetti con VIA positiva e MiC negativo)](https://www.greenme.it/?p=1367670)
- [QualEnergia: connessioni FER in calo](https://www.qualenergia.it/pro/articoli-pro/connessioni-fer-ancora-giu-domande-ready-to-build-11-gw/)
- [Advant Nctm: saturazione virtuale della rete](https://www.advant-nctm.com/news-e-approfondimenti/saturazione-virtuale-della-rete-il-nuovo-modello-delle-open-season-e-gli-impatti-sulle-operazioni-ma-nel-settore-delle-rinnovabili)
- [LavoriPubblici: aree idonee e legge 4/2026](https://www.lavoripubblici.it/news/aree-idonee-agrivoltaico-semplificazioni-legge-4-2026-testo-unico-fer-nota-anci-37461)
- [Infobuildenergia: sentenza del TAR sul decreto aree idonee](https://www.infobuildenergia.it/decreto-aree-idonee-sentenza-tar-regioni/)
- [BibLus: aree idonee in Emilia-Romagna (l.r. 5/2026)](https://biblus.acca.it/aree-idonee-emilia-romagna/)
- [BariToday: Puglia, linea conservativa](https://www.baritoday.it/economia/fonti-rinnovabili-in-puglia-priorita-tutela-paesaggio-agricolo.html)
- [TRM TV: aree idonee Puglia, nuovo testo (8/10/2026)](https://www.trmtv.it/attualita/2026_10_08/576835.html)
- [QualEnergia: Sicilia, approvata solo una parte del DDL](https://www.qualenergia.it/pro/articoli-pro/sicilia-aree-idonee-traguardo-resto-torna-commissione/)
- [pv magazine: prezzi dei progetti RTB 2026](https://www.pv-magazine.it/2026/04/13/progetti-rtb-nteaser-pv-tra-72-000-e-150-000-e-mwp-bess-tra-15-000-e-48-000-e-mw/)
- [TechCrunch: Glint Solar](https://techcrunch.com/2024/11/07/glint-solar-grabs-8m-to-help-accelerate-solar-energy-adoption-across-europe)
- [BibLus: Testo Unico Rinnovabili](https://biblus.acca.it/testo-unico-delle-rinnovabili/)

_Nota: i rilievi sulle slide 7 e 9 (DM 63/2024, soglie del Testo Unico) sono da confermare sui testi ufficiali._
