# HB-ES-PMSwX-Pl_Gosund
Umbau [Gosund SP211 und Baugleiche](https://www.gosund.com/download/smart_plug/128.html) zu HB-ES-PMSwX-Pl_SP1.

Dieses Projekt basiert auf der Arbeit von [pa-pa](https://github.com/pa-pa/AskSinPP) ,[Jérôme](https://github.com/jp112sdl/Beispiel_AskSinPP) und [Asselhead](https://github.com/Asselhead/Arduino-Pro-Mini-RF).

Angelehnt an das Projekt von [stan23](https://github.com/stan23/HM-ES-PMSw1-Pl_GosundSP1).


# Hardware

### Bauteile

Bauteile                   | Bezeichnung          | Anzahl | Kommentar
-------------------------- | -------------------- | ------ | ---------
C1                         | 10uF, +-20%, 6,3V    |   1    | G0402
C23                        | 4.7uF 10V            |   1    | G0402
C2, C3, C4, C5             | 100nF, 10%, 16V      |        | 
C41, C51, C91, C111        | 100nF, 10%, 16V      |        | 
C141, C151, C181           | 100nF, 10%, 16V      |   11   | G0402
C81                        | 12pF, 5%, 50V        |   1    | G0402
C101                       | 15pF, 5%, 50V        |   1    | G0402
C121                       | 1pF, +-0.25pF, 50V   |   1    | G0402
C122, C131                 | 1.5pF, +-0.25pF, 50V |   1    | G0402
C123                       | 3.3pF, +-0.25pF, 50V |   1    | G0402
DR121, DR123, DR124, DR131 | 12nH, 5%             |   4    | G0402
DR122, DR132               | 18nH, 5%             |   2    | G0402
R1                         | 10K                  |   1    | G0402
R171                       | 56K                  |   1    | G0402
U1                         | ATMEGA 644PA-MU      |   1    | QFN-44
U2                         | CC1101               |   1    | QFN-20
Q1                         | RESONATORS 26MHZ     |   1    | SMD-3225_4P



#### Sonstiges

~8,3 cm Draht als Antenne

### Programmieradapter
- 1x ISP (z.B. [diesen hier](https://www.diamex.de/dxshop/USB-ISP-Programmer-fuer-Atmel-AVR-Rev2))


# Software

### Fuses
Ext:  0xFF
High: 0xD2
Low:  0xE2

`C:\Program Files (x86)\Arduino\hardware\tools\avr\bin> .\avrdude -C ..\etc\avrdude.conf -p m644p -P com7 -c stk500 -U lfuse:w:0xE2:m -U hfuse:w:0xD2:m -U efuse:w:0xFF:m`


### Firmware

Projektverzeichnis: [HB-ES-PMSw1-Pl_GosundSP1](TBD)

Benötigt werden die Bibliotheken [AskSinPP](https://github.com/pa-pa/AskSinPP) aus dem master-Branch, sowie die [HLW8012](https://github.com/xoseperez/hlw8012), die [MightyCore](https://github.com/MCUdude/MightyCore), die [EnableInterrupt](https://github.com/GreyGnome/EnableInterrupt) und [Low-Power](https://github.com/rocketscream/Low-Power).


# Bauanleitung

TBD


# Kalibrierung

TBD


# Bilder
![Vorderseite](https://github.com/maxx3105/HB-ES-PMSwX-Pl_Gosund/blob/main/HB-ES-PMSwX-Pl_Gosund_top.png)
![Rückseite](https://github.com/maxx3105/HB-ES-PMSwX-Pl_Gosund/blob/main/HB-ES-PMSwX-Pl_Gosund_bottom.png)
