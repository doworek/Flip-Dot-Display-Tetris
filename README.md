# Tetris on flip-dot display

The aim of this project was to interface a flip-dot display with ARM microcontroller (STM32) and use it to run a game "Tetris" written in C++. It can be controlled via serial monitor or external buttons.
It required hours of reverse engineering and programming but definitely was worth it.

Parts used:
*  stm32f103c8t6 microcontroller
*  flip-dot display
*  breadboard
*  buttons, resistors and wires
*  AC/DC adapter 24V

## Display and schematics

Display used in this project has 9 rows i 28 columns of magnetic discs ("pixels") which are controlled by shift registers MC74HC595AN. Here is the programmed "welcome screen":

![20200121_155842](https://user-images.githubusercontent.com/61286976/75385206-9c36a680-58df-11ea-837d-6cedc7ac73a4.jpg)


Wiring diagram:

![schemat połączeń flip dot display](https://user-images.githubusercontent.com/61286976/75385240-ace71c80-58df-11ea-987b-3c2fed787ddf.png)

Buttons diagram (if used):

![buttons](https://user-images.githubusercontent.com/61286976/75386619-4a435000-58e2-11ea-8d47-4c8d4f9a039e.png)

When interfacing this display with a microcontroller I had to remember that ground isn't where it should be:

![20200106_132619](https://user-images.githubusercontent.com/61286976/75385218-a2c51e00-58df-11ea-84db-7868cafefb62.jpg)

## Tetris

Game in action:

![VideoCapture_20200121-160331](https://user-images.githubusercontent.com/61286976/75386540-2849cd80-58e2-11ea-8d10-0c1b0ed22c8f.jpg)

Game can be controlled via serial monitor. I used Putty, settings: "connection type" = "serial", change the port name and speed. Next "category": connection -> SSH -> serial -> "flow control" = "None". With these settings you can use keyboard keys "w", "s", "a", "d" to control the game.
