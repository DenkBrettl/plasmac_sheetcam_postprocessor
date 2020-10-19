# plasmac_sheetcam_postprocessor
A SheetCam PostProcessor for the LinuxCNC PlasmaC configuration

SheetCam PP for Plasmac (PlasmaC.scpost)

*** REQUIRED SETTINGS IN SHEETCAM ***
Navigate to Options >> Job options >> Tool change and deselect Use X, Use Y and Use Z 

*** USER OPTIONS IN THE POSTPROCESSOR***
There are four user defined options near the top of the PP, set these up as you prefer.

These two will show/hide the custom tool parameters when you view a tool:
cParms      = 0 -- set to 1 to show basic custom parameters
pmx485      = 0 -- set to 1 to show RS485 parameters

The next one will show/hide linunumbers in the resulting G-Code file:
lineNumbers = 0 -- set to 1 to show linenumbers

The next one difines whether arcs will processed as arcs or line segments:
noArcs      = 0 -- set to 1 to convert arcs to line segments

*** CENTRE SPOTTING ***
To do centre spotting you will need one of:
 Drill Operation (using any tool)
 Plasma tool named Centre Spot
 Plasma tool named Center Spot

*** SCRIBING ***
To use a scribe you will need to use one of:
 Marker tool (Plate Marker)
 Plasma tool named Air Scribe
 Plasma tool named Engraver
You will also need tool number 1 in the LinuxCNC tool table set with the correct X and Y offsets

------------------------------------------------------------------------------------------------

SheetCam Tool File for Plasmac (PlasmaC.tools)

The tool file only has code snippets and cut rules.

You could either:

1.  use this as your tools file and just add any required tools within SheetCam

2.  copy the contents and paste it to the end of your existing tool file and renumber any [Tooln] appropriately
