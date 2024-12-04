# Flowfields

Befehle auf der Grundlage des Konzepts der „Flow Fields“, die häufig in der generativen Kunst zu finden sind.

Sie verwenden eine Funktion (in unserem Fall Noise), um eine Reihe von Vektoren entlang eines Gitters oder Feldes zu erzeugen, die bestimmen, wie die Partikel durch dieses Feld fließen.

### `//ezflowfield`

<details>

<summary>Flow Field</summary>

**`//ezflowfield <Palette> <Linien> <Wiederholungen> <Geschwindigkeit> <palettenSkalar> <noise> [-m <Quelle>] [-h <distributionMode>] [-i <Schwungmasse >] [-g <Schwerkraft>] [-j <jitter>] [-b <Begrenzung>] [-x <xMod>] [-y <yMod>] [-z <zMod>] [-p <Fortschritt>] [-s <seed>] [-c] [-f] [-t]`**

**`Alias: //flow`**

Erzeugt ein Flussfeld innerhalb einer Auswahl, das dynamische Muster auf der Grundlage der vielen verfügbaren Parameter erstellt.

* **Palette**: Gibt die Palette der Blöcke an, die bei der Erzeugung des Flowfields verwendet werden sollen.
* **Linien**: Legt die Anzahl der Linien oder eine prozentuale Verteilung fest, um zu bestimmen, wie dicht das Flowfield innerhalb der Auswahl besiedelt ist.\
  e.g `100` wird 100 Linien erzeugen, `100%` erzeugt 1 Linie für jeden Block in der Region.
* **Wiederholungen** (Standart: 32): Die Anzahl der Wiederholungen oder Schritte pro Linie, die bestimmt, wie lang sie sein werden.
* **Geschwindigkeit** (Standart: 1): Die Geschwindigkeit, mit der sich Punkte auf der Oberfläche bewegen.
* **PalettenSkalar** (Standart: 1.0): Skaliert den Wert, der zur Auswahl eines Palettenblocks verwendet wird.
* **Noise** (Standart: `Perlin()`): Die Art des Noise, das zur Erzeugung des Flowfields verwendet wird.
* **-m**: Wendet eine Maske an, um die Startpunkte des Verlaufs zu begrenzen und den Effekt auf bestimmte Bereiche zu konzentrieren.
* **-h**: Aktiviert den Heightmap-Modus zur Erstellung von 2D-flowfields, mit optionalen Blockverteilungsmodi.
* **-i** (Standart: 0.0): Legt die Gewichtung der Schwungkraft des Flusses fest und steuert damit, wie stark frühere Bewegungsrichtungen die nächste beeinflussen.
* **-g** (Standart: (0,0,0) ): Wendet die Schwerkraft auf Punkte an und zieht sie in die angegebene Richtung.
* **-j** (Standart: (0,0,0) ): Fügt Jitter zu den Anfangspunkten von Linien hinzu. Nützlich mit der `-m` Flag. 
* **-b** (Standart: 0): Erweitert den Rechenbereich, ohne Blöcke außerhalb der ursprünglichen Auswahl zu platzieren. Platziert keine Blöcke außerhalb der Auswahl.
* **-x, -y, -z**: Ändert die Koordinaten des Verlaufs, um Transformationen wie Skalierung oder Drehung zu ermöglichen. Nimmt einen WorldEdit-Ausdruck auf, z. B. `-x *10`, um die x-Achse mit 10 zu multiplizieren.
* **-p** (Standart: 1:1): Passt die Stärke der Linie im Verlauf an, akzeptiert negative Werte, um entweder auf einer Punktstärke zu beginnen oder zu enden, die vom flow field abgezogen wird.
* **-s** (Standart: -1): Überschreibt den standardmäßige Noise seed.
* **-c**: Gibt die Krümmung des Feldes zurück.
* **-f**: Füllt Lücken mit dem niedrigsten Block in der Palette.
* **-t**: Erzeugt stattdessen ein 3D-flowfield. Die Generierung kann sehr viel Zeit in Anspruch nehmen.

</details>

### `//ezflowline`

<details>

<summary>Flow Line</summary>

**`/ezflowline <Muster> <Länge> <Schwerkraft> <Noise> [-i <Schwungkraft>] [-c <convexSelPoints>] [-s]`**

**`Alias: //flowline`**

Erzeugt eine einzelne Flow-Line basierend auf der Position und Blickrichtung des Spielers.\
Dieselbe Grundvoraussetzung wie ein Flow Field, aber es wird nur 1 Linie erzeugt.

* **Muster**: Bestimmt das Muster der zu platzierenden Blöcke.&#x20;
* **Länge**: Legt die Länge der flowline in Blöcken fest. Damit wird festgelegt, wie weit sich die Stromlinie vom Startpunkt aus erstreckt.
* **Schwerkraft** (Standart: -1): Wendet die Schwerkraft auf Punkte an und zieht sie in die angegebene Richtung.
* **Noise** (Standart: `Perlin()`): Die Art des Noise, das zur Erzeugung des flowfield verwendet wird.
* **-i** (Standart: 0.0): Passt die Wichtung der punktförmigen Masse an und steuert, wie stark frühere Bewegungsrichtungen zukünftige Richtungen beeinflussen. Ein Wert zwischen 0,0 und 1,0.
* **-c** (Standart: 0): Ist dieser Wert größer als 0, wird eine convex Auswahl aus der flowline erstellt, wobei die angegebene Anzahl von Punkten zur Definition der Form der Auswahl verwendet wird.
* **-s**: Ermöglicht das Ausrichten der flowline an Oberflächen, so dass die Linie an den Konturen der Landschaft oder der Strukturen, die sie schneidet, haften bleibt.

</details>
