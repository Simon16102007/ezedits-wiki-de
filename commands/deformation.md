# Beschreibung

Alle Unterbefehle sind unter `//ezdeform`  (`//ezd`) \
z.B. `//ezdeform hexagonalize`

## `//ezdeform ...`

### `hexagonalize`

<details>

<summary>Hexagonalize</summary>

**`//ezdeform hexagonalize [größe] [Luftspalt] [x_rotieren] [z_rotieren] [winkel_versatz]`**&#x20;

* **Größe** (Standart: 12): Legt die Größe der Hexagone fest.&#x20;
* **Luftspalt** (Standart: 0.0): Bestimmt die Breite des Luftspalts zwischen den Spalten.&#x20;
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
* **-h**: Wenn verwendet, wird der Bereich nur horizontal verformt.&#x20;
* **-v**: Wenn verwendet, wird der Bereich nur vertikal verformt.

</details>

### `rotate`

<details>

<summary>Rotate</summary>

**`//ezdeform rotate <Winkel> [-o]`**&#x20;

* **Winkel**: Legt den Drehwinkel in Grad fest..&#x20;
* **-o**: Wenn diese Option verwendet wird, wird die Position des Spielers als Rotationszentrum verwendet und nicht das Zentrum der Auswahl..

</details>

### `voronoialize`

<details>

<summary>Voronoialize</summary>

**`//ezdeform voronoialize [größe] [Luftspalt] [-s <seed>]`**

* **Größe** (Standart: 12): Bestimmt die Größe der Voronoi-Zellen.&#x20;
* **Luftspalt** (Standart: 0.0): Gibt die Breite des Luftspalts zwischen den Zellen an.&#x20;
* **-s** (Standart: -1): Optionaler seed für die Erzeugung des Musters.

</details>

### `voronoialize2`

<details>

<summary>Placeholder Name</summary>

**`//ezdeform voronoialize2 <Anzahl> [Luftspalt] [-s <seed>] [-r <seed_Abstoßung>] [-n <normalOffset>]`**

* **Anzahl**: Gibt die Anzahl der Zellen im Voronoi-Muster an.&#x20;
* **Luftspalt** (Standart: 0.0): Bestimmt die Breite des Luftspalts zwischen den Zellen.&#x20;
* **-s** (Standart: -1): Optionaler seedfür die Erzeugung des Musters.&#x20;
* **-r** (Standart: 15): Legt den Abstoßungsfaktor der Voronoi-Setzpunkte fest.&#x20;
* **-n** (Standart: 5): Passt den normalen Versatzfaktor an, der für dünnere Formen verringert werden kann..

</details>

### `voxelize`

<details>

<summary>Voxelize</summary>

**`//ezdeform voxelize <größen> <spalt> <Verzerrung> [-i <primär>] [-j <sekundär>] [-s <seed>] [-hv]`**

* **größen** (Standart: 3,3,3): Legt den Maßstab für jede Dimension fest.&#x20;
* **Spalt** (Standart: 0.0): Bestimmt die Breite des Luftspalts zwischen Voxeln.
* **Verzerrung** (Standart: 0.0): Passt die Stärke der zufälligen Gitterverzerrung an (Bereich: 0-1).&#x20;
* **-i** (Standart: y): Gibt die primäre Achse für die Gitterdrehung an.&#x20;
* **-j** (Standart: -x): Gibt die sekundäre Achse für die Gitterdrehung an.&#x20;
* **-s** (Standart: -1): Optionaler seed für zufällige Verzerrung.&#x20;
* **-h**: Wenn verwendet, wird der Bereich nur horizontal verformt.&#x20;
* **-v**: Wenn verwendet, wird der Bereich nur vertikal verformt.


</details>
