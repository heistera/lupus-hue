# lupus-hue

!! Steuere Philips Hue Lichter über die LUPUS XT+ Alarmanlage !!

Die LUPUS XT2+ Alarmanlage bietet u.a. auch eine Reihe von Home Automation Regeln, um verschiedene Aspekte eines intelligenten Heims
zu steuern. Unter anderem ist es möglich Lichter oder andere Verbraucher über die Unterputzrelais oder die Funksteckdosen zu schalten.

Das ist eine tolle Funktion für die Simulation einer Anwesenheit wenn die Anlage scharf gestellt wird. Bei einer großen Anzahl von
Lichtern geht das aber schnell ins Geld und hat auch eine Reihe von Einschränkungen:

- Lichter können nur ein- und ausgeschaltet werden (keine Farben, Lichttemperatur, Szenen, Übergänge etc.)
- Das Dimmen mit dem LUPUS Unterputzrelais mit Dimmerfunktion funktioniert zumindest bei mir nicht zufriedenstellend
- Die gegenwärtigen Home Automation Regeln bei LUPUS sind sehr eingeschränkt, insbesondere wenn man Regeln erstellen will, die den
  Lichtsensor abfragen oder den Sonnenstand berücksichtigen

Aus diesem Grund habe ich ein Projekt entwickelt, mit dem eine LUPUS XT2+ mit Hilfe der "Action URL"-Regel Philips Hue (oder kompatible) 
Lichter steuern kann.

Voraussetzungen:
+ LUPUS XT2+
+ Rapsberry Pi 3 (mit Rasbian basierend auf Jessie)
+ Philips Hue Bridge (nur getestet mit v2)
+ Philips Hue oder kompatible Leuchtmittel (z.B. auch Osram Lightify oder innr)

Optional:
+ LUPUS Lichtsensor (für lichtabhängige Steuerung)
+ LUPUS Bewegungsmelder (für bewegungsabhängige Steuerung)
+ OSRAM Lightify Plug (günstige Funksteckdose)
+ Andere Sensoren wie sie in den Home Automation Regeln genutzt werden 

Features:
+ Räume (Groups) oder Lichter ein- und ausschalten
+ Setzen von Helligkeit, Farben oder Lichttemperatur für Räume (Groups) oder einzelne Lichter
+ Aufrufen von Szenen (verschiedene Einstellungen für die Lichter eines Raums)
+ Setzen von Timern für das Ein- und Ausschalten (entspricht der "Einschalten für" von LUPUS aber auch mit "Ausschalten für")
+ Loops für Effekte (z.B. für die Signalisierung eines Zustands)
+ Ausführen von Kommandos abhängig vom Lux-Wert des Lichtsensors
+ Zeitverzögertes Ausführen von Kommandos bis ein Lux-Wert erreicht ist
