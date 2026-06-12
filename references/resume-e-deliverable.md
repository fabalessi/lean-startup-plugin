# Resume ("riprendi da dove hai lasciato") + Deliverables Hub

Due capacità che rendono i cruscotti un vero punto di ripartenza, non solo una fotografia. Il **Resume** fa ripartire il founder esattamente da dove aveva lasciato; il **Deliverables Hub** raccoglie in un posto tutto ciò che è stato prodotto, con stato e link. Vanno insieme: il conteggio "Da rivedere" del Resume sono i deliverable in attesa di conferma.

## Indice
1. Il protocollo Resume (comportamento)
2. La Resume bar (UI nel cruscotto)
3. resume-snapshot.json (schema)
4. Deliverables Hub (vista)

---

## 1. Il protocollo Resume (comportamento)

"Riprendi" prima ancora che un bottone è un **comportamento del coach**. Quando il founder dice *"riprendi"*, *"riprendi da dove eravamo"*, *"dove eravamo con [startup]"* o apre la giornata dopo una pausa, esegui questi passi in ordine:

1. **Leggi lo stato reale.** Apri la fonte di verità: la Task list dello sprint, i deliverable (con i loro stati), l'ultimo End-of-Day Check / Daily Briefing. Da qui ricavi i contatori: focus/priorità aperte, quante cose *Da rivedere*, quante in *scadenza/overdue*.
2. **Ritrova il filo dalle ultime chat.** Individua le ultime conversazioni sull'argomento e riassumi in 2-3 righe *dove eravate rimasti* e cosa era stato deciso. (Se è disponibile uno strumento per elencare/leggere le sessioni recenti, usalo per trovare le chat pertinenti; altrimenti basati sui deliverable e sull'ultimo EOD.) Mostra al founder i titoli/momenti di quelle chat così può riaprirle.
3. **Guarda piano e scadenze.** Confronta lo stato con lo sprint corrente e le date: elenca cosa è *in scadenza oggi*, cosa è *overdue*, e cosa è *Da rivedere* (aspetta una sua conferma per sbloccare il resto).
4. **Riparti con il prossimo passo concreto.** Proponi **il** prossimo task giusto: la priorità più alta sbloccata, coerente con l'obiettivo dello sprint. Se è auto-eseguibile, parti subito; altrimenti formula una domanda binaria con un default consigliato. Niente riepiloghi lunghi: l'obiettivo è rimettere in moto, non rifare la storia.

Principio: il Resume risponde a *"cosa faccio adesso"*, ancorato a piano e scadenze, non *"ecco tutto quello che è successo"*.

---

## 2. La Resume bar (UI nel cruscotto)

Una barra in cima al **Cockpit** (e opzionalmente alle altre viste) che materializza il protocollo. Contiene:

- **Titolo + sub** — "📍 Riprendi [Startup]" e una riga con fonte e data dell'ultimo aggiornamento.
- **Contatori** — *Focus/priorità aperte*, *Da rivedere*, *In scadenza/overdue*. Colorati: rosso se >0 su overdue/priorità, giallo su da rivedere.
- **Bottone "▶ Riprendi da dove hai lasciato"** — costruisce il prompt di resume (i contatori + la lista "Da rivedere" + i 4 passi del protocollo) e lo **invia alla chat** se l'ambiente lo consente (`sendPrompt(...)` o `window.cowork`), altrimenti lo **copia negli appunti** con un toast "Prompt copiato: incollalo in chat". Così funziona sia dentro Cowork sia aprendo l'HTML offline.
- **Lista "Da rivedere ora"** — espandibile, i deliverable/task in attesa di conferma, con priorità e flag overdue.

Comportamento dati a cascata (così la barra funziona sempre, anche via `file://`): parte da uno **snapshot embedded** nel file → se presente prova a leggere `resume-snapshot.json` → se è dentro Cowork prova i dati live via MCP. Ogni livello che riesce sovrascrive il precedente.

---

## 3. resume-snapshot.json (schema)

La fonte di verità leggera della Resume bar. Viene riscritta a ogni Daily Briefing / EOD (manuale o pianificato).

