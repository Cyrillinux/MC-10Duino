# MC-10 Alice Duino 0.0.10

Under GPL license

Add Tandy MC-10 / Matra Alice BASIC board transfer for Arduino IDE

* DISCLAIMER OF ALL WARRANTIES *

Platforms : MACOS and Windows, Linux soon.

This package is new projet, just begening, not official package and patch.

With Arduino UNO board compatible, allows to transfer a MC-10/Alice Text BASIC (.BAS.ino) file directly to Tandy MC-10 / Matra Alice, like cassette.

#Versions
0.0.1 : first MacOS
0.0.2 : MacOS, Windows
0.0.3->6 : Windows bugs fixed
0.0.7 : BASIC RIGHT$ added and Arduino schematic modified
0.0.8 : trs80gp replaces xroar
0.0.9 : bugs DATA fixed
0.0.10 : add last all BASIC functions

#Installation and test

1/ Donwload Arduino >= V1.8.19 

2/ Launch Arduino

3/ In Arduino->Preferences->Additional Board Manager URLS
        add Arduino IDE >= V1.8.19 :
                https://sourceforge.net/projects/mc10duino/files/packages/package_mc-10_index.json
        add Arduino IDE >= V2 : 
                https://github.com/Cyrillinux/MC-10Duino/releases/download/packages/package_mc-10_index.json
        
    (NOT https://bacciel.com/tools/package_mc-10_index.json is OLD version)
    
4/ In Tools->Boards:...->Board Manager
    search "MC-10" or "Alice"
    select and install "MC-10/Alice Devices"
    
5/ In Tools->Board:...
    select "Board : "MC-10/Alice Transfer Board BASIC" or "MC-10/Alice Simulating Local BASIC"
    
6/ Demos :
    HELLO.ino BASIC
    INVADERS.ino BASIC
    BREAKOUT.ino BASIC
    
    and build and upload !
    
    On MC-10 / Alice : CLOAD -> RUN
    
7/ Arduino UNO Pinout

D3 is output signal to MC-10/Alice cassette port.

                                                  560 Ohms
 to Positive REC+ on MC-10/Alice cassette port <----/\/\/\----+ (signal output)
                                                              |
                                                              |
      +--------------------------------------------------------------------
      | (RST) ( )[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [*] [ ] [ ] [ ]\
      |          GND D13 D12 D11 D10 D9  D8  D7  D6  D5  D4  D3  D2  D1  D0 |
      |                                                                     |
      [ USB ]                                                               |
      |                                             UNO R3                  |
      |                                                                     |
      |                                                                      \
      |                                                                   ( ) |
      |                                                                       |
      |                                                                       |
      |                                       [ ATMEGA328P ]                  |
      |                                                                       |
      |                                                                   ( ) |
      [ Power ]                  5V  3V3 VIN GND GND A0  A1  A2  A3  A4  A5   |
      |                   ( )    [ ] [*] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] /
      +---------------------------------------------------------------------+
                                      | 
                                      | 
           to GND MC-10/Alice REC- ---+

see complete manual MANUAL_MC-10_ALICE_DUINO in Doc.

Have Fun
Cyril
