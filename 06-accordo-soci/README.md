# 06 · Accordo tra soci

Documenti che regolano il rapporto **tra i due soci**, Gianluca Iaconeta e Luigi Zerulo.
Non riguardano la capofila: sono interni.

| File | Contenuto | Stato |
|---|---|---|
| [`documento-di-progetto.md`](documento-di-progetto.md) | Riassunto del progetto su cui i soci si impegnano — **Allegato A** della scrittura privata | 🟡 Bozza |
| [`scrittura-privata.md`](scrittura-privata.md) | Accordo tra i soci: ruoli, soldi, decisioni, rischi | 🟡 Bozza |
| [`domande-aperte.md`](domande-aperte.md) | **Lista di lavoro**: 10 assiomi e 48 domande, divise per chi deve rispondere, con spazio per le risposte | 🟡 13 + 10 parziali / 48 |

## Versioni stampabili

| PDF | Generato da |
|---|---|
| [`pdf/GEM-documento-di-progetto-v0.4.pdf`](pdf/GEM-documento-di-progetto-v0.4.pdf) | `documento-di-progetto.md` |
| [`pdf/GEM-scrittura-privata-soci-v0.4.pdf`](pdf/GEM-scrittura-privata-soci-v0.4.pdf) | `scrittura-privata.md`, **senza** commentario — la versione da firmare |
| [`pdf/GEM-scrittura-privata-soci-v0.4-con-commentario.pdf`](pdf/GEM-scrittura-privata-soci-v0.4-con-commentario.pdf) | `scrittura-privata.md`, **con** commentario — la versione da leggere |

I PDF sono **copie di lettura** con marcatura "Bozza v0.4": si rigenerano dal Markdown a ogni
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

## Ancore e rimandi interni

Ogni titolo di articolo porta un'**ancora invisibile** (`<!--#nome-->`) e ogni rimando nel
testo la ripete (`art. 8<!--decisioni-->`). Né GitHub né i PDF le mostrano. Servono al
controllo automatico, che a ogni generazione verifica:

- che gli articoli siano numerati 1, 2, 3… senza salti;
- che ogni "art. N" nel testo punti davvero all'articolo che intende (per *nome*, non per numero);
- che nessun rimando punti a un articolo cancellato;
- che nessun articolo sia rimasto senza commento, e nessun commento senza articolo.

**Se si cancella un articolo:** i numeri di quelli successivi scalano e i rimandi si sfasano.
Il generatore lo segnala e, in modalità riparazione, rinumera titoli e rimandi da solo.
Restano da sistemare **a mano** solo i rimandi all'articolo cancellato — il testo cita
qualcosa che non esiste più, e cosa scrivere al suo posto è una decisione, non un calcolo.

Quando si aggiunge un articolo nuovo: titolo nella forma `## Art. N — Titolo <!--#nome-->`,
e ogni rimando a un articolo nella forma `art. N<!--nome-->`.

L'esempio numerico dell'art. 7.3 è anche un foglio Google con i numeri modificabili:
**[GEM — Esempio art. 7](https://docs.google.com/spreadsheets/d/1rcSlygd33kjZxFmh8jQCCw9iLrsOHHEYOq34sJZtUcw/edit)**
(per averlo dentro il registro principale: tasto destro sulla scheda → *Copia in → Foglio esistente*).

## Dove si rivede: il Google Documento

Copia di revisione della scrittura privata, nella cartella Drive
**Progetto GEM → 06 · Accordo tra soci**:
**<https://docs.google.com/document/d/1FznIcVviozfEaZ69u2Ygc_B3EBVLvOV8RPOtFehyU9g/edit>**

> Il Documento è fermo alla **v0.2** (mattina del 16/09). Le versioni 0.3 e 0.4 recepiscono le
> risposte della videochiamata (art. 2, 4, 5, 6, 9, 10): il Documento si ricarica a fine giro.

| Chi | Cosa fa | Dove |
|---|---|---|
| Gianluca e Luigi | Leggono; **commentano** a margine; propongono correzioni in **modalità Suggerimento** | Google Documento |
| Claude | Legge commenti e suggerimenti, li riporta nel file originale, rigenera PDF e ricarica il Documento | Repository → Drive |

Regole:
- **L'originale è `scrittura-privata.md`.** Il Documento è una copia: se i due divergono, vale il file.
- Non modificare il Documento in modalità *Modifica* diretta: le correzioni non tracciate si perdono
  al ricaricamento. Usare *Suggerimento* (o un commento).
- Ogni ricaricamento del Documento **azzera i commenti** già recepiti: se un commento è ancora lì,
  non è ancora stato recepito.

## Percorso

1. I due soci leggono il Documento e il PDF con commentario, e annotano cosa non condividono
   (commenti e suggerimenti nel Documento, oppure a voce a Claude).
2. Le modifiche si fanno nel file Markdown, finché il testo non è condiviso; a ogni giro si
   rigenerano PDF e Documento.
3. Solo a quel punto si genera la versione da firmare, si firma e si archivia
   in `../allegati/` — e lo stato qui passa a ✅ Firmato.

> ⚠️ **Le bozze non sono consulenza legale né fiscale.** Prima della firma vanno lette dal
> commercialista — in particolare l'art. 7 della scrittura privata, che dipende da come il
> secondo socio può ricevere la sua quota in modo fiscalmente corretto.

## Punti che i soci devono decidere (non li può decidere il documento)

| # | Decisione | Dove nel testo |
|---|---|---|
| 1 | ~~Quale dei due è il **Socio Firmatario**~~ → **Gianluca Iaconeta** (deciso il 14/09) | Art. 2 |
| 2 | ~~**Soglia** di spesa~~ → **nessuna soglia**, spese al minimo, consenso solo fuori dal piano di cassa (deciso il 16/09) | Art. 9 |
| 3 | **Meccanismo fiscale** con cui il secondo socio riceve il 50 % | Art. 7 — col commercialista |
| 4 | ~~Se dare un **acconto** dopo l'80 %~~ → **nessun acconto**, margine diviso solo alla fine (deciso il 16/09) | Art. 6 |
| 5 | ~~Chi **anticipa** le caparre agli immobili~~ → **in parti uguali, restituiti a consuntivo** (deciso il 16/09); con quali soldi: piano di cassa | Art. 5 |
