# Ritmo operativo — Sprint, Daily Briefing, End-of-Day Check, Task list

Questa è la parte "gestione dell'operatività" della skill: il ritmo con cui un founder porta avanti il lavoro giorno per giorno senza perdere il filo del metodo. È annidata: lo **Sprint** è il contenitore (un ciclo di 1-2 settimane attorno a un esperimento), dentro ci sono i due rituali quotidiani (**Daily Briefing** all'avvio, **End-of-Day Check** alla chiusura) e la **Task list** che alimenta entrambi. Tutto si rende nei cruscotti (vista Cadenza) ma vive anche come output in chat. Per il contesto generale dei cruscotti vedi `cruscotti-operativi.md`.

```
SPRINT (1-2 settimane, 1 obiettivo legato a un esperimento)
 ├─ Daily Briefing      → ogni mattina: cosa conta oggi
 ├─ Task list           → il backlog dello sprint (stati + link)
 └─ End-of-Day Check    → ogni sera: cosa è chiuso, cosa resta (carry-forward)
   └─ Sprint Review      → a fine sprint: coincide con il pivot-or-persevere
```

## Indice
1. Sprint
2. Daily Briefing
3. End-of-Day Check
4. Task list (stati + link)
5. Come la skill li usa

---

## 1. Sprint

Lo **sprint** è l'unità di tempo del lavoro: un ciclo breve (consiglio: **1 o 2 settimane**) con **un solo obiettivo dominante**, sempre legato a far avanzare un esperimento o un'ipotesi. È la traduzione operativa del principio degli *small batches*: cicli corti, feedback rapido, correzione prima di accumulare errori.

Uno sprint ben fatto ha:
- **Obiettivo dello sprint** — una frase, legata alla riskiest assumption del momento ("portare l'attivazione 2ª settimana sopra il 75%"). Non una lista di cose, un risultato.
- **Durata e numero** — es. "Sprint 3 · 3-16 giu · giorno 4/10".
- **Backlog dello sprint** — i task confermati per raggiungere l'obiettivo (la Task list, §4).
- **Definition of done** — cosa significa "sprint riuscito": di norma *un esperimento completato con un dato*, non *task spuntati*.
- **Sprint Review** — a fine sprint coincide con il **pivot-or-persevere meeting**: si guarda il dato, si decide. (vedi `metodo-lean-startup.md` → pivot)

Regola anti-deriva: **un solo obiettivo per sprint**. Se ne servono due, sono due sprint. Lo sprint non è un contenitore di task qualsiasi: è il veicolo di un giro del loop Build-Measure-Learn.

---

## 2. Daily Briefing

Output di **avvio giornata** (in chat e/o pannello nella vista Cadenza). Serve a far partire il founder sapendo l'unica cosa che conta oggi, non a elencare tutto. Tienilo corto: si legge in 30 secondi.

**Formato:**
- **Data + sprint** — "Mar 9 giu · Sprint 3, giorno 4/10".
- **Stato del segnale** — NSM (valore vs soglia, colore), runway (mesi + pivot residui), esperimento attivo (giorni al primo dato). Sono gli stessi numeri del Cockpit.
- **Focus di oggi** — le 1-3 task **Confermate** o **In corso** che spingono l'obiettivo dello sprint. Solo quelle.
- **Alert** — kill-line vicine, decisioni in scadenza, rischi critici. Solo se ce ne sono.
- **In attesa di te** — eventuali task **Da rivedere** che aspettano una conferma del founder per sbloccarsi.

Principio: il briefing punta sempre all'obiettivo dello sprint. Se una task non serve a quell'obiettivo, oggi non è "focus".

---

## 3. End-of-Day Check

Output di **chiusura giornata** (in chat e/o pannello). È il momento di accountability: cosa è successo davvero e cosa sopravvive a domani (il *carry-forward*).

**Formato:**
- **Chiuso oggi** — task passate a **Fatto** (con link).
- **Dati nuovi** — qualunque numero raccolto oggi che muove una metrica o un'ipotesi (es. "+3 dev attivati, attivazione coorte 3 a 77%"). È qui che si aggiorna la fonte di verità.
- **Da rivedere → in attesa di conferma** — task arrivate a **Da rivedere** che il founder deve confermare o rimandare.
- **Carry-forward** — cosa resta aperto e si trascina a domani, con owner e scadenza.
- **Blockers** — cosa ha bloccato, e (se ricorrente) un mini *Five Whys* sulla causa radice invece di una pezza.
- **Setup per domani** — la prima cosa da fare all'avvio, così il briefing di domani parte già puntato.

Principio: l'EOD non misura quanto si è stati impegnati, ma **cosa si è imparato e cosa è ancora aperto**. Niente success theater.

---

## 4. Task list (stati + link)

La task list è il backlog operativo, di norma quello dello sprint corrente. Ogni task ha uno **stato** e un **link** alla cosa a cui si riferisce (deliverable, esperimento, documento, fonte). Il link è obbligatorio quando esiste un artefatto: rende la task verificabile e collega il lavoro alla fonte di verità.

**Stati canonici** (in ordine di flusso):
- **Da fare** — nel backlog, non iniziata.
- **In corso** — qualcuno ci sta lavorando ora.
- **Da rivedere** — completata ma **in attesa di conferma** del founder (è lo stato-cerniera: il lavoro c'è ma non è ancora validato). Chip giallo.
- **Confermato** — rivista e approvata dal founder: è "buona", può sbloccare ciò che dipende da lei. Chip verde-bordato.
- **Fatto** — chiusa e archiviata. Chip verde.

**Campi di una task:** descrizione · owner · scadenza · **stato** · **link** · (opz.) cosa sblocca.

**Perché "Da rivedere" e "Confermato" separati:** in una startup molto del lavoro lo produce qualcuno (o un agente) e il founder deve dare l'ok prima che diventi base per il passo dopo. "Da rivedere" segnala *pronto ma non ancora tuo*; "Confermato" segnala *approvato, costruisci sopra*. Tenere i due stati distinti evita di trattare come definitivo qualcosa che il founder non ha ancora guardato. Il Daily Briefing pesca da Confermato/In corso; l'EOD raccoglie i nuovi Da rivedere e li mette in attesa.

---

## 5. Come la skill li usa

- **Genera lo sprint** quando si avvia un esperimento (di norma in Fase 2-3): obiettivo legato all'ipotesi, durata, backlog iniziale di task.
- **Produci il Daily Briefing** quando il founder apre la giornata o chiede "cosa faccio oggi"; **l'EOD Check** a fine giornata o su richiesta. Entrambi corti, puntati sull'obiettivo dello sprint.
- **Tieni la Task list** come backlog dello sprint, aggiornando stati e link; rispetta la cerniera Da rivedere → Confermato (non promuovere a Confermato senza l'ok del founder).
- **Rendi tutto nei cruscotti**: nella vista Cadenza metti la sezione **Sprint** (obiettivo, giorno X/N, review), la **Task list** e i pannelli **Briefing**/**EOD**. Usa i componenti del template (`assets/dashboard-template.html`).
- **Offri di automatizzarli**: se il founder vuole, briefing al mattino ed EOD alla sera possono diventare attività ricorrenti pianificate (una al mattino, una a fine giornata). Proponilo, non darlo per scontato.
- **Chiudi lo sprint con la Sprint Review** = pivot-or-persevere sul dato dell'esperimento, poi apri lo sprint successivo.
