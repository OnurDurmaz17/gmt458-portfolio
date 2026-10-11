# GMT 458 - Assignment 1: Web Page Portfolio

**Developer:** Onur Durmaz  -  2210674030
**University:** Hacettepe University - Geomatics Engineering  

---

## 🤖 AI Usage & Time Spent
* **Total Estimated AI Engagement Time:** ~2.5 hours
* **Collaborative Process:** AI was utilized to help structure the responsive CSS layout, debug complex integrations for Leaflet and OpenLayers, and assist with the overall modern UI/UX design.

---

## 🗺️ Resolution of Mapping Issues

### Issue 1: Zoom-dependent Visibility (Zoom Threshold)
To prevent visual clutter at smaller map scales, point data is constrained to only appear when the user zooms in sufficiently.
* **Leaflet Solution:** Handled by grouping the target locations inside an `L.layerGroup` and using a `zoomend` event listener to dynamically add or remove the layer based on the current zoom level.
* **OpenLayers Solution:** Solved efficiently by applying the native `minZoom: 5` property directly to the vector layer that holds the marker features.

### Issue 2: Preventing Map Wrapping (Multi-World Duplication)
To maintain a professional look, the map is restricted from repeating multiple copies of the world horizontally when zoomed out.
* **Leaflet Solution:** Configured the base tile layer with the `noWrap: true` parameter and enforced absolute panning limits using the `bounds` property.
* **OpenLayers Solution:** Implemented by setting `wrapX: false` on the OpenStreetMap source and locking the view's scrolling limits using the `extent` property.

---

## ✨ Features Highlighted
* **Dynamic Day/Night Theme:** A fully responsive light and dark mode toggle that updates the UI styling and swaps the textures on the 3D globe.
* **Cinematic 3D Globe:** An animated, 3D rotating Earth that utilizes GPU-accelerated CSS to smoothly pan and zoom toward specific continental locations during page navigation.
* **Responsive Design:** A mobile-friendly, fluid layout utilizing CSS grids, modern card designs, and high-resolution spatial imagery.