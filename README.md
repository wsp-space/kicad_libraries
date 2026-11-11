# WSP KiCad Common Library

<p align="center">
    <source media="(prefers-color-scheme: dark)" srcset="assets/wsp_logos/logo_colour_dark.png" width="40%">
    <source media="(prefers-color-scheme: light)" srcset="assets/wsp_logos/logo_colour_light.png" width="40%">
    <img src="assets/wsp_logos/logo_colour_dark.png" alt="WSP Logo" width="40%">
</p>

A shared parts drawer for **和歌山大学宇宙開発プロジェクト (WSP)** — the Wakayama University team that flies hybrid rockets and stratospheric balloons.

The connectors, sensors, and power parts we reach for again and again live here as KiCad libraries, so a member can drop them onto a board instead of drawing them from scratch.

## What's inside 🧰

Common libraries for WSP hardware:

| Kind | What you get |
| --- | --- |
| **Symbols** | Schematic parts (`.kicad_sym`) |
| **Footprints** | PCB pads and courtyards (`.kicad_mod`) |
| **3D models** | Shapes for the 3D viewer, when we have them |

Look for libraries nicknamed with a `WSP_` prefix.

## Layout 🗂️

```
kicad_libraries/
├── symbols/                 # one .kicad_sym per library  (WSP_<Name>.kicad_sym)
├── footprints/              # one .pretty folder per library (WSP_<Name>.pretty/)
├── 3dmodels/                # one .3dshapes folder per library (WSP_<Name>.3dshapes/)
├── assets/                  # images for this README
├── sym-lib-table            # ready-made entries for every library
└── fp-lib-table
```

A symbol library and its footprint library share the same nickname,
so `WSP_Logo:WSP_Logo` works in both editors.

## Use it in KiCad 🪐

Every path goes through one path variable, **`WSP_KICAD_LIB`**.
Each machine can clone the repo wherever it likes; only the variable changes.

1. Clone this repository.
   ```sh
   git clone https://github.com/wsp-space/kicad_libraries.git
   ```
2. Set `WSP_KICAD_LIB` to the cloned folder, either
   - in KiCad: **Preferences → Configure Paths** → add `WSP_KICAD_LIB`, or
   - as an OS environment variable (KiCad picks it up on start):
     ```powershell
     # Windows
     setx WSP_KICAD_LIB "D:\Dev\kicad_libraries"
     ```
     ```sh
     # macOS / Linux (~/.zshrc or ~/.bashrc)
     export WSP_KICAD_LIB="$HOME/dev/kicad_libraries"
     ```
3. Open **Preferences → Manage Symbol Libraries** / **Manage Footprint Libraries**
   and add the lines from this repo's `sym-lib-table` / `fp-lib-table`
   (or add each file with **Add existing library** and replace the path prefix with `${WSP_KICAD_LIB}`).
4. Run `git pull` now and then to get new parts.

In footprints, point 3D models at `${WSP_KICAD_LIB}/3dmodels/WSP_<Name>.3dshapes/...`
so the 3D viewer works on every machine.

A **global** library is handy on your own machine. A **project** library travels more kindly when you hand a board to another member.

## License 📜

All symbols and footprints owned by WSP are shared under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) ([full text](LICENSE-CC_BY_4.0)). Other works is dependes on their own licenses, so please check the license of each part before using it.

You can copy them, tweak them, and pass them on. Please:

- Credit **和歌山大学WSP (Wakayama University Space Project)**
- Link back to this repository
- Say what you changed
- Keep a link to the license

## Add a part 🔧

If the whole team keeps redrawing the same thing, it belongs here.

1. Put symbols in `symbols/WSP_<Name>.kicad_sym` and footprints in `footprints/WSP_<Name>.pretty/`, and add both to `sym-lib-table` / `fp-lib-table`.
2. Open a pull request and mention which board or experiment the part is for.

Happy routing. May your courtyards stay clear and your balloons stay aloft. 🎈
