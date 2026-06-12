# Direttiva — Cruscotti operativi per chi lancia una startup

Questa è la direttiva per costruire i cruscotti (dashboard) che permettono a un founder di tenere **tutto sott'occhio** e gestire l'operatività, restando coerenti con il metodo Lean Startup. Non sono report da ammirare: sono strumenti decisionali che servono i meeting settimanali e i pivot-or-persevere. Per le definizioni dei concetti vedi `metodo-lean-startup.md`; per la conduzione delle fasi vedi `fasi-coaching.md`.

## Indice
1. Gli 8 principi (la parte che conta)
2. Il set ottimale di cruscotti
3. Quale set in base allo stadio
4. Design system neutro (token + componenti)
5. Pattern di build (sorgente unica → render)
6. Come la skill costruisce i cruscotti

---

## 1. Gli 8 principi

Questi principi vengono **prima** di qualunque scelta estetica. Se un cruscotto li viola, è un bel poster inutile.

1. **Misura validated learning, non attività.** Il rischio numero uno di un founder è il *success theater*: dashboard che salgono mentre non si impara nulla. Ogni pannello deve rispondere a "cosa abbiamo imparato e cosa decidiamo", non "quanto siamo stati impegnati".

2. **Bandisci le vanity metrics dalla prima riga.** Iscritti totali, follower, download cumulati, GMV cumulato non guidano decisioni. Mettili al massimo a piè di pagina, mai negli indicatori principali. Negli indicatori vanno metriche per **coorte** e relazioni **causa-effetto** (le tre A: Actionable, Accessible, Auditable).

3. **Ogni numero ha una soglia e dice cosa fare (semaforo decisionale).** Un numero senza soglia è decorazione. Ogni KPI porta con sé la sua kill-line o il suo target, e uno stato a colori: verde = verso il modello, giallo = sotto osservazione, rosso = kill-line superata → azione. Il founder deve poter decidere senza interpretare.

4. **La runway si misura in pivot, non solo in euro.** Accanto a cassa/burn/mesi, mostra **quanti pivot/esperimenti restano possibili**. È la metrica lean della sopravvivenza e cambia il modo in cui si guarda al tempo.

5. **Una sola fonte di verità.** I dati vivono in un file sorgente (`.md` o `.json`); il cruscotto HTML è la **rappresentazione visiva** di quel file. Si aggiorna la fonte, si rigenera la vista. Mai dati scritti a mano dentro l'HTML che divergono dalla realtà.

6. **Gerarchia a colpo d'occhio.** Un **Cockpit** che aggrega il "tutto sott'occhio" in una schermata, più poche **viste di approfondimento** legate da una cross-nav. Il founder apre il Cockpit ogni mattina; entra nelle viste solo quando una luce è gialla/rossa.

7. **Cadenza incorporata.** Il cruscotto esiste per servire due rituali: il **check settimanale** (sprint di esperimenti) e il **pivot-or-persevere meeting**. Includi sempre un blocco "questa settimana" e un blocco "prossima decisione".

8. **Adatta alla forma del business.** Per un marketplace o un business a più lati, sdoppia ipotesi e metriche **per ciascun lato** (domanda e offerta separate): un lato sano e uno morto fanno una media bugiarda.

---

## 2. Il set ottimale di cruscotti

Per un founder in incertezza estrema il set giusto è **1 Cockpit + 5 viste** (Ipotesi, Metriche, Runway, Cadenza, Deliverables). Di più diventa burocrazia; di meno si perde il filo. Tutte rese da un'unica fonte e legate da cross-nav. In cima al Cockpit (e opzionalmente alle altre) sta la **Resume bar** "riprendi da dove hai lasciato" — vedi `resume-e-deliverable.md`.

