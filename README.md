# pandora-box-manifest

Builder component **manifests** (field descriptors) for the Pandora Box low-code engine's
layout components — the extractor-generated SSOT, shipped as data. Pairs 1:1 with
[`pandora-box-layout`](https://github.com/stephenkingsley/pandora-box-layout) (the runtime
components), so a builder or a project reads the **exact** field config the builder uses
("builder == delivered").

Zero runtime dependencies — it's plain JSON plus structural TypeScript types.

## Install

```bash
npm install pandora-box-manifest
```

## Usage

```ts
import { manifests, components, manifest } from 'pandora-box-manifest';

manifests.WhatsNew;   // the WhatsNew component manifest (keyed by name)
components;            // ComponentManifest[]
manifest;             // { version, components }
```

Assign to your own `ComponentManifest` (e.g. from `pandora-box-react`) directly or with a cast —
the shapes match:

```ts
import type { ComponentManifest } from 'pandora-box-react';
export const whatsNewManifest = manifests.WhatsNew as ComponentManifest;
```

## Components covered

`Flex` · `Card` · `Overlay` · `Typography` · `MediaCaption` · `MediaCarousel`
· `HeroOverview` · `WhatsNew` · `UpcomingList` · `ServiceList`

## License

MIT
