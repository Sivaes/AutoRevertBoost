# Changelog

## 0.2.1
- Fixed clean 180s giving a boost. The spin is now measured on every physics step from takeoff to
  touchdown, instead of about 9 times a second, which missed the start and end of the turn.
- A landing must now end at least 12 degrees short of (or past) a half turn to count as a revert.
- Built on ReSkate 1.1.1.

## 0.2.0
- Rebuilt on the current ReSkate, which now includes the trainer. Nothing else about the boost changed.
- Revert Boost now reads and logs nothing until you turn it on, like ReSkate's own features.

## 0.1.0
- First release. Built on ReSkate 1.0.3 (game build 25414733).
- Revert Boost: land a spin a few degrees short of (or past) a half turn, the moment the game's
  auto revert finishes it, and gain forward speed. Chain reverts to keep building speed.
- Slider (+0.5 to +15 m/s) and on/off toggle in Insert > Skater > BOOSTS.
- Updates itself from this mod's GitHub releases (no `--no-update` flag needed).
- Crash reports and the log say the build is modified; crash reports carry `build.mod` and `build.mod_version`.
- Every landing with 30+ degrees of spin is written to `logs\ReSkate.log` as `Revert Boost:`.
