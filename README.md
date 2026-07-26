# ic-catalog.it — Landing page

Pagina statica singola (nessuna build necessaria), pronta per GitHub Pages.

## Deploy

1. Crea un repository GitHub (es. `ic-catalog-landing`), pubblico.
2. Carica `index.html` e `CNAME` nella root del repository (branch `main`).
3. Settings → Pages → Source: branch `main`, cartella `/ (root)` → Save.
4. Settings → Pages → Custom domain: scrivi `ic-catalog.it` → Save
   (il file `CNAME` già presente nel repo dovrebbe farlo riconoscere subito).
5. **Solo dopo** aver salvato il dominio su GitHub, configura il DNS su
   Register.it (pannello di gestione DNS del dominio):
   - 4 record A (host vuoto/apex) verso:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - 1 record CNAME per `www` verso `<tuo-username-github>.github.io`
   - (opzionale) 4 record AAAA verso:
     `2606:50c0:8000::153`, `2606:50c0:8001::153`,
     `2606:50c0:8002::153`, `2606:50c0:8003::153`
6. Aspetta la propagazione DNS (fino a 24h, spesso molto meno).
7. Torna su Settings → Pages e spunta "Enforce HTTPS" quando disponibile.

## Da fare prima di pubblicare

- Sostituire `info@ic-catalog.it` nel bottone CTA con l'indirizzo email
  reale che hai configurato (o lasciarlo così se hai già attivato quella
  casella sul dominio).
- Sostituire il testo placeholder nella sezione "prova sociale" con una
  citazione reale appena disponibile.
- Verificare il font Exo 2: la pagina ricade su un font di sistema se Exo 2
  non è caricato. Per usarlo davvero, aggiungere un import da Google Fonts
  nell'`<head>` (non incluso di default per tenere la pagina leggera finché
  non è necessario).
