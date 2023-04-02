(specs-layer-traffic-signs)=
# Layer - Traffic Signs

The signals layer is made of [traffic signs](dt-ops-city-traffic-signs).

Traffic signs sit on the road layer, outside the lanes, and can serve multiple purposes.

```{seealso}
The full set of currently existing signs is available 
[here](https://github.com/duckietown/signs-and-tags).
```

## Functional purposes

Some examples of uses of traffic signs that have a function 
(these functions are encoded in some Duckietown legacy behaviors):

```{note}
Traffic signs:
* identify the type of intersection (3- or 4-way);
* identify the position of the Duckiebot at the intersection;
* inform the Duckiebot of the coordination mechanism for this specific intersection (centralized or decentralized).
```
## Non-functional purposes

Traffic signs can be used for other purposes 
(these functions are not encoded in any Duckietown out-of-the-box behavior):

```{note}
Traffic signs can moreover be used for:
* naming roads (and making the department head happy);
* identifying pedestrian traffic areas;
* identifying parking lots.
```

---

Traffic signage in Duckietown is obtained through the union of traffic signs and 
`AprilTag` visual markers, as shown in {numref}`fig:traffic-sign-example`.

```{figure} ../../_images/appearance_specifications/signs/traffic-sign-example.png
:name: fig:traffic-sign-example
:width: 80%

A traffic sign in Duckietown (do not print this one out!)
```

We call the symbol above _traffic sign_, while the code below is an AprilTag.

```{note}
To print and assemble the signs refer to [](dt-ops-city-traffic-signs).
```

## Specifications

For traffic signage to be compliant:

* The center of the traffic signs is 13 cm height from the floor layer;
* The AprilTag is 6.5 cm sq.;
* There is a white border of roughly 0.8 cm around them;
* The signage stands perpendicular to the ground, and the angle of the sign with the road is $90^ \circ$.
* The signal is flat (no deformation / folding) and without wrinkles. This can be obtained, e.g., by printing the signs on thick paper.

## Types

The allowable traffic signs are as in {numref}`tab:traffic-signs`.

````{list-table} Duckietown Traffic Signs
:name: tab:traffic-signs

* - ```{figure} ../../_images/appearance_specifications/signs/stop.png
    :name: subfig:stop
    :width: 80%

    stop
    ```
  - ```{figure} ../../_images/appearance_specifications/signs/yield.png
    :name: subfig:yield
    :width: 80%

    yield
    ```
  - ```{figure} ../../_images/appearance_specifications/signs/no-right.png
    :name: subfig:no-right
    :width: 80%

    no-right-turn
    ```

* - ```{figure} ../../_images/appearance_specifications/signs/no-left.png
    :name: subfig:no-left
    :width: 80%

    no-left-turn
    ```
  
  - ```{figure} ../../_images/appearance_specifications/signs/no-enter.png
    :name: subfig:no-enter
    :width: 80%

    do-not-enter
    ```

  - ```{figure} ../../_images/appearance_specifications/signs/one-way-right.png
    :name: subfig:one-way-right
    :width: 80%

    one-way-right
    ```
* - ```{figure} ../../_images/appearance_specifications/signs/one-way-left.png
    :name: subfig:one-way-left
    :width: 80%

    one-way-left
    ```
  - ```{figure} ../../_images/appearance_specifications/signs/4-way.png
    :name: subfig:4-way-intersect
    :width: 80%

    4-way-intersect
    ```

  - ```{figure} ../../_images/appearance_specifications/signs/3-way-right.png
    :name: subfig:3-way-right
    :width: 80%

    right-T-intersect
    ```
* - ```{figure} ../../_images/appearance_specifications/signs/3-way-left.png
    :name: subfig:3-way-left
    :width: 80%

    left-T-intersect
    ```
  - ```{figure} ../../_images/appearance_specifications/signs/t-intersection.png
    :name: subfig:t-intersection
    :width: 80%

    t-intersection
    ```

  - ```{figure} ../../_images/appearance_specifications/signs/crossing.png
    :name: subfig:crossing
    :width: 80%

    pedestrian
    ```
* - ```{figure} ../../_images/appearance_specifications/signs/traffic-light.png
    :name: subfig:traffic-light
    :width: 80%

    t-light-ahead
    ```
  - ```{figure} ../../_images/appearance_specifications/signs/duckie-crossing.png
    :name: subfig:duckie-crossing
    :width: 80%

    duck-crossing
    ```

  - ```{figure} ../../_images/appearance_specifications/signs/parking.png
    :name: subfig:parking
    :width: 80%

    parking
    ```
  
  
````

(traffic-signs-placement)=
## Placement

Signs may appear on the opposite side and at the corner of the adjacent tile from which they are viewed. In the absence of any signs, it is assumed that all network flows are allowed so a sign MUST be placed and visible whenever this is not the case.

Signs must only be placed on empty tiles, or next to one of the other tile types if on the border of a map. As mentioned, it is important to not overlap the base of the sign stand with any road marking.

The sign placements for four different cases are shown in {numref}`tab:sign-placement`. At intersections, from each stop line 2 signs should be clearly visible:

1. the intersection type (traffic light or stop sign)
2. the intersection topology (3-way with correct orientation, or 4-way).


````{list-table} Placement of Traffic Signs
:name: tab:sign-placement

* - ```{figure} ../../_images/appearance_specifications/tiles/4-way-signs.svg
    :name: subfig:4-way-signs

    4-way intersection
    ```

  - ```{figure} ../../_images/appearance_specifications/tiles/3-way-signs.svg
    :name: subfig:3-way-signs

    3-way intersection
    ```

* - ```{figure} ../../_images/appearance_specifications/tiles/2-way-signs-straight.svg
    :name: subfig:2-way-signs-straight

    straight road
    ```

  - ```{figure} ../../_images/appearance_specifications/tiles/2-way-signs-turn.svg
    :name: subfig:2-way-signs-turn

    curved road
    ```

````

On straight and curved roads, additional signs can be added as desired. 
Their placement is indicated in {numref}`subfig:2-way-signs-straight` and {numref}`subfig:2-way-signs-turn`. 
The signs should be placed at the border between two tiles and should face towards oncoming traffic as indicated.

In these figures the arrow is the direction of the sign.
