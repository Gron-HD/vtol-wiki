# VTOL VR Squadron Wiki

**Zum Wiki: https://gron-hd.github.io/vtol-wiki/**

Wiki unserer VTOL VR Squadron, gebaut mit [Zensical](https://zensical.org) und gehostet auf GitHub Pages.
Jede Änderung auf dem Branch `main` wird automatisch veröffentlicht (Fortschritt im Tab *Actions*, dauert ca. 1–2 Minuten).

## Mitmachen

Am einfachsten direkt im Wiki: Auf jeder Seite oben rechts auf den Stift klicken, Text ändern, *Commit changes* klicken.
Die ausführliche Anleitung inklusive Markdown-Spickzettel steht im Wiki unter
[Mitmachen](https://gron-hd.github.io/vtol-wiki/mitmachen/).

Zum Bearbeiten braucht man einen GitHub-Account und muss als Mitarbeiter eingetragen sein
(*Settings → Collaborators → Add people*, die Person muss die Einladung annehmen).

## Aufbau

```
docs/
├── index.md              Startseite
├── flugzeuge/            Flugzeugübersicht und Seiten pro Muster
├── gefechtsdatenbank/    Bodenziele, SHORAD, RWR, Brevity, Jamming, Kneeboard, Leitfäden
├── verfahren/            Funk, Start & Landung, Formationen …
├── mitmachen/            Anleitung zum Bearbeiten
└── assets/bilder/        Alle Bilder, nach Bereich sortiert
zensical.toml             Einstellungen (Name, Farben, Funktionen)
.github/workflows/        Automatische Veröffentlichung
```

Neue Seiten erscheinen automatisch im Menü, die Reihenfolge ist alphabetisch nach Dateiname.

## Änderungen automatisch in Discord melden (optional)

1. In Discord: *Kanal-Einstellungen → Integrationen → Webhooks → Neuer Webhook*, URL kopieren.
2. In GitHub: *Settings → Webhooks → Add webhook*
   - **Payload URL:** die Discord-Webhook-URL **mit `/github` am Ende**
   - **Content type:** `application/json`
   - Ereignis: *Just the push event*
3. Ab jetzt erscheint jede Änderung am Wiki als Nachricht im Discord-Kanal.

Die Webhook-URL geheim halten: Wer sie kennt, kann in den Kanal posten.

## Lokal ansehen (optional)

```bash
pip install zensical
zensical serve
```

Dann im Browser `http://localhost:8000` öffnen.

## Quellen

- Kneeboard-Karten: [VTOL-VR-Kneeboard](https://github.com/buschwacker/VTOL-VR-Kneeboard) von buschwacker (CC0)
- Flugzeug-Leitfäden: inoffizielle Google Docs aus der Community
