
===============================
Hintergrundkarten
===============================

Hintergrundkarten (Basemaps) sind Hintergrund-Karten. Sie sind oft sehr praktisch, da sie einfach zu bedienen sind, eine leichte Orientierung auf der Kartenansicht ermöglichen und vielfältig sind.

.. note::
   Mit den Hintergrundkarten ist keine Interaktion möglich. Sie sind lediglich "Bilder" im Hintergrund!

Standard QGIS-Hintergrundkarten
===============================

Sie können jederzeit die Standard-OpenStreetMap als Hintergrundkarte zu Ihrer Kartenansicht hinzufügen. 

Es gibt zwei Möglichkeiten, OpenStreetMap als Hintergrundkarte hinzuzufügen.

**Option 1:** Suchen Sie im Panel ``Browser`` nach ``XYZ Tiles``. Öffnen Sie das Dropdown-Menü durch Anklicken und wählen Sie OpenStreetMap oder eine andere Hintergrundkarte aus.

**Option 2:** ``Layer`` -> ``Layer hinzufügen`` -> ``XYZ-Layer hinzufügen...`` -> Wählen Sie OpenStreetMap oder eine andere Hintergrundkarte.

**Standard-OpenStreetMap als Hintergrundkarte hinzufügen**

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/blob/main/fig/Add_basemap_OSM.mp4"></video>

Google und Bing Hintergrundkarten hinzufügen
--------------------------------------------

Um zusätzliche Hintergrundkarten ohne Plugins hinzuzufügen, müssen Sie ``XYZ Tiles`` konfigurieren. 
Klicken Sie im ``Browser-Panel`` mit der rechten Maustaste auf ``XYZ Tiles`` -> ``Neue Verbindung``.

``Name`` = Der Name der neuen Hintergrundkarte.

``URL`` = Sie können jede der URLs aus der untenstehenden Tabelle verwenden.

.. list-table:: URLs für Hintergrundkarten
   :widths: 20 30 50
   :header-rows: 1

   * - Name
     - Info
     - URL
   * - OpenTopoMap
     - Open-Source Topografische Karte basierend auf OSM und SRTM
     - https://tile.opentopomap.org/{z}/{x}/{y}.png
   * - Google Terrain
     -
     - https://mt1.google.com/vt/lyrs=t&x={x}&y={y}&z={z}
   * - Google Hybrid
     -
     - https://mt1.google.com/vt/lyrs=y&x={x}&y={y}&z={z}
   * - Google Satellite
     -
     - https://mt1.google.com/vt/lyrs=s&x={x}&y={y}&z={z}
   * - Google Road
     -
     - https://mt1.google.com/vt/lyrs=m&x={x}&y={y}&z={z}
   * - Google Roads only
     -
     - https://mt1.google.com/vt/lyrs=h&x={x}&y={y}&z={z}
   * - Google alternative Road map
     -
     - https://mt1.google.com/vt/lyrs=r&x={x}&y={y}&z={z}
   * - Bing Aerial
     -
     - http://ecn.t3.tiles.virtualearth.net/tiles/a{q}.jpeg?g=1

Vorteile bei der Verwendung von Hintergrundkarten über XYZ Tiles sind:
* Laden schneller
* Unterstützen Umprojizierung
* Unterstützen den Druck
* Werden von Online-Anwendungen wie QField unterstützt
