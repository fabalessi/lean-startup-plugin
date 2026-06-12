# Lancio Startup Lean — Lean OS for founders

🇬🇧 English · [🇮🇹 Italiano](#-italiano)

> A coaching skill for Claude (Cowork / Claude Code) that walks you through launching a startup with Eric Ries' **Lean Startup** method — and builds the **operational backend** to run it. Output in Italian, offline, rebrandable.

**Tagline:** turn your idea into hypotheses to validate, not a business plan to execute blindly.

---

## What it's for

Most startups don't die because they execute the plan badly — they die because they execute the wrong plan perfectly, building something nobody wants. This skill makes you work the other way around: progress isn't measured in features shipped or documents written, but in **validated learning** — learning proven with data from real customers. It coaches you to find out, as fast as possible, whether you *should* build what you have in mind.

## How it works

It's not a form filler. It's a conversational coach.

1. **It figures out where you are.** First thing it asks (or infers): do you have just an idea, a few customers already, or a product that won't grow? It enters at the right phase instead of restarting from zero.
2. **It asks the questions of that phase.** A few targeted questions at a time; it listens and distills your answers into the phase deliverable.
3. **It produces concrete artifacts.** Every closed phase saves a real document in your project folder.
4. **It protects you from the classic mistakes.** It blocks *vanity metrics*, pushes toward the smallest possible MVP, and treats the pivot as a tool, not a failure.

## When it triggers

"I want to launch a startup", "validate an idea", "is my idea working?", "build an MVP", "customer validation", "which metrics should I use", "should I pivot?" — even without saying "lean startup". Also on: dashboard / cockpit, sprint, morning briefing, task list, deliverables, "resume / where were we".

## The 7 phases (and what they produce)

1. **Framing & vision** → vision + problem/customer sheet.
2. **Risky assumptions & Lean Canvas** → assumptions register ranked by risk + Lean Canvas, with the *riskiest assumption* flagged.
3. **What to learn & metrics** → experiment sheet (hypothesis, actionable metric, success threshold, baseline).
4. **MVP** → the right MVP type (concierge, Wizard of Oz, video, smoke test) and the plan to build it.
5. **Measure** → cohort-based reading of the data vs. threshold (innovation accounting).
6. **Learn: pivot or persevere** → the decision, and if needed the pivot type from the catalog of 10.
7. **Accelerate** → the dominant engine of growth (sticky / viral / paid) and the metrics to watch.

## The operational backend — "Lean OS"

When there's real data to watch, the skill builds a **single-page backend** (sidebar + views, self-contained, offline, rebrandable via tokens):

- **Cockpit** — North Star vs. threshold, runway (in months *and* in remaining pivots), active experiment, hypotheses ledger.
- **Resume bar "▶ Pick up where you left off"** — reads the current state, recovers the thread from recent chats, checks plan and deadlines, proposes the next concrete step.
- **Hypotheses · Metrics · Runway** — the drill-down views (kill-lines, cohorts, capital).
- **Cadence** — Sprint, Daily Briefing, End-of-Day Check, Task list (with *To review* / *Confirmed* states + links).
- **Deliverables Hub** — everything produced, with a *Delivered by* column, To review⇄Confirmed toggle, and *▶ Launch review*.

Non-negotiable dashboard principles: no vanity metrics in the main indicators, every number paired with its threshold and a color state, runway also measured in pivots, a single source of truth that the HTML merely renders.

## What's in the package

- `SKILL.md` — the coach: flow, 7 phases, conduction rules.
- `references/` — `metodo-lean-startup.md` (definitions, MVP types, the 10 pivots, the 3 engines), `fasi-coaching.md` (questions and common mistakes per phase), `cruscotti-operativi.md` (dashboard directive), `ritmo-operativo.md` (sprint/briefing/EOD/tasks), `resume-e-deliverable.md` (resume protocol + deliverables hub), `lean-canvas-obsidian.md` (Obsidian install procedure).
- `assets/` — 4 document templates (hypotheses register, lean canvas, experiment sheet, pivot-or-persevere) + `dashboard-template.html` (the backend app-shell) + `obsidian-lean-canvas/` (the visual canvas for Obsidian).

## Extra: visual Lean Canvas for Obsidian

`assets/obsidian-lean-canvas/` ships a ready-to-use Lean Canvas template for Obsidian: 9 Markdown files (one per block) composed by a `.canvas` file in the classic canvas layout. Derived from [YJPL/lean-canvas-for-obsidian](https://github.com/YJPL/lean-canvas-for-obsidian) (MIT). Just ask "install the lean canvas in Obsidian": the skill locates your vault, copies the files and fixes the paths. Full procedure in `references/lean-canvas-obsidian.md`. Only requires Obsidian's core **Canvas** plugin (on by default).

## Requirements & notes

- **Language:** coaching output is in Italian.
- **Offline:** dashboards are self-contained HTML, no network dependencies.
- **Domain-agnostic:** software, physical product, marketplace, service, internal innovation.
- **Resume is stronger inside Cowork:** there it can list recent chats on the topic and send prompts directly; opened standalone, the HTML buttons copy the prompt to paste in chat.

## Installation

- **Claude Cowork / Claude.ai:** zip this folder with a `.skill` extension and upload it from *Settings → Capabilities*, or use the `.skill` release if available.
- **Claude Code:** copy the folder into your project's `.claude/skills/`.

## License

MIT — see [LICENSE](LICENSE). The embedded Obsidian template is derived from YJPL/lean-canvas-for-obsidian, also MIT.

---

# 🇮🇹 Italiano

> Un coach che ti accompagna a lanciare una startup col metodo **Lean Startup** di Eric Ries, e ti costruisce il **backend operativo** per gestire tutto. In italiano, offline, ribrandizzabile.

**Tagline:** trasforma l'idea in ipotesi da validare, non in un business plan da eseguire alla cieca.

## A cosa serve

La maggior parte delle startup non muore perché esegue male il piano, ma perché esegue benissimo il piano sbagliato — costruisce con successo qualcosa che nessuno vuole. Questa skill ti fa lavorare al contrario: il progresso non si misura in feature costruite o documenti scritti, ma in **validated learning** (apprendimento dimostrato con dati di clienti veri). Ti fa da allenatore per scoprire, il più in fretta possibile, *se devi* costruire quello che hai in mente.

## Come funziona (il flusso)

Non è un compilatore di moduli: è un coach conversazionale.

1. **Capisce a che punto sei.** Prima cosa ti chiede (o deduce) se hai solo un'idea, già qualche cliente, o un prodotto che non cresce — ed entra nella fase giusta, non riparte sempre da zero.
2. **Ti fa le domande della fase.** Poche domande mirate alla volta; ascolta e sintetizza le risposte nel deliverable di quella fase.
3. **Imposta il lavoro e produce gli artefatti.** A ogni fase chiusa salva un documento concreto nella tua cartella.
4. **Ti difende dagli errori classici.** Blocca le *vanity metrics*, spinge verso l'MVP più piccolo, tratta il pivot come strumento e non come fallimento.

## Quando si attiva

"Voglio lanciare una startup", "validare un'idea", "capire se la mia idea funziona", "costruire un MVP", "fare customer validation", "che metriche uso", "devo pivotare?" — anche senza dire "lean startup". E su: dashboard / cockpit / cruscotto, sprint, briefing del mattino, lista task, deliverable, "riprendi / dove eravamo".

## Le 7 fasi (e cosa producono)

1. **Inquadramento & vision** → vision + scheda problema/cliente.
2. **Ipotesi rischiose & Lean Canvas** → registro ipotesi ordinate per rischio + Lean Canvas, con la *riskiest assumption* evidenziata.
3. **Cosa imparare & metriche** → scheda esperimento (ipotesi, metrica actionable, soglia di successo, baseline).
4. **MVP** → il tipo di MVP giusto (concierge, Wizard of Oz, video, smoke test) e il piano per costruirlo.
5. **Measure** → lettura dei dati per coorte vs soglia (innovation accounting).
6. **Learn: pivot or persevere** → la decisione, e se serve il tipo di pivot dal catalogo dei 10.
7. **Accelerate** → il motore di crescita dominante (sticky / virale / paid) e le metriche da presidiare.

## Il backend operativo — "Lean OS"

Quando ci sono dati da presidiare, la skill costruisce un **vero backend a pagina singola** (sidebar + viste, self-contained, offline, ribrandizzabile dai token):

- **Cockpit** — North Star vs soglia, runway (in mesi *e* in pivot residui), esperimento attivo, ledger ipotesi.
- **Resume bar "▶ Riprendi da dove hai lasciato"** — analizza lo stato, ritrova il filo dalle ultime chat, guarda piano e scadenze, propone il prossimo passo.
- **Ipotesi · Metriche · Runway** — le viste di approfondimento (kill-line, coorti, capitale).
- **Cadenza** — Sprint, Daily Briefing, End-of-Day Check, Task list (stati *Da rivedere* / *Confermato* + link).
- **Deliverables Hub** — tutto il prodotto con colonna *Consegnato da*, toggle Da rivedere⇄Confermato, *▶ Lancia revisione*, confermati nascosti.

Principi non negoziabili dei cruscotti: niente vanity metrics negli indicatori, ogni numero con la sua soglia e uno stato a colori, runway anche in pivot, una sola fonte di verità di cui l'HTML è il render.

## Cosa contiene il pacchetto

- `SKILL.md` — il coach: flusso, 7 fasi, regole di conduzione.
- `references/` — `metodo-lean-startup.md` (definizioni, tipi di MVP, 10 pivot, 3 motori), `fasi-coaching.md` (domande ed errori per fase), `cruscotti-operativi.md` (direttiva dashboard), `ritmo-operativo.md` (sprint/briefing/EOD/task), `resume-e-deliverable.md` (resume + deliverables), `lean-canvas-obsidian.md` (procedura Obsidian).
- `assets/` — 4 template documentali (registro ipotesi, lean canvas, scheda esperimento, pivot-or-persevere) + `dashboard-template.html` (l'app-shell del backend) + `obsidian-lean-canvas/` (il canvas visuale per Obsidian).

## Extra: Lean Canvas visuale per Obsidian

In `assets/obsidian-lean-canvas/` la skill include un template pronto del Lean Canvas per Obsidian (9 blocchi `.md` + file `.canvas`, derivato da [YJPL/lean-canvas-for-obsidian](https://github.com/YJPL/lean-canvas-for-obsidian), MIT). Basta chiedere "installa il lean canvas in Obsidian": la skill individua il vault, copia i file e adatta i percorsi. Procedura completa in `references/lean-canvas-obsidian.md`. Richiede solo il core plugin **Canvas** di Obsidian (attivo di default).

## Requisiti & note

- **Lingua:** italiano.
- **Offline:** i cruscotti sono HTML self-contained, nessuna dipendenza di rete.
- **Generica:** software, prodotto fisico, marketplace, servizio, innovazione interna.
- **Resume più potente dentro Cowork:** lì può elencare le ultime chat sull'argomento e inviare i prompt; aprendo l'HTML da solo, i bottoni copiano il prompt da incollare in chat.

## In una frase, per chi la condivide

> *Lean OS: il copilota che porta la tua idea da "scommessa" a "imparata", e ti dà il cruscotto per gestire il lancio giorno per giorno.*

## Installazione

- **Claude Cowork / Claude.ai:** comprimi questa cartella in un archivio `.skill` (zip rinominato) e caricala da *Settings → Capabilities*, oppure usa la release `.skill` se presente.
- **Claude Code:** copia la cartella in `.claude/skills/` del progetto.

## Licenza

MIT — vedi [LICENSE](LICENSE). Il template Obsidian incluso deriva da YJPL/lean-canvas-for-obsidian, anch'esso MIT.
