# Lean Canvas in Obsidian — procedura di installazione

Variante visuale del Lean Canvas (Ash Maurya) per chi lavora in un vault Obsidian: 9 file Markdown (uno per blocco) composti da un file `.canvas` nel layout classico del canvas. Basata sul template open source [YJPL/lean-canvas-for-obsidian](https://github.com/YJPL/lean-canvas-for-obsidian) (MIT). Non è un plugin Obsidian: non servono manifest, release o community plugins — basta il core plugin **Canvas**, attivo di default.

## Quando usarla

In **Fase 1** del percorso, quando l'utente preferisce compilare il canvas visualmente in Obsidian invece del template tabellare `assets/lean-canvas.md`. I due formati sono equivalenti: il `.md` resta la fonte di verità testuale, il `.canvas` è la vista. Se l'utente menziona Obsidian, un vault, o chiede "il canvas visuale", proponi questa variante.

## Procedura

1. **Trova il vault.** Cerca una directory `.obsidian` nella cartella di progetto (`find <progetto> -maxdepth 3 -name ".obsidian" -type d`). Se non c'è, chiedi all'utente dove sta il vault o se vuole il solo template tabellare.
2. **Crea la sottocartella** `Lean Canvas/` nella root del vault (o dove preferisce l'utente).
3. **Copia i file** da `assets/obsidian-lean-canvas/` nella sottocartella: i 9 blocchi `.md` + `Lean Canvas.canvas`.
4. **Verifica i percorsi nel `.canvas`.** I nodi referenziano i file con percorso relativo alla root del vault: il template assume `Lean Canvas/<file>.md`. Se installi in una cartella con nome diverso, aggiorna il prefisso in ogni campo `"file"` del JSON.
5. **Apri** `Lean Canvas.canvas` in Obsidian per verificare che i 9 blocchi siano visibili e collegati.

## I 9 blocchi e l'ordine di compilazione (Maurya)

| # | File | Blocco |
|---|------|--------|
| 1 | 🤗 CUSTOMER SEGMENTS.md | Segmenti di clienti + early adopters |
| 2 | ❗️PROBLEM.md | Problema + alternative esistenti |
| 3 | 💎 UNIQUE VALUE PROPOSITION.md | UVP + high-level concept |
| 4 | 💡 SOLUTION.md | Soluzione |
| 5 | 🎯 CHANNELS.md | Canali |
| 6 | 💸 REVENUE STREAMS.md | Flussi di ricavo |
| 7 | 💰 COST STRUCTURE.md | Struttura dei costi |
| 8 | 🗝️ KEY METRICS.md | Metriche chiave |
| 9 | ✨ UNFAIR ADVANTAGE.md | Unfair advantage |

Compila i blocchi in quest'ordine, una conversazione alla volta come da Fase 1. Ogni casella è un'ipotesi: segnala con ⚠️ quelle più rischiose ancora da validare, e riporta la riskiest assumption nel `assets/registro-ipotesi.md`.

## Regole

- Non duplicare la fonte di verità: se l'utente usa il canvas Obsidian, compila i blocchi `.md` lì dentro e non mantenere in parallelo anche `assets/lean-canvas.md` compilato — scegline uno.
- I file `.md` dei blocchi sono normali note Obsidian: l'utente può linkarle dal resto del vault.
- Se l'ambiente blocca il clone diretto da GitHub, i file sono già inclusi in `assets/obsidian-lean-canvas/` — usa quelli.
