# Registro dei movimenti economici

**Il registro vive su Google Fogli**, così entrambi i soci lo aggiornano dal telefono, in diretta.

| | |
|---|---|
| 📊 **Foglio** | <https://docs.google.com/spreadsheets/d/1wyF1UJlqBcketwvZFwduXyAL3FsJajz-aPqYKOPWxIU/edit> |
| 📁 Cartella Drive | <https://drive.google.com/drive/folders/1pi-At6vpQarCtofPGBuuYgX3fke82UGR> |
| Proprietario | Account Google del firmatario |
| Accesso | Da condividere con il secondo socio in **modifica** |
| Versione originale Excel | Nella cronologia git (commit `59e1b27`), utile come modello di riserva |

> Il foglio è la **fonte unica** dei numeri del progetto. Questa pagina spiega come usarlo.
> Se un numero è nella repo ma non nel foglio, vale il foglio.

---

## I quattro fogli

| Foglio | Cosa contiene | Chi ci scrive |
|---|---|---|
| **Istruzioni** | Guida breve | Nessuno |
| **Parametri** | Numeri base (36 ospiti, 2.000 €, 80/20, 50/50) e **stime dei costi** per ospite | Solo qui si cambiano i numeri di base |
| **Movimenti** | **Il registro**: una riga per ogni movimento reale | Entrambi i soci |
| **Riepilogo** | Effettivo vs atteso, margine, ripartizione 50/50, cassa | Nessuno: si calcola da solo |

## Come si registra un movimento

1. Apri **Movimenti**, vai alla prima riga vuota.
2. Compila **solo le colonne A–F**. La colonna **G (Saldo progressivo)** si calcola da sola: non scriverci dentro.
3. **Importo sempre positivo**, anche per i costi. Il segno lo decide il *Tipo movimento*.
4. **Tipo movimento** e **Categoria** solo dai **menu a tendina**. Il Riepilogo somma su quei valori esatti: un testo scritto a mano, anche con una lettera diversa, non viene conteggiato.
5. Registra quando **il denaro si muove davvero** (incasso o pagamento), non quando si emette la fattura.
6. Sono pronte **80 righe**. Se finiscono: seleziona l'ultima cella della colonna G e trascinala in basso. Il Riepilogo legge fino alla riga 1000, quindi le righe aggiunte vengono conteggiate.

### Colonne

| Colonna | Contenuto |
|---|---|
| A · Data | Giorno in cui il denaro si è mosso |
| B · Tipo movimento | `Incasso` · `Costo` · `Distribuzione` |
| C · Categoria | `Tranche 80%` · `Tranche 20%` · `Altro incasso` · `Alloggio` · `Transfert` · `Mobility` · `Altro costo` · `Distribuzione Socio 1` · `Distribuzione Socio 2` |
| D · Descrizione | Testo libero: fattura, fornitore, cosa |
| E · Riferimento | A cosa si riferisce il movimento — vedi tabella sotto |
| F · Importo (€) | Numero positivo |
| G · Saldo progressivo (€) | **Calcolato.** Incasso somma; Costo e Distribuzione sottraggono |

### Cosa scrivere in "Riferimento"

Risponde alla domanda *"questo movimento a cosa si riferisce?"*, così tra sei mesi si capisce ancora.

| Movimento | Cosa scrivere | Esempio |
|---|---|---|
| Incasso dalla capofila | Tranche e numero di ospiti | `Tranche 80% — 36 ospiti` |
| Costo di alloggio | Struttura e camere/ospiti | `Struttura X — 12 camere singole` |
| Costo di transfert o mobility | Gruppo e data | `Bus arrivo 01/03 — 36 ospiti` |
| Costo legato a una sola persona | Codice dell'ospite | `Ospite 07 — rientro anticipato` |
| Distribuzione | Quale socio | `Socio 1 — acconto` |

> Nel foglio caricato il 14/09 l'intestazione della cella **E1** riporta ancora la dicitura
> precedente ("Ospite / Tranche di riferimento"): va sostituita a mano con **Riferimento**.
> È solo un'etichetta, nessuna formula dipende da quel testo.

### I tre tipi di movimento

| Tipo | Significato | Effetto sul saldo | Effetto sul margine |
|---|---|---|---|
| **Incasso** | Denaro che entra (tranche dalla capofila) | + | + |
| **Costo** | Denaro che esce verso fornitori | − | − |
| **Distribuzione** | Prelievo di un socio sulla sua quota | − | **nessuno** — non è un costo |

## Parametri: cosa toccare e cosa no

> I colori qui sotto sono quelli del **tema chiaro**. Con il tema scuro (es. iPad di notte)
> Google li adatta e "nero" diventa bianco: fa fede il foglio *Istruzioni*, non la tonalità.

- **Blu** = inserito a mano, si può cambiare (ospiti, prezzo, quote).
- **Giallo** = manca ancora. Oggi: le tre **stime di costo per ospite** (alloggio, transfert, mobility). Finché sono vuote, il *margine atteso* nel Riepilogo è pari al ricavo lordo, cioè **sovrastimato per costruzione**.
- **Nero** = formula. Non sovrascrivere.
- **Verde** = riferimento a un altro foglio.

## Il controllo che va fatto ogni tanto

In **Riepilogo**, la riga *"Verifica vs ultimo saldo progressivo"* deve coincidere con l'ultimo valore della colonna G in *Movimenti*. Sono due percorsi di calcolo diversi che devono dare lo stesso numero. **Se divergono**, una riga ha Tipo o Categoria scritti a mano invece che scelti dal menu.

## Backup

Una volta al mese, o dopo un movimento importante: *File → Scarica → Excel* e salva il file in
[`../allegati/`](../allegati/) come `AAAA-MM-GG-movimenti-backup.xlsx`. Costa trenta secondi e
mette al riparo da cancellazioni accidentali.
