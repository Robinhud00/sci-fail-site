# Sito sci-fail.com

File: `index.html` (la pagina), `assets/` (screenshot), `CNAME` (il dominio, non toccarlo).

## Pubblicare con GitHub Pages
1. Su github.com crea un repository **pubblico** chiamato `sci-fail-site`.
2. Add file → Upload files: carica `index.html`, `CNAME` e la cartella `assets` (trascina anche la cartella), poi Commit.
3. Settings → Pages → Source: «Deploy from a branch», Branch: `main` / `(root)` → Save.
4. Su Namecheap: Domain List → Manage (sci-fail.com) → Advanced DNS. Elimina i record di parcheggio (URL Redirect Record, CNAME `www` verso parkingpage.namecheap.com) e aggiungi:
   - 4 record **A** con Host `@` e valori `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - 1 record **CNAME** con Host `www` e valore `<tuo-username>.github.io` (il tuo username GitHub, senza https)
5. Torna su GitHub → Settings → Pages: in «Custom domain» scrivi `sci-fail.com`, Save. Quando il controllo è verde, spunta **Enforce HTTPS**.
6. La propagazione può richiedere da pochi minuti a qualche ora.

## Da controllare prima
- In `index.html` cerca `Robinhud00/diario-ricercatore`: deve essere l'indirizzo reale del repository del Diario (due link nella sezione «Scarica»).
- Per raccogliere le email: crea un modulo (Tally, Google Forms) e incolla il link nella riga `var WAITLIST_URL = "";` verso la fine del file.
