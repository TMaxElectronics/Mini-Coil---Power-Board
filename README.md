# This file is part of Mini-Coil open source DRSSTC project
If you want to build one have a look at the entire project here: ...link TBD...
Are you building one right now and need info on it? Then keep reading :)

# How to build this part of the coil
This board is the dc-bus capacitance and probably the simplest one in the entire coil. 

Here's what you'll need to build it:
 - Soldering Iron
 - Solder (I suggest leaded solder if you don't have a powerful iron)
 - PCB Components (listed below)
 - at least one Cap Board PCB :)
 
# BOM (bill Of Material)
The BOM can be found in the file "Bill of Materials-Mini-Coil - Power Board.xlsx". It contains part numbers of some of the specialised components for ordering on digikey.
There is a seperate line for items you can get from Wuerth Elektronik directly if you are in contact with them (ask for samples, they will probably give you the parts for free).
If you can't order from wuerth directly you can also order those parts on digikey.

The parts without a specified part number you need to search for yourselves as there are many different alternatives and its likely you already have some laying around anyway ;)

### non-critical components
In general it is almost always possible to substitute parts for other ones if you can't get/don't want to buy the specified ones. Here are some notes however:
 - the foil capacitor can be replaced by any other suitable voltage rated part that fits onto the footprint. There are also holes with a 37.5mm spacing for the cheaper single pin row capacitors. Just make sure you don't get ones with too little capacitance (how little is too little? can't tell you sorry, you'll have to measure that if you want to be sure)
 - the terminal blocks are likely to melt and weld themselves together if you buy cheap ones from ebay. Go spend that little bit of money and buy proper ones ;)
 - probably look for other relays, the ones I have are another ebay score. New they might be ridiculously expensive. Just make sure they come with a 24V coil!
 
### critical components
Unlike most components these cannot really be substituted easily
 - the IGBTs. Although you can use cheaper ones these are the ones that I trust. The cheap ones I've tried all blew up at fairly low currents. (the spec'd ones pull 500A peak I_prim easily)
 - the rectifier has a weird footprint, its unlikely you'll find a nice replacement.
 
# Assembly notes
Start with all of the SMD components (so on the top layer the TVS diodes and on the bottom the flyback diodes on the relays and the bypass cap for the current sensor). These parts will be annoying to solder later.
Then continue with the smaller THT parts, like the 100k voltage sense resistors and the varistors.

Just a top before you start with the large parts: this board has a super high thermal mass (especially noticeable on the pads of the power devices). You can make your life easier by using leaded solder, heating the board with some hot air as you solder (not too hot, you don't want to burn anything) or even better: pre-heat the board to 150°C or so in an oven (but use gloves when placing components of course :P).
Next place the redcube terminals and the current sensor and make doubly sure they are all soldered properly. The solder needs to flow all the way through the hole and up to the actual block or the terminals will break off after a while (trust me, I've tried to be lazy here :P). If you are having trouble you can apply some flux to the top of the hole and use hot air as support. **DO NOT** solder from both sides, that coul easily trap an air pocket in the joint and make it look good without actually being rigid enough!
Also make sure that the redcubes (especially the male ones) are soldered in flat and parallel with the board, otherwise it will be hard to connect the cap-board.

Then continue on with the remaining parts as you see fit, but **don't solder in the IGBTs and the rectifier just yet**, that is done in the bridge assembly step later.

# Testing
There is also nothing you absolutely *should* test here. If you want to you can also test the relays (just make sure to use a current limited supply to not kill the flyback diodes if you reverse the polarity :P).

# Disclaimer
This project utilises dangerous (lethal!) voltages! There is a high likelyhood of fire/personal harm if you don't know what you are doing. Use these files at your own risk. Any damage you do to yourself or other people with this project is not my responsibility.

I also make no promises about the correctness of any of the info given in this project or any of its files. It is also your responsibility to verify all of the data in this when building your own coil. You are thus responsible for any damage caused even by mistakes in these files.

Ensue the standard legal disclaimer text just to be sure... (modified for open hardware)

Permission is hereby granted, free of charge, to any person obtaining a copy of this data and associated documentation files (the “data”), to deal in the data without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the data, and to permit persons to whom the data is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the data.

THE DATA IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE DATA OR THE USE OR OTHER DEALINGS IN THE DATA.
