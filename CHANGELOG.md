# Changelog

## 0.3.0 — 2026-11-24

First public release. (0.1.0 and 0.2.0 were internal test builds.)

- **Light pools reach much farther, without block pop-in**: every light cell model is padded to a 3 km box
  (invisible corner markers at ±1.5 km) around its 300 m of lights. The sim streams and keeps large models from much
  farther away, and the real light on the road now holds out well beyond the ~1–1.5 km edge of 0.2.0.

## 0.2.0 — 2026-11-23

- **Light cells keep every light at every distance**: side-street lights no longer switch off about 1–3 km out, so
  there is no side-street pop-in (as Drzewiecki EPWA keeps all its lights in every LOD). Costs more frame rate.
- **Smaller light cells**: 300 m instead of 400 m (5,130 cells, at most 428 lights each, was 507).
- Bollard clustering of dense survey lamps stays off; lamps back to 273,903.

## 0.1.0 — 2026-11-23

First release: one package, `rb-warsaw-by-night`, for MSFS 2024.

- **Lamps from the City of Warsaw pole survey** (~251k street lamps), with OSM lamps and generated lamps filling gaps:
  273,903 in all. Lamps inside airport
  boundaries are left out, so airport sceneries such as Drzewiecki EPWA keep their own apron lighting.
- **3D lamp posts** at every lamp (LED arm, double-arm T pole, sodium cobra head, residential, lantern, bollard, mast).
- **Real light on the road in light cells**: the street lights live in light-only models per 400 m cell, so they are
  drawn as far as the sim allows (the same reach as airport lighting), not only within ~200 m of the camera.
  Major roads at 25,000 cd with 150° beams; local streets lit up close only.
- **Lamp colour from the city's LED tender**: 4000 K main roads, 3000 K local streets, sodium where it remains.
- **Halos** at every lamp, visible from any distance; brighter and larger on major roads.
- **Ground glow**: baked night-only light pools on the terrain in three steps (hidden near the camera, half strength
  from ~250 m, full from ~1 km) plus ~12 km far tiles, so the city stays lit on a long approach.
- **MSFS default street lights and feature-point lights switched off** inside the city boundary.
- Obstruction lights on masts and towers, floodlit pitches, fuel stations.

Known limits:

- Coverage ends at the city's administrative boundary; MSFS default lighting continues outside it.
- Up close, MSFS's exclusion takes effect only near the aircraft; from very far away MSFS's own distant city lights
  can show under ours.
- No EFB control panel yet.
- Squares with many surveyed path lights (e.g. Plac Defilad) get a full post per light; turning such clusters into
  bollards (`cityPoles.cluster`) is implemented but off, as it made the city look worse from a distance.
