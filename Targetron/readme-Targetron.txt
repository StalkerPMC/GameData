Targetron - Kerbal Space Program
Author: Jarcikon

This plugin displays a window listing all vessels in flight (including debris) in a convenient list, and allows you to target or take control of any vessel quickly. The list can be sorted by distance or vessel name and filtered by search text or vessel type. You can also right click a listed vessel to rename or, if close enough, target available docking ports.

The title bar displays the current target followed by an icon to change the sort mode (right click to cycle through sort modes in reverse). On the far right the green icon will minimize the window to a small placeholder when you are not using Targetron. Click the green icon again to restore the window.

Below the title bar is the target list. This list shows all available flights based on the search/filter critera. Each vessel name is listed followed by the distance from your current location. Your current target is listed in orange. Vessels which are controllable are listed in green. Debris is listed in gray. The target icon will set the listed vessel as your current target. The rocket icon will switch control to the listed vessel.

The bottom bar contains a search box. Only vessel names containing the search text will be listed. To the right of the search box is a series of icons to filter by vessel type. Only vessel types with icons lit (disabled icons are grayed out) will be displayed.

Right click any vessel (or left click when inside your ship) to open a context menu. Here you can rename the selected vessel as long as you are close enough (within a few km). You will also see available docking ports, which can be targeted when you are within ~200m. To help identify each docking port, the actual part will highlight red as you hover over it's listing.

You can resize the window by clicking and dragging the bottom-left or bottom-right corners.

Pro Tip: Right click a vessel type icon, then left click another icon and it will enable/disable all vessel types between the two.


FILE CONTENTS:
==========================
readme-Targetron.txt
GameData/Targetron/Plugins/Targetron.dll
GameData/Targetron/Icons/base.png
GameData/Targetron/Icons/debris.png
GameData/Targetron/Icons/dist_asc.png
GameData/Targetron/Icons/dist_desc.png
GameData/Targetron/Icons/eva.png
GameData/Targetron/Icons/flag.png
GameData/Targetron/Icons/lander.png
GameData/Targetron/Icons/name_asc.png
GameData/Targetron/Icons/name_desc.png
GameData/Targetron/Icons/nw-resize.png
GameData/Targetron/Icons/probe.png
GameData/Targetron/Icons/rocket.png
GameData/Targetron/Icons/rover.png
GameData/Targetron/Icons/ship.png
GameData/Targetron/Icons/station.png
GameData/Targetron/Icons/sw-resize.png
GameData/Targetron/Icons/target.png
GameData/Targetron/Icons/targetron.png
Source/Targetron.cs
Source/ToolbarWrapper.cs


INSTALLATION:
==========================
*****If upgrading from v1.0 or v1.1, delete Plugins/targetron.dll and PluginData/Targetron before installing!*****

1) Unzip the contents into the main KSP installation folder, or copy the contents of GameData into the {KSP Root}/GameData Folder. The Source folder is not required for functionality, only for developers wishing to see or modify the plugin code.

2) Restart KSP and the window will appear once in flight. No special parts are required to activate this plugin.


VERSION HISTORY:
==========================
v1.3.1 - 12/24/2013 - Added optional integration with Blizzy78's Toolbar Plugin (http://forum.kerbalspaceprogram.com/threads/60863-0-23-0-Toolbar-1-2-2-Common-API-for-draggable-resizable-buttons-toolbar)
			
v1.3 - 12/19/2013 - Docking ports listed on right-click context menu now highlight red when hovering over the listing
		  - Bug fix for lag when in EVA mode
		  - Added Target/Control options in right-click context menu
		  - Added vessel type icon next to each listing
		  - Right click sort mode icon to cycle in reverse
		  - Removed delay when changing sort modes
		
v1.2.2 - 10/6/2013 - All measurements are now in m, km, Mm, Gm, etc. (AUs removed)

v1.2.1 - 9/21/2013 - Fix for ISP mode (left click for context menu). Rename vessel option only works when the vessel is loaded (within a few km, I believe). Command vessel option only available if the clear to save flag is set.

v1.2 - 9/8/2013	- Added sorting, search filter, and vessel type filters
		- Right click listed vessel for context menu to rename or target available docking ports
		- Distances over 10 million km are displayed in AUs. Fixed bug for position and size not saving correctly

v1.1 - 8/20/2013 - Update for 0.21 compatibility and added tooltips

v1.0 - 5/11/2013 - Initial Release


Source code is free to use for non-commercial purposes under GPL3.