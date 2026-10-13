# Come collegarsi ai gestionali dei distributori: guida e soluzione

_Data: 13 ottobre 2026 · Per: il founder e il cofondatore tecnico · Collegato a: [blueprint-assistente-riordino.md](blueprint-assistente-riordino.md)_

> **Il problema sollevato dall'ingegnere:** ogni distributore usa un gestionale diverso, spesso vecchio, installato sul proprio server ("on premise"), a volte personalizzato o fatto in casa, e molti **non offrono API** né chiavi di accesso. Come colleghiamo il nostro assistente a tutti?
>
> **La risposta breve:** non si collega "a tutti" dal primo giorno. Si costruisce **un nucleo unico** con **adattatori diversi** per ogni tipo di gestionale. Si parte dal modo più semplice che funziona (file e fatture elettroniche) e si sale di livello solo dove serve. Il caso "senza API" è normale, ed è risolvibile.

---

## 1. Capire il mondo dei gestionali in 5 minuti

### Cosa c'è dentro un gestionale di distribuzione
| Dato | Esempio | Ci serve per |
|---|---|---|
| **Anagrafica clienti** | Bar Centrale, P. IVA, indirizzo, rappresentante, giorno di visita | Sapere chi scrive e chi è il suo rappresentante |
| **Anagrafica articoli** (catalogo) | Codice, descrizione, formato, unità di vendita (cassa da 24) | Capire "2 casse di Peroni 33" |
| **Listini** | Prezzi per cliente o per gruppo, sconti | Proporre e confermare i prezzi giusti |
| **Giacenze** (magazzino) | Quantità disponibili | Dire "è finita, ti va la 66?" |
| **Documenti**: ordini, DDT, fatture | Lo storico di cosa ha comprato ogni cliente | "Il solito", suggerimenti, promemoria |

### I tipi di gestionale che troveremo
| Tipo | Esempi | Come si comportano |
|---|---|---|
| **Cloud moderni** | Fatture in Cloud (oggi di TeamSystem, con API pubbliche documentate), alcune soluzioni TeamSystem e Zucchetti in cloud | Hanno **API**: il caso facile |
| **Grandi gestionali installati** | Linee TeamSystem (es. Lynfa, Alyante), Zucchetti (es. Ad Hoc Revolution), Passepartout (Mexal, Passcom), SAP Business One, Microsoft Dynamics | Spesso **API o web service solo tramite partner** o moduli a pagamento; la documentazione non è sempre pubblica. Il database sotto è quasi sempre accessibile (SQL Server o simili) |
| **Gestionali per piccole imprese** | Danea Easyfatt e simili | Pochi o nessuna API; **import ed export di file** (es. ordini da XML) spesso manuali |
| **Verticali per la distribuzione** | Software di piccole software house italiane per grossisti di bevande e food, spesso con app per i rappresentanti | Molto vari; la chiave è **la software house** che li segue |
| **Fatti in casa** | Database Access, Excel evoluti, programmi su misura | Nessuna API: si lavora con file o con il database |

> **Regola pratica:** quasi ogni gestionale, anche il più vecchio, sa fare almeno una di queste due cose: **esportare dati in un file** (CSV, Excel, XML) e **salvare tutto in un database**. È da lì che si parte.

---

## 2. I 6 modi per collegarsi a un gestionale

| # | Metodo | Come funziona | Pro | Contro | Quando usarlo |
|---|---|---|---|---|---|
| **1** | **API ufficiali** (REST o web service) | Il gestionale espone delle "porte" documentate; si accede con una chiave | Pulito, sicuro, supportato | Spesso non c'è, è a pagamento o passa da un partner certificato | Gestionali cloud e moderni |
| **2** | **Scambio di file** | Il gestionale esporta catalogo, clienti e storico in file (CSV, Excel, XML) in una cartella o via FTP; noi produciamo l'ordine in un formato che il gestionale sa importare | Funziona quasi ovunque, nessuna modifica al gestionale | Non in tempo reale (es. ogni ora o ogni notte); l'import a volte va lanciato a mano | **Il punto di partenza standard** |
| **3** | **Lettura diretta del database** | Un piccolo programma installato sul server del distributore legge (e in casi selezionati scrive) le tabelle del database (es. SQL Server via ODBC) | Dati quasi in tempo reale, senza bisogno di API | Bisogna capire la struttura delle tabelle; aggiornamenti del gestionale possono cambiarla; **scrivere** nel database è rischioso e può invalidare l'assistenza | Gestionali installati senza API, per **leggere** |
| **4** | **Fatture elettroniche e DDT** (formato FatturaPA) | Lo storico degli acquisti si ricava dai file XML delle fatture emesse, che **ogni distributore italiano ha per legge**; contengono righe con codice articolo, descrizione, quantità e prezzo | **Standard nazionale identico per tutti**, indipendente dal gestionale | Solo storico (non catalogo completo, non giacenze); arriva dopo la consegna | **Per lo storico e i suggerimenti**, da subito |
| **5** | **Partner e software house** | Il rivenditore o la software house del gestionale (chi lo installa e lo personalizza per il distributore) costruisce o abilita il collegamento | Hanno accesso, competenze e la fiducia del cliente | Costo e tempi; dipendenza da terzi | Gestionali chiusi e verticali; **canale di vendita** |
| **6** | **Automazione dell'interfaccia** (RPA) | Un "robot" usa il gestionale come farebbe una persona, cliccando e compilando | Funziona anche senza API, file o database | Fragile: si rompe se cambia una schermata | **Ultima spiaggia** |

