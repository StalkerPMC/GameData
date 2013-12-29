**--------------------------------**
||Docking Port Alignment Indicator||
||--------------------------------||
||----------Version 3.0-----------||
||-------Author: NavyFish---------||
**--------------------------------**

Thanks for trying out this mod! Check out the forum thread if you have any questions 
or would like to make suggestions.

http://forum.kerbalspaceprogram.com/threads/43901-0-23-Docking-Port-Alignment-Indicator-%28Version-3-0-Updated-12-18-13%29

Installation:

  
  *************************************IMPORTANT!!********************************************
  ********************************************************************************************
  **                                                                                        **
  **      Prior to installation, make sure to delete all previous versions of this mod!     **
  **                                                                                        **
  ********************************************************************************************
  *************************************IMPORTANT!!********************************************

  Extract the included GameData folder into your KSP directory and merge the contents.
  The included Source directory does not need to be extracted.


Changelog:

Version 3.0:
[update] Verified compatibility with KSP v0.23
[added]  Indicator's size can now be scaled freely (from settings window)
[added]  Toolbar-Plugin miniature icon for toggling the settings window
[added]  Glyph Font rendering to support indicator scaling
[fixed]  Indicator will now display at full resolution regardless of KSP's Texture Settings


Version 2.2:
[update] Verified compatibility with KSP v0.22
[changed] Roll degrees now range from 0-359.9 (was -180 to +180 before)
[fixed] Stock lateral docking ports (Inline Clampotron) now orient correctly!
[fixed] Settings window toggle-buttons now much more visible


Version 2.1:
[fixed] A bug that caused the velocity vector to behave incorrectly in certain circumstances [thanks Mr Shifty].
[fixed] CVEL now measures velocity along the target port's normal vector (intended behavior), not true velocity.
[fixed] Negated CVEL value when passing into back-hemisphere (red CDI region). Closure is now always a positive value.
[change] Velocity Indicator now draws on top of of Alignment Vector.
[change] Reduced sensitivity of alignment indicator near center of the gauge slightly.
[change] Removed forward velocity component of the velocity vector. Now full deflection always indicates 3.5 m/s of lateral velocity.
[change] Added slight exponential scaling to velocity vector near center of gauge.
[change] Velocity Indicator will display as a 'retrograde' vector when your alignment is greater than 90 degrees off-axis, indicating that translation controls have a reversed impact on the movement of the visual indicator. Moving the indicator towards the green cross will still bring you towards centerline.


Version 2.0:
[added] Course Deviation Indicators (CDI)
[added] Translational Velocity vector
[added] Closure velocity and distance readouts
[added] settings menu
[added] Increased precision of alignment indicator with exponential scaling
[change] Enhanced precision of roll indicator
[change] Retouched all graphics

Version 1.0: First Release


--------------------License Information-----------------------------------



This Plugin is Licensed under the Creative Commons - Attribution License.

In otherwords, feel free to use this source code in your own plugins, but do provide
credit to myself ("NavyFish") as the author and include a link to this mod's SpacePort page. 

A big thank you to Trueborn, creator of the SteamGuages plugin 
(http://kerbalspaceport.com/steamgauges/) - his work was an inspiration for this
mod and its aesthetic, and he was kind enough to let me use his texture assets as a
starting point for my own. 



License for the Toolbar Plugin:
Copyright (c) 2013, Maik Schreiber
All rights reserved.

Redistribution and use in source and binary forms, with or without modification,
are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
