# This project is WIP

# Overview
Device to detect Beta particles. Since only easy-to-come-by Beta emmiter I can get is a banana, let's call it a Banana detector.
The detector is based on many circuits available on the Internet with few tweaks.

# Function principle
Device utilizes set of PIN photo-diodes to detect passing Beta particles. 
Following analog circuit is only an I-V converter and amplifier with large amplification.
To reduce resistor noise I use T network inverting amplifier.

To detect voltage impulses caused by particle collisions STM32G031 is planned to be used.
Device might count caught particles over time and show such number on OLED I2C display as well as beeping with each collision.
Since I2C communication will add certain noise and since used MCU does not allow to split GND an GNDA, refresh rate of the display is planned low and measurement is conducted only in steady states.

![image](./figs/pcb.jpg)
