# WadFusion — Complete DOOM WAD Merger

WadFusion is an advanced DOOM WAD merge utility that combines official DOOM releases with community and commercial add-ons into a single IPK3 file for [GZDoom](https://zdoom.org/index). This enhanced version merges the best features of the original WadFusion with extensive WAD support from WadSmoosh-Plus, providing the most comprehensive DOOM collection tool available.

**Key Features:**
- Supports 30+ official, community, and commercial WADs
- Creates a single IPK3 file playable in GZDoom 4.14.1+
- Automatic dependency resolution and fallback systems
- Support for Unity/KEX port widescreen assets
- Master Levels with expanded "Rejects" content
- Multiple soundtrack variants (SIGIL, IDKFA)

If you're new to DOOM modding, see the [**Quick Start Guide**](#quick-start-guide) below.

## What's New in This Version

This version significantly expands WAD support by integrating capabilities from WadSmoosh-Plus:

### Official Content Support
- All original DOOM, DOOM II, and Final DOOM releases
- Master Levels for DOOM II (with optional "Rejects" expansion)
- SIGIL & SIGIL II with multiple soundtrack options
- Legacy of Rust (KEX re-release content)
- Unity/KEX port exclusive content and widescreen assets

### Community & Commercial Add-ons
- **Freedoom** - Open-source DOOM alternative
- **DOOM Zero** - Prequel campaign by Christopher Golden
- **Hell To Pay & Perdition's Gate** - Classic commercial releases
- **TNT: Revilution & Plutonia 2** - Fan-made sequels
- **No End in Sight** - Award-winning episode replacement
- **The Lost Episodes of DOOM** - Rare commercial add-on
- And many more (see complete list below)

## Quick Start Guide

1. **Download WadFusion** from the [releases page](https://github.com/Owlet7/wadfusion/releases)
2. **Extract** to a folder on your computer
3. **Copy your WAD files** to the `source_wads/` subfolder
4. **Run WadFusion** (`wadfusion.exe` on Windows, `wadfusion.py` on macOS/Linux)
5. **Confirm** when prompted - WadFusion will show you what episodes it can create
6. **Get GZDoom** from [zdoom.org](https://zdoom.org/downloads) if you don't have it
7. **Copy the generated `doom_fusion.ipk3`** to your GZDoom folder
8. **Launch GZDoom** and select "DOOM Fusion" as your IWAD

**That's it!** All your DOOM content will be available as separate episodes in the main menu.

## Requirements

- **GZDoom 4.14.1 or newer** (will not work with other engines)
- At least one supported IWAD (doom.wad, doom2.wad, etc.)
- Python 3.7+ (for non-Windows builds)

## Usage Options

WadFusion supports several command-line options for advanced users:

- `-h`, `--help` — Show help message and exit
- `-v`, `--verbose` — Show detailed extraction progress
- `-p`, `--patch` — Update existing IPK3 without re-extracting WADs
- `-d`, `--deflate` — Use DEFLATE compression (smaller files, slower)
- `-e`, `--extract-only` — Skip pre-authored content (for developers)

**Example:** `wadfusion.exe -v -d` (verbose output with compression)

## Complete WAD Support List

WadFusion supports a comprehensive range of DOOM content. You don't need all of these - WadFusion will work with whatever you have and can substitute missing dependencies when possible.

### 🎮 Official DOOM Releases

| WAD                | Description                          | Where to Get                                                                                         |
| ------------------ | ------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| `doom.wad`         | The Ultimate DOOM (Episodes 1-4)     | [Steam](https://store.steampowered.com/app/2280/) \| [GOG](https://www.gog.com/en/game/doom_doom_ii) |
| `doom2.wad`        | DOOM II: Hell on Earth               | [Steam](https://store.steampowered.com/app/2300/) \| [GOG](https://www.gog.com/en/game/doom_doom_ii) |
| `tnt.wad`          | TNT: Evilution (Final DOOM)          | [Steam](https://store.steampowered.com/app/2290/) \| [GOG](https://www.gog.com/en/game/final_doom)   |
| `plutonia.wad`     | The Plutonia Experiment (Final DOOM) | [Steam](https://store.steampowered.com/app/2290/) \| [GOG](https://www.gog.com/en/game/final_doom)   |
| `nerve.wad`        | No Rest for the Living               | Included with DOOM II Unity/KEX                                                                      |
| `masterlevels.wad` | Master Levels for DOOM II            | [KEX re-release](https://store.steampowered.com/app/2280/) or individual PWADs                       |

### 🏆 Official Add-ons & Expansions

| WAD                | Description                           | Where to Get                                               |
| ------------------ | ------------------------------------- | ---------------------------------------------------------- |
| `sigil.wad`        | SIGIL by John Romero                  | [Free download](https://romero.com/sigil)                  |
| `sigil_shreds.wad` | SIGIL Buckethead soundtrack           | [Free download](https://romero.com/sigil)                  |
| `sigil2.wad`       | SIGIL II by John Romero               | [Free download](https://romero.com/sigil)                  |
| `sigil2_mp3.wad`   | SIGIL II THORR soundtrack             | [Free download](https://romero.com/sigil)                  |
| `id1.wad`          | Legacy of Rust - Vulcan Abyss         | [KEX re-release](https://store.steampowered.com/app/2280/) |
| `id1-res.wad`      | Legacy of Rust - Resources            | [KEX re-release](https://store.steampowered.com/app/2280/) |
| `id24res.wad`      | Legacy of Rust - Additional Resources | [KEX re-release](https://store.steampowered.com/app/2280/) |
| `iddm1.wad`        | id Deathmatch Pack #1                 | [KEX re-release](https://store.steampowered.com/app/2280/) |
| `extras.wad`       | Unity/KEX Port Extras                 | Included with Unity/KEX releases                           |

### 🎪 Special Content

| WAD          | Description                     | Where to Get                                                                                                                   |
| ------------ | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| `sewers.wad` | Xbox DOOM secret level E1M10    | [idgames](https://www.doomworld.com/idgames/levels/doom/s-u/sewers2)                                                           |
| `betray.wad` | Xbox DOOM II secret level MAP33 | [Forum post](https://www.doomworld.com/forum/topic/128173-known-lost-wads-of-our-history/?page=4&tab=comments#comment-2481490) |
| `e1m4b.wad`  | Phobos Mission Control (Romero) | [idgames](https://www.doomworld.com/idgames/levels/doom/Ports/d-f/e1m4b)                                                       |
| `e1m8b.wad`  | Tech Gone Bad (Romero)          | [idgames](https://www.doomworld.com/idgames/levels/doom/Ports/d-f/e1m8b)                                                       |

### 🌟 Community & Commercial Add-ons

| WAD              | Description                             | Where to Get                                                                 |
| ---------------- | --------------------------------------- | ---------------------------------------------------------------------------- |
| `doomzero.wad`   | DOOM Zero by Christopher Golden         | [Free download](https://www.doomworld.com/forum/topic/117899-doom-zero/)     |
| `freedoom1.wad`  | Freedoom: Phase 1 (DOOM replacement)    | [Free download](https://freedoom.github.io/)                                 |
| `freedoom2.wad`  | Freedoom: Phase 2 (DOOM II replacement) | [Free download](https://freedoom.github.io/)                                 |
| `hell2pay.wad`   | Hell To Pay (commercial)                | Retail release - find your own copy                                          |
| `perdgate.wad`   | Perdition's Gate (commercial)           | Retail release - find your own copy                                          |
| `neis.wad`       | No End in Sight                         | [idgames](https://www.doomworld.com/idgames/levels/doom/Ports/megawads/neis) |
| `tntr.wad`       | TNT: Revilution                         | [idgames](https://www.doomworld.com/idgames/levels/doom2/megawads/tntr)      |
| `tnt2_beta6.wad` | TNT 2                                   | Community release                                                            |
| `pl2.wad`        | Plutonia 2                              | [idgames](https://www.doomworld.com/idgames/levels/doom2/megawads/pl2)       |
| `prcp.wad`       | Plutonia Revisited                      | Community release                                                            |
| `jptr_v40.wad`   | The Lost Episodes of DOOM               | Retail release - find your own copy                                          |
| `doom3do.wad`    | DOOM 3DO Soundtrack                     | [ModDB](https://www.moddb.com/games/doom/addons/doom-3do-music)              |

### 🔧 Unity/KEX Port Assets (Optional)

| WAD                 | Description                      | Notes                               |
| ------------------- | -------------------------------- | ----------------------------------- |
| `doomunity.wad`     | DOOM Unity widescreen assets     | Rename doom.wad from Unity port     |
| `doom2unity.wad`    | DOOM II Unity widescreen assets  | Rename doom2.wad from Unity port    |
| `tntunity.wad`      | TNT Unity widescreen assets      | Rename tnt.wad from Unity port      |
| `plutoniaunity.wad` | Plutonia Unity widescreen assets | Rename plutonia.wad from Unity port |
| `doomkex.wad`       | DOOM KEX widescreen assets       | Rename doom.wad from KEX port       |
| `doom2kex.wad`      | DOOM II KEX widescreen assets    | Rename doom2.wad from KEX port      |
| `tntkex.wad`        | TNT KEX widescreen assets        | Rename tnt.wad from KEX port        |
| `plutoniakex.wad`   | Plutonia KEX widescreen assets   | Rename plutonia.wad from KEX port   |

### 📁 Setting Up Your WADs

1. **Create a `source_wads` folder** in the same directory as `wadfusion.py`
2. **Copy your WAD files** into this folder
3. **Run WadFusion** - it will automatically detect which WADs you have

**File Naming:** WadFusion is flexible with file names. For example, these all work:
- `doom.wad`, `DOOM.WAD`, `doom1.wad`
- `doom2.wad`, `DOOM2.WAD` 
- `tnt.wad`, `TNT.WAD`
- `plutonia.wad`, `PLUTONIA.WAD`, `plut.wad`

### 🔄 Dependencies & Substitutions

WadFusion automatically handles dependencies:
- **Freedoom as DOOM substitute**: `freedoom1.wad` can replace `doom.wad`
- **Freedoom as DOOM II substitute**: `freedoom2.wad` can replace `doom2.wad`
- **Unity/KEX assets**: Will automatically use widescreen graphics if available
- **Multiple music packs**: SIGIL and SIGIL II support multiple soundtrack variants

## Advanced Usage

### Command Line Options

```bash
python wadfusion.py [options]
```

| Option               | Description                                     |
| -------------------- | ----------------------------------------------- |
| `-v, --verbose`      | Enable detailed output and progress information |
| `-p, --patch`        | Update existing IPK3 without re-extracting WADs |
| `-d, --deflate`      | Use DEFLATE compression instead of STORED       |
| `-e, --extract-only` | Extract WADs only, skip pre-authored content    |

### Special Features

- **Master Levels**: Automatically organizes and numbers all 20+ Master Levels
- **Map Prefixes**: Prevents conflicts by prefixing maps (e.g., `TN_MAP01.wad`, `PL_MAP01.wad`)
- **Version Detection**: Automatically detects Unity, KEX, and retail versions
- **Multi-format Music**: Supports OGG, MP3, and MIDI soundtrack variants
- **Widescreen Support**: Extracts Unity/KEX widescreen graphics when available

### Troubleshooting

**"WAD not found" errors:**
- Check that WAD files are in the `source_wads` folder
- Verify file names match supported patterns
- Use `-v` flag to see exactly which files WadFusion is looking for

**Missing dependencies:**
- WadFusion will tell you what's required and suggest alternatives
- Freedoom WADs can substitute for commercial IWADs in most cases

**Large file size:**
- Use `-d` flag for DEFLATE compression to reduce IPK3 size
- Consider which WADs you actually need - you don't need everything

## Master Levels & Special Content

### Master Levels Expanded Collection

WadFusion includes comprehensive Master Levels support with two modes:

**Standard Mode (21 maps)**: The official Master Levels as arranged by Xaser
**Expanded Mode (43 maps)**: Includes rejected and related bonus maps organized into sub-episodes

### Master Levels "Rejects" Collection

For the complete Master Levels experience, include these additional WADs:

| WAD            | Title                        | Where to Get                                                           |
| -------------- | ---------------------------- | ---------------------------------------------------------------------- |
| `cpu.wad`      | The C.P.U.                   | [idgames](https://www.doomworld.com/idgames/levels/doom2/a-c/cpu)      |
| `device_1.wad` | Device One                   | [idgames](https://www.doomworld.com/idgames/levels/doom2/d-f/device_1) |
| `dmz.wad`      | The D.M.Z.                   | [idgames](https://www.doomworld.com/idgames/levels/doom2/d-f/dmz)      |
| `cdk_fury.wad` | The Fury                     | [idgames](https://www.doomworld.com/idgames/levels/doom2/a-c/cdk_fury) |
| `e_inside.wad` | The Enemy Inside             | [idgames](https://www.doomworld.com/idgames/levels/doom2/d-f/e_inside) |
| `hive.wad`     | The Hive                     | [idgames](https://www.doomworld.com/idgames/levels/doom2/g-i/hive)     |
| `twm01.wad`    | Doom2 Map14 Homage           | [idgames](https://www.doomworld.com/idgames/levels/doom2/s-u/twm01)    |
| `mines.wad`    | Mines of Titan               | [idgames](https://www.doomworld.com/idgames/levels/doom2/m-o/mines2)   |
| `anomaly.wad`  | The Titan Anomaly            | [idgames](https://www.doomworld.com/idgames/levels/doom2/a-c/anomaly)  |
| `farside.wad`  | The Farside of Titan         | [idgames](https://www.doomworld.com/idgames/levels/doom2/d-f/farside)  |
| `trouble.wad`  | Trouble on Titan             | [idgames](https://www.doomworld.com/idgames/levels/doom2/s-u/trouble)  |
| `dante25.wad`  | Dante's Gate                 | [idgames](https://www.doomworld.com/idgames/levels/doom2/d-f/dante25)  |
| `achron22.wad` | Crossing Acheron             | [idgames](https://www.doomworld.com/idgames/levels/doom2/a-c/achron22) |
| `caball.wad`   | Caball                       | [doomshack.org](https://doomshack.org/uploads/caball.zip)              |
| `udtwid.wad`   | Ultimate Doom The Way id Did | [idgames](https://www.doomworld.com/idgames/levels/doom/s-u/udtwid)    |

⚠️ **Note**: [Works of the Masters](https://jp.itch.io/deluxe-master-levels) is NOT supported! Do not use WADs from that collection.

### Special Feature Details

**Unity/KEX Enhanced Assets:**
- Widescreen graphics automatically extracted when Unity/KEX WADs are present
- IDKFA soundtrack variants by Andrew Hulshult (toggleable in-game)
- Enhanced intermission screens and status bar icons

**SIGIL & SIGIL II Music:**
- Multiple soundtrack options (MIDI, Buckethead, THORR)
- Automatic detection of different SIGIL releases
- Runtime switching via in-game options menu

**John Romero's Bonus Maps:**
- Tech Gone Bad (`e1m8b.wad`) - Replaces E1M8
- Phobos Mission Control (`e1m4b.wad`) - Replaces E1M4
- Toggleable via in-game options menu

## Development & Contribution

WadFusion is designed to be extensible and welcomes community contributions.

### Key Architecture Files
- `wadfusion.py` - Main application logic and command-line interface
- `wadfusion_data.py` - WAD definitions, lump lists, and extraction rules
- `data/` - Lump extraction lists organized by WAD and content type
- `res/` - Pre-authored content (mapinfo, textures, scripts)
- `.github/copilot-instructions.md` - Detailed development guidelines

### Adding New WAD Support
1. Create lump lists in `data/` directory
2. Update `WADS` and `REPORT_WADS` lists in `wadfusion_data.py`
3. Define extraction rules in `WAD_LUMP_LISTS`
4. Add map prefixes if extracting levels
5. Update validation logic and episode detection

### Contributing
- Fork the repository and create feature branches
- Test with various WAD combinations before submitting PRs
- Update documentation for any new WAD support
- Follow existing code patterns and naming conventions

For detailed development instructions, see `.github/copilot-instructions.md`.

## Credits & License

**Original Projects:**
- **WadSmoosh** by JP LeBreton - Original DOOM WAD merger
- **WadSmoosh-Plus** by community contributors - Extended WAD support

**This Version:**
- Integrates the best features of both projects
- Adds comprehensive documentation and user experience improvements
- Maintains backward compatibility while significantly expanding capabilities

**Special Thanks:**
- JP LeBreton for creating the original WadSmoosh
- The wadsmoosh-plus community for expanding WAD support
- Fredrik Johansson and Devin Acker for the Omgifol library
- The DOOM community for preserving and enhancing these classic games
- All WAD authors and content creators who made these expansions possible

**License:** GPL v2 or later. See `LICENSE` for full details.

**Community:** Join the discussion on [GitHub Discussions](https://github.com/Owlet7/wadfusion/discussions) to share your experiences, ask questions, or showcase your DOOM collections!
