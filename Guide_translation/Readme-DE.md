
# Willkommen zum Tutorial / Leitfaden für Artems xdrip Version für GRT 2e!

Dieser Leitfaden ist automatisch übersetzt in:
- Chinesisch (CHN) 
- Deutsch (DE)
- Spanisch (ES)
- Französisch (FR)
- Italienisch (IT)
- Russisch (RU)
Ich spreche nur DE und EN, wenn Sie also Kontakt aufnehmen, tun Sie es bitte auf Englisch!

Diese Anleitung führt Sie durch alle Schritte, die nötig sind, um ein Watchface an xdrip anzupassen. Ich bin kein Muttersprachler, also können Sie gerne Änderungen vorschlagen.
Diese Anleitung konzentriert sich auf die Anpassung eines bestehenden Watchfaces an unsere Bedürfnisse. Wenn Sie kreativ und geschickt genug sind, um Ihr eigenes Watchface zu erstellen, wird Ihnen diese Anleitung bei den technischen Anpassungen helfen, um es in xdrip zu verwenden.

Bitte beachten Sie, dass diese Anleitung nur für **GTR 2e** gilt! Viele Dinge sind für verschiedene Uhren ähnlich, insbesondere für die GTR 2 und GTS 2(e). Wenn Sie diese Anleitung verwenden, um Watchfaces für andere Uhren zu erstellen, senden Sie bitte Textschnipsel über issue, damit diese Anleitung auch für andere Uhren passt. 

Der größte Dank geht an **Artem Kovalenko**, der Amazfit GTR2, GTR2e, GTS2, GTS2e, GTR42, Bip, BIP S und GTR 47 möglich gemacht hat! Außerdem hat er mir sehr geholfen, mein erstes eigenes Watchface zu erstellen.
#### Bitte unterstützen Sie ihn hier: https://www.patreon.com/xdrip_miband
Mehr über seine Projekte bezüglich xdrip können Sie hier lesen: https://bigdigital.home.blog/

