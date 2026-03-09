Copy paste
=================


==============================
Projekte und Ordnerstruktur
==============================

**🔙** `Zurück zur Startseite </content/intro.md>`_

Dieser Wiki-Artikel behandelt die bewährten Methoden für die Erstellung und Verwaltung von Geodaten und QGIS-Projekten.

Schritt-für-Schritt: Ein neues QGIS-Projekt von Grund auf einrichten
====================================================================

.. tip::
   Es hat sich bewährt, eine **Standard-Ordnerstruktur** für QGIS-Projekte zu verwenden, in der das Projekt, alle verwendeten Geodaten, Stil-Dateien und die Dokumentation gespeichert werden. 
1. Kopieren Sie die Standard-Ordnerstruktur für QGIS-Projekte an den Ort, an dem Sie Ihr gesamtes Projekt speichern möchten. Sie können die Standard-Ordnerstruktur *hier* herunterladen.
2. Öffnen Sie QGIS und erstellen Sie ein neues Projekt. Klicken Sie auf ``Projekt`` -> ``Neu``.

Ein neues QGIS-Projekt erstellen
--------------------------------

.. raw:: html

   <video width="100%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_new_project.mp4"></video>

3. Speichern Sie das neue Projekt im Ordner ``Project`` innerhalb der Standard-Ordnerstruktur und führen Sie einen Git Push durch.
4. Geben Sie Ihrem Projekt einen Namen und klicken Sie.

.. tip::
   Verwenden Sie keine Leerzeichen `` `` im Namen, sondern immer Unterstriche ``_``.

Projekt speichern
-----------------

.. raw:: html

   <video width="100%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_save_as.mp4"></video>

4. Überprüfen Sie das Koordinatenbezugssystem (KBS)/den EPSG-Code des Projekts und passen Sie es an das KBS/den EPSG-Code an, den Sie verwenden möchten. Weitere Informationen finden Sie im Wiki-Artikel zu `Projektionen <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_projections_wiki.html#how-to-check-epsg-code-crs-of-your-qgis-project-and-change-it>`_.

KBS/EPSG überprüfen und ändern
------------------------------

.. raw:: html

   <video width="100%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_change_project_CRS.mp4"></video>

.. tip::
   Die im Projekt verwendeten Layer-Daten werden nicht in der Projektdatei gespeichert. Stattdessen enthält die Projektdatei nur die Dateipfade, an denen sich die Layer-Daten zu dem Zeitpunkt befanden, als das Projekt zuletzt auf dem PC gespeichert wurde. Wenn der Speicherort dieser Layer-Daten nachträglich geändert wird, erscheint beim erneuten Öffnen des Projekts die Fehlermeldung "Nicht verfügbare Layer handhaben". Eine gute Datenorganisation mit einer festen und durchdachten Ordnerstruktur verhindert solche Probleme.

Bestehende QGIS-Projekte öffnen
===============================

Öffnen Sie QGIS -> ``Projekt`` -> ``Öffnen`` -> Wählen Sie Ihr Projekt aus.

**QGIS-Projekt öffnen**

.. raw:: html

   <video width="100%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_open_project.mp4"></video>

Standard-Ordnerstruktur
=======================

Die Standard-Ordnerstruktur hat zwei wesentliche Vorteile:

1. Durch die Weitergabe des gesamten Projektordners können wir sicher sein, dass das Projekt auch auf einem anderen Computer problemlos läuft.
2. Die Ordnerstruktur unterstützt die ordnungsgemäße Organisation von Geodaten und gewährleistet die stabile Funktion eines QGIS-Projekts.

Die Vorlage für die Ordnerstruktur kann `hier <https://github.com/GIScience/gis-training-resource-center/blob/main/fig/GIS_Project_folder_template.zip>`_ heruntergeladen werden.

.. figure:: /fig/Standard_project_folder_structure.drawio.svg
   :width: 800px
   :align: center
   :name: Standard_project_folder_structure_wikki

   Standard-Ordnerstruktur. Quelle: HeiGIT

---

.. _attribute_table_de:

