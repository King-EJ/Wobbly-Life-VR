# Wobbly-Life-VR
VR Mod for Wobbly Life

WOBBLY LIFE - VR MOD  v0.1.8
==========================================================================
(tested with Quest 3 VDXR)

INSTALL
1. Copy everything in this zip into the game folder (next to Wobbly Life.exe).
   You get winhttp.dll, doorstop_config.ini and the BepInEx folder (BepInEx 5.4.23 + the VR mod).
3. Start SteamVR / Quest Link / Virtual Desktop first (it must be the OpenXR runtime).
4. Start the game. The first start takes a little longer (BepInEx sets itself up).
   If the headset stays black, add the launch option  -force-d3d11
5. Settings: BepInEx\config\wobblylife.vr.cfg (created on the first run, changes apply live),
   or the VR settings menu in the headset (Y + left stick click, hold 1.7 s).
   Play single player (the VR controllers drive local player 1).

NEW IN 0.1.8
* The weather drone (and other vehicles whose camera sits on a part of the vehicle) now count as flying:
  normal right stick and gyro flying work in them.

NEW IN 0.1.7
* Gyro flying: in flying vehicles tilt the right controller to steer ([General] GyroFlight, also in the
  VR settings menu): RightStick = the tilt is the right stick (planes), LeftStick = the tilt is the left
  stick (helicopters, UFOs, ships). How you hold the controller when you get in is the middle
  (both stick clicks re-centre). GyroAngle = tilt for full stick, GyroInvertY.

NEW IN 0.1.6
* Flying vehicles (helicopter, plane, UFO, hot-air balloon, flying car, space ship, drone...): the right
  stick is the normal gamepad right stick ([General] FlyingVehicleKeywords).
* [General] RightStickMode: Turn (default) or Game = the normal gamepad right stick everywhere.
* [General] WalkDirection: Head (default), LeftHand or RightHand = walk where that controller points.
  Both also in the VR settings menu.

NEW IN 0.1.5
* Driving / running: the view no longer lags behind and shakes. Your Wobbly's body and the car you sit
  in are drawn smoothly between physics steps, the head's wobble is smoothed relative to the car / your
  hips, and you turn with the car ([Camera] TurnWithVehicle).
* Emote wheel: stays open while you hold the left trigger (it blinked shut), and the right stick picks
  the emote while it is open.

NEW IN 0.1.4
* Fixed: anything shown on the big screen (map, emote wheel, VR settings) stayed there after it closed.
  The game's UI camera never cleared the VR screen picture; now it does.
* Right stick click (R3) switches first / third person. Hold the right stick click = gamepad Back.
* Hand HUD: the time was shown twice (it is part of the minimap) - now minimap + to-do list
  (the to-do list shows when the game shows it).

NEW IN 0.1.3
* Fixed: the main menu's picture stayed on the big screen in front of you during play. Menu screens
  now only show while the game itself shows them.

NEW IN 0.1.2
* Fixed: the screen in front of you was solid and blocked your view. The game's UI camera has a colour
  effect that filled the see-through screen picture; it is switched off for the VR screen.
* The game camera's own helper canvas is left alone (world icons are placed with it).
* Post-processing on the VR eyes: retried, and the log says why if it fails.

NEW IN 0.1.1
* The minimap, time / weather and to-do list float by your left hand while playing (and are left out
  of the big screen). In menus everything is on the big screen again. [UI] HandHud / HandHudSize /
  HandHudOffset, also in the VR settings menu.

HOW IT PLAYS
------------
- First person: you see from your Wobbly's head (your own head and hat are hidden). Your Wobbly faces
  where you look, walking goes where you look, the upper body leans where you look up / down.
- Your Wobbly's arms reach to where your real hands are. Hold a grip to grab what that hand touches,
  let go to drop it.
- Third person: you stand where the game's camera is. The view stays level, the right stick turns it.
- Switch first / third person: click the right stick (R3).
- Minimap, time and to-do list: by your left hand. Menus and the rest of the HUD: on a floating
  screen in front of you.
- Cutscenes: you stand where the game's camera is ([Camera] CutsceneView).

CONTROLS
--------
The VR controllers act as an Xbox controller, so the game's own gamepad layout decides what each
button does (the log lists it under "Game actions (Rewired) -> gamepad"). Change in [GamepadButtons].

  Left stick ............. walk (gamepad left stick)    Right stick ........ turn (snap)
  
  Left grip .............. LT (grab with the left arm)  Right grip ......... RT (grab with the right arm)
  
  A / B .................. A / B                        Y .................. Y
  
  X (tap) ................ X                            X (hold) ........... d-pad up
  
  Right trigger .......... RB                           Right stick down ... LB
  
  Left trigger ........... d-pad down                   Left stick click ... L3
  
  X + Y .................. Start (pause)                Right stick click (hold) ... Back / View
  
  Right stick click (tap). switch first / third person
  
  Both stick clicks ...... re-centre the view
  
  Y + left stick click (hold 1.7 s) ... VR settings menu
  
  In menus the right stick is the gamepad's right stick.
  ![Controller layout](https://github.com/King-EJ/Wobbly-Life-VR/blob/main/WL.jpg?raw=true)

Issues
------
When entering flying vehicles you might be turn wrong way

when you start 1st time may want to re-center L3+R3

sometimes you have to have a controller connected to start game

CREDITS & LICENCES
------------------
Uses Astien's OpenXR bridge (see BepInEx\plugins\WobVR\LICENSES). Free, non-commercial.