### 2.0 — Cockpit (home, tutto sott'occhio)
**Scopo:** la schermata che il founder guarda ogni giorno. Aggrega il segnale, non i dettagli.
**Indicatori in cima (KPI strip):**
- **North Star Metric** — valore attuale vs soglia, con stato a colori.
- **Runway** — mesi residui **e** pivot residui.
- **Esperimento attivo** — quale ipotesi sta testando + giorni al primo dato.
- **Ledger ipotesi** — quante validate / aperte / smentite.
**Pannelli sotto:** focus della settimana (2-3 cose), alert (kill-line vicine, decisioni in scadenza, rischi critici), e un riquadro "prossima decisione pivot-or-persevere". Niente grafici pesanti qui: il Cockpit è semaforico, le viste approfondiscono.

### 2.1 — Hypothesis & Experiment Board (il motore lean)
**Scopo:** il cuore del metodo. Rende visibile il loop Build-Measure-Learn.
**Contenuto:** le leap-of-faith assumptions ordinate per rischio, ognuna con **kill-line** esplicita e stato (aperta / in test / validata / smentita). Per l'ipotesi in test, la **card esperimento**: ipotesi → metrica → tipo di MVP → criterio di successo → risultato → decisione. È la vista che alimenta la `scheda-esperimento.md`.

### 2.2 — Innovation Accounting (metriche)
**Scopo:** dimostrare che si sta imparando a costruire un business sostenibile, anche con ricavi ~0.
**Contenuto:** tabelle per **coorte** (attivazione, retention, conversione coorte dopo coorte), ciascuna con **baseline → target → attuale**; la metrica del **motore di crescita** dominante (churn/retention, coefficiente virale, oppure LTV/CAC); e una separazione netta tra metriche actionable (in alto) e vanity (relegate, segnalate come tali). Qui stanno i pochi grafici utili: trend per coorte, funnel.

### 2.3 — Runway & Capitale
**Scopo:** la sopravvivenza, in chiave lean.
**Contenuto:** cassa attuale, burn mensile, runway in mesi, **pivot residui**, soglia di allarme (a che mese scatta la decisione raise/cut), e — se previsto — il piano di raise (quanto, per fare cosa, runway post-raise). Trigger automatici evidenziati quando il burn supera le soglie.

