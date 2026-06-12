# Guida alle fasi del coaching

Dettaglio operativo per condurre ciascuna fase: domande da porre, segnali da cogliere, errori comuni, come chiudere la fase. Conduci in modo conversazionale — poche domande mirate alla volta, non un interrogatorio. Per le definizioni dei concetti vedi `metodo-lean-startup.md`.

---

## Fase 0 — Inquadramento e vision

**Cosa ottenere:** separare la visione (la destinazione, stabile) dalla strategia (il come, testabile e cambiabile), e mettere a fuoco problema e cliente ipotizzato.

**Domande:**
- In una frase, quale mondo vuoi vedere quando questa startup avrà avuto successo? (vision)
- Quale problema specifico risolvi, e per chi? Descrivimi la persona, non "tutti".
- Come fa oggi questa persona a cavarsela senza di te? Cosa usa al posto tuo?
- Perché tu, perché ora?

**Errori comuni:** confondere la soluzione con il problema ("il mio problema è che non esiste la mia app" — no, quello è la soluzione); descrivere un cliente troppo ampio.

**Chiusura:** poche righe di vision + una scheda problema/cliente. Passa alla Fase 1.

---

## Fase 1 — Ipotesi rischiose e Lean Canvas

**Cosa ottenere:** trasformare l'idea in un elenco di **leap-of-faith assumptions** ordinate per rischio, e fotografare il modello nel Lean Canvas.

**Domande:**
- Perché un cliente dovrebbe volere questa cosa? Cosa stai dando per scontato che possa non essere vero? (→ value hypothesis)
- Una volta che hai un cliente felice, come ne arrivano altri? (→ growth hypothesis)
- Tra tutte queste convinzioni, quale, se fosse falsa, manderebbe all'aria tutto il resto? (→ riskiest assumption)

**Come condurre:** elenca con la persona 5-10 cose che "devono essere vere" perché il business funzioni. Per ognuna chiedi: quanto sei sicuro che sia vera (1-5)? quanto è grave se è falsa (1-5)? Ordina per rischio = incertezza × gravità. La prima della lista è ciò che testerete.

**Errori comuni:** trattare come ipotesi solo le cose tecniche ("riusciamo a costruirlo") e dimenticare quelle di mercato ("qualcuno lo vuole / pagherà / lo trova"); dare per scontata la growth hypothesis.

**Chiusura:** compila `assets/registro-ipotesi.md` e `assets/lean-canvas.md`. Evidenzia la riskiest assumption. Passa alla Fase 2.

---

## Fase 2 — Cosa imparare e quali metriche

**Cosa ottenere:** per la riskiest assumption, definire **in anticipo** il criterio che la conferma o la smentisce e la **metrica actionable** che lo misura. Stabilire la baseline.

