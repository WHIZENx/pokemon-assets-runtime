# PokeGoBreeze Runtime Assets

Public, generated runtime assets used by [PokeGoBreeze](https://poke-go-breeze.vercel.app/).

This repository is a read-only distribution mirror. It keeps the image files required by the PokeGoBreeze web application and API publicly accessible without exposing credentials or the private asset-processing source repository.

## Contents

| Path | Description |
| --- | --- |
| [`icon/`](./icon/) | Pokémon icons and supported form variants. |
| [`pokemon-animation/all/`](./pokemon-animation/all/) | Animated Pokémon profile images and supported variants. |
| [`manifest.json`](./manifest.json) | Publication metadata, source revision, file counts, sizes, and section checksums. |

The repository is generated automatically. Asset directories and the manifest should not be edited manually because the next publication may replace those changes.

## Using an asset

Use a URL pinned to a commit when reproducible output and long-lived caching are important:

```text
https://raw.githubusercontent.com/WHIZENx/pokemon-assets-runtime/<commit>/icon/bulbasaur.png
https://raw.githubusercontent.com/WHIZENx/pokemon-assets-runtime/<commit>/pokemon-animation/all/bulbasaur.gif
```

Use the `master` branch when the latest published asset is preferred:

```text
https://raw.githubusercontent.com/WHIZENx/pokemon-assets-runtime/master/icon/bulbasaur.png
```

File names are normalized by the asset pipeline and may include a form or variant suffix, such as `-mega`, `-galar`, or another supported form identifier. Check the repository tree or `manifest.json` rather than assuming that every Pokémon or form has every asset type.

## Updates and integrity

An automated publisher synchronizes the required runtime files from the maintained source and updates `manifest.json`. The manifest records:

- the source revision used for the publication;
- the publication timestamp;
- file and byte counts for each published section; and
- a SHA-256 digest for each section inventory.

Consumers that need deterministic builds should read the manifest and pin asset URLs to the published commit instead of tracking `master`.

## Scope and availability

This mirror exists primarily for PokeGoBreeze. It is publicly readable and may be useful to other projects, but it is not a versioned package or a general-purpose asset CDN and does not provide an uptime or compatibility SLA. Large animations make a full clone expensive; fetch only the files you need whenever possible.

For missing or incorrect assets, open an issue in this repository or in the [PokeGoBreeze project](https://github.com/WHIZENx/PokeGoBreeze) and include the Pokémon, form, expected file name, and affected URL.

## Legal notice

Pokémon and related names, characters, and imagery are trademarks and copyrights of their respective owners. This repository is an unofficial fan-project resource and is not affiliated with, endorsed by, or sponsored by Nintendo, The Pokémon Company, Game Freak, or Niantic. Public access to this repository does not grant additional rights to the underlying artwork; users are responsible for ensuring that their use is permitted.
