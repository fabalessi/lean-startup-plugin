*** ITA ***

# Lean OS — Lancio Startup Lean

> Una skill per Claude (Claude Code / Cowork) che ti fa da **coach Lean Startup** e ti costruisce il **backend operativo** per gestire il lancio. In italiano, offline, ribrandizzabile.

Questa repository è un **marketplace di plugin per Claude Code**: contiene il plugin `lancio-startup-lean`, installabile con un comando.

---

## Installazione (Claude Code)

```bash
# 1. Aggiungi questo marketplace (sostituisci USERNAME con il tuo handle GitHub)
/plugin marketplace add USERNAME/lean-os-startup

# 2. Installa il plugin
/plugin install lancio-startup-lean@lean-os
```

In alternativa, da un clone locale:

```bash
/plugin marketplace add ./lean-os-startup
/plugin install lancio-startup-lean@lean-os
```

Per aggiornare dopo un push: `/plugin marketplace update lean-os`.

> Cowork: puoi anche installare la skill direttamente dal file `.skill` (vedi i Release della repo), oppure copiare la cartella `plugins/lancio-startup-lean/skills/lancio-startup-lean/` tra le tue skill.

---

## Cosa fa

Non è un compilatore di moduli: è un coach conversazionale. Capisce a che punto sei, ti fa le domande della fase, e produce gli artefatti man mano. Ti porta dall'idea alle ipotesi validate in 7 fasi (vision → ipotesi & Lean Canvas → metriche → MVP → measure → pivot-or-persevere → accelerate), difendendoti dagli errori classici: vanity metrics, MVP troppo grandi, pivot vissuti come fallimenti.

Quando ci sono dati da presidiare, costruisce un **vero backend a pagina singola** (sidebar + viste, self-contained, offline):

- **Cockpit** — North Star vs soglia, runway (mesi + pivot residui), esperimento attivo, ledger ipotesi.
- **Resume bar "▶ Riprendi da dove hai lasciato"** — analizza lo stato, ritrova il filo dalle ultime chat, riparte da piano e scadenze.
- **Ipotesi · Metriche · Runway** — viste di approfondimento.
- **Cadenza** — Sprint, Daily Briefing, End-of-Day Check, Task list (stati *Da rivedere* / *Confermato* + link).
- **Deliverables Hub** — tutto il prodotto con *Consegnato da*, toggle Da rivedere⇄Confermato, *▶ Lancia revisione*.

Dettaglio completo nel [README della skill](plugins/lancio-startup-lean/skills/lancio-startup-lean/README.md).

---

## Struttura della repository

```
lean-os-startup/
├── .claude-plugin/
│   └── marketplace.json          # catalogo del marketplace "lean-os"
├── plugins/
│   └── lancio-startup-lean/
│       ├── .claude-plugin/
│       │   └── plugin.json        # manifest del plugin
│       └── skills/
│           └── lancio-startup-lean/   # la skill (SKILL.md, references/, assets/)
├── examples/
│   └── lean-os-backend-demo.html  # demo del backend (startup fittizia "Faro")
├── README.md
├── LICENSE                         # MIT
└── .gitignore
```

## Demo

Apri `examples/lean-os-backend-demo.html` nel browser: è il backend "Lean OS" popolato con una startup di esempio (dati fittizi) — sidebar, cockpit, viste, resume bar e Deliverables interattivi.

## Licenza

[MIT](LICENSE) © 2026 Fabio Alessi


*** ENG ***

# Lean OS — Lean Startup Launch

> A skill for Claude (Claude Code / Cowork) that acts as your **Lean Startup coach** and builds the **operational backend** you need to manage a startup launch. Available in Italian, works offline, and can be rebranded.

This repository is a **plugin marketplace for Claude Code** and includes the `lean-startup-launch` plugin, which can be installed with a single command.

---

## Installation (Claude Code)

```bash
# 1. Add this marketplace (replace USERNAME with your GitHub handle)
/plugin marketplace add USERNAME/lean-os-startup

# 2. Install the plugin
/plugin install lean-startup-launch@lean-os
```

Alternatively, from a local clone:

```bash
/plugin marketplace add ./lean-os-startup
/plugin install lean-startup-launch@lean-os
```

To update after pushing changes:

```bash
/plugin marketplace update lean-os
```

> Cowork: you can also install the skill directly from the `.skill` file (see the repository Releases), or copy the folder `plugins/lean-startup-launch/skills/lean-startup-launch/` into your personal skills directory.

---

## What It Does

This is not a form generator. It is a conversational coach.

It understands your current stage, asks the right questions for that phase, and progressively generates the required artifacts. It guides you from idea to validated hypotheses through seven stages:

**Vision → Hypotheses & Lean Canvas → Metrics → MVP → Measure → Pivot or Persevere → Accelerate**

Along the way, it protects you from common startup mistakes such as vanity metrics, oversized MVPs, and treating pivots as failures.

Whenever data management becomes necessary, it builds a **real single-page operational backend** (sidebar + views, self-contained, offline):

* **Cockpit** — North Star Metric vs threshold, runway (months + remaining pivots), active experiment, hypothesis ledger.
* **Resume Bar "▶ Continue where you left off"** — analyzes project status, reconstructs context from previous conversations, and resumes from the current plan and deadlines.
* **Hypotheses · Metrics · Runway** — dedicated deep-dive views.
* **Cadence** — Sprints, Daily Briefing, End-of-Day Check, Task List (statuses: *Needs Review* / *Confirmed* with links).
* **Deliverables Hub** — central repository of all project outputs with *Delivered By*, review status toggle (*Needs Review ⇄ Confirmed*), and *▶ Launch Review* action.

Full details are available in the skill's README:

`plugins/lean-startup-launch/skills/lean-startup-launch/README.md`

---

## Repository Structure

```text
lean-os-startup/
├── .claude-plugin/
│   └── marketplace.json            # "lean-os" marketplace catalog
├── plugins/
│   └── lean-startup-launch/
│       ├── .claude-plugin/
│       │   └── plugin.json         # plugin manifest
│       └── skills/
│           └── lean-startup-launch/ # skill files (SKILL.md, references/, assets/)
├── examples/
│   └── lean-os-backend-demo.html   # backend demo (fictional startup "Faro")
├── README.md
├── LICENSE                         # MIT
└── .gitignore
```

## Demo

Open `examples/lean-os-backend-demo.html` in your browser to explore the Lean OS backend populated with a sample startup (fictional data), including the sidebar, cockpit, views, resume bar, and interactive Deliverables Hub.

## License

MIT License © 2026 Fabio Alessi

