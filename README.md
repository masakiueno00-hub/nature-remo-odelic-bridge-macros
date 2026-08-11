# Nature Remo button macros

These public XML files contain only one-byte commands for the local ESP32
bridge. They contain no ODELIC Lighting ID, authentication key, challenge,
MAC address, or reusable ODELIC packet.

## Main buttons

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
| `odelic_off.xml` | `05` | Living group OFF |

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

## Optional legacy button

`odelic_on.xml` sends bridge value `01`, the official all-on marker. It is
kept as an optional compatibility button and is not one of the 17 main
fixed-state buttons above.

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
