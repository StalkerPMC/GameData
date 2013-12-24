Firespitter Plane parts and Helicopter Rotors by Snjo.
agogstad@gmail.com

License:
You may reuse any part of this pack, as long as you give credit in the download file and on the download post/page. For reuse of the plugin, please either direct people to download the dll from my official release on the spaceport, OR recompile the wanted partmodule/class with a new class name to avoid conflicts.
UV map texture guides are included so you can reskin to your liking.

The included sounds were taken from  a free sample off http://www.Sounddogs.com, and a public domain effect from http://soundbible.com/tags-propeller.html,
and helicopter sound from http://free-loops.com/7162-helicopter-sounds.html. Electric sound: http://soundbible.com/500-Electric-Motor-2.html
Mustang sound from this video: http://www.youtube.com/watch?v=-yTHDQZL1dE

v6.1.1
-Fixed some FAR Values. Included two example craft re-tweaked for FAR.
-A surprise

v6.1

-FAR values added to biplane wings and F-86 wings (FAR is optional as always!)
-CoM indicator bug fixed, replace engines on existing craft for a fix. (Removed 0/0 electric resource node from engines)
-Some wings have had module changes, which will reset the texture selection. For craft already in flight, you can EVA a Kerbal an Repaint the part.
-All example craft renamed with the prefix FS to make them easier to find
-Guide PDF updated
-Added Normal map (etc) switching support to FStextureSwitch

v6.0
Watch the video! http://www.youtube.com/watch?v=mhYmNTkQylM

-Biplanes! Make you own WWI planes with these new parts. Be an Ace or a Twenty-Minuter!
This is a whole matching part set with alternate switchable textures on each part.

-New custom lift and wing code that is more realistic and more customizable.
-Custom lift is used in the biplane parts and the F-86 wings. (The legacy F-86 wings are included as a zip in the Parts/Aero folder)
-Auto deploying leading edge slats, and flaps on the F-86 wings.
-KSP 0.23 Compatability with tweakables. Fewer silly popups, more nice tweaks.
-Action Group to increase/decrease hover height in heli/VTOL rotors.
-Wheels have less sideways friction for safer take offs and landings.
-Wheel motor reversing bug fix.
-FSwheel friction override bug fixed.

v5.6
-KSP 0.22 compatibility

Parts:
-Avro Lancaster Engines. Surface mounted big engines, one variant with internal landing gear, one without.
-All parts have been assigned a science node (costs have not been set)

Useful tweaks:
-FAR fix: if FAR is present, the control surface range module is disabled to fix incompatibility.
-Turned Allow Surface Attach on for tail control surfaces.
-The bomber cockpit is now less indestructible. (Fixed collider order)
-The bomber wings have proper collision detection
-Wheel and engine settings in the SPH now affect the whole symmetry group.
-VTOL steering can be toggled on and off with an action group (without affecting the steering setup)

Minor tweaks you don�t care about:
-Tweaks to the default rotation code in multi axis engine and part turner.
-atmospheric nerf can be disabled to allow for vacuum operations (the module itself is still required on relevant parts)
-FSwheel: suspension overrides can have negative values if overrideModelSpringValues = True 
-FSwheel: disable collider at a given time during retraction.
-VTOL steering supports models with inverted transforms through invertSteering = True

v5.5
-F-86 fighter jet wing with deployable leading edge for increased lift+drag
-F-86 tail control surfaces (elevators and rudder)
-Folding electric plane propeller
-Greatly reduced the weight of the landing gear. (Check the balance of your craft)
-Added brake lights to some gears
-Trim tool displays current trim
-Updatet gyroscope and nose SAS to use the new SAS module. Converted cockpits to the new reaction wheel system. (very weak reaction wheels) (thanks to PolecatEZ for some input)
-Water Launch Module: On slower machines, try setting a longer timer setting if you are put back to the runway at lunch. Edit the line timer = 4.0 to a higher value (seconds). (Parts\Utility\FS_moveCraftGadget\part.cfg)
-Plugin: Deprecated the FSswitchButtonHandler function, replaced by FSgenericButtonHandler. Removed FSbuttonHandler in favor of FSgenericButtonHandlerID

v5.4
-new landing gear functionality: motor, roll retracted, friction overrides, etc.
-VTOL steering (pitch and yaw through engine rotation, roll through thrust variation)
-Texture switcher module. Switch textures in the hangar for parts (Currently only implemented on Bomber nose art)
-New float code to combat the new KSP versions inability to float things.
-Updated Water Launch module to work with the new KSP version.
- Updated FAR values on the wings. Might allow for less bugginess. You still need to delete the FSwingletRangeAdjustment module in each wing cfg for full control though.
-Support for arrays of values in cfg files through FSnodeLoader

v5.3.1

Bug fix:
- The main propeller engine thrustTransform position was in the wrong place (on the new model)

v5.3

-Added the current version of the parts guide as a pdf in the zip
-Propellers at full speed switch to a blur graphic (editable cfg value)
-New model for the original propeller engines

v5.2

