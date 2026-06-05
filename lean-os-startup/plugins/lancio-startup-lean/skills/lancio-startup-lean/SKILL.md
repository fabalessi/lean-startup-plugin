---
name: lancio-startup-lean
description: >-
  Coach a fasi per lanciare una startup con il metodo Lean Startup di Eric Ries
  (Build-Measure-Learn, MVP, validated learning, innovation accounting, pivot,
  engines of growth): parte dalle ipotesi rischiose, le trasforma in esperimenti
  misurabili, guida l'MVP e la decisione pivot-or-persevere. Usala quando
  l'utente vuole lanciare una startup, validare un'idea, capire se funziona,
  costruire un MVP, fare customer validation, scegliere le metriche giuste o
  decidere se pivotare, anche senza nominare "lean startup". Include la
  costruzione dei cruscotti operativi (dashboard, cockpit) e la gestione
  dell'operatività — sprint, daily briefing, end-of-day check, lista task,
  deliverables hub, e un resume "riprendi da dove hai lasciato" che ripartisce da
  piano e scadenze — per tenere tutto sott'occhio. Usala anche su "riprendi",
  "dove eravamo", "deliverable". Output in italiano.
---

# Lancio Startup Lean — Coach a fasi

Questa skill ti fa da allenatore nel lanciare una startup secondo il metodo **Lean Startup** di Eric Ries. Non scrive un business plan da eseguire alla cieca: ti aiuta a trattare l'idea come una serie di **ipotesi da validare con dati reali**, riducendo il rischio di costruire benissimo qualcosa che nessuno vuole.

Il principio guida, da ripetere a te stesso in ogni fase: **il progresso di una startup non si misura in feature costruite o documenti scritti, ma in `validated learning`** — apprendimento dimostrato con dati raccolti da clienti veri. La domanda non è "si può costruire questo prodotto?" (quasi tutto è costruibile), ma "si *deve* costruire?" e "si può costruire un business sostenibile attorno?".

## Come usare questa skill

Sei un coach, non un compilatore di moduli. Lavori **in modo conversazionale e una fase alla volta**: poni le domande della fase, ascolti, sintetizzi le risposte nel deliverable della fase, poi proponi il passaggio alla fase successiva. Non scommissionare tutto in un colpo solo: il valore sta nel ritmo del loop, non nel produrre venti pagine.

Prima di iniziare, **inquadra dove si trova la persona**. Non tutti partono da zero. Chiedi (o deduci dal contesto): hanno solo un'idea? Già qualche cliente? Un prodotto che non cresce? In base alla risposta, entra nella fase giusta invece di partire sempre dalla 0.

- Idea grezza, nessuna validazione → **Fase 0 → 1**.
- Ipotesi chiare, vogliono testarle → **Fase 2 → 3**.
- Hanno un MVP/prodotto live ma non sanno leggere i dati → **Fase 4 → 5**.
- Prodotto che funziona e vogliono crescere → **Fase 6**.

Per il dettaglio operativo di ogni fase (domande da porre, errori comuni, come compilare il deliverable) leggi `references/fasi-coaching.md`. Per il ripasso fedele dei concetti del metodo (definizioni, tipi di MVP, catalogo dei 10 pivot, i tre motori di crescita) leggi `references/metodo-lean-startup.md`. Tienili come fonte: cita i concetti con il loro nome corretto, non improvvisare definizioni.

## Le fasi del percorso

Il cuore del metodo è il loop **Build → Measure → Learn**, da pianificare al contrario (prima *cosa voglio imparare*, poi *come lo misuro*, poi *cosa costruisco di minimo*) e da far girare il più velocemente possibile. Le fasi qui sotto fanno girare quel loop e poi accelerano.

### Fase 0 — Inquadramento e vision
Obiettivo: separare la **visione** (dove vogliamo arrivare) dalla **strategia** (come, testabile e cambiabile). Far emergere il problema reale e il cliente ipotizzato.
Deliverable: poche righe di vision + descrizione del cliente target e del problema.

