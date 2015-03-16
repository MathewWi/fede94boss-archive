### Creare Funzioni Extra ###

Oggi impareremo i comandi base per creare funzioni extra o semplicemente per facilitarci il lavoro:

Per prima cosa creiamo un ciclo
```
while true do
```
Questo comando fa ripetere l'azione

Il comando base per inserire una nuova funzione è
```
function
```
ad esso va affiancato il nome della funzione(un nome che vogliamo noi e,tra parentesi le informazioni che bisognerà inserire per il normale funzionamento della funzione).

Oggi creeremo una funzione esempio per scegliere come avviare un file(quindi per facilitarci un compito e non per creare una funzione extra)

iniziamo dichiarando la funzione

```
function playpbp (dir,file)
```
Con questa parte ho detto che la funzione playpbp per funzionare avrà bisogno di un valore dir e di un altro d nome "file"

ora scriviamo la funzione
```
player = System.startOSK("KERNEL","Come aprire file?")
if player == "KERNEL" then
System.runeboot(dir.."/"..file)
end
if player == "PSX" then
System.startPSX(dir.."/"..file)
end
if player == "UPDATE" then
System.startUpdate(dir.."/"..file)
end
end 
```

Analizziamo il tutto,
il primo pezzo serve a far comparire la tastiera sony da dove decidere l'immissione della modalità di avvio del file e invece i restanti 3 if fan si che se verrà scritto KERNEL nella tastiera si avvierà il file normalmente,se si scriverà PSX allora si avvierà come gioco per la playstation 1 e se scritto UPDATE farà partire l'aggi0ornamento della psp.

Ricapitolando il codice sarà:
```
function playpbp (dir,file)
player = System.startOSK("KERNEL","Come aprire file?")
if player == "KERNEL" then
System.runeboot(dir.."/"..file)
end
if player == "PSX" then
System.startPSX(dir.."/"..file)
end
if player == "UPDATE" then
System.startUpdate(dir.."/"..file)
end
end 
```

Ora basterà mettere la funzione in azione così(faccio un esempio):

```
playpbp("ms0:/PSP/GAME/HB","EBOOT.PBP")
```

cosi faremo si che il file "EBOOT.PBP" posizionato nella cartella HB nella cartella dei giochi possa esser far partito nei 3 modi possibili.
ora non rimane che scrivere la fine della pagina:

```
screen:flip()
screen:waitVblankStart()
end
```
Avete creato la vostra prima funzione!

Ricapitolando ecco il codice finale come risulterà:
```
while true do
function playpbp (dir,file)
player = System.startOSK("KERNEL","Come aprire file?")
if player == "KERNEL" then
System.runeboot(dir.."/"..file)
end
if player == "PSX" then
System.startPSX(dir.."/"..file)
end
if player == "UPDATE" then
System.startUpdate(dir.."/"..file)
end
end
playpbp("ms0:/PSP/GAME/HB","EBOOT.PBP")
screen:flip()
screen:waitVblankStart()
end
```