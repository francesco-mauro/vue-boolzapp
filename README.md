# Boolzapp

Una replica di WhatsApp Web in Vue.js, fatta durante il Master Full Stack di Boolean ad aprile 2024.

## Cosa fa

- **Lista dei contatti** con avatar, ora e anteprima dell'ultimo messaggio.
- **Ricerca:** mentre scrivi, la lista mostra solo i contatti il cui nome contiene il testo.
- **Conversazione:** cliccando un contatto si apre la sua chat, con i messaggi inviati e ricevuti in due stili diversi.
- **Invio dei messaggi:** scrivi e premi Invio, il messaggio compare con data e ora. Dopo un secondo arriva una risposta automatica.
- **Responsive:** sotto i 991 pixel la colonna dei contatti si riduce ai soli avatar, sotto i 540 resta solo la chat.

## Strumenti

Vue 3 (da CDN, senza build), HTML, CSS con media query per tablet e mobile, Font Awesome.

## Come provarlo

Non serve installare niente: scarica il repository e apri `index.html` nel browser.

```bash
git clone https://github.com/francesco-mauro/vue-boolzapp.git
```

## Com'è fatto

- `index.html`: la struttura della pagina e i template Vue (`v-for`, `v-model`, `@keyup.enter`, classi dinamiche per i messaggi inviati e ricevuti).
- `assets/data.js`: l'app Vue, con i contatti di esempio e i metodi per filtrare, cambiare chat, inviare e rispondere.
- `assets/css/`: lo stile principale più due fogli caricati solo su tablet e mobile.
