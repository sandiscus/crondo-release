# Kataloge

Zwei signierte Listen, die Studio und das Display lesen. Beide werden maschinell erzeugt – **nicht von Hand bearbeiten**.

| Datei | Inhalt | Wer liest sie |
|---|---|---|
| `themes.json` + `themes.json.sig` | alle Theme-Pakete mit Gerät, Datei, Größe, SHA-256, Version und Datum | Studio: prüft die Signatur und bietet nur gültige Themes an |
| `profiles.json` + `profiles.json.sig` | alle Fahrzeugprofile (252 Einträge, Stand 2026-11-16) | Studio: zeigt die Auswahl „Fahrzeug aus Katalog“ |

## Prüfung

Beide Listen tragen eine Ed25519-Signatur des Release-Schlüssels. Stimmt sie nicht oder fehlt sie, gilt die Liste als ungültig und wird verworfen – Studio meldet das, statt etwas Unsicheres anzubieten.

## Stand

| Datum | themes.json | profiles.json |
|---|---|---|
| 2026-11-16 | 22 Einträge (elf Themes je Gerät) | 252 Profile |

Änderungen an den Listen stehen in [`../themes/README.md`](../themes/README.md) (Themes) beziehungsweise [`../profiles/README.md`](../profiles/README.md) (Profile).