-Trim adjustment gadget
-Move to water at launch module
-VTOL action editor options
-fixed FSanimateGeneric always animating at launch
-Added static normal/reverse actions to the engine thrust reversers
-Bug fix: Electric rotors would try to reach parked rotation at odd times.
-Added thrustRPM functionality to FSplanePropellerSpinner

v5.1

-Bomb Bay (open the doors in the action editor for easier payload placement)
-Fuel drop Tank
-The Electric helicopter rotor can now start deployed (by using the action editor popup in the hangar)
-Engines with reverse thrust capabilities can now set default state in the hangar action editor
-FSanimateGeneric, replacement module for ModuleAnimateGeneric.
	(EVA toggle, custom speed, set start state in hangar, multiple animations per part)
-Bug fix: Wheel colliders spamming errors on launch
-Bug fix: GUI parts spamming nullrefs when launching from main menu directly to runway


v5.0 KSP 0.20.0

Changes:

Changed part names, now start with FS! Read more below.
fighterTailGear
bomberLandingGear
propellerEngine
PropellerEnginePush
PropellerEngineElectric
copterRotorMain
copterRotorMainElectric
copterRotorMainLarge
copterRotorTail
copterRotorTail2
copterRotorFenestron
copterRotorFenestronBothFins
copterRotorFenestronNoFins
FSswampEngine - corrected typo (FSswampEnginre)
fighterWing
jerrycan
fighterLandingGear

Changed many PartModule plugin class names.
Added a new module to handle engine sounds. Allows for sounds to run even at the bottom throttle levels on propeller engines. It more consistently plays the engage engine sound, and has an optional overheat warning sound.

