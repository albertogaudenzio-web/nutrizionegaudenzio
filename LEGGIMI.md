# Sito di Alberto Gaudenzio – Dietista a Padova

Sito statico (HTML + CSS), pronto per GitHub + Netlify. Nessun database, nessun cookie, nessun servizio esterno.

## 1. Dati da sostituire PRIMA di pubblicare

Usa "Trova e sostituisci in tutti i file" (in VS Code: Ctrl+Shift+H) su tutta la cartella:

| Cerca | Sostituisci con | Esempio |
|---|---|---|
| `https://www.tuodominio.it` OK | il tuo dominio, senza `/` finale | `https://www.albertogaudenziodietista.it` |
| `+39 000 000 0000` OK | il numero come vuoi mostrarlo | `+39 347 123 4567` |
| `+390000000000` OK | il numero per i link "chiama" (senza spazi) | `+393471234567` |
| `390000000000` OK | il numero WhatsApp (senza + e senza spazi) | `393471234567` |
| `info@tuodominio.it` OK | la tua email | `info@albertogaudenziodietista.it` |
| `https://www.instagram.com/tuoprofilo/` | il link al tuo profilo Instagram | |

Attenzione all'ordine: sostituisci prima `+390000000000`, poi `390000000000`.

Facoltativo: nel codice (dati strutturati) manca il CAP dello studio. Se vuoi aggiungerlo, cerca `"streetAddress":"Via Nicotera, 8"` e aggiungi subito dopo `,"postalCode":"351XX"` con il CAP corretto.

## 2. Immagini da sostituire

Tutte in `images/`. Sostituisci il file mantenendo **lo stesso nome** (formato .jpg):

| File | Contenuto suggerito | Formato |
|---|---|---|
| `logo.jpg` | il tuo logo (quadrato) | 400×400 |
| `hero.jpg` | tua foto in studio (verticale) | 900×1050 |
| `alberto.jpg` | tuo ritratto | 800×900 |
| `servizio-*.jpg` | una foto per ogni servizio | 1200×800 |
| `og-image.jpg` | immagine mostrata quando il sito viene condiviso su WhatsApp/social | 1200×630 |
| `favicon.png`, `apple-touch-icon.png` | icona del sito (versione piccola del logo) | 64×64 e 180×180 |

Comprimi le foto prima di caricarle (es. squoosh.app), idealmente sotto i 200 KB ciascuna.

## 3. Colori

I colori sono all'inizio di `css/style.css` (variabili `--green-...`). Quando hai il logo, cambia `--green-700` con il verde esatto del logo.

## 4. Pubblicazione

1. Crea un repository su GitHub e carica **il contenuto** di questa cartella (index.html deve stare nella radice).
2. Su Netlify: *Add new site → Import from GitHub* → scegli il repository. Build command: vuoto. Publish directory: vuoto (o `/`).
3. In Netlify, *Domain management* → aggiungi il tuo dominio e attiva HTTPS (gratuito).
4. Ogni modifica caricata su GitHub aggiorna il sito in automatico.

## 5. Dopo la pubblicazione (SEO)

1. **Google Search Console**: aggiungi il dominio e invia la sitemap `https://www.tuodominio.it/sitemap.xml`.
2. **Google Business Profile**: inserisci lo stesso nome, indirizzo e telefono del sito (devono coincidere esattamente) e il link al sito.
3. Chiedi ai pazienti soddisfatti di lasciare una recensione su Google: è il fattore più importante per comparire nelle ricerche "dietista Padova".
4. Inserisci il link al sito nella bio di Instagram.

## Struttura

- `index.html` – Home
- `chi-sono.html`, `servizi.html`, `prima-visita.html`, `tariffe.html`, `faq.html`, `contatti.html`
- 9 pagine servizio (`nutrizione-sportiva.html`, `dimagrimento.html`, `composizione-corporea.html`, ...)
- `privacy.html`, `cookie.html`, `404.html`
- `sitemap.xml`, `robots.txt`, `_headers` (impostazioni Netlify)
- `css/`, `js/`, `fonts/` (caratteri ospitati sul sito, licenza OFL), `images/`
