# Prüfstand – GitHub-Vollversion

- Quelle: aktuelle vollständige HTML-Version mit König Stress, alle drei Etappen, Boss, Ergebnissen/CSV und Urkunde.
- Einzige Paket-Anpassungen im Spiel: Service-Worker-Anmeldung wieder aktiviert; Link unter Mehr zur isolierten Animation hinzugefügt. Andere Quelldateien bleiben unverändert.
- Boss-Auslöser, Szenenzustand, Pause, Schonfrist, Speichern/Laden, Figur, Kollision und Ergebnisfunktionen unverändert verglichen. Lehrpersonen-Daten und Freigabefelder unverändert.
- JavaScript-Syntax für das vollständige Spiel und den Service Worker geprüft.
- Szenen-Regressionstests: echte 3D-Geometrie mit abgefangenem GL-Zeichenaufruf, endliche Mesh-Daten, Zeitpause, Rückkehrkamera, 55-Sekunden-Ende, Schonfrist und WebGL-Ausfall.
- Rückfall-Regressionstests: ruhige Textszene, pending-Spielstand, sechssekündige Kurzfassung, danach erledigter Zustand.
- Offline-Tests in simuliertem Service-Worker-Kontext: index.html, Startadresse mit und ohne Lehrer-Parameter, separate animation.html, Manifest und Icons; Betrieb unter /klasse/spiel/ statt Domain-Wurzel; explizite Aktualisierung; nur eigene alte Caches löschen; unvollständige Releases anhand SHA-256 ablehnen.
- Prüfsummen aller fünf Offline-Dateien entsprechen release.json. ZIP auf Lesbarkeit und vollständige Dateien geprüft.
- Keine QA-Seiten, Fotos, interne Testskripte oder Test-Spielstände im ZIP.

Nicht geprüft: tatsächliche Veröffentlichung auf GitHub, echte Service-Worker-Installation in Safari/Chrome auf einem Handy, GPU-Durchlauf dieser Paketversion, Ton/Touch/Akku/Wärme auf realen Geräten und kompletter Durchlauf bis zum Boss-Sieg mit Export. Browser-Vorschau dieser neuen Paketadresse ist beim Öffnen zeitlich abgebrochen.

Nächster Schritt: Paketinhalt in GitHub hochladen, Pages erfolgreich veröffentlichen lassen, dann auf mindestens einem iPhone und einem Android-Handy einschliesslich Offline-Neustart und Ergebnisexport testen.
