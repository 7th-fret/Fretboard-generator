What is this?
=============

This is a simple javascript tool for generating fretboard layouts for luthiers. You can specify various parameters, such as fret count, scale length, and whether you're targeting a CNC router or laser cutter, and then it'll generate a SVG or DXF file for you, that looks a little like this:

![Freboard](fretboard.svg)

It is provided free to use under the GNU Public License v3 license, copyright Michael Dales 2017.

For more details, visit http://electricflapjack.com/ or contact me at michael@electricflapjack.com.

Demo: https://electricflapjack.com/opensource/fretboard/

How to use this?
================

There's two ways I'd make use of a design file generated by this: using a laser cutter to etch the slots ready for sawing (the etching will make a nice groove the saw blade can follow), or by using this to drive a CNC router with a very small bit (e.g., a 0.5mm bit).

Personally I use the first method. The generated file will let you etch a grove that is 0.5mm wide, which you can then cut properly using a narrow saw. I use a Japanese Dozuki back saw with a 0.3mm blade, to cut the actual slots. Most fret wire have a tang width of 0.5mm, so using a 0.3mm saw means that you can hammer the frets into the slots without using any glue to hold them in.

I also turn on the fret alignment markings, which I resize in the laser cutter software to touch the edge of the wood I'm using, so that I can clearly mark the 0th and 12th fret on the back of the fretboard, and align with similar markings I've made on the neck piece.

The rough workflow I've used successfully is:

1. Take the fretboard wood, and laser etch on the fret groves - the dot inlays are in the DXF/SVG file for reference, but I do not cut or etch them.
1. Glue the etched fretboard to your neck using the optional alignment markers.
1. Before radiusing, use your dozuki saw to cut the fret slots, remembering that as you radius the board you will lose wood at the edge.
1. Hammer in the frets without using glue.

Alternatively you can select the CNN option which will generate a line rather than a slot, and use a very small router bit to make the slots. Again, you could just do a small pass with the router and saw them if you want to get away without using glue.


Still to do
============

* Find a way to make the DXF contain polylines, but that's probably more an issue with MakerJS than with this project.


Third party libraries
=====================

This project utilises three open source projects:

* jQuery - https://jquery.com/ (MIT license)
* MakerJS - https://maker.js.org/ (Apache License 2.0)
* Download - https://github.com/rndme/download (MIT license)
