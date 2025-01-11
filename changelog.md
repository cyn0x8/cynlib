# Changelog

## v4.0.0

- Retroactively improved GitHub changelog.
- Improved and added to documentation.
- Linked example videos in the GitHub readme.
- Removed some redundant code and fixed a few stability issues.
- Replace internal usages of `FlxTimer` with `Sequence`.
- Added notekinds:
  - `cynlib.notekinds.MissNote`
    - Parameters must be accessed after `onNoteIncoming` until [Funkin#3292](https://github.com/FunkinCrew/Funkin/issues/3292) and [Funkin#3989](https://github.com/FunkinCrew/Funkin/issues/3989) are resolved.
  - `cynlib.notekinds.NoAnimationNote`
- Added shaders:
  - `cynlib.shaders.AberrationShader`
  - `cynlib.shaders.SaturationShader`
  - `cynlib.shaders.VignetteShader`
- Changes to `cynlib.menu.Menu`:
  - Added support for mouse-based items, separate from keyboard-based ones. See internal documentation for more info.
- Changes to `cynlib.menu.MenuItem`:
  - Now respects `enabled` property (whoops).
- Changes to `cynlib.neocam.Neocam`:
  - Can now have a `startPosition`, `startZoom`, and `startBumpPattern` on creation.
  - Now uses the 1-measure bump pattern instead of none by default.
  - Added optional relative bump/bump patterns and relative note offset.
  - Removed `debugMode`.
- Changes to `cynlib.sequence.Sequence`;
  - No longer uses `FlxTimer`s (having hscript issues).
- Changes to `cynlib.song.SongHelper`:
  - Changed `PlayState` creation callback names.
  - Added step-based callback integer map for song events
  - Added `stageReset` callback array.
  - Now calls callbacks when playtesting during charting (not minimal mode).

## v3.0.0

- Added partial documentation.
- Adjusted module priorities.
- Changes to `cynlib.song.SongManager`:
  - Renamed to `SongHelper` and simplified.

## v2.0.0

- Changed to package based modules/classes.
- Changes to `cynlib.reloader.Reloader`
  - Small stability fixes with sorting.
- Changes to `cynlib.util.MathUtil`:
  - Added `smoothLerpDecay` and `smoothLerpPrecision` ([credit to Freya Holmer](https://twitter.com/FreyaHolmer/status/1757918211679650262)).
    - Temporary until [Funkin#3617](https://github.com/FunkinCrew/Funkin/pull/3617) gets merged.
  - Removed `remap` (can use `FlxMath.remapToRange` and `FlxMath.bound` instead).

## v1.0.0

- Initial release.