Removed HoverEngine (now found in FS Experiments:
https://dl.dropboxusercontent.com/u/22972712/FSexperiments.zip

- Info Popup: The hot-key can be deactivated with a button, so it will not interfere with RCS keybinds in flight mode.

--- Important ---
All these re-namings will severely affect you ability to continue a saved game with craft that contain any of the engines or wings. Back up your save games!
It will also give errors on saved craft that contain these changed parts. You can, if you are a notepad hero, go into the craft file, find any part names or FS part module names that don't start with FS, and add FS to the names.
I successfully resurrected the included example craft this way. You will want to pull the engine off and replace it afterwards.

I'd really appreciate it if you play around with this and reported any errors on this forum.
Thanks, and I'm sorry if I broke your stuff :)

v4.2

- Electric 0.5m propeller
- Windmilling propellers, with constant spin rate while active.
- An  empty bomber fuselage section for reduced weight. (Take off with the included K-17 mk5 to see how much easier that is to get off the ground and land)
- f-86 style tail jet
- Info window popup part for explaining action groups etc. Good for shared craft files or hard to remember setups.
- 0.5m engine can now reverse for push prop setups, or taxiing (using a new module that can be used on any engine)
- Tail rotor max thrust is now 0.25-32 instead of 0.25-infinity
- Increased propeller engine isp from 1200 to 2000
- Increased old propeller response speed
- Increased node strength on the bomber parts. and landing gears. You can now land a heavy plane without breaking apart.
- Toggle engine ignition, landing gear brakes and retraction from EVA
- Air brake deployment state is now persistent
- Uncommented wing FAR values
- Performance tweaks (caching values), and made classes public
- crew fuselage IVA (not too pretty, but eliminates an IVA cam switch bug)
- hover switch now works in the original copter cockpit
- Apache monitors will display info window text

v4.1

Seaplane floats. Tail float with non lifting rudder (only works in water)
Smoothed the animation of the IVA flight sticks in non-precision mode
The tail gears now have 150 impact resistance to get around their tendency to blow up on takeoff/landing
Less info on the helicopter rotor context menu, so it will fit on screen.
Corrected attach points for the fighter cockpit

v4.0

Oblong Mustang style parts
-Fighter Cockpit w/ IVA
-Apache Cockpit with working monitors and experimental camera
-Liquid fuel, structural, battery, and rocket fuel fuselage
-Tail
-Nose engine mount
-0.5m nose engine with new sound
-Nose air intake
-round-oblong adapter
Bomber landing gear
Swiveling Apache gear with left/right asymmetry for wider stance
Radar altitude on context menu in some cockpits
Helicopter height hover lock
Experimental Hover Engine
Inline cockpit
IVA monitors can toggle gears, ASAS, Abort, etc. Display flight data and fuel.



v3.5.2

-The VTOL engines now automatically invert if on the left side of the craft, so all engines start out with the proper rotation setup.
v3.5.1
This update tweaks and fixes bugs. No new parts.

-Tail gears work again. Reverting to the vanilla setup means you can take off, but they won�t roll retracted. Win some, lose some.
-F.A.R. values included in the wings for users for Ferram�s mod. Uncomment the values at the bottom of the cfg files to enable.
-You can now adjust the range of control surfaces and winglet motion. Useful for tweaking the responsiveness of your craft, or shorter takeoffs. The module can be used in stock wings.
-Some small adjustments to lift values.
v3.5

-Double click the cockpit side windows and bombsight to switch to external cameras
-VTOL: Actions/context menu button to cycle through different max rotations, like 45, 90, 130.
-Increased the breaking force of the tail boom and engine mount. My VTOLs kept breaking apart.
-Removed fuel in the bomber wings to help fuel flow. Can be re-enabled in the cfg.
-Fixed large tail wing attach point. small boost in effect.
v3.4

-B17 style cockpit
-VTOL propeller engine
-ASAS and mechjeb works now
-key bind for auto hover
-prop rotor when idle
-Trimmable tail rotors
-Old trim system removed, using vanilla Alt+direction instead. Alt+x resets trim
-Swamp boat engine
-Wing extenders for the large wings
-Large fuselage and tail section
-Larger version of the tail wing
.craft files

BUGS: tail gear works poorly for taildraggers in 0.18.4. Works fine in 0.18.2
v3.3.1 HOTFIX

I forgot to include a resource file for the helicopter engines. Please re-download if you downloaded in the first 15 minutes. Sorry about that!
v3.3
New stuff:
-B-17 style wings. Big, with lots of lift. (So much that if you want to use them on smaller planes, you will want to reduce the lift in the cfg.)
-Tail winglets and rudders
-Nice engine mount for putting your propeller engines on the front of your wings.
-Deployable Air Brakes. Throw them on your wings or where ever you want, deploy with context menu or incrementally with action groups set in the hangar, and you will lose air speed rapidly for shorter landings.
-Regular non-fenestronian tail rotors. One with a wing for stack mount on the boom, one without wing for surface mount.
-Gyroscope, a small surface mountable avionics package.
-A WIP lighter, large cockpit with less torque. Just a reconfig of the Mark3, a mesh is coming.

Changes:
-All helicopter rotors have changed default orientation, so they are the right way when placed. This will mess up your existing craft. Consider skipping these parts if you are in the middle of a mission.
-Joystick support, and support for remapped keys. Precision mode also works. Using a joystick, wheel steering is now actually very useful.
-Almost every part looks sharper, due to a better way of setting shading on them.
-Electric rotors use a custom air resource (FSCoolant) to not be overpowered air intakes for jets.
-No visible air intake thingie on the electric propeller rotor.
-The auto hover now has limited rotation angles, making it weaker, but less jarring.
-Some texture changes.
-The passenger fuselage has a new simpler mesh. I've tried to keep the UV map exactly the same, but some changes to a custom texture will probably be required.
-Probably other stuff I've forgotten.

v3.2

-Bug fix: The fenestron could stop a TTech nuclear reactor from charging. Fixed by setting idle maxThust to 0.001.
-Bug fix: Overheating due to hover is back

v3.1

-New and improved fenestrons (tail rotors). No longer uses RCS effect, but works more like an engine. Toggle output strength by context menu.
Consumes a little bit of electricity. Because it is now possible to place the wrong way around for steering, there�s a little arrow that should be pointed down on the part, and the option to invert steering by right clicking it.
-Two additional fenestron models by request, one without fins, one with two.
-Auto hover now works on other planets and continents. (A coding challenge, but not noticeable if you just stayed around KSC)
-Tripled the ISP of the electric engines

v3.0

-Sweeping changes to the atmospheric performance. Thrust levels depend on thickness of the atmosphere.
-A cockpit with internals. Less built in SAS for better helicopter performance.
-Larger selection of airplane and helicopter engines, including electric.
-Action groups to toggle max thrust on the helicopter engines.
-Auto hover with F. Watch out for overheating!
-Many other tweaks

v2.3
-Realism update for the helicopter engine:
Please note the painted arrow to place correctly
You can trim the engine with Alt
No RCS effect, altering instead the angle of the main thrust
The swashplate tilts
Proper constant spin speed, with spin up/down time
Easier placement (collisions allowed)
-Reversible main plane propeller (context menu)
Please note that the engine has been flipped 180 degrees. This will affect already built craft. Skip this part if you are worried about an ongoing flight. (FS_propEngine)
-Steerable, trimmable landing gear (context menus and action groups)
-There�s a bit of fuel in the wings, with room for more
-A passenger carrying fuselage with a bit of fuel in it. The model/texture is still WIP.
-A Jerry can

v 2.2
-Fighter plane wings
-You can turn the wheels using context menus or action groups. Might be good for rovers.
-A pushing variant of the propeller engine
Note: the Part folder names now start with FS_, you might want to clean out the old ones. Sorry for the mess

v 2.1 Hotfix:
Wheel brakes now work thanks to input from c7studios. And source code included in the package.
-There is a chance you may need some force to start moving again after stopping completely with parking brakes. This is due to the craft entering Landed state, and is a general game issue with planes.

v 2.0
-Helicopter main rotor and tail rotor.
-Better textures
-Main wheels visually roll
-Symmetrical placement of gears
-Editable textures with UV maps.

v 1.0
Initial Release
-Landing Gear
-Tail Gear
-Propeller engine
-Fighter Wings
