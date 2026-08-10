# Nature Remo button macros

These public XML files contain only one-byte commands for the local ESP32
bridge. They contain no ODELIC Lighting ID, authentication key, challenge,
MAC address, or reusable ODELIC packet.

| File | Bridge value | Result |
| --- | --- | --- |
| `odelic_on.xml` | `01` | Restore the Living group's previous ON state |
| `odelic_warm_60pct.xml` | `02` | Warm endpoint, 60% brightness |
| `odelic_warm_40pct.xml` | `03` | Warm endpoint, 40% brightness |
| `odelic_warm_20pct.xml` | `04` | Warm endpoint, 20% brightness |
| `odelic_off.xml` | `05` | Living group OFF |

The bridge exposes service
`625dfc6f-36f7-4936-b726-de5014c7ef22` and a Write With Response command
characteristic `313e2b82-1941-4a1f-8265-8319a395a6cc`. Nature Remo sends
each value with `WRITE_REQUEST`.

Upload this directory to a public GitHub repository. In Nature Home, create
one button per XML file and paste its normal GitHub `blob` URL, for example:

```text
https://github.com/OWNER/REPOSITORY/blob/main/nature_remo_macros/odelic_off.xml
```

Do not add the private eight-digit Lighting ID to this directory or public
repository.