```json
{
  "updatedAt": "2026-06-03 09:00",
  "source": "Daily Briefing",
  "focus": 2,
  "review": 3,
  "overdue": 1,
  "list": [
    { "taskId": "exp-attivazione", "task": "Bozze precaricate — esperimento attivazione", "prio": "P0", "over": false },
    { "taskId": "copy-onboarding", "task": "Copy onboarding (da confermare)", "prio": "P1", "over": false },
    { "taskId": "canale-community", "task": "Setup test canale community", "prio": "P1", "over": true }
  ]
}
```

`focus` = priorità aperte/P0; `review` = quante "Da rivedere"; `overdue` = quante oltre scadenza; `list` = le voci da mostrare nell'espandibile.

---

## 4. Deliverables Hub (vista)

Stessa idea dell'hub deliverable usato in progetti reali: **un posto solo dove vedere tutto ciò che è stato prodotto**, filtrabile per categoria e per stato, ogni voce con il link al file. Diventa la sesta vista del set (cross-nav: Cockpit · Ipotesi · Metriche · Runway · Cadenza · Deliverables).

**Campi di un deliverable:** titolo · categoria (es. Validazione, Prodotto, Pitch, Ops, Marketing) · **consegnato da** (nome dell'agente o della persona che l'ha prodotto) · **stato** · data · **link** al file · (opz.) nota / tipo.

**Stati canonici** (coerenti con la Task list):
- **Bozza** — prima stesura.
- **In corso (WIP)** — in lavorazione.
- **Da rivedere** — pronto, in attesa di conferma del founder. (Alimenta il contatore del Resume.)
- **Confermato** — approvato, è una base solida su cui costruire.
- **Bloccato** — fermo, in attesa di un input/decisione.
- **Archiviato** — superato, tenuto per storia.

**Interazione stato (Da rivedere ⇄ Confermato).** Per i deliverable in questi due stati la cella di stato mostra **due bottoni interscambiabili** — "Da rivedere" e "Confermato" — così il founder cambia stato con un clic:
- Quando un deliverable è **Da rivedere**, accanto ai bottoni compare **▶ Lancia revisione**: genera e invia (o copia) un **prompt di revisione** — apri il file, verificalo contro l'obiettivo dello sprint e i criteri di qualità, elenca cosa correggere, e concludi proponendo «Confermare» o «Rimandare con modifiche». È così che il founder fa partire la review dall'hub.
- Quando lo si imposta su **Confermato**, il deliverable **esce dalla vista «Attivi» e non si vede più** lì: resta solo nella tab **Confermato**. La vista di default è «Attivi» (tutto tranne Confermato e Archiviato), con un avviso di quanti confermati sono nascosti. Promuovere a Confermato richiede sempre l'ok del founder, non automatizzarlo.

**Funzioni della vista:** filtri per categoria e per stato in cima (default «Attivi»); colonna **Consegnato da**; i deliverable in "Da rivedere" sono gli stessi che la Resume bar conta e mette in cima.

**Document Viewer (integrato).** Cliccando il nome del deliverable (o "📄 apri") si apre un **viewer a comparsa** (slide-over) che mostra il **contenuto del documento reso a video** — titoli, liste, tabelle, citazioni, grassetti — senza uscire dal backend. Funziona **offline**: il contenuto Markdown dei deliverable è **embedded** nell'app (una mappa `DOCS` titolo→markdown, riscritta quando i file cambiano), reso da un piccolo renderer Markdown inline; quando l'app gira servita via http o dentro Cowork, in alternativa può leggere i file dalla fonte. Dal viewer, per i deliverable in *Da rivedere*, sono disponibili anche **▶ Lancia revisione** e **✓ Conferma** (che li sposta in Confermato e li toglie dalla vista Attivi). Così l'hub non è solo un elenco con link: è il posto dove **leggi e approvi** i documenti.

**Come la skill la costruisce:** tieni la lista dei deliverable in un array nella sorgente (o in un `.json`), un oggetto per file prodotto dalle fasi (con `consegnato da` valorizzato: agente o persona), e rendila con i componenti del template (`assets/dashboard-template.html`), inclusi i bottoni toggle e il bottone di revisione. Aggiorna lo stato man mano: una bozza diventa "Da rivedere" quando è pronta, "Confermato" solo dopo l'ok del founder.
