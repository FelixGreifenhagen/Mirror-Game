# Informatik Projekt Nr.2 : The Mirror Game
*von Teda und Leonard, 12e*

## Inhaltsverzeichnis

* [Programm](#Programm)
* [Aufbau](#Aufbau)
  * [Grundprinzip](#Grundprinzip)
  * [Start und Ende](#Start-und-Ende)
* [Wichtige Objekte](#Wichtige-Objekte)
  * [Spiegel](#Spiegel)
  * [Laser](#Laser)
  * [Sender](#Sender)
  * [Empfänger](#Empfänger)
  * [Hindernisse](#Hindernisse)
* [Extras](#Extras)  
  * [Anleitung](#Anleitung)
  * [Münze](#Münze)
* [Arbeitstagebuch](https://github.com/LeoandTeda/-/blob/master/Arbeitstagebuch.md) 
  
## Das Programm <a name="Programm"></a>
  
![image](https://user-images.githubusercontent.com/42579285/48960806-160b1200-ef70-11e8-82f8-a4498ecd9050.png)
  
Um unser Projekt zu programmieren haben wir das Programm snap! benutzt, da dies besonders für Anfänger gut geeignet ist, da keine Kenntnisse in einer Programmiersprache für die Verwendung vorausgesetzt werden. Snap vereinfacht dabei den Quellcode in Blöcke, welche je nach belieben zusammengeheftet werden können. Dabei werden Fehler anders als beim normalen programmieren schnell erkannt und es werden zudem viele Tipps sowie Anleitungen gegeben. Snap beruht dabei auf einer sehr visuellen Programmiersprache.
  
   
## Der Aufbau <a name="Aufbau"></a>

### Das Grundprinzip <a name="Grundprinzip"></a>

 Das Grundprinzip des Mirror Games besteht darin, dass ein Laserstrahl von einem Sender ausgestrahlt wird und mit der Hilfe von 
 Spiegeln, dessen Winkel der Spieler verstellen kann so abgelenkt wird, dass der Laser auf einen Empfänger treffen kann. 
 Das Spiel besteht aus acht Leveln. Die Schwierigkeitsstufe steigt im Verlauf des Spiels, indem Hindernisse umgangen werden müssen
 und mehr Spiegel hinzugefügt werden. 
 Bei Abschließen eines Levels wird automatisch das nächste Level gestartet.
![skizzespiegelgame](https://user-images.githubusercontent.com/42579285/51129379-9c362d00-182a-11e9-9421-87373cbd7f21.png)


### Start und Ende <a name="Start und Ende"></a>
   
  Das Spiel beginnt mit einem schlichten Startbildschirm, der nur den Namen des Spiels und einen Startbutton enthält.
   
   ![startbildschirm](https://user-images.githubusercontent.com/42579285/52284035-f3c84400-2963-11e9-9d08-2bce29d4f387.png)
   
  Dazu wird der folgende Block in das Script der Stage eingefügt, um alle Sprites bis auf den Startbutton zu hiden und das Costume des
  Background Startbildschirm sichtbar zu machen.
   
 ![startbildschirmskript](https://user-images.githubusercontent.com/42579285/52297876-fb96e100-2981-11e9-8181-663dbbb6b693.png)

   
  Beim Anklicken des Startbuttons wird die Größe angepasst und der Befehl "Start" gebroadcasted.
   
  Im Script der Stage wird beim Empfangen dieses Befehls der Wechsel zum Costume Levelauswahl angefordert.
  Die einzelnen Sprites, die mit einem passenden Levelcostume ausgestattet sind, empfangen ebenfalls diesen Befehl, werden sichtbar
  und ordnen sich ihre vorher bestimmte Position zu. 
   
   ![levelauswahl](https://user-images.githubusercontent.com/42579285/52294381-790a2380-2979-11e9-9fcb-4c54e333833e.png)
   
   ![levelscript](https://user-images.githubusercontent.com/42579285/52294887-b7541280-297a-11e9-91ed-872bf72574df.png)
   
  Der zweite Block wird wichtig sobald der Spieler sich für eins der Level entscheidet. Sobald ein Level Button angeklickt wird, wird
  eine Nachricht mit dem jeweiligen Levelnamen gebroadcastet. Im Script der Stage wird der zugehörige Block aktiviert, der die
  Levelbuttons hidet und die Spiegel, Hindernisse, den Sender und den Empfänger sichtbar werden lässt. Zusätzlich wird auch der
  Background der Stage zu Empty geändert.
   
  ![levelscript2](https://user-images.githubusercontent.com/42579285/52295635-a0162480-297c-11e9-9d6b-22289dc0407f.png)
   
  Außerdem wird neben dem Levelnamen der Befehl Gamestart gebroadcastet. Dieser hat zur Folge, dass das eigentliche Spiel, je nach
  Level mit einem anderen Design gestartet wird. 
   
  Der wohl entscheidenste Teil des Blocks ist allerdings, dass die Variable Level auf die jeweilige Zahl des Levels gesetzt wird.
   
  Wird bei der Levelauswahl der Button "coming soon" geklickt, wird der Spieler zurück zum Startbildschirm geführt.
   
  ![comingsoonscript](https://user-images.githubusercontent.com/42579285/52297989-34cf5100-2982-11e9-9a12-f108b3f36a27.png)
   
   
## Wichtige Objekte <a name="Wichtige-Objekte"></a>

### Die Spiegel <a name="Spiegel"></a>

Die Spiegel spielen in diesem Projekt die Hauptrolle und geben dem Spiel auch seinen Namen. Dabei erfüllen sie mehrere Kriterien. Zum einen lassen sie sich per Maus bewegen, zum anderen reflektieren sie den Laserstrahl. Um dies zu verwirklichen wurden mehrere Funktionen aus Snap benutzt.

Angefangen mit der Anzahl der Spiegel, welche erscheinen sollen. So wird bei Beginn jedes Levels die Anzahl der Spiegel auf fünf gesetzt.

![Unbenannt](https://user-images.githubusercontent.com/42579285/55480872-7e09ed00-5621-11e9-8b3c-657ff11a92ad.png)

Dabei werden wie im Screenshot sichtbar fünf Klone des Spiegels erstellt, undzwar mit der "create a clon of myself" Funktion. Wird nun ein Level ausgewählt, steigt die Level Variable auf den ausgewählten Wert. Ist nun zum Beispiel Level = 1 wird folgender Block aktiviert:

![Unbenannt](https://user-images.githubusercontent.com/42579285/55481140-04263380-5622-11e9-9d8c-07e541fe8a41.png)

Dieser legt fest, wie viele Spiegel im Level erscheinen. In diesem Fall sind es zwei Spiegel und die restlichen drei Stück werden mit dem befehl "delete this clone" gelöscht. Zudem werden die Richtung, sowie die X- und Y-Position jedes Spiegels in unterschiedlichen Listen gespeichert, was für den weiteren Verlauf noch wichtig ist. Solch ein Block wurde für jeweils alle acht Level erstellt und unterscheidet sich nur inder Anzahl der Spiegel.

Die nächsten zwei großen Hauptblöcke sorgen dafür, dass sich jeder Spiegel individuell bewegen lässt:

![Unbenannt](https://user-images.githubusercontent.com/42579285/55481891-9f6bd880-5623-11e9-8d2a-52fd7fc23fd3.png)
![Unbenannt](https://user-images.githubusercontent.com/42579285/55481932-bca0a700-5623-11e9-8f60-a59bf7775e2c.png)

Auch hier bietet Snap wieder mehrere Funktionen, welche zum gewünschten Ziel führen. Mithilfe von "when I start as a clone" wird jeder Spiegel einzelnd betrachtet. Hinzu kommen "touching.." Funktionen, welche feststellen, ob die Spiegel gerade durch die Maus bewegt werden sollen. Das ganze Verfahren ist dabei sehr kompliziert, damit sich die Spiegel richtig bewegen und lässt sich nur mithilfe mehrerer Variablen, sowie Listen, als auch Control Befehlen bewerkstelligen. Der ganze Block wird dabei von einer "forever" Klammer umspannt, da dies die ganze Zeit gilt und nicht nur einmal.

Der gesamte Script Bereich der Spiegel wird dabei durch drei kleine Blöcke abgerundet, welche dafür sorgen, dass falls der Spieler das Level geschafft hat oder zurück zum Homescreen möchte, die einzelnen Spiegelklone wieder gelöscht werden mithilfe von "delete this clone".

![Unbenannt](https://user-images.githubusercontent.com/42579285/55482910-cb885900-5625-11e9-8049-2dbc2813ccd7.png)

### Der Laser <a name="Laser"></a>

Das zweitwichtigste nach den Spiegeln ist der Laser, welcher durch die Spiegel reflektiert wird, an Hindernissen vorbeikommen muss und schlussendlich den Empfänger erreichen soll. Dies gestaltet sich in schwerer als gedacht, da es keine "Laser Funktion" gibt. Deshalb wird die Pen Funktion benutzt, welche eigentlich als Zeichentool gedacht ist.

![Unbenannt](https://user-images.githubusercontent.com/42579285/55483238-79940300-5626-11e9-8f71-4335709f9234.png)
![Unbenannt](https://user-images.githubusercontent.com/42579285/55483392-c4157f80-5626-11e9-85d4-7795fa0fe32e.png)

Wie man schon an Hand der Screenshots sehen kann, besteht der Laser aus einem sehr großen Block und einem etwas kleineren. Der große Block ist der Rote Laser in Form einer roten Linie. So wird durch "set.." die Laser Länge und Größe festgelegt. Außerdem wird mit dem Block Laser-Level-Position die Startposition des Lasers für jedes Level festgelegt. Dies geht mithilfe der "Make a Block" Option in Snap:

![Unbenannt](https://user-images.githubusercontent.com/42579285/55483782-9f6dd780-5627-11e9-96cd-83d25a1f5783.png)

Dadurch wird der Block nicht noch länger. Danach wird ein Klon erschaffen, welche in die festgelegt Richtung fliegt, solange er nicht auf ein Hindernis, einen Spiegel oder den Spielrand trifft. Trifft er auf ein Hindernis oder den Spielrand verschwindet der Strich. Falls er aber auf einen Spiegel trifft wird der Strich reflektiert mithilfe von der Richtung des Spiegels, sowie des Striches. Erreicht der Strci sein Ziel, also "touching Empfänger" wird das Spiel geresetet und alle Daten aus den Listen werden durch "delete all.." gelöscht.

Um nun aus dem Strich einen Laser zu machen, wird der zweite kleinere Block benötigt. Dieser ist auch ein Klon des Lasers ist aber weiss und startet 0,1 Sekunden verspätet. Dadurch folgt ein weisser Strich einem roten, was dazu führt, dass eine Art Laser entsteht. Dieser weisse Strich hat einen sehr ähnlichen Fuktionsaufbau, wie der rote und wird auch an den Spiegeln reflektiert.

### Der Sender <a name="Sender"></a>


### Der Empfänger <a name="Empfänger"></a>


### Die Hindernisse <a name="Hindernisse"></a>



## Extras <a name="Extras"></a>

### Die Anleitung <a name="Anleitung"></a>

 Um dem Spieler einen groben Überblick über das Spielprinzip zu ermöglichen, wird eine kurze Spielanleitung eingefügt. 
 Die Möglichkeit diese einzusehen besteht, wenn sich der Spieler auf der Levelübersicht befindet. 
 Dafür wird ein Sprite mit einem Fragezeichen costume angelegt (Hilfe!). Dieses hat jeglich die Funktion bei erhalten der Nachricht
 "Start" an die gewünsche position zu gehen und bei anklicken des Sprites "Anleitung" zu broadcasten.  
 
 ![Informatik](https://user-images.githubusercontent.com/42579285/55668557-1398bd00-586c-11e9-922e-787166cfb9f2.png)

 Die Anleitung an sich ist ein weiterer Sprite, allerdings ohne costume, dass ausschließlich auf den gebroadcasteten Befehl Anleitung reagiert. Sobald dieser Empfangen wird positioniert sich die Anleitung und es wird mit dem Befehl "say..." gearbeitet. Da die Anleitung nicht in ein Textfeld passt, muss noch eingebaut werden, dass bei anklickendes Textes der weitere Text sichtbar wird.
 Sobald wieder auf den Homebutton geklickt wird, wird der Spieler wie immer zur levelauswahl zurückgeführt.


#### [Zum Arbeitstagebuch](https://github.com/LeoandTeda/Mirror-Game/blob/master/Arbeitstagebuch.md)
