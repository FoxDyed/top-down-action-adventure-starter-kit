# Twin Stick Drop In

This folder contains **copies** of the twin-stick controller, controller overlay menu, interaction prompt, and arrow projectile dependencies.

## How to install into another Godot project

1. Copy the contents of this folder into your target project's root (`res://`) while preserving paths.
2. Add/verify these input actions in `Project Settings -> Input Map`:
   - `p1_move_left`, `p1_move_right`, `p1_move_up`, `p1_move_down`
   - `p1_aim_left`, `p1_aim_right`, `p1_aim_up`, `p1_aim_down`
   - `p1_aim`, `p1_jump`, `p1_pause`, `p1_camera_RR`, `p1_camera_RL`, `p1_interact`
3. Instantiate `res://ui/ControllerMenu.tscn` in your main scene if you want runtime controller scheme switching.
4. Use `res://characters/player/PlayerEntity.tscn` for the included twin-stick-ready player.

## Drop-in tweaks already applied in these copies

- Debug dependency removed (`DebugStats` calls removed).
- Controller menu reduced to 2 options:
  - Two Stick Controls
  - Two Stick Auto-Shoot Controls
- `GameDataStore` range/default adjusted for 2 controller options.
- `PlayerEntity` copy no longer depends on one-stick or keyboard/mouse controller scenes.
- `PlayerEntity` copy now safely handles missing optional autoloads (`Dialogic`, `GameManager`).

## Binary assets

Binary files are intentionally not duplicated in this bundle. See `BINARY_FILES_TO_COPY.txt` for the required icon file paths to copy from the source project.
