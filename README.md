# CS140M--Lab4

Part 2:

i)  The bit resolutions for the fast channels are: 12 (5.33 rate), 10 (6.15 rate), 8 (7.27 rate), 6 (8.88 rate). The bit resolutions for the slow channels are: 12 (4.21 rate), 10 (4.71 rate), 8 (5.33 rate), 6 (6.15 rate). I found this under table 81 in the STM32L4S5xx data sheet.

ii) While the ADC measures voltage, the photoresistor only changes in its resistance. When its darker, the photoresistor's resistance goes up, and when its brighter the photoresistor's resistance goes down. Without the resistor, the ADC value printed to terminal is around 4095, which shows that there's no change in voltage to be read. With the photoresistor there is a connection to the ground, and so the LDR and resistor can share the voltage, so the resistance  increasing or decreasing from the photoresistor can actually be shown in the readings.


Part 3:

i) The highest resolution in the datasheet is 12-bits, thus the formula is (9/4096)*Vref

ii) With a smaller sampling rate, the audio becomes less smooth, and more harsh. This happens because the sampling rate is what determines how well the audio is reproduced, and a smaller sampling rate means larger steps in between samples, so the sound will be harsher and louder. The sin waves sound smooth and consistent, while the square waves sound like a buzz. The sawtooth waves sound like a mix of both. This is explained by it reproducing both of the harmonics produced by the sin and square wave. The capacitor blocks DC and passes only AC. Without the capacitor in the signal path, the DC will also be sent to the headphones, potentially damaging them. 
