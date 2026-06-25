# Block & Item ID Map

This document tracks the current block and item ID assignments used by JRJR Enhanced 1.2.5.

## v0.3.0 - Forestry Compatibility

### Reserved / Active Block IDs

| Mod | Config file | Entry | ID | Notes |
|---|---|---:|---:|---|
| IC2 | `IC2.cfg` | `blockHarz` | 190 | Resin |
| IC2 | `IC2.cfg` | `blockOreCopper` | 191 | Copper ore |
| IC2 | `IC2.cfg` | `blockMachine` | 195 | IC2 machines |
| IC2 | `IC2.cfg` | `blockRubWood` | 196 | Rubber wood |
| Forestry | `forestry/base.conf` | `soil` | 197 | Forestry soil |
| IC2 | `IC2.cfg` | `blockOreTin` | 198 | Tin ore |
| IC2 | `IC2.cfg` | `blockOreUran` | 199 | Uranium ore |
| IC2 | `IC2.cfg` | `blockGenerator` | 200 | IC2 generator |
| Forestry | `forestry/base.conf` | `machine` | 205 | Forestry machines |
| Forestry | `forestry/base.conf` | `mill` | 208 | Forestry mill |
| Railcraft | `railcraft.cfg` | `block.detector` | 280 | Moved to avoid Forestry conflicts |
| Railcraft | `railcraft.cfg` | `block.track` | 281 | Moved to avoid Forestry conflicts |
| Railcraft | `railcraft.cfg` | `block.utility` | 282 | Moved to avoid Forestry conflicts |
| Railcraft | `railcraft.cfg` | `block.cube` | 284 | Moved to avoid Forestry conflicts |
| Railcraft | `railcraft.cfg` | `block.elevator` | 285 | Moved to avoid Forestry conflicts |
| Railcraft | `railcraft.cfg` | `block.structure` | 286 | Moved to avoid Forestry conflicts |
| Forestry | `forestry/base.conf` | `oreTin` | 4093 | High block ID |
| Forestry | `forestry/base.conf` | `resources` | 4094 | High block ID |
| IC2 | `IC2.cfg` | `blockRubSapling` | 4095 | High block ID |

## Forestry Item IDs

| Config file | Entry | ID |
|---|---|---:|
| `forestry/base.conf` | `fertilizerBio` | 5000 |
| `forestry/base.conf` | `fertilizerCompound` | 5001 |
| `forestry/base.conf` | `apatite` | 5002 |
| `forestry/base.conf` | `ingotCopper` | 5003 |
| `forestry/base.conf` | `ingotTin` | 5004 |
| `forestry/base.conf` | `ingotBronze` | 5005 |
| `forestry/base.conf` | `wrench` | 5007 |
| `forestry/base.conf` | `gearBronze` | 5008 |
| `forestry/base.conf` | `bucketBiomass` | 5009 |
| `forestry/base.conf` | `sturdyMachine` | 5010 |
| `forestry/base.conf` | `vialCatalyst` | 5012 |
| `forestry/base.conf` | `bioFuel` | 5013 |
| `forestry/base.conf` | `bioMass` | 5014 |
| `forestry/base.conf` | `bucketBiofuel` | 5015 |
| `forestry/base.conf` | `liquidMilk` | 5016 |
| `forestry/base.conf` | `peat` | 5017 |
| `forestry/base.conf` | `ash` | 5018 |
| `forestry/base.conf` | `gearCopper` | 5019 |
| `forestry/base.conf` | `waterCan` | 5020 |
| `forestry/base.conf` | `canEmpty` | 5021 |
| `forestry/base.conf` | `biomassCan` | 5022 |
| `forestry/base.conf` | `biofuelCan` | 5023 |
| `forestry/base.conf` | `gearTin` | 5024 |
| `forestry/base.conf` | `hardenedMachine` | 5025 |
| `forestry/base.conf` | `iodineCapsule` | 5026 |
| `forestry/pipes.conf` | `propolisPipe` | 14000 |

## Known Changes

| Version | Change |
|---|---|
| v0.3.0 | Replaced `forestry-client-A-1.4.8.7_bc2.2.jar` with `forestry-client-A-1.4.6.1.jar`. |
| v0.3.0 | Moved Railcraft block IDs away from `204` and `205` to avoid conflicts with Forestry. |

## Notes

- Forestry 1.4.6.1 is currently the working Forestry version.
- The previous Forestry 1.4.8.7 `_bc2.2` build failed with a BuildCraft API compatibility error.
- Railcraft was moved to the `280-286` block ID range.
- IC2 block IDs are currently mostly unchanged from the working v0.2.0 snapshot.