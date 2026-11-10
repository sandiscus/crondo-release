# CRONDO – Downloads

Zusatzanzeige fürs Auto: OBD-Daten auf einem kleinen Display, eingerichtet über CRONDO Studio am PC.

<!-- Jeder Abschnitt mit „Marketing:" ist ein Platzhalter. Text von der Rolle Marketing einsetzen,
     technische Angaben (Dateinamen, Größen) bleiben wie sie sind. Stand des Gerüsts: 11.11.2026, Kurator. -->

## Was liegt hier

Dieses Repo enthält nur fertige Pakete, keinen Quelltext (Entscheidung ADR 0008).

| Pfad | Inhalt |
|---|---|
| `firmware/<gerät>/<board>/<version>/` | Firmware-Paket (`.crondo`) je Gerät und Version, z. B. `firmware/iris/ws146b/0.4.0-alpha.11/0.4.0-alpha.11.crondo` |
| `themes/` | Theme-Pakete (`.theme`) mit Signatur (`.theme.sig`) |
| `latest/themes.json` + `.sig` | signierter Theme-Katalog, den Studio liest |

Geräte: **Iris** (rund, Board `ws146b`) und **Prism** (eckig, Board `ws28`).

## CRONDO Studio installieren (Windows)

**Marketing:** Text – Download, Setup starten, SmartScreen-Hinweis erklären (die Pakete sind nicht signiert, Windows fragt deshalb einmal nach), erster Start, Sprachauswahl entfällt.

Technische Angaben für den Text: Windows 10/11 (64 Bit), Installer als `.exe`, Studio aktualisiert sich nicht selbst.

## Firmware aufspielen

**Marketing:** Text – Studio starten, Gerät per USB verbinden, Firmware-Datei wählen, aufspielen, Gerät startet neu. Hinweis: während des Aufspielens nicht trennen.

Technische Angaben: Firmware-Paket ist signiert und wird vor dem Aufspielen geprüft; nur Pakete für das passende Board sind zulässig.

## Theme-Pakete

**Marketing:** Text – Theme-Pakete ändern das Aussehen des Displays; sie werden über Studio eingespielt und sind frei verfügbar.

Technische Angaben: Werks-Theme ist `minimal`; zusätzlich Classic, All-out, Bunny, Flames. Jedes Paket trägt eine Signatur, die das Gerät beim Einspielen prüft. Der Katalog `latest/themes.json` ist signiert.

## Updates

**Marketing:** Text – neue Version erscheint hier, ältere Versionen bleiben liegen (Rückweg möglich), Changelog unten lesen.

## Rollback

Ein Zurückspielen einer älteren Firmware ist möglich. **Marketing:** Text – wann das sinnvoll ist (z. B. nach einem Fehler in einer neuen Version) und dass Profile und Einstellungen erhalten bleiben.

## Changelog

Je Version ein Eintrag, neueste zuerst. Quelle der Zeilen: `plan/verlauf.md` im Entwicklungs-Repo (der Kurator trägt sie ein).

| Version | Datum | Inhalt |
|---|---|---|
| 0.4.0-alpha.11 | 2026-11-10 | **Marketing:** aus `plan/verlauf.md` übernehmen (Themes im Gerät nutzbar, Signatur je Theme-Paket) |
| 0.4.0-alpha.10 | 2026-11-10 | **Marketing:** aus `plan/verlauf.md` übernehmen |

## Support

**Marketing:** Text – Support-Paket in Studio erzeugen (Sicherung + Logs in einer Datei, ca. 64 kB) und per Mail an die Support-Adresse schicken; Hinweis, dass manche Mail-Programme kleine Anhänge haben.

## Rechtliches

- Lizenztexte: **Marketing/Produkt** – Verweis auf `LIZENZEN.txt` im Studio-Paket (enthält u. a. die LGPL-Hinweise zu Qt).
- Datenschutz: **Marketing/Produkt** – Text; technisch gilt: die Firmware sendet nichts, Studio lädt nur den Theme-Katalog und die Update-Seite (kein Konto, keine Kennung).
