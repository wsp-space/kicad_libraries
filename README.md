# WSP KiCad Common Library

![WSP Logo (Darkmode)](assets/wsp_logos/logo_colour_dark.png#gh-dark-mode-only)
![WSP Logo (Lightmode)](assets/wsp_logos/logo_colour_light.png#gh-light-mode-only)

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

## Use it in KiCad 🪐

1. Clone this repository and keep the folder where KiCad can see it.
   ```sh
   git clone https://github.com/wsp-space/kicad_libraries.git
   ```
2. In KiCad, open **Preferences → Manage Symbol Libraries**, or **Manage Footprint Libraries**.
3. Choose **Add existing library** and point at each `.kicad_sym` file, or each footprint folder.
4. Give it a nickname that starts with `WSP_`, then pick the part from that library in the schematic or PCB editor.

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

1. Put symbols and footprints in a clearly named `WSP_` library.
2. Open a pull request and mention which board or experiment the part is for.

Happy routing. May your courtyards stay clear and your balloons stay aloft. 🎈
