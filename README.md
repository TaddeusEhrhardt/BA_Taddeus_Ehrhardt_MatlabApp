# Anleitung Mathlab-App

! Achtung: Die entwickelte App befindet sich in einem frühen Stadium der Entwicklung. Es gibt nicht genügen Fehlerüberwachung und eine weiterentwicklng wird empfohlen
## 1.	Medien laden

<ol type="a">
  <li>mind. 2 Aufnahmen von 10x10 mm Schachbrettmuster über „Checkerboard Calibration“ laden – warten bis sich Vorschau Fenster öffnet (kann geschlossen werden)</li>
  <li>„Select FORWARD Sequence“  Bildfolge Vorwärtsverformung laden (Mehrfachauswahl im Explorer)</li>
  <li>„Select BACKWARD Sequence“  Bildfolge Zurückverformung laden (Mehrfachauswahl im Explorer)</li>
</ol>

## 2.	automatisierter Zuschnitt
<ol type="a">
  <li>„Select Origin and Axis“  manuelle Auswahl der Fixpunkte (0,0), (200,0), (0,200) in ersten Bild der Vorwärts-Reihe</li>
  <ul>
    <li>Fenster öffnet sich -> beliebiger Punkt kann vermessen werden -> Ausgabe der Koordinaten in Matlab-Konsole</li>
    <li>Auswahl des Ursprungs und der Achsen kann wiederholt werden (überschreibend)</li>
  </ul>
  <li>„Apply ROT / CROP“ – Anwenden der Rotation und des Zuschnittes der Bildateien im Zwischenspeicher, 
    Achtung: nach dem zuschnitt neu geladene Bilder müssen erst erneut zugeschnitten werden. 
    Ein Neustart der App und somit ein Löschen des Zwischenspeichers wird vor dem Laden neuer Bilderreihen empfohlen, da keine interne Überprüfung stattfindet.</li>
</ol>
    
## 3.	Tracking und Export
<ul>
  <li>„Tracking“ initialisiert den Trackinprozess für alle geladenen Bilder (vorwärts und rückwärts), darf erst NACH dem Zuschnitt erfolgen! 
    Sollte der Trackingpunkt nicht zuverlässig oder fehlerhaft erkannt werden, kann es sein, dass eine Anpassung der Parameter des Histogrammbasierten Trackers notwendig ist (createMask())</li>
  <li>Download-Button -> Export einer .csv Datei mit sequenziellen Positionen aus vor- und Rückwärtsverformung des getrackten Punktes</li>
</ul>

## 4.	Weitere Funktionen

<ul>
  <li>Pipetten-Button -> Vermessen eines beliebigen Punktes, Ergebnisanzeige im Hauptfenster neben dem Button nach Auswahl in der Vorschau.</li>
  <li>Abspielen der Vorwärts-Sequenz aus dem zwischenspeicher (mit oder ohne Zuschnitt) mit optionaler Anzeige des Tracking Ergebnisses</li>
</ul>


## Empfohlene Anpassungen / Erweiterungen / To-Dos:

<ul>
  <li>Einzelner Export vorwärts/rückwärts-Koordinaten</li>
  <li>Debug-Funktionen</li>
  <li>mehr Fehlerkontrolle</li>
  <li>Informationen über geladene Bilddateien anzeigen lassen (Anzahl, Dateinamen, etc in Tabelle o.Ä)</li>
  <li>Vollständig automatischer Zuschnitt</li>
</ul>