======================
Attributtabelle in QGIS
======================

**🔙** `Zurück zur Startseite </content/intro.md>`_

Die Attributtabelle, eine Kernkomponente von Geoinformationssystemen (GIS), **organisiert und präsentiert** detaillierte Informationen über Objekte in einem ausgewählten Layer.  Jede **Zeile** in der Tabelle repräsentiert ein **Objekt**, während die **Spalten** spezifische **Attribute** speichern. Diese Tabelle erleichtert das Suchen, Auswählen, Sortieren, Filtern und Bearbeiten von Objekten.

.. figure:: /fig/attribute_table.png
   :width: 600 px
   :name: attribute_table_wiki

   Beispiel einer Attributtabelle in QGIS.

Grundlagen der Attributtabelle
==============================

Die Attributtabelle öffnen und Objekte sortieren
------------------------------------------------

* **Attributtabelle öffnen:** Klicken Sie mit der rechten Maustaste auf Ihren Layer und wählen Sie ``Attributtabelle öffnen``.
* **Spalte sortieren:** Klicken Sie auf eine Spaltenüberschrift.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_show_attribute_table.mp4"></video>

Objekte in der Attributtabelle manuell auswählen
------------------------------------------------

* **Auswählen:** Klicken Sie auf die Zeilen der Objekte.
* **Mehrfachauswahl:** Um mehrere Objekte auszuwählen, drücken Sie :kbd:`Strg` (:kbd:`Cmd` auf MacOS) und wählen Sie die ``Objekte`` aus.
* **Nur ausgewählte Objekte anzeigen:** Öffnen Sie unten links in der Attributtabelle das Dropdown-Menü und wählen Sie ``Ausgewählte Objekte anzeigen``. Um wieder alle Objekte anzuzeigen, klicken Sie auf ``Alle Objekte anzeigen``.
* **Nur nicht ausgewählte Objekte anzeigen:** Wählen Sie Objekte aus und klicken Sie auf |mActionInvertSelection|.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_attribute_table_select.mp4"></video>

Objektauswahl aufheben
----------------------

* **Auswahl aufheben:** Klicken Sie auf |mActionDeselectActiveLayer| oder verwenden Sie :kbd:`Strg` + :kbd:`Umschalt` + :kbd:`A`.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_attribute_table_unselect.mp4"></video>

Auf ein bestimmtes Objekt zoomen
--------------------------------

* **Zoomen:** Klicken Sie mit der rechten Maustaste auf Ihr Objekt und wählen Sie ``Auf Objekt zoomen``.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_zoom_to_feature.mp4"></video>

Tabellenansicht vs. Formularansicht
===================================

QGIS bietet zwei Ansichten zur einfachen Bearbeitung von Daten in der Attributtabelle:

* **Tabellenansicht:** |mActionOpenTable| Dieser Modus zeigt die Werte mehrerer Objekte in einem tabellarischen Format an, wobei jede Zeile einem Objekt und jede Spalte einem Feld entspricht.
* **Formularansicht:** |mActionFormView| Dieser Modus zeigt alle Attribute *eines* ausgewählten Objekts an.

Um zwischen diesen Modi zu wechseln, verwenden Sie die Schaltflächen |mActionFormView| |mActionOpenTable| in der unteren rechten Ecke der Attributtabelle.

Attributtabelle - Datenbearbeitung
==================================

Daten in der Attributtabelle ändern
-----------------------------------

* **Attributtabelle öffnen:** Klicken Sie mit der rechten Maustaste auf Ihren Layer und wählen Sie ``Attributtabelle öffnen``.
* **Daten bearbeiten:** Aktivieren Sie den Bearbeitungsmodus, indem Sie auf |mActionToggleEditing| klicken.
  - Navigieren Sie zu dem Objekt und wählen Sie das Attribut aus, das Sie bearbeiten möchten.
  - Nehmen Sie Ihre Änderungen vor.
* **Änderungen speichern:** Klicken Sie auf |mActionSaveEdits| **oder** deaktivieren Sie den Bearbeitungsmodus durch Klick auf |mActionToggleEditing| und bestätigen Sie die Änderungen, indem Sie Ihren Layer speichern.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/Attributtabel_edit.mp4"></video>

