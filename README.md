# CRONDO – Downloads

Zusatzanzeige fürs Auto: Dein Auto zeigt seine Werte auf einem kleinen Display – Geschwindigkeit, Drehzahl, Temperaturen, Verbrauch, Beschleunigungszeiten und Fehlercodes im Klartext. Eingerichtet wird alles am PC mit CRONDO Studio.

> **Stand: Alpha.** Dieses Repo enthält Testpakete für Tester, keinen Verkauf. Funktionen können sich noch ändern; Fehler bitte melden (siehe „Support").

## Was liegt hier

Dieses Repo enthält nur fertige Pakete, keinen Quelltext (Entscheidung ADR 0008).

| Pfad | Inhalt |
|---|---|
| `firmware/<gerät>/<board>/<version>/` | Firmware-Paket (`.crondo`) je Gerät und Version, z. B. `firmware/iris/ws146b/0.4.0-alpha.11/0.4.0-alpha.11.crondo` |
| `themes/` | Theme-Pakete (`.theme`) mit Signatur (`.theme.sig`) |
| `latest/themes.json` + `.sig` | signierter Theme-Katalog, den Studio liest |

Geräte: **Iris** (rund, Board `ws146b`) und **Prism** (eckig, Board `ws28`). Beide laufen mit derselben Software, jedes Gerät bekommt sein eigenes Firmware-Paket.

## Was du brauchst

- **Display:** für Iris ein Waveshare **ESP32-S3-Touch-LCD-1.46B** (rund, 1,46″, 412 × 412), für Prism ein Waveshare **ESP32-S3-Touch-LCD-2.8**. Genau diese Modelle – andere Boards laufen nicht.
- **OBD-Adapter:** ein ELM327-kompatibler Adapter mit **Bluetooth LE** (Bluetooth 4.0 oder neuer). Ältere Adapter mit klassischem Bluetooth funktionieren nicht. Steckt der Adapter in der OBD-Buchse deines Autos, verbindet sich das Display selbst damit.
- **USB-C-Datenkabel** (kein reines Ladekabel) für die Einrichtung und den Strom im Auto – aus der USB-Buchse des Radios oder einem 12-V-Adapter.
- **Windows-PC** (10/11, 64 Bit) für die Einrichtung, Updates und Theme-Pakete.
- **Halter** für die Montage. Gehäuse und Halter sind 3D-Druck-Teile; Dateien und Hinweise kommen mit dem Tester-Zugang.

Dein Auto braucht eine OBD-II-Buchse (in der EU Pflicht bei Benzinern ab 2001, Diesel ab 2004). Welche Werte dein Auto liefert, entscheidet der Hersteller – fehlt ein Wert, zeigt das Display `--`.

## CRONDO Studio installieren (Windows)

1. Studio von **crondo.app** herunterladen, sobald der Auftritt online ist – als Tester bekommst du den Link mit deinem Zugang.
2. Die Setup-Datei starten.
3. Windows meldet beim ersten Start, dass die App nicht signiert ist. Das ist bekannt und beabsichtigt (der Installer trägt bewusst keine Code-Signatur). Über **Weitere Informationen → Trotzdem ausführen** geht es weiter.
4. Den Anweisungen des Installers folgen, danach Studio über die Verknüpfung starten.
5. Studio aktualisiert sich **nicht** selbst – eine neue Studio-Version installierst du wieder über den Installer.

Studio braucht kein Konto und keine Anmeldung. Es liest das Gerät per USB und lädt aus diesem Repo nur den Theme-Katalog und die Update-Seite.

## Firmware aufspielen

1. Display mit dem USB-C-**Datenkabel** an den PC stecken.
2. Studio starten und warten, bis das Gerät erkannt ist (Reiter „Gerät").
3. Im Reiter „Firmware" das passende Paket für dein Gerät wählen – Iris oder Prism, je nach Board.
4. Aufspielen starten. Das Gerät startet danach von selbst neu.
5. **Während des Aufspielens nicht trennen.** Bricht der Vorgang ab, das Gerät nicht abziehen, sondern das Aufspielen erneut starten.

Das Paket ist signiert und wird vor dem Aufspielen geprüft; ein Paket für ein anderes Board wird abgelehnt. Fahrzeugprofil, Einstellungen und Bestzeiten bleiben beim Firmware-Wechsel erhalten.

## Theme-Pakete

Ein Theme ändert das Aussehen des ganzen Displays – Schriften, Farben, Zeiger, Hintergründe. Es gibt fünf: **Minimal** (ab Werk), **Classic**, **All-out**, **Bunny** und **Flames**, jeweils für Iris und Prism.

1. In Studio das Theme-Paket wählen (`.theme` aus `themes/`).
2. Studio überträgt das Paket per USB aufs Display; das Display prüft die Signatur und nimmt nur geprüfte Pakete an.
3. Danach das Theme auswählen – das Display startet dabei einmal neu.

Die Pakete liegen hier kostenlos. Welche Themes dein Gerät nutzen darf, hängt von deiner Lizenz ab. Die Akzentfarbe (acht Farben) stellst du unabhängig vom Theme ein, am Gerät oder in Studio; sie wirkt sofort.

## Updates

Neue Versionen erscheinen hier unter `firmware/<gerät>/<board>/<version>/`. Ältere Versionen bleiben liegen – der Rückweg ist damit jederzeit möglich. Vor dem Aufspielen lohnt ein Blick ins Changelog unten: Was ist neu, was hat sich geändert.

## Rollback

Eine ältere Firmware kannst du jederzeit wieder aufspielen: gleicher Weg wie beim Update, nur die ältere Version wählen. Sinnvoll ist das, wenn eine neue Version bei dir einen Fehler zeigt, den die vorige nicht hatte. Einstellungen, Fahrzeugprofil, Gas-Skala, Bestzeiten und Logs bleiben dabei erhalten.

## Changelog

Je Version ein Eintrag, neueste zuerst. Quelle der Zeilen: `plan/verlauf.md` im Entwicklungs-Repo (der Kurator trägt sie ein).

| Version | Datum | Inhalt |
|---|---|---|
| 0.4.0-alpha.11 | 2026-11-10 | Theme-Pakete sind jetzt signiert: Das Display nimmt nur geprüfte Pakete an und meldet sonst eine fehlende oder ungültige Signatur. Dazu eine Sperre, damit nicht zwei Programme gleichzeitig auf dasselbe Gerät zugreifen (Windows und macOS/Linux). |
| 0.4.0-alpha.10 | 2026-11-10 | Alle fünf Themes kommen als Paket statt fest in der Firmware: Die Firmware wird deutlich kleiner, Themes lassen sich einzeln nachinstallieren und austauschen. |

## Support

Wenn etwas nicht läuft:

1. Studio starten, Reiter **„Support"**.
2. **Support-Paket erstellen** – eine Datei mit Sicherung und Logs, etwa 64 kB. Studio zeigt vorher als Liste, was drin ist.
3. Die Datei an die Adresse schicken, die du mit deinem Tester-Zugang bekommen hast. Etwas Platz im Postfach hilft: manche Mail-Programme begrenzen Anhänge.

Im Paket stehen technische Daten und die Logs, die das Display ohnehin aufzeichnet. Schick nur, was du mitschicken willst – vor dem Speichern siehst du die Inhaltsliste.

## Rechtliches

- **Lizenztexte:** im Studio-Paket als `LIZENZEN.txt` (enthält unter anderem die LGPL-Hinweise zu Qt).
- **Datenschutz:** Die Firmware sendet nichts. Studio lädt nur den Theme-Katalog und die Update-Seite aus diesem Repo – ohne Konto, ohne Kennung, ohne Tracking, ohne Cookies. Lokal auf deinem PC gespeichert werden nur deine Einstellungen, gesicherte Logs und Profile.
- Verkauf, Preise, AGB und Widerruf sind nicht Teil dieses Repos; sie stehen auf crondo.app, sobald der Auftritt online ist.
