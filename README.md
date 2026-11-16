# VTOL VR Squadron Wiki

Wiki der Squadron, gebaut mit [Zensical](https://zensical.org) und gehostet auf GitHub Pages.
Die Inhalte liegen im Ordner `docs/`. Eine Anleitung zum Bearbeiten steht im Wiki unter **Mitmachen**.

## Einmalige Einrichtung

1. **Repository anlegen:** Auf GitHub ein neues, öffentliches Repository `vtol-wiki` erstellen.
2. **Dateien hochladen:** Den Inhalt dieses Ordners hochladen (*Add file → Upload files*).
   Wichtig: Der versteckte Ordner `.github/` muss mit hoch. Falls der Browser-Upload ihn nicht mitnimmt,
   die Datei `.github/workflows/docs.yml` per *Add file → Create new file* mit genau diesem Pfad anlegen und den Inhalt hineinkopieren.
3. **Pages aktivieren:** *Settings → Pages → Build and deployment → Source:* **GitHub Actions** wählen.
4. **Platzhalter ersetzen:** In `zensical.toml` überall `DEIN-GITHUB-NAME` durch deinen GitHub-Namen ersetzen.
   Heißt das Repository anders als `vtol-wiki`, auch das anpassen.
5. Nach 1–2 Minuten ist das Wiki erreichbar unter `https://DEIN-GITHUB-NAME.github.io/vtol-wiki/`
   (Fortschritt im Tab *Actions*).

## Weitere Bearbeiter hinzufügen

*Settings → Collaborators → Add people* und GitHub-Namen eintragen. Die Person muss die Einladung annehmen.

## Änderungen automatisch in Discord melden (optional)

1. In Discord: *Kanal-Einstellungen → Integrationen → Webhooks → Neuer Webhook*, URL kopieren.
2. In GitHub: *Settings → Webhooks → Add webhook*
   - **Payload URL:** die Discord-Webhook-URL **mit `/github` am Ende**
   - **Content type:** `application/json`
   - Ereignis: *Just the push event*
3. Ab jetzt erscheint jede Änderung am Wiki als Nachricht im Discord-Kanal.

Die Webhook-URL geheim halten: Wer sie kennt, kann in den Kanal posten.

## Lokal ansehen (optional, nur für Technik-Interessierte)

```bash
pip install zensical
zensical serve
```

Dann im Browser `http://localhost:8000` öffnen.
