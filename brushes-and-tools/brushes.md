# Brushes

Alle Brushes sind unter dem `//ezbrush ...` (`//ezbr`) Command enthalten.



## `//ezbrush ...`

### `gradient`

<details>

<summary>Gradient Brush</summary>

**`//ezbr gradient <Palette> [Radius] [Interpolation] [stärke] [-av] [-n <noise>] [-z <größe>] [-d <Distanz Funktion>]`**

Mit dem `gradient` brush können sie zunächst mit 2 Punkten eine Fläche definieren, innerhalb dieser Fläche kann mit einer gewünschten Blockpalette gemalt werden, die abstände zwischen den verschiedenen Blockarten wird durch die makierte Distanz bestimmt.

**<u>Linksklick</u> um eine Fläche an Ihrem Zielblock zu starten**\
**<u>Schleichen + Linksklick</u> um eine Fläche an der Spieler Position zu starten**\
**<u>Rechtsklick</u> um das Ende der Ebene am Zielblock festzulegen ODER um zu malen wenn die Fläche bereits festgelegt ist**\
**<u>Schleichen + Rechtsklick</u> um das Ende an der Spieler Position festzulegen ODER um zu malen wenn die Fläche bereits festgelegt ist**\
**<u>Zweithand Tauschen (Standart Taste F)</u> um zwischen GLOBAL und PER_ITEM aktiven Farbverläufen umzuschalten**

* **Palette**: Gibt die Palette für den Farbverlauf an.
* **Radius** (Standart: 8): Legt den Radius des Brushes fest.
* **Interpolation** (Standart: KEINE): Bestimmt die Art der Interpolation, die für den Farbverlauf verwendet wird.
* **Stärke** (Standart: 0.5): Stellt die Stärke der Interpolation ein, mit einem normalen Bereich von 0 bis 1.
* **-a**: Wenn aktiviert, kann der Gradient Luftblöcke ersetzen.
* **-v**: Deaktiviert die WorldEditCUI-Integration.
* **-n \<noise>** (Standart: `Weiß()`): Fügt dem Farbverlauf ein zugrunde liegendes Rauschen hinzu.
* **-z \<größe>** (Standart: 1): Bestimmt die größe des Rauschens.
* **-d \<Distanz Funktion>** (Standart: KEINE): Legt den Abstandsmodus fest, der den Pinsel so verändert, dass er auf der Grundlage des Abstands zum Ausgangsblock mit der angegebenen Abstandsfunktion arbeitet.

</details>

### `gradientstroke`

<details>

<summary>Gradient Stroke Brush</summary>

**`//ezbr gradientstroke <Palette> [Radius] [Interpolation] [stärke] [-adv] [-n <noise>] [-z <größe>]`**

Der `gradientstroke` brush erlaubt die Anwendung von Farbverläufen entlang eines durch die Auswahl von Punkten definierten Pfades (Strich).

**<u>Linksklick</u> um Punkte hinzuzufügen**\
**<u>Schleichen + Left Click</u> Um den letzten Punkt zu entfernen**\
**<u>Rechtsklick</u> um zu Bestätigen und den gradient stroke zu plazieren**\
**<u>Schleichen + Rechtsklick</u> um alle Punkte zu Löschen**\
**<u>Zweithand Tauschen (Standart Taste F)</u> Um zwischen GLOBAL und PER_ITEM zu wechseln**

* **Palette**: Gibt das Blockmuster für den Farbverlauf an.
* **Radius** (Standart: 8): Legt den Radius des Brushes fest.
* **Interpolation** (Standart: LINEAR): Bestimmt die Art der Interpolation, die für den Gradientenübergang verwendet wird.
* **Stärke** (Standart: 0.5): Stellt die Stärke der Interpolation ein, mit einem normalen Bereich von 0 bis 1.
* **-a**: Wenn aktiviert, kann der Gradient Luftblöcke ersetzen.
* **-d**: Aktiviert den Modus 'Abstand zur Mitte', der den Farbverlauf auf der Grundlage des Abstands zur Mitte der Strichlinie statt des Abstands entlang des Strichs verwendet.
* **-v**: Deaktiviert die WorldEditCUI-Integration.
* **-n \<noise>** (Standart: `Weiß()`): Fügt dem Gradienteneffekt ein zugrunde liegendes Noise hinzu.
* **-z \<scale>** (Standart: 1): Ändert die Skala des Noise.

</details>

### `paletteshift`

<details>

<summary>Palette Shift Brush</summary>

**`//ezbr paletteshift <Palette> [Radius] [Änderung]`**

Ersetzt Blöcke, die der Palette entsprechen, durch Palettenblöcke, die um den angegebenen Wert verschoben sind.
Bei einem Verschiebungswert von 2 werden zum Beispiel alle Objekte des ersten Palettenblocks durch den dritten ersetzt.

* **Palette**: Gibt das Blockmuster für den Farbverlauf an.
* **Radius** (Standart: 8): Legt den Radius des Brushes fest.
* **Änderung** (Standart: 1): Der Betrag, um den Blöcke innerhalb der Palette verschoben werden sollen

</details>
