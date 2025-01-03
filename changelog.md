# Changelog

## v3.1.0

- improved and added more documentation
- `Menu` now has support for mouse-based items, separate from keyboard-based ones
- `MenuItems` now respect their `enabled` property (whoops)
- `Neocam` can now have a `startPosition`, `startZoom`, and `startBumpPattern` on creation
- `Neocam` now uses the 1-measure bump pattern instead of none by default
- added optional relative bump/bump patterns and relative note offset to `Neocam`
- removed `debugMode` from `Neocam`
- `Sequence` no longer uses `FlxTimer`s (hscript issues)
- `SongHelper` now calls callbacks when playtesting during charting (not minimal mode)
- changed internal usages of `FlxTimer` to use `Sequence`
- removed some redundant code and fixed a few stability issues

## v3.0.0

- simplified `songHelper` (previously `songManager`)
- added documentation
- adjusted module priorities

## v2.0.0

- changed to package based modules/classes
- small stability fixes with reloader sorting
- added `smoothLerpDecay` and `smoothLerpPrecision` to `MathUtil` ([credit to Freya Holmer](https://twitter.com/FreyaHolmer/status/1757918211679650262))
  - temporary until https://github.com/FunkinCrew/Funkin/pull/3617 gets merged
- removed `remap` from `MathUtil` (can use `FlxMath.remapToRange` and `FlxMath.bound`)

## v1.0.0

initial