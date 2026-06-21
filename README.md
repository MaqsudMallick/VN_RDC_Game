# Rental Dao Companion

A xianxia visual novel built with [Ren'Py](https://www.renpy.org/). Ren'Py is
cross-platform, so the game runs on Windows, macOS, and Linux (and can be built
for Android/web).

> **Mature content.** This project contains adult themes and nudity.

## Requirements

- [Ren'Py SDK **8.5.3**](https://www.renpy.org/latest.html) (the version this
  project was authored and compiled against).

## Running the game

The repository **is** the Ren'Py project (this folder is the project root). You
run it with your own copy of the Ren'Py SDK — nothing platform-specific is
committed.

**With the Ren'Py launcher (any OS):**
1. Open the Ren'Py launcher from the SDK.
2. Set the "projects directory" to the folder that contains this repo, or place
   the cloned folder next to the SDK's other projects.
3. Select **VN_RDC_Game** and click **Launch Project**.

**From the command line:**
```sh
# macOS / Linux — from the SDK directory:
./renpy.sh /path/to/VN_RDC_Game

# Windows — from the SDK directory:
renpy.exe C:\path\to\VN_RDC_Game
```

## Project layout

```
game/
  *.rpy            # Ren'Py source (options, gui, screens, …)
  script.rpyc      # compiled story bytecode (see note below)
  images.rpa       # packed game art (sprites, CGs, backgrounds)
  gui/ audio/ libs/ # UI, audio, support files
```

## Notes for contributors

- **Art** is packed into `game/images.rpa`. Ren'Py loads it automatically. To
  edit individual images you unpack the archive (e.g. with `unrpa`), drop loose
  PNGs back into `game/images/`, and Ren'Py will prefer the loose files.
- **Story** ships as compiled `game/script.rpyc`; the editable `script.rpy`
  source is intentionally not committed (to keep the plot out of the repo's
  file view). The game runs fine from the bytecode. Editing the story requires
  the source — ask the maintainer.
