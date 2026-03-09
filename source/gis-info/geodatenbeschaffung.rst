Geodatenbeschaffung - Ergänzung
===================

Für die Analysen im Tutorium nutzen wir eine vielzahl unterschiedlicher Datensätze aus verschiedenen Quellen. Auch für eure Abschlussaufgabe
werdet ihr Geodaten von unterschiedlichen Websites, Behörden, Open-Data-Portalen, etc. beziehen.

Hier findet eine unvollständige Liste, wo ihr Geodaten herunterladen könnt.

Darüber hinaus könnt ihr hier vorbei schauen. Hier wurde von der AG geoinformatik der Uni Tübingen eine Übersicht erstellt: https://felixweinschenk.github.io/Website_Datenquellen_Geoinformatik/

Um die passenden Daten für Ihr Projekt zu finden, können Sie Online-Plattformen für den Datenaustausch nutzen. Einige der wichtigsten Portale sind unten aufgeführt.

## Worauf Sie bei der Datensuche achten sollten

**Datenquelle:** Stellen Sie immer sicher, dass Sie Daten aus vertrauenswürdigen Quellen verwenden. Die Organisation, die die Daten bereitstellt, ist der beste Indikator. Darüber hinaus sind die Verwendung der Daten in seriösen Kontexten oder die Anzahl der Downloads gute Anhaltspunkte.

**Datengröße:** Manchmal können Sie auf Daten in verschiedenen Maßstäben, Auflösungen usw. zugreifen. Wählen Sie einen Datensatz, der für Ihren Zweck geeignet ist und den Sie problemlos verarbeiten können. Wenn Sie beispielsweise nur Daten für eine bestimmte Region benötigen, wählen Sie nur die Daten dieses Verwaltungsgebiets aus.

**Datenformat:** Möglicherweise stehen verschiedene Formate zur Auswahl. Überlegen Sie, was für Ihre Anforderungen am praktischsten ist – sowohl für die eigene Nutzung als auch für die eventuelle Weitergabe.

**Erfassungsdatum:** Prüfen Sie unbedingt, wann die Daten erhoben wurden und ob dieses Datum mit Ihren Anforderungen übereinstimmt. Kontrollieren Sie, ob eventuell aktuellere Daten aus einer anderen Quelle verfügbar sind.

**Datenlizenz:** Welche Art von Lizenz haben die Daten? Wie dürfen Sie diese nutzen oder teilen und wie muss die Quelle zitiert werden? Vergewissern Sie sich, dass Sie die Lizenzbestimmungen einhalten, um rechtliche Schwierigkeiten zu vermeiden.

