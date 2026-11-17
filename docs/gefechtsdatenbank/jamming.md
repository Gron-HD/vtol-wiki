# Jamming

Jamming bedeutet, gegnerische Radare gezielt zu stören (Teil der elektronischen Kampfführung, EloKa).

Zusammenfassung des [Jamming & Radar Tutorials](https://www.youtube.com/watch?v=4b5b-U3Gz8U) zu den neuen Radar- und Jammer-Funktionen in **Update 1.8**.

!!! tip "Kurz gesagt"
    - **Radar:** Höhenanzeige, Scan in Reihen, einstellbarer Cursor, B-Scope-Ansicht, manueller Slew-Modus und Raketenstart schon mit Soft Lock.
    - **Jammer:** bis zu 4 Ziele, Band je nach Zieltyp, drei Zuweisungsmodi (A-RAD, TGP, GPS), aber **kein Radar während des Störens**.
    - **Selbst gestört:** einen schon bestehenden Hard Lock halten, sonst auf die Störsignatur schießen.

## Änderungen am Radar

### Höhenanzeige

Neben jedem Kontakt steht jetzt seine Höhe in Tausend Fuß (z. B. „23“ = 23.000 ft). Wenn man ein Ziel anklickt, steht derselbe Wert auch unter „A“ (Angels).

### Neues Scan-Muster

Früher hat das Radar den ganzen Bereich wie ein Kegel horizontal abgetastet. Jetzt scannt es in **Reihen (Bars)**: Es beginnt unten und arbeitet sich automatisch Reihe für Reihe nach oben. Die Leiste links mit dem wandernden Marker zeigt, welche Reihe gerade gescannt wird.

!!! note
    Ein Ziel in großer Höhe (z. B. 50.000 ft) kann deshalb 2–3 Sekunden brauchen, bis es erscheint.

### Radar-Optionen

| Option | Einstellungen | Wirkung |
| ------ | ------------- | ------- |
| **Cursor Speed** | 40–100 (Standard 60) | Wie schnell sich der grüne Doppelstrich-Cursor bewegt |
| **Display** | PPI (Standard) / B-Scope | PPI ist die gewohnte Kegelansicht. B-Scope zeigt dasselbe als Quadrat, laut Autor ohne funktionalen Unterschied. |
| **FOV-Modus** | Auto / Slew | Siehe unten |

**Auto:** Das Radar scannt automatisch den ganzen Himmel ab, Ziele sind also grundsätzlich immer sichtbar.

**Slew (manuell):** Mit dem linken Thumbstick stellt man zuerst den Abstand der Bars ein und schiebt dann den ganzen Block nach oben oder unten (z. B. nur 32.000–60.000 ft oder 0–23.000 ft).

!!! warning
    Im Slew-Modus werden Ziele außerhalb des eingestellten Höhenbereichs **nicht angezeigt**. Man muss also den richtigen Teil des Himmels absuchen.

### Soft Lock und Hard Lock

- Einfacher Klick = **Soft Lock** (das Ziel wird nummeriert markiert und im HUD angezeigt). Doppelklick = **Hard Lock** (eine Linie zum Ziel erscheint).
- Mehrere Soft Locks gab es schon vorher. Neu ist ein **Stern**, der das gerade ausgewählte Ziel markiert.

!!! tip "Wichtigste Neuerung"
    Radargelenkte Raketen kann man jetzt schon mit einem ausgewählten **Soft Lock** abfeuern. Ein Hard Lock ist dafür nicht mehr nötig.

## Das Jammer-Modul

![Jammer-Seite im MFD](../assets/bilder/gefechtsdatenbank/jamming/jammer-mfd.png){ width="480" }
/// caption
Die Jammer-Seite im MFD.
///

Je nach Anzahl der montierten Jammer-Pods (0, 1 oder 2) sieht man entsprechend viele Blöcke. Jeder Pod hat zwei Knoten (Balken), und jeder Knoten stört ein eigenes Ziel. Mit zwei Pods kann man also **bis zu 4 Ziele gleichzeitig** stören.

### Frequenzbänder

| Band | Wirkt gegen | Verfügbarkeit |
| ---- | ----------- | ------------- |
| **High** | Flak (AAA), Missile-Warning-Truck, eigenes Radar der AIM-120, sobald sie „pitbull“ geht (also auf ihr eigenes Radar umschaltet) | F/A-26, F-45, T-55 |
| **Mid** | Flugzeugradare und SAM-Radare | F/A-26, F-45, T-55 |
| **Low** | Funk (auch In-Game-Voice-Chat) und GPS, möglicherweise auch GPS-gelenkte Munition | nur EF-24 und GECM-Truck |

### Zielzuweisung

=== "A-RAD"

    1. Auf der A-RAD-Seite ein Emitter-Ziel (z. B. eine Radarschüssel) auswählen.
    2. Zur Jammer-Seite wechseln, den gewünschten Knoten auswählen und **A-RAD** drücken. Ein weißes Kästchen zeigt das zugewiesene Ziel an, der Status lautet „DS“ (Dish Site) / Standby.
    3. **Start** drücken, der Knoten sendet jetzt (Transmit). Auf der A-RAD-Seite sieht man den Störstrahl.
    4. Für bis zu vier Knoten wiederholen, so lassen sich vier Stellungen unabhängig voneinander stören. Mit zwei Bildschirmen geht das bequemer.

    **Stoppen oder Leistung umverteilen:** Einen Knoten auswählen und **Stop** drücken. Oder mit dem Power-Regler links/rechts die Leistung komplett von Knoten A auf B (oder umgekehrt) verschieben. Dabei bleibt die Zielzuweisung erhalten.

=== "TGP"

    - Gestört wird immer der Punkt, auf den der Zielbehälter (TGP) gerade zeigt: Ziel mit dem TGP aufschalten, auf der Jammer-Seite **TGP** wählen, **Start** drücken.
    - Schwenkt man den TGP auf ein anderes Ziel, wandert der Störstrahl mit.
    - **Nur ein Ziel gleichzeitig** möglich.

=== "GPS"

    - Auf der GPS-Seite den gewünschten Punkt auswählen (grün markiert), auf der Jammer-Seite **GPS** wählen und **Start** drücken.
    - Für weitere Punkte wiederholen, **bis zu 4 GPS-Ziele** gleichzeitig.
    - Die Ziele bleiben gespeichert: Fliegt man aus dem Abdeckungsbereich und dreht wieder um, beginnt das Stören automatisch neu. Man muss nichts neu erfassen.

!!! note "Abdeckung"
    Wie beim TGP muss das Ziel ungefähr **vor dem Flugzeug** liegen. Ziele hinter einem gehen verloren.

!!! danger "Stören oder Radar, beides geht nicht"
    Solange der Jammer aktiv ist, zeigt das eigene Radar **„Jammer On“** und **keine Ziele** an. Erst nach dem Stoppen funktioniert das Radar wieder.

## Wenn man selbst gestört wird

Getestet in einer Multiplayer-Lobby, frontal aufeinander zufliegend:

- Der störende Gegner ist auf dem Radar **nicht sichtbar**, obwohl er klar in Reichweite ist.
- **Zweischneidig:** Man kann die Störsignatur aufschalten und eine Rakete darauf abfeuern. Das ist keine echte Lenkung, die Rakete fliegt nur grob in Richtung des Störers. Sie kann aber eventuell genug Radarsignal durchbekommen, um das Ziel doch noch zu erfassen.
- **Bestehender Hard Lock:** Wer schon vor Beginn des Störens einen Hard Lock hatte, behielt ihn nach Erfahrung des Autors. Es war, als würde gar nicht gestört.
- **Soft Lock** geht dagegen sofort verloren. Während des Störens einen neuen Soft oder Hard Lock zu bekommen, ist praktisch unmöglich.

## Quellen

- :fontawesome-brands-youtube: [Video: Jamming & Radar Tutorial](https://www.youtube.com/watch?v=4b5b-U3Gz8U)
- :lucide-book-open: [VTOL VR Wiki: Electronic Warfare (Mechanic)](https://vtolvr.wiki.gg/wiki/Electronic_Warfare_(Mechanic)), mehr oder weniger nützlich
