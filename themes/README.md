# Themes

Jedes Theme ändert das ganze Display: Schriften, Farben, Zeiger, Hintergründe. Die Pakete liegen hier je Gerät; der signierte Katalog, den Studio liest, steht in [`../latest/`](../latest/).

## Aufbau

| Datei | Bedeutung |
|---|---|
| `<gerät>_<theme>.theme` | Theme-Paket |
| `<gerät>_<theme>.theme.sig` | Signatur des Pakets – das Display prüft sie beim Einspielen |
| `<gerät>_<theme>.theme.version` | Versionsstempel (Datum + laufende Nummer), z. B. `2026-11-11.1` |
| `../latest/themes.json` + `.sig` | Katalog aller Themes, signiert; Quelle für Studio |

## Die Themes

| Kennung | Name | Charakter |
|---|---|---|
| `minimal` | Minimal | dünne Schrift, Lichtband – **ab Werk eingestellt** |
| `classic` | Classic | Segmentringe |
| `allout` | All-out | Farbverlauf, Schaltleuchten, Karten |
| `bunny` | Bunny | Zeigerinstrument mit Kaninchen, das auf die Drehzahl reagiert |
| `wings` | Wings | Zeigerinstrument mit Flügelmotiv (bis 12.11.2026 unter der Kennung `flames`) |
| `flames` | Flames | Hot Rod: Flammen, Chrom (Kennung seit 13.11.2026 neu vergeben) |
| `neon` | Neon Drive | Synthwave: Sonne, Gitter, Leuchtsegmente |
| `heritage` | Heritage | klassisches Instrument: Gold, Elfenbein |
| `blueprint` | Blueprint | technische Zeichnung |
| `terrain` | Terrain | topografische Karte |
| `bloom` | Bloom | Kirschblüten |

Elf Themes je Gerät, alle für Iris und Prism.

## Einspielen

Studio → Reiter **Einstellungen** → Theme wählen → übernehmen. Studio löscht dabei die Pakete, die nicht mehr gebraucht werden, und spielt das gewählte auf; das Display prüft die Signatur.

**`minimal` liegt immer auf dem Gerät** und wird nie gelöscht: Es ist die Rückfallebene, die ohne Lizenz und ohne weitere Pakete funktioniert.

## Changelog Katalog

| Stand | Einträge | Änderung |
|---|---|---|
| 2026-11-16 | 22 | Katalog neu erzeugt und signiert – elf Themes je Gerät, keine Karteileichen mehr (zwei Einträge ohne Paket aus dem Stand vom 13.11. sind bereinigt). |
| 2026-11-15 | 22 | Katalog neu erzeugt; `flames` wieder als eigenes Theme, `wings` bleibt bestehen. |
| 2026-11-13 | 20 | Sechs Dekor-Themes dazu (Flames, Neon Drive, Heritage, Blueprint, Terrain, Bloom); Umbenennung `flames` → `wings` für das Zeigerinstrument. |
| 2026-11-10 | 10 | Signierte Pakete und Versionsstempel eingeführt (fünf Themes je Gerät). |
| 2026-11-08 | 10 | Erster Katalog: fünf Themes je Gerät als Paket statt fest in der Firmware. |
