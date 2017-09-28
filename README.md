# AVR Studio 7 x Arduino sketch imports

Arduino sketches imported into AVR Studio 7 to make use of on-chip debugger

## Importing

1. From File>New>Project double-click "Create project from Arduino sketch"
2. Select Sketch File, Arduino IDE Path, Board and Device.

NB If board is changed, project probably will need to be re-imported (TBA).

## Caveats

Importing simple sketches such as Blink.ino is not a problem. Importing more complex sketches such as StardardFirmata.ino throws errors. To get around this, leave only the library imports i.e.
```
#include <Servo.h>
#include <Wire.h>
#include <Firmata.h>
```
plus bare minimum i.e.
```
void setup()
{
}

void loop()
{
}

```
Once imported, paste the code back into Sketch.cpp in AVR Studio 7, making sure includes are left and setup() and loop() functions are overwritten.

