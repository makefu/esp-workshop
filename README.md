# Löten
##ESP
- Auslöten des 0Ohm Widerstands (der Mittlere)
- Spannungswandler 5V -> 3V
- Pin Header
- Stecker für ws2812b Led

##USB Serial
###notwendig:

- "circuit bending" ... nur Spass ... das ist nur ein Beispielbild

![](http://bitcrusher.free.fr/images/tutones/audiones_PCB_04_Step_04.JPG)

- wir benötigen lediglich eine Brücke für +5V vom USB Stecker zum roten Kabel (diagonal über die Platine)


###damit ich ruhig schlafen kann:
- alle überstehenden Litzen, Drähte abzwicken
- USB Gehäuse/Zugentlastung anlöten



## Erste Schritte mit dem Breadboard (Microcontroller Prototyping)
- grün -> Rx des ESP
- weiss -> Tx des ESP
- schwarz -> GND
- rot -> ist der Widerstand ausgelötet? wichtig! -> VCC
^^ beim Einstecken blinkt die blaue Led? Yeah - so weit alles richtig gemacht: Erfolgserlebnis




# nodemcu
## esptool installieren (optional)
- linux: [esptool](https://github.com/espressif/esptool)`pip install esptool`
- windows: [esp8266 flasher]( https://github.com/nodemcu/nodemcu-flasher/raw/master/Win64/Release/ESP8266Flasher.exe  )
## firmware flashen
- GPIO0 -> GND
- resetten
- esptool.py chip_id -> funktioniert
- cd firmware
## esplorer
- öffnen
- BAUD 115200
- Verbinden
- datei -> öffnen -> blink.lua


#IOT für Einsteiger: SMD löten + ESP8266 prototyping hands-on workshop


**Datum**: Samstag 20.Mai 15-18 Uhr

##Hast du zu Hause vorbereitet:
* Download + install [Arduino IDE ]( https://www.arduino.cc/en/main/software )
  * Start Arduino IDE and open Preferences window. (Datei -> Voreinstellungen)
  Enter **http://arduino.esp8266.com/stable/package_esp8266com_index.json** into Additional Board Manager URLs field. You can add multiple URLs, separating them with commas.
Open Boards Manager from Tools > Board menu and install esp8266 platform (and don't forget to select your ESP8266 board from Tools > Board menu after installation).
* [Esplorer installieren]( https://esp8266.ru/esplorer/ )


##Agenda

* Vorstellungsrunde: Wer bist du? Warum elektro-Internet-Kleingeräte? (aka IOT)
* Schnelle Einführung in Elektronik Prototyping
    * Spannung, Widerstand und Ampere?!
    ![](http://www.sengpielaudio.com/ohms-law-illustrated.gif)
     [du willst tatsächlich mehr wissen?](http://www.brucewilles.de/grundlagen.html)
    * IO pins, Wo muss man aufpassen, lessons learned
      * + und - nicht vertauschen!
      * - und + nicht vertauschen!
      * der magische Rauch ist essentiell für die Funktion der elktrischen Bauteile. Er muss in den Bauteilen verbleiben.
      * Wenn ein Mikrocontroller Pin nur 3V tolerant ist geht er bei 5V kaputt (manchmal nicht sofort)
    * USB-Serial
      * rx <-> tx, hyperterminal -> funktioniert?

* 30 min SMD löten: Hands-on Workshop (Einsteiger-level)
    * a USB-Serial Kabel “hacken” damit es richtige 5V liefert
    * Löte den ESP8266 an das PCB Adapter-Board
    * Spannungsregler, ws2812b (RGB led mit Microcontroller), Stecker, Gewürze
* Einführung Arduino IDE + hands-on
    * “blinke-led” für IOT (Web-Server im WLAN)
* Schnelle Einführung: NodeMCU (LUA) + hands -on
    * wlan setup
    * find your box (e.g. mybox.connector.one)
    * control rgb led from your smartphone
* happy hacking, social, Pizza?


Die Agenda wird ggfs. kurzfristig angepasst.

**Unkostenbeitrag** 10€ p.P. für das super Esp8266-Dev-Set, das Ihr zum weiter hacken mit nach Hause nehmen müsst.






