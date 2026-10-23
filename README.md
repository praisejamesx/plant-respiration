# Plant Respiration

An author-hosted Osmograph domain Vial for plant-health context.

**Status:** local project, not yet pushed or published. The web app does not host this
source. Install it from this project's manifest URL once it is published.

## What is here

| File | Purpose |
|---|---|
| `vial.json` | The `osmograph.domain-pack/1` manifest |

This project is currently declarative. It has no sandboxed `ui.html` or
`home.html`. The workspace records plant context, array response, and a manual
journal; it does not claim ethylene detection, pest diagnosis, or pathogen
detection.

## Validate

From the Osmograph desktop repository:

```bash
cd /home/praisejamesx/Documents/Documents/Research/coglab/OpenSmell/osmograph-desktop
npm run validate:vial -- /home/praisejamesx/Documents/Documents/code/osmograph-vials/plant-respiration
```

Run the project's own contract test:

```bash
npm test
```

## Scope

The current constants table has no ethylene channel. A change signal is not a
pest or pathogen diagnosis. If the Vial later gains a sensor UI, it must include
the real array field and state exactly what the array can and cannot see.

## License

CC BY 4.0, as declared in `vial.json`.
