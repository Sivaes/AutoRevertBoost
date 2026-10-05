# ReSkate Revert Boost @MOD@

Land an unfinished spin and the game's **auto revert** finishes the turn for you. With this mod on,
that landing also gives you a **forward speed boost**, so you keep your momentum, and chaining reverts
builds more and more speed.

## Use
1. Press **Insert**, open **SKATER**, and find the **BOOSTS** card.
2. Turn **Revert Boost** on. It is off by default.
3. Set **Revert boost** to how much speed each revert adds (+0.5 to +15 m/s, where 1 m/s is 3.6 km/h).
   The default is +2 m/s (about 7 km/h).
4. Spin, land short of a half turn, and chain them.

A landing counts as a revert when the spin ended 12 to 45 degrees short of (or past) a half turn after
at least 90 degrees of turning in the air. A clean 180 (or 360) gives no boost. Speed is never boosted above about 144 km/h.

## Install
1. Install ReSkate normally and run it once.
2. Install this mod from the ReSkate launcher's **MODS** tab (or drag the zip onto the launcher).
3. **Close the game and the launcher.**
4. Open the mod's folder (`Mods\<author>-ReSkate_RevertBoost`) and double-click **Install.bat**.
   It saves your current `ReSkate.dll` and `ReSkateLauncher.exe` in a `backup` folder there, then
   copies this mod's over them.
5. Start `ReSkateLauncher.exe` as usual.

This extra step is needed because the mod is a build of ReSkate itself (it changes the game's code),
and the launcher can only place files in the Mods folder.

**Uninstall:** close the game and the launcher and run **Uninstall.bat**.

## Updates
This mod **updates itself**. Its launcher checks this mod's releases on GitHub each time you start it
(the same way ReSkate's own launcher does) and installs the new `ReSkate.dll` and launcher, so you do
not need any command-line flag. Turn that off in the launcher's Settings if you prefer.

It follows **this mod's** releases, not ReSkate's. When the ReSkate project ships a new version, this mod
needs the new source merged and rebuilt first, so it can lag behind ReSkate for a while. If you want
ReSkate's own updates right away, run **Uninstall.bat** to go back to the stock files.

## Crashes
This build is **modified**, and it says so: the start-up notice shows `Modified build: ReSkate_RevertBoost <version>`
and the log (`logs\ReSkate.log`) notes when Revert Boost is turned on or off.

If the game or launcher crashes and **Send crash reports** is on (launcher Settings > ADVANCED), the crash dump and
that session's log are uploaded to the ReSkate project exactly as with stock ReSkate, but the report is
**labelled as coming from this mod** (`build.mod` and `build.mod_version`), so the ReSkate developers can
tell it apart from their own. Please do not ask them to fix crashes in a modified build; report them
here instead: https://github.com/@REPO@/issues

If you suspect the mod: turn **Revert Boost** off (Insert > Skater > BOOSTS) and see if it still happens,
and send the end of `logs\ReSkate.log`. A crash cannot be traced to the mod automatically, so this
is how to tell.

## Good to know
- Built on **ReSkate @BASE@** (mod version @MOD@). ReSkate's own TRAINER tab is separate and keeps working: Revert Boost lives under SKATER > BOOSTS.
- Do not install it together with other mods that also replace `ReSkate.dll` (for example the ReSkate
  Trainer): the last one installed wins.
- It follows ReSkate's session rules. If a host turns boosts off, Revert Boost is off too.
- It unlocks no cosmetics and ships no game data.

## Tuning feedback
Every landing with 30 or more degrees of spin writes a line starting with `Revert Boost:` to
`logs\ReSkate.log`, with the spin, the physics states and whether a boost fired. Please include a few
of them in any bug report.

## Source and license
GPL-3.0, the same as ReSkate. Source: https://github.com/@REPO@

Not affiliated with EA, Full Circle or the ReSkate developers. You need your own copy of skate. on Steam.
