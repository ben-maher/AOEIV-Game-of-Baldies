# AOEIV – Game of Baldies

![Game of Baldies mod logo](./mod.png)

A small **Age of Empires IV Content Editor** mod (“tuning pack”) made for our group.

## What this mod changes

### 1) Higher population cap
- Increases the population cap to **1000**.

### 2) Richer resource nodes (more resources per deposit)
This mod increases the **total resources available per node** (amount in the ground, not gather rate):
- **Gold**: **40,000** (small) / **80,000** (large)
- **Stone**: **40,000** (small) / **80,000** (large)

### 3) Trees have more wood
- **Trees**: **150 → 1500** per tree

### 4) Defensive structures are tougher
- **Stone Wall segments**: **3000 → 9000** HP
- **Stone Wall gates**: **3000 → 9000** HP
- **Outposts**: **750 → 7500** HP
- **Keeps**: **4000 → 15000** HP

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
- Walls / gates / bastions / outposts / keeps live under:
  - `assets/attrib/instances/ebps/races/**/buildings/**`
- Core references (not necessarily authoritative if per-race overrides exist):
  - `assets/attrib/instances/ebps/races/core/buildings/`

## Editing tips
- In the Content Editor, make sure you are browsing **base game assets**, then **copy/override** into the mod.
- For resource nodes, the relevant field is typically:
  - `resource_deposit_ext.initial_amount`
- For HP, the relevant field is typically:
  - `health_ext.hitpoints`