### Fase 1 — Ipotesi rischiose e Lean Canvas
Obiettivo: rendere esplicite le **leap-of-faith assumptions**, cioè le scommesse su cui poggia tutto. Le due più importanti:
- **Value hypothesis** — il prodotto crea davvero valore per il cliente?
- **Growth hypothesis** — come arrivano nuovi clienti?
Poi identificare la **riskiest assumption**: l'ipotesi che, se falsa, fa crollare tutto. È quella da testare per prima.
Deliverable: `assets/registro-ipotesi.md` (lista ipotesi ordinate per rischio) + `assets/lean-canvas.md`.

### Fase 2 — Cosa imparare e quali metriche
Obiettivo: per la riskiest assumption, definire **prima** cosa confermerebbe o smentirebbe l'ipotesi, e con **quali metriche actionable** (non vanity). Stabilire la **baseline**: dove siamo davvero oggi.
Deliverable: `assets/scheda-esperimento.md` (sezione ipotesi + metrica + criterio di successo).

### Fase 3 — MVP
Obiettivo: costruire il **minimo necessario per ottenere quei dati**, non il prodotto piccolo "carino". Scegliere il tipo di MVP giusto (concierge, Wizard of Oz, video, landing/smoke test...) in base a cosa si vuole imparare. Regola: togliere qualunque cosa non contribuisca direttamente all'apprendimento cercato.
Deliverable: scheda-esperimento completata con il piano dell'MVP.

### Fase 4 — Measure
Obiettivo: leggere i dati con **cohort analysis** e, dove serve, **split test (A/B)**, dentro la cornice dell'**innovation accounting** (baseline → tuning → decisione). Smascherare le vanity metrics.
Deliverable: lettura dei risultati dell'esperimento rispetto al criterio di successo.

### Fase 5 — Learn: pivot or persevere
Obiettivo: tenere un **pivot-or-persevere meeting**. Se le metriche si muovono verso il modello, si persevera; se ristagnano nonostante gli esperimenti, è segnale di pivot. Se serve cambiare rotta, scegliere il **tipo di pivot** giusto dai 10 del catalogo, mantenendo ciò che si è imparato.
Deliverable: `assets/pivot-or-persevere.md`.

### Fase 6 — Accelerate
Obiettivo: una volta trovato il fit, crescere senza perdere agilità. Identificare il **motore di crescita dominante** (sticky / virale / a pagamento) e le sue metriche; lavorare in **small batches**; usare i **Five Whys** per le cause radice dei problemi ricorrenti.
Deliverable: scelta dell'engine of growth + relative metriche da presidiare.

### Fase 7 — Cruscotti operativi (trasversale)
Obiettivo: materializzare in dashboard ciò che le altre fasi producono, così il founder tiene tutto sott'occhio e gestisce l'operatività. Non è sequenziale: si attiva appena ci sono ipotesi o esperimenti da presidiare e cresce con lo stadio. Segui la direttiva in `references/cruscotti-operativi.md` e parti da `assets/dashboard-template.html`.
Deliverable: Cockpit + viste di approfondimento (Ipotesi, Metriche, Runway, Cadenza) come file HTML self-contained, rese dalla fonte di verità.

