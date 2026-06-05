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

[MIT](LICENSE) © 2026 Fabio Alessi (PopUp.it)
