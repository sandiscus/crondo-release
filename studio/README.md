# CRONDO Studio (PC)

CRONDO Studio richtet das Display ein: Firmware aufspielen, Fahrzeugprofil wählen, Theme setzen, Logs sichern. Die Setup-Datei liegt **nicht** im Git (rund 47 MB je Version), sondern als Release-Asset bei GitHub – der Link steht auf crondo.app.

## Versionen

| Version | Plattform | Datum | Datei |
|---|---|---|---|
| 0.4.0-alpha.14 | Windows 10/11, 64 Bit | 2026-11-15 | `CRONDO-Studio-0.4.0-alpha.14-Setup.exe` + `SHA256SUMS.txt` |

Ältere Versionen bleiben als Release erhalten und lassen sich weiter herunterladen – der Rückweg ist derselbe wie beim Update, nur mit der älteren Datei.

## Installation (Windows)

1. Setup starten. Windows meldet **„unbekannter Herausgeber“** – die Datei ist nicht signiert, das ist in der Alpha so vorgesehen. Über „Weitere Informationen“ → „Trotzdem ausführen“ installieren.
2. Installiert wird **im eigenen Benutzerprofil** (`%LOCALAPPDATA%\Programs\CRONDO Studio`), es sind keine Administratorrechte nötig.
3. Nutzerdaten (Einstellungen, Profile, Logs, Sicherungen) liegen in `%LOCALAPPDATA%\Crondo\Studio` und bleiben bei einer Deinstallation stehen.
4. Lizenzhinweise zu allen Fremdprogrammen: Startmenü-Eintrag **„Lizenzhinweise“** (`LIZENZEN.txt`, Volltexte unter `assets/legal/`).

## Was die Alpha kann

Erstinstallation am Gerät, Fahrzeug und Profil wählen, Firmware aufspielen und zurückrollen, Themes aufspielen, Seiten und Akzentfarbe setzen, Logs ansehen und ein Support-Paket erstellen, Admin-Reiter für die Paketveröffentlichung.

## Changelog Studio

| Version | Datum | Inhalt |
|---|---|---|
| 0.4.0-alpha.14 | 2026-11-15 | Erstes Windows-Paket: Installation im Nutzerprofil ohne Adminrechte, Lizenzhinweise im Startmenü, unsigniert (SmartScreen-Hinweis erwartet). Version gleichauf mit der Firmware. |

## Noch nicht verfügbar

macOS- und Linux-Pakete. Wer die Admin-Funktionen (Pakete bauen und signieren) braucht, nutzt vorerst den Mac-Build.
