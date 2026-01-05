Custom Everquest maps for use with the Zeal addon, on the Quarm server

## How to Use
- Install Zeal from https://github.com/CoastalRedwood/Zeal/releases
- Make a folder called map_files in your eq directory, and put the text file for the maps you want in there.
- Use the command `/map data_mode nointernalpoi` to get the custom points to appear instead of the default points. Or use `/map data_mode both`to get the custom points along with the default.
You could also go into Zeal options > Map > Map data source, and turn it to `Both - No Internal POI` or `Both` to get the same results as the commands. 
You'll also need to turn Labels to All within the Zeal map options. You can cycle through the options with a hotkey if you assign one via zeal options > Keyboard > ToggleMapLabels

## Contents
The text files, like `nexus.txt` contain custom map data for the zone which matches the name of the file. For each map, there is an image which is not needed for the map to function. They are just there to preview the map.

In general, these maps are not made for things like raid content or deep strategic information. My focus is on general information for a zone. Think of them as post-it notes added to certain maps.

## Map Generation
I use a spreadsheet to help translate actual in-game points to the format expected by the Zeal map parser. I've shared a basic version of the spreadsheet here: 
https://docs.google.com/spreadsheets/d/1NUBPFq8bBZBE8T703Oy-7_vSVP0Q8Q6R8jZiL-kCSNI
### Columns
- Column A is just used for notes
- Column B is the code that should be pasted into a map text document
- Column C is the label text that will be added to the map. Or if the generated code is a line, it is just a note.
- Columns D,E,F are for the color of the marker as RGB values from 0 to 255
- Columns G,H,I are the position of the label or line point. The Z value currently has no effect on the output.
- Columns J,K are used for moving the entire marker quickly. Sometimes when generating a group of markers, you will find that you have the spacing right, but want to move everything over by a certain value. This is a quick way of pasting in a move distance without having to do the math for every point in a collection.
- Columns L,M are the calculated midpoints of a box or line. Useful as a reference for positioning multiple elements.
### Rows
- Rows 3-4 are examples of labels. Labels are placed on a single point. Row 3 and 4 are each individual labels.
- Rows 6-9 make up a single box. If you want to create a new box, copy all 4 rows. For Y and X values, put the top left point in the first row, and the bottom right point in the second row. 4 lines of code will be generated which represent the full box.
- Row 11 is a single line. Input the Y and X values of the start and end points to generate a line between those points.

## Current maps
- South Karana (southkarana.txt)

Useful for hunting Quillmane. Spawn points are marked with magenta crosses, placeholders are noted in the top right
- Thurgadin (thurgadina.txt)

Gives a reminder on the steps needed to create the Thurgadin Gate Potion (Vial of Velium Vapors)
- Timorous Deep (timorous.txt)

Adds labels showing the destination of the firepots which are easier to see than the default labels, which require zooming in
- Bazaar (bazaar.txt)

Simple info about the charisma needed to get the best value from npc merchants