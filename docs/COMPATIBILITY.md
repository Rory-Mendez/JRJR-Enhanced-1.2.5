# Compatibility Notes

This document records all compatibility decisions made during the development of **JRJR Enhanced**.

Its purpose is to explain why specific mod versions were selected and document known compatibility issues.

---

## Stable Environment

The following versions have been tested together and are considered stable.

| Component       | Version                  |
| --------------- | ------------------------ |
| Minecraft       | 1.2.5                    |
| Minecraft Forge | 3.4.9.171                |
| Java            | 8 (tested with 1.8.0_51) |
| LWJGL           | 2.9.4                    |

---

## Fixed ID Strategy

JRJR Enhanced uses fixed Block IDs and Item IDs instead of automatic allocation.

Reasons:

* Prevent conflicts when adding new mods.
* Keep IDs stable between releases.
* Simplify future maintenance.
* Improve compatibility with old Minecraft 1.2.5 mods.

The complete allocation can be found in `docs/ID_MAP.md`.

---

## Forestry

### Stable Version

* Forestry 1.4.6.1

### Tested

* Forestry 1.4.8.7_bc2.2

#### Result

The newer Forestry build is incompatible with BuildCraft 3.1.5 and causes initialization failures.

JRJR Enhanced uses Forestry 1.4.6.1.

---

## Railcraft

Railcraft originally conflicted with Forestry block allocations.

The conflict was solved by moving Railcraft to a dedicated Block ID range.

---

## ThaumCraft

ThaumCraft originally conflicted with IndustrialCraft².

The conflict was solved by assigning ThaumCraft its own reserved Block ID range.

---

## Portal Gun

Portal Gun required manual Block ID reassignment to avoid conflicts with Forestry.

After the ID changes the mod loads correctly.

---

## Steve's Carts

Steve's Carts stores its configuration inside:

.minecraft/Steve's Carts/

instead of the standard `config/` directory.

The default Block IDs conflict with BuildCraft and must be changed manually.

---

## Not Enough Items (NEI)

## Stable Configuration

| Component       | Version |
| --------------- | ------- |
| CodeChickenCore | 0.5.3   |
| NotEnoughItems  | 1.2.2.4 |

NEI is installed as a jar mod.

---

### Tested Versions

#### NEI 1.3.0.1

Issues observed:

* Recipe viewer crashes with some IndustrialCraft² recipes.
* Inconsistent compatibility with legacy plugins.

Status:

Not recommended.

---

#### NEI 1.2.2.4

Status:

Stable.

Recipe viewing works correctly for the tested mods.

---

## NEI Plugins

| Plugin            | Status       |
| ----------------- | ------------ |
| RedPower Plugin   | Supported    |
| IC2 Plugin        | Incompatible |
| Railcraft Plugin  | Incompatible |
| ThaumCraft Plugin | Incompatible |

The base version of NEI already provides recipe support for most installed mods.

Only the RedPower plugin provided additional functionality without introducing instability.

---

## Additional Pipes

Compatible with BuildCraft 3.1.5.

No additional configuration required.

---

## Logistics Pipes

Compatible with BuildCraft 3.1.5.

No additional configuration required.

---

## ComputerCraft

Compatible with BuildCraft, RedPower and IndustrialCraft².

No compatibility changes required.

---

## Known Limitations

* Some EE2 items expose internal metadata variants that are not craftable.
* Some IC2 powered item states (charged/discharged) do not have crafting recipes by design.
* Steve's Carts configuration is stored outside the standard config directory.

---

## Development Philosophy

JRJR Enhanced prioritizes:

* Stability
* Reproducibility
* Fixed ID allocation
* Compatibility with legacy Minecraft 1.2.5 mods

Whenever multiple versions are available, the most stable combination is preferred over the newest release.