Eine neue Spalte hinzufügen
---------------------------

* **Neue Spalte hinzufügen:** Aktivieren Sie den Bearbeitungsmodus, indem Sie auf |mActionToggleEditing| klicken -> klicken Sie auf |mActionNewAttribute|, das Fenster ``Feld hinzufügen`` öffnet sich.
* **Spaltenvariablen festlegen:** Füllen Sie das Fenster aus und klicken Sie auf ``OK``.
  * ``Name`` = Name der Spalte.
  * ``Kommentar`` = Zusätzliche Informationen zur Spalte.
  * ``Typ`` = Wählen Sie die Art der Daten, die die Spalte enthalten soll. Tabelle der Datentypen unten.

.. list-table:: Datentypen
   :widths: 30 70
   :header-rows: 1

   * - Typ
     - Eigenschaft
   * - Ganze Zahl (Integer)
     - Ganze Zahlen wie Anzahlen, Mengen oder IDs.
   * - Ganze Zahl (Integer 64-bit)
     - Größere ganze Zahlen für sehr große Anzahlen.
   * - Dezimalzahl (Real)
     - Zahlen mit Dezimalstellen, nützlich für Messungen und Brüche.
   * - Text (String)
     - Alphanumerische Zeichen, wie Namen und Beschreibungen.
   * - JSON (String)
     - Strukturierte Textdaten, oft für komplexe Informationen genutzt.
   * - Datum
     - Spezifische Kalenderdaten.
   * - Datum & Zeit
     - Datum und Uhrzeit zusammen.
   * - Binärobjekt (BLOB)
     - Zum Speichern binärer Daten wie Bilder, Audio oder Dateien.
   * - Boolean
     - Einfache Wahr/Falsch- oder Ja/Nein-Werte.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_add_column.mp4"></video>

Spalten löschen
---------------

* **Spalte löschen:** Aktivieren Sie den Bearbeitungsmodus, indem Sie auf |mActionToggleEditing| klicken.
  - Klicken Sie auf |mActionDeleteAttribute|.
  - Wählen Sie die Spalten aus, die Sie löschen möchten.
  - Klicken Sie auf ``OK``.
  - Klicken Sie auf |mActionSaveEdits|.

.. hint::
   Um mehrere Spalten auszuwählen, drücken Sie :kbd:`Strg` und wählen Sie die Spalten an.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/qgis_delet_column.mp4"></video>

---

.. _automation_qgis_de:

================================================
Automatisierung in QGIS (Der Model Builder)
================================================

**🔙** `Zurück zur Startseite </content/intro.md>`_

Warum Automatisierung?
======================

Automatisierung vereinfacht Aufgaben, indem sie den Aufwand für den Benutzer verringert und Fehler durch weniger manuelle Wiederholungen minimiert. Sie ermöglicht Modularisierung, verbessert die Wiederverwendbarkeit und reduziert Redundanz durch die wiederholte Nutzung eines definierten Sets benötigter Werkzeuge. In QGIS lässt sich dies mit dem "Model Designer" (Modellierungswerkzeug) erreichen. 
Der QGIS Model Designer
=======================

Der Model Designer ist ein visuelles Werkzeug, mit dem Benutzer einen Workflow mit allen in QGIS verfügbaren Werkzeugen erstellen und bearbeiten können, der sich einfach und zeiteffizient wiederholt anwenden lässt. Er bietet eine grafische Oberfläche, um Workflows durch die Verbindung von Geoverarbeitungswerkzeugen und Algorithmen aufzubauen. Der Benutzer kann Eingaben, Ausgaben und den Datenfluss zwischen verschiedenen Verarbeitungsschritten definieren.

Nutzung des Model Designers/Grafischen Modellierers
---------------------------------------------------

