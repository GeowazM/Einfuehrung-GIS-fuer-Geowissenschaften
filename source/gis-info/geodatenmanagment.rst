Geodatenmanagment
=================

Im Rahmen der Aufgaben werden eine Vielzahl von Daten heruntergeladen. Eine ordentliche Verwaltung beugt nicht nur Fehlern und Komplikationen
vor, sondern schafft auch eine bessere Übersichtlichkeit in der ihr eure Daten schnell wiederfinden könnt.

Speicherort
-----------

Die GIS-Dateien sollten auf einem lokalen Speichermedium abgelegt werden, um schnelle Abläufe zu gewährleisten und Komplikationen zu
vermeiden. Vom Speichern der Daten in einem Cloud-Server wird abgeraten, da dies durch fehlerhafte Datenzugriffe eures GIS Programms zu
Fehlermeldungen oder einfrierenden Programmen führen kann (siehe dazu auch “Umlaute/Sonderzeichen/Leerzeichen in Dateipfaden” auf der Seite `Hinweise <ttps://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/gis-info/hinweise.html>`__).

Datenbenennung
--------------

Wie bereits in den `Hinweisen <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/gis-info/hinweise.html>`__ beschrieben, können bestimmte Schriftzeichen zu Fehlern in der
Verarbeitung von Daten durch euer GIS Programm führen. Sowohl der Dateipfad, unter dem die GIS-Daten gespeichert werden, als auch die
Namen der Daten selbst sollten daher keine Leerzeichen, Sonderzeichen oder Umlaute(ä,ö,ü) enthalten. Versucht zudem eure Datennamen kurz zu
halten. Zum einen werden dadurch Fehlerquellen reduziert. Zum Anderen muss für lange Datennamen die `Layers
List <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/gis-info/nutzeroberflaeche.html>`__
verbreitert werden, um den vollständigen Namen lesen zu können. Dies reduziert die Größe der
`Kartenansicht <https://giscience.courses-pages.gistools.geog.uni-heidelberg.de/qgis-book//content/karto/layerkonzept/Layer.html>`__
und somit die Übersichtlichkeit beim Arbeiten im GIS Programm (siehe dazu auch “Umlaute/Sonderzeichen/Leerzeichen in Dateipfaden” auf der
Seite `Hinweise <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/gis-info/hinweise.html>`__).

Ordnerstruktur
--------------

Eine gute und übersichtliche Ordnerstruktur erleichtert das Arbeiten mit GIS Programmen enorm. Legt euch daher am besten noch vor dem ersten
Tutorium Ordner für die Dateien an, mit denen ihr im Laufe des Semesters arbeiten werdet. Achtet darauf die Dateipfade nicht zu lang werden zu
lassen, um Komplikationen zu vermeiden. Wir empfehlen dabei folgende Struktur:

Dokumente/studium/geo/gis/ex0/

In diesem Ordner dann jeweils Unterordner input, interim und output (keine Umlaute) in denen ihr jeweils alle benötigten Daten speichern könnt.

Im Rahmen der Kartographie Übung werden neben den Eingangsdaten, die in diesem GitLab Repository verfügbar sind und runtergeladen werden sollen
eigentlich nur die QGIS Projektdateien eine Rolle spielen. Um die sich eine saubere Struktur anzugewöhnen ist die Empfehlung trotzdem, Daten
und Projektdateien in separten Ordnern *daten/* und *projekte/* abzulegen.

Somit würde der Teil des Dateisystems für die Übung z.B. wie folgt aussehen:

.. figure:: https://github.com/GeowazM/gis-training-resource-heigit/blob/main/fig/Standard_project_folder_structure.drawio.svg
   :alt: Screenshot_from_2021-08-13_08-43-20

   Screenshot_from_2021-08-13_08-43-20

**Hinweis:** Achtet bei der Ordnerstruktur darauf diese nachträglich nicht zu verändern.


Projekte
--------------

Dieser Wiki-Artikel behandelt die bewährten Methoden für die Erstellung und Verwaltung von Geodaten und QGIS-Projekten.

Schritt-für-Schritt: Ein neues QGIS-Projekt von Grund auf einrichten
--------------

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

.. figure:: https://github.com/GeowazM/gis-training-resource-heigit/blob/main/fig/Standard_project_folder_structure.drawio.svg
   :width: 800px
   :align: center
   :name: Standard_project_folder_structure_wikki

   Standard-Ordnerstruktur. Quelle: HeiGIT

