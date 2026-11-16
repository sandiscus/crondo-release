# Firmware-Pakete

Hier liegen die Firmware-Pakete für beide Displays – je Gerät, Board und Version ein eigener Ordner.

## Aufbau

| Pfad | Bedeutung |
|---|---|
| `iris/ws146b/<version>/<version>.crondo` | Paket für **Iris** (rund, 1,46″, 412 × 412) |
| `prism/ws28/<version>/<version>.crondo` | Paket für **Prism** (eckig, 2,8″, 320 × 240) |
| `…/<version>_sim.crondo` | Simulator-Paket (nur für Tests am Schreibtisch, nicht für Kunden) |

Ein Paket passt nur zum eigenen Board. Es ist signiert und wird von Studio **vor** dem Aufspielen geprüft; ein Paket für das andere Gerät wird abgelehnt.

## Was vorliegt

| Version | Iris | Prism | Datum |
|---|---|---|---|
| 0.4.0-alpha.16 | ✓ | – | 2026-11-16 |
| 0.4.0-alpha.15 | – | – | 2026-11-15 (nur im Entwicklungsstand, kein Paket veröffentlicht) |
| 0.4.0-alpha.14 | ✓ | ✓ | 2026-11-13 |
| 0.4.0-alpha.13 | ✓ | ✓ | 2026-11-12 |
| 0.4.0-alpha.12 | ✓ | – | 2026-11-11 |
| 0.4.0-alpha.11 | ✓ | ✓ | 2026-11-10 |
| 0.4.0-alpha.10 | ✓ | ✓ | 2026-11-10 |

## Aufspielen und Rückweg

1. Display mit dem Datenkabel an den PC, CRONDO Studio starten.
2. Reiter **Firmware**, passendes Paket wählen, aufspielen. Das Gerät startet danach neu.
3. **Rückweg:** gleicher Weg, nur die ältere Version wählen. Profile und Einstellungen bleiben erhalten.

Während des Aufspielens nicht trennen. Bricht es ab, bleibt das Gerät im bisherigen Stand und Studio meldet den Fehler.

## Changelog Firmware

| Version | Datum | Inhalt |
|---|---|---|
| 0.4.0-alpha.16 | 2026-11-16 | Nur die Versionsnummer, keine Funktionsänderung – Gleichstand mit Studio. |
| 0.4.0-alpha.15 | 2026-11-15 | Theme-Betrieb: Das Display zeigt, welche Themes installiert sind und wie viel Platz frei bleibt, räumt abgebrochene Übertragungen auf und meldet klarer, wenn ein Theme nicht passt. Gespeicherte Kennung „flames“ wird einmalig auf „wings“ umgestellt. **Kein Paket veröffentlicht** – die Änderungen stecken in alpha.16. |
| 0.4.0-alpha.14 | 2026-11-13 | Theme-Speicher konnte volllaufen: abgebrochene Übertragungen blieben als Reste liegen und blockierten danach jedes Aufspielen. Reste werden jetzt automatisch entfernt, freier Platz wird angezeigt, Studio prüft die Größe vor dem Senden. |
| 0.4.0-alpha.13 | 2026-11-12 | Theme-Übertragung wieder schnell: nach einer Umstellung war sie auf winzige Häppchen zurückgefallen (ein großes Theme brauchte rund drei Minuten). Jetzt größere Blöcke – wieder im Sekundenbereich. |
| 0.4.0-alpha.12 | 2026-11-11 | Bunny-Gesichter folgen den Drehzahlbereichen: müde im unteren Bereich, neugierig in der Mitte, erschrocken kurz vor der roten Linie. |
| 0.4.0-alpha.11 | 2026-11-10 | Theme-Pakete sind signiert – das Display nimmt nur geprüfte Pakete an. Dazu eine Sperre gegen zwei Programme am selben Gerät. |
| 0.4.0-alpha.10 | 2026-11-10 | Alle Themes kommen als Paket statt fest in der Firmware: kleinere Firmware, Themes lassen sich einzeln nachinstallieren und austauschen. |
