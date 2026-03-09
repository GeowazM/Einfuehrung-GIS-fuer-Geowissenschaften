=======
Erweiterungen / Plugins
=======

Es gibt zahlreiche Erweiterungen für QGIS, auch Plugins genannt, die erweiterte Funktionalitäten bieten. Wenn Sie eine bestimmte Aufgabe haben und QGIS nicht über die passende Funktionalität verfügt, sollten Sie in der Regel nach einem Plugin suchen. Sie können danach googeln oder im Plugin-Fenster suchen. 

Plugins in QGIS sind nützliche Zusatzwerkzeuge, die Sie verwenden können, um einige Aufgaben zu erleichtern. Plugins werden von QGIS-Entwicklern und anderen unabhängigen Benutzern geschrieben, die die Kernfunktionalität der Software erweitern möchten. Diese Plugins werden in QGIS für alle Benutzer kostenlos zur Verfügung gestellt. Einmal installiert, bleiben Plugins in QGIS verfügbar.

.. note::
   Sie müssen Plugins nicht für jedes neue Projekt neu installieren.

Installation von Plugins
========================

Um ein Plugin zu installieren: ``Erweiterungen`` -> ``Erweiterungen verwalten und installieren...`` -> ``Alle`` -> Nach dem Plugin suchen -> ``Erweiterung installieren``.

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/qgis_plugins.mp4"></video>

.. tip::
   Wenn Sie eine bestimmte Erweiterung nicht finden können, überprüfen Sie die Groß-/Kleinschreibung und die korrekte Verwendung von Leerzeichen. Wenn Sie eine Erweiterung immer noch nicht finden können, müssen Sie möglicherweise die experimentellen Erweiterungen in den Optionen zulassen (siehe unten).

Plugins verwalten
=================

Wenn Sie installierte Plugins derzeit nicht verwenden, kann es nützlich sein, diese zu deaktivieren, um überfüllte Werkzeugleisten zu vermeiden und die Anzahl offener Bedienfelder zu reduzieren.

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/Manage_plugins.mp4"></video>

Experimentelle Erweiterungen zulassen
=====================================

Experimentelle Erweiterungen befinden sich entweder noch in der Entwicklung oder es handelt sich um veraltete Erweiterungen, die nicht mehr für die neueren Versionen von QGIS optimiert/angepasst werden. Dennoch kann die Verwendung experimenteller Erweiterungen nützlich sein:

* Spezifische Funktionen werden von keiner anderen Erweiterung unterstützt.
* Als Alternative, falls es Probleme mit einer anderen Erweiterung gibt.
* Ein Tutorial verwendet eine bestimmte Erweiterung.

.. raw:: html

   <video width="100%" controls src="https://github.com/GeowazM/gis-training-resource-heigit/raw/main/fig/Experimentel_plugins.mp4"></video>

.. tip::
   Aufgrund der oft fehlenden Optimierung für die verwendete QGIS-Version können experimentelle Erweiterungen vermehrt Fehlermeldungen oder andere Probleme bis hin zum Absturz von QGIS verursachen. Experimentelle Erweiterungen sollten daher nur für die Nutzung aktiviert und danach wieder deaktiviert werden. Stellen Sie außerdem sicher, dass der aktuelle Arbeitsfortschritt gespeichert ist, um Datenverlust bei einem Absturz von QGIS zu vermeiden.

Herunterladen des QuickOSM-Plugins
==================================

Um Daten herunterzuladen und in Ihr QGIS zu importieren, eignet sich das Plugin **QuickOSM** hervorragend. Zuerst müssen Sie es installieren, indem Sie im Tab ``Erweiterungen verwalten und installieren`` danach suchen.

.. dropdown:: Wie man das Plugin herunterlädt

   .. figure:: /fig/managa_install_plugins.png
      :width: 400px
      :align: center
      :name: managa_install_plugins_wiki

      Erweiterungen verwalten und installieren.

   .. figure:: /fig/install_quickosm.png
      :width: 800px
      :name: install_quickosm_wiki
      :align: center

      Installation von QuickOSM.

Um das neu installierte Plugin zu starten, klicken Sie auf |quickosmplugin| oder navigieren Sie zu ``Vektor`` -> ``QuickOSM``.

Befolgen Sie diese Schritte, um Daten abzurufen:

1. Wählen Sie einen Schlüssel (Key) und einen Wert (Value) aus der Dropdown-Liste. Wenn Sie unsicher sind, schauen Sie hier nach: `taginfo.openstreetmap.org <https://taginfo.openstreetmap.org>`_.

.. figure:: /fig/key_value_quickosm.png
   :width: 800px
   :align: center
   :name: key_value_quickosm_wiki

   Auswahl von Key und Value in QuickOSM.

2. Begrenzen Sie das Gebiet, indem Sie den Namen Ihrer Region eingeben.
3. Klappen Sie den Reiter ``Erweitert`` (Advanced) auf. Wählen Sie nur die Datentypen aus, die Sie erwarten, um Fehler zu minimieren.

.. figure:: /fig/quickosm_usage.png
   :width: 800px
   :align: center
   :name: quickosm_usage_wiki

   Ausführen des QuickOSM-Plugins.

4. Klicken Sie auf ``Abfrage ausführen`` (Run query).

.. dropdown:: Wie man Daten für mehrere Abfragen abruft

   Wenn Sie weitere Daten im selben Gebiet abrufen möchten, können Sie eine Abfrage hinzufügen, indem Sie auf |plus_quickosm| klicken. Achten Sie darauf, den richtigen logischen Operator ``Und`` (And) oder ``Oder`` (Or) zu wählen. Wenn Sie unsicher sind, überprüfen Sie diese `Wikiseite </content/Wiki/en_qgis_non_spatial_queries_wiki>`_.

..
   Hier werden die Inline-Bilder als Substitutions definiert:

.. |quickosmplugin| image:: fig/quickosmplugin.png
.. |plus_quickosm| image:: fig/plus_quickosm.png