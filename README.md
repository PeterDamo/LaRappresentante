# Classe Eventi 📅

App mobile (PWA) per gestire le quote degli eventi di una classe scolastica: compleanni, regalo maestre, gite, feste e altro.

## Funzioni
- **Genitori**: elenco nominativi (genitore, figlio/a, telefono, data di nascita), import veloce incollando un elenco.
- **Eventi**: tipo, data, quota a persona (o libera), spesa sostenuta, note, chi partecipa (es. esclude il genitore del festeggiato).
- **Per ogni genitore e evento**: importo versato, data, note; "Salva e prossimo" per inserire velocemente.
- **Totali**: raccolto, mancante, quanti hanno pagato / parziali / mancano, saldo (raccolto − spesa), per evento e globali.
- **Extra**: ricerca e filtri, sollecito WhatsApp (singolo o elenco a chi manca), condivisione elenco, compleanni in arrivo con creazione evento in un tap, riepilogo per tipo, "chi deve ancora versare", cassa residua, archivio eventi chiusi, duplica evento, backup/ripristino JSON, export CSV per Excel, tema scuro, funziona offline.

## Pubblicazione su GitHub Pages
1. Crea un nuovo repository su GitHub e carica questi file (o `git push`).
2. In **Settings → Pages → Build and deployment** scegli **Source: GitHub Actions**.
3. Al primo push su `main` il workflow pubblica l'app su `https://<utente>.github.io/<repo>/`.
4. Dal telefono apri il link → menu del browser → **Aggiungi a schermata Home** (Android: "Installa app").

## Dove sono i dati
Nel browser del telefono (`localStorage`), non su un server: nessun costo e dati privati dei bambini non pubblicati online.
Usa **Altro → Salva / condividi backup** regolarmente; il file si ripristina su un altro telefono o lo si passa a un altro rappresentante.

Quando pubblichi modifiche, incrementa `VERSION` in `sw.js` per far aggiornare l'app ai telefoni.

## APK Android (opzionale)
Il workflow **Crea APK Android** (scheda Actions → *Run workflow*) compila `classe-eventi.apk` con Capacitor.
A fine lavoro scarica il file da **Artifacts** in fondo alla pagina dell'esecuzione (è uno zip che contiene l'APK).
Sul telefono: apri l'APK e consenti l'installazione da "origini sconosciute". È un APK di debug, adatto all'uso personale/di classe (non per il Play Store).
