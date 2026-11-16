# Mitmachen

Jede Seite ist eine einfache Textdatei im Format **Markdown** (`.md`). Du brauchst nur einen GitHub-Account und musst als Mitarbeiter im Repository eingetragen sein.

## Eine Seite bearbeiten

1. Auf der Wiki-Seite oben rechts auf den :lucide-pencil: **Stift** klicken.
2. GitHub öffnet die Datei im Editor. Text ändern, mit **Preview** kontrollieren.
3. Auf **Commit changes…** klicken, kurz beschreiben, was du geändert hast, und bestätigen.
4. Nach ca. 1–2 Minuten ist die Änderung live.

## Neue Seite anlegen

1. Im Repository in den passenden Ordner unter `docs/` gehen, z. B. `docs/flugzeuge/`.
2. **Add file → Create new file**, Namen vergeben, z. B. `f-45a.md`. Bitte nur Kleinbuchstaben, Zahlen und Bindestriche verwenden.
3. Die erste Zeile ist die Überschrift: `# F-45A`.
4. Die Seite erscheint automatisch im Menü. Gern auch in der Übersichtstabelle des Bereichs verlinken.

## Bilder hochladen

1. In `docs/assets/bilder/` auf **Add file → Upload files** klicken.
2. Im Text einbinden (Pfad relativ zur Seite):

```markdown
![Beschreibung](../assets/bilder/mein-screenshot.png)
```

## Spickzettel

=== "Tabelle"

    ```markdown
    | Spalte A | Spalte B |
    | -------- | -------- |
    | Wert 1   | Wert 2   |
    ```

    | Spalte A | Spalte B |
    | -------- | -------- |
    | Wert 1   | Wert 2   |

=== "Hinweis-Box"

    ```markdown
    !!! tip "Titel"
        Text der Box, mit 4 Leerzeichen eingerückt.
    ```

    !!! tip "Titel"
        Text der Box, mit 4 Leerzeichen eingerückt.

    Weitere Typen: `note`, `info`, `warning`, `danger`, `example`.
    Mit `???` statt `!!!` wird die Box einklappbar.

=== "Checkliste"

    ```markdown
    - [ ] offen
    - [x] erledigt
    ```

    - [ ] offen
    - [x] erledigt

=== "Text"

    ```markdown
    **fett**, *kursiv*, ==markiert==
    [Link](https://example.com)
    Taste: ++ctrl+s++
    ```

    **fett**, *kursiv*, ==markiert==
    [Link](https://example.com)
    Taste: ++ctrl+s++

!!! info "Tabellen bequem erstellen"
    Größere Tabellen am einfachsten in Excel/Google Sheets bauen und mit einem Konverter wie *tableconvert.com* in Markdown umwandeln.
