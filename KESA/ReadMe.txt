Kerbin Engineering and Science Administration Resource Integration v0.1

The Module Manager config file contained herein changes the water resource used by the Interstellar plugin to be the same water resource used by the TAC Life Support plugin.  Addition integration between these two plugins and other plugins is planned for the future.

To install this addon, just place the KESA folder in your ../Kerbal Space Program/GameData folder.

In order for this addon to work, you MUST have the following plugins installed properly:

KSP Interstellar v0.9.1  (http://forum.kerbalspaceprogram.com/threads/43839)
TAC Life Support v0.7  (http://forum.kerbalspaceprogram.com/threads/40667)
Module Manager v1.5  (http://forum.kerbalspaceprogram.com/threads/55219)

Note:  Module Manager is included in the KSP Interstellar distrobution.  Thread link is included in case you need to download a new copy of Module Manager for some reason.

Known Issues:

- Any vessels launched prior to installing this addon will retain their KSPI LqdWater storage.  New vessels of the same design will not have any KSPI LqdWater storage.  New vessels launched of the same design will have the correct resources.
- Any vessels launched while this addon is installed, then loaded after this addon is uninstalled will retain their TACLS Water while receiving KSPI Water to the amount of the max amount it can store in stock KSPI.  New vessels launched of the same design will have the correct resources.

Change Log:

v0.1 - 12/XX/2013
- Changed nuclear thermal rockets to use TACLS Water instead of KSPI LqdWater.
- Changed the base water resource for Interstellar's plugin to use TACLS Water instead of KSPI LqdWater.
- Changed the oceans on Eve, Kerbin, and Laythe to contain TACLS Water instead of KSPI LqdWater.
- Changed the composition of the soil on Duna and Vall to contain ice that melts into TACLS Water instead of KSPI LqdWater.
- Changed the KSPI Water Storage Tank part to store TACLS Water instead of KSPI LqdWater.  Reduced the amount of water stored to account for using the higher density of water defined by TACLS.
- Changed the KSPI Refinery to extract TACLS Water when splashed down on Eve, Kerbin, and Laythe or landed on Duna and Vall.  Changed the small internal water tank to store TACLS Water instead of KSPI LqdWater.