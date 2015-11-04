# Raspberry FM Station with Flask Frontend


Nachgebaut von [instructables.com](http://www.instructables.com/id/Use-Si4703-FM-Breakout-Board-on-Arduino-Uno/step2/Step-2-Wiring-Diagram/)

### Raspberry Pi GPIO Belegung

![Raspberry Pi GPIO Belegung][gpio]

[gpio]: http://raspberry.tips/wp-content/uploads/2014/12/Serial-Interfaces1.png

[Vergleichsbelegung RPI2](http://raspberrypiguide.de/howtos/raspberry-pi-gpio-how-to/)


[Anleitung zum Aktivieren von i2c im Raspberry PI](https://learn.adafruit.com/adafruits-raspberry-pi-lesson-4-gpio-setup/configuring-i2c)

### Mapping

3V auf 3,3V
GND auf GND
A5 auf 14
A4 auf 15
D2 auf 18

|  Arduino | Si4704  | Raspberry   |
|---|---|---|
|3V|VCC|3,3V|
|GND|GND|GND|
|A5| SCLK|GPIO 1|
|A4|SDIO/SDA|GPIO 0|
|D2|RST|GPIO18|




### Installation

	sudo apt-get install build-essential libi2c-dev i2c-tools python-dev libffi6 libffi-dev
    virtualenv si4703
    source si4703/bin/activate
    pip install -r requirements
    python server.py
