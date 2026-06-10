# my-starfallex-slop
my starfallex gmod slop scripts

---

## [prop_disguise_extra.txt](https://github.com/teufortressIndustries/my-starfallex-slop/blob/main/prop_disguise_extra.txt)

Disguise yourself as any physical prop (ragdolls and some models not supported yet). Supports a hologram (client) mode for passive blending and a full physics (server) mode for active movement, with multiple handling styles.

### Controls

| Key | Action |
|-----|--------|
| `WASD` | Move / Roll / Fly around |
| `Space` | Jump (Omni & Vehicle modes) / Fly Upward (Glide mode) |
| `Ctrl` (Duck) | Fly Downward (Glide mode) |
| `Z` (Zoom) | Copy the model, skin, material, and color of the prop you are looking at |
| `ALT1` (Tap) | Toggle between Hologram (client) and Physical (server) modes |
| `ALT2` | Freeze or unfreeze your physical prop in place |
| `Shift` (Sprint) | Cycle handling styles: **Omni** → **Vehicle** → **Glide** |
| `Alt` (Walk) | Detach from your prop to roam freely, or reattach to sync back up |
| `R` (Reload) | Possess an unowned prop in your crosshair while detached |
| `TAB` (Scoreboard) | Play a random audio taunt from the configured soundboard |
| `Left Click` (Attack) | Toggle view-steering while in Vehicle mode |

> ⚠️ **Note:** For `ALT1` and `ALT2` to register, bind them to standard execution keys via the developer console first.
> ```
> bind . +alt1
> bind / +alt2
> ```

### Chat Commands

Change your active prop model directly via text chat:

```
!prop models/props_junk/watermelon01.mdl
```

### Handling Styles

- **Omni** — Classic ball-rolling physics. Move in any direction relative to your eye angle.
- **Vehicle** — Torque-based throttle and steering. Press Attack (Left Click) to steer the way you look.
- **Glide** — Smooth noclip-style flight using eye-angle tracking.

---

## [healing_station.txt](https://github.com/teufortressIndustries/my-starfallex-slop/blob/main/healing_station.txt)

A Medigun-style support script that locks onto teammates and dynamically spawns healing kits or armor batteries at their feet.

### Features

- **Target Locking** — Tap `Left Click` (ATTACK) while looking at a teammate within 300 units to lock onto them. Tap again to unlock or switch targets.
- **Smart Dispensing** — Automatically checks the target's status and prioritizes spawning health kits (`item_healthkit`) until they are maxed out, then switches to armor batteries (`item_battery`).
- **Audio Loops** — Plays dynamic charging sound effects while actively dispensing, with an error sound if the target is already full.
- **Custom HUD** — Displays an on-screen diagnostic window showing the target's name, current health, armor status, and lock state.

---

## [who_is_that.txt](https://github.com/teufortressIndustries/my-starfallex-slop/blob/main/who_is_that.txt)

A cheap knockoff G-Man sightings mod. Periodically spawns a silent, black G-Man hologram somewhere in the world around you. If you look directly at him, he disappears.

### Features

- **Random Sightings** — G-Man appears at a randomized interval between a configurable minimum and maximum delay.
- **Positional Bias** — Spawn location is biased toward behind and out of your field of view, with line-of-sight verification so he always has a clear path to you.
- **Spotted & Vanish** — Once your crosshair gets within the configured angle threshold, a short delay triggers and G-Man removes himself.
- **Distance-Scaled Vanish** — The further away G-Man spawns, the longer he lingers after being spotted before disappearing.
- **Ambient Sound** — Plays a directional wind-chime sound cue from G-Man's direction on spawn.
- **Server Reporting** — Sends a net message to the server logging which player spotted him and from how far away.
- **Whitelist Support** — Optional SteamID64 whitelist to restrict sightings to specific players only.

### Configuration (top of script)

| Variable | Default | Description |
|----------|---------|-------------|
| `SPAWN_DELAY_MIN` | `60` | Minimum seconds between sightings |
| `SPAWN_DELAY_MAX` | `1800` | Maximum seconds between sightings |
| `SPAWN_RADIUS` | `1000` | Max distance G-Man can spawn from you (units) |
| `SPAWN_BEHIND_BIAS` | `0.5` | How strongly spawns are biased behind you (`0` = anywhere, `1` = strictly behind) |
| `SPOT_ANGLE` | `65` | Degrees from crosshair center that counts as "noticing" him |
| `VANISH_DELAY` | `0.2` | Seconds before vanishing when spotted up close |
| `VANISH_DELAY_MAX` | `0.6` | Seconds before vanishing when spotted at max range |
| `WHITELIST_ON` | `false` | Enable/disable the SteamID whitelist |
