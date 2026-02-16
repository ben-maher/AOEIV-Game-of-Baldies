# AOEIV – Game of Baldies

A small **Age of Empires IV Content Editor** mod (“tuning pack”) made for our group.

## What this mod changes

### 1) Higher population cap
- Increases the population cap to **1000**.

### 2) Richer resource nodes (more resources per deposit)
Increases the **total resources available per node** by modifying the `initial_amount` in `resource_deposit_ext` for:
- Gold deposits (large + small)
- Stone deposits (large + small)

This changes the *amount in the ground*, not gather rate.

### 3) Wall HP adjustment
- Sets **Stone Wall segment** hitpoints to **6000** via:
  - `assets/attrib/instances/ebps/races/core/buildings/building_defense_wall.xml`

Note: Walls are defined in `races/core` in this project, so this change should apply game-wide unless a specific civilization overrides wall EBPS elsewhere.

## Files of interest

- Mod package: `Game of Baldies.aoe4mod`
- Packed archive: `archives/Game_of_Baldies.sga`
- Editable mod assets: `assets/`

### Resource deposits
- `assets/attrib/instances/ebps/gameplay/resources/gold/resource_gold_deposit.xml`
- `assets/attrib/instances/ebps/gameplay/resources/gold/resource_gold_deposit_small.xml`
- `assets/attrib/instances/ebps/gameplay/resources/stone/resource_stone_deposit.xml`
- `assets/attrib/instances/ebps/gameplay/resources/stone/resource_stone_deposit_small.xml`

### Defensive structures
- `assets/attrib/instances/ebps/races/core/buildings/building_defense_wall.xml`
- `assets/attrib/instances/ebps/races/core/buildings/building_defense_keep.xml`

## Editing tips
- In the Content Editor, make sure you are browsing **base game assets**, then **copy/override** into the mod.
- For resource nodes, the relevant field is typically:
  - `resource_deposit_ext.initial_amount`
- For HP, the relevant field is typically:
  - `health_ext.hitpoints`
