# Puddipacks

<p align="center"><img src="https://raw.githubusercontent.com/PuddiDuddi/Puddipacks/main/assets/icon_full.png" width="400" alt="Puddipacks"></p>

Eight biome-tiered backpacks for Smoothbrain's Backpacks mod. One backpack at a time. Small packs. A new tier lightens the load. An upgrade adds slots.

Requires [Smoothbrain-Backpacks](https://valheim.hexium.gg/mods/Smoothbrain/Backpacks) 1.3.10 or newer. Recommended: [AzuExtendedPlayerInventory](https://valheim.hexium.gg/mods/Azumatt/AzuExtendedPlayerInventory) for a dedicated backpack slot.

## Design

- **One pack per biome.** Eight tiers from Meadows to the Deep North.
- **Tier gives weight reduction.** Upgrade gives slots. Each tier has 2 upgrades (3 stars). Each upgrade adds one row or one column.
- **Each tier consumes the previous pack.** The base size of a new tier is the 2-star size of the previous tier. A fresh pack is a small step back in slots and a step forward in weight.
- **One pack in the inventory.** `unique: global`. No stacking of packs.
- **Slot ceiling is 35.** The vanilla Explorer's Backpack ceiling is 28.
- **Tier recipes are the main cost.** Upgrades cost about 30% and 45% of the tier recipe. Costs are per level, not cumulative.
- **Every recipe has at most 4 ingredients.** This is the number the crafting window shows.
- **Upgrades need Protection Idols.** Two idols for 2 stars, three for 3 stars. No idol on the craft itself. The idol tier matches the biome of the pack. Idols are loot from chests and cannot be crafted.
- **Teleport is on by default.** Every pack carries its contents through portals, ore included. See "Turn off teleport" below to change this.

## Tiers

| Tier | Biome | Name | Station | 1 star | 2 star | 3 star | Weight of contents | Teleport |
|---|---|---|---|---|---|---|---|---|
| 1 | Meadows | Scrap Satchel | Workbench 1 | 4x2 (8) | 5x2 (10) | 6x2 (12) | 100% | yes |
| 2 | Black Forest | Forest Knapsack | Workbench 3 | 5x2 (10) | 6x2 (12) | 5x3 (15) | 93% | yes |
| 3 | Swamp | Bog Pack | Forge 2 | 6x2 (12) | 5x3 (15) | 6x3 (18) | 86% | yes |
| 4 | Mountain | Frostbound Pack | Forge 3 | 5x3 (15) | 6x3 (18) | 7x3 (21) | 79% | yes |
| 5 | Plains | Plainsrunner Pack | Forge 4 | 6x3 (18) | 7x3 (21) | 6x4 (24) | 71% | yes |
| 6 | Mistlands | Eitrweave Pack | Black Forge 1 | 7x3 (21) | 6x4 (24) | 7x4 (28) | 64% | yes |
| 7 | Ashlands | Cinder Pack | Black Forge 3 | 6x4 (24) | 7x4 (28) | 8x4 (32) | 57% | yes |
| 8 | Deep North | Northwind Pack | Black Forge 4 | 7x4 (28) | 8x4 (32) | 7x5 (35) | 50% | yes |

## Recipes

| Tier | Tier recipe | 2 star | 3 star |
|---|---|---|---|
| 1 | Leather Scraps 40, Deer Hide 16 | Leather Scraps 12, Deer Hide 5, Wooden Protection Idol 2 | Leather Scraps 18, Deer Hide 7, Wooden Protection Idol 3 |
| 2 | Troll Hide 20, Bronze Nails 40, Resin 40, Scrap Satchel | Troll Hide 6, Bronze Nails 12, Bronze Protection Idol 2 | Troll Hide 9, Bronze Nails 18, Resin 10, Bronze Protection Idol 3 |
| 3 | Iron 32, Ancient Bark 60, Guck 20, Forest Knapsack | Iron 10, Ancient Bark 18, Guck 6, Iron Protection Idol 2 | Iron 14, Ancient Bark 27, Guck 9, Iron Protection Idol 3 |
| 4 | Silver 32, Wolf Pelt 20, Wolf Hair Bundle 20, Bog Pack | Silver 10, Wolf Pelt 6, Silver Protection Idol 2 | Silver 14, Wolf Pelt 9, Wolf Hair Bundle 6, Silver Protection Idol 3 |
| 5 | Black Metal 32, Lox Pelt 20, Linen Thread 60, Frostbound Pack | Black Metal 10, Linen Thread 18, Black Metal Protection Idol 2 | Black Metal 14, Lox Pelt 9, Linen Thread 27, Black Metal Protection Idol 3 |
| 6 | Eitr 40, Scale Hide 20, Carapace 40, Plainsrunner Pack | Eitr 12, Carapace 12, Black Marble Protection Idol 2 | Eitr 18, Scale Hide 9, Carapace 18, Black Marble Protection Idol 3 |
| 7 | Flametal 32, Asksvin Hide 20, Charred Bone 40, Eitrweave Pack | Flametal 10, Charred Bone 12, Flametal Protection Idol 2 | Flametal 14, Asksvin Hide 9, Morgen Sinew 6, Flametal Protection Idol 3 |
| 8 | Bloodgold 32, Moose Hide 20, Timberwood 40, Cinder Pack | Bloodgold 10, Timberwood 12, Bloodgold Protection Idol 2 | Bloodgold 14, Moose Hide 9, Nornathread 5, Bloodgold Protection Idol 3 |

## Looks

Each tier shows more parts of the backpack model and has its own accent color.

| Tier | Accent | Parts |
|---|---|---|
| Scrap Satchel | tan hide | body, flap |
| Forest Knapsack | pine green | + front pouch |
| Bog Pack | guck olive | + side pouch, knife |
| Frostbound Pack | frost blue | + bedroll, straps |
| Plainsrunner Pack | wheat gold | + pot, tool straps |
| Eitrweave Pack | eitr blue | + metal clips, ring |
| Cinder Pack | ember orange | all parts |
| Northwind Pack | bloodgold crimson, gold metal | all parts |

## Turn off teleport

All packs allow teleport by default. This means you can carry ore and metal through a portal inside the pack. To block this, edit one word per pack in a text file. No tools are needed.

1. Open your mod manager (Hexium Mod Manager or r2modman). Select your Valheim profile.
2. Go to **Config editor** in the left menu. Find `BackpacksPuddipacks` in the list and open it. If you do not use a mod manager, open the file `BepInEx/config/BackpacksPuddipacks.yml` in Notepad.
3. Find the line `teleport: true`. There is one line for every pack, eight in total.
4. Change `true` to `false` on the packs that must not teleport. Keep the two spaces at the start of the line. Do not change anything else.
5. Save the file. Restart the game.

Example. This blocks ore teleport on the Bog Pack only:

```yaml
"Bog Pack":
  ...
  weight factor: 0.84
  teleport: false
```

On a dedicated server, edit the file in the server config folder. The server sends the setting to all players.

A safe middle option: set `teleport: false` on tiers 1 to 6 and keep `true` on the Cinder Pack. Then ore teleport unlocks in the Ashlands, at the same time as the vanilla stone portal.

## Installation

1. Install with a mod manager, or copy the `config` folder into `BepInEx/config`.
2. The included `org.bepinex.plugins.backpacks.cfg` sets `Use External YAML = On` and disables the vanilla Explorer's Backpack recipe. If you keep your own cfg, set these two values yourself.
3. On a server, the YAML file in the server config folder is enough. Clients do not need the file.

## Notes

- The file name must start with `Backpacks` and end with `.yml`. The plugin loads every file that matches `Backpacks*.yml`.
- Backpacks in Backpacks is set to `NotAllowed`.
- Existing backpacks keep their size until the next upgrade. New sizes apply to new packs.

## Credits

- Smoothbrain for the Backpacks mod, CookieMilk for the backpack assets.
- Thordomr and Valkerion for the example packs that shaped the balance.
