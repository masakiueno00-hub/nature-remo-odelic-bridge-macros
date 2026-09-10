# Nature Remo button macros

These public XML files contain only one-byte commands for the local ESP32
bridge. They contain no ODELIC Lighting ID, authentication key, challenge,
MAC address, or reusable ODELIC packet.

## Living / dining ceiling-pair buttons

These existing values now send two fixed individual-light (`C0`) events: first
to Living 3, then to Living 2. They do not address Living 1 / みかまさや部屋.

| File | Bridge value | Result |
| --- | --- | --- |
| `odelic_warm_100pct.xml` | `06` | Warm endpoint, 100% brightness |
| `odelic_warm_80pct.xml` | `07` | Warm endpoint, 80% brightness |
| `odelic_warm_60pct.xml` | `02` | Warm endpoint, 60% brightness |
| `odelic_warm_40pct.xml` | `03` | Warm endpoint, 40% brightness |
| `odelic_warm_20pct.xml` | `04` | Warm endpoint, 20% brightness |
| `odelic_neutral_100pct.xml` | `08` | Neutral midpoint (full light), 100% brightness |
| `odelic_neutral_80pct.xml` | `09` | Neutral midpoint, 80% brightness |
| `odelic_neutral_60pct.xml` | `0A` | Neutral midpoint, 60% brightness |
| `odelic_neutral_40pct.xml` | `0B` | Neutral midpoint, 40% brightness |
| `odelic_neutral_20pct.xml` | `0C` | Neutral midpoint, 20% brightness |
| `odelic_daylight_100pct.xml` | `0D` | Daylight endpoint, 100% brightness |
| `odelic_daylight_80pct.xml` | `0E` | Daylight endpoint, 80% brightness |
| `odelic_daylight_60pct.xml` | `0F` | Daylight endpoint, 60% brightness |
| `odelic_daylight_40pct.xml` | `10` | Daylight endpoint, 40% brightness |
| `odelic_daylight_20pct.xml` | `11` | Daylight endpoint, 20% brightness |
| `odelic_nightlight.xml` | `12` | First-stage nightlight |
| `odelic_off.xml` | `05` | Living/dining ceiling pair OFF |

## みかまさや部屋 buttons（12個）

These values address only the fixed Living 1 virtual address confirmed by the
read-only topology query.

| File | Bridge value | Result |
| --- | --- | --- |
| `odelic_mikamasaya_warm_100pct.xml` | `60` | Warm endpoint, 100% brightness |
| `odelic_mikamasaya_warm_80pct.xml` | `61` | Warm endpoint, 80% brightness |
| `odelic_mikamasaya_warm_60pct.xml` | `62` | Warm endpoint, 60% brightness |
| `odelic_mikamasaya_warm_40pct.xml` | `63` | Warm endpoint, 40% brightness |
| `odelic_mikamasaya_warm_20pct.xml` | `64` | Warm endpoint, 20% brightness |
| `odelic_mikamasaya_neutral_100pct.xml` | `65` | Neutral midpoint, 100% brightness |
| `odelic_mikamasaya_neutral_80pct.xml` | `66` | Neutral midpoint, 80% brightness |
| `odelic_mikamasaya_neutral_60pct.xml` | `67` | Neutral midpoint, 60% brightness |
| `odelic_mikamasaya_neutral_40pct.xml` | `68` | Neutral midpoint, 40% brightness |
| `odelic_mikamasaya_neutral_20pct.xml` | `69` | Neutral midpoint, 20% brightness |
| `odelic_mikamasaya_nightlight.xml` | `6F` | First-stage nightlight |
| `odelic_mikamasaya_off.xml` | `70` | みかまさや部屋 OFF |

## Father room buttons

