# Warsaw by Night — installation

Night lighting for Warsaw in **Microsoft Flight Simulator 2024**.

## Requirements

- Microsoft Flight Simulator 2024 (PC). Not built or tested for MSFS 2020.
- About 75 MB of disk space.
- No other add-ons needed.

## Install

1. Close MSFS.
2. Unzip the archive. It contains one folder, `rb-warsaw-by-night`, and these text files.
3. Move the `rb-warsaw-by-night` folder into your MSFS 2024 **Community** folder, or link it with your add-on
   linker (MSFS Addons Linker, Addon Manager and similar).
   - Default for the Microsoft Store / Xbox app:
     `%LOCALAPPDATA%\Packages\Microsoft.Limitless_8wekyb3d8bbwe\LocalCache\Packages\Community`
   - Default for Steam: `%APPDATA%\Microsoft Flight Simulator 2024\Packages\Community`
   - If you chose another location, look up `InstalledPackagesPath` in `UserCfg.opt` (in the folder above
     `Packages`); the Community folder is inside that path.
4. Start MSFS and fly to Warsaw at night.

To update, delete the old `rb-warsaw-by-night` folder first, then copy in the new one.

## Remove older test builds

If you had development builds, remove or unlink these so nothing loads twice: `rb-warsaw-lights`,
`rb-warsaw-lights-glow`, `rb-warsaw-lights-default-off`, `rb-warsaw-lights-posts`, `rb-warsaw-lights-probe*`,
`rb-warsaw-lights-efb`.

## Recommended settings

- Graphics → **Objects Level of Detail** and **Terrain Level of Detail**: higher values let the light on the
  streets reach farther (100 or more recommended).
- The lighting is night-only: street lights and ground glow come on with the sim's day/night cycle.

## Known limitations

- **Coverage** is Warsaw within its administrative boundary. Outside it, MSFS default lighting continues.
- **Halos by day:** the glow dots at the lamp heads (drawn as airport-style light sprites) are also visible in
  daylight, faintly. MSFS gives these sprites no day/night switch. A day/night-aware replacement is in testing.
- **Default lights far away:** the package switches off MSFS's own street lights inside the city. MSFS applies that
  only near the aircraft, so from very far away the default city lights can still show under ours.
- **Airports:** no lamps are placed inside airport boundaries, so airport sceneries such as Drzewiecki Design EPWA keep
  their own apron lighting. Roads around airports keep our lamps; with an airport scenery that also lights them, those
  stretches may get light from both.
- **Lamp types and colours** are inferred: the city's lamp survey gives positions only, so LED or sodium and the lamp
  design come from OpenStreetMap tags, road class and distance from the centre.
- **Performance:** about 274,000 lamps. On weaker systems, lower Objects Level of Detail first.
- No in-sim control panel (EFB) yet.

## Uninstall

Close MSFS and delete (or unlink) the `rb-warsaw-by-night` folder.

## Support

Report problems with a screenshot and your position (or the street name) as an issue at
https://github.com/Tolya1/WarsawByNightReleases/issues. New versions are published at
https://github.com/Tolya1/WarsawByNightReleases/releases.

Data sources and credits: see CREDITS.md.
