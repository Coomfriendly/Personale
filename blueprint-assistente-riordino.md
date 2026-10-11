# Blueprint dell'idea: assistente di riordino per distributori Horeca

_Data: 11 ottobre 2026 · Versione 1 · Segue: [concept-assistente-riordino-horeca.md](concept-assistente-riordino-horeca.md)_

> Questo documento dà una **struttura completa all'idea**: problema, cliente, prodotto, modello di business, numeri, vantaggi, rischi e decisioni aperte. Non è un piano operativo. Tutti i numeri sono **ipotesi da verificare**.

---

## 1. L'idea in tre righe

**Per** i distributori Horeca regionali che vendono tramite rappresentanti di zona,
**[nome provvisorio]** è un assistente su WhatsApp che **raccoglie i bisogni dei locali tra una visita e l'altra, consiglia cosa ordinare e prepara l'ordine** che il rappresentante conferma in pochi secondi.
**A differenza** delle app di raccolta ordini e di Choco, **non aspetta l'ordine: lo costruisce insieme al cliente durante la settimana, e aiuta il rappresentante a vendere meglio.**

### Nomi provvisori (solo per parlarne)
| Nome | Idea |
|---|---|
| **Bozza** | L'ordine che si costruisce da solo durante la settimana |
| **Riordina** | Diretto, si capisce subito |
| **Il Giro** | Il "giro" del rappresentante, linguaggio del settore |
| **Banco** | Dal bancone del bar |

---

## 2. Il problema, per ciascun attore

| Attore | Problema | Prova attuale | Da verificare |
|---|---|---|---|
| **Barista** | Si dimentica cosa serve quando arriva il rappresentante; durante la settimana i bisogni nascono e si perdono | Esperienza del founder | È comune tra altri baristi? |
| **Barista** | Il rappresentante non consiglia e non propone novità | Esperienza del founder | Idem |
| **Rappresentante** | Visite lunghe, clienti che "non ricordano", poco tempo per consigliare, richiamate dopo la visita | Ipotesi | Domande al rappresentante |
| **Distributore** | Vendite perse: il cliente compra altrove ciò che ha dimenticato, o non compra; promozioni dei produttori che non arrivano al bancone; nessun dato su cosa chiedono i clienti | Ipotesi | Domande al titolare |
| **Distributore** | Margini sotto pressione: traffico nei locali -0,8% nel 2025, rincari dei produttori | Dati Italgrob | — |

---

## 3. Il cliente iniziale (chi paga e chi usa)

### Chi paga: il profilo del distributore ideale
| Caratteristica | Profilo |
|---|---|
| Tipo | Distributore **multimarca** Horeca (bevande, a volte anche food) |
| Dimensione | **300-3.000 clienti attivi**, **2-15 rappresentanti** di zona |
| Area | Regionale o provinciale; **primo territorio: Calabria** |
| Come vende oggi | Soprattutto con il **rappresentante che passa** a giorni fissi; WhatsApp usato in modo informale |
| Struttura | Spesso azienda familiare, gestionale tradizionale |
| Esempio reale | Il distributore principale del bar del founder (Scaramozzino Srl, Maierato) |

### Chi usa
| Utente | Profilo |
|---|---|
| **Il locale** | Bar, caffetterie, pub, ristoranti, pizzerie. Titolare o responsabile acquisti. Usa WhatsApp ogni giorno |
| **Il rappresentante** | Riceve la bozza e le note prima della visita; conferma l'ordine |
| **Il titolare del distributore** | Vede risultati e dati: ordini assistiti, prodotti recuperati, promozioni accettate |

### Chi NON è il cliente iniziale (per ora)
- Grandi distributori nazionali e grandi marchi (Galbani, San Carlo, produttori di bevande): hanno già sistemi propri.
- Fornitori piccolissimi che lavorano solo su WhatsApp: ordini troppo piccoli.
- Venditori con il furgone ("tentata vendita"): vendono sul momento, non c'è un ordine da preparare.

---

## 4. La proposta di valore

| Per chi | "Lavoro" da svolgere | Cosa gli toglie | Cosa gli dà |
|---|---|---|---|
| **Barista** | Avere sempre la merce giusta senza perderci tempo | Dimenticanze, attese, conti a memoria | Un posto dove segnare tutto in un secondo (vocale, foto, testo), suggerimenti utili, conferme |
| **Rappresentante** | Fare più visite e vendere di più | Visite lunghe, clienti impreparati | Bozza pronta, note su cosa proporre, clienti che "si sono già fatti la lista" |
| **Distributore** | Vendere di più a ogni cliente e tenerlo | Vendite perse, rappresentanti poco efficaci, buio sui dati | **Ordine medio più alto**, più visite per rappresentante, dati sulla domanda, un canale per le promozioni |

