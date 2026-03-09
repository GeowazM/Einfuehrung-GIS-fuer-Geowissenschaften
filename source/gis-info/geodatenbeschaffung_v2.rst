Geodatenbeschaffung 
===================

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

## Übersicht nützlicher Daten-Repositorys

### Allgemeine Geodaten

+------------------+-------------------------------------------------------+------------------------------------+
| Name             | Daten                                                 | Link                               |
+==================+=======================================================+====================================+
| Natural Earth    | Administrative und physische Geographie               | https://www.naturalearthdata.com/  |
+------------------+-------------------------------------------------------+------------------------------------+
| Geonames         | Administrative Geodaten                               | https://www.geonames.org/          |
+------------------+-------------------------------------------------------+------------------------------------+
| OpenAfrica       | Open-Source-Daten über Afrika                         | https://africaopendata.org/dataset |
+------------------+-------------------------------------------------------+------------------------------------+
| DivaGIS          | Div. Daten, z. B. Verwaltung, Straßen, Klima          | http://www.diva-gis.org/gdata      |
+------------------+-------------------------------------------------------+------------------------------------+
| Open Topography  | Topographische Daten                                  | https://opentopography.org/        |
+------------------+-------------------------------------------------------+------------------------------------+
| OSM Boundaries   | Verwaltungsgrenzen (OSM-Login erforderlich)           | https://osm-boundaries.com         |
+------------------+-------------------------------------------------------+------------------------------------+
| GADM             | Verwaltungsgrenzen                                    | gadm.org                           |
+------------------+-------------------------------------------------------+------------------------------------+

### Humanitäre Daten

+------------------------------+-----------------------------------------------------------+--------------------------------------+
| Name                         | Daten                                                     | Link                                 |
+==============================+===========================================================+======================================+
| Humanitarian Data Exchange   | Offene Daten verschiedener humanitärer Organisationen     | https://data.humdata.org             |
+------------------------------+-----------------------------------------------------------+--------------------------------------+
| Healthsites                  | Standorte von Gesundheitseinrichtungen                    | https://healthsites.io/              |
+------------------------------+-----------------------------------------------------------+--------------------------------------+
| UNHCR Geoservices            | Daten über vertriebene Bevölkerungsgruppen                | https://data.unhcr.org/en/situations |
+------------------------------+-----------------------------------------------------------+--------------------------------------+
| Waterpoint                   | Daten über Wasserstellen                                  | https://www.waterpointdata.org       |
+------------------------------+-----------------------------------------------------------+--------------------------------------+

### Katastrophendaten

+-----------------------+-------------------------------------------------------------+----------------------------------------------+
| Name                  | Daten                                                       | Link                                         |
+=======================+=============================================================+==============================================+
| MapAction             | Ressourcen für Notfallkartierung                            | https://maps.mapaction.org/                  |
+-----------------------+-------------------------------------------------------------+----------------------------------------------+
| Fieldmaps.io          | Daten- und Kartendownload für humanitäre Zwecke             | https://fieldmaps.io                         |
+-----------------------+-------------------------------------------------------------+----------------------------------------------+
| ACLED                 | Konfliktdaten                                               | https://acleddata.com/data-export-tool       |
+-----------------------+-------------------------------------------------------------+----------------------------------------------+
| GDACS                 | Katastrophen-Datenbank                                      | https://www.gdacs.org                        |
+-----------------------+-------------------------------------------------------------+----------------------------------------------+
| ZKI/DLR               | Hochwasserausmaß, Schäden, Erdbeobachtung                   | https://activations.zki.dlr.de/en/activations/|
+-----------------------+-------------------------------------------------------------+----------------------------------------------+
| WFP VAM               | Ernährungssicherheit, Gefahren, Konflikte                   | https://dataviz.vam.wfp.org/                 |
+-----------------------+-------------------------------------------------------------+----------------------------------------------+

*(Hinweis: Weitere Kategorien wie Bevölkerungsdaten, Gebäudedaten und Fernerkundung folgen demselben Schema.)*

## OpenStreetMap Daten

OpenStreetMap (OSM) ist ein Gemeinschaftsprojekt mit dem Ziel, eine freie und editierbare Karte der Welt zu erstellen. Im Gegensatz zu herkömmlichen Karten erlaubt OSM jedem, Kartendaten beizutragen. Dies hat OSM zu einer wertvollen Ressource für Navigation, Stadtplanung und humanitäre Hilfe gemacht.

Es gibt drei gängige Wege, OSM-Vektordaten in QGIS zu importieren: **Geofabrik.de**, das **HOT Export Tool** und das **QuickOSM Plugin**.

.. tip::
   Wenn Sie den Export von OSM-Daten üben möchten, absolvieren Sie die **Übung 4: Exportieren von OSM-Daten**.

### QuickOSM Plugin
Das QuickOSM-Plugin ermöglicht den schnellen Download von OSM-Daten direkt in QGIS. Um effizient damit zu arbeiten, ist ein Verständnis des OSM-Datenmodells (Key-Value-Paare bzw. **Tags**) wichtig. Beispielsweise werden Krankenhäuser oft über den Tag `amenity=hospital` gefunden.

1. Installieren Sie das Plugin über `Erweiterungen` → `Erweiterungen verwalten und installieren`.
2. Öffnen Sie es über `Vektor` → `QuickOSM`.
3. Wählen Sie Schlüssel (Key) und Wert (Value) aus.
4. Begrenzen Sie das Gebiet (z. B. "Canvas Extent" oder Ortsname).
5. Klicken Sie auf `Abfrage ausführen`.

## Selbsttest-Fragen

.. admonition:: Testen Sie Ihr Wissen
   :class: note

   1. **Welche Kriterien sollten Sie bei der Auswahl von Geodaten prüfen?**
      
      .. dropdown:: Antwort
         - **Quelle/Vertrauenswürdigkeit**: Stammen die Daten von seriösen Organisationen?
         - **Größe/Auflösung**: Passt der Detailgrad zum Projekt?
         - **Format**: Ist das Format kompatibel (z. B. GeoPackage)?
         - **Datum**: Sind die Daten aktuell genug?
         - **Lizenz**: Darf ich die Daten für meine Zwecke nutzen?

   2. **Warum ist die „Datenlizenz“ so wichtig?**

      .. dropdown:: Antwort
         Die Lizenz legt fest, was rechtlich erlaubt ist (Teilen, Modifizieren, kommerzielle Nutzung). Die Missachtung kann zu rechtlichen Konsequenzen führen.

   3. **Wie beeinflusst das Erfassungsdatum die Nutzbarkeit?**

      .. dropdown:: Antwort
         Landschaften und Infrastruktur ändern sich. Alte Straßendaten führen heute zu falschen Routenberechnungen; alte Waldkarten bilden aktuelle Abholzungen nicht ab.

   4. **Was sind Herausforderungen bei der Integration verschiedener Quellen?**

      .. dropdown:: Antwort
         Unterschiedliche Aktualität, verschiedene Koordinatensysteme (CRS), lückenhafte Metadaten oder abweichende Attributbezeichnungen (z. B. unterschiedliche Schreibweisen von Distriktnamen).