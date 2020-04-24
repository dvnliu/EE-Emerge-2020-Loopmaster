# Drumpad/Keypad Code
The code for the drumpad/keypad was developed in the energia IDE and is fairly straightforward: It polls the GPIO pins for a change of state, either being pressed or released. The code reads the status of each pin and compares it to a flag that describes the state it was previously in. When pressed a PRESS flag is set, and is not removed until the digital value of the pin falls below the boolean value of the flag. Then the process is repeated. Each pin sends a unique 8 bit char to through UART to the bela telling it which key was pressed/released.