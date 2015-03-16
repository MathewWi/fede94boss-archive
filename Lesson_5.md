## Le Array(Funzioni Base) ##

Di notevole funzionalità e versatilità sono le array(o tabelle). Tali costruttori possono essere utilizzati per la gestione di stringhe e quindi la notevole diminuzione di caricamenti nel caso di un Filebrowser,di una shell,di un PSP-Info e molto altro.

Un array si esprime con questo comando:
```
nomedellarray = {}
```

NOTA: Per scrivere delle parentesi graffe con la tastiera italiana bisogna premere "SHIFT+ALT GR+è" tutti insieme per ottenere "{" invece "SHIFT+ALT GR+il segno + affianco al segno è" per ottenere "}".
Con questo comando diciamo che l'array denominata "nomedellarray" è vuota.
E come facciamo ad aggiungerci un elemento?
La risposta è semplice:

```
nomedellarray[1] = System.cfwVersion()
```

In questo esempio abbiamo detto che l'elemento 1 dell'array "nomedellarray" sarà il firmware installato sulla nostra PSP!Semplice?

Vediamo qualche altro comando.
Per stampare a schermo un elemento si usa questo meccanismo:

```
screen:print(0,0,nomedellarray[1],colore)
```

Non c'è bisogno di spiegazione.

Tramite le array potete ridurre i caricamenti degli stessi dati ad una volta sola ad esempio al posto di fare:

```
while true do
info = System.cfwVersion()
screen:print(0,0,info,colore)
end
```

Il quale vi implica il ricaricamento dell'informazione sul Firmware installato ogni volta. Potrete fare:

```
info = {}
info[1] = System.cfwVersion()
while true do
screen:print(0,0,info[1],colore)
end
```

Con questo semplice metodo il firmware rilevato verrà caricato una sola volta e quindi non porterà ad uno spreco inutile della RAM.