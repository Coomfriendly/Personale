# Concept: l'assistente di riordino tra una visita e l'altra del rappresentante

_Data: 11 ottobre 2026 · Evoluzione di: [analisi-critica-agente-ordini-fornitori.md](analisi-critica-agente-ordini-fornitori.md)_
_Basato sull'esperienza diretta del founder, titolare di un bar in provincia di Vibo Valentia._

---

## 1. Cosa ci dice la tua esperienza

### Come arrivano davvero gli ordini nel tuo bar
| Tipo di fornitore | Come ordini | Dimensione | Adatto a un agente? |
|---|---|---|---|
| **Distributore principale** (es. Scaramozzino Srl, Maierato) | **Rappresentante di zona** che passa | Ordini grandi e ricorrenti | ✅ **Sì: è il caso centrale** |
| Fornitori piccolissimi | **WhatsApp con il titolare** | Ordini piccoli | ❌ Troppo piccoli per pagare |
| Rappresentanti locali di grandi marchi (es. Galbani, San Carlo) | WhatsApp | Medi | ⚠️ I grandi marchi hanno già sistemi propri |
| Venditori con il furgone | Vendita al momento | Variabile | ❌ Non c'è un ordine da prendere |

### Cosa cambia rispetto all'analisi precedente
- **L'ipotesi H1 dell'analisi precedente, nel tuo caso, è in gran parte falsa:** gli ordini importanti **non** arrivano via WhatsApp, ma tramite il **rappresentante che passa**. WhatsApp lo usano soprattutto i fornitori piccoli, che non pagherebbero un agente.
- **Quindi copiare Choco** (raccogliere gli ordini che arrivano già via WhatsApp, vocali ed email) **qui non basta**: in zone come la tua il canale principale è la visita.
- **Ma sono emersi due problemi nuovi, più interessanti:**
  1. **Ti dimentichi cosa ordinare** proprio quando arriva il rappresentante.
  2. **Il rappresentante spesso non ti consiglia** e non ti vende bene.
- **E hai descritto tu la soluzione:** *"un chatbot che mi risponde sempre e si segna cosa vorrei prima che venga il rappresentante, così quando arriva mi conferma e basta."*

> **Il problema non è "prendere l'ordine". È tutto quello che succede tra una visita e l'altra**: i bisogni che nascono durante la settimana e si perdono, e i consigli che nessuno dà.

---

## 2. Il concept

### In una frase
> **Un assistente su WhatsApp, offerto dal distributore ai suoi clienti, che raccoglie i bisogni del locale tra una visita e l'altra, suggerisce cosa ordinare e prepara l'ordine che il rappresentante conferma in pochi secondi.**

### Come funziona nella settimana di un bar
```
 LUNEDÌ-GIOVEDÌ (tra una visita e l'altra)
   Barista ──► WhatsApp: "segna 2 casse di Peroni" · vocale · foto dello scaffale vuoto
                 │
                 ▼
   Assistente: "Segnato. Il weekend scorso hai finito l'acqua frizzante: la aggiungo?"
               "Questa settimana c'è la promo sull'aperitivo: ti interessa?"
                 │
                 ▼
   BOZZA D'ORDINE che cresce durante la settimana

 GIORNO DELLA VISITA
   Assistente ──► Rappresentante: "Bar X: bozza pronta (12 righe). Note: chiede info
                  sulla nuova birra artigianale. Non ordina il prosecco da 6 settimane."
   Rappresentante ──► rivede con il barista, consiglia, CONFERMA in pochi secondi
                 │
                 ▼
   Ordine nel gestionale del distributore → consegna

 DOPO
   Assistente ──► Barista: "Consegna prevista giovedì. Tutto ok con l'ultimo ordine?"
```

### Valore per ciascuno
| Attore | Problema di oggi | Cosa cambia |
|---|---|---|
| **Barista** | Si dimentica cosa serve; nessuno lo consiglia; deve aspettare il rappresentante | Segna i bisogni quando nascono, riceve suggerimenti utili, la visita dura meno |
| **Rappresentante** | Visite lunghe, clienti che non ricordano, poco tempo per consigliare | Arriva con la bozza pronta e i punti da proporre: **più clienti per giorno, ordini più ricchi**. L'assistente lo aiuta, non lo sostituisce |
| **Distributore** | Vendite perse (prodotti dimenticati, nessuna proposta), rappresentanti poco efficaci, nessun dato su cosa vogliono i clienti | **Ordini più grandi e completi**, rappresentanti più produttivi, dati sulla domanda, fidelizzazione dei clienti |
| **Produttori di bevande** (ipotesi) | Faticano a far arrivare le promozioni fino al bancone | Un canale diretto e misurabile per le promozioni, tramite il distributore |