**Il messaggio per il distributore, in una frase:**
> *"I tuoi clienti si dimenticano metà delle cose che vorrebbero comprare. Noi le raccogliamo per te durante la settimana."*

---

## 5. Il prodotto

### Il ciclo base (la "settimana tipo")
```
  ① RACCOGLIERE        ② SUGGERIRE           ③ PREPARARE           ④ CONFERMARE       ⑤ IMPARARE
  Il locale segna      L'assistente propone   Prima della visita,   Il rappresentante  Ogni ordine
  durante la           ciò che manca o        il rappresentante     rivede, consiglia, migliora i
  settimana            che conviene           riceve bozza e note   conferma           suggerimenti
  (testo, vocale,      (storico, stagione,                          → gestionale
  foto)                promozioni)
```

### Le funzioni, per fasi
| Funzione | Versione 1 (il minimo per provare il valore) | Versione 2 | Versione 3 |
|---|---|---|---|
| Raccolta dei bisogni su WhatsApp (testo, vocali) | ✅ | Foto di scaffali e liste scritte a mano | |
| Riconoscimento dei prodotti dal catalogo del distributore | ✅ (catalogo caricato) | Dizionario dei nomi colloquiali che impara | |
| Bozza d'ordine che cresce durante la settimana | ✅ | | |
| Invio della bozza al rappresentante prima della visita | ✅ | Note su cosa proporre | |
| Conferma del rappresentante con un tocco | ✅ (via WhatsApp o pagina web) | | |
| Promemoria al locale ("domani passa il rappresentante: vuoi aggiungere qualcosa?") | ✅ | | |
| Suggerimenti basati sullo storico del locale | | ✅ | Su locali simili, stagione, eventi, meteo |
| Promozioni del distributore e dei produttori | | ✅ | Campagne misurate per i produttori |
| Inserimento automatico nel gestionale | | ✅ (gestionali più diffusi) | |
| Ordini urgenti tra una visita e l'altra (consegna fuori giro) | | ✅ | |
| Cruscotto per il titolare | Report semplice | ✅ | Analisi della domanda |

### Cosa il prodotto NON fa (scelte deliberate)
- **Non sostituisce il rappresentante:** l'ordine resta suo.
- **Non gestisce pagamenti né consegne.**
- **Non è un chatbot generico:** risponde solo su ordini, prodotti e servizio del distributore. È anche un requisito: dal 15 gennaio 2026 WhatsApp **vieta gli assistenti AI generici** sulla sua piattaforma per le aziende, ma **consente quelli legati a un servizio specifico** come la conferma degli ordini.
- **Non è un'app da scaricare:** il locale usa WhatsApp, che ha già.

### Esempi di conversazione
**Il locale durante la settimana**
> 🧑 *(vocale)* "Segnami due casse di Peroni da 33 e l'acqua frizzante"
> 🤖 "Fatto: 2× Peroni 33 cl (cassa da 24), acqua frizzante 1 L (cassa da 12): quella che prendi di solito? Giovedì passa Marco."

**Il giorno prima della visita**
> 🤖 "Domani passa Marco. Nella tua lista ci sono 4 prodotti. L'ultima volta avevi preso anche il Crodino: lo aggiungo?"

**Al rappresentante, la mattina**
> 🤖 "Bar Centrale: bozza pronta (6 righe, circa 380 €). Ha chiesto della nuova birra artigianale. Non ordina il prosecco da 5 settimane."

---

## 6. I dati: cosa serve e cosa si accumula

| Dato | Da dove | Quando |
|---|---|---|
| Catalogo e codici articolo | Distributore (esportazione dal gestionale) | Dall'inizio |
| Clienti, rappresentante assegnato, giorni di visita | Distributore | Dall'inizio |
| Storico degli ordini per cliente | Distributore | Versione 1-2 |
| Listini per cliente, disponibilità | Gestionale del distributore | Versione 2 |
| Promozioni | Distributore e produttori | Versione 2 |
| **Linguaggio reale degli ordini** ("le verdi", "il solito") | **Le conversazioni stesse** | Si accumula nel tempo |

> **Il circolo virtuoso:** più ordini passano dall'assistente, meglio capisce il linguaggio dei baristi e meglio suggerisce. Questo è il vantaggio che si costruisce nel tempo.

---

## 7. Il modello di business

