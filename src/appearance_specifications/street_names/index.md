(specs-layer-street-names)=
# Layer - Street Name Signs {bdg-warning}`BETA`

```{note}
The traffic sign type described here is experimental. Use at your own risk!
```

## Specifications

* Font: Arial.

* Color: white as foreground and green as background.

* Border: no additional borders

* The rounded corners are modified into 90 degrees.

* Height: center of the sign height is 1.5 in. (**2.1 in**),

* Width: Currently 4.5 in for id 500-511. (**6.1 in +1.1 in "ST" or 5.5 in + 1.7 in “AVE”**)

* Alphabet =  English upper case. Different writing systems may need different algorithms.

* Text direction: Horizontal for alphabetical languages.

```{todo}
clarify street name conventions
```

### Placement

* **Similar to traffic lights**: The street name should sit on a pole that is based at the corner of the tile outside of the allowable driving region. The bottom of the street name should be at a height of 7in, and allow a Duckiebot to pass through. The street names should be visible from both sides of the road.

Every segment of road must have at least one road name sign.

Every turn tile should have a road name sign.

The placement of the road name signs is as indicated in {numref}`fig:name-placement`).

````{list-table} Placement of Road Name Signs
:name: fig:name-placement

* - ```{figure} ../../_images/appearance_specifications/tiles/name-signs-turn.svg
    :name: subfig:name-signs-turn

    Turn
    ```

  - ```{figure} ../../_images/appearance_specifications/tiles/name-signs-straight.svg
    :name: subfig:name-signs-straight

    Straight
    ```
````

Street name signs should never be perpendicular to the road - they are too big and obtrusive.
