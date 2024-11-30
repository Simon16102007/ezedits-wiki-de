# Beschreibung

Alle Unterbefehle sind unter `//ezdeform`  (`//ezd`) \
z.B. `//ezdeform hexagonalize`

## `//ezdeform ...`

### `hexagonalize`

<details>

<summary>Hexagonalize</summary>

**`//ezdeform hexagonalize [größe] [Luftspalt] [x_rotieren] [z_rotieren] [winkel_versatz]`**&#x20;

* **Größe** (Standart: 12): Legt die Größe der Hexagone fest.&#x20;
* **Luftspalte** (Standart: 0.0): Bestimmt die Breite des Luftspalts zwischen den Spalten.&#x20;
* **X Rotation** (Standart: 0.0): Legt den Drehwinkel der Spalte entlang der X-Achse fest, in Grad.&#x20;
* **Z Rotation** (Standart: 0.0): Legt den Drehwinkel der Spalte entlang der Z-Achse fest, in Grad.&#x20;
* **Winkel versatz** (Standart: 60.0): Passt den Versatzwinkel an und steuert die Form (Bereich: 0-90 Grad).

</details>

### `noise`

<details>

<summary>Noise</summary>

**`//ezdeform noise <noise> [stärke] [-z <größe>] [-s <seed>]`**

* **Noise**: Gibt die Art des für die Verformung zu verwendenden Noise an.&#x20;
* **Stärke** (Standart: 2.0): Legt die Stärke des Noise effekts fest.&#x20;
* **Größe** (Standart: 1): Bestimmt das Ausmaß des Noise.&#x20;
* **-s** (Standart: -1): Optionaler seed für das Noisemuster.&#x20;
* **-h**: Wenn verwendet, wird der Bereich nur horizontal verformt..&#x20;
* **-v**: Wenn verwendet, wird der Bereich nur vertikal verformt.

</details>

### `rotate`

<details>

<summary>Rotate</summary>

**`//ezdeform rotate <angle> [-o]`**&#x20;

* **Angle**: Sets the angle of rotation, in degrees.&#x20;
* **-o**: When used, uses the player's position as the center of rotation instead of the selection's center.

</details>

### `voronoialize`

<details>

<summary>Voronoialize</summary>

**`//ezdeform voronoialize [size] [air_gap] [-s <seed>]`**

* **Size** (Default: 12): Determines the size of the voronoi cells.&#x20;
* **Air Gap** (Default: 0.0): Specifies the width of the air gap between cells.&#x20;
* **-s** (Default: -1): Optional seed for generating the pattern.

</details>

### `voronoialize2`

<details>

<summary>Placeholder Name</summary>

**`//ezdeform voronoialize2 <amount> [air_gap] [-s <seed>] [-r <seed_repulsion>] [-n <normalOffset>]`**

* **Amount**: Specifies the cell amount in the voronoi pattern.&#x20;
* **Air Gap** (Default: 0.0): Determines the width of the air gap between cells.&#x20;
* **-s** (Default: -1): Optional seed for generating the pattern.&#x20;
* **-r** (Default: 15): Sets the voronoi seed point repulsion factor.&#x20;
* **-n** (Default: 5): Adjusts the normal offset factor, which can be decreased for thinner shapes.

</details>

### `voxelize`

<details>

<summary>Voxelize</summary>

**`//ezdeform voxelize <scales> <gap> <distortion> [-i <primary>] [-j <secondary>] [-s <seed>] [-hv]`**

* **Scales** (Default: 3,3,3): Sets the scale for each dimension.&#x20;
* **Gap** (Default: 0.0): Defines the width of the air gap between voxels.
* **Distortion** (Default: 0.0): Adjusts the strength of random grid distortion (range: 0-1).&#x20;
* **-i** (Default: y): Specifies the primary axis for grid rotation.&#x20;
* **-j** (Default: -x): Specifies the secondary axis for grid rotation.&#x20;
* **-s** (Default: -1): Optional seed for random distortion.&#x20;
* **-h**: When used, only voxelizes horizontally.&#x20;
* **-v**: When used, only voxelizes vertically.

</details>