### Chi paga cosa
| Chi | Paga? | Come |
|---|---|---|
| **Distributore** | ✅ | **Canone mensile per cliente attivo** sull'assistente (il cliente che lo usa almeno una volta al mese) |
| Locale | ❌ Gratis | È ciò che lo convince a usarlo |
| Produttori (in futuro, ipotesi) | ✅ | Per campagne e promozioni consegnate e misurate |

### Logica del prezzo (ipotesi)
| Opzione | Esempio | Pro | Contro |
|---|---|---|---|
| **A. Per cliente attivo** | 2-4 € per locale attivo al mese | Cresce con l'uso, facile da capire | Ricavo basso per i distributori piccoli |
| B. Fisso per fasce | 300 € (fino a 300 clienti), 800 € (fino a 1.000), 1.500 € (oltre) | Prevedibile | Meno legato al valore |
| C. Percentuale sul valore aggiuntivo | 1-2% degli ordini "assistiti" | Legato al risultato | Difficile da misurare e da accettare |

**Scelta consigliata come ipotesi di lavoro:** **A + minimo mensile** (es. 3 € per cliente attivo, minimo 250 €/mese).

### Economia per un distributore tipo (ipotesi)
| Voce | Valore |
|---|---|
| Clienti del distributore | 800 |
| Clienti che usano l'assistente (adozione 40%) | 320 |
| Ricavo mensile (3 €/cliente attivo) | **~960 €/mese, ~11.500 €/anno** |
| **Valore per il distributore**: se l'ordine medio dei clienti attivi cresce del 4% | 320 clienti × ~1.200 €/mese di acquisti × 4% ≈ **15.000 €/mese di vendite in più** |
| Margine lordo del distributore su quelle vendite (ipotesi 15-20%) | **~2.300-3.000 €/mese**, cioè 2-3 volte il costo |

### Costi variabili (ordine di grandezza)
| Voce | Stima |
|---|---|
| WhatsApp Business: risposte entro 24 ore da un messaggio del cliente | **Gratuite** |
| WhatsApp: messaggi "di servizio" avviati dall'azienda (promemoria, bozze) | ~0,02-0,03 € a messaggio in Italia (_tariffe da verificare sul listino Meta_) |
| WhatsApp: messaggi promozionali | ~0,06-0,08 € a messaggio |
| Elaborazione AI (testo e trascrizione dei vocali) | Pochi centesimi per cliente al mese (_da stimare con il tuo amico ingegnere_) |
| **Costo variabile per cliente attivo** | **~0,30-0,80 €/mese** (ipotesi) |
| Margine lordo stimato | **~75-90%** |

> Il costo più pesante **non è variabile**: è l'**avvio** di ogni distributore (caricare il catalogo, collegare il gestionale, formare i rappresentanti). Va standardizzato il più possibile.

### Dimensione dell'opportunità
| Livello | Stima |
|---|---|
| Distributori Horeca in Italia | ~3.400 |
| Con rappresentanti di zona e il profilo giusto (ipotesi 40-50%) | ~1.400-1.700 |
| Ricavo medio annuo per distributore | ~8.000-20.000 € |
| **Mercato servibile in Italia** | **~11-34 M€/anno** |
| Per 1 M€ di ricavi annui | ~50-120 distributori |
| Estensioni | Altri grossisti (food, carni, ortofrutta, pulizia, caffè); produttori con rete di agenti; Spagna, Portogallo, Grecia |

---

## 8. Misurare se funziona

### La metrica principale
> **Valore degli ordini "assistiti" al mese**: gli ordini in cui almeno una riga è nata dall'assistente (segnata dal cliente o suggerita).

### Le metriche di supporto
| Metrica | Cosa dice |
|---|---|
| % di clienti che scrivono almeno una volta tra due visite | Se l'abitudine nasce |
| % di visite con bozza pronta | Se il ciclo funziona |
| Righe aggiunte grazie ai suggerimenti | Se i suggerimenti hanno valore |
| Ordine medio dei clienti attivi, prima e dopo | **Il ritorno per il distributore** |
| Durata media della visita | Il risparmio per il rappresentante |
| Errori di riconoscimento dei prodotti | L'affidabilità |
| Rappresentanti che lo usano davvero | Se il canale lo accetta |

---

## 9. Strategia di ingresso (logica, non piano operativo)

| Fase | Logica |
|---|---|
| **1. Un distributore, una zona** | Dimostrare il valore con dati reali in un territorio conosciuto (il tuo distributore, il tuo bar) |
| **2. Distributori vicini** | Nel settore tutti si conoscono: una referenza locale vale più di qualsiasi pubblicità |
| **3. Canali** | Associazioni di categoria (Italgrob), **software house dei gestionali** di distribuzione (integrazione e rivendita), consorzi di acquisto dei distributori |
| **4. Allargare** | Altri tipi di grossisti, altre regioni, poi altri paesi del Sud Europa |

