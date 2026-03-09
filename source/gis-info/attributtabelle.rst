======================
Attributtabelle in QGIS
======================

Die Attributtabelle, eine Kernkomponente von Geoinformationssystemen (GIS), **organisiert und präsentiert** detaillierte Informationen über Objekte in einem ausgewählten Layer.  Jede **Zeile** in der Tabelle repräsentiert ein **Objekt**, während die **Spalten** spezifische **Attribute** speichern. Diese Tabelle erleichtert das Suchen, Auswählen, Sortieren, Filtern und Bearbeiten von Objekten.

.. figure:: https://raw.githubusercontent.com/GeowazM/gis-training-resource-heigit/refs/heads/main/fig/en_vector_data_overview.png
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

   <video width="90%" controls muted src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/qgis_show_attribute_table.mp4"></video>

Objekte in der Attributtabelle manuell auswählen
------------------------------------------------

* **Auswählen:** Klicken Sie auf die Zeilen der Objekte.
* **Mehrfachauswahl:** Um mehrere Objekte auszuwählen, drücken Sie :kbd:`Strg` (:kbd:`Cmd` auf MacOS) und wählen Sie die ``Objekte`` aus.
* **Nur ausgewählte Objekte anzeigen:** Öffnen Sie unten links in der Attributtabelle das Dropdown-Menü und wählen Sie ``Ausgewählte Objekte anzeigen``. Um wieder alle Objekte anzuzeigen, klicken Sie auf ``Alle Objekte anzeigen``.
* **Nur nicht ausgewählte Objekte anzeigen:** Wählen Sie Objekte aus und klicken Sie auf |mActionInvertSelection|.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/qgis_attribute_table_select.mp4"></video>

Objektauswahl aufheben
----------------------

* **Auswahl aufheben:** Klicken Sie auf |mActionDeselectActiveLayer| oder verwenden Sie :kbd:`Strg` + :kbd:`Umschalt` + :kbd:`A`.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GIScience/GeowazM/gis-training-resource-heigit/raw/main/fig/qgis_attribute_table_unselect.mp4"></video>

Auf ein bestimmtes Objekt zoomen
--------------------------------

* **Zoomen:** Klicken Sie mit der rechten Maustaste auf Ihr Objekt und wählen Sie ``Auf Objekt zoomen``.

.. raw:: html

   <video width="90%" controls muted src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/qgis_zoom_to_feature.mp4"></video>

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

   <video width="90%" controls muted src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/Attributtabel_edit.mp4"></video>

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

   <video width="90%" controls muted src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/qgis_add_column.mp4"></video>

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

   <video width="90%" controls muted src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/qgis_delet_column.mp4"></video>
