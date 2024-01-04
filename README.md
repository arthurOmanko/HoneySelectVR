# HoneySelect VRmod with LRE & IBL

This mod is for integrating existing VirtualReality HoneySelect mod (VRmod) with Linear Rendering Experiment (LRE) and Image Based Lighting (IBL),
and adding some improvements. All post-processing effects (from UnityStandardAssets), functions of Camera lens, Skyboxes(Cubemaps) and Lighting functions
have been able to be used on Honey Select VR environment.
The main way to use this mod have already been referred on the site of existing each mod.
If User wants to know about each mod in detail, please see them.

- VRmod
https://github.com/Eusth/HoneySelectVR
- LRE & IBL
https://joan6694.bitbucket.io/
- IPA
https://github.com/Eusth/IPA
- About IBL
https://www.theschoolofsin.com/ibl-and-image-quality
- About LRE
https://docs.unity3d.com/540/Documentation/Manual/LinearLighting.html
- LRE&IBL Starting Guide
https://www.patreon.com/posts/meta-body-skin-26688397  
  
Thanks very much, these autors!

## [Installation]
1. Extract the zip file into User's HoneySelect directory.
2. Run (HoneySelect|StudioNEO)_(64|32)_for_VR_with_IBL
3. Enjoy super high quality on VR!

**Caution!** 
- This mod might rewrite some existing files and cause some bugs depending on User's environment.
  Please back up Game root folder before installing necessarily.
- This mod has no internet connections at all. If User encounters any Firewall problem, it would be by original Game. All origianl codes before changing are from authors cited above and the provider has added no codes about outgoing connections. However if you see documents on web from clicking on IBL GUI, the limitation shall not be applied to.
- This mod will often have heavy loads on memory especially, so User might get freezed or encounter PC crashes on VR execution. 
  In the case, User can decrease the number of post-processing effects or also have no effects (ApplyShaders = false).
  Please be careful to avoid any probelm caused by the case.
- Chara texture will get weird on Title, (enabling/disabling) self shadow, switching (seated/standing) mode, applying shader (as long as known as of now).
  The provider doesnt know about this reason very sorry. If User encounters this problem, initialize scene or chara.
  Until quitting Application , it will not happen twice. 
