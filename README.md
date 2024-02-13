# serratus-geo-utils

A collection of tools related to the creation and visualization of geographic data related to the [serratus](https://serratus.io/) project.

# src/deck.gl.html

A single page HTML file that takes a list of coordinates as input and renders them as markes into a world map with a minimal graphical style.

The code makes use of [deck.gl](https://deck.gl/), a high-performance data visualization library for browsers.

In order to render your own data, there's two variables near the top of the file that you need to set up:

* `DECKGL_ICONLAYER_DATA`
    * A JSON array with a list of objects (markers) that you want to be displayed
    * Each of these objects should have the following properties:
        * color: an array with three numbers with the RGB value of the color you'd like to use for the current marker
        * coordinates: an array with two numbers, latitude and longitude, with the location where you'd want the marker to be
        * tooltip: a string of text that will be displayed when users move their mouse over the current marker

* `DECKGL_INITIALVIEWSTATE`
    * A JSON object with the properties of the initial viewport that is shown when the map loads
    * Properties:
        * latitude: latitude of the center coordinate of the map
        * longitude: longitude of the center coordinate of the map
        * zoom: default zoom level for the map
