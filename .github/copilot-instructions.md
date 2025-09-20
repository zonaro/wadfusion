# WadFusion Developer Instructions

## Project Overview
WadFusion is a Python-based WAD merge utility that combines multiple DOOM/DOOM II WAD files into a single IPK3 file for GZDoom. It's derived from WadSmoosh and now includes extensive support for community and commercial add-ons integrated from wadsmoosh-plus.

## Architecture & Key Files

### Core Components
- `wadfusion.py` - Main application logic, command-line interface, and extraction orchestration
- `wadfusion_data.py` - Configuration tables defining supported WADs, lump lists, and file mappings
- `data/` - Lump extraction lists organized by WAD and content type (graphics, music, patches, etc.)
- `res/` - Pre-authored content (mapinfo, textures, scripts) copied directly to output
- `omg/` - Modified Omgifol library for WAD file manipulation

### Data Flow
1. **Detection**: Scan `source_wads/` for supported WAD files using case-insensitive matching
2. **Validation**: Check WAD dependencies and extract version-specific lumps (Unity/KEX variants)
3. **Extraction**: Process each WAD through `extract_lumps()` and `extract_iwad_maps()` 
4. **Assembly**: Copy pre-authored resources, apply patches, rename files
5. **Packaging**: Create compressed IPK3 using ZipFile

## WAD Support Architecture

### WAD Categories
- **Core IWADs**: doom.wad, doom2.wad, tnt.wad, plutonia.wad
- **Official Add-ons**: nerve.wad, sigil.wad, id1.wad, masterlevels.wad
- **Community WADs**: doomzero.wad, freedoom1/2.wad, neis.wad
- **Commercial WADs**: hell2pay.wad, perdgate.wad, jptr_v40.wad
- **Fan Projects**: tntr.wad, pl2.wad, prcp.wad, tnt2_beta6.wad

### Configuration Pattern
Each WAD requires entries in:
1. `WADS` list (extraction order)
2. `REPORT_WADS` list (detection/reporting) 
3. `WAD_LUMP_LISTS` dict (content to extract)
4. `WAD_MAP_PREFIXES` dict (map filename prefixes)
5. Corresponding `data/` files listing specific lumps

### Dependency System
- Many WADs require base IWADs (freedoom can substitute for doom.wad/doom2.wad)
- Version detection functions check for specific lumps (`doom_is_registered()`, `extras_is_kex()`)
- Dynamic lump list modification in `add_to_wad_lump_lists()` based on available WADs

## Development Workflows

### Adding New WAD Support
1. Create lump lists in `data/` (e.g., `graphics_newwad`, `music_newwad`)
2. Add WAD name to `WADS` and `REPORT_WADS` lists
3. Define lump extraction in `WAD_LUMP_LISTS`
4. Add map prefix to `WAD_MAP_PREFIXES` if extracting maps
5. Add validation logic in `extract_iwads()`
6. Update episode detection in `get_eps()`

### Command Line Options
- `-v/--verbose`: Enable detailed logging
- `-p/--patch`: Update existing IPK3 without re-extracting WADs
- `-d/--deflate`: Use DEFLATE compression instead of STORED
- `-e/--extract-only`: Skip pre-authored content (development mode)

### Special Processing
- **Master Levels**: Custom map ordering and numbering system
- **SIGIL/SIGIL2**: Multiple soundtrack variants with runtime switching
- **Unity/KEX ports**: Widescreen asset extraction and version detection
- **Xbox levels**: Special map placement (E1M10, MAP33)

## Critical Implementation Details

### File Naming Conventions
- Maps use prefixes to avoid conflicts (TN_MAP01.wad, PL_MAP01.wad)
- Alternative WAD names handled via `SIGIL_ALT_FILENAMES` arrays
- Case-insensitive matching via `get_wad_filename()`

### Resource Management
- Temporary directory `temp/` cleared on each run
- Pre-authored content in `res/` takes precedence over extracted lumps
- Special handling for music format conversion (MP3, OGG renaming)

### Error Handling
- Extensive dependency validation with informative error messages
- Graceful degradation when optional WADs missing
- Error tracking via `num_errors` global counter

## Testing Considerations
- Test with various WAD combinations and missing dependencies
- Verify map extraction and numbering for complex scenarios
- Check IPK3 loading in GZDoom for validation
- Test both verbose and quiet modes

## Integration Notes
- Recent integration merged wadsmoosh-plus capabilities
- Maintains backward compatibility with existing WAD collections
- Extensive community WAD support while preserving official content focus