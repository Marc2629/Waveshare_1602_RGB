# Waveshare 1602 RGB LCD

This repository provides a new module file for the Waveshare 1602 RGB LCD screen. The example provided by Waveshare wasn't working for me, so I created this module.

## Getting Started

### Prerequisites

Ensure you have the `smbus` library installed. If not, you can install it using:
`pip install smbus`

# Installation
1. Clone this repository to your local machine or download the LCD1602.py file.
2. Place the LCD1602.py file in the directory where your main code resides.

# Usage
To use the module in your project, follow these steps:

1. Import the `RGB1602` class from the `LCD1602` module:

`from LCD1602 import RGB1602`

2. Create an instance of the RGB1602 class:

`lcd = RGB1602(16, 2)  # Initialize a 16x2 LCD`

3. Use the instance methods to control the LCD. For example:

```lcd.clear()
lcd.setColorWhite()
lcd.setCursor(0, 0)
lcd.printout("Hello, World!")```
  
# Example
Here is a simple example demonstrating how to use the RGB1602 class:

```import time
from LCD1602 import RGB1602
  
# Initialize the LCD
lcd = RGB1602(16, 2)  # 16 columns and 2 rows
lcd.clear()
lcd.setColorWhite()
  
# Display a message
lcd.setCursor(0, 0)
lcd.printout("Hello, World!")
  
# Flash the message
for _ in range(5):
    lcd.clear()
    time.sleep(0.5)
    lcd.setCursor(0, 0)
    lcd.printout("Hello, World!")
    time.sleep(0.5)```
      
# Additional Information
Ensure your I2C bus is correctly configured on your Raspberry Pi.
Refer to the class methods in LCD1602.py to explore more functionalities.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

# Acknowledgments
Thanks to Waveshare for the original example, which inspired this module.
