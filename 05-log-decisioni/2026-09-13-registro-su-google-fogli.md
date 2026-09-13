# 2026-09-13 · Registro movimenti spostato su Google Fogli

- **Stato:** ✅ Attiva
- **Decisa da:** Firmatario
- **Sostituisce:** parte della decisione [2026-09-12 struttura repository](2026-09-12-struttura-repository.md) (il registro come file Excel nella repo)
- **Sostituita da:** —

## Contesto

Il registro dei movimenti era un file Excel dentro la repository. Per aggiornarlo andava
scaricato, aperto e ricaricato; due soci che modificano lo stesso file binario non hanno
modo di unire le versioni.

## Decisione

Il registro diventa un **Google Foglio** nella cartella Drive condivisa "Progetto GEM".
Nella repository resta [`04-pagamenti/movimenti-economici.md`](../04-pagamenti/movimenti-economici.md)
con il link e la guida d'uso. Le formule, i menu a tendina e i quattro fogli sono gli stessi
della versione Excel; la versione Excel resta nella cronologia git come modello di riserva.

## Motivazione

Aggiornamento in diretta dal telefono, da parte di entrambi, senza scaricare nulla.
Per un registro compilato a mano nell'arco di mesi conta più della coerenza "tutto in un posto".

## Conseguenze

- Il foglio va **condiviso in modifica** con il secondo socio.
- Backup mensile in `allegati/` (File → Scarica → Excel).
- Il foglio ha 80 righe pronte; il Riepilogo legge fino alla riga 1000.
- Ogni riferimento nella repo al file `.xlsx` è stato aggiornato al nuovo documento.
