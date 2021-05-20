# looking-glass-scripts
Odds and ends to interface with Looking Glass

### Using `make_quilt`
'Make Quilt' takes in a sequnce of rendered frames from the output of [btparker's fork of the Blender LKG addon](https://github.com/btparker/blenderLKG) (install by [downloading the looking_glass_tools.zip from the release](https://github.com/btparker/blenderLKG/releases/tag/v4.0-alpha) and select within Blender 2.92 Preferences->Add-ons->Install).

Help output:
```
Create a Looking Glass Quilt file

optional arguments:
  -h, --help            show this help message and exit
  --file-pattern FILE_PATTERN, -fp FILE_PATTERN
                        Target files pattern, such as
                        "render/foo.{:04d}.{:02d}.png"
  --output OUTPUT, -o OUTPUT
                        Output filename and path of desired file
  --tiles-h TILES_H, -th TILES_H
                        Number of tiles, horizontal
  --tiles-v TILES_V, -tv TILES_V
                        Number of tiles, vertical
  --video
  --tile-first TILE_FIRST, -tf TILE_FIRST
                        Index of the first tile
  --frame-first FRAME_FIRST, -ff FRAME_FIRST
                        Index of the first frame
  --frame-last FRAME_LAST, -fl FRAME_LAST
                        Index of the last frame
  --frames-per-second FRAMES_PER_SECOND, -fps FRAMES_PER_SECOND
                        Frames per second for video
```
Example:
```sh
make_quilt -fp "new-render/{:04d}.{:02d}.png" -o test/foo --video -ff 0 -fl 49
```
