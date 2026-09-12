# 2026-09-12 · Struttura della repository e impostazione del tracciamento

- **Stato:** ✅ Attiva
- **Decisa da:** Firmatario
- **Sostituisce:** —
- **Sostituita da:** —

## Contesto

Il progetto GEM è in trattativa con la capofila spagnola. Le condizioni economiche sono
state concordate **a voce** e non esiste documentazione scritta strutturata. Serve un
punto unico dove tenere traccia di trattativa, contratto, logistica, pagamenti e decisioni.

## Decisione

Repository di sola documentazione, senza backend né codice applicativo:

- Knowledge base in **Markdown**, organizzata **per fasi** (`01-` … `05-`).
- Un **README principale** che riflette solo lo **stato corrente**, senza storico duplicato.
- Uno **storico immutabile** delle decisioni in `05-log-decisioni/`.
- Un unico file **`04-pagamenti/movimenti-economici.xlsx`** per tutti i movimenti economici,
  aggiornato **manualmente**.

## Motivazione

- Le fasi hanno tempi diversi e devono poter essere aggiornate **in modo indipendente**.
- Separare "stato corrente" da "storico" evita il problema tipico dei documenti unici,
  che diventano illeggibili e in cui non si capisce più cosa vale oggi.
- L'Excel resta lo strumento giusto per i numeri: già noto, ricalcola da solo, apribile
  da chiunque senza strumenti aggiuntivi.
- Nessuna automazione: il volume di movimenti è basso e il costo di manutenzione di un
  automatismo supererebbe il beneficio.

## Conseguenze

- Ogni movimento economico va inserito **a mano**: se non si inserisce, il quadro è falso.
- Il README va aggiornato a ogni cambiamento di stato, altrimenti perde la sua funzione.
- I file di log non vanno mai riscritti.
