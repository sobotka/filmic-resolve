# Filmic Resolve
## What is it?
This is a repository to use [Filmic](https://github.com/sobotka/filmic-blender) in Resolve. It will allow you to
work seamlessly in Resolve with Filmic Base Log Encoded files.
## How is it used?
1. Download this repository via zip or Git.
2. Create a unique directory `Filmic` under your Resolve LUTs director. This is accessible via
the `File` `Project Settings` `Color Management` tab, by pressing the button `Open LUT Folder`.
3. Extract and copy the LUTs into the newly created Resolve `Filmic` folder. After doing so, return
to Resolve and press the `Update Lists` button directly above the `Open LUT Folder`.
4. In the `File` `Project Settings` `Color Management` tab, change the `Timeline Color Space` to `Rec.709 (Scene)`.
5. In the same tab, change the `3D Input Lookup Table` to `Filmic Resolve - Base Log Encoding to Scene Linear`.
6. In the same tab, change the `3D Output Lookup Table` to `Filmic Resolve - Scene Linear to Base Log Encoding`.

You are ready to go!
## What encodings are currently supported?
Currently, any Filmic Base Log Encoding files should work seamlessly. Simply save your imagery with the Filmic Base Log
Encoding, and load them into your media gallery within Resolve. Once inside Resolve, the default output will be displayed
with the flatter Filmic Base Log Encoding appearance, ~~and the full selection of Filmic aesthetic lookups are available
from the `Color` workspace, under the `LUTs` sub-workspace. Select an aesthetic contrast and you can refine the grade accordingly.~~

The Fusion tab within Resolve should receive the Timeline based scene linear radiometric data as well, allowing you to
perform proper radiometrically referred compositing.

## What currently isn't supported?
Currently the aesthetic contrast lookups are not working. In addition to this, loading directly from scene linear EXRs is not yet supported.

## What is the colourimetry of Filmic?
Please see the original repository for full colourimetry information.

TL;DR: The colourimetry of Filmic is based on BT.709 based primaries. The Filmic Log Encoding Base is a pure, normalized
log base two encoding, anchored around a middle grey value of `0.18`, with a +6.5 to -10.0 EV range. The gamut mapping
will properly map out of gamut values on the high intensity end to appropriate display referred output values.