### Chi paga
| Chi | Perché | Modello |
|---|---|---|
| **Il distributore** (pagante principale) | Più vendite per cliente e rappresentanti più produttivi: il ritorno si misura in euro | Abbonamento mensile in base al numero di clienti attivi |
| Il bar | Lo usa **gratis** (come Choco con i ristoranti) | — |
| Produttori di bevande (ipotesi futura) | Promozioni consegnate e misurate | Percentuale o canone sulle campagne |

---

## 3. Perché è diverso da quello che esiste

| Chi | Cosa fa | Differenza |
|---|---|---|
| **Choco** (OrderAgent) | Raccoglie ordini già inviati via WhatsApp, vocali ed email e li inserisce nel gestionale | Lavora sugli ordini **che arrivano già**. Non riempie il tempo **tra le visite** né consiglia. Non è in Italia |
| **Salesforce Agentforce** per i beni di consumo | Assistente per i rappresentanti e per i distributori, anche su WhatsApp | Pensato per **grandi marchi** con grandi budget, non per il distributore regionale |
| **Mobisale** (Genie) | Il rappresentante inoltra WhatsApp, vocali e foto; l'AI ricava gli articoli | Strumento per il rappresentante, non un assistente **per il cliente** |
| **GrubMarket, Dashmote** | AI per trovare nuovi clienti e preparare offerte | Si concentrano sull'acquisizione, non sul **riordino dei clienti esistenti** |
| App di raccolta ordini per rappresentanti (software house italiane) | Il rappresentante inserisce l'ordine sul tablet | Digitalizzano la visita, ma non quello che succede **prima** |

> **Lo spazio:** nessuno sembra combinare, per il **distributore regionale**, un assistente **per il cliente su WhatsApp** che **raccoglie i bisogni tra le visite**, **consiglia** e **prepara la visita del rappresentante**.

---

## 4. Smontare il concept

| # | Obiezione | Gravità | Risposta possibile |
|---|---|---|---|
| 1 | **I baristi lo userebbero davvero?** Serve un'abitudine nuova (scrivere quando manca qualcosa) | 🔴 Alta | Deve essere facilissimo: un vocale, una foto, "segna". E deve dare qualcosa in cambio (suggerimenti, promozioni, conferme). **Lo puoi verificare su te stesso per primo** |
| 2 | **Il rappresentante lo vede come una minaccia** (paura di essere sostituito o di perdere provvigioni) | 🔴 Alta | L'ordine resta suo: l'assistente **lavora per lui**, gli porta la bozza e i punti da proporre. Va presentato come uno strumento per vendere di più |
| 3 | **Il distributore paga?** Aziende familiari, spesso diffidenti verso la tecnologia | 🔴 Alta | Ritorno misurato su pochi clienti: valore medio dell'ordine prima e dopo, prodotti "dimenticati" recuperati |
| 4 | **Serve accesso ai dati del distributore** (catalogo, prezzi per cliente, storico, giacenze) | 🟠 Media | Si può partire con catalogo e storico esportati; l'integrazione completa con il gestionale arriva dopo |
| 5 | **Suggerimenti sbagliati o insistenti** rovinano la fiducia | 🟠 Media | Pochi suggerimenti, basati sullo storico del locale e su locali simili; controllo del distributore sui contenuti |
| 6 | **I grandi marchi (Galbani, San Carlo) hanno già i loro sistemi** | 🟡 | Non sono il cliente iniziale: il cliente è il **distributore multimarca regionale** |
| 7 | **Mercato del Sud frammentato e lento** | 🟠 Media | È anche un vantaggio: i grandi player (Choco, Salesforce) non ci arrivano. Le referenze tra distributori della stessa zona contano molto |
| 8 | **Choco o altri aggiungono le stesse funzioni** | 🟡 | Possibile nel tempo; il vantaggio iniziale è la **conoscenza del canale "rappresentante + bar"** del Sud Italia |
| 9 | **WhatsApp**: costi e regole dell'API Business, messaggi promozionali regolati | 🟡 | Messaggi su richiesta del cliente e conversazioni di servizio; le promozioni vanno dosate |

---

## 5. Ipotesi critiche (le cose da capire prima di costruire)

| # | Ipotesi | Come capirlo | Peso |
|---|---|---|---|
| **A1** | Il problema "mi dimentico cosa ordinare" e "il rappresentante non mi consiglia" è **comune** tra i baristi, non solo tuo | Chiederlo ad altri baristi che conosci (stesso distributore e altri) | 🔴 Decisiva |
| **A2** | I baristi **scriverebbero davvero** all'assistente durante la settimana | **Provarlo su te stesso**: per 2-3 settimane annota su una chat (anche con te stesso) ogni cosa che ti manca. Quante cose avresti segnato? Quante ne avresti dimenticate? | 🔴 Decisiva |
| **A3** | Il distributore **perde vendite** per prodotti dimenticati e proposte mancate, e questo vale abbastanza da pagare | Domande al titolare e al rappresentante di Scaramozzino (sotto) | 🔴 Decisiva |
| **A4** | I rappresentanti **lo accettano** | Parlarne con il tuo rappresentante | 🟠 |
| **A5** | Il distributore può **condividere** catalogo, prezzi e storico dei clienti | Domanda al titolare | 🟠 |
| **A6** | Esistono **molti distributori simili** a Scaramozzino (multimarca, regionali, con rappresentanti di zona) | Associazioni (Italgrob), elenchi provinciali, i tuoi fornitori | 🟠 |

