Dopo aver creato la nostra paginetta normale per fare in modo di passare ad una nuova pagina LUA tramite la pressione di un tasto bisogna fare cosi:

```
pad = Controls.read()
```

Dichiariamo che "pad" carica i "controlli" della psp

```
if pad:cross() then
```

Poniamo la condizione "Se Tasto X è premuto"

```
System.currentDirectory("ms0:/PSP/GAME/NOMENOSTRAHOMEBREW/SYSTEM")
dofile("NUOVAPAGINA.lua")
end
```

Diciamo al programma la directory dove è contenuta la nuova pagina da aprire e poi tramite il "dofile" gli diciamo come si chiama il file.