### 2.4 — Cadenza & Operatività (sprint/calendar)
**Scopo:** trasformare il piano in settimane e dare il ritmo quotidiano.
**Contenuto:** la sezione **Sprint** (obiettivo dello sprint legato all'esperimento, giorno X/N, data della review = pivot-or-persevere); i due rituali quotidiani **Daily Briefing** e **End-of-Day Check**; la **Task list** dello sprint con stati e link; la **timeline a gate**; e i due registri di accountability: **decision log** e **risk register**. Questo è anche il "carry-forward": cosa sopravvive al cambio di giorno/settimana/sprint.
**Dettaglio:** sprint, briefing, EOD e task list (inclusi gli stati *Da rivedere* e *Confermato* e la colonna *Link*) sono definiti in `ritmo-operativo.md`. Leggi quel file quando costruisci questa vista o quando l'utente chiede un briefing, un check di fine giornata, uno sprint o una lista task.

> Nota: decision log e risk register possono stare come pannelli dentro la vista Cadenza per i team piccoli, oppure diventare una vista dedicata quando il progetto cresce.

### 2.5 — Deliverables Hub
**Scopo:** un posto solo dove vedere tutto ciò che è stato prodotto, con stato e link.
**Contenuto:** lista/tabella dei deliverable filtrabile per categoria e per stato (Bozza · In corso · Da rivedere · Confermato · Bloccato · Archiviato), ogni voce con link al file. Non duplica i contenuti, li **linka** (regola della fonte di verità unica). I deliverable in *Da rivedere* sono gli stessi che la Resume bar conta e mette in cima. Dettaglio in `resume-e-deliverable.md`.

### 2.6 — Resume bar (elemento trasversale)
Non è una vista ma una **barra** in cima al Cockpit: "📍 Riprendi [Startup]" con contatori (focus/P0, da rivedere, in scadenza), la lista "da rivedere ora" e il bottone **▶ Riprendi da dove hai lasciato**, che invia (o copia) il prompt di resume. È la materializzazione del **protocollo Resume** (leggi stato → ritrova il filo dalle ultime chat → guarda piano e scadenze → riparti col prossimo passo). Vedi `resume-e-deliverable.md`.

---

## 3. Quale set in base allo stadio

Non servono tutte e cinque dal giorno uno. Costruiscile man mano che diventano vere.

- **Solo idea (Fase 0-1):** Cockpit minimale + Hypothesis Board. Non c'è ancora nulla da contare in coorti.
- **In validazione (Fase 2-4):** aggiungi Innovation Accounting e Runway & Capitale. È il set completo, il momento in cui i cruscotti rendono di più.
- **Post product-market fit (Fase 6):** porta in primo piano la vista del **motore di crescita** dentro Innovation Accounting, e irrobustisci Cadenza con la pianificazione di crescita.

Regola: un cruscotto si crea quando c'è un dato vero da metterci, non prima. Un pannello pieno di "TBD" educa il founder a ignorare il cruscotto.

---

## 4. Design system neutro

I cruscotti generati dalla skill usano un sistema **neutro e ribrandizzabile**: stessa struttura solida delle dashboard OPS (KPI strip, card, chip di stato, cross-nav, sorgente → render), ma colori e font controllati da pochi token, così chiunque lanci una startup può adattarli al proprio brand cambiando una manciata di variabili.

### Token (CSS custom properties)
Definiscili una volta in `:root`; ribrandizzare = cambiare questi valori.

```
--bg            sfondo pagina (neutro chiaro)
--surface       superficie card (bianco)
--ink           testo primario (quasi-nero)
--muted         testo secondario
--line          hairline / bordi
--accent        colore brand primario (un solo accento forte)
--ok / --ok-bg          stato verde (verso il modello)
--warn / --warn-bg      stato giallo (sotto osservazione)
--crit / --crit-bg      stato rosso (kill-line superata)
--tbd                   stato neutro (dato mancante)
--font-sans     font UI
--font-display  font per titoli (può coincidere)
--r-card / --r-chip     raggi
```

### Componenti canonici
Riusali identici in tutte le viste per coerenza cognitiva:
- **KPI strip** — fila di 3-4 card numeriche: etichetta maiuscoletto + numero grande + sottotesto con soglia/contesto + pallino di stato.
- **Card** — contenitore base (surface, bordo `--line`, raggio `--r-card`).
- **Chip di stato** — pillola colorata: `ok` / `warn` / `crit` / `tbd`. È il vocabolario visivo del semaforo decisionale.
- **Ledger card (ipotesi)** — titolo ipotesi + riga **kill-line** evidenziata (bordo rosso a sinistra) + chip di stato.
- **Tabella coorte** — righe = coorti (es. settimana di ingresso), colonne = step funnel/tempo; celle con intensità o stato.
- **Timeline a gate** — barra orizzontale con i momenti-decisione marcati.
- **Sprint banner** — obiettivo dello sprint + giorno X/N + data review. Un solo obiettivo per sprint.
- **Task list** — descrizione, owner, scadenza, **stato** (Da fare / In corso / Da rivedere / Confermato / Fatto), **link**. Gli stati *Da rivedere* (pronto ma in attesa di conferma del founder) e *Confermato* (approvato) sono distinti apposta.
- **Pannelli Daily Briefing / End-of-Day Check** — riquadri corti per l'avvio e la chiusura della giornata.
- **Tabella accountability** — decision log / risk register: voce, fonte, owner, scadenza, sblocca, stato (chip).
- **Resume bar** — barra scura in cima al Cockpit: titolo, contatori, lista "da rivedere", bottone "Riprendi da dove hai lasciato" (invia/copia il prompt di resume).
- **Tabella Deliverables** — titolo, categoria, stato, data, link; con filtri per categoria e stato in cima.

### Regole estetiche
Stile moderno e d'impatto basato su **box a fondo colorato**: KPI e card hanno una tinta morbida (gradiente tenue) e un'ombra soffusa, con angoli ampi. La tinta segue lo **stato** — il colore ha sempre un significato: verde = verso il modello, ambra = sotto osservazione, rosso = kill-line/critico, accent (brand) = neutro/informativo. Quindi un box rosso comunica un problema, non è decorazione. Gerarchia tipografica netta: numeri grandi e in grassetto (colorati con la tinta dello stato per impatto), etichette piccole in maiuscoletto come pill. Un solo colore-brand d'accento, ribrandizzabile dai token. Elementi di forte impatto (resume bar, sprint banner, bottoni) usano un gradiente. Mobile-friendly ma pensato per desktop (il founder ci lavora).

---

## 5. Pattern di build

Il cruscotto è un **vero backend a pagina singola** ("Lean OS"), non un set di file statici separati: un'unica app con **sidebar di navigazione** a sinistra, **top bar** in alto e le viste che si commutano via JS senza reload. Dà la sensazione di un prodotto, restando self-contained.

- **App-shell single-page.** Un unico `.html` con: sidebar (logo + voci di nav con icona: Cockpit · Ipotesi · Metriche · Runway · Cadenza · Deliverables + footer founder), top bar (titolo vista + ricerca + data + avatar), e un'area contenuto con un `<div class="view">` per vista (una visibile, le altre `hidden`). Un piccolo script cambia vista al clic sulla voce di sidebar e aggiorna il titolo.
- **Self-contained, offline.** CSS e JS inline, nessuna dipendenza di rete: si apre con doppio clic, funziona senza server. (Per i grafici, SVG inline o canvas vanilla; niente CDN.)
- **Sorgente → render.** I dati vivono in un `.md`/`.json` sorgente (fonte di verità); l'app è il render. La Resume bar e la lista deliverable leggono uno snapshot embedded (riscritto a ogni Briefing/EOD) con fallback opzionale a `.json` e ai dati live MCP dentro Cowork.
- **Naming e versioning.** Un solo file app, es. `Acme_LeanOS_v1_2026-06-03.html` (o `index.html`). Data e versione in top bar/footer.
- **Parti dal template.** Usa `assets/dashboard-template.html`: è già l'app-shell completa (sidebar, top bar, le 6 viste, Resume bar, Deliverables interattivo). Ribrandizza i token in `:root`, sostituisci i `{{...}}`, riempi le viste dai deliverable delle fasi.

---

## 6. Come la skill costruisce i cruscotti

I cruscotti sono una **capacità trasversale** del coach, non una fase isolata: si attivano quando il percorso produce dati veri da presidiare (di norma da Fase 1-2 in poi). Quando il founder ha ipotesi nel registro o esperimenti in corso, proponi di materializzarle in un Cockpit + Hypothesis Board, e fai crescere il set con lo stadio (vedi §3).

Procedura:
1. **Conferma la fonte di verità.** Se la startup ha già i deliverable della skill (`registro-ipotesi.md`, `scheda-esperimento.md`, ecc.), quelli SONO la fonte: il cruscotto li rende. Altrimenti crea un breve `*-source.md` con i dati.
2. **Scegli il set** in base allo stadio (§3). Non generare viste piene di TBD.
3. **Istanzia dal template** (`assets/dashboard-template.html`), una vista alla volta, rispettando gli 8 principi — in particolare: niente vanity negli indicatori, ogni numero con soglia e stato, runway in pivot.
4. **Lega le viste** con la cross-nav e, se più d'una, crea l'`index.html` hub.
5. **Salva nella cartella del founder** così i file restano suoi, e ricorda che si rigenerano dalla fonte a ogni aggiornamento (idealmente al check settimanale e dopo ogni pivot-or-persevere).

Il cruscotto non sostituisce il pensiero: serve i due rituali (check settimanale, pivot-or-persevere) e tiene il founder onesto su cosa ha davvero imparato.
