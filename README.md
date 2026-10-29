# Viventa BVJ: Christmas Escape – vollständiges Spiel für GitHub Pages

## Hochladen

1. ZIP auf deinem Computer entpacken.
2. In deinem GitHub-Repository den **Inhalt** dieses Ordners hochladen: `index.html`, `animation.html`, `sw.js`, `manifest.json`, den ganzen Ordner `icons`, `release.json`, `.nojekyll`, `THIRD_PARTY_LICENSES.txt`, `build_release.py` und diese README. `index.html` muss direkt im gewählten Veröffentlichungsordner liegen, nicht in einem zusätzlichen Unterordner. Nicht die ZIP-Datei selbst hochladen.
3. Im Repository **Settings → Pages** öffnen.
4. **Source: Deploy from a branch**, Branch **main**, Ordner **/(root)** wählen und **Save** klicken.
5. Warten, bis GitHub die Veröffentlichung als erfolgreich meldet. Die dort angezeigte Pages-Adresse öffnen. Der Schüler-Link ist die Startadresse des Spiels, nicht der GitHub-Code-Link.

Quelle zu den GitHub-Einstellungen: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Kein npm, Node oder Build-Schritt für den ersten Upload nötig. `.nojekyll` ist beim Entpacken eventuell versteckt. Falls der Web-Uploader sie nicht anzeigt, ist das für diese einfachen HTML-Dateien unkritisch; die übrigen Dateien und der icons-Ordner sind nötig.

## Was enthalten ist

- Vollständiges Spiel: Schule, 3D-Labyrinth, Schattenstadt, Boss-Kampf, Lernfragen, Garderobe, Zeitmessung, Ergebnisse, CSV und Urkunde.
- Aktuelle 3D-Boss-Zwischenszene mit humanoidem König Stress, schwarzem Zepter, Schonfrist und sechssekündiger Kurzfassung für während der Szene gespeicherte Spielstände.
- Im normalen Boss-Kampf bleibt das bisherige Wolkenmodell erhalten; Hitbox, Angriffe und Warnkreis bleiben unverändert.
- Die eigentliche Boss-Szene zeigt nur Lehrpersonen mit `aktiv:true` und `freigegeben:true`. Diese Felder wurden nicht verändert. Ohne Freigaben erscheint der Lichtstrahl.
- **Mehr → 3D-Animation · alle 8 Lehrpersonen (Entwurf)** öffnet die getrennte Vorschau in einem neuen Tab. Sie zeigt alle acht als Entwurf und schreibt keine Spielstände. Alternativ `animation.html` unter derselben Pages-Adresse öffnen.
- Manifest, Icons, Offline-Cache und Hinweis auf neue Versionen. Nach einem vollständig erfolgreichen ersten Laden kann das Spiel offline starten. Keine externen Modell- oder Bilddownloads für den Spielstart.

Die Vorschau ist zusätzlich enthalten. `index.html` ist immer das vollständige Spiel und startet keine Animationsvorschau automatisch.

## Nach dem ersten Laden / Offline

1. Spiel über HTTPS öffnen, im Hauptmenü «Mehr» öffnen und warten, bis **Offline bereit auf diesem Gerät** erscheint. Falls das Einrichten fehlschlägt, online erneut laden; dann ist Offline-Start noch nicht zugesichert.
2. Auf iPhone optional über das Teilen-Menü «Zum Home-Bildschirm» hinzufügen; auf Android über den Browser «Zum Startbildschirm hinzufügen» bzw. «App installieren», sofern angeboten.
3. Danach ohne Netz erneut öffnen und Spiel sowie Mehr → Animation prüfen. Offline-Speicher gilt je Gerät und Browser. Löschen von Website-Daten entfernt auch den lokalen Fortschritt und den Offline-Cache.

## Updates

1. Änderungen an `index.html`, `animation.html`, Manifest oder Icons vornehmen.
2. Im Paketordner `python3 build_release.py` ausführen. Das erzeugt einen neuen Cache-Namen, `sw.js` und passende Datei-Prüfsummen in `release.json`.
3. Alle zusammengehörenden Dateien in **einem Commit** hochladen. Nicht nur `sw.js` oder `release.json` austauschen. Bei unvollständigem Upload bleibt die bisherige Offline-Version erhalten.
4. Nach erfolgreicher GitHub-Veröffentlichung Spiel online öffnen. Bei **Neue Version verfügbar** zuerst am Checkpoint speichern und den Update-Knopf antippen. Der Spielstand wird vor dem Neuladen gespeichert.
5. Auf iPhone und Android die neue Version prüfen. Bei einem sehr alten Service Worker kann noch einmal online neu laden nötig sein. Keine Spielstände über «Website-Daten löschen» zurücksetzen, wenn sie erhalten bleiben sollen.

## Lehrpersonen und Test

Lehrer-Modus: Adresse um `?lehrer=1` ergänzen oder fünfmal auf das Logo tippen. Der vorhandene PIN ist `2741`, im HTML über `TEACHER_PIN` änderbar. Der PIN ist ein einfacher Schutz gegen versehentliches Öffnen und kein geheimer Server-Zugang.

Vor der Klasse auf einem echten iPhone/Safari und Android/Chrome prüfen: Start, Touch, Ton, Drehen, Fragen, Checkpoints, Boss bis zum Sieg, Szenenzeit, Speichern/Laden, Ergebnis kopieren, CSV, Urkunde und Offline-Neustart. Browser-/Codeprüfungen ersetzen keinen realen Gerätetest. Die Freigaben für Lehrpersonen sind weiterhin als Entwurf zu behandeln.

Ergebnisse bleiben im Browser des jeweiligen Geräts. Ein GitHub-Upload sammelt die Ergebnisse nicht zentral. Auf derselben Domain und demselben Browser können andere Versionen dieselben localStorage-Schlüssel verwenden.

## Handy-Vorschau v2
Unter Mehr → Lehrpersonen ansehen: alle acht Figuren in zwei Reihen, grössere Szenenfläche, ruhigere Frontkamera. Optionen sind einklappbar. Die Vorschau verändert weder Spielstand noch Freigaben. Im Boss-Finale gelten weiterhin aktiv und freigegeben.
