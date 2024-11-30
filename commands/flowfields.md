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
* **Noise** (Standart: `Perlin()`): The type of noise used to generate the flowfield.
* **-m**: Applies a mask to limit the flow's start points, focusing the effect on specific areas.
* **-h**: Enables heightmap mode for creating 2D flowfields, with optional block distribution modes.
* **-i** (Standart: 0.0): Sets the inertia weighting of the flow, controlling how much previous movement directions influence the next.
* **-g** (Standart: (0,0,0) ): Applies gravity to points, pulling them in the specified direction.
* **-j** (Standart: (0,0,0) ): Adds jitter to the start points of lines. Useful with `-m` flag.
* **-b** (Standart: 0): Expands the calculation boundary without placing blocks outside the original selection. Does not place blocks outside the selection.
* **-x, -y, -z**: Modify the coordinates of the flow, allowing for transformations like scaling or rotation. Takes in a WorldEdit expression, e.g `-x *10` to multiply the x axis by 10.
* **-p** (Standart: 1:1): Adjusts the strength of the line as it progresses, accepts negative values to either start or end on a point strength that subtracts from the flow field.
* **-s** (Standart: -1): Overrides the default noise seed.
* **-c**: Returns the curl of the field.
* **-f**: Fills gaps with the lowest block in the palette.
* **-t**: Generates a 3D flowfield instead. May require a lot of time to generate.

</details>

### `//ezflowline`

<details>

<summary>Flow Line</summary>

**`/ezflowline <pattern> <length> <gravity> <noise> [-i <inertia>] [-c <convexSelPoints>] [-s]`**

**`Alias: //flowline`**

Generates a single flow-line based on the actor's position and viewing direction.\
The same fundamental premise as a Flow Field, but only generating 1 line.

* **Pattern**: Determines the pattern of blocks to place.&#x20;
* **Length**: Sets the length of the flowline in blocks. This defines how far the flowline will extend from the starting point.
* **Gravity** (Standart: -1): Applies gravity to points, pulling them in the specified direction.
* **Noise** (Standart: `Perlin()`): The type of noise used to generate the flowfield.
* **-i** (Standart: 0.0): Adjusts the point inertia weighting, controlling how much previous movement directions influence future directions. A value between 0.0 and 1.0.
* **-c** (Standart: 0): If greater than 0, creates a convex selection out of the flowline, using the specified number of points to define the selection's shape.
* **-s**: Enables snapping of the flowline to surfaces, making the line adhere to the contours of the landscape or structures it intersects.

</details>
