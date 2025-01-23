# Changelog

## v4.0.0

- Retroactively improved GitHub changelog and readme.
- Improved and added much more documentation, with examples.
- Removed some redundant code and fixed a few stability issues.
- Replaced internal usages of `FlxTimer` with `Sequence`.
- Added notekinds:
  - `cynlib.song.notekinds.AltNote`
    - A note kind that plays the sing animation with the "alt" suffix.
  - `cynlib.song.notekinds.MissNote`
    - A note kind that causes the note to be "missed" by the player or opponent.
    - Parameters can only be accessed after `onNoteIncoming`.
      - Temporary until [Funkin#3292](https://github.com/FunkinCrew/Funkin/issues/3292) is resolved and [Funkin#2635](https://github.com/FunkinCrew/Funkin/pull/2635) merged.
  - `cynlib.song.notekinds.NoAnimationNote`
    - A note kind that skips the singing animation for the note.
- Added shaders:
  - `cynlib.shader.shaders.AberrationShader`
  - `cynlib.shader.shaders.SaturationShader`
  - `cynlib.shader.shaders.VignetteShader`
- Added `cynlib.save.Save`
  - A helper module for managing mod save data.
- Added `cynlib.shader.ShaderCoordFix`.
  - Globally fixes incorrect shader coordinates when the game is resized.
- Added `cynlib.song.NoteAnimOverride`.
  - Helper module for overriding note singing animations.
- Added `cynlib.song.SingleVocalsFix`.
  - Fixes muting issues with single-vocal songs.
- Added `cynlib.song.SymmetricStrums`
  - A simple helper class that makes the strumlines symmetric like in other engines.
- Changes to `cynlib.menu.Menu`:
  - Added support for mouse-based items, separate from keyboard-based ones. See internal documentation for more info.
- Changes to `cynlib.menu.MenuItem`:
  - Added `hitbox` property for mouse-based items.
  - Now respects `enabled` property (whoops).
- Changes to `cynlib.neocam.Neocam`:
  - Can now have a `startPosition`, `startZoom`, and `startBumpPattern` on creation.
  - Now uses the 1-measure bump pattern instead of none by default.
  - Added optional relative bump/bump patterns and relative note offset.
  - Removed `debugMode`.
  - Controllers are now only auto-destroyed during a mod reload instead of also when `PlayState` is destroyed.
- Changes to `cynlib.sequence.Sequence`;
  - No longer uses `FlxTimer`s (having hscript issues).
- Changes to `cynlib.song.SongHelper`:
  - Added `PlayState` instance and cameras to `songVars`.
  - Callback arrays now use a priority system similar to `cynlib.reloader.Reloader`.
  - Replaced `createPre` and `createPost` callbacks with `create`.
  - Added `stageReset` callbacks and corresponding `onStageReset` function to be called by stage scripts.
  - Added `closePersist` and `close` callbacks.
  - Added `events` callback integer map for step-based song events.
  - Now calls callbacks when playtesting during charting (not minimal mode).
- Changes to `cynlib.util.GenUtil`:
  - Added `randomCallback`.
  - Added `intColorToVec4`.
  - Added `sanitizePath`.
- Changed to `cynlib.util.MathUtil`:
  - Added `mod`.
    - Temporary until [Funkin#3617](https://github.com/FunkinCrew/Funkin/pull/3617) gets merged.

## v3.0.0

- Added partial documentation.
- Adjusted module priorities.
- Changes to `cynlib.song.SongManager`:
  - Renamed to `SongHelper` and simplified.

## v2.0.0

- Changed to package-based modules/classes.
- Changes to `cynlib.reloader.Reloader`
  - Small stability fixes with sorting.
- Changes to `cynlib.util.MathUtil`:
  - Added `smoothLerpDecay` and `smoothLerpPrecision` ([credit to Freya Holmer](https://twitter.com/FreyaHolmer/status/1757918211679650262)).
    - Temporary until [Funkin#3617](https://github.com/FunkinCrew/Funkin/pull/3617) gets merged.
  - Removed `remap` (can use `FlxMath.remapToRange` and `FlxMath.bound` instead).

## v1.0.0

- Initial release.
