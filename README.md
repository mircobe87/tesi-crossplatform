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
  - **Applicazione.tex**  : sorgente del capitolo *L'Applicazione*
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
 - [fncychap](http://ctan.org/pkg/fncychap "Seven predefined chapter heading styles")
 - [frontespizio](http://ctan.org/pkg/frontespizio "Create a frontispiece for Italian theses")
 - [hyperref](http://ctan.org/pkg/hyperref "Extensive support for hypertext in LATEX")
 - [inputenc](http://ctan.org/pkg/inputenc "Accept different input encodings")
 - [mathptmx](http://ctan.org/pkg/mathptmx "Use Times as default text font, and provide maths support")
 - [natbib](http://ctan.org/pkg/natbib "Flexible bibliography support")
 - [setspace](http://ctan.org/pkg/setspace "Set space between lines")
 - [url](http://ctan.org/pkg/url "Verbatim with URL-sensitive line breaks")

## Uso di `maketesi`

###Compilare la tesi
Eseguire il comando

`./maketesi`

per avviare il processo di compilazione. Se tutto ha successo,
si troverà nella root del repo git il file `tesi.pdf`.

### Generare il frontespizio
E' possibile generare solo il frontespizio da far firmare ai relatori.

`./maketesi -f`

genera il frontespizio nel file **frontespizio.pdf**

### Ripulire l'ambiente
Usando questi comandi non viene eseguito nessun processo di compilazione ma
vengono solo eliminati i file indesiderati.

#### Ripulire la cartella dei sorgenti
Il processo di compilazione genera un sacco di file intermedi
nella cartella `./tex/`, se si desidera questi file possono essere rimossi con il comando

`./maketesi -c-tex`

#### Ripulire la cartella delle grafiche
Durante la compilazione i file `.epf` vengono convertiti in `.pdf`, è possibile
rimuovere questi file superflui con il comando

`./maketesi -c-gfx`

#### Ripulire la cartella dei sorgenti e delle grafiche
E' possibile ripulire entrambe le cartelle con il comando

`./maketesi -c`

## Contribuire
Sarebbe opportuno mantenere ogni capito della relazione in un file `.tex` separato incluso poi nel file principale tramite il comando `/include{...}`.

