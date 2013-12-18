Kerbal Joint Reinforcement, v1.5
Copyright 2013, Michael Ferrara, aka Ferram4


    This file is part of Kerbal Joint Reinforcement.

    Kerbal Joint Reinforcement is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    Kerbal Joint Reinforcement is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with Kerbal Joint Reinforcement.  If not, see <http://www.gnu.org/licenses/>.


This plugin stiffens the connections between parts, reducing the wobble between part.  It also has the option to further stiffen the connections between parts connected to decouplers and launch clamps.

***************************************************
****** INSTALLING KERBAL JOINT REINFORCEMENT ******
***************************************************

Merge the GameData folder with the existing one in your KSP directory.  KSP will then load it as an add-on.
The source folder simply contains the source code (in C#) for the plugin.  If you didn't already know what it was, you don't need to worry about it; don't copy it over.


********************************
****** EXCITING FEATURES! ******
********************************

-- Stiffness of joints now scales with connection area size

	- No need to add struts between part stacks if the parts are wider than 1.25m
	- High thrust / heavy engines don't need to be strutted to the tank above them to prevent part dancing / sliding off axis under load
	- Larger parts will have stiffer connections to balance their larger masses / sizes


-- Option to stiffen interstage connections

	- Parts connected to a decoupler will be connected to each other, reducing flex at the connection to reasonable levels


-- Option to stiffen launch clamp connections

	- Less vehicle movement on vessel initialization
	- Warning: may cause spontaneous rocket disintegration if rocket is too large and overconstrained (far too many lanuch clamps; their connections will fight each other and give rise to phantom forces)


-- Option to make connection strengths weaker to counteract increases in stiffness


-- Joint Stiffness parameters can be tweaked in included config.xml file

	- config value documentation:


General Values

	Type	Name				Default Value		Action

	bool	reinforceAttachNodes		1			--Toggles stiffening of all vessel joints
	bool	reinforceDecouplersFurther	1			--Toggles stiffening of interstage connections
	bool	reinforceLaunchClampsFurther	1			--Toggles stiffening of launch clamp connections
	bool	debug				0			--Toggles debug output to log; please activate and provide log if making a bug report
	float	massForAdjustment		0.01			--Parts below this mass will not be stiffened

Linear "Soft" Movement Limit

	Type	Name				Default Value		Action

	float	linSpring			500			--Stiffness of spring used for soft limit of linear joint movement; larger values increase stiffness, 0 "locks" movement (doesn't truly lock)
	float	linLim				0.05			--Distance part can move before it hits linear limit
	float	linDamp				5			--Strength of movement damper used for soft limit of linear joint movement; larger values increase strength, 0 "locks" movement (doesn't truly lock)
	float	linBounce			0			--Ranges from 0 to 1, how much the part can "bounce" off the limit;

Angular "Soft" Movement Limit (Currently zeroed; read: disabled)

	Type	Name				Default Value		Action

	float	angSpring			0			--Stiffness of spring used for soft limit of angular joint movement; larger values increase stiffness, 0 "locks" movement (doesn't truly lock)
	float	angLim				0			--Distance part can move before it hits angular limit
	float	angDamp				0			--Strength of movement damper used for soft limit of angular joint movement; larger values increase strength, 0 "locks" movement (doesn't truly lock)
	float	angBounce			0			--Ranges from 0 to 1, how much the part can "bounce" off the limit;

Linear "Drive" Values (universally scales linear strength of connections)

	Type	Name				Default Value		Action

	float	linearDriveSpring		50000			--Factor used to scale stiffness of linear connections
	float	linearDriveDamper		20			--Factor used to scale damping of motion in linear connections
	float	linearMaxForceFactor		1			--Factor used to scale maximum force that can be applied before connection "gives out"; does not control joint strength

Angular "Drive" Values (universally scales angular strength of connections)

	Type	Name				Default Value		Action

	float	angularDriveSpring		100000			--Factor used to scale stiffness of angular connections
	float	angularDriveDamper		600			--Factor used to scale damping of motion in angular connections
	float	angularMaxForceFactor		1			--Factor used to scale maximum force that can be applied before connection "gives out"; does not control joint strength

Joint Strength Values

	Type	Name				Default Value		Action

	float	breakForceMultiplier		1			--Factor scales the failure strength (for forces) of joint connections; 1 gives stock strength
	float	breakTorqueMultiplier		1			--Factor scales the failure strength (for torque) of joint connections; 1 gives stock strength
	float	breakStrengthPerArea		40			--Overrides above values if not equal to 1; joint strength is based on the area of the part and failure strength is equal to this value times connection area

Part and Module Exemptions

	Type	Name				Default Value		Action

	string	exemptPartType0			MuMechToggle		--Part stiffening not applied to this type of "Part"; exemption to avoid interference with Infernal Robotics
	string	exemptPartType1			MuMechServo		--Part stiffening not applied to this type of "Part"; exemption to avoid interference with Infernal Robotics

	string	exemptModuleType0		WingManipulator		--Part stiffening not applied to parts with this type of PartModule; exemption to prevent problems with pWings
	string	exemptModuleType1		SingleGroupMan		--Part stiffening not applied to parts with this type of PartModule; exemption to prevent problems with procedural adapter included with pWings
	string	exemptModuleType2		KerbalEVA		--Part stiffening not applied to parts with this type of PartModule; exemption to prevent problems with Kerbals in command seats

Further part and module exemptions can be added using the same formating and changing the number


Decoupler Stiffening Extension Types

	Type	Name					Default Value		Action

	string	decouplerStiffeningExtensionType0	ModuleEngines		--Decoupler stiffening will look for parts beyond this part type to add to stiffening
	string	decouplerStiffeningExtensionType1	ModuleHybridEngine	--Decoupler stiffening will look for parts beyond this part type to add to stiffening
	string	decouplerStiffeningExtensionType2	ModuleHybridEngines	--Decoupler stiffening will look for parts beyond this part type to add to stiffening
	string	decouplerStiffeningExtensionType3	ModuleEngineConfigs	--Decoupler stiffening will look for parts beyond this part type to add to stiffening
	string	decouplerStiffeningExtensionType4	ModuleDecouple		--Decoupler stiffening will look for parts beyond this part type to add to stiffening
	string	decouplerStiffeningExtensionType5	ModuleAnchoredDecoupler	--Decoupler stiffening will look for parts beyond this part type to add to stiffening
	string	decouplerStiffeningExtensionType6	ProceduralFairingBase	--Decoupler stiffening will look for parts beyond this part type to add to stiffening


***********************
****** CHANGELOG ******
***********************
v1.5
Features
--Updated to KSP 0.23
--Joint breaking strength can now be set to be dependent on connection area, so large part connections can have realistically large strength; on by default
--Vessels are further strengthened for the first 30 physics frames after coming off rails or loading; this helps prevent jitters during intialization from breaking things apart

Bugfixes:
--Fixed launch clamps not being clamped to the ground after staging
--Fixed an issue where the Kraken would throw launchpads at craft in orbit

v1.4.2
Bugfixes
--Fixed an issue that would allow more wobble to exist than it should have
--General tweaks to reduce wobbling further

v1.4.1
Bugfixes
--Fixed an issue where maximum joint forces were calculated incorrectly
--Fixed an issue where docking could cause exceptions to be thrown and cause lag

v1.4
Features
--Changed calculation of surface-attached connection area to be more accurate

Bugfixes
--Fixed an issue where lots of wobble would occur between stack-attached parts of very different sizes

v1.3
Features
--Better solution for failure to apply decoupler ejection forces
--Will not apply stiffening to parts below a given mass; mass can be changed in config
--Properly updates on docking

Bugfixes
--Fixed a serious issue where launch clamps would lock the ship to the surface

v1.2
Features
--Workaround for stock KSP bug where struts would prevent decoupler ejection forces from being applied

Tweaks
--Reduced default maxForceFactors to be more reasonable levels

BugFixes
--Fixed serious issue where struts would not properly disconnect
--Fixed serious issue where decouplers would not function properly


v1.1
Features
--Stiffness of joint no longer erroneously dependent on breakForce / breakTorque
--Decoupler stiffening function made more comprehensive

BugFixes
--Fixed an issue where radial decouplers would not be affected by by further decoupler stiffening
--Fixed an issue where decoupler further stiffening would cause Nulls to be thrown when attached to physics-disabled parts
--Fixed an issue where procedural fairings would be locked to the rocket
--Fixed an issue where Infernal Robotics parts would not function
--Temporary stopgap measure: stiffening not applied to pWings to prevent ultra-flexy wings

Known Issues
--Decouplers create no detach force with extra decoupler stiffening enabled
	Same issues as strut attachment bug

v1.0
Release