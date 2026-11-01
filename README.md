# Andrea · Coach

Web app personale (PWA per iPhone) con check-in giornaliero, piano di allenamento adattivo, alimentazione, progressi e Coach AI.

## Struttura
- `public/` — app statica (index.html, service worker, icone, foto, promemoria.ics)
- `api/coach.js` — funzione serverless Vercel che chiama l'API di Anthropic
- `vercel.json` — output in `public/`, header per .ics e service worker

## Deploy
1. Carica il repository su GitHub.
2. Su Vercel: Add New → Project → importa il repository. Framework: Other. Nessun comando di build.
3. Settings → Environment Variables: `ANTHROPIC_API_KEY` = la tua chiave. Facoltativa: `ANTHROPIC_MODEL` (default `claude-sonnet-5-5`).
4. Redeploy.

## Su iPhone
- Apri l'indirizzo in Safari → Condividi → Aggiungi alla schermata Home.
- Nella card «Promemoria» tocca «Aggiungi al Calendario» per le notifiche ricorrenti (anche su Apple Watch).

I dati restano nel browser dell'iPhone (localStorage).
