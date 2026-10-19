
*** Fixes for Altium Library Loader ***

*** Issues ***

1. Altium 26.1.1 and newer versions crashed on PCBServer.SendMessageToRobots.
2. ZIP extraction failed on Russian Windows because the script checked the localized f.Type value.

*** Fixes applied ***

1. Disabled the problematic PCBServer.SendMessageToRobots calls for PCB objects.
2. Fixed ZIP handling: the script now searches for .epw files by file extension instead of relying on the localized f.Type value.

The updated version was tested and confirmed working in:
Altium 26.1.1
Altium 26.5.0

*** Installation ***

Copy the script file AltiumLL.vbs to the following folder:

C:\Users\User Name\OneDrive\Documents\AltiumLL\


Then confirm file replacement.





18-10-26

Line 2413 modified to include "On Error.." because some times the http request fails and stops the script with a user error notification but the fail is not really important.