- Whether or not User has already installed noraml IBL or LRE, this mod works only on VR execution(command option = "--vr") not depending on it. Normal IBL&LRE are separeted from IBL&LRE of this mod during Application execution, so both dont influence with each other.   
- ${***_(64|32)_Data}\Managed\IllusionInjector.dll in this mod controlls this mod's LRE&IBL on VR. If User changes this DLL, on VR execution User might encounter any bugs. Use the DLL and this mod's LRE&IBL together. 
- User had not better display any other windows except for this Game window on PC Screen. If cursor on other windows, controllers might not get reactive. Cursor-confined function on Game window is a little irregular yet.
- GGmod (clothes with highheel) DLL might sometimes influence IK/FK of chara with highheel attached by GGmod, so during VR, lookup, necklock or IK/FK of chara might sometimes get weird. Then once please put it on/off clothes (especially highheel attached by GGmod). The weird situation of chara would correct.   
- If you using other VR tools as of now except for here, your game might work unproperly. Then reconsider removing other VR tools (${GameFolder}/Plugins/**.dll files etc.). For example, might have to remove *.dll as below,  
     + VRGIN_NEO.dll  
     + StudioNEOVR.dll  
     + Vrboop.dll  
     + GripMoveForHSVRStudio.dll  
     + GripMoveForHSVR.dll  

## [Requirements]
- Game updated with the last patch and DLC installed
- Installed and set up SteamVR
- HSExtSave plugin  
https://joan6694.bitbucket.io/


## [Mod Settings]
- VRmod:  
  -- ${GameFolder}\vr_settings_for_IBL.xml   --- each VR setting  
  -- ${GameFolder}\vr_for_IBL.log   --- Log on VR execution
- IBL:      
  -- ${GameFolder}\Plugins\HSIBL\Presets_for_VR   --- IBL Preset for VR  
  -- ${GameFolder}\abdata\plastic\cubemaps   --- IBL cubemaps (common with normal IBL if there is)  
  -- ${GameFolder}\UserData\modprefs.ini   --- IBL setting on [HSIBLforVR] item. For initial GUI size etc.
- LRE:      
  -- ${GameFolder}\UserData\GraphicSetting\Config_for_VR.xml   --- LRE setting for VR. Shadow or imageEffect settings etc. Dir:[Common, Shadow, ImageEffect, Style, AntiAliasing].


## Modes & Controls

HoneySelectVR comes in two *modes*:

| Mode        | Description         |
| ----------- | ------------------- |
| Seated      | This mode lets you play the game with a mouse, keyboard, or gamepad.<br />The controls are essentially the same as in the main game. The screen is presented on a big monitor in front of you. |
| Standing    | *Default mode.* As soon as tracked controllers are registered by the game, it switches into *standing mode*, also called *room scale mode*. In this mode, you can freely move around and use your Vive or Touch controllers to stuff. |

### Common Mode
On both Seated and Standing Mode, same shortcuts would be used.

#### Keyboard Shortcuts

Keys &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;          | Effect
:------------:  | ------
<kbd>F5</kbd> | GUI of IBL on/off. [default shortcut. If want to change, please change the shortcut parameter on [HSIBLforVR] item in ${GameFolder}\UserData\modprefs.ini.]
<kbd>Ctrl</kbd>+<kbd>C</kbd>, <kbd>Ctrl</kbd>+<kbd>C</kbd> | Change to Standing/Seated mode.
<kbd>Ctrl</kbd>+<kbd>C</kbd>, <kbd>Ctrl</kbd>+<kbd>V</kbd> | Enable (very experimental) third person camera. [Was used for this video](https://www.youtube.com/watch?v=0klN6gd1ybM). If get on, this makes a Camera Box at (0, 0, 0) which User can grab and put where User hope. The display of the camera gets displayed on User's PC monitor. Very interesting!
<kbd>Alt</kbd>+<kbd>S</kbd> | Save settings (IPD, screen position, etc.). Write the last saved state on ${GameFolder}\vr_settings_for_IBL.xml.
<kbd>Alt</kbd>+<kbd>L</kbd> | Load settings (from last saved state).
<kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>L</kbd> | Reset settings to the initial state (all default values of ${GameFolder}\vr_settings_for_IBL.xml).
<kbd>Ctrl</kbd>+<kbd>F5</kbd> | Apply shaders (Post-processing Effects get applied (such as SSAO, ToneMapping, Color Grading etc.))
<kbd>Alt</kbd>+<kbd>NumPad +</kbd> <br /> <kbd>Alt</kbd>+<kbd>NumPad –</kbd> | Increase / decrease player scale
<kbd>Ctrl</kbd>+<kbd>F12</kbd> | 360 Panorama Capture on VR. (=> ${GameFolder}\UserData\cap)
<kbd>Ctrl</kbd>+<kbd>Q</kbd> | Toggle fixing of Field of View for Camera (on IBL lens item). If want full functions of lens on IBL, unfix by toggle. 
<kbd>Shift</kbd>+<kbd>Ctrl</kbd>+<kbd>C</kbd> | Most GUI Default textures get changed from transparent into opaque to improve UI/UX usability. Do this when IBL GUI on.
<kbd>Shift</kbd>+<kbd>UpArrow</kbd> <br /> <kbd>Shift</kbd>+<kbd>DownArrow</kbd> | Increse / decrease the GUI resolution.

### Seated Mode

As stated earlier, the controls are basically the same as in the main game with the exception of a few VR-related shortcuts. You are presented with a screen in front of your that replaces your monitor and can be configured via the settings or via shortcuts (see below).

#### Keyboard Shortcuts

Keys &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;      | Effect
:----:     | ------
<kbd>F4</kbd> | Switch GUI projection mode (Flat, Curved, Spherical).
<kbd>F7</kbd> | Toggle camera rotation lock (only around horizontal axis) (disabled by default). This prevents the camera to *tilt* because such movements are known to cause cyber sickness.
<kbd>F12</kbd> | Recenter
<kbd>NumPad +</kbd> <br /> <kbd>NumPad –</kbd> | Move GUI up / down.
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>NumPad +</kbd> <br /> <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>NumPad –</kbd> | Rotate GUI left / right
<kbd>Ctrl</kbd>+<kbd>NumPad +</kbd> <br /> <kbd>Ctrl</kbd>+<kbd>NumPad –</kbd> | Increase / decrease GUI size.
<kbd>Shift</kbd>+<kbd>NumPad +</kbd> <br /> <kbd>Shift</kbd>+<kbd>NumPad –</kbd> | Increase / decrease GUI distance
<kbd>Ctrl</kbd>+<kbd>X</kbd> | Impersonate a chara Approximately along User's line of sight (not matching in regar with height)
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> | Impersonate a chara Exactly along User's line of sight (matching all x, y, z position)

### Standing Mode

The *standing mode* is where things start to get interesting. This mode is pretty much disconnected from the usual game in that it comes with its very own controls -- although you can still use your mouse and your keyboard.

#### Keyboard Shortcuts

Keys      | Effect
----      | ------


## Tools

These tools are mainly meant to be used in *standing mode* but some of them are also available in *seated mode*. By default, your left hand will start with the *menu tool* and your right hand will start with the *warp tool*. In order to change them on either hand, press the *menu button* on your Vive controller. [See here an overview of buttons](https://forums.unrealengine.com/attachment.php?attachmentid=87367&d=1460020388).

**You can get in-game help any time by holding the menu button!**

### Menu Tool (seated / standing)
![menu_tool](https://user-images.githubusercontent.com/68005887/89115910-d62c5a00-d4c8-11ea-8fe4-e96d8b8173ba.png)  

With the *menu tool* you can interact with the user interface of the game. There are, in fact, two ways you can control the mouse: a two-handed way that makes use of a laser pointer, and a one-handed way that lets you use your trackpad like a ... touchpad!

#### Laser pointer
![laser_pointer](https://user-images.githubusercontent.com/68005887/89115930-0f64ca00-d4c9-11ea-84d9-7c39582e845a.jpg)  

To use the laser pointer, simply point the *other controller* at the menu screen. A laser pointer will appear and you can easily interact with the UI. To make a click, press the trigger button.

#### Trackpad

To use the trackpad, slide with your thumb over the trackpad and the mouse cursor will move accordingly. To make a click, press the trackpad.

#### Attaching, Detaching and Resizing the Menu
![scale](https://user-images.githubusercontent.com/68005887/89115937-20154000-d4c9-11ea-96f9-975ffb9da280.jpg)  


It's possible to detach and resize the menu you're holding at any point in the game.

Simply press the grip button to "let go" of the menu screen -- the screen will then stay put where you left it. You can even use other tools and still interact with the screen using the *laser pointer* mechanism.

Furthermore, it's possible to *resize* the screen. In order to do that, point both your controllers at a screen, press the trigger button, and move the controllers apart. It's also possible to move the screen around like this.

Lastly, to take control of the screen again, press the grip button once more.

#### UI/UX abstract on Menu
Tag      |  Move   | 
----     | ------  | 
only one hand needed
<kbd>trackpad</kbd>+<kbd>move</kbd> | move mouse cursor (when laser invisible)
<kbd>trackpad</kbd>+<kbd>push</kbd> | click mouse cursor
<kbd>trigger</kbd> | click mouse cursor
<kbd>menu</kbd> | display menu
<kbd>grip</kbd> | put GUI or grab put GUI
both hands needed
<kbd>trigger</kbd>+<kbd>trigger</kbd> | resize put GUI.

### Warp Tool (standing)
![warp_tool](https://user-images.githubusercontent.com/68005887/89115946-358a6a00-d4c9-11ea-87b0-ba7e6088070a.png)  

The *warp tool* is only available in room scale mode and allows you to jump around in the scene.

#### Warping

In order to warp, touch the trackpad, choose your position and press. While touching the trackpad you are able to see:

1. Where you will warp to
2. Your play area
3. A HMD that further shows where your head will be

You can also *rotate* your play area while touching the trackpad by drawing circles with your thumb.

![warp](https://user-images.githubusercontent.com/68005887/89115953-49ce6700-d4c9-11ea-811b-39a77fc49fe3.jpg)  


#### UI/UX abstract on Warp
By improved UI/UX and leap functions, User can easily move where User want.  
Tag      |  Move   | 
----     | ------  | 
only one hand needed
<kbd>menu</kbd>+<kbd>trigger</kbd> | warp in front of chara along User's line of sight
<kbd>tigger</kbd>+<kbd>1 second</kbd> | impersonate chara along User's line of sight
<kbd>trackpad</kbd> | warp where User wants (position, rotation)
<kbd>grip</kbd>+<kbd>move</kbd> | move and rotate where User wants
<kbd>trigger</kbd>+<kbd>grip</kbd>+<kbd>menu</kbd>+<kbd>0.5s</kbd> | All axes rotation on/off when moving
<kbd>trigger</kbd>+<kbd>triple clicks</kbd> | move with seen chara during animation
<kbd>trigger</kbd>+<kbd>double clicks</kbd> | cancell moving with chara
<kbd>menu</kbd>+<kbd>holding</kbd> | display menu on warp mode
both hands needed
<kbd>Menu</kbd>+<kbd>UpArrow</kbd>+<kbd>trigger</kbd> <br /> <kbd>Menu</kbd>+<kbd>DownArrow</kbd>+<kbd>trigger</kbd> | decrease/increase the distance up to chara on leaping.

### Play Tool (Standing / Seated)
![play_tool](https://user-images.githubusercontent.com/68005887/89115805-5ce03780-d4c7-11ea-811d-c2b4ceb54b09.png)  
The play tool is used to interact with the scene.  
#### UI/UX abstract on PlayTool
Tag      |  Move   | 
----     | ------  | 
only one hand needed
<kbd>trigger</kbd>+<kbd>DoubleClicks</kbd> | FinishIn or Drink
<kbd>grip</kbd>+<kbd>DoubleClicks</kbd> | Both Gone or Vomit
<kbd>trackpad</kbd>+<kbd>DoubleClicks</kbd> | FinishOut
<kbd>trackpad</kbd>+<kbd>trigger</kbd> | I'm coming!
<kbd>trackpad</kbd>+<kbd>slide along y-axis</kbd> | Change piston speed, Go In/Out, etc.
<kbd>menu</kbd> | display each fuction

## VR Settings & Tweaks

Settings can be changed in the file *vr_settings_for_IBL.xml*, which is generated the first time you start the game. Use `RenderScale` to tweak the resolution, **not** the internal game resolution dialog, as that one will currently only change the resolution of the GUI.

Tag      | Default | Effect | Mode
----     | ------  | ------ | ----
`<Distance>` | 1.2 | Sets the distance between the VRcamera and the GUI. [meter] | Seated
`<OffsetY>` | -0.2 | Sets the vertical offset of the GUI. [meter] | Seated
`<Angle>` | 70 | Sets the width of the arc the GUI takes up, Range:[50..360].  | Seated
`<Rotation>` | 0 | On default, degrees of the GUI get rotated around the horizontal axis (y-axis), Range:[0..360]. | Seated
`<PitchLock>` | false | Whether or not rotating only around the horizontal axis (y-axis) is allowed (all axes rotation ok = false). | Seated
`<Projection>` | Flat | The curviness of the monitor in seated mode. Select (Flat, Curved, Spherical). | Seated
`<IPDScale>` | 0.8 | Sets the scale of the camera. The higher, the more gigantic the player is. | Seated / Standing
`<RenderScale>` | 1 | Sets the render scale of the renderer. Increase for better quality but less performance, decrease for more performance but poor quality, Range:[0..2 or more if possible]. | Seated / Standing
`<MirrorScreen>` | false | Sets whether or not the view should be mirrored on User's PC monitor. When this true and on StudioNeo, all ok. When this true and on mainGame/CharaMake, at first, change Seated/Standing mode to activate by keyboard shortcut [default: Ctrl-C, Ctrl-C], otherwise FPS would decrease drastically (researching the reason currently...). | Seated / Standing
`<SpeechRecognition>` | false | Whether or not speech recognition is enabled. Refer to the manual for details. | Seated / Standing
`<Locale>` | en-US | Locale to use for speech recognition. Make sure that you have installed the corresponding language pack. A dictionary file will automatically be generated at `UserData/dictionaries`. | Seated / Standing
`<Rumble>` | true | Sets whether or not rumble is activated. | Seated / Standing
`<Leap>` | true | Whether or not Leap Motion support is activated. | Standing 
`<DefaultDistanceOfLeap>` | 0.5 | Default distance up to chara on leaping. [meter] | Standing
`<HeightCoincidenceOnLeap>` | false | On leaping up to a chara, whether the height of VRCamera matches with chara's. | Standing
`<CursorMoveMultiplier>` | 1 | To change cursor moving speed multiplier (especially influencing the speed of object moving by MoveController). | Seated / Standing
`<ChangeAllDefaultGUITexture>` | true | This is whether changing normal transparent GUIs into opaque GUIs because of being difficult to see normal transparent GUI on VR environment. [opaque = true] | Seated / Standing
`<GrabRotationImmediateMode>` | true | Determines the rotation mode. If enabled, pulling the trigger while grabbing will immediately rotate you. When disabled, doing the same thing will let you 'drag' the view. [deprecated] | Standing
`<RotationMultiplier>` | 2.5 | How quickly the view should rotate when doing so with the controllers. [deprecated] | Standing
`<ApplyShaders>` | true | Sets whether or not post-processing shaders should automatically be applied to the camera. If you want high FPS not Post-Processing Effects, set false. | Seated / Standing
`<NearClip>` | 0.01 | Within this distance, seen chara gets transparent. If too small, Camera might shake sometimes. [meter] | Seated / Standing
`<SpeedOfMouseWheel>` | 3 | Speed of mouse wheel on PlayTool. This would influence the speed of piston changing etc. | Seated / Standing

## Especially HSIBLforVR, VRCamera and Lighting Settings
Settings can be changed in the file *${GameFolder}\UserData\modprefs.ini*,

Tag      | Default | Effect
----     | ------  | ------
`<effectTypeFilter>` | 3 | default effect type on IBLGUI. [1: 4K, 2: LRE, 3: Both]
`<defaultCharaMakerCubemap>` | blank | default cubemap on starting CharaMaker
`<shortcut>` | F5 | IBL GUI on/off key
`<Window.x, y, width, height>` | --- | default position, size of IBLGUI
`<DefaultFrontLightDefaultRotation.x, y, z>` | (0, 6, 0) | default rotation of the default directionalFrontLight (+ directionalFrontMapLight) attached at VRcamera. For example, when (45, 90, 0), lights come from the 10 o'clock direction. each Range[0..360]
`<DefaultBackLightDefaultRotation.x, y, z>` | (0, 200, 0) | default rotation of the default directionalBackLight attached at VRcamera. For example, when (45, 270, 0), light comes from the 2 o'clock direction. each Range[0..360]
`<AllRotationCameraSave>` | 0 | Whether all axes rotation data of VRCamera saved or not (only horizontal axis) when saving camera data on StudioNEO. [0 = only horizontal axis, 1 = all axes] 
`<CameraFrontLightRotationToDefaultOnSceneLoad>` | 0 | On loading a scene on StudioNEO, whether making the rotation of default directional front lights attached at VRCamera set at default rotation or not (using saved lights rotation data). If you always prefer default front lights rotation, use this option. [0 = using saved data, 1 = set at default rotation]