### E la "via zero": nessuna integrazione
Per il primo pilota si può partire **senza collegamenti automatici**. Il distributore esporta una volta catalogo, clienti e listini in Excel; noi carichiamo i file. La bozza confermata arriva **all'ufficio ordini o al rappresentante** (WhatsApp, email, PDF, pagina web) e viene inserita nel gestionale come oggi. **Si misura il valore prima di investire nell'integrazione.**

---

## 3. La soluzione: un nucleo unico, tanti adattatori

```
                         ┌────────────────────────────────────────┐
  WhatsApp, vocali,      │          IL NOSTRO NUCLEO (cloud)        │
  foto dei locali  ───►  │  Assistente AI · bozze · suggerimenti    │
                         │  ───────────────────────────────────────  │
                         │  MODELLO DATI COMUNE ("canonico")         │
                         │  Clienti · Articoli · Listini · Giacenze  │
                         │  · Storico · Ordini                       │
                         └──────────────▲───────────────┬───────────┘
                                        │ dati          │ ordini confermati
             ┌──────────────┬───────────┼───────────┬───┴──────────┬──────────────┐
             │              │           │           │              │              │
       Adattatore     Adattatore   Adattatore   Adattatore    Adattatore    Adattatore
         API            FILE        DATABASE     FATTURE XML    PARTNER       MANUALE
      (gestionali     (CSV/XLS/    (connettore  (storico da    (software     (Excel una
       cloud)          XML via      locale sul   FatturaPA)     house)        tantum +
                       cartella     server del                                ufficio
                       o FTP)       distributore)                             ordini)
```

### I tre principi
1. **Un solo modello dati interno.** L'assistente ragiona sempre su "Cliente", "Articolo", "Listino", "Ordine", con gli stessi campi. Ogni gestionale viene **tradotto** in questo modello da un adattatore. Aggiungere un nuovo gestionale significa scrivere un nuovo adattatore, non rifare il prodotto.
2. **Leggere molto, scrivere poco.** Leggere dati (catalogo, storico) è sicuro. **Scrivere** gli ordini nel gestionale è delicato: all'inizio l'ordine si consegna come file da importare o come bozza da confermare, e solo dopo si passa alla scrittura automatica, con partner o API ufficiali.
3. **Il connettore locale "chiama fuori".** Per i gestionali installati sul server del distributore si usa un piccolo programma (agente o connettore locale) che **esce verso il nostro cloud** su HTTPS, come fa un browser. Così **non serve aprire porte nel firewall** del distributore, che è spesso il blocco principale.

### Come si comporta il connettore locale
| Funzione | Dettaglio |
|---|---|
| Installazione | Un programma leggero su un PC o server del distributore, sempre acceso |
| Lettura | Legge database (in sola lettura) o la cartella dove il gestionale esporta i file |
| Sincronizzazione | Invia al cloud solo le **modifiche** (nuovi articoli, prezzi, documenti) ogni pochi minuti o ogni ora |
| Ordini | Riceve gli ordini confermati e li deposita come **file nel formato di import** del gestionale (o li scrive dove è sicuro farlo) |
| Sicurezza | Connessione cifrata in uscita, credenziali in sola lettura, nessun dato oltre il necessario |

---

## 4. Il trucco italiano: la fattura elettronica come fonte dello storico

In Italia ogni fattura tra imprese passa dal **Sistema di Interscambio** in un **formato XML unico (FatturaPA)**. Ogni distributore conserva le fatture **emesse** ai suoi clienti, e ogni gestionale le sa esportare. Ogni riga contiene, di norma:

