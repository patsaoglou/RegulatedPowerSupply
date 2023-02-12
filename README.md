# +/-15V Regulated Power Supply
In this repository i share the schematic, measurements and prototype board photos of the simple dual rail regulated/unregulated output power supply i designed using Altium Designer. 
The board uses two diode voltage doubler circuit to rectify the ac sinewave coming from a 40Vpk-pk transformer i salvaged from an old ups, in order to take advantage of the two ac peaks to create two indepentant full peak voltage rails. The two voltage rails get filtered from 2 power 10000UF 35V Capacitors which i opted in case i wanted to supply a high power circuit directly with unregulated voltage with the disadvantage of voltage flactuations caused by loading the circuit.

Voltage flactuations can be eliminated by regulating the Voltage of the power rails. In this way, you give headroom to the unregulated rail to flactuate in loading instances while regulators sense the voltage change in the output and tweak their internal transistors to increase or decrease the current in order to keep the regulated supply voltage stable no matter what until of course you run out of headroom.

HF noise of the outputs of the positive and negative regulator gets Decoupled by a pair of 10UF 25V electrolytic caps and 0.1UF ceramic caps while a pair of 470UF 25V electrolytic caps provide some more current storage. 

Regulated supplies are typical to voltage sensetive circuits like voltage gain stages in audio amps in which voltage instabilities create distortion and change the characteristics of the circuit while still using the unregulated voltage to power current gain stages which are not so sensetive to voltage.

This project was really fun also because of the prototype board which will become handy for future,mainly audio projects that require dual voltage rails.
If you have any questions or you would like to recommend any changes to the design feel free to contact me. I would highly appreciate it!

Prototype Build Video:
https://www.youtube.com/watch?v=nPICWO84uSs

PCB layout live:
https://www.youtube.com/watch?v=I7pFWdqES8I

Voltage Doubler video:
https://www.youtube.com/watch?v=xjfeVQ6uwTY

# Schematic
![15V Regulated Power Supply - Schematic](https://user-images.githubusercontent.com/93339707/218340856-096448a3-d286-4cb4-b37c-ab1656805967.PNG)

# Prototype Board
![Prototype Front](https://user-images.githubusercontent.com/93339707/218340942-cceb875e-bad2-4532-9507-f401b9033664.jpg)

# PCB Design
![PCB](https://user-images.githubusercontent.com/93339707/218340864-56c4a273-85a9-41d4-8f99-6fb1d680ae68.PNG)

# PCB Produced by JLCPCB
![20230213_000428](https://user-images.githubusercontent.com/93339707/218340900-825523fe-031f-4001-bcb7-912c3006a957.jpg)

Hand Soldered the components! The final result:
![20230213_000732](https://user-images.githubusercontent.com/93339707/218340907-0a84c59c-813a-45ab-98a0-0d41187fff4f.jpg)

# Measurements
Noise in the Regulated-Filtered rail - Unloaded:
Less than 10mVpk-pk noise at 20us time Division(20 MHZ Analog Oscilloscope)
![2W Loaded Noise Stable Regulated Voltage](https://user-images.githubusercontent.com/93339707/218340971-cebc6170-efdc-43b3-91ce-a919bbf33100.jpg)

Noise in the Unregulated-Unfiltered rail - Unloaded:
Bigger than previous measurements with same osciloscope settings
![Unregulated-No HF Output Decoupling Noise](https://user-images.githubusercontent.com/93339707/218340988-1892ef18-27e7-418b-ac9b-84ca5ea2c5ef.jpg)

2W Load Noise and Regulated Voltage stable:
![Regulated Unloaded-Filtered Noise](https://user-images.githubusercontent.com/93339707/218340995-b2b23ef9-e578-4667-a451-ffc96c3bc786.jpg)
