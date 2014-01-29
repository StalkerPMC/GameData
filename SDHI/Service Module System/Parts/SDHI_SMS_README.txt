Sum Dum Heavy Industries Service Module System - Mod Parts Pack

Version:	1.7	(KSP 0.23+)

Author: 	Robin "sumghai" Chang	techadv@alphacompanyforums.com

License:	Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)
		http://www.creativecommons.org/licenses/by-sa/3.0/

Disclaimer:	This parts pack is for an alpha game - Use at own risk. 
		If your computer blows up, it's not my problem.



===Dependencies===

Parts in this pack conform to the new CFG file definition scheme, and as such are only compatible with KSP versions 0.23+.

Two external plugins are required, and will need to be downloaded separately:

 - stupid_chris's RealChute Parachute Systems plugin, for parachute functionality.

 - Snjo's Firespitter plugin, for the tweakable IACBM guidance fin animations.



===Installation Instructions===

(NOTE: Make sure that any previous versions of the parts pack are removed before installation) 

Copy all contents from GameData folder into its namesake in your KSP installation.



===Usage===

 - This parts pack is specifically designed for use with the stock Mk1-2 Command Pod

 - For detailed assembly / configuration instructions, refer to http://bit.ly/kspSumghaiSDHI_SMS_Manual

 - No Launch Escape Systems or Escape Towers are included in this pack; either build your own using stock parts, or try the ones from KSPX or BFGfreak's Prilla LES add-ons.



===Uninstallation Instructions===

Remove the SDHI folder and all its contents from the GameData folder.

If you have other SDHI part packs you wish to keep, just remove the Service Module System subfolder.


===Release Notes===
1.7          13 January 2014
---------------------------

Changes / Fixes
 - Dropped FusTek_Sumghai.DLL in favour of external dependency on Snjo's Firespitter plugin
    - You will need to download and install the latest version of Firespitter yourself
    - This change now allows the IACBM guidance fins to be tweakable within the VAB/SPH


1.6          24 December 2013
---------------------------

Changes / Fixes
 - Added new 0.23 EFFECTS{} for parachute sounds (stupid_chris)
 - Tweaked main parachute deployment altitude slightly; the mains will now deploy almost immediately after drogues are cut, instead of after a (decidedly terrifying) period of free-fall. 


1.5          8 December 2013
---------------------------

Changes / Fixes:
 - Compatibility upgrade to take advantage of new features in RealChute v0.3
    - Parachute drag is now dependent on effective canopy area rather than stock drag
    - Command Pod assembly will now hang under parachute anchor realistically without the need for the CoMOffset hack, and as such the latter has been removed


1.4          24 November 2013
---------------------------

Changes / Fixes:
 - Parachute-equipped docking ports now use stupid_chris's RealChute Parachute Systems plugin
    - Drogues will now auto-cut properly before automatically deploying the main chutes
    - Docking port lights can now be toggled normally during parachute deployment
    - This is not included in the pack, so you will need to download it separately
 - Updated drogue parachute textures to distinguish them from the main parachutes



1.3          8 November 2013
---------------------------

Features:
 - New Part
    - SDHI 2.5m Avionics Ring
 - Avionics Ring is essentially the upper decoupler portion of the full Service Module, with a bonus battery, reaction wheel and toggleable integrated fuel-to-electricity converter
    - This is particularly useful for people who want to build their own Service Module, but also use the SDHI Heat Shield and Boost Protective Cover 


1.2          25 October 2013
---------------------------

Changes:
 - VAB/SPH: Moved SDHI 2.5m Service Module Adapter and SDHI 2.5m Service Module Fairing to Aero tab
 - R&D: Moved SDHI 2.5m Service Module Adapter to "Supersonic Flight" node
    - If you have unlocked this part previously in Career Mode, you will need to edit your persistence file to temporarily remove the adapter from the list of unlocked parts, and then re-unlock after restarting the game
 - Modified SDHI Mk1-2 Pod Boost Protective Cover collider to allow the Mk1-2 Pod underneath to be selected
    - Hover your mouse pointer over the "Cut To Rescue" graphic on the cover and right-click



1.1          17 October 2013
---------------------------

Changes:
 - Compatibility Patch for KSP 0.22+
 - All parts have now been assigned to the appropriate nodes in the Research & Development Tech Tree
    - Parts are in the same Tier Level as the Mk1-2 Command Pod (i.e. Tier 5)
    - "Specialized Construction" unlocks:
        - SDHI 2.5m Heat Shield
        - SDHI 2.5m Service Module Adapter
        - Clamp-O-Tron Docking Port - Parachute version
        - IACBM 1.25m - Parachute version
    - "Supersonic Flight" unlocks:
        - SDHI Mk1-2 Pod Boost Protective Cover
        - SDHI 2.5m Service Module Fairing
    - "Heavier Rocketry" unlocks:
        - SDHI 2.5m Service Module
        - LV-909 Liquid Fuel Engine (Fairingless)



1.0          12 October 2013
---------------------------

Features:
 - Initial release
 - New parts
    - SDHI Mk1-2 Pod Boost Protective Cover
    - Clamp-O-Tron Docking Port - Parachute version
    - IACBM 1.25m - Parachute version
    - SDHI 2.5m Heat Shield
    - SDHI 2.5m Service Module
    - LV-909 Liquid Fuel Engine (Fairingless)
    - SDHI 2.5m Service Module Fairing
    - SDHI 2.5m Service Module Adapter
 - Boost Protective Cover is ogive-shaped to fit stock Mk1-2 Pod and any surface-attached accessories underneath
    - Staging activates both the shroud decoupler and jettison solid rocket motors
    - If shroud jettison is to be triggered via action groups, both the decoupler and the solid motors must be manually mapped to the same action key
 - Docking Ports come with short-range illumination lamps and integrated drogue/main parachute system
    - Clamp-O-Tron variant is compatible with stock standard-sized docking ports
    - IACBM variant is compatible with the FusTek Station Parts Expansion add-on
 - Service Module comes with:
    - Non-staged CM-SM decoupler to prevent accidental Pod/Service Module seperation during flight (action groups or right-click context menu used instead)
    - Toggleable integrated fuel-to-electricity converter for use


Bugs/Known Issues
 - Drogue parachutes do not auto-cut until mains are fully deployed
    - This is due to the use of *two* ModuleParachutes, which is technically "hacky" by KSP standards
    - Unlike BobCat's Orion spacecraft, however, the parachute-equipped docking ports will use the greater of the two drag configurations, guaranteeing a safe landing
        - Warranty void if parachutes are deployed on a planetary body other than Kerbin
 - Docking Port Lights become untoggleable after parachute deployment
    - This is because of the way KSP handles animations; the game can only save the state of one animation at a time, and the docking ports need several animations to handle the various parachute deployment stages and the lights.
