### Lezione 1: Hello World ###

L'Hello World cnsiste nel stampare sullo schermo della PSP una semplice scritta.
Iniziamo installando ed aprendo l'Unofficial Miro LUA,una volta aperto premiamo su File e poi su Nuovo e creiamo una Nuova Pagina.Salvatela dove vorrete e chiamatela "SYSTEM.lua"
Ora vi uscira scritto sullo schermo una riga di colore verde,cancellatela!Bene,lo spazio dove avete cancellato la scritta è il vostro foglio di lavoro dove scriverete tutti i codici e i programmi che creerete in futuro.
Iniziamo col definire che colore utilizzare per la nostra scritta e scriviamo così:

```
nomedelcolore = Color.new(var1,var2,var3)
```

Sostituiamo nomedelcolore col il nome del colore che abbiamo scelto e sostituiamo var1,var2,var3 ai valori di Rosso,Verde e Blu che ha il colore che vogliamo fare.Per vedere tali colori apriamo il Paint di Windows,clicchiamo su Colori e poi su Modifica Colori(in alto)clicchiamo sul colore da usare,clicchaimo su Definisci colori personalizzati e vedrete tre parametri,corrisponderanno a quelli che dovrete inserire al posto dei tre var:


nel mio esempio scriverò:

```
verde = Color.new(0,255,0)
```

fatto questo andiamo accapo e scriviamo:

```
sfondo = Image.createEmpty(480,272)
```

Questo comando serve per creare un immagine vuota,i numeri 480 e 272 corrispondono alla grandezza in pixel che dovrà avere l'immagine e noi abbiamo messo questi numeri perchè sono rispettivamente larghezza ed altezza dello schermo della PSP.

Dopo di ciò andiamo accapo e scriviamo:

```
screen:blit(0,0,sfondo,0,0,sfondo:width(),sfondo:height(),false)
```

Analizziamo il codice:

screen definisce che si agirà sullo schermo e non su di una immagine
blit comando per stampare sullo schermo delle immagini
0,0 rispettivamente la posizione X(larghezza) ed Y(altezza) dell'immagine o scritta o linea da stampare
sfondo in questo caso il nome che abbiamo dato all'immagine creata
sfondo:width() questo comando dice che la larghezza dell'immagine sarà uguale a 480
sfondo:height() questo comando dice che l'altezza dell'immagine saràuguale a 272
false dice che l'immagine da stampare non deve essere trasparente(se si mette true sara trasparente)

Dopo aver scritto questo andiamo accapo e scriviamo:

```
screen:print(0,0,"Hello World",nomedelcolore)
```

Analizziamo quest'altro codice:

screen gia abbiamo imparato a cosa serve
print questo comando viene utilizzato per stampare a schermo una scritta
0,0 gia sappiamo a cosa serve
"Hello World" questo è il testo che verrà stampato,si mette sempre fra le virgolette
nomedelcolore qui dovrete mettere il nome del colore che avevate precedentemente scritto

Dopo di tutto ciò possiamo avviarci alla chiusura del file.Scriviamo:

```
screen:flip()
screen:waitVblankStart()
```

Questi comandi servono per definire la fine del codice e l'attesa dello schermo prima di essere pulito(con il comando waitVblankStart) non avendo messo nessun numero l'attesa sarà infinita.

Ricapitolando ecco il codice come si presenterà nel mio esempio:
```
verde = Color.new(0,255,0)
sfondo = Image.createEmpty(480,272)
screen:blit(0,0,sfondo,sfondo:width(),sfondo:height(),false)
screen:print(0,0,"Hello World",verde)
screen:flip()
screen:waitVblankStart()
```

Salviamo il codice.Colleghiamo la PSP al PC,posizioniamoci sulla cartella PSP/GAME ( dove vanno tutte le homebrew che scarichiamo e che creeremo),creiamo una cartella a piacere e inseriamoci dentro l'EBOOT del LUA Player HM 7,poi creiamo sempre in questa cartella un'altra cartella denominata SYSTEM ed inseriamoci dentro il file SYSTEM.LUA,scolelghiamo la psp e proviamo la nostra homebrew.