.. figure:: /fig/en_data_sources_examples_cartong.png
   :name: de_data_sources_examples_cartong
   :width: 600 px

   Daten für Karten oder GIS-Analysen können aus verschiedenen Quellen stammen (Quelle: [CartONG](https://www.cartong.org/en/)).


==============================
Arten von Geodaten
==============================

* Vektordaten
* Rasterdaten
* Nicht-räumliche Daten umgewandelt in Geodaten

Vektordaten
===========

Vektordaten können die folgenden Datenformate aufweisen: 
.. list-table:: Vektordaten Formate
   :widths: 15 25 60
   :header-rows: 1

   * - Dateiendung
     - Name
     - Beschreibung
   * - ``.shp``
     - Shapefile
     - Veraltetes, aber noch weit verbreitetes Geodatenformat. Kann nur einen Datensatz enthalten. Ein Shapefile **muss** diese Dateien enthalten: ``.shp``, ``.shx`` und ``.dbf``. Es kann auch weitere Dateien enthalten wie: ``.prj``, ``.sbn``, ``.sbx``, ``.cpg``, ``.qix``.
   * - ``.gpkg``
     - GeoPackage
     - Sehr vielseitiges Geodatenformat und der neue Standard für Geodaten. Kann mehrere Dateien enthalten (Vektor, Raster und nicht-räumliche Daten wie Tabellen).
   * - ``.kml``
     - Keyhole Markup Language
     - Geodatenformat zur Verwendung mit Google Earth.
   * - ``.gpx``
     - GPS Exchange Format
     - Geodatenformat für den Austausch von Koordinaten. Zum Beispiel für Wegpunkte von Tracks.
   * - ``.geojson``
     - GeoJSON
     - Ähnlich wie Shapefiles, speichert jedoch alle Informationen in einer einzigen Datei.

Rasterdaten
===========

Rasterdaten können die folgenden Datenformate aufweisen: 
.. list-table:: Rasterdaten Formate
   :widths: 20 20 60
   :header-rows: 1

   * - Dateiendung
     - Name
     - Beschreibung
   * - ``.tif`` / ``.tiff`` / ``.geotiff``
     - Tag Image File Format
     - Gängiges Format für Raster- und Bilddaten. Verfügt nicht notwendigerweise über georeferenzierte Informationen. Wenn eine .tif-Datei georeferenzierte Informationen besitzt, wird sie als GeoTIFF bezeichnet.
   * - ``.nc``
     - netCDF
     - Standard-Datenformat für wissenschaftliche Daten wie Geschwindigkeit oder Temperatur. Kann eine Rasterdatei sein. Kann mehrere Datensätze enthalten.
   * - ``.asc``
     - Esri ASCII Grid files
     - Altes, einfaches Rasterdateiformat, immer mit georeferenzierten Informationen.

Textdaten
=========

.. list-table:: Textdaten Formate
   :widths: 15 25 60
   :header-rows: 1

   * - Dateiendung
     - Name
     - Beschreibung
   * - ``.xls``
     - EXCEL
     - Datenformat, das für EXCEL verwendet wird. EXCEL ist ein weit verbreitetes Tabellenkalkulationsprogramm.
   * - ``.csv``
     - Comma-separated values
     - Sehr gängiges Datenformat, das Daten mit Kommas oder anderen Trennzeichen separiert.

Bewährte Praktiken
==================

Das untenstehende Video gibt einen guten Überblick über Geodatenformate und bietet Tipps zur Dateibenennung und zu anderen bewährten Praktiken.

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/kggwFZHXCl4?si=i2lLEo0u0wGdB759" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>



Weitere Quellen
==================



+-----------------------------+----------------------------------------+
| Name                        | Welche Datensätze (u.a.)               |
+=============================+========================================+
| `Bundesamt für Kartographie | z.B. Verwaltungsgebiete für            |
| und                         | Deutschland                            |
| Geodäsie <                  |                                        |
| http://www.geodatenzentrum. |                                        |
| de/geodaten/gdz_rahmen.gdz_ |                                        |
| div?gdz_spr=deu&gdz_akt_zei |                                        |
| le=5&gdz_anz_zeile=1&gdz_un |                                        |
| t_zeile=0&gdz_user_id=0>`__ |                                        |
+-----------------------------+----------------------------------------+
| `USGS Earth                 | z.B. Landsat, Sentinel, SRTM, Aster,   |
| Explorer <https://          | Land Cover                             |
| earthexplorer.usgs.gov/>`__ |                                        |
+-----------------------------+----------------------------------------+
| `Humanitarian Data          | Infrastruktur, Bevölkerung, Wirtschaft |
| Exchange <ht                |                                        |
| tps://data.humdata.org/>`__ |                                        |
+-----------------------------+----------------------------------------+
| `Free GIS                   | eine Sammlung mit Links zu sehr vielen |
| Data <http://freegis        | Themenbereichen                        |
| data.rtwilson.com/#home>`__ |                                        |
+-----------------------------+----------------------------------------+
| `Pangaea <                  | Freie Daten zu                         |
| https://www.pangaea.de/>`__ | umweltwissenschaftlichen Themen        |
+-----------------------------+----------------------------------------+
| `SRTM                       | SRTM Höhendaten mit 90m Auflösung      |
| Data <http://srtm.          |                                        |
| csi.cgiar.org/srtmdata/>`__ |                                        |
+-----------------------------+----------------------------------------+
| `OpenAerialMap <htt         | Luft- und Sattelitenbilder weltweit    |
| ps://openaerialmap.org/>`__ | (z.B. HD mit 46m Auflösung)            |
+-----------------------------+----------------------------------------+
| `Copernicus & Land          | Hoch aufgelöste, europaweite           |
| Monitoring Service der      | Rasterdaten zu Besiedelung, Land       |
| EU <https://land.cop        | Cover, Wäldern, uvm.                   |
| ernicus.eu/pan-european>`__ |                                        |
+-----------------------------+----------------------------------------+
| `Global Human Settlement    | Globale Rasterdaten zu                 |
| Layer                       | Bevölkerungszahlen, Bebauung,          |
| <https://human-settlement.e | Gebäudehöhen uvm                       |
| mergency.copernicus.eu/>`__ |                                        |
+-----------------------------+----------------------------------------+
| `Open GeoData               | Geodatenportal des Landes              |
| BW <https://o               | Baden-Württemberg, u.a.                |
| pengeodata.lgl-bw.de/#/>`__ | hochaufgelöstes DGM, DTKs, …           |
+-----------------------------+----------------------------------------+

Nützliche Plugins
----------------------

- GeoBasis_Loader
- QuickOSM
- QuickMapServices


+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| Name                                                                                                                                       | Kurzbeschreibung Geodaten              | Maßstabsebene    |
+============================================================================================================================================+========================================+==================+
| `One Geology <https://onegeology.org/>`__                                                                                                  | Geoscience data via web services       | Weltweit         |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `Open Topography <https://portal.opentopography.org/datasets>`__                                                                           | High-resolution elevation data         | Weltweit         |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `Global Volcanism Program <https://volcano.si.edu/>`__                                                                                     | Volcanoes of the World database        | Weltweit         |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `European Geological Data Infrastructure <https://www.europe-geology.eu/>`__                                                               | Geological information across Europe   | Europa           |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `British Geological Survey <https://www.bgs.ac.uk/hosted-websites/>`__                                                                     | Sammlung von Geow. Programmen          | Weltweit         |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `USGS Earth Explorer <https://earthexplorer.usgs.gov/>`__                                                                                  | Download von SRTM & Landsat Daten      | Weltweit         |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `USGS Earthquakes <https://earthquake.usgs.gov/earthquakes/map/?extent=-45.08904,-173.67188&extent=84.9901,251.01563>`__                   | Download von Erdbeben                  | Weltweit         |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `PaleoClim <http://www.paleoclim.org/>`__                                                                                                  | Paleoklimatische Geodaten              | Weltweit         |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `Southern Permian Basin Atlas <https://www.nlog.nl/southern-permian-basin-atlas>`__                                                        | Geochemie permischer Gesteine          | Zentral Europe   |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `Bundesanstalt für Geowissenschaften und Rohstoffe <https://www.bgr.bund.de/DE/Themen/Geodatenmanagement/Geoportal/geoportal_node.html>`__ | Geodatenportal des BGR                 | Deutschland      |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `Geothermisches Informationssystem <https://www.geotis.de/geotisapp/geotis.php>`__                                                         | Geothermische Daten                    | Deutschland      |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `NIBIS Kartenserver <https://nibis.lbeg.de/cardomap3/>`__                                                                                  | Geofachdaten von Niedersachsen         | Niedersachsen    |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+
| `LGRB Kartenservice <https://maps.lgrb-bw.de/>`__                                                                                          | Geofachdaten zu BW                     | BW               |
+--------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------+------------------+


Deutschland und Europa
----------------------

-  Bundesamt für Kartographie und Geodäsie: https://gdz.bkg.bund.de/index.php/default/digitale-geodaten.html
-  Eurostat - Geographische Daten: https://ec.europa.eu/eurostat/de/web/gisco/geodata

Grenzen
-------

-  Deutschland: http://opendatalab.de/projects/geojson-utilities/#
-  Europa: https://ec.europa.eu/eurostat/de/web/gisco/geodata/reference-data/administrative-units-statistical-units/nuts
-  Weltweit: http://www.naturalearthdata.com/

OpenStreetMap
-------------

-  Geofabrik - OpenStreetMap Data Extracts:  http://download.geofabrik.de/
-  Overpass Turbo

   -  Allgemein: https://wiki.openstreetmap.org/wiki/Main_Page
   -  Tags: https://wiki.openstreetmap.org/wiki/Tags

Physische Geographie
--------------------

-  Bundesanstalt für Geowissenschaften und Rohstoffe (BGR)

   -  Geoviewer:
      https://www.bgr.bund.de/DE/Gemeinsames/Geoviewer/geoviewer_node.html
   -  Produkt Center: https://produktcenter.bgr.de/terraCatalog/Start.do

-  Wetter - DWD: https://cdc.dwd.de/portal/

Humangeographie
---------------

-  Bevölkerung: https://wopr.worldpop.org/
