# 3_Led_patterns
A sequence of LED Pattern whenever a key from keypad is pressed

# LED Pattern Controller

## Overview

This project controls a series of LEDs connected to an Arduino board, allowing users to select different lighting patterns via serial input. The code demonstrates the use of digital I/O pins to create various LED patterns, enhancing understanding of basic Arduino operations.

## Components

- Arduino board (e.g., Uno, Mega)
- 4 LEDs
- 4 current-limiting resistors (220Ω recommended)
- Breadboard and jumper wires

## Circuit Diagram

1. Connect the cathode (short leg) of each LED to the ground (GND) on the Arduino.
2. Connect the anode (long leg) of each LED to a current-limiting resistor.
3. Connect the other end of each resistor to digital pins 2, 3, 4, and 5 on the Arduino.

## Code Explanation

### Variables and Function Declarations

- `int ledPin;`: Variable to store the current LED pin being manipulated.
- `int reqdPattern;`: Variable to store the pattern number input by the user.

### Functions

- `ledPattern1()`: Turns all LEDs on sequentially, then turns them off sequentially with a 1-second delay.
- `ledPattern2()`: Turns each LED on and off one by one with a 1-second delay.
- `ledPattern3()`: Turns all LEDs on in reverse order, then turns them off in reverse order with a 1-second delay.
- `ledPattern4()`: Turns on odd-numbered LEDs, then even-numbered LEDs, and then turns them off in the same sequence with a 1-second delay.

### Setup

In the `setup()` function:
- Serial communication is initialized at 9600 baud.
- Pins 2 through 5 are set as OUTPUT.
- The user is prompted to enter a pattern number.

### Loop

In the `loop()` function:
- The code checks for available serial input.
- The pattern number entered by the user is read and stored in `reqdPattern`.
- Depending on the input, the corresponding pattern function (`ledPattern1()`, `ledPattern2()`, `ledPattern3()`, `ledPattern4()`) is called.
- If an invalid pattern number is entered, an error message is displayed.

## Usage Instructions

1. Assemble the circuit as per the circuit diagram.
2. Upload the provided code to the Arduino board.
3. Open the Serial Monitor from the Arduino IDE (Tools -> Serial Monitor).
4. Set the baud rate to 9600 in the Serial Monitor.
5. Enter a pattern number (1, 2, 3, or 4) to see the corresponding LED pattern.
6. If an invalid pattern number is entered, the Serial Monitor will display "Invalid Pattern".

## Example Output

- Entering `1` will sequentially turn all LEDs on and off.
- Entering `2` will turn each LED on and off one by one.
- Entering `3` will sequentially turn all LEDs on and off in reverse order.
- Entering `4` will turn on and off odd-numbered and then even-numbered LEDs.

Enjoy experimenting with different LED patterns and enhance your understanding of Arduino programming!