Außerdem vielen Dank an:

 - [**SashaCX75**](https://amazfitwatchfaces.com/forum/memberlist.php?mode=viewprofile&u=113690) für die Hilfe bei der Erstellung des Watchfaceditors 
 - alle watchface-Ersteller


> 

### Beispiel Watchface


Im Ordner [01-WF-MD225-Version3-xdrip-ready](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/01-WF-MD225-Version3-xdrip-ready
"01-WF-MD225-Version3-xdrip-ready") finden Sie das Endprodukt eines eigenen Watchfaces. Ich werde hier ein anderes Repository mit einem anderen Watchface verlinken, das ich später erstellt habe. 

**Wenn Sie Ihr eigenes Watchface erstellt haben, teilen Sie es bitte mit anderen. Wir könnten sie in einem Repository sammeln, zögern Sie nicht, mich via issue zu kontaktieren.


## Dinge, die Sie brauchen

Ich werde die folgenden Tools verwenden. Du wirst sie alle brauchen. Alle unten aufgeführten Tools sind für den persönlichen Gebrauch kostenlos.

1. Windows-Betriebssystem
2. **WFE**: [AmazFit WatchFace editor 2 für Windows](https://amazfitwatchfaces.com/forum/viewtopic.php?p=8392#p8392)
3. **PS**: Photoshop (Version CS2 ist kostenlos erhältlich) https://archive.fo/255q5#selection-1663.0-1663.29
5. **WF**: Ein Watchface. (nächstes Kapitel)
6. Laden Sie das gesamte Repository herunter, wir werden später einige Dateien aus dem Ordner "Guide" benötigen. Sie können dieses Repository herunterladen, indem Sie auf den grünen "Code"-Button oben auf dieser Seite klicken und "Download ZIP" wählen.

## Suchen Sie nach einem Watchface, das Sie verwenden möchten

Wenn Sie kein eigenes Watchface erstellen wollen, können Sie hier nach Watchfaces suchen: https://amazfitwatchfaces.com/gtr/top?compatible=GTR_2
Donwloaden Sie die gewünschte Datei. Bitte achten Sie darauf, für welche Uhr das Watchface erstellt wurde.

**Etwas sehr Wichtiges:** 

 - Je kleiner das Watchface ist, desto besser. Wir kommen später darauf zurück, aber alle Bilder inklusive der json-Datei sollten nicht größer als 50kb sein. 
 - Eine Größe von 50kb (rohe Bilder und die json-Datei) führt zu einer Ladezeit von ca. 10 Sekunden und Sie wollen nicht, dass es länger dauert, wegen der Batterielebensdauer und Sie wollen nicht bis morgen warten.
 - Das bedeutet weniger Icons, weniger wechselnde Dinge (außer Zahlen, und ja, nur Zahlen). 
 - Vermeiden Sie Zifferblätter mit Farbverläufen (wenn eine Farbe in eine andere übergeht). 
 - Denken Sie daran, dass wir in der Lage sein wollen, unseren Blutzucker leicht abzulesen, also müssen wir irgendwo etwas Platz schaffen. Ich würde mindestens 1/3 der Oberfläche für alle xdrip-bezogenen Informationen vorsehen

# 1. Anleitung / Tutorial

1. Laden Sie den gesamten Ordner mit der neuesten Version des WFE (watchface editor) herunter, der oben verlinkt ist. 
2. Sie finden den "download"-Button oben rechts, wir brauchen den ganzen Ordner! 
3. Nach dem Anklicken von download wählen Sie "direct download". Es wird eine Datei wie "AmazFit_Watchface_Editor_2_v5.1.zip" heruntergeladen.
4. Entpacken Sie die Datei
5. Öffnen Sie (in meinem Fall) "AmazFit_Watchface_Editor_2".
6. Starten Sie "AmazFit_Watchface_Editor_2.exe".
7. Buttom rechts, wähle "Entpacken der komprimierten Bin".
8. Wählen Sie das Watchface, das Sie zuvor heruntergeladen haben
9. Das entpackte Watchface finden Sie hier: ...\AmazFit_Watchface_Editor_2\Watch_face
10. Nun müssen Sie sich mit dem WFE vertraut machen.
11. Ich werde nur die absoluten Grundlagen erläutern. Um mehr über den Watchface-Editor und seine Möglichkeiten zu erfahren, schauen Sie bitte hier: https://amazfitwatchfaces.com/forum/viewtopic.php?f=14&t=1571
Direkter Link zur englischen Übersetzung: https://translate.google.com/translate?hl=ru&sl=ru&tl=en&u=https%3A%2F%2Fowagner.ru%2Famazfitgtr%2Fwfcreator%2Fwatchfaces_creator_lesson%2F
12. Gehen Sie auf den Reiter "Bearbeiten" und klicken Sie sich durch die verschiedenen Optionen auf der rechten Seite. 
13. Wählen Sie "Ebenenreihenfolge", um Dinge wie die Datumsreihenfolge zu definieren (tt-mm-jj oder mm-tt-jj).

> **Wichtiger Hinweis:** 
> Unser wichtigstes Ziel ist es, die Größe zu reduzieren. Wie geschrieben
> oben geschrieben, wollen wir unter 50kb rohe png-Dateien (einschließlich .json) bekommen.
> 
> Der beste Weg, die Größe zu reduzieren:
> - weniger Bilder
> - weniger Farben (ergibt kleinere Bilddateien)
> - Systemschriftart verwenden (eine Einstellung auf der Registerkarte "Bearbeiten" von WFE, wo immer Zahlen angezeigt werden).

14. Wenn Sie mit Ihren Änderungen fertig sind, speichern Sie das Watchface (Reiter "Bearbeiten", unten in der Mitte "Json speichern")

> **Die Dinge, die mir sehr geholfen haben:**
> - Bild 0001.png ist immer der Hintergrund. Normalerweise ist es notwendig, den Hintergrund so anzupassen, dass er zu einem Glukose-Diagramm und allen benötigten Daten passt. Verwenden Sie dazu Photoshop oder ein anderes Programm
> - Schauen Sie sich die entpackten Bilder an, löschen Sie alle, die Sie nicht brauchen.
> - Sie müssen die Dateien von 0001- xxxx umbenennen. Sie werden später Probleme bekommen, wenn die Dateien nicht in einer Reihe stehen. Es ist nicht möglich, dass eine
> Nummer dazwischen fehlt. Es sollte wie folgt aussehen: 0001, 0002, ......
> 0015.) Sie können https://www.bulkrenameutility.co.uk/Download.php verwenden, um Dateien massenhaft umzubenennen.

15. Wechseln Sie zu dem Ordner, der die json-Datei und alle benötigten Dateien auf Ihrem Computer enthält.
16. Erstellen Sie ein Backup der vorhandenen Dateien und der json-Datei.

## 1.1 Bearbeiten des Hintergrunds Ihres Ziffernblatts
Wenn Ihr Zifferblatt eine einfarbige Farbe hat, können Sie diese in der WFE bearbeiten. Aber du musst ein Bild erstellen, auf dem das xdrip Datum platziert wird, also erstelle ein farblich passendes Bild in PS und überspringe den folgenden Teil, wo ich beschreibe, wie man das Bild ausschneidet.

17. Öffne 0001.png (dein Hintergrundbild) in PS
18. Gehe zu Bild-->Modus und ändere es zurück zu RGB
19. Wähle das Rechteck-Werkzeug durch Drücken von "M" und wähle den Teil, in dem deine xdrip-Daten angezeigt werden sollen.
![##**PS_cut_xdrip_part_01.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_01.PNG)

20. Klicken Sie mit der rechten Maustaste hinein und wählen Sie "Ebene durch Ausschneiden".
21. Speichern Sie diese Datei als PS-Datei (.psd)
22. Blenden Sie den Rest des Bildes aus, indem Sie auf das Augensymbol auf der rechten Seite (Ebenen) auf Ebene 1 klicken
![## **PS_cut_xdrip_part_02.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_02.PNG)
23. Drücken Sie "c", um das Schneidewerkzeug zu benutzen.
24. Schneide das Bild auf die Größe des sichtbaren Teils deines Ziffernblatts zu.
25. Drücken Sie zur Bestätigung die Eingabetaste oder das Häkchen im oberen Bereich
26. Speichern Sie das Bild unter dem Namen **mein_bild.png**.
27. Öffnen Sie die gespeicherte psd-Datei und machen Sie dasselbe mit dem Rest des Ziffernblatts, so dass wir das Hintergrundbild in 2 Dateien aufgeteilt haben.


### 1.1.1 Bildgröße reduzieren
28. Öffnen Sie jede Datei, eine nach der anderen, mit PS.
29. Klicken Sie auf Daten--> Für Web speichern
30. In dem neuen Fenster solltest du auf der rechten Seite folgendes auswählen:
	- png-8
	- Sie können ein wenig herumprobieren und bestimmte Farben löschen, um die Größe des Bildes noch weiter zu verringern. Sie können die neue Dateigröße unten rechts sehen.
	- Die Dateien müssen im png-Format vorliegen! 
	- Wenn Sie einen seltsamen Rand um Ihre Bilder haben:
		- Gehe auf Bild, Modus und ändere es in "indizierte Farben", bevor du es für das Web speicherst.
31. Speichern Sie die Datei durch Überschreiben (Sie haben vorher ein Backup gemacht). Ich habe keine Möglichkeit gefunden, dies für alle Dateien auf einmal zu tun, lassen Sie es mich wissen, wenn Sie wissen, wie.

### 1.1.2 Platzieren Sie my_image.png an der richtigen Stelle in der WF
32. Wenn Sie nun WFE wieder öffnen, sollten Sie bemerken, dass wir einen Ausschnitt in der Mitte des Zifferblattes haben. (falls nicht, speichere das ausgeschnittene Bild als Hintergrundbild)
33. Navigiere zu Bearbeiten--> Aktivität -->Fettverbrennung-->Symbol
34. Kopiere das folgende Bild hierher: ## GTR-2-WF-Xdrip-EN/[Guide](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/Guide)/**0099.png** es ist nur 1 Pixel. Wir werden es später per Code durch das my_image.png ersetzen. Aber das spart uns eine Menge Watchface-Größe.
35. Jetzt müssen wir es in der linken oberen Ecke unseres Ausschnitts platzieren. Um die richtigen Koordinaten zu finden, lesen Sie das folgende Thema (Wie man die richtigen Koordinaten in PS findet)

## 1.2 Vorbereiten des endgültigen Zifferblattes
Was Sie bis jetzt in 1 Ordner haben sollten:
- eine json-Datei, die Sie mit WFE erstellt haben
- alle benötigten WF-Dateien, maximal in der Größe reduziert
- my_image.png, maximal verkleinert
--> wir nähern uns der endgültigen WF :)

36. Navigieren Sie zu ....\AmazFit_Watchface_Editor_2\Tools
37. halten Sie Shift+Rechtsklick in diesem Ordner
38. Wählen Sie "Powershell-Fenster hier öffnen".
39. Um dein json zu packen, musst du nur zum tools-Ordner navigieren und den Befehl wie folgt ausführen  
main.exe --gtr2 47 --file config-file.json`, wobei config-file.json ein Speicherort für die json-Datei ist.
	- Ich hatte ein paar Probleme damit und musste den ganzen Pfad vor der main.exe hinzufügen, so dass es etwas wie das folgende war:
		- C:\Benutzer\twinko\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Tools\main. exe --gtr2 47 --file C:\Users\TwinkosTower\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Watch_face\gtr2-g7en-colormix03-346659-994092c337\Small\WF_2_V01.json`
40. Als Ergebnis sollten Sie eine entpackte bin-Datei erhalten. Diese Datei müssen Sie dann in xdrip verwenden. Xdrip injiziert die benötigten Ressourcen in diese Datei, komprimiert sie und sendet sie an die Uhr.
41. Benennen Sie die bin-Datei um in: my_watchface.bin
42. Erstellen Sie einen neuen Ordner und fügen Sie die folgenden Dateien ein:
- die von uns erstellte my_watchface.bin
- mein_bild.png



## 1.3 Bearbeiten der config.json

Die config.json definiert, wo auf der my_image.png welche xdrip-Daten wie angezeigt werden. Sie unterscheidet sich von der json, die vom WFE erstellt wird, nicht verwechseln!

Die originale config.json, die Artem erstellt hat, ist hier verlinkt:
https://github.com/twinko/GTR-2-WF-Xdrip-EN/blob/main/Guide/config.json
Sie haben das Repository bereits heruntergeladen, holen Sie sich die Datei aus dem Guide-Ordner!



> **Allgemeines, was man wissen sollte:**
> - diese config.json bezieht sich nur auf my_image.png
> - Wenn wir also über Koordinaten (x und y) sprechen, basiert das auf my_image.png und seiner Gesamtgröße, nicht auf dem gesamten Watchface
> - lesen Sie Artems Beitrag über die Ausrichtung hier: https://github.com/bigdigital/xDrip-miband/issues/5#issuecomment-878008056
> - text_align: "rechts" 
> - man muss die Pixel von der rechten Seite aus zählen
> - wenn es also heißt: x: 100 und text_align ist rechts, zählt man 100 Pixel von der rechten Seite des Bildes, wo das Element platziert wird

### 1.3.1 Wie findet man die richtigen Koordinaten in PS
43. Öffnen Sie mein_Bild.png in PS
44. Drücken Sie F8, ein kleines Infofenster wird angezeigt
45. Wenn du mit der Maus über das Bild fährst, siehst du, wie sich die X- und Y-Zahlen bewegen. 

### 1.3.2 config.json erklärt
46. Öffnen Sie die config.json mit notepad
47. Sie sehen kleine Cluster, die ziemlich selbsterklärend sind
48. Wir müssen nur resource_to_replace, X, Y font_size vielleicht bg_color des Graphen bearbeiten

#### 1.3.2.1 resource_to_replace
49. Geben Sie die Nummer des Bildes ein, das wir für Fettverbrennung-->Icon gewählt haben (wenn Ihr erstes Bild 0001.png heißt, reduzieren Sie die Zahl um eins. Der Algorithmus beginnt die Zählung bei 0)

#### 1.3.2.2 "x" , "y" und "text_align": "rechts",
50. Wie in "Wie finde ich die richtigen Koordinaten in PS" beschrieben, können Sie die richtige Position für Ihre xdrip-Daten finden. 

> **Hinweis**: Die Systemschriftart ist "Segoe UI", also drücken Sie t in PS, um Text zu schreiben und
> fügen Sie einen Standardtext in Ihre my_image.png ein und suchen Sie die richtigen
> Koordinaten. Denke daran, dass *x und y die untere linke Seite des ersten
> Buchstaben/Zahl*. Speichern Sie die Datei my_image.png nicht mit den Zahlen, die Sie
> aufgeschrieben haben, das wird später von Artems Magie erledigt, wir machen das in PS
> um die richtigen Koordinaten herauszufinden, sonst nichts.

51. Ändern Sie nun alle Koordinaten nach Ihren Bedürfnissen.
52. Achtung: es gibt einige Werte, die die folgende Zeile haben: `"text_align": "right",` für diese haben wir eine andere Regel für die Koordinaten. *Füge die Buttom-Koordinate des letzten Buchstabens/der letzten Zahl ein.

#### 1.3.2.3 "font_size"
53. Geben Sie die gleiche Schriftgröße ein, die Sie in PS gewählt haben.

### 1.3.3 Speichern Sie die config.json
54. Speichern Sie die config.json in den Ordner mit der my_image.png und der my_watchface.bin (config.json nicht my_config.json!)


## 1.4 Hochladen und Testen

55. Wir sollten jetzt einen Ordner mit den folgenden Dateien haben:
- config.json 
- mein_bild.png 
- my_watchface.bin  
56. Füge diese 3 Dateien in den xdrip-Ordner auf deinem Smartphone ein 
- Der benötigte xdrip-Ordner befindet sich hier:
	- Internatspeicher/xdrip oder
	- root/storage/emulated/0/xdrip
57. Aktivieren Sie das benutzerdefinierte Watchface in den xdrip-Einstellungen.
58. Erledigt!

# 2. Fußnote

Bitte eröffne hier ein Thema, wenn du auf Probleme stößt. Bitte recherchieren Sie vorher selbst, ich bin auch nur ein normaler Mensch, der das in seiner Freizeit macht. 
https://github.com/twinko/GTR-2-WF-Xdrip-EN/issues

Wenn ihr Vorschläge habt, wie man die Anleitung verbessern kann oder wie man sie auch für andere Watchfaces verwenden kann, dann schreibt bitte ebenfalls ein Issue :)

Ich hoffe diese Anleitung war hilfreich :)