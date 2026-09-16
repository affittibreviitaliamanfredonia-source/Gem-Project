# Inquadramento fiscale

> ⚠️ **Questo file è una traccia di lavoro, non un parere fiscale.**
> Ogni punto va confermato dal commercialista **prima** di emettere la prima fattura.

## Impostazione assunta

| Voce | Valore |
|---|---|
| Natura operazione | Prestazione di servizi **B2B** verso soggetto passivo UE (Spagna) |
| Territorialità | **Art. 7-ter DPR 633/1972** → rilevante nel paese del committente |
| IVA in fattura | **Nessuna** — inversione contabile |
| Dicitura | *"Operazione non soggetta a IVA ai sensi dell'art. 7-ter DPR 633/72 — inversione contabile / reverse charge"* |
| Chi assolve l'IVA | La capofila, in Spagna |

## ⚠️ Verifica preliminare bloccante: 7-ter o 7-quater?

**Questo è il punto fiscale più delicato del progetto e va sciolto per primo.**

L'art. 7-ter vale per i servizi B2B in generale, ma l'**art. 7-quater DPR 633/72** deroga
per le prestazioni **relative a beni immobili** — comprese quelle **alberghiere e di
alloggio** — che restano rilevanti **dove si trova l'immobile**, quindi **in Italia**,
a prescindere da dove è stabilito il committente.

Le due letture possibili:

| Lettura | Qualificazione | Conseguenza |
|---|---|---|
| **A** | Servizio **complesso** di accoglienza (coordinamento, assistenza, mobility, **collocamento in azienda** con contratto e accompagnamento, gestione documentale), di cui l'alloggio è una componente | 7-ter → fattura **senza IVA** |
| **B** | Prestazione essenzialmente di **alloggio** in Italia | 7-quater → **IVA italiana dovuta** (10 % o 22 % secondo la qualificazione) |

**Impatto economico se vale la lettura B e il prezzo resta 2.000 € "netti":**
l'IVA diventa un costo interno, non un semplice giro contabile. Su 72.000 €, al 10 %
sarebbero circa **7.200 €** che erodono direttamente il margine dei due soci; al 22 %,
circa **15.840 €**. È un ordine di grandezza che può azzerare il margine.

**Azione richiesta:** sottoporre al commercialista la descrizione esatta del servizio
(cosa viene fornito, con quale peso relativo) e ottenere per iscritto la qualificazione,
**prima** di firmare il contratto e prima di emettere fattura. Vedi Q4 nel
[README](../README.md#4-questioni-aperte--bloccanti).

## Condizioni necessarie perché il reverse charge regga

- [x] La capofila è un **soggetto passivo IVA**: ente commerciale, confermato dai soci il 16/09.
- [ ] Il **VAT number** è valido e **attivo su VIES** alla data della fattura.
- [ ] Stampa della verifica VIES archiviata in [`../allegati/`](../allegati/).
- [ ] Il VAT è riportato in fattura.
- [ ] La qualificazione 7-ter è confermata dal commercialista (vedi sopra).

> Se il VAT non è attivo a VIES, l'operazione **non** è in reverse charge: si fattura con
> IVA italiana. Il controllo va rifatto alla data di **ciascuna** delle due fatture.

## Adempimenti per fattura

| Adempimento | Nota |
|---|---|
| Fattura elettronica via SdI | Verso soggetto estero: codice destinatario convenzionale (`XXXXXXX`) e trasmissione via SdI, che assolve la comunicazione delle operazioni transfrontaliere |
| Tipo documento / natura operazione | Da confermare col commercialista in base alla qualificazione scelta |
| Numerazione e registrazione | Secondo il sezionale in uso presso l'emittente |
| Bollo | Verificare se dovuto in base all'importo e alla natura dell'operazione |

## Fatture previste

| # | Tranche | Imponibile (36 ospiti) | Evento | Emessa il | N. fattura | Incassata il |
|---|---|---|---|---|---|---|
| 1 | 80 % | 57.600 € | Arrivo (fattura qualche giorno prima, incasso il giorno dell'arrivo) | — | — | — |
| 2 | 20 % | 14.400 € | Partenza + controllo documentale | — | — | — |

> Gli importi si ricalcolano sul numero **effettivo** di ospiti al momento dell'emissione.
> Ogni fattura emessa e ogni incasso vanno registrati nel registro su Google Fogli
> ([`../04-pagamenti/movimenti-economici.md`](../04-pagamenti/movimenti-economici.md)).

## Da chiarire col commercialista

1. **7-ter o 7-quater** — qualificazione del servizio (vedi sopra). 🔴 Bloccante.
2. Codice **tipo documento** e **natura operazione** corretti per la fattura elettronica.
3. Trattamento dei **costi di alloggio in acquisto** e relativa detraibilità dell'IVA.
4. Eventuali **imposte di soggiorno** comunali e chi ne è responsabile.
5. Momento di **effettuazione dell'operazione** ai fini IVA per la tranche 80 % anticipata.
