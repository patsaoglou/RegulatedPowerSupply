# +/-15V Regulated Power Supply
In this repository i share the schematic, measurements and prototype board photos of the simple dual rail regulated/unregulated output power supply i designed using Altium Designer. 
The board uses two diode voltage doubler circuit to rectify the ac sinewave coming from a 40Vpk-pk transformer i salvaged from an old ups, in order to take advantage of the two ac peaks to create two indepentant full peak voltage rails. The two voltage rails get filtered from 2 power 10000UF 35V Capacitors which i opted in case i wanted to supply a high power circuit directly with unregulated voltage with the disadvantage of voltage flactuations caused by loading the circuit.

Voltage flactuations can be eliminated by regulating the Voltage of the power rails. In this way, you give headroom to the unregulated rail to flactuate in loading instances while regulators sense the voltage change in the output and tweak their internal transistors to increase or decrease the current in order to keep the regulated supply voltage stable no matter what until of course you run out of headroom.

HF noise of the outputs of the positive and negative regulator gets Decoupled by a pair of 10UF 25V electrolytic caps and 0.1UF ceramic caps while a pair of 470UF 25V electrolytic caps provide some more current storage. 

Regulated supplies are typical to voltage sensetive circuits like voltage gain stages in audio amps in which voltage instabilities create distortion and change the characteristics of the circuit while still using the unregulated voltage to power current gain stages which are not so sensetive to voltage.

This project was really fun also because of the prototype board which will become handy for future,mainly audio projects that require dual voltage rails.
If you have any questions or you would like to recommend any changes to the design feel free to contact me. I would highly appreciate it!

Prototype Build Video:
https://www.youtube.com/watch?v=nPICWO84uSs&t=528s

PCB layout live:
https://www.youtube.com/watch?v=I7pFWdqES8I&t

Voltage Doubler video:
https://www.youtube.com/watch?v=xjfeVQ6uwTY&t=234s

# Schematic
![Schematic Img](https://user-images.githubusercontent.com/93339707/210030845-90ff6a7a-e69c-4319-8153-c5faffaedb36.PNG)

# PCB
![PCB](https://user-images.githubusercontent.com/93339707/206906663-fa0a0da7-1aa8-4e94-b23c-c645e5d6191a.PNG)

# Prototype Board
![Angled](https://user-images.githubusercontent.com/93339707/205380627-ada68a13-40e7-4769-9c57-3eb6e3ad0a54.jpg)

# Measurements
Noise in the Regulated-Filtered rail - Unloaded:
Less than 10mVpk-pk noise at 20us time Division(20 MHZ Analog Oscilloscope)
![Regulated Unloaded-Filtered Noise](https://user-images.githubusercontent.com/93339707/205380697-64e5b459-90c5-4f99-88ad-d5b11598d511.jpg)

Noise in the Unregulated-Unfiltered rail - Unloaded:
Bigger than previous measurements with same osciloscope settings
![Unregulated-No HF Output Decoupling Noise](https://user-images.githubusercontent.com/93339707/205381326-b04e22c4-0c26-4b9f-bc8c-8b3832f5821c.jpg)

2W Load Noise and Regulated Voltage stable:
![2W Loaded Noise Stable Regulated Voltage](https://user-images.githubusercontent.com/93339707/205381458-67b8481f-7a17-4c6d-8eb0-d87a37ccd6ea.jpg)

