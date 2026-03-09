QGIS Oberläche
===========================

Hier gehts zu den (aktuellen) Videos: 
`QGIS Nutzeroberfläche kennen lernen <https://giscience.github.io/gis-training-resource-center/content/Wiki/en_qgis_interface_wiki.html>`__



Übersicht
---------

.. figure:: https://raw.githubusercontent.com/GeowazM/gis-training-resource-heigit/refs/heads/main/fig/en_QGIS_GUI.png
   :alt: Übersicht GUI. © Copyright HeiGIT gGmbH

   Übersicht GUI. © Copyright HeiGIT gGmbH

| **1) Layers List / Browser Panel**
| Die Layer-Liste zeigt alle Layer/Dateien an, die im Projekt geladen
  sind. Man kann Layer einblenden/ausblenden und weitere Eigenschaften
  einstellen. Falls aus Versehen deaktiviert, über View-> Panels-> Layer
  wieder herstellen (s. `Anzeigen ein- und
  ausblenden <GUI#anzeigen-ein-und-ausblenden>`__).

| **2) Toolbars**
| Toolsbars sind *Shortcuts* um besonders häufig genutze Befehle
  auszuführen. So gibt es beispielsweise spezielle Toolbars für Vektor
  und Rasterdateien, aber auch allgemeine um z.B. euer Projekt zu
  speichern etc.

.. figure:: https://raw.githubusercontent.com/GeowazM/gis-training-resource-heigit/refs/heads/main/fig/Digitizing_Toolbar.png
   :alt: Toolbar- Beispiel Digitalisierung. © Copyright HeiGIT gGmbH

   Toolbar- Beispiel Digitalisierung. © Copyright HeiGIT gGmbH.

| **3) Kartenansicht**
| Die Kartenansicht ist der zentrale Bestandteil jedes GIS Programms. Hier werden die Geodaten angezeigt. Die Kartenansicht hat eine
  Projektion, welche nicht immer mit der Projektion der Layer übereinstimmen muss.

| **4) Status-Leiste**
| In der Status-Leiste findet ihr zentrale Informationen zur aktuellen Kartenansicht. Hier stellt ihr die Projektion der Kartenansicht ein
  und den Maßstab. Ihr könnt die Koordinaten des Mauszeigers ablesen und so schnell die Koordinaten von Punkten auf der Karte herausfinden. Ihr
  könnt eure Kartenansicht drehen, z.B. wenn ihr eine nach Süden ausgerichtete Karte erstellen möchtet.

| **5) Layer Styling Panel**
| Standardmäßig nicht angezeigt (s.\ `Anzeigen ein- und ausblenden <GUI#anzeigen-ein-und-ausblenden>`__). Ein einfacher Weg um
  die Darstellung von Layern zu modifizieren.

Verschieben der Kartenansicht
-----------------------------

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video/qgis_move.mp4">

.. raw:: html

   </video>

-  man kann auch mit den *Pfeiltasten* verschieben

Zoomen in der Kartenansicht
---------------------------

.. raw:: html

   <video width="90%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video/qgis_zoom.mp4">

.. raw:: html

   </video>

-  man kann auch durch *Scrollen* Zoomen
-  oder mit ``Ctrl+`` bzw. ``Ctrl-``

Eigenschaften von Objekten anzeigen
-----------------------------------

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video//qgis_identify.mp4">

.. raw:: html

   </video>

Projektion der Kartenansicht einstellen (Projekt-KBS)
-----------------------------------------------------

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video/qgis_map_projection.mp4">

.. raw:: html

   </video>

Projekt speichern und öffnen
----------------------------

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video/qgis_save_project.mp4">

.. raw:: html

   </video>

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video/qgis_open_project.mp4">

.. raw:: html

   </video>

| **Hinweis:**
| Die im Projekt verwendeten Layer-Daten werden nicht in der Projekt-Datei gespeichert. Stattdessen enthält die Projekt-Datei
  lediglich die Dateipfade, wo sich die Layer-Daten zum Zeitpunkt der letzten Abspeicherung des Projekts auf dem PC befunden haben. Sollte
  der Speicherort dieser Layer-Daten nachträglich verändert werden, kommt es bei erneuter Öffnung des Projektes zur Fehlermeldung “nicht
  verfügbare Layer behandeln”. Eine gute *Datenorganisation /Allgemeines/Datenorganisation* mit einer festen und durchdachten Ordnerstruktur verhindert solche Probleme.

Anzeigen ein- und ausblenden
----------------------------

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video/Anzeigen_einblenden_ausblenden.mp4">

.. raw:: html

   </video>

Toolbars verschieben und anordnen
---------------------------------

An jeder Toolbar gibt es ein Feld aus zwei gepunkteten Linien. Wenn man mit dem Mauszeiger hinüberfährt bis ein Pfeilkreuz erscheint und dann
die linke Maustaste gedrückt hält, kann man die Toolbar verschieben. Dies ermöglicht eine individualisierte Anordnung der eigenen Werkzeuge.
Durch die Komprimierung aller Toolbars in wenige Zeilen kann zudem noch das Fenster der Kartenansicht vergrößert werden.

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/Einfuehrung-GIS-fuer-Geowissenschaften/tree/master/source/img/video/qgis_arrange_toolbars.mp4">

.. raw:: html

   </video>

Erweiterungen (Plugins) installieren
------------------------------------

Für QGIS gibt es zahlreiche Erweiterungen, auch *Plugins* genannt, die
erweiterte Funktionalitäten zur Verfügung stellen.

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/qgis_plugins.mp4">

.. raw:: html

   </video>

| **Hinweis:**
| Solltet ihr eine spezifische Erweiterung nicht finden, überprüft eure
  Groß-/Kleinschreibung und die korrekte Verwendung von Leerzeichen.
  Sollte eine Erweiterung weiterhin nicht auffindbar sein, müssen
  eventuell die experimentellen Erweiterungen in den Optionen erlaubt
  werden (siehe unten).

Erweiterungen verwalten
-----------------------

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/Erweiterungen_verwalten.mp4">

.. raw:: html

   </video>

Experimentelle Erweiterungen erlauben
-------------------------------------

| Experimentelle Erweiterungen sind entweder noch in der Entwicklung,
  oder es handelt sich um veraltete Erweiterungen, die nicht mehr für
  die neueren Versionen von QGIS weiter optimiert/angepasst werden.
  Trotzdem kann die Verwendung experimenteller Erweiterungen sinnvoll
  sein:
| \* Spezifische Funktionen werden in keiner anderen Erweiterung
  unterstützt.
| \* Alternative, wenn es bei einer anderen Erweiterung zu Problemen
  kommt.
| \* Ein Tutorial greift auf eine bestimmte Erweiterung zurück.

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/Experimentelle_Erweiterungen.mp4">

.. raw:: html

   </video>

| **Hinweis:**
| Aufgrund der oftmals fehlenden Optimierung für die verwendete
  QGIS-Version, kann es bei experimentellen Erweiterungen vermehrt zu
  Fehlermeldungen oder anderen Problemen bis hin zum Absturz von QGIS
  kommen. Experimentelle Erweiterungen sollten daher sicherheitshalber
  nur für die Verwendung aktiviert und anschließend wieder deaktiviert
  werden. Vergewissert euch zusätzlich, dass der aktuelle
  Arbeitsfortschritt gespeichert ist, um einem Datenverlust beim Absturz
  von QGIS zu entgehen.

Weitere Ressourcen
==================

-  `QGIS-Doku: An Overview of the
   Interface <https://docs.qgis.org/3.4/de/docs/training_manual/introduction/overview.html>`__
