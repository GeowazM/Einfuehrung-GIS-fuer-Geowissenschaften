Digitalisierung
===============

Digitalisierung ist der Prozess der Umwandlung geografischer Daten aus Karten oder Bildern in eine digitale Form, die üblicherweise als Vektordaten dargestellt wird.
Während dieses Vorgangs werden räumliche Informationen aus Karten oder Bildern nachgezeichnet, wobei Punkte, Polylinien oder Polygone entstehen. 
Um Daten für einen neuen Datensatz zu digitalisieren, müssen Sie immer zuerst den Datensatz erstellen, bevor Sie ihn mit digitalisierten Daten füllen können.

Die Digitalisierungswerkzeugleiste in QGIS
==========================================

.. image:: https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/Digitizing_Toolbar.png

- Die Digitalisierung in QGIS erfolgt primär über die **Digitalisierungswerkzeugleiste**. Um diese zu aktivieren, navigieren Sie zu ``Ansicht`` -> ``Werkzeugleisten`` -> ``Digitalisierungswerkzeugleiste``.

.. figure:: https://raw.githubusercontent.com/GeowazM/gis-training-resource-heigit/refs/heads/main/fig/Toggle_editingbox.png
   :name: de_qgis_3.40_activate_digitisation_toolbar_wiki
   :width: 550 px

.. figure:: https://raw.githubusercontent.com/GeowazM/gis-training-resource-heigit/refs/heads/main/fig/en_qgis_3.40_activate_digitisation_toolbar_wiki.png
   :name: de_qgis_3.40_activate_digitisation_toolbar_wiki
   :width: 550 px


Basemaps hinzufügen 
========

QuickMapServices
----------------

-  Online-Karten (z.B. eines Tile Map Services) in die Kartenansicht
   einbetten
-  QuickMapServices Plugin installieren
-  eine Basemap auswählen und der Kartenansicht hinzufügen
-  (evtl. Projektion der Kartenansicht auf *Web Mercator* setzen)

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/MVMzDY2RqQU?si=pdr2BXrySGSdPEmC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


Einen neuen Layer erstellen
===========================

1. Navigieren Sie in der oberen Leiste zu ``Layer`` -> ``Layer erstellen`` -> ``Neuen GeoPackage-Layer erstellen...`` oder ``Neuen Shapefile-Layer erstellen...``.
2. Ein neues Fenster öffnet sich. Hier können Sie die Layer-Eigenschaften festlegen.
3. Klicken Sie unter ``Datenbank`` auf die drei Punkte |three_points| und navigieren Sie zu dem Ordner, in dem Sie den neuen Datensatz speichern möchten.
4. *Speziell für Shapefiles*: Stellen Sie die Dateikodierung auf ``UTF-8`` ein.
5. ``Geometrietyp``: Wählen Sie die Art der Geometrie, die Sie digitalisieren möchten: Punkte, Linien oder Polygone.

.. margin::

   .. tip::
      Wenn Sie planen, entfernungsbasierte Berechnungen mit dem neuen Datensatz durchzuführen, stellen Sie sicher, dass Sie ein **metrisches** KBS (Koordinatenbezugssystem) verwenden. Die Maßeinheiten für den Layer sind dann in Metern und nicht in Grad (siehe `Metrische und geografische Koordinatenbezugssysteme <https://giscience.github.io/gis-training-resource-center/content/Module_2/en_qgis_projections.html#metric-and-geographic-coordinate-reference-systems>`_).

