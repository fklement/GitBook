# Linked IoT

## Zielsetzung:
-   	Durch Verwendung von Linked-Data und Webstandards soll Semantische Interoperabilität ermöglicht werden
-   	Ziel ist es aufzuzeigen wie bestehende Standards, aus dem Bereich Linked-Data für IoT verwendet werden können
-   	Um eine möglichst große Zielgruppe zu erreichen, soll das ganze einfach umsetzbar sein (und möglichst kostengünstig gehalten werden)
-   	 Durch einen Modularen Aufbau soll es allen ermöglicht werden ihre eigenen Komponenten zu verwenden
-   	Um der Zielgruppe einen möglichst einfachen Einstieg zu ermöglichen soll eine ausführliche Dokumentation erstellt werden

## Problemstellung:
-   	Linked Data hat bereits seine Machbarkeit als Mittel zur Verbindung und Integration von Daten im Web demonstriert
-   	Durch Linked Data können strukturierte Daten semantisch miteinander verbunden werden, um ihre Beziehung zueinander zu beschreiben
-   	Momentan ist es schwierig die verschiedenen Übertragungsweisen einzelner Sensoren zu bündeln und miteinander zu verknüpfen
- Nur durch hohen Aufwand können verschiedene Sensoren angesprochen werden, jedoch eine völlig unabhängige Verarbeitung von vorher unbekannten Strukturen und Typen der Sensordaten ist zurzeit nicht möglich
- Mit dem Einsatz von Constrained Devices muss auf deren jeweilige Limitationen geachtet werden

## Lösungsansatz:
-       Um den Modularen Aufbau zu ermöglichen, wird für das Sensor-Board eine Bibliothek mit Abstrakten Klassen erstellt, die im eigenen Projekt implementiert werden können und im Arduino-File aufgerufen werden
-       Der Kontext, der bei JSON-LD Verwendung findet, wird auf dem Gateway gespeichert
-       Um mit einheitlichen Webstandards für die Übertragung Arbeiten zu können, muss die Bridge als Vermittlungsstelle dienen
-       Mithilfe eines Webinterface, wird die Initialisierung und Übertragungs-Konfiguration zur Bridge eines Sensor-Boards ermöglicht
-       Die Kopplung zwischen Sensor und Gateway wird mittels Webstandart realisiert
-   	Durch die Übertragung des Kontextes bereits bei der Kopplung, wird die Bandbreite beim eigentlichen Payload (Übertragung der Sensordaten) reduziert
-   	Beim übertragen der Sensor-Daten fordert die Bridge den benötigten Kontext des jeweiligen Sensor-Boards beim Gateway an und published den Sensor-Wert auf den zusammengesetzten Topic
