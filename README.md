# my-starfallex-slop
my starfallex gmod slop scripts

## [prop_disguise_extra.txt](https://github.com/teufortressIndustries/my-starfallex-slop/blob/main/prop_disguise_extra.txt)
An advanced prop disguise script featuring multiple handling styles, a visual history stack, dynamic physical attachments, and a soundboard.

### Controls
* **WASD**: Move / Roll / Fly around.
* **Space**: Jump (Omni & Vehicle modes) / Fly Upward (Glide mode).
* **Duck (Ctrl)**: Fly Downward (Glide mode).
* **Zoom Key (Z)**: Copy the model, skin, material, and color of the prop you are looking at.
* **ALT1**: Toggle between **Hologram** and **Physical** modes (Hold for 0.4 seconds). 
    * *Tap ALT1*: Undo / swap backward through your possessed prop history.
    * *Tap Duck + ALT1*: Redo / swap forward through your possessed prop history.
* **ALT2**: Freeze or unfreeze your physical prop in place.
* **Sprint (Shift)**: Cycle through handling styles: **Omni** (Classic ball rolling) -> **Vehicle** (Throttle & steering) -> **Glide** (Smooth noclip guidepoint tracking).
* **Walk (Alt)**: Detach from your prop to roam freely, or attach back to it.
* **Reload (R)**: Possess the prop in your crosshair while detached.
* **Scoreboard (TAB)**: Play a random audio taunt from the configured soundboard.

* **Note**: For ALT1 and ALT2 keys to work, you have to bind them first in console.
* Example: `bind / +alt2` < binds your slash key to ALT2

### Chat Commands
You can change your appearance directly via text chat:
* `!prop models/props_junk/watermelon01.mdl`

---

## [healing_station.txt](https://github.com/teufortressIndustries/my-starfallex-slop/blob/main/healing_station.txt)
A Medigun-style support script that locks onto teammates and dynamically spawns healing kits or armor batteries at their feet.

### Features
* **Target Locking**: Tap **Left Click (ATTACK)** while looking at a teammate within 300 units to lock onto them. Tap again to unlock or switch targets.
* **Smart Dispensing**: Automatically checks the target's status and prioritizes spawning health kits (`item_healthkit`) until they are maxed out, then switches to armor batteries (`item_battery`).
* **Audio Loops**: Plays dynamic charging sound effects while actively dispensing, with an error sound if the target is already full.
* **Custom HUD**: Displays an on-screen diagnostic window showing the target's name, current health, armor status, and lock state.
