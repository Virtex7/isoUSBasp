isoUSBasp
=========

3kV isolated USBasp-compatible Atmel AVR8 USB programmer

description in German Language:

3kV Dauerlast-isolierter USBasp mit Leistungstreibern am Ausgang

diese Version des bekannten Atmel-Programmiergeräts USBasp von Thomas Fischl
enthält ein paar zusätzliche Fähigkeiten:

- überall LEDs
- LEDs statt Zenerdioden am USB-Port (schöner!)
- galvanisch isolierter ISP-Port
- galvanisch getrennte Target-Supplyfunktion bis 200mA in 3,3 und 5V
- automatische Einstellung der Programmierspannung
- Leistungstreiber an den Programmierpins mit je +-70mA dauerkurzschlussfest
- Schmitt-Trigger-Eingänge mit Signalrückgewinnung
- per Schalter einstellbare slowSCK-Funktionalität für 128kHz-Targets


effektiv soll dieser Programmieradapter überall eingesetzt werden, auch wenn das Target
auf einer viel höheren Spannungsebene liegt, als der zur Programmierung eingesetzte PC.
Auch werden durch eine Massetrennung Masseschleifen und damit bedingte Fehlerströme
vermieden, die zur Beschädigung des PCs und des Programmiergeräts führen können.

Desweiteren ist jeder Programmierpin mit Schutzbeschaltung gegen Überspannung,
Dauerkurzschluss und in Grenzen gegen Rückspeisung geschützt.

Die Programmierspannung stellt sich automatisch ein, wenn am Vref-Pin des ISP-Anschlusses
eine Spannung anliegt. Default ist 3,3V, auch wenn keine Spannung am Vref-Pin liegt.
Umschaltgrenze ist 3,6V, dabei wird dann auf 5V ISP-Spannung umgeschaltet.

Es ist auch möglich den Vref-Anschluss zu bestromen, also das Target mit Strom zu
versorgen. Maximalstrom ist dabei 200mA bei 5V und ca 300mA bei 3,3V, durch einen
Widerstand dauerhaft kurzschlussfest. (dabei bricht die Spannung zusammen)



Hardware:

Schaltplan und Layout und alle nötigen Libs wurden entweder von mir erstellt oder sind
Teil des OpenSource-Projekts KiCad (EDA)
Ich empfehle die Verwendung einer selbst kompilierten Version von KiCad, da diese die
aktuellste Version ist und KiCad momentan recht schnell entwickelt wird.


Software:

Das Produkt ist zu fast 100% kompatibel zur FISCHL-USBasp-Software, dafür wurden ein paar
Inverter extra verbaut, das hätte man auch in Software machen können.
Allerdings muss das Relais an PC3 nach erfolgter Anmeldung am USB angeschaltet werden,
das ist und wird die einzige Modifikation an der Software.


Daher verweise ich auch auf die Homepage von Thomas Fischl:
http://www.fischl.de/usbasp/
