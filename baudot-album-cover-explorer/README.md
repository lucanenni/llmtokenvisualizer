# Il codice Baudot nella copertina di X&Y

Uno strumento interattivo dedicato a un vero easter egg discografico: la copertina dell'album *X&Y* dei Coldplay (2005) traduce il titolo in blocchi colorati seguendo il codice Baudot. Qui puoi costruire il tuo blocco con qualunque parola e provare a decifrarlo.

Fa parte della raccolta [cs-and-ict-teaching-materials](../README.md).

## Come si usa

Il progetto è statico, non richiede build né server: basta aprire [index.html](index.html) nel browser.

In alternativa, da questa cartella:

```bash
python3 -m http.server 8000
```

e poi visita `http://localhost:8000`.

## Cosa mostra

- Scrivi una parola breve: ogni carattere diventa una colonna di 5 blocchi (colorato = 1, vuoto = 0), esattamente come il meccanismo usato nella copertina reale.
- Il preset "X&Y" ricostruisce l'esempio vero: X (11101), un cambio di stato FIGS (11011), il simbolo & (11010), un cambio di stato LTRS (11111), Y (10101).
- Uno switch nasconde le etichette, per provare a decifrare il codice a occhio prima di vedere la soluzione.

## Concetti didattici illustrati

- Applicazione pratica del codice Baudot già visto in [baudot-code-explorer](../baudot-code-explorer/), inclusi i cambi di stato LTRS/FIGS necessari per rappresentare simboli come "&".
- Come una **convenzione arbitraria** (blocco = 1, vuoto = 0) trasformi un'immagine in dati, e viceversa — la stessa idea alla base di ogni rappresentazione digitale.

## Nota su originalità e diritti

Questa pagina **non riproduce la copertina reale** dell'album (colori, layout e title-art specifici sono opera dello studio Tappin Gofton): ricrea solo il *meccanismo* di codifica — un fatto tecnico, verificabile e di dominio pubblico — con una propria griglia e una propria palette di colori generata algoritmicamente.

## Struttura dei file

- [index.html](index.html) — markup della pagina
- [style.css](style.css) — stile dell'interfaccia
- [script.js](script.js) — tavola ITA2 (identica a quella verificata in baudot-code-explorer), codifica e decodifica del testo

## Licenza

Vedi la [LICENSE](../LICENSE) del repository principale.