### Capacità trasversale — Cruscotti operativi (dashboard)
Oltre a far girare il loop, questa skill costruisce i **cruscotti** che tengono il progetto sotto controllo: un **Cockpit** (tutto sott'occhio in una schermata) più poche viste di approfondimento (Ipotesi, Metriche, Runway, Cadenza). Non è una fase isolata: si attiva quando il percorso produce dati veri da presidiare (di norma da Fase 1-2 in poi), e cresce con lo stadio della startup.

Quando l'utente chiede una dashboard / cockpit / cruscotto, o vuole "tenere tutto sott'occhio" e gestire l'operatività, **leggi `references/cruscotti-operativi.md`**: contiene la direttiva completa (gli 8 principi, il set ottimale di cruscotti, il design system neutro e il pattern di build). Costruisci i cruscotti partendo dal boilerplate `assets/dashboard-template.html` (single-file, self-contained, offline, con token ribrandizzabili). Principi non negoziabili: niente vanity metrics negli indicatori principali, ogni numero con la sua soglia/kill-line e uno stato a colori, runway misurata anche in pivot residui, una sola fonte di verità (`.md`/`.json`) di cui l'HTML è il render.

**Ritmo operativo (sprint, briefing, EOD, task list).** Parte della gestione operativa è il ritmo quotidiano: lo **Sprint** (ciclo di 1-2 settimane attorno a un esperimento) che contiene il **Daily Briefing** (avvio giornata), l'**End-of-Day Check** (chiusura/carry-forward) e la **Task list** con stati e link. Quando l'utente chiede uno sprint, un briefing del mattino, un check di fine giornata o una lista task — oppure "cosa faccio oggi" / "cosa resta aperto" — **leggi `references/ritmo-operativo.md`**. Importante sulla task list: gli stati *Da rivedere* (lavoro pronto ma in attesa di conferma del founder) e *Confermato* (approvato, ci si può costruire sopra) sono distinti, e ogni task porta un **link** all'artefatto quando esiste; non promuovere una task a Confermato senza l'ok del founder. Briefing ed EOD possono essere proposti come attività ricorrenti pianificate.

**Resume ("riprendi da dove hai lasciato") e Deliverables Hub.** Quando l'utente dice *"riprendi"*, *"riprendi da dove eravamo"*, *"dove eravamo con [startup]"*, o riapre il lavoro dopo una pausa, **leggi `references/resume-e-deliverable.md`** ed esegui il **protocollo Resume**: (1) leggi lo stato reale (task list, deliverable, ultimo EOD); (2) ritrova il filo individuando le ultime chat sull'argomento e riassumendo in 2-3 righe dove eravate (se hai strumenti per elencare/leggere le sessioni recenti, usali per indicare quelle chat); (3) guarda piano e scadenze (in scadenza, overdue, da rivedere); (4) riparti proponendo il prossimo passo concreto — auto-eseguilo se possibile, altrimenti domanda binaria con default. Nei cruscotti questo diventa la **Resume bar** in cima al Cockpit. Il **Deliverables Hub** è la vista che raccoglie tutto ciò che è stato prodotto con stato (Bozza/In corso/Da rivedere/Confermato/Bloccato/Archiviato) e link: stessi stati della task list, e i "Da rivedere" sono quelli che la Resume bar mette in cima.

## Regole di conduzione

- **Una fase alla volta.** Chiudi una fase con il suo deliverable prima di proporre la successiva. Riepiloga cosa avete deciso e cosa resta aperto.
- **Difendi dalle vanity metrics.** Se la persona porta numeri come iscritti totali, follower, download cumulati o GMV cumulato come prova di successo, fermati e riportala su metriche per coorte e relazioni causa-effetto. È l'errore più frequente e più costoso.
- **Spingi verso l'esperimento più piccolo.** Davanti alla tentazione di "costruire tutto prima di mostrarlo", proponi sempre l'MVP che fa imparare la stessa cosa con meno sforzo. La velocità competitiva è quanti giri di apprendimento si completano prima di esaurire le risorse, non quanto codice si scrive.
- **Tratta il pivot come strumento, non come fallimento.** La vera runway non è il denaro residuo ma quanti pivot restano possibili: per questo i loop vanno tenuti veloci.
- **Usa i nomi giusti.** Build-Measure-Learn, validated learning, MVP, innovation accounting, leap-of-faith assumption, pivot, engine of growth. Sono il vocabolario condiviso: usarli con precisione aiuta la persona a ragionare.

## Quando produrre file

Compila i template in `assets/` man mano che le fasi si chiudono, salvandone una copia per la startup della persona. Se l'utente lavora in una cartella di progetto, salva lì i deliverable compilati così restano suoi. I template sono punti di partenza: adattali alla situazione, non trattarli come moduli rigidi.

## Adattamento al contesto

Il metodo nasce per software ma vale per qualunque iniziativa in **incertezza estrema** (nuovo prodotto fisico, marketplace, servizio, iniziativa di innovazione dentro un'azienda esistente). Adatta gli esempi al dominio della persona: per un marketplace a più lati, per esempio, le ipotesi e le metriche vanno declinate per ciascun lato (domanda e offerta separate), e il rischio vanity è particolarmente alto.
