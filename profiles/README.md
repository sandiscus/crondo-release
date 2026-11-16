# Fahrzeugprofile

Profile sagen dem Display, was dein Auto liefert: Drehzahlgrenzen, Gänge, Reifengröße, Verbrauchskennfeld. Hier liegen sie als Katalog – je Hersteller, Modell, Baujahr und Motor eine Datei.

## Aufbau

| Pfad | Bedeutung |
|---|---|
| `<hersteller>/<modell>/<baujahr>/<motor>.json` | ein Profil, z. B. `vw/golf/1998-2002/diesel-1.9-agr.json` |
| `../latest/profiles.json` + `.sig` | signierter Katalog aller Profile mit Datei, Größe und Prüfsumme |

**Stand: 2026-11-16, 252 Profile** über 14 Hersteller (Audi, BMW, Ford, Honda, Hyundai, Kia, Mazda, Mini, Opel, Renault, Seat, Škoda, Toyota, VW).

## Was ein Profil enthält

Name und Version, Status (bestätigt oder vorläufig), Drehzahlgrenzen (`rpm_max`, `rpm_red`, `cold_rpm`), Temperaturen, Gänge und Reifengröße. Was das Auto tatsächlich liefert, entscheidet der Hersteller – Profile für dasselbe Modell können je Motor abweichen.

## Eigenes Profil

Im Display gibt es dafür den **Aufnahme-Modus**: Er misst Gangzuordnung und Verbrauch im Fahrbetrieb und schreibt ein Profil. Eigene Profile bleiben lokal am Gerät bzw. in Studio; sie werden nicht in diesen Katalog hochgeladen.

## Changelog

| Stand | Einträge | Änderung |
|---|---|---|
| 2026-11-16 | 252 | Katalog neu erzeugt und signiert, Profile für die ersten 14 Hersteller. |
