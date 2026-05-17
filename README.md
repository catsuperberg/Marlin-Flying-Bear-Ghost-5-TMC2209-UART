# Base Ghost 5 Configuration
This configuration is based on [Sergey1560/Marlin_FB4S](https://github.com/Sergey1560/Marlin_FB4S).

## UART Rewiring for All Four Drivers
To get all four drivers working over UART, some rewiring was necessary.
- For connection details, check the pin definitions in:  
  `Marlin\src\pins\stm32f1\pins_MKS_ROBIN_NANO.h`

- To connect UART pins to the board, wires with resistors are required, as described in:  
  `Marlin\Configuration_adv.h` (line 2710, *Trinamic Smart Drivers* section)

- A wire with a single Dupont connector on both ends is ideal for splicing and adding a resistor in the middle.  
  All used pins on the board have connectors for this.

- For this board, some driver pins should be moved to the top side (as shown in the photo) to avoid making connections through the socket and to connect wires going to connectors on the motherboard.

![prepared drivers](<pictures/drivers prepared for uart.jpg>)
