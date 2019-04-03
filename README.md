# Informatik Projekt Nr.2 : The Mirror Game
*von Teda und Leonard, 12e*

## Inhaltsverzeichnis

* [Programm](#Programm)
* [Spielidee](#Spielidee)
* [Aufbau](#Aufbau)
  * [Grundprinzip](#Grundprinzip)
* [Arbeitstagebuch](https://github.com/LeoandTeda/-/blob/master/Arbeitstagebuch.md) 
  
## Das Programm <a name="Programm"></a>
  
![image](https://user-images.githubusercontent.com/42579285/48960806-160b1200-ef70-11e8-82f8-a4498ecd9050.png)
  
Um unser Projekt zu programmieren haben wir das Programm snap! genutzt, da dies besonders für Anfänger gut geeignet ist, da keine Kenntnisse in einer Programmiersprache für die Verwendung vorausgesetzt werden. Snap vereinfacht dabei den Quellcode in Blöcke, welche je nach belieben zusammengeheftet werden können. Dabei werden Fehler anders als beim normalen programmieren schnell erkannt und es werden zudem viele Tipps sowie Anleitungen gegeben. Snap beruht dabei auf einer sehr visuellen Programmiersprache.
  
## Die Spielidee <a name="Spielidee"></a>
   
   
## Der Aufbau <a name="Aufbau"></a>

### Das Grundprinzip <a name="Grundprinzip"></a>

   Das Grundprinzip des Mirror Games besteht darin, dass ein Laserstrahl von einem Sender ausgestrahlt wird und mit der Hilfe von 
   Spiegeln, dessen Winkel der Spieler verstellen kann so abgelenktwird, dass der Laser auf einen Empfänger treffen kann. 
   Das Spiel besteht aus acht Leveln. Die Schwierigkeitsstufe steigt im Verlauf des Spiels, in dem Hindernisse umgangen werden müssen
   und mehr Spiegel hinzugefügt werden. 
   Bei Abschließen eines Levels wird automatisch das nächste Level gestartet.
![skizzespiegelgame](https://user-images.githubusercontent.com/42579285/51129379-9c362d00-182a-11e9-9421-87373cbd7f21.png)


### Startbildschirm, Levelauswahl und Endbildschirm
   
   Das Spiel beginnt mit einem schlichten Startbildschirm, der nur den Namen des Spiels und einen Startbutton enthält.
   
   ![startbildschirm](https://user-images.githubusercontent.com/42579285/52284035-f3c84400-2963-11e9-9d08-2bce29d4f387.png)
   
   Dazu wird der folgende Block in das Script der Stage eingefügt, um alle Sprites bis auf den Startbutton zu hiden und das Costume des
   Background Startbildschirm sichtbar zu machen.
   
 ![startbildschirmskript](https://user-images.githubusercontent.com/42579285/52297876-fb96e100-2981-11e9-8181-663dbbb6b693.png)

   
   Beim anklicken des Startbuttons wird die Größe angepasst und der Befehl "Start" gebroadcasted.
   
  Im Script der Stage wird beim Empfangen dieses Befehls der Wechsel zum costume Levelauswahl angefordert.
   Die einzelnen Sprites, die mit einem passenden Level costume ausgestattet sind, empfangen ebenfalls diesen Befehl, werden sichtbar
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
   
   Wird bei der Levelauswahl der Button coming soon geklickt, wird der Spieler zurück zum Startbildschirm geführt.
   
   ![comingsoonscript](https://user-images.githubusercontent.com/42579285/52297989-34cf5100-2982-11e9-9a12-f108b3f36a27.png)
   
   

Plan: Spiegelspiel:
-mehrere Level
-Einfach->Schwer (mehr Spiegel/Hindernisse)
-Versuche?
-Startbildschirm+Endbildschirm
-Menü (Einstellungen)
-Spiegel einstellen:
  -Winkel
  -(Verschieben)
  -Laserstrahl reflektiert
 


#### [Zum Arbeitstagebuch](https://github.com/LeoandTeda/Mirror-Game/blob/master/Arbeitstagebuch.md)
