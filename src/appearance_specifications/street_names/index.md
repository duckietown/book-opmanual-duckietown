(specs-layer-street-names)=
# Layer - Street Name Signs {bdg-warning}

```{attention}
The traffic sign type described here is experimental. Use at your own risk!
```

Street names are non functional (i.e., they are not hardcoded in any Duckiebot behavior), but can add a pleasing outreach element to the city.

```{tip}
Especially if you are an Assistant Professor, you should consider dedicating the main avenue of your Duckietown to your Department Head. 
```

## Specifications

* Font: Arial.
* Alphabet =  English upper case. Different writing systems may need different algorithms.
* Color: white as foreground and green as background.
* Border: no additional borders.
* Width: Currently 4.5 in for id 500-511. (**6.1 in +1.1 in "ST" or 5.5 in + 1.7 in “AVE”**)
* Text direction: Horizontal for alphabetical languages.

### Placement

Street name signs should be placed outside of the allowable driving region. The street names should be visible from both sides of the road.

If you chose to adopt signs, every segment of road must have at least one road name sign.

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
