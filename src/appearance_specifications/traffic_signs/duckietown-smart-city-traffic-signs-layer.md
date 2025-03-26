```{seo}
:description: Discover the functional and non-functional uses of Duckietown traffic signs, including specifications, placement rules, and approved sign types.
:keywords: Duckietown, traffic signs, AprilTags, robotics, Duckiebots, intersection control, modular cities, signage compliance, robotics education, smart city
```

(specs-layer-traffic-signs)=
# Layer - Traffic Signs

The signals layer consists of [traffic signs](dt-ops-city-traffic-signs). These traffic signs are placed on the road layer, outside the lanes, serving both functional and non-functional purposes.

```{seealso}
The full set of currently existing signs is available 
[here](https://github.com/duckietown/signs-and-tags).
```

## Functional Purposes

Traffic signs can serve specific functions that are encoded in some Duckietown legacy behaviors. For instance:

```{note}
Traffic signs:
- Identify the type of intersection (3- or 4-way).
- Indicate the Duckiebot's position at the intersection.
- Communicate the coordination mechanism for the specific intersection (centralized or decentralized).
```

## Non-Functional Purposes

Traffic signs can also be used for purposes not encoded in Duckietown's out-of-the-box behavior. Examples include:

```{note}
Traffic signs can be used for:
- Naming roads (e.g., to honor the department head).
- Indicating pedestrian traffic areas.
- Marking parking lots.
```

---

Traffic signage in Duckietown combines traditional traffic signs and `AprilTag` visual markers, as shown in {numref}`fig:traffic-sign-example`.

```{figure} ../../_images/appearance_specifications/signs/traffic-sign-example.png
:name: fig:traffic-sign-example
:width: 50%

A traffic sign in Duckietown (do not print this one out!)
```

The symbol above is referred to as a _traffic sign_, while the code below represents an AprilTag.

```{note}
For instructions on printing and assembling traffic signs, refer to [](dt-ops-city-traffic-signs).
```

## Specifications

For traffic signage to be compliant:
- The center of traffic signs must be 13 cm above the floor layer.
- AprilTags must measure 6.5 cm squared.
- There should be a white border of approximately 0.8 cm around the AprilTags.
- Signs must stand perpendicular to the ground and form a $90^\circ$ angle with the road.
- Signs must be flat, with no deformation or wrinkles (use thick paper for best results).

## Types

The allowable traffic signs in Duckietown are listed in {numref}`tab:traffic-signs`.

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

(specs-layer-traffic-signs-placement)=
## Traffic Sign Placement

Traffic signs should be placed on empty tiles or at the border of a map. It is crucial to ensure the base of the sign stand does not overlap with any road markings.

At intersections, two signs should be clearly visible from each stop line:
1. The intersection type (e.g., traffic light or stop sign).
2. The intersection topology (e.g., 3-way with orientation, or 4-way).

Sign placements for different scenarios are illustrated in {numref}`tab:sign-placement`.

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

    Straight road
    ```

  - ```{figure} ../../_images/appearance_specifications/tiles/2-way-signs-turn.svg
    :name: subfig:2-way-signs-turn

    Curved road
    ```

````

On straight and curved roads, additional signs can be added as desired. Their placement is indicated in {numref}`subfig:2-way-signs-straight` and {numref}`subfig:2-way-signs-turn`. These signs should face oncoming traffic.
