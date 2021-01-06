# CP2077-keybinds

## CPNK 2077 Keybind Fixes

CyberPunk's ported control scheme locks down the F key as the game's action button. This fix rebinds CyberPunk's "use" key to "E".

Players can use this format to remap their inputs to whichever keys they want.  Clone or download the repo for the modified XML file in addition to a list of valid keynames.

## Where do I put this?

The included XML file is designed to overwrite __CyberPunk's inputUserMappings.xml file__ inside the Steam Library folder.

Standard Steam installs usually define the directory as:

```C:\Program Files (86x)\Steam\steamapps\common\CyberPunk 2077\r6\config```

A list of currently-bound keys can be found under ```%APPDATA%``` on Windows 10 installations for each user:

```%LOCALAPPDATA%\CD Projekt Red\Cyberpunk 2077\UserSettings.json```

### How do I make changes?

Control-H is your friend. Be sure to use quotes when changing ```"IK_Key"``` values to avoid unbinding  the function keys. See below.

******

## What keys can I rebind in CyberPunk?

Almost all of them. To avoid the ```None``` UI bug, try to be consistant and keep changes containted to the inputUserMappings.xml file, while removing and backing up both the original userInputMappings.xml the ```UserSettings.json``` found inside ```APPDATA```.

Most important thing item is to try not to leave anything unbound, as CP2077 doesn't seem to like that too much. For example, while you may never uses ```Sprint(toggle)```, bind it anyway away from your other keys.

 ___As a general rule, if a key is used for two or more different actions, replace them all with the same key.___

For example, the included .xml mappings have rebound the game's use key from *"F"* to *"E"*. On top of being the game's activation key, "F" was also used in 32 other contexual actions, all of which have been rebound individually to the "E" key.

## What did __YOU__ rebind?

All controls are now similar to Counter-Strike Global Offensive's usual bindings:
| `button id` | "IK_keyAlias" |
| --- | --- |
| R | Reload |
| MouseWheelDown | Jump |
| E | Use |
| Left Shift | Sprint (Hold) |
| Left Control | Crouch (Hold) |
| Mouse4 and Mouse5 | Added to the first and second weapon slots as additional bindings |

******

## What's the input format?

Keys are denoted by their ```button ID```. A full list of CP2077's ```button ID```'s (originally taken from the Witcher 3, as this was a common complaint there, too) is included in the zip.

General formatting is shown below with standard .xml indentations.

```xml
            <mapping name="CharacterPanel_Button" type="Button" >
            <button id="IK_C" />
         </mapping>
```

Where ```"IK_C"``` indicates the __C key__ is used to call the ___Character panel__. Players can add additional keys that perform the same function by adding additional ```button ID```s as shown below.

```xml
            <mapping name="Inventory_Button" type="Button">
            <button id="IK_I" />
            <button id="IK_P" />
        </mapping>
```

Mouse keys follow the standard pattern.

|`button id`|"IK_MouseAlias"|
| --- | --- |
|`button id`|"IK_Mouse4"|
|`button id`|"IK_MouseWheelUp"|
|`button id`|"IK_MouseWheelDown"|
|`button id`|"IK_Mouse5"|

#### But I'm left-handed

I'm sorry. I've made a left-handed file using the traditional left-handed ESDF movement keys, "T" as reload, and "R" as the the use key. Feel free to customize to your liking.

## Contributing

Pull requests with custom bindings are welcome as long as they include a .txt of ____which actions were remapped to which key___ as seen above.
