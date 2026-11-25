# Repository Guidelines

## Project Structure & Module Organization

This repository contains a 6502 microcomputer hardware design. Design files currently live in `kicad/`:

- `6502.kicad_pro`, `6502.kicad_sch`, and `6502.kicad_pcb`: modern mainboard project, schematic, and PCB.
- `6502-bb.kicad_pcb` and `6502-bb.pro`: prototype board.
- `6502.sch`, `6502.pro`, and `6502-cache.lib`: legacy design files and symbol cache.
- `3D/`: STEP models; `gerber/` and `gerber-bb/`: manufacturing exports.
- `6502.csv`, `layout.pdf`, render images, and `memory_map.numbers`: BOM and supporting documentation.

`kicad/README.md` documents board previews and the memory map. No firmware source or automated test directory is currently present.

## Development & Validation Commands

With KiCad executables available on your PATH, run from the repository root:

- `kicad kicad/6502.kicad_pro`: open the mainboard project.
- `pcbnew kicad/6502-bb.kicad_pcb`: open the prototype PCB.
- `git diff --check`: check text changes for whitespace errors.
- `git status --short`: review changed files and generated artifacts.

The mainboard PCB was saved with KiCad 9.0. Use a compatible version and review any format migration separately. There is no scripted build, lint, or test pipeline; generate manufacturing outputs through KiCad.

## Editing & Naming Conventions

Let KiCad manage native file formatting and indentation. Preserve component references, net names, and the `6502` / `6502-bb` filename prefixes. Use concise Markdown with descriptive headings for documentation. Avoid unrelated editor rewrites and committing autosaves, caches, or backup archives.

## Testing Guidelines

Run schematic Electrical Rules Check (ERC) and PCB Design Rules Check (DRC) for affected designs. Review connectivity, footprints, board outlines, silkscreen, and 3D placement. Record unresolved violations and their justification. Inspect regenerated Gerbers and drill files before fabrication. No automated coverage target exists; the README currently labels v1.0.0 unverified.

## Commit & Pull Request Guidelines

History uses short, descriptive subjects such as `Add BOM` and `Update README`; follow that style. Keep commits focused. PRs should explain the hardware change, identify affected boards, report ERC/DRC results, and include screenshots for layout changes. Link relevant issues and state whether manufacturing exports were regenerated.

## Library Configuration

`fp-lib-table` and `sym-lib-table` contain absolute paths from another machine. Resolve the referenced Arduino and 6502 libraries locally; prefer project-relative paths when sharing fixes. Verify library and 3D model resolution before saving designs.
