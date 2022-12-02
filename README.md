# RegulatedPowerSupply
In this repository i share the schematic, measurements and prototype board photos of the simple regulated/unregulated output power supply i designed using Altium Designer. 
The board uses two diode voltage doubler circuit to rectify the ac sinewave coming from a 20Vpk-pk transformer i salvaged from an old ups, in order to take advantage of the two ac peaks to create two indepentant full peak voltage rails. The two voltage rails get filtered from 2 power 10000UF 35V Capacitors which i opted in case i wanted to supply a high power circuit directly with unregulated voltage with the disadvantage of voltage flactuations caused by loading the circuit.

Voltage flactuations can be eliminated by regulating the Voltage of the power rails. In this way, you give headroom to the unregulated rail to flactuate in loading instances while regulators sense the voltage change in the output and tweak their internal transistors to increase or decrease the current in order to keep the supply regulated supply voltage stable no matter what until of course you run out of headroom.

The outputs of the positive and negative regulators get Decoupled from HF noise by a pair of 10UF 25V electrolytic caps and 0.1UF ceramic caps while a pair of 470UF 25V electrolytic caps provide some more current storage. 

Regulated supplies are typical to voltage sensetive circuits like voltage gain stages in audio amps in which voltage instabilities create distortion and change the characteristics of them while still using the unregulated voltage to power current gain stages which are not so sensetive to voltage.

This project was really fun also because of the prototype board which will become handy for future mainly audio projects that require dual voltage rails.
If you have any questions or you would like to recommend any changes to the design feel free to contact me. I would highly appreciate it!

Video comming soon in my YT channel and maybe a pcb layout live in altium so stay tuned in:
https://www.youtube.com/@pantelisEVs
Voltage Doubler video: https://www.youtube.com/watch?v=xjfeVQ6uwTY&t=234s

# Prototype Board
![Prototype Front](https://user-images.githubusercontent.com/93339707/205380614-cfa87be2-d736-42ff-bf09-846073a82f6c.jpg)
![Prototype Back](https://user-images.githubusercontent.com/93339707/205380618-36da5fdb-f112-412a-9f1c-47b36f82a095.jpg)
![Angled](https://user-images.githubusercontent.com/93339707/205380627-ada68a13-40e7-4769-9c57-3eb6e3ad0a54.jpg)
# Measurements
Noise in the Regulated-Filtered rail - Unloaded:
Less than 10mVpk-pk noise at 20us time Division(20 MHZ Analog Osciloscope)
![Regulated Unloaded-Filtered Noise](https://user-images.githubusercontent.com/93339707/205380697-64e5b459-90c5-4f99-88ad-d5b11598d511.jpg)
Noise in the Unregulated-Unfiltered rail - Unloaded:
Bigger than previous measurements with same osciloscope settings
![Unregulated-No HF Output Decoupling Noise](https://user-images.githubusercontent.com/93339707/205381326-b04e22c4-0c26-4b9f-bc8c-8b3832f5821c.jpg)
2W Load Noise and Regulated Voltage stable:
![2W Loaded Noise Stable Regulated Voltage](https://user-images.githubusercontent.com/93339707/205381458-67b8481f-7a17-4c6d-8eb0-d87a37ccd6ea.jpg)

