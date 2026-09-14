# Puddipacks

Seven biome-tiered backpacks for Smoothbrain's Backpacks mod. One backpack at a time. Small packs. A new tier lightens the load. An upgrade adds slots.

Requires [Smoothbrain-Backpacks](https://thunderstore.io/c/valheim/p/Smoothbrain/Backpacks/) 1.3.9 or newer. Recommended: [AzuExtendedPlayerInventory](https://thunderstore.io/c/valheim/p/Azumatt/AzuExtendedPlayerInventory/) for a dedicated backpack slot.

## Design

- **One pack per biome.** Seven tiers from Meadows to Ashlands.
- **Tier gives weight reduction.** Upgrade gives slots. Each tier has 2 upgrades (3 stars). Each upgrade adds one row or one column.
- **Each tier consumes the previous pack.** The base size of a new tier is the 2-star size of the previous tier. A fresh pack is a small step back in slots and a step forward in weight.
- **One pack in the inventory.** `unique: global`. No stacking of packs.
- **Slot ceiling is 32.** The vanilla Explorer's Backpack ceiling is 28.
- **Tier recipes are the main cost.** Upgrades cost about 60% and 90% of the tier recipe. Costs are per level, not cumulative.
- **Ore teleport only on the Ashlands tier.**

## Tiers

| Tier | Biome | Name | Station | 1 star | 2 star | 3 star | Weight of contents | Teleport |
|---|---|---|---|---|---|---|---|---|
| 1 | Meadows | Scrap Satchel | Workbench 1 | 4x2 (8) | 5x2 (10) | 6x2 (12) | 100% | no |
| 2 | Black Forest | Forest Knapsack | Workbench 3 | 5x2 (10) | 6x2 (12) | 5x3 (15) | 92% | no |
| 3 | Swamp | Bog Pack | Forge 2 | 6x2 (12) | 5x3 (15) | 6x3 (18) | 84% | no |
| 4 | Mountain | Frostbound Pack | Forge 3 | 5x3 (15) | 6x3 (18) | 7x3 (21) | 75% | no |
| 5 | Plains | Plainsrunner Pack | Forge 4 | 6x3 (18) | 7x3 (21) | 6x4 (24) | 67% | no |
| 6 | Mistlands | Eitrweave Pack | Black Forge 1 | 7x3 (21) | 6x4 (24) | 7x4 (28) | 58% | no |
| 7 | Ashlands | Cinder Pack | Black Forge 2 | 6x4 (24) | 7x4 (28) | 8x4 (32) | 50% | yes |

## Recipes

| Tier | Tier recipe | 2 star | 3 star |
|---|---|---|---|
| 1 | Leather Scraps 20, Deer Hide 8 | Leather Scraps 12, Deer Hide 5 | Leather Scraps 18, Deer Hide 7 |
| 2 | Scrap Satchel, Troll Hide 10, Bronze Nails 20, Resin 20 | Troll Hide 6, Bronze Nails 12 | Troll Hide 9, Bronze Nails 18, Resin 10 |
| 3 | Forest Knapsack, Iron 16, Ancient Bark 30, Guck 10 | Iron 10, Ancient Bark 18, Guck 6 | Iron 14, Ancient Bark 27, Guck 9 |
| 4 | Bog Pack, Silver 16, Wolf Pelt 10, Wolf Hair Bundle 10 | Silver 10, Wolf Pelt 6 | Silver 14, Wolf Pelt 9, Wolf Hair Bundle 6 |
| 5 | Frostbound Pack, Black Metal 16, Lox Pelt 10, Linen Thread 30 | Black Metal 10, Linen Thread 18 | Black Metal 14, Lox Pelt 9, Linen Thread 27 |
| 6 | Plainsrunner Pack, Eitr 20, Scale Hide 10, Carapace 20 | Eitr 12, Carapace 12 | Eitr 18, Scale Hide 9, Carapace 18 |
| 7 | Eitrweave Pack, Flametal 16, Asksvin Hide 10, Charred Bone 20, Morgen Sinew 6 | Flametal 10, Charred Bone 12 | Flametal 14, Asksvin Hide 9, Charred Bone 18, Morgen Sinew 5 |

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