**Domande:**
- Cosa, concretamente, vedresti accadere se questa ipotesi fosse vera? E se fosse falsa?
- Quale numero, osservabile su persone reali, lo dimostra? (spingi verso comportamenti: % che completa un'azione, % che torna, % che paga)
- Qual è la soglia oltre la quale dici "validato"? Decidila adesso, prima dell'esperimento, per non razionalizzare dopo.
- Sai già dove sei oggi su quel numero? (baseline)

**Difesa anti-vanity (importante):** se arrivano "iscritti totali", follower, download cumulati, GMV cumulato, fermati. Sono vanity metrics: salgono comunque e non dicono se il prodotto migliora. Riporta su metriche per coorte e su relazioni causa-effetto (vedi le tre A in `metodo-lean-startup.md`).

**Chiusura:** compila la parte alta di `assets/scheda-esperimento.md` (ipotesi, metrica, criterio di successo, baseline). Passa alla Fase 3.

---

## Fase 3 — MVP

**Cosa ottenere:** definire il **minimo necessario per ottenere quei dati**. Scegliere il tipo di MVP in base a cosa si vuole imparare.

**Scelta del tipo di MVP** (dettaglio in `metodo-lean-startup.md`):
- Vuoi sapere se esiste **domanda**, prima di costruire? → video MVP o smoke test / landing page.
- Vuoi capire se la tua **soluzione risolve davvero** il problema, su pochi utenti? → concierge MVP (servizio a mano).
- Vuoi testare l'**esperienza di un prodotto automatizzato** senza costruirlo? → Wizard of Oz.

**Domande:**
- Qual è la cosa più piccola e più rapida che possiamo mettere davanti a una persona vera per imparare X?
- Cosa stai pensando di costruire che *non* serve a questo apprendimento? (tagliarlo)
- Quanto tempo per il primo dato? Se la risposta è "settimane", c'è un MVP più piccolo.

**Errori comuni:** costruire troppo ("la facciamo bene e poi la mostriamo"); aspettare la perfezione per paura del giudizio. Ricorda: l'MVP deve poter sembrare imbarazzante.

**Chiusura:** completa `assets/scheda-esperimento.md` con il piano dell'MVP e la data del primo dato. Passa alla Fase 4 quando i dati arrivano.

---

## Fase 4 — Measure

**Cosa ottenere:** leggere i dati dell'esperimento con **cohort analysis** e, se serve, **split test**, dentro l'**innovation accounting**.

**Domande:**
- Cosa hanno *fatto* le persone, non cosa hanno detto? (i comportamenti battono le opinioni)
- Guardando le coorti nel tempo, il comportamento migliora coorte dopo coorte o è piatto?
- Il risultato supera la soglia di successo che avevamo fissato in Fase 2?
- C'è una spiegazione causale, o è rumore / effetto di qualcos'altro?

**Errori comuni:** leggere totali cumulati invece di coorti; attribuire a una feature un miglioramento che potrebbe venire da altro (senza split test); spostare la soglia a posteriori.

**Chiusura:** scrivi la lettura dei risultati nella scheda-esperimento. Passa alla Fase 5.

---

## Fase 5 — Learn: pivot or persevere

**Cosa ottenere:** decidere con lucidità. Tenere un **pivot-or-persevere meeting**.

**Domande:**
- Gli esperimenti recenti stanno spostando le metriche verso il modello, o ristagnano nonostante gli sforzi?
- Quanti esperimenti abbiamo già fatto su questa ipotesi? (molti esperimenti senza progresso = segnale di pivot)
- Se dovessimo pivotare, cosa di ciò che abbiamo imparato terremmo?
- Quale dei 10 tipi di pivot descrive il cambiamento? (vedi catalogo in `metodo-lean-startup.md`)

**Inquadramento:** il pivot non è un fallimento, è uno strumento. La runway reale è quanti pivot restano possibili. Aiuta la persona a non viverlo come sconfitta.

**Chiusura:** compila `assets/pivot-or-persevere.md` con la decisione e la motivazione basata sui dati. Se "persevera" → torna in Fase 2/3 con il prossimo esperimento. Se "pivota" → torna in Fase 1 con la nuova ipotesi. Se c'è product-market fit solido → Fase 6.

---

## Fase 6 — Accelerate

**Cosa ottenere:** crescere mantenendo agilità. Identificare il **motore di crescita dominante** e presidiarne le metriche; lavorare in **small batches**; usare i **Five Whys** sulle cause radice.

**Domande:**
- Da dove arrivano davvero i nuovi clienti: restano e si accumulano (sticky), si portano dietro altri (virale), o li compri con margine positivo (paid)?
- Qual è la metrica chiave di quel motore? (churn/retention; coefficiente virale; LTV/CAC)
- Stiamo rilasciando in lotti piccoli e frequenti o in "big bang"?
- Quando qualcosa si rompe ripetutamente, abbiamo cercato la causa radice o solo messo pezze?

**Chiusura:** dichiara il motore di crescita scelto e le 1-2 metriche da presidiare. Imposta la cadenza dei pivot-or-persevere meeting per non smettere di imparare mentre si cresce.
