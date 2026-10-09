# Analisi critica: uno "store" di soluzioni AI verticali pronte da installare, per chi non è tecnico

_Data: 9 ottobre 2026_

**L'intuizione del founder:** molte startup di oggi sono "un LLM specializzato su un processo verticale". Invece di farne una, si potrebbe creare un **negozio (e-commerce) di queste verticalizzazioni**, vendute come **pacchetti facili da installare e attivabili al volo**: una sorta di **GitHub per chi non è tecnico**.

---

## 0. In una pagina

- **L'osservazione di partenza è giusta:** buona parte delle startup AI sono flussi di lavoro verticali costruiti sopra un LLM. Ed è proprio per questo che **uno store che le raccoglie compete con tutte loro e con i giganti che le ospitano**.
- **L'offerta c'è già, in quantità enorme e quasi tutta gratuita:**
  - oltre **30.000 server MCP** nel registro ufficiale;
  - migliaia di skill e plugin per Claude;
  - milioni di GPT personalizzati;
  - template n8n e Make.

  **Il problema non è che manchino soluzioni, ma che non si sa quali funzionano, come collegarle ai propri strumenti e chi le sistema quando si rompono.**
- **Gli store li stanno costruendo le piattaforme dove gli utenti lavorano già:** la directory di app e plugin di ChatGPT, i plugin di Claude, l'**Agent Store di Microsoft 365 Copilot**, **AgentExchange di Salesforce** (unito ad AppExchange e allo Slack Marketplace nel 2026), Google. **Un negozio indipendente non ha gli utenti**.
- **Il precedente è negativo:** il **GPT Store** di OpenAI ha avuto milioni di GPT ma una monetizzazione per i creatori **poco chiara o assente**, e secondo alcune fonti i GPT personalizzati vengono ritirati e trasformati in plugin. Gli store che funzionano sono quelli **dentro il software che l'azienda usa già** (su AgentExchange un fornitore ha fatto 2 M$ in 9 mesi, con l'80% dei clienti arrivati dalla scoperta dentro il prodotto).
- **Per chi non è tecnico il difficile non è installare:** è **collegare** l'agente ai propri dati e programmi (gestionale, fatturazione elettronica, email, CRM), **adattarlo** al proprio modo di lavorare, **fidarsi** (privacy, GDPR, AI Act) e **mantenerlo**. Questo è un **servizio**, non un download.
- **Verdetto: 🔴 come marketplace generico.** 🟡 in una forma diversa: **catalogo curato per le PMI italiane, già collegato ai gestionali italiani, con installazione e assistenza incluse** (l'"App Store + tecnico che te lo installa"). Oppure una **suite verticale per una sola categoria professionale**.

---

## 1. Dare forma all'idea

### Cosa sarebbe, concretamente
```
  Creatori (sviluppatori, consulenti, startup)          Clienti (PMI, professionisti, non tecnici)
        │ pubblicano "pacchetti verticali"                     │ cercano "una soluzione per..."
        ▼                                                      ▼
   ┌───────────────────────────── LO STORE ───────────────────────────────┐
   │ catalogo · recensioni · installazione con 1 clic · pagamento · aggiornamenti │
   └──────────────────────────────────────────────────────────────────────┘
        │                                                      │
        ▼                                                      ▼
   Guadagno dello store: commissione                 Il pacchetto deve funzionare con
   (15-30%) o abbonamento                            i SUOI dati e i SUOI programmi
```

### Esempi di "pacchetti verticali"
| Pacchetto | Per chi | Cosa deve collegare |
|---|---|---|
| Risposta automatica alle richieste di preventivo | Artigiani, imprese edili | Email, WhatsApp, listino |
| Solleciti di pagamento e riconciliazione delle fatture | PMI | Fatturazione elettronica, banca |
| Gestione delle prenotazioni e recensioni | Ristoranti, hotel | Booking, Google Business, PMS |
| Lettura delle bollette e ottimizzazione energetica | PMI, condomini | PDF, portali dei fornitori |
| Prima bozza delle pratiche | Studi professionali | Gestionale di studio, documenti dei clienti |

---

## 2. Smontare l'idea

| # | Obiezione | Evidenza | Gravità | Si può rispondere? |
|---|---|---|---|---|
| 1 | **Le piattaforme sono già gli store.** Chi controlla il "sistema operativo" (ChatGPT, Claude, Copilot, Salesforce, Google) controlla anche il negozio, come Apple e Google con le app | Directory di app e plugin di ChatGPT; plugin di Claude Code; Agent Store di Microsoft 365 Copilot (oltre 70 agenti al lancio); AgentExchange (oltre 1.000 agenti e strumenti) | 🔴 Alta | Solo **dove le piattaforme non arrivano** (lingua, software locali, servizio sul posto) |
| 2 | **Offerta sovrabbondante e gratuita** | ~30.000 server MCP; Smithery, Glama e mcp.so con migliaia di voci; migliaia di skill gratuite; template n8n | 🔴 Alta | Il valore non è "avere più pacchetti", ma **selezionare quelli che funzionano** |
| 3 | **I marketplace indipendenti di agenti faticano a far guadagnare** | GPT Store: monetizzazione dei creatori poco chiara; Poe è citato come unica eccezione con guadagni attivi | 🔴 Alta | Lo store deve guadagnare dal **servizio**, non dalla commissione su pacchetti da pochi euro |
| 4 | **Doppio problema dell'uovo e della gallina** | Servono creatori per attirare clienti e clienti per attirare creatori | 🟠 Media-alta | Partire con **pochi pacchetti fatti in casa** o selezionati, non con un marketplace aperto |
| 5 | **Per un non tecnico "installare" non basta** | Il pacchetto deve leggere il suo gestionale, la sua posta, le sue fatture; se cambia qualcosa si rompe | 🔴 Alta | È **l'opportunità vera**: integrazione, configurazione e assistenza |
| 6 | **Fiducia e responsabilità** | Dati dei clienti, GDPR, AI Act (pienamente applicabile da agosto 2026); chi risponde se l'agente sbaglia una fattura? | 🟠 Media | Catalogo **curato e verificato**, non aperto a chiunque |
| 7 | **Le startup verticali migliori vogliono il cliente diretto** | Se un pacchetto funziona, il creatore preferisce vendere da solo e tenersi la relazione | 🟠 Media | Lo store serve soprattutto alla **coda lunga** (consulenti, piccoli sviluppatori), che vale meno |
| 8 | **I gestionali italiani aggiungono l'AI da soli** | TeamSystem, Zucchetti e altri integrano funzioni AI nei loro prodotti (_da verificare caso per caso_) | 🟠 Media | Collaborare con loro, o puntare ai processi che **attraversano più programmi** |
| 9 | **Competenze richieste** | Integrazioni, sicurezza, manutenzione | 🟠 Media | La versione "servizio" si avvia con strumenti esistenti (n8n, Make, connettori); per scalare serve un socio tecnico |

**Conclusione dello smontaggio:** "un GitHub o App Store di agenti verticali per non tecnici" **come marketplace aperto e generico cade**. Le piattaforme hanno già gli utenti e i loro store, l'offerta è gratuita e sovrabbondante, e il vero ostacolo per chi non è tecnico non è il download ma l'integrazione e la fiducia.

---

## 3. Il problema riformulato

| Visto dall'idea | Visto dalla realtà |
|---|---|
| "Mancano pacchetti facili da installare" | **Ci sono troppi pacchetti, e nessuno garantisce che funzionino con i miei strumenti** |
| "Serve un negozio" | **Serve qualcuno che scelga, colleghi, adatti e mantenga** |
| Valore: catalogo | Valore: **curatela + integrazione con i software locali + assistenza** |
| Modello: commissione | Modello: **canone mensile per soluzione installata e mantenuta** |

> **Analogia:** il negozio di app esiste già (ce l'ha ogni piattaforma). Manca **il tecnico di fiducia che te le installa, le collega al tuo gestionale e te le aggiusta**, in italiano e con prezzi da PMI.

---

## 4. Forme alternative a confronto

| | **A. Marketplace aperto di agenti verticali** (forma proposta) | **B. Catalogo curato per PMI italiane + installazione e assistenza** | **C. Suite verticale per una sola professione** | **D. Strumenti per consulenti AI che vendono pacchetti ai clienti** |
|---|---|---|---|---|
| Cosa fa | Chiunque pubblica, chiunque compra | 20-50 soluzioni **testate**, già collegate ai software italiani (fatturazione elettronica, gestionali diffusi, PEC, home banking), installate e mantenute | Un insieme di agenti per **un mestiere** (es. officine, agenzie immobiliari, studi tecnici, ristoranti) | Piattaforma con cui consulenti e piccole agenzie confezionano, installano, fatturano e mantengono gli agenti dei loro clienti |
| Chi paga | Clienti (commissione) | **PMI: canone mensile per soluzione** (es. 50-300 €) | Professionisti: abbonamento | Consulenti: abbonamento o percentuale |
| Concorrenza | 🔴 Piattaforme e registri gratuiti | 🟡 System integrator e consulenti locali, gestionali che aggiungono AI | 🟠 Startup verticali (tante) | 🟠 Agent.ai, Relevance AI, Lindy, n8n, Make |
| Vantaggio difendibile | Nessuno | **Integrazioni italiane + fiducia + assistenza** | Conoscenza del mestiere | Effetto rete tra consulenti |
| Adatto a te | ❌ | ✅ **Sì all'inizio**: commerciale e organizzativo, con strumenti no-code esistenti | ⚠️ Solo se conosci un mestiere | ⚠️ Serve un team tecnico |
| Scalabilità | Alta in teoria, nulla in pratica | **Media**: il catalogo scala, l'assistenza no (ma si può fare tramite partner) | Media-alta | Alta, se si crea la rete |
| **Valutazione** | 🔴 | 🟡 **La più realistica** | 🟡 | 🟡 |

### La forma B più nel dettaglio
- **Il cliente:** PMI e professionisti italiani che **vogliono usare l'AI ma non sanno da dove partire** e non hanno un informatico interno.
- **L'offerta:** un catalogo breve di soluzioni per **processi comuni** (preventivi, solleciti, prenotazioni, recensioni, prima lettura dei documenti, risposte ai clienti), **già collegate** ai software diffusi in Italia.
- **Il modello:** canone per soluzione attiva, che comprende installazione, adattamento e manutenzione. Più avanti, **una rete di installatori locali** (consulenti, informatici di zona) che ricevono una percentuale.
- **Il vantaggio nel tempo:** ogni nuova installazione rende il catalogo più affidabile; le integrazioni con i software italiani sono lavoro che **le piattaforme globali non fanno**.
- **Il collegamento con l'idea della rete nei piccoli centri:** gli installatori locali potrebbero essere proprio le persone qualificate che vivono in provincia.

### Esempio di economia (ipotesi)
| Voce | Valore |
|---|---|
| Canone medio per soluzione | 100 €/mese |
| Soluzioni per cliente | 2 |
| Ricavo per cliente all'anno | ~2.400 € |
| **Per 1 M€ di ricavi annui** | **~420 clienti** |
| Costo nascosto | Assistenza: va contenuta con soluzioni standard e partner locali |

---

## 4-bis. Il modello del "rivenditore di sistemi cassa" applicato all'AI

_Spunto del founder: un'azienda retail che vende punti cassa e soluzioni per negozi ("ARMENTARO retail"; non ho trovato informazioni pubbliche con questo nome, quindi uso il modello tipico del settore)._

### Come funziona il modello dei sistemi cassa
| Elemento | Nei sistemi cassa | Equivalente AI |
|---|---|---|
| Prodotto | Registratore telematico + POS + gestionale del punto vendita | Pacchetti di agenti per i processi del negozio o della PMI |
| Chi produce | Produttori (es. DTR con MoitoIOT), software house | Piattaforme AI + chi confeziona i pacchetti |
| Chi vende e installa | **Rivenditori locali** con tecnici sul territorio | Rivenditori o installatori AI locali |
| Ricavo ricorrente | **Contratti di assistenza, verifiche periodiche obbligatorie**, aggiornamenti | Canone di manutenzione e aggiornamento |
| Motore della domanda | **Obblighi di legge**: scontrino elettronico, verifiche periodiche, integrazione POS-RT obbligatoria dal 2026 | ❌ **Nessun obbligo**: la domanda è facoltativa |

### La differenza decisiva: l'obbligo
I rivenditori di sistemi cassa vivono di una domanda **resa obbligatoria dalla legge**. Ogni negozio deve avere il registratore telematico, farlo verificare e integrarlo con il POS. **Per l'AI non esiste un obbligo simile.** L'unico aggancio normativo è l'**AI Act**: chi usa sistemi di AI deve garantire un livello adeguato di **alfabetizzazione sull'AI** del personale (art. 4) e rispettare GDPR e trasparenza. Può essere un argomento di vendita, ma non è un obbligo forte come lo scontrino elettronico.

### L'opportunità nascosta: i rivenditori esistenti come canale
- Il **D.Lgs. 108/2024** apre alla possibilità di registratori **solo software**, e l'hardware perde peso. **I rivenditori di sistemi cassa e di informatica rischiano di perdere una parte del loro business** e cercano nuovi prodotti da vendere ai clienti che già seguono.
- Hanno già ciò che a una startup manca: **la fiducia di migliaia di negozi, i tecnici sul territorio e i contratti di assistenza in corso.**
- **Quindi:** invece di costruire una propria rete, si diventa il **"produttore e distributore" di pacchetti AI per i rivenditori esistenti**. Come DTR fornisce cassa e gestionale ai dealer, la startup fornirebbe il **catalogo AI, gli strumenti per installarlo, la formazione e l'assistenza di secondo livello**. Il rivenditore lo vende e lo installa ai suoi clienti.

| | Rete propria (forma B) | **Distributore per i rivenditori esistenti** |
|---|---|---|
| Velocità di accesso ai clienti | Lenta | **Veloce**: i rivenditori hanno già i clienti |
| Costo commerciale | Alto | Basso: si vendono pochi accordi con rivenditori, non migliaia di contratti |
| Margine | Più alto per cliente | Più basso (si divide con il rivenditore), ma scala meglio |
| Rischio | Assistenza diretta | Qualità variabile dei rivenditori; dipendenza dal canale |
| Adatto a te | ✅ | ✅ **Molto**: è un lavoro di accordi commerciali e di rete |

**Nuove ipotesi critiche per questa variante:**
- **H6:** i rivenditori di sistemi cassa e informatica **vogliono** vendere AI e hanno le competenze minime per installarla con un buon supporto.
- **H7:** i loro clienti (negozi, bar, ristoranti, piccole imprese) **hanno processi abbastanza standard** (prenotazioni, recensioni, ordini ai fornitori, magazzino, risposte ai clienti) da poter usare pacchetti uguali per tutti.

---

## 5. Ipotesi critiche

| # | Ipotesi | Perché potrebbe essere falsa | Peso |
|---|---|---|---|
| H1 | Le PMI **pagano un canone mensile** per soluzioni AI installate e mantenute | Potrebbero aspettare che le funzioni arrivino "gratis" nei programmi che già usano | 🔴 Decisiva |
| H2 | Esistono **5-10 processi comuni** abbastanza simili tra aziende diverse da essere standardizzati | Ogni PMI lavora a modo suo: se ogni installazione è su misura, il modello diventa consulenza | 🔴 Decisiva |
| H3 | I costi di **assistenza** restano sotto controllo | Le integrazioni si rompono quando cambiano i software o le API | 🟠 |
| H4 | I **gestionali italiani** lasciano spazio | Potrebbero integrare le stesse funzioni nel giro di 1-2 anni | 🟠 |
| H5 | Si trovano **installatori locali** affidabili | Qualità variabile, rischio per la reputazione | 🟡 |

---

## 6. Verdetto

| Domanda | Risposta |
|---|---|
| L'intuizione è giusta? | **Sì**: molte startup AI sono "LLM + processo verticale", e chi non è tecnico non riesce a usarle |
| Lo store/marketplace funziona? | **No**: le piattaforme hanno già gli utenti e i loro negozi, l'offerta è gratuita e sovrabbondante, e il problema non è il download |
| Cosa regge? | **Curatela + integrazione con i software italiani + installazione e assistenza**, venduta in abbonamento alle PMI |
| È una startup? | **Sì, ma "tech-enabled services"**: cresce più lentamente di un software puro, perché parte dell'assistenza è lavoro umano |
| Adatta a te? | **Sì, più di molte idee precedenti**: si può avviare con strumenti no-code esistenti e capacità commerciali. Per scalare servirà un socio tecnico |
| Le due ipotesi decisive | **H1** (pagano un canone) e **H2** (i processi sono abbastanza standard) |

### Confronto con le altre idee
| Idea | Verdetto | Startup? | Adatta a te? |
|---|---|---|---|
| Permitting Intelligence | 🟡 | Sì, di nicchia | Con un socio esperto |
| Rete per startup nei piccoli centri | 🟡 | No (impresa d'impatto) | ✅ Molto |
| Dati di prodotto AI-ready verticali | 🟡 | Sì (dati e servizi) | ✅ se conosci un settore |
| **Catalogo AI curato e installato per PMI** | 🟡 | Sì (servizi con tecnologia) | ✅ |

**Nota:** le ultime tre idee convergono sullo stesso punto. **L'AI c'è già; quello che manca alle PMI italiane è chi la rende utilizzabile nel loro contesto.** È probabilmente il filo conduttore più solido emerso finora.

---

## Fonti

- [Digital Applied: marketplace di agenti AI nel 2026, scoperta e distribuzione](https://www.digitalapplied.com/blog/ai-agent-marketplaces-2026-discovery-distribution)
- [Fast.io: i principali marketplace di agenti AI nel 2026](https://fast.io/resources/top-ai-agent-marketplaces/)
- [InstantDM: i migliori marketplace di agenti AI nel 2026](https://instantdm.com/blog/best-ai-agent-marketplaces-2026)
- [Taskade: plugin ChatGPT, directory, GPT e storia](https://www.taskade.com/blog/chatgpt-plugins)
- [Top5Apps: lo store di plugin di ChatGPT nel 2026](https://top5apps.ai/news/chatgpt-plugin-extensions-store-2026/)
- [GitHub: awesome-chatgpt-apps (directory delle app di ChatGPT)](https://github.com/rdmgator12/awesome-chatgpt-apps)
- [Microsoft 365 Developer Blog: l'Agent Store in Microsoft 365 Copilot](https://devblogs.microsoft.com/microsoft365dev/introducing-the-agent-store-build-publish-and-discover-agents-in-microsoft-365-copilot/)
- [Microsoft: gli agenti in Microsoft 365 Copilot](https://www.microsoft.com/en-us/microsoft-cloud/blog/2025/09/25/empower-your-workforce-with-agents-in-microsoft-365-copilot/)
- [Salesforce: lancio di AgentExchange](https://www.salesforce.com/news/press-releases/2025/03/04/agentexchange-announcement/)
- [SalesforceBen: AppExchange, Slack Marketplace e Agentforce uniti, con 50 M$](https://www.salesforceben.com/appexchange-slack-marketplace-and-the-agentforce-ecosystem-are-now-one-with-fresh-50m-funding/)
- [SalesforceDevops: AgentExchange, la scommessa sulla fiducia](https://salesforcedevops.net/index.php/2026/04/14/agentexchange-salesforces-bet-that-trust-can-scale-with-agentic-speed/)
- [LevelUpSalesforce: AgentExchange supera le 120 app](https://levelupsalesforce.com/momentum-on-the-move-agentexchange-surges-past-120-apps-with-100-developers)
- [Alex Cloudstar: il marketplace di plugin di Claude Code nel 2026](https://www.alexcloudstar.com/blog/claude-code-plugin-marketplace-skills-2026)
- [Ryan Doser: cosa esiste davvero come marketplace di skill per Claude](https://ryandoser.com/claude-skills-marketplace/)
- [LocalSkills: 8 directory di skill a confronto](https://localskills.sh/blog/claude-skills-marketplace-guide)
- [DevToolHub: il registro MCP in numeri](https://devtoolhub.com/mcp-registry-by-the-numbers/)
- [Daniel Vaughan: scoperta dei server MCP tra Smithery, Glama e registro ufficiale](https://codex.danielvaughan.com/2026/05/27/codex-cli-mcp-server-discovery-registries-smithery-glama-official-registry/)
- [FlowHunt: i migliori costruttori di agenti AI nel 2026](https://www.flowhunt.io/it/blog/best-ai-agent-builders-2026/)
- [Konverso: piattaforme no-code per agenti AI nel 2026](https://www.konverso.ai/en/blog/top-ai-agent-platform-in-2026)
- [Gartner: il panorama dei costruttori di agenti no-code](https://gcom.pdo.aws.gartner.com/en/articles/no-code-agent-builders-emerging-market)
- [Product Hunt: N8N Central](https://www.producthunt.com/p/n8n-central/n8n-central)

_Nota: molti numeri (GPT creati, server MCP, skill, ritiro dei GPT personalizzati) vengono da blog e directory di terze parti e sono in parte contraddittori. L'economia per cliente è un'ipotesi._