- Öffnen Sie das Werkzeug unter ``Verarbeitung`` -> ``Grafische Modellierung...``.
- Speichern Sie die Modelldatei in einem Ordner Ihrer Wahl, indem Sie in der oberen Leiste auf die Schaltfläche |qgis_save_project_as| ``Modell speichern als...`` klicken.
- Öffnen Sie ein bestehendes Modell über ``Modell`` -> ``Modell öffnen...`` und navigieren Sie zur Modelldatei.

.. raw:: html

   <video width="100%" controls src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/en_qgis_3.40_open_model_file.mp4"></video>

Modell-Komponenten
------------------

Es gibt zwei Arten von Modellkomponenten, die Sie zum Erstellen von Workflows verwenden können:

**Eingaben (Inputs):** Das Modell beginnt mit Eingabedaten. Dies können Vektor-Layer, Raster-Layer, CSV-Dateien oder sogar Werte oder Ausdrücke sein. Meistens werden Sie Layer als Eingaben verwenden.

**Algorithmen:** Die Verarbeitungsschritte bestehen aus Algorithmen oder Werkzeugen, die in QGIS verfügbar sind, wie z.B. Zuschneiden (Clipping), Umprojizieren, Verbinden nach Attributwerten usw.

Ein Modell erstellen
--------------------

**Eingaben hinzufügen**

- Sie können dem Modell Eingaben über den Reiter ``Eingaben`` auf der linken Seite des Model Builder-Fensters hinzufügen, indem Sie entweder einen :kbd:`Doppelklick` darauf ausführen oder sie auf die Arbeitsfläche des Model Builders ziehen.
- Nach dem Hinzufügen öffnet sich ein neues Fenster, in dem Sie die Beschreibung der Eingabe (die als Titel erscheint) sowie den Geometrietyp für Vektordaten festlegen und auswählen können, ob es sich um eine obligatorische oder optionale Eingabe für den Workflow handelt.

.. raw:: html

   <video width="100%" controls src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/en_qgis_3.40_model_adding_inputs.mp4"></video>

**Verarbeitungsschritte hinzufügen:**

- Im Panel ``Algorithmen`` auf der linken Seite des Model Builder-Fensters können Sie Verarbeitungsschritte oder Algorithmen aus den QGIS-Verarbeitungswerkzeugen auswählen. Zum Beispiel das "Puffer"-Werkzeug zum Puffern eines Straßennetzwerks mit einem Radius von 500 Metern.
- Um einen Algorithmus hinzuzufügen, machen Sie einfach einen :kbd:`Doppelklick` darauf oder ziehen Sie ihn auf die Arbeitsfläche.
- Nach dem Hinzufügen öffnet sich das Parameterfenster des Algorithmus. Es sieht dem normalen Parameterfenster für diesen Algorithmus ähnlich, mit ein paar Ausnahmen:
  1. Sie können eine Beschreibung hinzufügen.
  2. Sie müssen den ``Eingabelayer`` entweder als Modelleingabe oder als Ausgabe eines anderen Algorithmus im Modell definieren.
  3. Die Ausgabe des Algorithmus kann als Modellausgabe definiert werden, indem Sie einen Namen eingeben.
  - Abhängig vom Algorithmus können noch andere Unterschiede auftreten.

.. figure:: /fig/en_qgis_3.40_model_adding_algorithms.png
   :width: 500 px
   :name: en_qgis_3.40_model_adding_algorithms

   Die Parameterseite für den "Puffer"-Algorithmus im Model Builder.

- Sobald Sie die Parameter festgelegt haben, klicken Sie auf ``OK``.

.. raw:: html

   <video width="100%" controls src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/en_qgis_3.40_model_adding_algorithms.mp4"></video>

**Weitere Verarbeitungsschritte hinzufügen**

- Sie können mehrere Algorithmen verketten, indem Sie ``Algorithmusausgabe`` für den ``Eingabelayer`` wählen und eine Ausgabe eines vorherigen Algorithmus auswählen.

**Ausführen des Modells**

Um das Modell auszuführen, klicken Sie auf den grünen Pfeil in der oberen Leiste, ein neues Fenster öffnet sich, in dem Sie Ihre Eingaben eingeben/spezifizieren müssen, dann klicken Sie auf "Starten". Ausgabe-Layer werden automatisch zu Ihrer QGIS-Projektansicht hinzugefügt.

