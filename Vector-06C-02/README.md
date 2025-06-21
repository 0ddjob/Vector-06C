# Вектор 06Ц.02/Vector 06C.02
## Connector Pinouts

### XS3 "J1" & XS4 "J2"
Joystick 1 & 2 connections.<br>
|Цель|-<|
|---|---|
|1|Верх/Up|
|2|0V/Ground|
|3|Право/Right|
|4|Наз(?)/Down|
|5|Кн.2/Button 2|
|6|Лево/Left|
|7|Кн.1/Button 1|

### XS5 "RGB"
|Цель|-<|
|---|---|
|1|Збук/Sound|
|2|Видео/Video|
|3|Blue|
|4|Green|
|5|Red|
|6|0V/Ground|
|7|Упров/Control|

Pin 2 appears to be composite video and thus can be used for C.SYNC.<br>
Pin 7 is connected to +12V so likely used for SCART control.<br>

### XS7 "CTV"
This three pin connector appears to control whether the RGB signal is inverted or not.  The "target" (Цель) could be the type of RGB decoder (?): MC-3 or MC-31.<br>

From the schematic:
|Цель|-<|
|---|---|
|МЦ-3|1|
|П/?|2|
|МЦ-31|3|

Pin 1 = ground<br>
Pin 2 = XOR input on D61 & D67<br>
Pin 3 = no connection (pin 2 is pulled up to +5V)<br>

D61 & D67 are КР1533ЛП5 (74ALS86) which are quad two-input XOR gates.<br>

The functionality is that when 1-2 are bridged then one input to the XOR gates is low, meaning the RGB signal is not affected: RGB low remains low, RGB high remains high.<br>
If 2-3 are bridged then one input is high which inverts the RGB signal: if RGB is low then it becomes high, and high becomes low.<br>

### XS8 "Power"
|Цель|-<|
|---|---|
|1|0V/Ground|
|2|-5V|
|3|+5V|
|4|-5V|
|5|+12V|
|6|0V/Ground|
|7|+5V|