### Domande utili per capire (per te, il tuo rappresentante e il titolare del distributore)
**A te stesso:**
- Quante volte al mese ti accorgi di aver dimenticato qualcosa dopo la visita? Cosa fai allora (aspetti la visita successiva, compri altrove, chiami)?
- Quanto vale, più o meno, quello che compri **altrove** perché te ne sei dimenticato?

**Al rappresentante:**
- Quanti clienti visita al giorno e quanto dura una visita?
- Quante volte i clienti gli dicono "non ricordo" o lo richiamano dopo?
- Gli farebbe comodo arrivare con la lista già pronta? Cosa lo preoccuperebbe?

**Al titolare del distributore:**
- Quanti clienti e quanti rappresentanti ha? Che gestionale usa?
- Sa quanto perde in vendite "dimenticate" o in clienti che comprano altrove?
- Riceve promozioni dai produttori che faticano ad arrivare ai clienti?
- Pagherebbe per aumentare del X% il valore medio degli ordini?

---

## 6. Dimensione dell'opportunità (stima da verificare)

| Voce | Ipotesi |
|---|---|
| Distributori Horeca in Italia | ~3.400 |
| Multimarca regionali con rappresentanti di zona (come Scaramozzino) | Ipotesi: la maggior parte dei piccoli e medi |
| Clienti attivi per distributore | 300-2.000 |
| Prezzo indicativo | 1-3 € per cliente attivo al mese, oppure 300-2.000 € al mese per distributore |
| Ricavo medio per distributore | ~5.000-25.000 €/anno |
| **Per 1 M€ di ricavi annui** | **~40-200 distributori** |
| Valore per il distributore | Se l'ordine medio cresce anche solo del 3-5% su centinaia di clienti, il ritorno supera di molto il costo (_da verificare con i dati veri_) |

---

## 7. Giudizio sul concept

| Domanda | Risposta |
|---|---|
| Il concept è più forte della versione "copia di Choco"? | **Sì, nel tuo contesto.** Nasce da come funzionano davvero gli ordini nel Sud (visita del rappresentante), da un problema che vivi tu e da una soluzione che hai descritto tu |
| Chi paga? | **Il distributore**, perché vende di più e i suoi rappresentanti rendono di più. Il bar lo usa gratis |
| Cosa lo distingue? | Lavora **tra una visita e l'altra**, **consiglia**, e **aiuta il rappresentante** invece di sostituirlo |
| Il rischio più grande | Che i baristi **non prendano l'abitudine** di scrivere (A2) e che il distributore **non veda abbastanza ritorno** (A3) |
| Il primo test | **Su te stesso e con Scaramozzino**: il tuo bar e il tuo distributore sono il laboratorio perfetto |
| Il tuo amico ingegnere informatico | Arriva nel momento giusto: **dopo** aver chiarito A1-A3, quando il concept è solido |
| Giudizio | 🟢🟡 **Il concept più centrato emerso finora** |

---

## Fonti

- [Choco: OrderAgent](https://choco.com/us/choco-ai)
- [Choco: pagina stampa (mercati)](https://choco.com/uk/press)
- [Salesforce: Consumer Goods (Agentforce)](https://www.salesforce.com/in/consumer-goods/?bc=OTH)
- [Mobisale: funzionalità AI](https://mobisoft.co/ai-capabilities/?lang=en)
- [Digital Commerce 360: GrubMarket lancia un agente AI per i venditori](https://www.digitalcommerce360.com/2026/06/10/grubmarket-ai-agent-for-sales-team/)
- [Distribution Strategy: GrubMarket, agente AI per i distributori alimentari](https://distributionstrategy.com/?p=10793)
- [Pulse 2.0: Dashmote, Series A da 6 M$ per DashSalesAI](https://pulse2.com/dashmote-6-million-series-a-raised-to-advance-dashsalesai-and-expand-operations)
- [Dealermatix: AI e raccolta ordini (gennaio 2026)](https://dealermatix.com/2026/01/29/)
- [Money.it: il fatturato Ho.Re.Ca. vale 107 miliardi (dati Italgrob)](https://www.money.it/il-fatturato-horeca-e-cresciuto-del-23-in-5-anni-oggi-vale-107-miliardi)

_Nota: non ho trovato informazioni pubbliche su Scaramozzino Srl; il nome e il ruolo vengono dall'esperienza del founder. Prezzi, ricavi e aumento dell'ordine medio sono ipotesi da verificare. Le descrizioni dei concorrenti vengono dai loro materiali commerciali._
