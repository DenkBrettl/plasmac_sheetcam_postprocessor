# plasmac_sheetcam_postprocessor
A SheetCam PostProcessor for the LinuxCNC PlasmaC configuration

SheetCam PP for Plasmac (PlasmaC.scpost)

*** REQUIRED SETTINGS IN SHEETCAM ***
<br>Navigate to Options >> Job options >> Tool change and deselect Use X, Use Y and Use Z 

*** USER OPTIONS IN THE POSTPROCESSOR***
<br>There are four user defined options near the top of the PP, set these up as you prefer.

These two will show/hide the custom tool parameters when you view a tool:
<br>cParms      = 0 -- set to 1 to show basic custom parameters
<br>pmx485      = 0 -- set to 1 to show RS485 parameters

The next one will show/hide linunumbers in the resulting G-Code file:
<br>lineNumbers = 0 -- set to 1 to show linenumbers

The next one difines whether arcs will processed as arcs or line segments:
<br>noArcs      = 0 -- set to 1 to convert arcs to line segments

*** CENTRE SPOTTING ***
<br>To do centre spotting you will need one of:
<br>Drill Operation (using any tool)
<br>Plasma tool named Centre Spot
<br>Plasma tool named Center Spot

*** SCRIBING ***
<br>To use a scribe you will need to use one of:
<br>Marker tool (Plate Marker)
<br>Plasma tool named Air Scribe
<br>Plasma tool named Engraver

You will also need tool number 1 in the LinuxCNC tool table set with the correct X and Y offsets

------------------------------------------------------------------------------------------------

SheetCam Tool File for Plasmac (PlasmaC.tools)
<br>The tool file only has code snippets and cut rules.

You could either:
<br>1.  use this as your tools file and just add any required tools within SheetCam
<br>2.  copy the contents and paste it to the end of your existing tool file and renumber any [Tooln] appropriately