**Perché partire dal Sud:** è dove il modello "rappresentante che passa" pesa di più e dove i grandi player (Choco, Salesforce) non arrivano.

---

## 10. Posizionamento e vantaggio difendibile

### Mappa del posizionamento
```
                         LAVORA CON IL CLIENTE (il locale)
                                    ▲
         Ristoply, Beak             │        ★ [nome provvisorio]
         (app del locale per        │        (assistente del cliente che
          inviare ordini)           │         prepara la visita e consiglia)
                                    │
 ASPETTA L'ORDINE ──────────────────┼────────────────── COSTRUISCE L'ORDINE
                                    │                   E CONSIGLIA
         Choco (raccoglie gli       │        Salesforce Agentforce,
          ordini che arrivano),     │        Mobisale (per grandi marchi
          app per rappresentanti    │         e reti di vendita)
                                    ▼
                         LAVORA PER IL DISTRIBUTORE
```

### Vantaggi che si costruiscono nel tempo
1. **Il linguaggio reale degli ordini Horeca in italiano** (e nei dialetti): ogni conversazione lo migliora.
2. **Lo storico della domanda** di migliaia di locali: permette suggerimenti migliori e, in futuro, dati utili ai produttori.
3. **Le integrazioni con i gestionali italiani** di distribuzione: lavoro noioso che i concorrenti esteri non fanno.
4. **Le relazioni nel canale**: distributori, rappresentanti, associazioni.

---

## 11. Rischi e risposte

