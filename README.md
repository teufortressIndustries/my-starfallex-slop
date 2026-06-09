# my-starfallex-slop
my starfallex gmod slop scripts

## [prop_disguise_extra.txt](https://github.com/teufortressIndustries/my-starfallex-slop/blob/main/prop_disguise_extra.txt)
An optimized, event-driven prop disguise script utilizing low-frequency validation timers instead of expensive processing loops. Features integrated invisible vehicle seating, standalone movement nodes, and a responsive client soundboard gateway.

### Controls
* **WASD**: Move / Roll / Fly around.
* **Space**: Jump (Omni & Vehicle modes) / Fly Upward (Glide mode).
* **Duck (Ctrl)**: Fly Downward (Glide mode).
* **Zoom Key (Z)**: Copy the model, skin, material, and color of the prop you are looking at.
* **ALT1 (Tap)**: Toggle completely between **Hologram (Client)** and **Physical (Server)** modes.
* **ALT2**: Freeze or unfreeze your physical prop physics body in place.
* **Sprint (Shift)**: Cycle handling styles: **Omni** (Classic ball rolling) -> **Vehicle** (Torque-based throttle & steering) -> **Glide** (Smooth noclip guidepoint tracking).
* **Walk (Alt)**: Detach from your prop to roam freely (leaves hologram/prop behind), or attach back to sync up with it.
* **Reload (R)**: Possess the custom unowned prop in your crosshair while detached.
* **Scoreboard (TAB)**: Play a random audio taunt from the script configuration array.

> ⚠️ **Note**: For ALT1 and ALT2 keys to register, you must bind them to standard execution keys first via your developer console.
> * *Example:* `bind . +alt1` and `bind / +alt2`

### Chat Commands
You can forcefully change your active model path directly via text chat:
* `!prop models/props_junk/watermelon01.mdl`

---

## [healing_station.txt](https://github.com/teufortressIndustries/my-starfallex-slop/blob/main/healing_station.txt)
A Medigun-style support script that locks onto teammates and dynamically spawns healing kits or armor batteries at their feet.

### Features
* **Target Locking**: Tap **Left Click (ATTACK)** while looking at a teammate within 300 units to lock onto them. Tap again to unlock or switch targets.
* **Smart Dispensing**: Automatically checks the target's status and prioritizes spawning health kits (`item_healthkit`) until they are maxed out, then switches to armor batteries (`item_battery`).
* **Audio Loops**: Plays dynamic charging sound effects while actively dispensing, with an error sound if the target is already full.
* **Custom HUD**: Displays an on-screen diagnostic window showing the target's name, current health, armor status, and lock state.
