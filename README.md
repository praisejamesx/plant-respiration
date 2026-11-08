# Plant Respiration

An author-hosted Osmograph domain Vial for one-plant change monitoring.

**Status:** v0.6.0. Installs as **Ungated** because it has no held-out evidence
block. It is not a reviewed Aromatory listing and it makes no measured
false-alarm, latency, or minimum-detectable-effect claim. The host gate and the
project tests pass; real-rig validation is still outstanding.

## What is here

| File | Purpose |
|---|---|
| `vial.json` | The `osmograph.domain-pack/2` manifest and anomaly profile |
| `ui.html` | The sandboxed workspace body fragment |
| `home.html` | The compact sandboxed Home view |

The profile is a starting point, not evidence. The host compiles it into the
detector: at least two channels must clear their sensitivity-scaled budget, the
profile's persistence, hysteresis, confidence floor, and coverage gate apply,
and the call is withheld when the enclosure moved. The workspace's 2×CV band
explains the channels; it is not a competing detector. This Vial does not
identify ethylene, a pest, a pathogen, or a care fault.

## Validate

From the Osmograph desktop repository:

```bash
cd /home/praisejamesx/Documents/Documents/Research/coglab/OpenSmell/osmograph-desktop
npm run validate:vial -- /home/praisejamesx/Documents/Documents/code/osmograph-vials/plant-respiration
```

From the `opensmell-rs` repository:

```bash
noses lint /home/praisejamesx/Documents/Documents/code/osmograph-vials/plant-respiration
noses test /home/praisejamesx/Documents/Documents/code/osmograph-vials/plant-respiration
```

`noses lint` and `noses test` pass with warnings. `noses publish` refuses until
a real evidence block exists; that is deliberate.

Run the project's own contract test:

```bash
npm test
```

## Install locally

Serve this directory over HTTP, then paste its `/vial.json` URL into
**Vials → Aromatory → Install from URL**. Do not install from a local file: the
host cannot fetch `ui.html` or `home.html` from a file import.

## Scope

Same plant, same array, same enclosure, and the same time of day. A reading does
not transfer across arrays, rooms, or seasons. The response is a mixed-gas
signal; water, light, temperature, humidity, handling, cleaning products, people,
and sensor drift all move it. A quiet array is not proof of health.

## License

CC BY 4.0, as declared in `vial.json`.
