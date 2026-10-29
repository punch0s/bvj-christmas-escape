# Lehrpersonen-Vorschau: Handy v2

Die vollständige Spielversion bleibt enthalten. Nur der Link unter Mehr wurde verständlicher beschriftet; sämtliche Spielregeln und Freigabewerte sind unverändert.

## Geändert in animation.html

- Alle acht Lehrpersonen als getrennte Entwurfs-Vorschau; kein Zugriff auf echte Spielstände.
- Zwei Reihen, hintere Reihe auf einem Podest; grössere Figuren und besser unterscheidbare Kleidungsfarben mit goldener Tönung.
- Frontkamera beim Zuspruch statt enger Kamerafahrt durch die Gruppe.
- Szenenfläche aus dem wirklichen Abstand zwischen Kopfzeile und Untertitel berechnet. Optionen zunächst eingeklappt.
- Weniger lange Verbindungsstäbe, die sich vor den Figuren kreuzen.

## Prüfungen

JavaScript-Syntax und simulierte Vorschau geprüft: acht Figuren, Freigaben unverändert, isolierter Speicher, Pause, Zeitregler, Software-3D und Ende ohne Boss-Start. Projektionsgrenzen für alle acht Figuren in 844×390, 915×412 und 390×844 geprüft; Software-Standbild intern angesehen. Offline-Cache mit simulierten Browser-APIs geprüft.

Keine Prüfung auf echtem iPhone, Android oder echter GPU. Das Layout muss dort noch mit Grosse Schrift, Ruhig und eingeblendeten Optionen kontrolliert werden. Vor allem auf alten Geräten kann die Software-Darstellung grob und langsam bleiben.

Dreiecke bei Sekunde 36: Kulisse 492, Schüler 1164, König 956, Lehrpersonen samt Podest/Stützen 4580, Licht 164, insgesamt 7356. Keine neuen Posen-Caches, keine Bilddateien. Weniger Stützen senken die Geometriekosten; die grössere Bildschirmdarstellung kann zusätzliche Pixelarbeit verursachen.

Wichtig: Im normalen Boss-Finale erscheinen weiterhin nur Lehrpersonen mit aktiv:true und freigegeben:true. Alle acht stehen im Spiel weiterhin auf freigegeben:false. Die Entwurfs-Vorschau ist kein Nachweis einer Freigabe.

## Upload

ZIP entpacken und den gesamten Inhalt in das GitHub-Repository hochladen. Nicht nur index.html ersetzen. Anschliessend im Spiel das angebotene Update laden; eine laufende Runde vorher beenden oder speichern. Unter Mehr → Lehrpersonen ansehen die neue Vorschau öffnen.