| Rischio | Tipo | Risposta |
|---|---|---|
| I locali non prendono l'abitudine di scrivere | Adozione | Massima semplicità (vocale, "segna"), promemoria il giorno prima della visita, vantaggi concreti (promozioni, conferme) |
| I rappresentanti lo vivono come una minaccia | Canale | Presentarlo come il **loro** assistente; l'ordine resta loro, con la loro provvigione |
| Il distributore non vede ritorno | Valore | Misurare l'ordine medio prima e dopo su un gruppo di clienti |
| Errori nel riconoscimento dei prodotti | Tecnico | Conferma esplicita al cliente; il rappresentante rivede comunque la bozza |
| Integrazione con gestionali vecchi | Tecnico | Partire senza integrazione (esportazioni e bozza da ricopiare), poi integrare i più diffusi |
| **Regole di WhatsApp** | Piattaforma | Restare un assistente **specifico per gli ordini** (consentito); usare il canale ufficiale della WhatsApp Business API |
| **AI Act**: obbligo di trasparenza (chi parla con un'AI deve saperlo; regole applicabili da agosto 2026) | Normativo | Dichiararlo chiaramente nella prima conversazione |
| **GDPR**: dati dei clienti, vocali | Normativo | Il distributore è titolare dei dati, la startup è responsabile del trattamento; contratti e informative chiari |
| Choco o una software house fanno lo stesso | Concorrenza | Velocità, specializzazione sul modello "rappresentante + locale", relazioni territoriali |
| Dipendenza da pochi distributori all'inizio | Business | Crescere per referenze nella stessa area, poi con i canali |

---

## 12. Ipotesi da verificare prima di costruire

| # | Ipotesi | Peso | Chi può risponderti |
|---|---|---|---|
| **A1** | I baristi si dimenticano spesso cosa ordinare e non ricevono consigli | 🔴 | Tu, altri baristi |
| **A2** | I baristi **scriverebbero** all'assistente durante la settimana | 🔴 | **Tu**, provandolo su te stesso per 2-3 settimane |
| **A3** | Il distributore **perde vendite** abbastanza da pagare 250-1.500 €/mese | 🔴 | Titolare del distributore |
| A4 | I rappresentanti lo accettano | 🟠 | Il tuo rappresentante |
| A5 | Il distributore condivide catalogo, clienti e storico | 🟠 | Titolare |
| A6 | Ci sono molti distributori simili | 🟠 | Italgrob, i tuoi fornitori, elenchi provinciali |

---

## 13. Decisioni aperte (da prendere tu)

| Decisione | Opzioni | Considerazioni |
|---|---|---|
| **Nome** | Bozza, Riordina, Il Giro, Banco, altro | Meglio corto e in italiano, comprensibile da baristi e distributori |
| **Prezzo** | Per cliente attivo, a fasce, a percentuale | Ipotesi di lavoro: per cliente attivo con un minimo mensile |
| **Il primo distributore** | Scaramozzino o un altro | Serve un titolare aperto alle novità e con almeno 2-3 rappresentanti |
| **Ambito iniziale** | Solo bevande o anche food | Le bevande sono più semplici (catalogo stabile, ordini ripetitivi) |
| **Ruolo del tuo amico ingegnere** | Cofondatore o collaboratore | Qui la tecnologia è metà dell'azienda: meglio cofondatore |
| **Il tuo ruolo** | Prodotto e vendite, conoscenza del cliente | Il tuo vantaggio: parli la lingua di baristi e rappresentanti |

---

## 14. Per il tuo amico ingegnere (schema tecnico di alto livello)

```
 WhatsApp Business API (canale ufficiale)
        │  messaggi, vocali, foto
        ▼
 ┌──────────────────────── Servizio dell'assistente ────────────────────────┐
 │ 1. Trascrizione dei vocali (speech-to-text in italiano)                   │
 │ 2. Comprensione dell'ordine (LLM): prodotti, quantità, formati, "il solito"│
 │ 3. Abbinamento al catalogo (ricerca sui codici + dizionario colloquiale)   │
 │ 4. Bozza d'ordine per cliente e per visita                                │
 │ 5. Suggerimenti (storico, regole, promozioni)                             │
 │ 6. Livello di sicurezza: se non è sicuro, chiede o passa a una persona     │
 └───────────────────────────────────────────────────────────────────────────┘
        │                              │                         │
        ▼                              ▼                         ▼
 Rappresentante                 Gestionale del            Cruscotto del
 (bozza + note,                 distributore              distributore
  conferma)                     (prima esportazione,      (metriche)
                                poi integrazione)
```

**Domande tecniche da approfondire con lui:**
- Quanto è affidabile oggi la trascrizione dei vocali in italiano con dialetto e rumore di bar?
- Come abbinare in modo robusto "le verdi" o "quella del mese scorso" a un codice articolo?
- Quanto costa per cliente al mese l'elaborazione AI?
- Come si esportano catalogo e storico dai gestionali di distribuzione più diffusi?

---

## Fonti

- [Money.it: il fatturato Ho.Re.Ca. vale 107 miliardi (dati Italgrob)](https://www.money.it/il-fatturato-horeca-e-cresciuto-del-23-in-5-anni-oggi-vale-107-miliardi)
- [QdS: filiera Ho.Re.Ca. a 107,1 miliardi](https://qds.it/in-5-anni-fatturato-filiera-ho-re-ca-23-a-1071-mld/)
- [Beverfood: Italgrob contro gli aumenti di listino del beverage](https://www.beverfood.com/italgrob-contro-aumenti-listino-beverage/)
- [Choco: OrderAgent](https://choco.com/us/choco-ai)
- [Choco: pagina stampa (mercati)](https://choco.com/uk/press)
- [Salesforce: Consumer Goods](https://www.salesforce.com/in/consumer-goods/?bc=OTH)
- [Mobisale: funzionalità AI](https://mobisoft.co/ai-capabilities/?lang=en)
- [Ristoply](https://www.ristoply.com/)
- [Beak](https://www.b2beak.com/)
- [Whautomate: tariffe WhatsApp Business API in Italia](https://whautomate.com/whatsapp-business-api-pricing-italy)
- [YCloud: aggiornamento dei prezzi dei messaggi WhatsApp da luglio 2026](https://www.ycloud.com/blog/whatsapp-api-message-pricing-update-effective-july-1-2026)
- [Go4whatsup: prezzi WhatsApp Business API in Italia](https://go4whatsup.com/italy/whatsapp-business-api-pricing/)
- [Meta for Developers: WhatsApp Business Platform, prezzi per i fornitori AI](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing/ai-providers/)
- [TechCrunch: WhatsApp cambia i termini per vietare i chatbot generici](https://techcrunch.com/2025/10/18/whatssapp-changes-its-terms-to-bar-general-purpose-chatbots-from-its-platform)
- [Respond.io: la policy WhatsApp sui chatbot nel 2026](https://respond.io/blog/whatsapp-chatbot-policy-2026)
- [Respond.io: il divieto dei chatbot generici su WhatsApp](https://respond.io/blog/whatsapp-general-purpose-chatbots-ban)

_Nota: prezzi WhatsApp indicativi e in parte contraddittori tra le fonti; vanno verificati sul listino ufficiale Meta. Adozione, ordine medio, aumento delle vendite, margini e dimensione del mercato sono ipotesi. Gli obblighi di AI Act e GDPR sono riassunti in modo semplificato: per l'applicazione concreta serve un parere legale._