Sobald Sie die Erstellung Ihres Workflows abgeschlossen haben oder das Ergebnis Ihres Modells testen möchten, können Sie das Modell ausführen. Dies führt automatisch alle Verarbeitungsschritte aus, die Sie in die grafische Modellierung eingegeben haben, und erstellt Layer in Ihrem QGIS-Projekt für die definierten Ausgaben:

- Klicken Sie in der oberen Leiste des Model Builder-Fensters auf die Schaltfläche |qgis_3.40_run_model| ``Modell ausführen``.
- Ein neues Fenster öffnet sich; hier definieren Sie, welche Layer Ihres QGIS-Projekts als Eingabelayer für Ihr Modell fungieren sollen.
- Klicken Sie auf ``Starten``. Nach Abschluss erscheinen die berechneten oder verarbeiteten Layer in Ihrer QGIS-Hauptkartenansicht.

---

.. _basemaps_de:

===============================
Hintergrundkarten (Basemaps)
===============================

**🔙** `Zurück zur Startseite </content/intro.md>`_

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

   <video width="100%" controls src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/Add_basemap_OSM.mp4"></video>

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

---

.. _types_of_geodata_de:

==============================
Arten von Geodaten
==============================

**🔙** `Zurück zur Startseite </content/intro.md>`_

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

---

.. _single_symbol_de:

==============================
Einzelsymbol-Klassifizierung
==============================

**🔙** `Zurück zur Startseite </content/intro.md>`_

- Standardmäßig visualisiert QGIS alle Layer in der Einstellung ``Einzelsymbol``.
- Das bedeutet, dass alle Objekte eines Layers gleich visualisiert werden.
- In dieser Einstellung können Sie viele Parameter wie Farbe oder Deckkraft ändern, **aber Sie können keine Daten klassifizieren!**

**Um den Stil eines Layers anzupassen...**
- Klicken Sie mit der rechten Maustaste auf Ihren Layer.
- Klicken Sie auf ``Eigenschaften`` (Symbologie).
- Bestätigen Sie, dass die Layer-Einstellung auf ``Einzelsymbol`` steht.
- Wählen Sie im Dropdown-Menü die Farbe Ihrer Wahl. Für weitere Farboptionen wählen Sie im Dropdown-Menü ``Farbe wählen``.
- *Optional:* Sie können die Deckkraft/Transparenz des Layers anpassen. Dies kann sehr nützlich sein, wenn Sie mehrere sich überschneidende Layer anzeigen möchten.
- *Optional:* Hier können Sie den Einheitentyp festlegen. Dies ist nützlich, wenn Sie beispielsweise Punkte in einer bestimmten Größe visualisieren möchten.
- *Optional:* Hier können Sie Standard- und zuvor verwendete Stile schnell finden.
- Klicken Sie auf ``Anwenden``, um Ihre Anpassungen wirksam zu machen.
- Klicken Sie auf ``OK``, um das Fenster zu schließen.

.. figure:: /fig/Single_symbol_classify.png
   :width: 900px
   :name: Single_symbol_classify_wiki
   :align: center

.. raw:: html

   <video width="900%" controls src="https://github.com/GIScience/gis-training-resource-center/raw/main/fig/Single_symbol_video.mp4"></video>

---

.. _qgis_basics_de:

==============================
QGIS Grundlagen
==============================

**🔙** `Zurück zur Startseite </content/intro.md>`_

Unterabschnitte:
================

* `Installation von QGIS <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_installation_wiki.html>`_
* `QGIS Benutzeroberfläche <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_interface_wiki.html>`_
* `Projekte und Ordnerstruktur <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_projects_folder_structure_wiki.html>`_
* `Projektionen <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_projections_wiki.html>`_
* `Hintergrundkarten <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_basemaps_wiki.html>`_
* `Plugins (Erweiterungen) <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_plugins_wiki.html>`_
* `Datenquellen <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_data_sources_wiki.html>`_