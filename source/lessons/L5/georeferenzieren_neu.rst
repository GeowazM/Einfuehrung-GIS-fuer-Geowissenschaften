Georeferenzierung
========

   * **Raster >> Georeferenzierung** (ggfs. Erweiterung GDAL-Georeferenzierung installieren)

Wichtiges zur Georeferenzierung
-------------------------------

Ziel der Georeferenzierung ist es, einen Geodatensatz ohne Realwelt-Koordinaten anhand von Referenzdaten mit Realweltkoordinaten so
zu übersetzten, dass danach ein räumlicher Bezug hergestellt ist. Dabei wird das Koordinatensystem des zu georeferenzierenden Geodatensatzes
anhand von Passpunkten modifiziert: mithilfe von Rotation(Drehung), Translation(Verschiebung) und Skalierung(Dehnung/Stauchung) und ggf. Entzerrung wird der Geodatensatz räumlich verortet.

Wichtig für die Übung sind zwei Methoden: 
   1. Georeferenzieren auf Grundlage einer analogen Karte: 
 
      * Boordinatenbezugssystem (KBS) muss bekannt sein
      * Mindestens 4 Koordinatenpunkte müssen bekannt sein
      * Pixelwerte müssen auf Meterangaben skaliert werden
      * als Passpunkte werden die Schnittpunkte vom Gitternetz des zugrundeliegenes KNE verwendet
      * Vorteil: Schnittpunkte genau in Karte ablesbar und damit Passpunkte präzise setzbar 
   2. Georeferenzieren auf Grundlage eines Luftbilds: 
      
      * Passpunkte wählen anhand von gut verortbaren Orten in den beiden Datensätzen Zentral für die Georeferenzierung sind Passpunkte, anhand derer von QGIS
         eine Regression vorgenommen wird. Die Genauigkeit der Georeferenzierung steht und fällt daher mit der Genauigkeit der Passpunkte. 
         Die gewählten Passpunkte sollten daher drei Eigenschaften erfüllen – sie sollten

      * ausreichend viele sein (→ Mindestanzahl der Passpunkte erfüllen → RMS-Fehler bestimmbar)
      * gut verteilt sein (→ je näher zusammen, desto weniger aussagekräftig der RMS-Fehler für Genauigkeit der Georeferenzierung)
      * möglichst gut zu verorten sein (→ exaktere Übereinstimmung der Passpunkte)
   
Je nachdem, wie gut diese Eigenschaften erfüllt sind, wirkt sich dies auf die Genauigkeit der Übersetzung aus. Diese wird von QGIS durch den
RMS-Fehler berechnet – je niedriger dieser ist, desto genauer die Georeferenzierung, sofern die obigen Bedingungen erfüllt sind.


.. admonition:: Start your georeferencing project

    **Du kannst zwischen verschiedenen Karten, die du georeferenzieren sollst, auswählen**.
    
    - `Georeferenzieren <https://giscience.github.io/gis-training-resource-center/content/Module_3/en_qgis_georeferencing.html>`__

Weitere Ressourcen:
-------------------

-  `Tutorial: Wie georeferenziere ich eine gescannte Karte in QGIS? <http://de.digital-geography.com/QGIS-tutorial-teil-1-wie-georeferenziere-ich-eine-gescannte-karte-mit-QGIS/>`__

Allgemeine Fehlerhinweise
-------------------------

Fehler können unter anderem zu Stande kommen durch:
   * fehlerhaftes Ablesen der Koordinaten (beim Ablesen von Passpunktkoordinaten im Kartengrid) 
   * eine fehlende Übereinstimmung zwischen Projekt-KBS, KBS des georeferenzierten Layers und übrigen Layern vor Beginn des Georeferenzieren

.. admonition:: QGIS Georeferenzierung
    :class: admonition-youtube

    ..  youtube:: qZUQ_keQnAc

    `Bonn Center for Digital Humanities on Youtube <https://www.youtube.com/watch?v=qZUQ_keQnAc>`_.