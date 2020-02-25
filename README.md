# Tetris on flip-dot display

The aim of this project was to interface a flip-dot display with ARM microcontroller (STM32) and use it to run a game "Tetris" written in C++.

Parts used:
*  stm32f103c8t6 microcontroller
*  flip-dot display
*  breadboard
*  buttons, resistors and wires
*  AC/DC adapter 24V

# Budowa i połączenia wyświetlacza.

Wykorzystany wyświetlacz składa się z 9 rzędów i 28 kolumn dysków magnetycznych ("pikseli"), które z jednej strony są czarne, a z drugiej żółte. Sterowanie nimi wspomagane jest przez rejestry przesuwne MC74HC595AN. Zdjęcia przedstawiające wspomniany wyświetlacz:

"Zgaszony" wyświetlacz.

"Zapalony" wyświetlacz.

Schemat połączeń przedstawiony jest na rysunku poniżej:

Przy podłączaniu wyświetlacza do płytki należy pamiętać, że masa znajduje się po innej stronie niż reszta pinów:
