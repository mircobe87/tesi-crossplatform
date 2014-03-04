# Tesi di laurea triennale in informatica

## Contenuto
 
- **tex/** : contiene i file sorgenti *LaTeX* dove il file principale è **tesi.tex**.
  - **tesi.tex**         : file principale che contiene tutto il preambolo e tutti gli `include{...}` del caso
  - **frontespizio.tex** : sorgente del frontespizio
  - **dedica.tex**       : sorgente della pagine della dedica
  - **sommario.tex**     : sorgente del sommario
  - **scheletro.tex**    : anteprima della struttura della relazione
  - **Introduzione.tex** : sorgente del capitolo *Introduzione*
  - **SviluppoApplicazioniMobili.tex** : sorgente del capitolo *Sviluppo Applicazioni Mobili*
  - **FrameworkValutati** : sorgente del capitolo *Framework Valutati*
  - **Conclusioni.tex**   : sorgente del capitolo *Conclusioni*
- **graphics/** : contiene gli elementi grafici utilizzati.
  - **unipi.pdf** : logo dell'università
- **maketesi** : semplice script *bash* per compilare la relazione in formato pdf.
- **README.md** : questo file.

## Pacchetti LaTeX utilizzati

Prima di compilare il documento con il comando `./maketesi` assicurarsi di avere
installato nel proprio sistema i seguenti pacchetti:

 - [babel](http://ctan.org/pkg/babel "Multilingual support for Plain TEX or LATEX")
 - [fancyhdr](http://ctan.org/pkg/fancyhdr "Extensive control of page headers and footers in LATEX2ε")
 - [frontespizio](http://ctan.org/pkg/frontespizio "Create a frontispiece for Italian theses")
 - [hyperref](http://ctan.org/pkg/hyperref "Extensive support for hypertext in LATEX")
 - [inputenc](http://ctan.org/pkg/inputenc "Accept different input encodings")
 - [natbib](http://ctan.org/pkg/natbib "Flexible bibliography support")
 - [setspace](http://ctan.org/pkg/setspace "Set space between lines")
 - [url](http://ctan.org/pkg/url "Verbatim with URL-sensitive line breaks")

## Uso di `maketesi`

###Compilare la tesi
Eseguire il comando

`./maketesi`

per avviare il processo di compilazione. Se tutto ha successo,
si troverà nella root del repo git il file `tesi.pdf`.

### Ripulire la cartella dei sorgenti
Il processo di compilazione genera un sacco di file intermedi
nella cartella `./tex/`, se si desidera questi file possono essere rimossi con il comando

`./maketesi -c`

**nota** che in questo modo non viene eseguito nessun processo di compilazione ma viene solo ripulita la cartella dei sorgenti.

## Contribuire
Sarebbe opportuno mantenere ogni capito della relazione in un file `.tex` separato incluso poi nel file principale tramite il comando `/include{...}`.

