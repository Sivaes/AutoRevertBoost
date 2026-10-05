# ReSkate Revert Boost

A small patch for [ReSkate](https://github.com/Dingo-Shenanigans/ReSkate) (GPL-3.0). Land an unfinished spin
(the game's auto revert) and gain forward speed; chain reverts to keep building it. Slider and toggle in
Insert > SKATER > BOOSTS. Off until you turn it on.

This repository holds only the patch (`patches/revert-boost.patch`), the files for the Thunderstore package
(`thunderstore/`) and the workflows that build it. ReSkate's source is fetched from the ReSkate project when
you build, so nothing of theirs is copied here.

## Status
0.2.1 fixes clean 180s being boosted (0.2.0 measured the spin about 9 times a second and missed the
start and end of the turn). Untested in game until a log shows it. Next: boost only when the game's own
auto revert happens, and bring back board bends.

## Build it
1. Actions > **Build Revert Boost** > Run workflow.
2. `upstream_ref`: a ReSkate release tag such as `v1.1.1` (or `main`). `mod_version`: this mod's version (x.y.z).
3. Leave **publish** off for a zip to test or send to a friend; download it from the run's Artifacts.
4. Tick **publish** to create a GitHub release whose launcher updates players automatically.

The run summary lists the applied patch and the repository commit, which is also stamped into the build
(start-up notice and `logs\ReSkate.log`). If the **Apply the patch** step fails, ReSkate changed a file the
patch edits and the patch needs updating.

Not affiliated with EA, Full Circle or the ReSkate developers.