6. Wählen Sie das KBS (Koordinatenbezugssystem), das Sie für den neuen Layer verwenden möchten. Standardmäßig ist das Projekt-KBS eingestellt. Wenn Sie das KBS ändern möchten, klicken Sie auf |mIconProjectionEnabled|.
7. Unter ``Neues Feld`` können Sie dem neuen Layer Spalten hinzufügen. Hier definieren Sie, welche Art von Informationen/Daten in der Attributtabelle für jedes Objekt verfügbar sein werden.
   
   - ``Name``: Geben Sie der neuen Spalte einen Namen, der die Informationen repräsentiert, die Sie darin speichern möchten.
   - ``Typ``: Hier können Sie den Datentyp für die neue Spalte auswählen. Beispielsweise fügt ``Text (String)`` eine neue Spalte mit Textdaten hinzu. Für numerische Daten können Sie ``Ganze Zahl (Integer)`` oder ``Dezimalzahl (Real)`` wählen.
   - ``Maximale Länge`` definiert die maximale Anzahl von Zeichen, die das Feld haben kann. Dies ist relevant für die Textlänge oder die Genauigkeit von Dezimalzahlen. Beispielsweise sollten Sie eine hohe maximale Länge für Textfelder festlegen, wenn Sie lange Straßennamen wie "Martin Luther King Jr. Boulevard" (34 Zeichen) erwarten.
   - Klicken Sie auf |mActionNewAttribute|, um die neue Spalte zur ``Feldliste`` hinzuzufügen.

8. Sobald Sie alle Felder hinzugefügt haben, klicken Sie auf ``OK``.

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/en_qgis_create_layer.mp4"></video>


Geometrien zu einem Layer hinzufügen
===================================

Punktdaten erstellen
--------------------

1. Wählen Sie im Layer-Bedienfeld den Punkt-Layer aus, dem Sie Daten hinzufügen möchten.
2. Gehen Sie zur Digitalisierungswerkzeugleiste und klicken Sie auf **den gelben Stift**. Nun befindet sich der Layer im Bearbeitungsmodus.
3. Klicken Sie auf die **blauen Punkte**.
4. Klicken Sie mit der linken Maustaste auf das Objekt, das Sie digitalisieren möchten.
5. Sobald Sie klicken, erscheint ein Fenster mit dem Namen ``[Ihr Layer-Name] - Objektattribute``. Hier können Sie die Informationen zu diesem Objekt in die verschiedenen Spalten eintragen, basierend auf der Attributtabelle des Layers.

.. figure:: https://raw.githubusercontent.com/GeowazM/gis-training-resource-heigit/refs/heads/main/fig/New_point_creation_data.png 
   :width: 700px
   :name: point_creation
   :align: center

.. 
   Add another picture with more columns

6. Sobald Sie mit der Digitalisierung fertig sind, klicken Sie auf |mActionSaveEdits|, um Ihre Änderungen zu speichern.
7. Klicken Sie erneut auf |mActionToggleEditing|, um den Bearbeitungsmodus zu beenden.

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/Creat_point_feature.mp4"></video>


Liniendaten erstellen
---------------------

Die Methode ähnelt der Digitalisierung eines Punktes (siehe oben). Zuerst müssen Sie einen neuen Linien-Layer erstellen oder einen bestehenden verwenden.

.. attention:: 
   Wenn Sie einen neuen Linien-Layer erstellen, denken Sie daran, den Geometrietyp auf Linien zu ändern, da wir nun Liniendaten erstellen.

1. Wählen Sie im Layer-Bedienfeld den Linien-Layer aus, dem Sie Daten hinzufügen möchten.
2. Klicken Sie in der Digitalisierungswerkzeugleiste auf |mActionToggleEditing|. Nun befindet sich der Layer im Bearbeitungsmodus.
3. Klicken Sie auf |mActionCaptureLine|.
4. Erstellen Sie die Linie in der Kartenansicht, indem Sie mit einem :kbd:`Linksklick` Stützpunkte hinzufügen. Wenn Sie fertig sind, machen Sie einen Rechtsklick auf den letzten Punkt, um die Bearbeitung der Geometrie abzuschließen.
5. Ein neues Fenster mit dem Titel ``[Ihr Layer-Name] - Objektattribute`` wird angezeigt. Hier können Sie die Spalteninformationen für das Objekt ausfüllen.  
6. Sobald Sie mit der Digitalisierung fertig sind, klicken Sie auf |mActionSaveEdits|, um Ihre Änderungen zu speichern.
7. Klicken Sie erneut auf das Symbol |mActionToggleEditing|, um den Bearbeitungsmodus zu beenden.

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/Creat_line_feature.mp4"></video>


Polygondaten erstellen 
----------------------

