# Lisbona 21K

Piano di allenamento a test e diario corse verso la
**EDP Lisbon Half Marathon del 7 marzo 2027**.

22 settimane in quattro fasi (base, qualità, specifica, taper), dal 5 ottobre 2026.

## Come funziona

- **Oggi**: la seduta del giorno e il form per registrarla.
- **Piano**: settimana per settimana.
- **Andamento**: previsione per Lisbona, VDOT, soglia, VAM, grafici.

### Le andature si ricalibrano dai test

L'app usa le formule di Daniels–Gilbert. Il punto di partenza è la mezza della
M6C (1:50:46, VDOT 40). Ogni volta che registri un test, si aggiornano da sole:

| Test | Cosa inserisci | Cosa aggiorna |
|---|---|---|
| 5 km / 10 km a tutta | il tempo | VDOT, tutte le andature, previsione Lisbona |
| 30' di soglia | FC media ultimi 20' | tutte le zone di FC |
| VAM 7' | i metri percorsi | VAM e indice di resistenza (mezza / VAM) |
| FC fissa sul tapis | ritmo medio a 145 bpm | grafico dell'efficienza aerobica |
| Lungo con deriva | FC 1ª e 2ª metà | deriva cardiaca |

Per i test conta la ripetibilità: stesso percorso (o pista), stesse scarpe,
stesse condizioni.

### Inserimento dei dati

Ritmo e tempi si scrivono solo con le cifre: `535` diventa 5:35, `2230` diventa
22:30, `14512` diventa 1:45:12. Per le sedute di soglia e VO2max inserisci ritmo
e FC della parte centrale, non la media dell'uscita.

I dati restano su questo dispositivo. Rotellina in alto a destra per esportarli,
importarli o azzerarli. Il diario del blocco precedente resta salvato anche se
non compare.

## Deploy su GitHub Pages

Sostituisci i file nel repo esistente e fai `git push`. Se parti da zero:

```bash
git init && git add . && git commit -m "Lisbona 21K"
git branch -M main
git remote add origin https://github.com/<tuo-utente>/<repo>.git
git push -u origin main
```

Repo → *Settings* → *Pages* → Branch `main`, folder `/ (root)`.

Su iPhone: Safari → *Condividi* → **Aggiungi a Home**. Se avevi già l'app
installata col nome vecchio, rimuovila e aggiungila di nuovo per vedere il nome
nuovo (i dati restano, sono legati al dominio).

## File

| File | Ruolo |
|---|---|
| `index.html` | Tutta l'app, self-contained |
| `sw.js` | Service worker: offline e aggiornamenti |
| `manifest.webmanifest` | Nome, icone, modalità standalone |
| `*.png` | Icone |

---

Il piano è indicativo e non sostituisce il parere di un medico o fisioterapista.
