```{seo}
:description: Learn step-by-step assembly of Duckietown road tiles, including straight, curved, and intersection segments, for compliant and functional layouts.
:keywords: Duckietown, road tiles, assembly guide, robotics, Duckiebots, intersections, curved roads, straight roads, robotics education, tilemap, smart city
```

(dt-ops-tiles)=
# Assembly - Road Tiles

```{needget}
* Knowledge of the [Duckietown Appearance Specifications](book)
* Materials: compliant tiles, white, yellow and red road markings ([Duckietown project shop](https://get.duckietown.com/products/duckietown-navigation-starter-pack))
* Tools: scissors (or a sharp cutter) and a ruler
---
* You will have tiles that comply with the Duckietown operation standards
* You can move on to [Assembly of other components](#dt-ops-assembly)
```

(dt-ops-tiles-foreword)=
## Before we begin 
```{tip}
To ensure that your streets will last long, make sure to follow these steps: 
* Clean the tiles with a mixture of water and soap, or alcohol, and let them dry completely before attaching tapes.
* Place the yellow tape on the tile and cut out pieces rather than pre-cutting them. This ensures proper adhesion by preventing loss of glue.
```

(dt-ops-tiles-straight)=
## Straight Roads

Each straight road segment has:

- Solid white markings on the outer sides of the lanes (right of the direction of travel).
- Dashed yellow markings at the center.
- Each lane is 21 cm wide (from the end of the white to the beginning of the yellow).

(dt-ops-tiles-straight-assembly)=
### Assembly

Refer to {numref}`fig:tile_instruction_straight_3` for the following steps:

1. Place the yellow tape in the middle of the tile
2. Ensure the yellow tape is properly centered, with a distance of 27.25 cm from the tape’s edge to the tile's edge
3. Cut the yellow tape into 2.5 cm pieces, starting 5 cm from the tile's outer edge.
4. Add white lane markings at the outer parts of the tile, 21 cm from the yellow tape

```{figure} ../../_images/assembly/tilemap/instructions/straight_3_done_arrows.png
:width: 80%
:name: fig:tile_instruction_straight_3
:align: center
:alt: Assembled straight Duckietown tile with measurements

Finished straight road segment with measurements.
```

(dt-ops-tiles-curves)=
## Curved Roads

Each curved road segment has:

- Solid white markings on the outer sides of the lanes (right of the direction of travel).
- Dashed yellow markings at the center.
- Each lane is 21 cm wide (from the end of the white to the beginning of the yellow).

```{figure} ../../_images/appearance_specifications/tiles/curved_appearance_spec.png
:width: 80%
:name: fig:tile_instruction_curved_3-2
:align: center
:alt: Assembled curved Duckietown tile with measurements


Final result: curved Duckietown tile (with measurements)
```

(dt-ops-tiles-curves-assembly)=
### Assembly

If you have a laser cutter, use the provided [Duckietown curve tile construction template](https://github.com/duckietown/docs-opmanual_duckietown/tree/daffy/book/opmanual_duckietown/TileTemplates/CurvedTileTemplate) to proceed more swiftly and precisely in the assembly process. 

```{figure} ../../_images/assembly/tilemap/instructions/curved_1_done.png
:width: 80%
:name: fig:curved-tile-template-usage
:align: center
:alt: How to use the Duckietown curve tile construction template

Using the provided construction template makes building Duckietown curve tiles more joyful
```

Without construction template, mark a quarter-circle path for the yellow tape using a string. Follow the guidelines for tape placement and lane width measurements in {numref}`fig:tile_instruction_curved_3`.

```{figure} ../../_images/assembly/tilemap/instructions/curved_3_done.png
:width: 80%
:name: fig:tile_instruction_curved_3
:align: center
:alt: Building a curved Duckietown tile, first lane


Start from the yellow line and then measure the lane width to determine the position of the white tape 
```

```{figure} ../../_images/assembly/tilemap/instructions/curved_5_done.png
:width: 80%
:name: fig:tile_instruction_curved_5
:align: center
:alt: Building a curved Duckietown tile, second lane


Take 3-5 measurement points across the quarter-circumference to identify the location of the outer lane white tape. Aim to having the correct lane width but do not overdo it, autonomy algorithms should be robust to small variations of lane widths. 
```

(dt-ops-tiles-intersections)=
## Intersections

Each intersection (3- or 4-way) has:

- Solid white markings on the outer sides of the lanes.
- Dashed yellow markings at the center.
- Solid red markings for stop signs.
- Each lane is 21 cm wide.

### Assembly of 4-Way Intersection

1. Place four yellow tape strips, centered and extending 6 cm from the tile’s edge.
2. Align red tape horizontally with the edge and cut it to 21 cm, as shown in {numref}`fig:tile_instruction_4way_7`.
3. Cut yellow markings into 5 cm pieces and add white tape at the corners.

```{figure} ../../_images/assembly/tilemap/instructions/4way_7_done.png
:width: 80%
:name: fig:tile_instruction_4way_7
:align: center
:alt: Assembled 4-way Duckietown intersection tile


4-way intersection road segment.
```

### Assembly of 3-Way Intersection

3-way intersections follow the same process, except one edge uses white tape instead of red and yellow. The result can be seen in {numref}`fig:tile_instruction_3way_1`.

```{figure} ../../_images/assembly/tilemap/instructions/3way_1_done.png
:width: 80%
:name: fig:tile_instruction_3way_1
:align: center
:alt: Assembled 3-way Duckietown intersection tile


3-way intersection road segment.
```

(dt-ops-tiles-troubleshooting)=
### Troubleshooting

```{trouble}
My tape tends to detach from the tiles. The glue is no good.
---
Follow these steps:
1. Clean tiles with a water and alcohol solution to remove residual oils, and dry them completely.
2. Apply tape directly to the tiles and cut on-site to maintain glue strength.
3. Use a heat source (e.g., a hair dryer) to warm the tape after application, softening the glue for better adhesion.
```


