# Benvenuti al tutorial/guida per le watchface personalizzate per la versione Artems xdrip per GRT 2e!

Questa guida vi condurrà attraverso tutti i passi necessari per adattare una watchface a xdrip. Io non sono un parlante nativo, quindi sentitevi liberi di suggerire modifiche.
Questa guida si concentra sull'adattamento di una watchface esistente alle nostre esigenze. Se siete abbastanza creativi e abili da creare la vostra watchface, questo tutorial vi aiuterà con gli adattamenti tecnici per usarla in xdrip.

Ricordate che questa guida è solo per **GTR 2e**! Molte cose sono simili per diversi orologi, specialmente per il GTR 2 e il GTS 2(e). Se state usando questa guida per creare watchfaces per diversi orologi, vi preghiamo di inviare snipets di testo via issue per aiutare questa guida a soddisfare anche diversi orologi. 

Il merito principale va ad **Artem Kovalenko** che ha reso possibile Amazfit GTR2, GTR2e, GTS2, GTS2e, GTR42, Bip, BIP S e GTR 47! Inoltre mi ha aiutato molto a creare il mio primo watchface.
#### Per favore supportatelo qui: https://www.patreon.com/xdrip_miband
Potete leggere di più sui suoi progetti riguardanti xdrip qui: https://bigdigital.home.blog/

