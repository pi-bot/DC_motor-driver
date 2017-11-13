# Arduino library for the PiBots dual motor driver

Version: 2.0.0 <br>
Release date: 2016-08-18 <br>

## Summary
This is a library for the DC PiBot motors.
It makes it simple to drive two brushed, DC motors.

## Getting started
There is a script that automatically loads this library into the PiBots Arduino IDE. (See the config directory of the Pioneers repo for more details. 


### Manual Install

If this does not work, you can manually install the library:

1. Download the
   [latest release archive from GitHub](https://github.com/pi-bot/DC_motor-driver/releases)
   and decompress it.
2. Rename the folder "lps-arduino-xxxx" to "DRV8835MotorShield".
3. Drag the "DRV8835MotorShield" folder into the "libraries" directory inside your
   Arduino sketchbook directory. You can view your sketchbook location by
   opening the "File" menu and selecting "Preferences" in the Arduino IDE. If
   there is not already a "libraries" folder in that location, you should make
   the folder yourself.
4. After installing the library, restart the Arduino IDE.

## Example program

An example sketch is available that shows how to use the library.  You
can access it from the Arduino IDE by opening the "File" menu,
selecting "Examples", and then selecting "DRV8835MotorShield".  If
you cannot find these examples, the library was probably installed
incorrectly and you should retry the installation instructions above.

### Demo

The demo ramps motor 1 from stopped to full speed forward, ramps down
to full speed reverse, and back to stopped. Then, it does the same
with the other motor.

## Documentation
- `void setM1Speed(int speed)` <br> Set speed and direction for
  motor 1. Speed should be between -400 and 400. The motors brake at 0
  speed. Positive speeds correspond to motor current flowing from M1A
  to M1B. Negative speeds correspond to motor current flowing from M1B
  to M1A.
- `void setM2Speed(int speed)` <br> Set speed and direction for
  motor 2. Speed should be between -400 and 400. The motors brake at 0
  speed. Positive speeds correspond to motor current flowing from M2A
  to M2B. Negative speeds correspond to motor current flowing from M2B
  to M2A.
- `void setSpeeds(int m1Speed, int m2Speed)` <br> Set speed and
  direction for motor 1 and 2.
- `void flipM1(bool flip)` <br> Flip the direction meaning of the
  speed passed to the setSpeeds function for motor 1.  The default
  direction corresponds to flipM1(false) having been called.
- `void flipM2(bool flip)` <br> Flip the direction meaning of the
  speed passed to the setSpeeds function for motor 2.  The default
  direction corresponds to flipM2(false) having been called.

## Version history

* 2.0.0 (2016-08-18): Updated library to work with the Arduino Library Manager.
* 1.0.1 (2014-08-15): Fix pin initializations so the Arduino Due doesn't drive the motors when the sketch starts.
* 1.0.0 (2014-08-15): Original release.
