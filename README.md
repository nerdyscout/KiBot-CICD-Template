[![kibot](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/kibot.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/kibot.yml)
[![platformio](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/platformio.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/platformio.yml)
[![reuse](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/reuse.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/reuse.yml)

---

# KiCAD-CICD-Template

This repository provides different CI/CD workflows used for projects using [KiCAD](https://www.kicad.org/) and [PlatformIO](https://platformio.org).

## workflows

### KiBot

[KiBot](https://github.com/INTI-CMNB/KiBot/) is used to generate all kind of documentation from a KiCAD6 project.

Whenever a file matching `pcb/*.kicad_*` changes this workflow will trigger.

The following documents are generated on every build:

```
- pcb/cad/
   - dxf/
      - AutoCAD - DXF
   - boardview - BRD
   - 3D render - STEP
- pcb/docs/
   - bom/
      - Interactive BOM - HTML
      - Octopart list - CSV
      - KiCost - XLSX (disabled)
   - schematic - PDF
- pcb/img/
   - pcb/$fab/$style/
      - PCB top - SVG
      - PCB bottom - SVG
   - render/ (disabled)
      - PCB render - PNG
   - schematic - SVG
- pcb/gerbers - ZIP
```

### PlatformIO

used to rebuild your source code whenever it changes.

### REUSE

used to insure every file got a propper license. 

## getting started

- [ ] hit the "use this template" button and give your project a name
- [ ] clone this new repository localy
- [ ] replace content of README.md
- [ ] Code
   - [ ] put your code in the `src/` folder using platformio
- [ ] PCB
   - [ ] change the filenames in `pcb/*.kicad_*` matching your repository name
   - [ ] create your PCB
- [ ] run `reuse --lint`
   - [ ] make sure the licenses of `pcb/*` fits your needs
   - [ ] make sure the licenses of `src/*`, `include/*`, `lib/*`, `test/*` fits your needs
- [ ] commit and push all those changes regulary to your project