Inoltre grazie a:

 - [**SashaCX75**](https://amazfitwatchfaces.com/forum/memberlist.php?mode=viewprofile&u=113690) ha aiutato a creare il watchfaceditor 
 - tutto il creatore di watchface


> 

### Esempio di watchface


Nella cartella [01-WF-MD225-Versione3-xdrip-ready](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/01-WF-MD225-Version3-xdrip-ready
"01-WF-MD225-Versione3-xdrip-ready") troverete il prodotto finale di una watchface personalizzata. Collegherò qui un altro repository con diverse watchface che ho creato più tardi. 

**Se avete creato la vostra watchface per favore condividetela con gli altri. Potremmo raccoglierli in un repo, sentitevi liberi di contattarmi via issue.**


## Cose di cui avete bisogno

Userò i seguenti strumenti. Avrete bisogno di tutti loro. Tutti gli strumenti qui sotto sono gratuiti per uso personale.

1. Sistema operativo Windows
2. **WFE**: [AmazFit WatchFace editor 2 per Windows](https://amazfitwatchfaces.com/forum/viewtopic.php?p=8392#p8392)
3. **PS**: Photoshop (la versione CS2 è disponibile gratuitamente) https://archive.fo/255q5#selection-1663.0-1663.29
5. **WF**: Un watchface. (capitolo successivo)
6. Scaricate l'intero repository, avremo bisogno di alcuni file più tardi dalla cartella "Guide". Puoi scaricare questo archivio cliccando sul pulsante "codice" in cima a questa pagina e scegliendo "Download ZIP".

## Cerca una watchface che vorresti usare

Se non stai creando la tua watchface, puoi dare un'occhiata alle watchface qui: https://amazfitwatchfaces.com/gtr/top?compatible=GTR_2
Donwload il file desiderato. Si prega di fare attenzione all'orologio per cui è stata creata la watchface.

**Qualcosa di molto importante:** 

 - Più piccola è la watchface, meglio è. Ci arriveremo dopo, ma tutte le immagini, incluso il file json, non dovrebbero essere più grandi di 50kb. 
 - La dimensione della watchface di 50kb (immagini grezze e il json) risulterà in un tempo di caricamento di circa 10 secondi e non volete che ci voglia più tempo, a causa della durata della batteria e non volete aspettare fino a domani.
 - Questo significa meno icone, meno cose che cambiano (esclusi i numeri, e sì, solo i numeri). 
 - Evitare watchfaces con gradienti (quando un colore si sposta in un altro). 
 - Ricordate che vogliamo essere in grado di leggere facilmente la nostra glicemia (BG), quindi dobbiamo fare un po' di spazio libero da qualche parte. Calcolerei almeno 1/3 della watchface dedicata a tutte le informazioni relative a xdrip

# 1. Guida / Tutorial

1. Scaricate l'intera cartella dell'ultima versione del WFE (watchface editor), collegata sopra. 
2. Potete trovare il bottone "download" in alto a destra, abbiamo bisogno di tutta la cartella! 
3. Dopo aver cliccato su download scegli "download diretto". Verrà scaricato un file come "AmazFit_Watchface_Editor_2_v5.1.zip".
4. Estrarre il file
5. Aprire (nel mio caso) "AmazFit_Watchface_Editor_2".
6. Avviare "AmazFit_Watchface_Editor_2.exe".
7. Con il tasto destro del mouse, scegliete "Unpack compressed bin".
8. Scegli la watchface che hai scaricato prima
9. La watchface scompattata può essere trovata qui: ...\AmazFit_Watchface_Editor_2\Watch_face
10. Ora è necessario familiarizzare con il WFE.
11. Spiegherò solo le basi assolute. Per saperne di più sull'editor di watchface e le sue possibilità, date un'occhiata qui: https://amazfitwatchfaces.com/forum/viewtopic.php?f=14&t=1571
Link diretto alla traduzione inglese: https://translate.google.com/translate?hl=ru&sl=ru&tl=en&u=https%3A%2F%2Fowagner.ru%2Famazfitgtr%2Fwfcreator%2Fwatchfaces_creator_lesson%2F
12. Vai alla scheda "Edit" e clicca attraverso le diverse opzioni sul lato destro. 
13. Scegli "Layer order" per definire cose come l'ordine della data (dd-mm-yy o mm-dd-yy).

> **Suggerimento importante:** 
> Il nostro obiettivo più importante è ridurre le dimensioni. Come scritto
> sopra vogliamo ottenere meno di 50kb di file png grezzi (incluso .json).
> 
> Il modo migliore per ridurre le dimensioni:
> - meno immagini
> meno colori (rende i file immagine più piccoli)
> - usare il font di sistema (un'impostazione nella scheda di modifica della WFE dove mostra i numeri).


14. Quando hai finito con le tue modifiche, salva la watchface (scheda "Modifica", in basso nel mezzo "salva Json")

> **Cose che mi hanno aiutato molto:**
> - l'immagine 0001.png è sempre lo sfondo. Normalmente è necessario adattare lo sfondo per adattarlo al grafico del glucosio e a tutti i dati necessari. Usa Photoshop per questo o un altro programma
> - Dai un'occhiata alle immagini scompattate e cancella tutte quelle che non ti servono.
> - Devi rinominare i file da 0001- xxxx Avrai problemi in seguito se i file non sono in fila. Non è possibile avere un
> numero in mezzo che manca. Dovrebbe essere come: 0001, 0002, ......
> 0015.) Puoi usare https://www.bulkrenameutility.co.uk/Download.php per rinominare in blocco i file.

15. Vai alla cartella che include il json e tutti i file necessari sul tuo computer.
16. Fate un backup dei file esistenti e del json

## 1.1 Modificare lo sfondo della tua watchface
Se la vostra watchface ha un colore semplice, modificatelo nel WFE. Ma avrai bisogno di creare un'immagine, dove tutta la data xdrip è posizionata, quindi crea un'immagine che corrisponda al colore in PS e salta la parte seguente, dove descrivo come tagliare l'immagine.

17. Aprite 0001.png (la vostra immagine di sfondo) in PS
18. Andate in Picture-->Mode e cambiate di nuovo in RGB
19. Selezionate il Rightangle-Tool premendo "M" e scegliete la parte dove volete che vengano mostrati i vostri dati xdrip.
![##**PS_cut_xdrip_part_01.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_01.PNG)

20. Cliccate con il tasto destro all'interno e scegliete "Layer by cutting".
21. Salvare questo file come file PS (.psd)
22. Nascondere il resto dell'immagine cliccando l'icona dell'occhio sul lato destro (Layers) sul Layer 1
![## **PS_cut_xdrip_part_02.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_02.PNG)
23. Premere "c" per usare lo strumento di taglio
24. Tagliate l'immagine fino alla dimensione della parte visiva del vostro watchface.
25. Premere "enter" per confermare o la spunta in alto
26. Ora salvate questo come **mio_immagine.png**
27. 27. Aprite il file psd salvato e fate la stessa cosa per il resto della watchface, in modo da avere l'immagine di sfondo, divisa in 2 file.


### 1.1.1.1 Ridurre le dimensioni dell'immagine
28. Aprite ogni file, uno dopo l'altro con PS.
29. Cliccare su Dati--> Salva per il web
30. Nella nuova finestra dovresti scegliere sulla destra
	- png-8
	- Puoi armeggiare un po' ed eliminare colori specifici, questo ridurrà la dimensione dell'immagine ancora di più. Puoi vedere la nuova dimensione del file in basso a destra
	- I file devono essere png! 
	- Se incontri uno strano bordo intorno alle tue immagini:
		- vai immagine, Modalità e cambialo in "colori indicizzati" prima di salvarlo per il web
31. Salva il file sovrascrivendo (hai fatto un backup prima). Non ho trovato un modo per farlo a tutti i file in una volta sola, fammi sapere se sai come fare.

### 1.1.2 Metti my_image.png al posto giusto nel WF
32. Ora aprite di nuovo WFE, dovreste notare che abbiamo un ritaglio al centro della nostra watchface. (in caso contrario salvate la vostra immagine di ritaglio come immagine di sfondo)
33. andate su Edit--> Activity -->Fat-burning-->Icon
34. Copiate la seguente immagine che si trova qui: ## GTR-2-WF-Xdrip-IT/[Guida](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/Guide)/**0099.png** è solo 1 pixel. La sostituiremo in seguito con la my_image.png tramite il codice. Ma questo ci fa risparmiare un sacco di dimensioni della watchface.
35. Ora dovete metterlo nell'angolo in alto a sinistra del nostro ritaglio. Per trovare le coordinate giuste, leggete il seguente argomento (Come trovare le coordinate giuste in PS)

## 1.2 Preparare la watchface finale
Quello che dovreste avere finora in 1 cartella
- un json che hai creato con WFE
- tutti i file WF necessari, di dimensioni ridotte al massimo
- my_image.png, di dimensioni ridotte al massimo
--> ci stiamo avvicinando al vostro WF finale :)

36. Navigare su ....\AmazFit_Watchface_Editor_2\Tools
37. tieni premuto shift+click destro in questa cartella
38. Scegliete "Aprire la finestra Powershell qui".
39. Per impacchettare il vostro json dovete solo navigare nella cartella tools ed eseguire il comando come questo  
Main.exe --gtr2 47 --file config-file.json` dove config-file.json è la posizione del vostro json.
	- Ho avuto qualche problema con questo e ho avuto bisogno di aggiungere l'intero percorso davanti al main.exe in modo che fosse qualcosa di simile a questo:
		- C:\Userstwinko\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Tools\main. exe --gtr2 47 --file C:\Users\TwinkosTower\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Watch_face\gtr2-g7en-colormix03-346659-994092c337\Small\WF_2_V01.json`
40. Come risultato, dovresti ricevere un file bin scompattato. Questo file dovrebbe essere usato in xdrip. Xdrip inietterà la risorsa richiesta in questo file, lo comprimerà e lo invierà all'orologio.
41. rinominare il bin in: my_watchface.bin
42. Creare una nuova cartella, mettendo i seguenti file:
- il my_watchface.bin che abbiamo creato
- my_image.png

## 1.3 Modifica del config.json

Il config.json definisce dove, su my_image.png, vengono mostrati i dati xdrip e come. È diverso dal json creato dalla WFE, non confonderli!

Il config.json originale creato da Artem è collegato qui:
https://github.com/twinko/GTR-2-WF-Xdrip-EN/blob/main/Guide/config.json
Hai scaricato il repository prima, prendi il file dalla cartella Guide!



> **Cose generali da sapere:**
> - questo config.json è relativo solo a my_image.png
> - quindi se parliamo di coordinate (x e y) è basato su my_image.png e sulla sua dimensione totale, non sull'intera watchface
> - leggi il post di Artems sull'allineamento qui: https://github.com/bigdigital/xDrip-miband/issues/5#issuecomment-878008056
> - text_align: "right" 
> - devi contare i pixel partendo dal lato destro
> - quindi se si legge: x: 100 e text align è a destra, contando 100 pixel dal lato destro dell'immagine è dove l'elemento è posizionato

### 1.3.1 Come trovare le coordinate giuste in PS
43. Aprire my_image.png in PS
44. premete F8, apparirà una piccola finestra informativa
45. Se muovete il mouse sopra l'immagine, vedrete i numeri X e Y muoversi. 

### 1.3.2 spiegato il config.json
46. aprite il config.json con notepad
47. Vedete dei piccoli cluster, che si spiegano da soli
48. Abbiamo solo bisogno di modificare resource_to_replace, X, Y font_size forse bg_color del grafico

#### 1.3.2.1 resource_to_replace
49. mettete il numero dell'immagine che abbiamo scelto per Fat-burning-->Icon (se la vostra immagine fiurst si chiama 0001.png) riducete il numero di uno. L'algoritmo inizia a contare con 0)

#### 1.3.2.2 "x" , "y" e "text_align": "right",
50. come descritto in "Come trovare le giuste coordinate in PS" puoi trovare la giusta posizione per posizionare i tuoi dati xdrip. 

> **Suggerimento**: Il font di sistema è "Segoe UI" quindi premi t in PS per scrivere del testo e
> metti del testo defualt nel tuo my_image.png e cerca le giuste
> coordinate. Ricorda *x e y sono in basso a sinistra della prima
> lettera/numero*. Non salvare il my_image.png con i numeri che hai
> scritto, questo sarà fatto dopo dalla magia di Artems, lo facciamo in PS
> per trovare le coordinate giuste, non per altro.

51. Ora cambiate tutte le coordinate secondo le vostre esigenze.
52. Attenzione: ci sono alcuni valori che hanno la seguente linea: `"text_align": "right",` per questi abbiamo una regola diversa per le coordinate. *Inserisci la coordinata destra dell'ultima lettera/numero.

#### 1.3.2.3 "font_size"
53. Mettete la stessa dimensione del carattere che avete scelto in PS

### 1.3.3.3 Salva il config.json
54. Salva il config.json nella cartella che include my_image.png e my_watchface.bin (config.json non my_config.json!)


## 1.4 Caricare e testare

55. Ora dovremmo avere una cartella con i seguenti file
- config.json 
- mia_immagine.png 
- my_watchface.bin  
56. inserire questi 3 file nella cartella xdrip del vostro smartphone 
- La cartella xdrip necessaria si trova qui:
	- Internat storage/xdrip o
	- root/storage/emulated/0/xdrip
57. Abilitare la watchface personalizzata nelle impostazioni di xdrip.
58. Fatto!

# 2. Nota a piè di pagina

Per favore aprite un problema qui se incontrate problemi. Per favore fate le vostre ricerche in anticipo, io sono solo un ragazzo normale che fa questo nel suo tempo libero. 
https://github.com/twinko/GTR-2-WF-Xdrip-EN/issues

Se avete suggerimenti su come migliorare il guiode o renderlo adatto anche ad altre watchfaces, scrivete pure un problema :)

Spero che questa guida sia stata utile :)

