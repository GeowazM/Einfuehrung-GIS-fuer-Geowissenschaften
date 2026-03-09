Automatisierung - der Model Builder
===============

Der QGIS Model Builder, auch als Graphical Modeler bekannt, ist ein Werkzeug in QGIS, das es Benutzern ermöglicht, benutzerdefinierte Workflows für die 
Verarbeitung und Analyse von Geodaten zu erstellen. Mit einer visuellen Oberfläche können bestehende QGIS-Tools und -Funktionen in einer benutzerdefinierten 
Reihenfolge angeordnet und verbunden werden, um wiederholte oder komplexe Aufgaben zu automatisieren.

Vorteile des QGIS Model Builders
-------------
1. Automatisierung: Der Model Builder ermöglicht die Automatisierung von Arbeitsabläufen, wodurch wiederholte Aufgaben effizienter und konsistenter ausgeführt werden können.
2. Benutzerfreundlichkeit: Die visuelle Oberfläche macht es einfach, komplexe Modelle zu erstellen, ohne dass umfangreiche Programmierkenntnisse erforderlich sind.
3. **Reproduzierbarkeit**: Einmal erstellte Modelle können gespeichert und mit verschiedenen Datensätzen wiederverwendet werden, was Zeit und Aufwand spart.
4. Fehlerreduktion: Durch die Automatisierung und Standardisierung von Prozessen werden menschliche Fehler minimiert.
5. Flexibilität: Der Model Builder unterstützt eine Vielzahl von Eingaben und Algorithmen, sodass komplexe und maßgeschneiderte Analysen möglich sind.

Tutorial
-------------

.. admonition:: QGIS Model Builder
    :class: admonition-youtube

    ..  youtube:: eZb5VLTc9-o&t=306s

    `Geospatial School  on Youtube <https://www.youtube.com/watch?v=eZb5VLTc9-o&t=306s>`_

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
