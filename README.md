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

  
  ## Die Spielidee <a name="Spielidee"></a>


### Das Grundprinzip <a name="Grundprinzip"></a>

   Das Grundprinzip des Mirror Games besteht darin, dass ein Laserstrahl von einem Sender ausgestrahlt wird und mit der Hilfe von 
   Spiegeln, dessen Winkel der Spieler verstellen kann so abgelenktwird, dass der Laser auf einen Empfänger treffen kann. 
   Das Spiel besteht aus acht Leveln. Die Schwierigkeitsstufe steigt im Verlauf des Spiels, in dem Hindernisse umgangen werden müssen
   und mehr Spiegel hinzugefügt werden. 
   Bei Abschließen eines Levels wird automatisch das nächste Level gestartet.
   
   
   ## Der Aufbau <a name="Aufbau"></a>

![skizzespiegelgame](https://user-images.githubusercontent.com/42579285/51129379-9c362d00-182a-11e9-9421-87373cbd7f21.png)


### Startbildschirm, Levelauswahl und Endbildschirm
   
   Das Spiel beginnt mit einem schlichten Startbildschirm, der nur den Namen des Spiels und einen Startbutton enthält.
   
   ![startbildschirm](https://user-images.githubusercontent.com/42579285/52284035-f3c84400-2963-11e9-9d08-2bce29d4f387.png)
   
   Dazu wird der folgende Block in das Script der Stage eingefügt, um alle Sprites bis auf den Startbutton zu hiden und den Background
   Startbildschirm sichtbar zu machen.
   
   ![startbildschirmskript](https://user-images.githubusercontent.com/42579285/52284041-f62a9e00-2963-11e9-8ca8-b5e8fae46c72.png)
   
   Beim anklicken des Startbuttons wird die Größe angepasst und der Befehl "Start" gebroadcasted.
   
   Dies hat zur Folge, dass 
   Die einzelnen Sprites, die mit einem passenden Level costume ausgestattet sind, empfangen ebenfalls diesen Befehl, werden sichtbar
   und ordnen sich ihre vorher bestimmte Position zu. 
   
   ![levelauswahl](https://user-images.githubusercontent.com/42579285/52294381-790a2380-2979-11e9-9fcb-4c54e333833e.png)

https://scratch.mit.edu/projects/239667020/#editor

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
 
 ![regenbogen](https://user-images.githubusercontent.com/42579285/50080722-07b9ba00-01ed-11e9-8d04-2fd8a6d8e229.png)

![bil d3](https://user-images.githubusercontent.com/42579285/50164155-3796b980-02e2-11e9-9115-ed1e9642fe88.png)

#### Zum Arbeitstagebuch (https://github.com/LeoandTeda/-/blob/master/Arbeitstagebuch.md)