| Campo della riga | Esempio |
|---|---|
| Codice articolo | PER33V24 |
| Descrizione | Birra Peroni 33 cl vetro cassa 24 |
| Quantità e unità | 2 casse |
| Prezzo unitario | 18,40 € |
| Cliente (dall'intestazione) | Bar Centrale, P. IVA |

**Cosa ci dà:** lo **storico completo degli acquisti** di ogni cliente, nello **stesso formato per tutti i distributori**, senza toccare il gestionale. È la base per "il solito", per i promemoria ("non ordini il prosecco da 5 settimane") e per i suggerimenti.

**Limiti:** non contiene il catalogo completo, né le giacenze, né i listini futuri, ed è "a posteriori". Va combinato con almeno un file di catalogo e listino.

> **Perché è un vantaggio competitivo:** i concorrenti esteri non partono da qui. Per noi è un **adattatore universale per lo storico**, valido per tutti i 3.400 distributori.

---

## 5. La strategia per livelli

| Livello | Cosa colleghiamo | Come | Tempo di avvio per distributore (stima) | Quando |
|---|---|---|---|---|
| **0. Manuale** | Catalogo, clienti, listini una tantum; ordini all'ufficio ordini | Excel + bozza via WhatsApp, email o PDF | Ore o pochi giorni | **Pilota** |
| **1. File + fatture** | Catalogo e listini aggiornati; storico dalle fatture XML; ordini come file da importare | Export programmato del gestionale + adattatore file + adattatore FatturaPA | Pochi giorni | Primi clienti |
| **2. Connettore locale** | Dati quasi in tempo reale (giacenze, nuovi articoli); deposito automatico degli ordini | Connettore sul server, lettura del database o della cartella di export | 1-3 settimane per il primo cliente di un gestionale, molto meno per i successivi | Quando un gestionale si ripete tra i clienti |
| **3. API e partner** | Integrazione completa, anche scrittura degli ordini, app del rappresentante | API ufficiali o accordo con la software house | Variabile | Gestionali più diffusi nel segmento |

**La regola d'oro:** si costruisce un adattatore "vero" (livello 2-3) **solo per i gestionali che si ripetono** tra i clienti. Il primo cliente con un certo gestionale paga il lavoro di scoperta; i successivi lo riusano.

---

## 6. I partner: il ponte verso i gestionali chiusi

Ogni gestionale installato ha intorno una rete di **rivenditori e software house** che lo installano, lo personalizzano e lo assistono presso i distributori. Spesso:
- hanno **accesso** al database e conoscono la struttura delle tabelle;
- sanno quali **moduli di import ed export** sono disponibili;
- sono gli unici di cui il distributore si fida per "toccare" il gestionale.

**Per noi possono essere:**
1. **Chi costruisce l'adattatore** per il loro gestionale (pagato una volta, poi riusato);
2. **Un canale di vendita**: propongono l'assistente ai loro clienti distributori e ricevono una percentuale. È lo stesso modello dei rivenditori di sistemi cassa che avevamo discusso.

---

## 7. Come scoprire, distributore per distributore, cosa c'è

Domande da fare al titolare o al suo referente informatico:
1. **Che gestionale usate?** Versione? È installato sul vostro server o in cloud?
2. **Chi vi segue il gestionale?** (software house, rivenditore, informatico interno)
3. Il gestionale **esporta** catalogo, clienti, listini e documenti in Excel, CSV o XML? Si può programmare l'export automatico?
4. Il gestionale **importa** ordini da file? In che formato?
5. I rappresentanti usano un'**app o un tablet** per gli ordini? Di quale fornitore?
6. Dove sono salvate le **fatture elettroniche emesse**? Si possono esportare in XML?
7. Esiste un **PC o server sempre acceso** dove installare un piccolo connettore?

| Risposte tipiche | Livello di partenza |
|---|---|
| Gestionale cloud con API | 3 |
| Installato, esporta file e importa ordini | 1, poi 2 |
| Installato, nessun import | 1 (lettura) + ordini all'ufficio |
| Fatto in casa o Excel | 0-1 |

---

## 8. Sicurezza, privacy e responsabilità

| Tema | Scelta |
|---|---|
| **Accesso in sola lettura** | Il connettore usa credenziali che possono solo leggere; la scrittura degli ordini avviene come file da importare o tramite canali ufficiali |
| **Dati minimi** | Si sincronizza solo ciò che serve all'assistente (niente contabilità, stipendi, ecc.) |
| **GDPR** | Il distributore è titolare dei dati; noi siamo responsabili del trattamento, con un contratto apposito (DPA) |
| **Assistenza del gestionale** | Nessuna modifica al database senza l'accordo della software house, per non far perdere l'assistenza al distributore |
| **Tracciabilità** | Registro di tutto ciò che viene letto e inviato |

---

## 9. Cosa significa per il prodotto e per il pitch

- **Non serve integrarsi con tutti per partire.** Il pilota si fa al livello 0, il primo cliente pagante al livello 1.
- **Il vantaggio competitivo cresce per somma:** ogni gestionale integrato diventa un adattatore riusabile. Dopo 10-20 distributori nella stessa area si coprono probabilmente i gestionali più diffusi del segmento (_da verificare sul campo_).
- **La fattura elettronica** dà lo storico a tutti, subito, nello stesso formato: è un argomento forte anche nel pitch.
- **Le software house** possono essere il miglior alleato: aprono la porta dei gestionali chiusi e portano clienti.

### Una frase per il pitch
> *"Ci colleghiamo a qualsiasi gestionale: dove ci sono API usiamo le API, dove non ci sono leggiamo i file o il database con un connettore sicuro, e lo storico lo prendiamo dalle fatture elettroniche, che in Italia hanno tutti nello stesso formato."*

---

## 10. Domande da approfondire con l'ingegnere

1. **Il modello dati comune:** quali campi minimi per cliente, articolo, listino, ordine?
2. **Il connettore locale:** in che linguaggio, come si aggiorna da remoto, come si gestiscono le credenziali in sola lettura?
3. **L'adattatore FatturaPA:** come leggere in modo robusto le righe (codici articolo mancanti, descrizioni diverse per lo stesso prodotto)?
4. **L'abbinamento dei prodotti:** come collegare "la Peroni piccola" al codice giusto usando catalogo, storico e dizionario colloquiale?
5. **Il formato di import ordini** dei gestionali dei primi distributori: va verificato caso per caso.
6. **MCP** (lo standard aperto per collegare un'AI a strumenti e dati): ha senso esporre gli adattatori anche come strumenti per l'assistente?

---

## Fonti

- [Tom's Hardware: collegare il gestionale a un LLM con TeamSystem, Zucchetti e Mexal](https://www.tomshw.it/aioperator/ai-nel-workflow-contabile-come-collegare-il-gestionale-a-un-llm-con-teamsystem-zucchetti-e-mexal)
- [DataUnchain: integrazioni ERP e gestionali italiani](https://dataunchain.com/it/integrazioni-erp/)
- [Logicalab: moduli di sincronizzazione tra gestionale ed e-commerce](http://www.logicalab.it/integrazione-gestionale-con-e-commerce-moduli-di-sincronizzazione/)
- [Web Elettronica: API custom per SAP, Zucchetti, Mexal](https://web-elettronica.it/servizi/integrazione-api-gestionali-sap-zucchetti-mexal/)
- [IFG: integrazione custom tra Shopify B2B e Zucchetti, TeamSystem, Danea](https://ifgecommerce.com/en/blogs/articoli-shopify/integrazione-custom-api-shopify-gestionale)
- [ApiCenter: integrazione TeamSystem e Zucchetti](https://apicenter.io/integrations/teamsystem/zucchetti/)
- [Prestalia: configurazione dell'export ordini verso Danea](https://help.prestalia.it/en/documentation/export-orders-prestashop-danea/configuration-3/)
- [Micronaet: script di import ordini da CSV Mexal (esempio di codice)](https://bazaar.launchpad.net/~anna-g/micronaet/anna/revision/721/mexal_order_statistic/etl/import_order.py)
- [Order Sender: CRM e integrazione con i gestionali](https://www.ordersender.com/?p=6685)
- [Fiscozen: cos'è lo SDI e come funziona](https://www.fiscozen.it/guide/significato-sdi/)
- [Keliweb: API per scaricare i file originali SDI](https://fatture.keliweb.it/docs/4.0/methods/downloadOriginalSDI)
- [Chift: le migliori piattaforme di unified API](https://www.chift.eu/blog/best-unified-api-platforms)
- [Apideck: stato dell'accounting tech europeo nel 2026](https://www.apideck.com/resources/state-of-european-accounting-tech-2026)

_Nota: la disponibilità di API, web service e funzioni di import/export cambia da gestionale a gestionale e da versione a versione; molte informazioni vengono da fornitori di integrazioni e vanno verificate con le software house. I tempi di avvio sono stime da confermare con l'ingegnere._
