# 06 · Accordo tra soci

Documenti che regolano il rapporto **tra i due soci**, Gianluca Iaconeta e Luigi Zerulo.
Non riguardano la capofila: sono interni.

| File | Contenuto | Stato |
|---|---|---|
| [`documento-di-progetto.md`](documento-di-progetto.md) | Riassunto del progetto su cui i soci si impegnano — **Allegato A** della scrittura privata | 🟡 Bozza |
| [`scrittura-privata.md`](scrittura-privata.md) | Accordo tra i soci: ruoli, soldi, decisioni, rischi | 🟡 Bozza |

## Versioni stampabili

| PDF | Generato da |
|---|---|
| [`pdf/GEM-documento-di-progetto-v0.1.pdf`](pdf/GEM-documento-di-progetto-v0.1.pdf) | `documento-di-progetto.md` |
| [`pdf/GEM-scrittura-privata-soci-v0.1.pdf`](pdf/GEM-scrittura-privata-soci-v0.1.pdf) | `scrittura-privata.md`, **senza** commentario — la versione da firmare |
| [`pdf/GEM-scrittura-privata-soci-v0.1-con-commentario.pdf`](pdf/GEM-scrittura-privata-soci-v0.1-con-commentario.pdf) | `scrittura-privata.md`, **con** commentario — la versione da leggere |

I PDF sono **copie di lettura** con marcatura "Bozza v0.1": si rigenerano dal Markdown a ogni
versione. Le correzioni si fanno nei file `.md`, non nel PDF.

## Il commentario

Ogni articolo della scrittura privata è seguito da un blocco **💬 Commentario** che lo spiega
in parole semplici: cosa dice, perché c'è, cosa succede se manca.

Regole che lo tengono allineato al contratto:

1. **Il commento vive dentro l'articolo**, nello stesso file, subito dopo il testo. Non esiste
   un file separato: se un articolo viene tolto o rinominato, il suo commento lo segue.
2. **Non fa parte dell'accordo.** La versione da firmare lo esclude automaticamente.
3. Quando si modifica un articolo, si rilegge il suo commento: se non corrisponde più, si corregge
   nello stesso commit.
4. Il generatore dei PDF **segnala** gli articoli rimasti senza commento.

L'esempio numerico dell'art. 7.3 è anche un foglio Google con i numeri modificabili:
**[GEM — Esempio art. 7](https://docs.google.com/spreadsheets/d/1rcSlygd33kjZxFmh8jQCCw9iLrsOHHEYOq34sJZtUcw/edit)**
(per averlo dentro il registro principale: tasto destro sulla scheda → *Copia in → Foglio esistente*).

## Percorso

1. I due soci leggono entrambi i documenti e annotano cosa non condividono.
2. Le modifiche si fanno **qui**, in Markdown, finché il testo non è condiviso.
3. Solo a quel punto si genera la versione da firmare (PDF/Word), si firma e si archivia
   in `../allegati/` — e lo stato qui passa a ✅ Firmato.

> ⚠️ **Le bozze non sono consulenza legale né fiscale.** Prima della firma vanno lette dal
> commercialista — in particolare l'art. 7 della scrittura privata, che dipende da come il
> secondo socio può ricevere la sua quota in modo fiscalmente corretto.

## Punti che i soci devono decidere (non li può decidere il documento)

| # | Decisione | Dove nel testo |
|---|---|---|
| 1 | ~~Quale dei due è il **Socio Firmatario**~~ → **Gianluca Iaconeta** (deciso il 14/09) | Art. 2 |
| 2 | **Soglia** oltre la quale una spesa richiede il consenso di entrambi | Art. 9 |
| 3 | **Meccanismo fiscale** con cui il secondo socio riceve il 50 % | Art. 7 — col commercialista |
| 4 | Se dare un **acconto** dopo l'incasso dell'80 % e in che misura | Art. 6 |
| 5 | Chi **anticipa** le caparre agli immobili e con quali soldi | Art. 5 |
| 6 | Se includere il patto di **non concorrenza** (art. 12) | Art. 12 |
