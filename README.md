# CardSync Pro — Prototipo narrativo (scenetta di consegna)

Prototipo statico (un solo file `index.html`, nessun server necessario) per
provare la scenetta narrativa di consegna della bustina giornaliera.
Pensato per essere pubblicato con **GitHub Pages** così da poter caricare
sfondi e sprite reali e vederli funzionare da qualunque dispositivo.

## Struttura delle cartelle

```
index.html
immagini/
  sfondi/
    trama1/
      centro.png
      lab.png
      negozio.png
      postino.png
      cielo.png
      boss.png
    trama2/
      (stessi nomi di trama1)
  sprite/
    default/
      player.png
      companion.png
      nurse.png
      professor.png
      shopkeeper.png
      mailman.png
      flyer.png
      boss.png
    premium/
      (stessi nomi di default)
```

**Importante — i nomi dei file sono fissi**, perché il sito li cerca con
quel nome esatto: se un file manca o è scritto diverso, quella scena resta
semplicemente con lo sprite/sfondo disegnato via CSS (nessun errore
visibile, si vede solo il segnaposto). Formati accettati: `.png`, `.jpg`,
`.jpeg`, `.webp` — vanno bene tutti, l'importante è il nome prima
dell'estensione.

Le cartelle sono già create (con un file `.gitkeep` vuoto dentro, solo per
farle comparire su Git: cancellalo pure quando ci carichi la prima immagine
vera, o lascialo lì, non dà fastidio).

`trama1`/`trama2` e `default`/`premium` sono due varianti alternative —
nel sito pubblicato trovi un pulsante "🖼️ Importa sprite/sfondi (TEST)" in
basso che apre un pannello con cui passare dall'una all'altra al volo, per
confrontarle. Se ti servono più di due varianti, si aggiungono in due minuti
(basta dirmelo).

### Dimensioni consigliate per le immagini

- **Sprite personaggi**: qualunque dimensione va bene (vengono adattati),
  ma per restare nitidi con lo stile "pixel" meglio partire da immagini
  piccole e squadrate, per esempio 128×168 px o multipli, con sfondo
  trasparente (PNG).
- **Sfondi scena**: pensati per riempire un riquadro largo e basso, per
  esempio 840×440 px o proporzioni simili; JPG va benissimo, non serve la
  trasparenza.

## Come pubblicare con GitHub Pages

1. Crea un repository su GitHub (pubblico, altrimenti Pages richiede un
   piano a pagamento) e carica dentro tutto il contenuto di questa cartella
   (compreso `index.html` nella **radice** del repository, non dentro una
   sottocartella).
2. Vai su **Settings → Pages** del repository.
3. In "Source" scegli **Deploy from a branch**, poi branch **main** e
   cartella **/ (root)**. Salva.
4. Dopo un minuto o due il sito è online all'indirizzo che GitHub mostra in
   quella stessa pagina (di solito
   `https://<tuo-utente>.github.io/<nome-repository>/`).
5. Da lì in poi: ogni volta che carichi/sostituisci un'immagine nelle
   cartelle giuste (anche direttamente dall'interfaccia web di GitHub,
   trascinando il file dentro la cartella corretta) e aspetti che Pages
   ripubblichi (di solito sotto il minuto), la vedi comparire nel sito.

Non serve altro: niente build, niente installazioni, `index.html` funziona
da solo.

## Cos'è ancora temporaneo

- Il pulsante "🖼️ Importa sprite/sfondi (TEST)" e il tasto rapido di
  caricamento da questo browser dentro quel pannello sono strumenti di
  prova e verranno rimossi quando gli asset definitivi saranno scelti e
  integrati direttamente nel codice.
- I tasti fisici START/SELECT sotto lo schermo sono momentaneamente
  collegati a "avanza di giorno" e "ricomincia dal giorno 1" per poter
  testare la storia senza aspettare le mezzanotte vere: anche questo verrà
  tolto quando il giorno avanzerà da solo.