| File | Bridge value | Result |
| --- | --- | --- |
| `odelic_father_warm_100pct.xml` | `30` | Warm endpoint, 100% brightness |
| `odelic_father_warm_80pct.xml` | `31` | Warm endpoint, 80% brightness |
| `odelic_father_warm_60pct.xml` | `32` | Warm endpoint, 60% brightness |
| `odelic_father_warm_40pct.xml` | `33` | Warm endpoint, 40% brightness |
| `odelic_father_neutral_100pct.xml` | `34` | Neutral midpoint, 100% brightness |
| `odelic_father_neutral_80pct.xml` | `35` | Neutral midpoint, 80% brightness |
| `odelic_father_neutral_60pct.xml` | `36` | Neutral midpoint, 60% brightness |
| `odelic_father_neutral_40pct.xml` | `37` | Neutral midpoint, 40% brightness |
| `odelic_father_nightlight.xml` | `38` | First-stage nightlight |
| `odelic_father_off.xml` | `39` | Father room group OFF |

## Children room buttons

| File | Bridge value | Result |
| --- | --- | --- |
| `odelic_children_warm_100pct.xml` | `40` | Warm endpoint, 100% brightness |
| `odelic_children_warm_80pct.xml` | `41` | Warm endpoint, 80% brightness |
| `odelic_children_warm_60pct.xml` | `42` | Warm endpoint, 60% brightness |
| `odelic_children_warm_40pct.xml` | `43` | Warm endpoint, 40% brightness |
| `odelic_children_neutral_100pct.xml` | `44` | Neutral midpoint, 100% brightness |
| `odelic_children_neutral_80pct.xml` | `45` | Neutral midpoint, 80% brightness |
| `odelic_children_neutral_60pct.xml` | `46` | Neutral midpoint, 60% brightness |
| `odelic_children_neutral_40pct.xml` | `47` | Neutral midpoint, 40% brightness |
| `odelic_children_nightlight.xml` | `48` | First-stage nightlight |
| `odelic_children_off.xml` | `49` | Children room group OFF |

## Loft buttons（登録する12個）

These twelve buttons address only raw group `07`, which the read-only live query
confirmed for all four OD361678BR downlights. The nightlight entry uses the
official app's common-CCT warm low-output command, not the ceiling-light `C5`
nightlight opcode.

| File | Bridge value | Result |
| --- | --- | --- |
| `odelic_loft_warm_100pct.xml` | `50` | Warm endpoint, 100% brightness |
| `odelic_loft_warm_80pct.xml` | `51` | Warm endpoint, 80% brightness |
| `odelic_loft_warm_60pct.xml` | `52` | Warm endpoint, 60% brightness |
| `odelic_loft_warm_40pct.xml` | `53` | Warm endpoint, 40% brightness |
| `odelic_loft_neutral_100pct.xml` | `54` | Neutral midpoint, 100% brightness |
| `odelic_loft_neutral_80pct.xml` | `55` | Neutral midpoint, 80% brightness |
| `odelic_loft_neutral_60pct.xml` | `56` | Neutral midpoint, 60% brightness |
| `odelic_loft_neutral_40pct.xml` | `57` | Neutral midpoint, 40% brightness |
| `odelic_loft_nightlight.xml` | `58` | Official warm low-output nightlight equivalent |
| `odelic_loft_off.xml` | `59` | Loft group OFF |
| `odelic_loft_warm_20pct.xml` | `5E` | Warm endpoint, 20% brightness |
| `odelic_loft_neutral_20pct.xml` | `5F` | Neutral midpoint, 20% brightness |

## Optional legacy button

`odelic_on.xml` is retained only as a historical file. Bridge value `01` is now
rejected, because a group-01 broadcast would also operate みかまさや部屋. Do
not register or use this legacy button.

The bridge exposes service
`625dfc6f-36f7-4936-b726-de5014c7ef22` and a Write With Response command
characteristic `313e2b82-1941-4a1f-8265-8319a395a6cc`. Nature Remo sends
each value with `WRITE_REQUEST`.

Upload this directory to a public GitHub repository. In Nature Home, create
one button per XML file and paste its normal GitHub `blob` URL, for example:

```text
https://github.com/OWNER/REPOSITORY/blob/main/odelic_off.xml
```

Do not add the private eight-digit Lighting ID to this directory or public
repository.
