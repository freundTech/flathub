# Music Assistant Companion
[Music Assistant Companion](https://github.com/music-assistant/companion) is made with Tauri and built using npx, yarn and cargo packages.

## Source generation
To transform their package locks into flatpak sources, [flatpak-builder-tools](https://github.com/flatpak/flatpak-builder-tools) is used.

```sh
# Generate companion sources for use with cargo
<path-to flatpak-builder-tools>/cargo/flatpak-cargo-generator.py -o cargo-sources.json <path-to companion>/src-tauri/Cargo.lock

# Generate companion sources for use with npm (Make sure the `frontend` submodule is initialized)
flatpak-node-generator --no-requests-cache -r -o node-sources.json npm <path-to companion>/yarn.lock
```
