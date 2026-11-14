# Change Marker

Compare two pictures of the same place taken on different dates, mark what changed, and export the marks for Google Earth
(KMZ, KML), for GeoJSON tools such as geojson.io, or as a CSV list of the marks.

Open it at https://alislayman.github.io/change-marker/, or download `index.html` and open it in Chrome, Edge or Firefox:
the whole tool is that one file. The pictures you open and the marks you draw stay in your browser; the tool sends them
nowhere.

## What it does

1. **Pictures.** Drop a before and an after picture: screenshots of a satellite viewer (for example NASA Worldview or the
   Copernicus Browser), downloads, a KMZ ground overlay, or a picture with its world file. Under **Taken on**, type the date
   each picture was taken: a screenshot does not carry it.
2. **Line them up.** Automatically (OpenCV feature matching), or with pinned pairs by hand, then check with the
   checkerboard view.
3. **Put on the map.** Pin three places far apart and not in a line, pasting their coordinates from Google Maps; or type
   the corners, or load a world file or a KML.
4. **Compare.** Side by side, swipe, blink, fade, checkerboard.
5. **Find changes (drafts).** Plants lost, burned ground (on short-wave infrared pictures), brighter or darker ground,
   structure lost or gained, small new objects. Every result is a draft until a person keeps it.
6. **Mark.** Areas, lines and points, by kind, each with an ID, a note, the two dates the change was seen between (**Use the
   dates on screen** writes the two Taken on dates) and its size in hectares or metres. Links in a mark's box open its place in
   Google Maps, Google Earth, the Copernicus Browser, NASA FIRMS fires, EFFIS burnt areas and geojson.io, on its dates.
7. **Export.** KMZ (marks coloured by kind and dated for Google Earth's time slider, with both pictures as ground
   overlays), KML, GeoJSON, a CSV list of the marks, PNG pictures with a legend, SVG overlays, and the work itself (JSON).
   **Open saved work** brings back a saved JSON or KMZ.

The browser keeps your marks between visits, and offers to bring them back; **Save work** keeps them in a file.

A picture shows where the ground changed and between which dates, never who did it or why.

## Notes

* The automatic line-up and Find changes load OpenCV.js 4.12 from jsDelivr the first time they are used, so they need the
  internet once. To work offline, put an OpenCV.js build named `opencv.js` next to `index.html`.
* Made by Green Southerners. OpenCV.js: Apache License 2.0.
