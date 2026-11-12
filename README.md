# Boolzapp

**Prova la demo:** https://francesco-mauro.github.io/vue-boolzapp/

Una replica di WhatsApp Web in Vue.js, scritta ad aprile 2024 durante il Master Full Stack di Boolean.

## Cosa fa

- **Lista dei contatti** con avatar, ora e anteprima dell'ultimo messaggio.
- **Ricerca:** mentre scrivi, la lista mostra solo i contatti il cui nome contiene il testo.
- **Conversazione:** cliccando un contatto si apre la sua chat, con i messaggi inviati e ricevuti in due stili diversi.
- **Invio dei messaggi:** scrivi e premi Invio, il messaggio compare con data e ora. Dopo un secondo arriva una risposta automatica.
- **Responsive:** sotto i 991 pixel la colonna dei contatti si riduce ai soli avatar, sotto i 540 si stringe ancora e la chat prende quasi tutto lo schermo.

## Bug corretti nel 2026

Il progetto è del 2024 e il codice è rimasto quello di allora, tranne alcune correzioni fatte a novembre 2026:

- **Ricerca e chat sbagliata:** con la ricerca attiva, cliccando un contatto si apriva la chat di un altro. Il click passava la posizione nella lista filtrata, che poi veniva usata su quella completa. Ora passa il contatto, e la sua posizione si cerca nella lista completa.
- **Telefono:** sotto i 540 pixel la colonna dei contatti spariva e non si poteva più cambiare chat. Ora resta, con i soli avatar.
- **Risposta automatica nella chat sbagliata:** se dopo aver scritto si cambiava chat entro un secondo, l'«Ok» arrivava nella chat appena aperta. Ora il contatto viene salvato prima del timer.
- **Versione di Vue fissa:** la pagina caricava sempre l'ultima Vue 3, ora la 3.5.44, così un aggiornamento non può rompere la demo.

## Strumenti

Vue 3.5.44 (da CDN, senza build), HTML, CSS con media query per tablet e mobile, Font Awesome.

## Come provarlo

Non serve installare niente: scarica il repository e apri `index.html` nel browser.

```bash
git clone https://github.com/francesco-mauro/vue-boolzapp.git
```

## Com'è fatto

- `index.html`: la struttura della pagina e i template Vue (`v-for`, `v-model`, `@keyup.enter`, classi dinamiche per i messaggi inviati e ricevuti).
- `assets/data.js`: l'app Vue, con i contatti di esempio e i metodi per filtrare, cambiare chat, inviare e rispondere.
- `assets/css/`: lo stile principale più due fogli caricati solo su tablet e mobile.
