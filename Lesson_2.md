### Lezione 2: Le Variabili ###

E' ora di capire cosa sono le variabili e come si utilizzano.
Le variabili possono far riferimento ad un numero,ad una stringa o ad una funzione e/o variabile.

Ecco un esempio di ognuno dei casi sopraddetti:

```
variabilenumero = 1
variabilestringa = "Ciao"
variabilefunzione = System.currentDirectory()
variabilevariabile = variabilenumero
```

Analizziamo i vari casi e vediamo il loro possibile uso:

Tutte le variabili da come vedete hanno un nome e per definire da cosa sono formate si usa il simbolo =.
La variabilenumero si puo usare per calcoli matematici o per definire il valore di una certa funzione.Ecco 2 esempi:

```
risultato = variabilenumero + 1
screen:print(variabilenumero,0,"Hello World",verde)
```

Il primo codice dice che la variabile denomianta risultato sarà il risultato del valore di varaibilenumero + 1 quindi risultato varrà 2.
Per il secondo caso invece la variabile viene usata per selezionare la posizione della scritta.

Il risultato della variabilestringa deve essere immessa sempre fra virgolette e puo essere usata per essere considerato come un testo o la posizione di un file.
Esempi:

```
screen:print(0,0,variabilestringa,verde)
dofile(variabilestringa)
```

Nel primo codice la variabile viene usata come se fosse il testo da stampare mentre nel secondo come se fosse un file(il comando dofile serve per aprire dei file LUA)

Arriviamo alla variabile funzione che viene usata per semplificarci le idee,è utile se si vogliono raggruppare tutti i comandi a inizio foglio oppure per non dover riscrivere il codice di una funzione ogni volta.Esempio:

```
screen:print(0,0,variabilefunzione,verde)
```

Con questo codice stamperemo a schermo la posizione in cui ci troveremo nelle directory(esempio la cartella della nostra hb)

Invece per le variabili che utilizzano altre variabili,sono le meno utilizzate perchè le meno utili.Possono servire per creare delle variabili da salvare prima che vengano modificate ma questo sistema lo vedremo più in la.