1. Wählen Sie im Layer-Bedienfeld den Polygon-Layer aus, dem Sie Daten hinzufügen möchten.
2. Klicken Sie auf |mActionToggleEditing|, um den Bearbeitungsmodus zu starten.
3. Klicken Sie auf ``Polygon digitalisieren`` |mActionCapturePolygon|, um Polygone hinzuzufügen.
4. Zeichnen Sie ein Polygon in der Kartenansicht mit einem :kbd:`Linksklick`. Ein :kbd:`Rechtsklick` beendet die Polygon-Erstellung und verbindet den ersten und den letzten hinzugefügten Punkt. 
5. Ein neues Fenster öffnet sich. Hier können Sie die Spalteninformationen für dieses Objekt hinzufügen. 
6. Speichern Sie die Änderungen durch Klicken auf das Symbol |mActionSaveEdits| und beenden Sie den Bearbeitungsmodus, indem Sie auf das Symbol |mActionToggleEditing| klicken. 

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/en_qgis_digitize_add_feature.mp4"></video>


Bestehende Geometrien ändern
============================

1. Wählen Sie im Layer-Bedienfeld den Layer mit der Geometrie, die Sie bearbeiten möchten, durch Anklicken aus. Er wird blau hervorgehoben.
2. Klicken Sie in der Digitalisierungswerkzeugleiste auf |mActionToggleEditing|, um den Bearbeitungsmodus zu starten.
3. Klicken Sie in der Digitalisierungswerkzeugleiste auf |qgis_3.40_vertex_tool|. Nun können Sie die Stützpunkte von Geometrien verschieben und bearbeiten.
4. Wenn Sie fertig sind, vergessen Sie nicht, den Bearbeitungsmodus durch Klicken auf |mActionToggleEditing| zu beenden und Ihre Änderungen zu speichern. 

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/en_qgis_digitize_move_vertices.mp4"></video>


Ring zu bestehendem Polygon-Layer hinzufügen
--------------------------------------------

In QGIS erfolgt das Hinzufügen von Ringen zu Polygonen mit der "Erweiterten Digitalisierungswerkzeugleiste". Um die Werkzeugleiste zu aktivieren, navigieren Sie zu ``Ansicht`` -> ``Werkzeugleisten`` -> ``Erweiterte Digitalisierungswerkzeugleiste``.

.. image:: https://raw.githubusercontent.com/GeowazM/gis-training-resource-heigit/refs/heads/main/fig/Toolbox.png

1. Klicken Sie auf |mActionToggleEditing|, um den Bearbeitungsmodus eines Polygon-Layers zu starten.
2. Klicken Sie auf |mActionAddRing| (z. B. um den Innenhof eines Gebäudes zu kartieren oder - wie im Video gezeigt - einen Kreis zu erstellen, um eine Insel im See zu markieren).

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/en_qgis_digitize_add_ring.mp4"></video>


Weitere Ressourcen
==================

Das untenstehende YouTube-Video zeigt den gesamten Prozess der Digitalisierung von Polygonen in QGIS etwas detaillierter. Beachten Sie, dass die Person im Video eine ältere QGIS-Version verwendet, weshalb einige Dinge in Ihrer Version anders aussehen könnten.

.. raw:: html

   <iframe width="560" height="315" src="https://youtu.be/embed/Zer558SnKX4?si=ELKStx6y5_B_ilRe" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

.. 
   Hier werden die Inline-Bilder als Substitutions definiert, damit sie oben im Text korrekt eingefügt werden.

.. |three_points| image:: /fig/Three_points.png
.. |mIconProjectionEnabled| image:: /fig/mIconProjectionEnabled.png
.. |mActionNewAttribute| image:: /fig/mActionNewAttribute.png
.. |mActionToggleEditing| image:: /fig/mActionToggleEditing.png
.. |mActionCapturePoint| image:: /fig/mActionCapturePoint.png
.. |mActionSaveEdits| image:: /fig/mActionSaveEdits.png
.. |mActionCaptureLine| image:: /fig/mActionCaptureLine.png
.. |mActionCapturePolygon| image:: /fig/mActionCapturePolygon.png
.. |qgis_3.40_vertex_tool| image:: /fig/qgis_3.40_vertex_tool.png
.. |mActionAddRing| image:: /fig/mActionAddRing.png