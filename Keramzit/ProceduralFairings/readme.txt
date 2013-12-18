--- Forum thread ---
http://forum.kerbalspaceprogram.com/showthread.php/39512-0-21-Procedural-Fairings-2-1-base-rings-new-models-and-more

--- Download ---
http://kerbalspaceport.com/procedural-fairings/

--- License ---
http://creativecommons.org/licenses/by/3.0/


--- Finding the KSP main folder ---
The first step to installing an add-on is to locate the KSP folder in your computer. This is where KSP keeps all of its files, including your game saves and screenshots. The KSP folder is located where you unzipped it when you first downloaded the game. If you got KSP from Steam, right-click it in your Steam library and select "properties", then switch to "local files" tab and press "browse local files". This should open the game folder. In the KSP main folder there's "GameData" folder which contains all add-ons. If you didn't install any, it'll have only "Squad" sub-folder - that's stock "add-on" from the developers of the game.


--- Installation ---
Unzip GameData folder into your KSP folder, so that you have KSP/GameData/Keramzit/ProceduralFairings folder.
Don't try to put files in any other folders, it won't work.
You don't need "Source" folder, unless you want to modify and compile plug-in code yourself.


--- How to use ---
Tutorial:
http://imgur.com/a/xCF0q

The parts are in the Aerodynamics tab.
Put a fairing base under your payload. Remember to add a decoupler if you need one.
Attach side fairing and it'll be reshaped for your payload automatically.
Enable symmetry and you get a nice rocket.
Remember to rearrange stages to jettison fairings at the proper stage.
Change your payload, and the fairings will adapt to it.
Fairing bases come in all sizes, the same side fairings can be used with all of them.

If you flip another fairing base upside down and add it above your payload, the side fairings will stick to it instead of creating a nose cone, so you get inline fairings between two bases.
There are low-profile base rings intended for inline fairings, but you can use them for the regular ones as well.

Mouse over the fairing side and press F to adjust ejection force.
Mouse over the fairing side and press L to lock/unlock fairing shape (it's for advanced use, you most likely don't need this).

Hold R and move mouse over the fairing base to adjust side fairing radius. This will also affect base/nose cones.
Mouse over the fairing base and press G to toggle fuel crossfeed (disabled by default). You can also do it from right-click menu in flight.
Mouse over the fairing base and press T to toggle auto-struts (enabled by default). These invisible struts hold side fairings together. You might still need to strut your payload to prevent wobble.

Hold N and move mouse over the interstage adapter to adjust its base radius.
Hold Y and move mouse over the interstage adapter to adjust its top radius.
Hold H and move mouse over the interstage adapter to adjust its height (position of the top node).
Hold J and move mouse over the interstage adapter to adjust extra fairing height (above the top node).


--- Version history ---
2.4.3
Improved payload scanning for interstage adapter.
Recompiled for KSP 0.23.

2.4.2
Zero-radius payload is now used when no payload attached, so fairings will always reshape.
Added parts to the tech tree.
Moved fuselage shrouds to Structural tab.
Changing adapter attachment node size with radius.

2.4.1
Disabled fuel crossfeed on the interstage adapter - enable at your own risk, it confuses Engineer Redux to death.
Added stock decoupler module to the interstage adapter topmost node to help with delta-v calculations.
Improved fairing shape for interstage adapter when fairing top is inside payload.

2.4
Added procedural interstage fairing adapter with adjustable radii and height which decouples from the top part when fairings are ejected.
Added conic fuselage.
Fixed another inline fairing shape bug.

2.3
Changed fuselage texture to distinguish it from fairings.
You can now lock fairing shape: mouse over the side fairing/fuselage and press L.
Reduced side nodes size for smaller base rings and 0.625m fairing base (for easier placement).
Fixed inline fairings making a top cone when there should be just a cylinder.

2.2
Added experimental egg-shaped fuselage (a side fairing without decoupler).
Moved fairing decoupler code to separate PartModule.
Auto-struts are now created between the top inline base and side fairings as well. NOTE: if you payload is wobbly, the sides might still wobble.
Fixed bug with misplaced fairings on new ring bases.

2.1
Added low-profile fairing bases (base rings), intended for inline fairings. All of them have 4 side fairing attachment points.
Replaced base model with one that looks more lightweight. It has the same size etc., so it won't break your existing ships.
You can now toggle fuel crossfeed for fairing base: mouse over and press G in editor or use right-click menu in flight.
You can now disable auto-struts between side fairings: mouse over the base and press T.
Fixed inline fairings not connecting with the top base sometimes.
Fixed nested inline fairings not connecting to the proper base.
Fairing outline (blue lines) is not displayed now for inline fairings if sides are attached to any of the two bases.

2.0
Inline truncated fairings are now created between two bases (one must be flipped). It won't work properly for off-center bases. If you want it off-center, tell me what for and how it should look.
You can now change ejection force by pressing F when mouse is over the side fairing.
Fixed rapid unplanned disassembly of side fairings when going out of time warp sometimes.

1.3
Fixed ejection direction bug - it shouldn't matter how you place fairings now.

1.2
Added invisible automatically placed struts between side fairings to mostly eliminate wobble.
Replaced ejectionNoseDv with ejectionTorque so that all ejected fairings have the same motion, regardless of shape.
Improved payload scanning for better fitting of mesh and box colliders.
You can now adjust radius by moving the mouse over the base part while holding R (the default key, can be changed in part .cfg).
Fixed "recursion" bug which caused misplaced fairings to grow out of control. (It's also a foundation for future inline fairings).
Using a (hopefully) better method to offset side fairing center of mass.
Using proportionally smaller part of texture for 1/3 (and smaller) side fairings to reduce texture stretching.
Renamed "capsule-shaped" fairings to "egg-shaped" to be more Kerbal.

1.1
Fix for future FAR compatibility (needs fixed FAR version to actually work).
Less rotation on eject to reduce collisions with payload and lower stages.
Conic side fairings added, original ones are made a bit more capsule-shaped.

1.0
Initial release.
