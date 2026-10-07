# 775-RC-BTS7960-and-Arduino-Uno-

/* 
FL --- FR
|      |
|      |
BL --- BR

Parts List:
- Lipo 12V Battery
- Double BTS7960 Driver Module x 2
- Arduino Uno
- 775 12V Motors x 4
- HM-10 BLE Module
- Buck Converter (PSU)

Motor Wiring (Parallel):

Module 1 (LEFT SIDE):
- frontLeft and backLeft motors in parallel
- These motors are on the same vertical line (left side)

Module 2 (RIGHT SIDE):
- frontRight and backRight motors in parallel
- These motors are on the same vertical line (right side)

Pin Connections:

BTS7960 Module 1 (LEFT SIDE):
- VCC -> Arduino 3.3V
- L_EN, R_EN -> Arduino 3.3V 
- GND -> Arduino GND
- RPWM -> Arduino Digital Pin 6 (R1PWM)
- LPWM -> Arduino Digital Pin 5 (L1PWM)

BTS7960 Module 2 (RIGHT SIDE):
- VCC -> Arduino 3.3V
- L_EN, R_EN -> Arduino 3.3V
- GND -> Arduino GND
- RPWM -> Arduino Digital Pin 11 (R2PWM)
- LPWM -> Arduino Digital Pin 10 (L2PWM)

Motor Power:
- Both modules M+ and M- terminals connect to respective motors in parallel
- Both modules power terminals (B+, B-) connect to battery (11.1V - 30V)

Bluetooth Module HM-10:
- VCC -> Arduino 5V
- GND -> Arduino GN
- TX -> Arduino Pin 2
- RX -> Arduino Pin 3

Notes:
- R1PWM/R2PWM control forward motion
- L1PWM/L2PWM control backward motion
- When one side moves forward and other backward = turning
- Both modules share the same power source (battery)
- Enable pins are tied to 3.3V for constant enable
*/
