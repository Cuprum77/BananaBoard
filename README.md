# BananaBoard
## Project description
The BananaBoard is a solution to a problem of hooking up power supplies with standard 4mm Banana Plugs to Breadboards.
It was based on the idea of not having to own multiple cables and being easier to use, rather than relying on 4mm Banana Plug to Alligator clips or the 4mm Banana Plug to 2.54mm Pin header cables.

![alt text][trio]

## Design 
The PCB itself is designed around the [Keystone Electronics 575-4](https://www.keyelco.com/product.cfm/product_id/2379) Banana Plug sockets.

The design itself had to follow these requirements:
* Fit into the [BB830] breadboard popularized by [Ben Eater](https://eater.net/)
* Have footprints for at least 2 bypass capacitors per rail
* Onboard PTC fuse to avoid damage to the breadboard
* Bypass for PTC fuse if fuse is not desired
* Adjustable pin header slots so you can adjust it to your breadboard

So far all those requirements have been implemented on the first prototype.

## Breadboard Requirements
It *should* fit any board that fits within this dimension: 

  If the positive and negative rail are not mirrored on either side:
  * Positive rail to positive rail: 1.65" ± 0.025".

  If the positive rail and negative rail are mirrored on either side:
  * Positive rail to positive rail: 1.75" ± 0.025".

However, this has not been tested on any other breadboard than the [BB830]

![alt text][breadboard]

## Difficulties
Originally the project had no thermal relief under the idea that we should be limiting the current as little as possible, however that turned out to be a huge mistake as it made soldering almost impossible with a lower wattage iron due to the amount of copper. 
The uploaded version should be fixed and that should not be an issue with future orders.

## Art
To make the circuit board a bit more interesting, the users of the [Styropyro](https://styropyro.com/) Discord server was petitioned to come up with ideas on what to populate it with,
and does therefor contain artwork based off inside jokes and meme culture.

![alt text][singular]

## Connection
The design itself has connection indicators on the bottom side if one does not care for the artwork.
Example on suggested polarity
![alt text][pinout]
**Important**, the PCB itself is not polarized, does not have polarized components and does __not__ care if you connect it backwards!
However that assumes that you use non-polarized capacitors!

## Ordering
The files were sent off to to a manufacturer and got the ENIG treatment to enhance the artwork.
Total cost for the PCB came to aproximately €16.10 including shipping for 3 boards.

## Design files
If you desire to order these yourself, you can download the attached [gerber file](production/gerber.zip).
However you are encouraged to download the entire repo and verify the files yourself using
`git clone https://github.com/Cuprum77/BananaBoard.git`

Note that this project was originally built using KiCAD 6, however it has been updated to [KiCAD 7](https://www.kicad.org/download/).

## License
Hardware is licensed under [CERN OHL](LICENSE) while each artwork on the PCB are protected under their creators copyright and should be respected.

[singular]: https://github.com/Cuprum77/BananaBoard/blob/main/Images/single_pcb.jpg "PCBs from Aisler"
[trio]: https://github.com/Cuprum77/BananaBoard/blob/main/Images/all_pcbs.png "PCBs from Aisler"
[breadboard]: https://github.com/Cuprum77/BananaBoard/blob/main/Images/breadboard_example.jpg "PCBs from Aisler"
[pinout]: https://github.com/Cuprum77/BananaBoard/blob/main/Images/example-pinout.png "Pinout"
[BB830]: http://www.busboard.com/BB830T
