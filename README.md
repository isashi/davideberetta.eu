# davideberetta.eu

Sito personale/portfolio di Davide Beretta.

## Stack

- [Astro](https://astro.build) — output statico
- TypeScript
- CSS custom con token/variabili per palette e temi

## Comandi

```bash
npm install
npm run dev       # sviluppo con hot reload, http://localhost:4321
npm run build     # controllo tipi + build statica in dist/
npm run preview   # anteprima locale della build
```

## Struttura

- `src/pages/index.astro` — pagina unica (one-page)
- `src/components/` — hero con logo animato, about, card "cosa faccio", progetti, form di contatto, footer
- `src/styles/global.css` — stili globali (tema scuro, animazione del logo, card con hover-reveal)
- `public/images/` — header e icone delle card; `header_compressed.jpg` è ancora l'immagine stock del sito precedente, da sostituire/ottimizzare più avanti
- `public/favicon.ico`

## Note

- Il form di contatto (`ContactForm.astro`) ha un `action="#"` segnaposto: va collegato a un servizio reale (es. Formspree) prima della pubblicazione.
