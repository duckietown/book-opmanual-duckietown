# Appearance Specifications {#dt-ops-appearance-specifications status=ready}

<div class='requirements' markdown="1">

Requires: Nothing.

Results: Knowledge of the Duckietown appearance specifications

Next Steps: [Duckietowns and Duckiebots](#dt-ops-city-definitions), or [Duckietown assembly](#dt-ops-assembly).

</div>

This document describes the Duckietown appearance specification. Specifications are a set of rules for which a functional system has been verified. This means that if these rules are followed while building a Duckietown, Duckiebots will (most probably!) work.

Any Duckietown not adhering to the rules described here cannot be considered a Duckietown, and may cause the Duckiebots operating within them to fail in unexpected ways.

Small perturbations to the appearance specifications might affect negatively the performance of Duckiebots, although most algorithms are robust to variations.

<!--

Version history

Note here the changes to the specification, so that we are able to keep the different Duckietowns synchronized.

* Version 1.0 - used for MIT 2.166

* Version 2.0 - user for Fall 2017 and throughout 2018.

Overview

Duckietown is built with two layers:
1. The first is the *floor layer*. The floor is built of interconnected exercise mats with tape on them.
2. The second layer is the *signals layer* and contains all the signs and other objects that sit on top of the mats.

Note that the visual appearance of the area where the Duckietown is created is variable. If you discover that this appearance is causing negative performance, a "wall" of blank tiles constructed vertically can be used to reduce visual clutter.

-->

## Layer 1 - The Floor Layer {#dt-ops-floor-app-specs status=ready}

The floor layer is made of interlocking black tiles. Each tile represents one road element: straight, curve, 3-way intersection, 4-way intersection and empty tile. The road elements are positioned in specific orders to create compliant Duckietowns. The road elements are shown in [](#fig:tiles), note that the left turn and right turn tiles are symmetric: one is the 90 degree rotation of the other.


Each tile is square and measures 61 x 61 cm (2 ft x 2 ft) from the outer edges of the interlocking dents. The thickness of the tiles is not as important as the surface roughness. The objective is having good grip between the Duckiebots and the road in order to minimize slipping of the wheels.

<div figure-id="fig:tiles" figure-class="flow-subfigures" figure-caption="The principal tile types in Duckietown">
    <div figure-id="subfig:straight" figure-caption="DT17_tile_straight">
        <img src="DT17_tile_straight-texture.png" style='width: 20ex'/>
    </div>
    <div figure-id="subfig:DT17_tile_curve_left" figure-caption="DT17_tile_curve_left">
        <img src="DT17_tile_curve_left-texture.png" style='width: 20ex'/>
    </div>
    <div figure-id="subfig:DT17_tile_curve_right" figure-caption="DT17_tile_curve_right">
        <img src="DT17_tile_curve_right-texture.png" style='width: 20ex'/>
    </div>
    <div figure-id="subfig:DT17_tile_three_way_center" figure-caption="DT17_tile_three_way_center">
        <img src="DT17_tile_three_way_center-texture.png" style='width: 20ex'/>
    </div>
    <div figure-id="subfig:DT17_tile_four_way_center" figure-caption="DT17_tile_four_way_center">
        <img src="DT17_tile_four_way_center-texture.png" style='width: 20ex'/>
    </div>
    <div figure-id="subfig:DT17_tile_empty" figure-caption="DT17_tile_empty">
        <img src="DT17_tile_empty-texture.png" style='width: 20ex'/>
    </div>
</div>


<div figure-id="fig:DT17_map_loop3" figure-caption="A 3 by 3 city loop (DT17_map_loop3)">
    <img src="DT17_map_loop3-texture.png" style='width: 8cm'/>
</div>


<div figure-id="fig:DT17_usage_four_way" figure-caption="Four way intersection usage">
    <img src="DT17_usage_four_way-texture.png" style='width: 8cm'/>
</div>
<div figure-id="fig:DT17_usage_three_way" figure-caption="Three way intersection usage">
    <img src="DT17_usage_three_way-texture.png" style='width: 8cm'/>
</div>


The empty tiles can be of any color, although it is discouraged to use the same colors as the road markings (red, white and yellow).

For tiles to become road elements, we need to apply road markings. Road markings can be obtained through the application of tapes of different colors and sizes.

### Tapes {#dt-ops-app-spec-tapes status=ready}

There are 3 colors of tapes used in Duckietown: white, yellow, and red.

#### White tape

\begin{proposition}\label{prop:white_tape}
A Duckiebot on a road never collides with Duckiebots or other Duckietown elements if it never crosses or touches a white tape strip.
\end{proposition}

Here are some facts about the white tapes:

* White tapes must be solid (not dashed);

* The width of the white tape is roughly **4.8 cm** (1.88 inches);

* The white tape is always placed on the right hand side of a lane. We assume that the Duckiebots drive on the right hand side of the road.

Comment: this should be part of the "traffic rules" sections.

* For curved roads, the white lane marker is formed by five pieces of white tape, while the inner corner is formed by three pieces, placed according to the specifications in the image below, where the edge pieces are matched to adjacent straight or curved tiles ([](#fig:curved)).

<div figure-id="fig:curved" figure-caption="The specification for a curved road tile">
  <img src="opmanual_duckietown/images/tiles/curved_appearance_spec.png" style='width: 30em; height:auto'/>
</div>

#### Yellow tape

Here are some facts about the yellow tapes:

* Yellow tape must be dashed (not solid);

* Each piece should be **5 cm** long and placed with a **2.5 cm** gap between each piece;  

* The width of the yellow tape is roughly 2.4cm (0.94 inches);

* The yellow tape is always placed on the left hand side of a lane, i.e., in the center of the road. We assume that the Duckiebots drive on the right hand side of the road.

Yellow tapes on curves: see curved road image ([](#fig:curved)) in white tape section. Pieces at tile edges should be in center of lane, piece at the middle of the curve should be approximately 21 cm from middle of inner center white piece of tape, with approximated circular arc in between.

#### Red tape

Red tapes MAY **only** appear on **intersection** tiles.

The width of the red tape must be the same as the white roll (roughly 4.8cm or 1.88 inches) and should cross the entire lane perpendicular to the road.

The placement of red tape should always be **under** yellow and white tape, as shown, e.g., in [](#fig:DT17_usage_four_way) or [](#fig:DT17_usage_three_way).

A Duckiebot navigates Duckietown by a sequence of:

* Navigating one or more straight tiles until a red tape appears,
* Waiting for the coordination signal,
* Executing an intersection traversal,
* Re-localizing in a straight tile.

\begin{proposition}
If the Duckiebot stops before or ON the red strip, no collisions are possible.
\end{proposition}

### Topological Constraints During Map Construction

Here are some topological rule constraints that must be met:

1. An intersection can NOT be adjacent to a curved road tile or another intersection tile.

2. Any two adjacent non-empty tiles must have a feasible path from one to the other **of length two**: if they are adjacent, they must be connected.

Some examples of **non-conforming** topologies are shown in [](#fig:violates).

<div figure-id="fig:violates" figure-class="flow-subfigures" figure-caption="Some non-conforming Duckietown map topologies">
    <div figure-id="subfig:violates1" figure-caption="Topology violates rule 2 since the bottom two curved tiles are adjacent but not connected">
        <img src="violates1.pdf" style='width: 20ex;height:auto'/>
    </div>
    <div figure-id="subfig:violates2" figure-caption="Topology violates rule 1 since curved tiles are adjacent to intersection tiles ">
        <img src="violates2.pdf" style='width: 20ex;height:auto'/>
    </div>
    <div figure-id="subfig:violates3" figure-caption="Topology violates rule 2 since left-most tiles are adjacent but not connected">
        <img src="violates3.pdf" style='width: 20ex;height:auto'/>
    </div>
</div>


### Parking Lots {#parking status=draft}

Note: The tile types described here are experimental. Use at your own risk!

A parking lot is a place for Duckiebots to go when they are tired and need a rest.

A parking lot introduces three additional tile types:

1. **Parking lot entry tile**: This is similar to a straight  tile except with a red stop in the middle. The parking lot sign ([](#fig:parking)) will be visible from this stop line.
2. **Parking spot tiles**:
3. **Parking spot access tiles**:

<!--
TODO: the tape on the spot and spot access tiles is currently not yet specified.
-->
The following are the rules for a conforming parking lot:

1. One "parking spot" has size one tile.
2. From each parking spot, there is a path to go to the parking lot entry tile that does not intersect any other parking spot. (i.e. when a Duckiebot is parked, nobody will disturb it).
3. From any position in any parking spot, a Duckiebot can see at least two orthogonal lines or a sign with an April tag.
<!--
TODO: this point needs further specification
-->

### Launch Tiles {#launch-tiles status=draft}

Note: The tile type described here is experimental. Use at your own risk!

A "launch tile" is used to introduce a new Duckiebot into a Duckietown in a controllable way. The launch file should be placed adjacent to a turn tile so that a Duckiebot may "merge" into Duckietown once the initialization procedure is complete.
<!--
TODO: Specification for tape on the launch tile
-->
A "yield" sign should be visible from the launch tile.

## Layer 2 - Signage and Lights

<!--

**IMPORTANT:** All signage should sit with base on the floor and stem coming through the connection between the tiles.

-->

Generally, it is advisable to adhere signal layer elements to the tiles with double-sided tape. **Under no circumstances should any tape be obscured by the base of the stands**. At least a 0.5 cm free (black) space should separate any line from a signal layer elements' base.     

## Traffic Signs {#traffic-signs status=ready}

Traffic signage in Duckietown is obtained through the union of a traffic signs and an April Tag, as shown in [](#fig:traffic-sign-example)

<div figure-id="fig:traffic-sign-example" figure-caption="A traffic sign in Duckietown (do not print this one out!)">
  <img src="traffic-sign-example.png" style='width: 20em; height:auto'/>
</div>

We call the symbol above _traffic sign_, while the code below is an AprilTag.

Requires: To print and assemble the signs refer to [](#dt-ops-city-traffic-signs).

### Specifications

For traffic signage to be compliant:

* The center of the traffic signs is 13 cm height from the floor layer;
* The AprilTag is 6.5 cm sq.;
* There is a white border of roughly 0.8 cm around them;
* The signage stands perpendicular to the ground, and the angle of the sign with the road is $90^ \circ$.
* The signal is flat (no deformation / folding) and without wrinkles. This can be obtained, e.g., by printing the signs on thick paper.

### Types

The allowable traffic signs are as in [](#fig:traffic-signs).

<div figure-id="fig:traffic-signs" figure-class="flow-subfigures" figure-caption="Duckietown Traffic Signs">
  <div figure-id="subfig:stop" figure-caption="stop">
    <img src="stop.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:yield" figure-caption="yield">
    <img src="yield.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:no-right" figure-caption="no-right-turn">
    <img src="no-right.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:no-left" figure-caption="no-left-turn">
    <img src="no-left.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:no-enter" figure-caption="do-not-enter">
    <img src="no-enter.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:one-way-right" figure-caption="oneway-right">
    <img src="one-way-right.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:one-way-left" figure-caption="oneway-left">
    <img src="one-way-left.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:4-way-intersect" figure-caption="4-way-intersect">
    <img src="4-way.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:3-way-right" figure-caption="right-T-intersect">
    <img src="3-way-right.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:3-way-left" figure-caption="left-T-intersect">
    <img src="3-way-left.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:t-intersection" figure-caption="T-intersection">
    <img src="t-intersection.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:crossing" figure-caption="pedestrian">
    <img src="crossing.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:traffic-light" figure-caption="t-light-ahead">
    <img src="traffic-light.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:duckie-crossing" figure-caption="duck-crossing">
    <img src="duckie-crossing.png" style='width:8em;height:auto'/>
  </div>
  <div figure-id="subfig:parking" figure-caption="parking">
    <img src="parking.png" style='width:8em;height:auto'/>
  </div>
</div>

### Placement {#traffic-signs-placement status=ready}

Signs may appear on the opposite side and at the corner of the adjacent tile from which they are viewed. In the absence of any signs, it is assumed that all network flows are allowed so a sign MUST be placed and visible whenever this is not the case.

Signs must only be placed on empty tiles, or next to one of the other tile types if on the border of a map. As mentioned, it is important to not overlap the base of the sign stand with any road marking.

The sign placements for four different cases are shown in [](#sign-placement). At intersections, from each stop line 2 signs should be clearly visible: 1) the intersection type (traffic light or stop sign) and 2) the intersection topology (3-way with correct orientation, or 4-way).

<!--

At present, 4-way intersections must be equipped with traffic lights for safe navigation.

-->

<div figure-id="fig:sign-placement" figure-class="flow-subfigures" figure-caption="Placement of Traffic Signs">
  <div figure-id="subfig:4-way-signs" figure-caption="4-way intersection">
    <img src="4-way-signs.pdf" style='width:15em;height:auto'/>
  </div>
  <div figure-id="subfig:3-way-signs" figure-caption="3-way intersection">
    <img src="3-way-signs.pdf" style='width:15em;height:auto'/>
  </div>
  <div figure-id="subfig:2-way-signs-straight" figure-caption="straight road">
    <img src="2-way-signs-straight.pdf" style='width:15em;height:auto'/>
  </div>
  <div figure-id="subfig:2-way-signs-turn" figure-caption="curved road">
    <img src="2-way-signs-turn.pdf" style='width:15em;height:auto'/>
  </div>
</div>

On straight and curved roads, additional signs can be added as desired. Their placement is indicated in [](#subfig:2-way-signs-straight) and [](#subfig:2-way-signs-turn). The signs should be placed at the border between two tiles and should face towards oncoming traffic as indicated.

In these figures the arrow is the direction of the sign.


## Street Name Signs {#street-name-signs status=beta}

### Specifications


* Font: arial.

* Color: white as foreground and green as background.

* Border: no additional borders

* The rounded corners are modified into 90 degrees.

* Height: center of the sign height is 1.5 in. (**2.1 in**),

* Width: Currently 4.5 in for id 500-511. (**6.1 in +1.1 in "ST" or 5.5 in + 1.7 in “AVE”**)

* Alphabet =  English upper case. Different writing systems may need different algorithms.

* Text direction: Horizontal for alphabetical languages.

<!--
TODO: clarify street name conventions
-->

### Placement

* **Similar to traffic lights**: The street name should sit on a pole that is based at the corner of the tile outside of the allowable driving region. The bottom of the street name should be at a height of 7in, and allow a Duckiebot to pass through. The street names should be visible from both sides of the road.

Every segment of road must have at least one road name sign.

Every turn tile should have a road name sign.

The placement of the road name signs is as indicated in [](#fig:name-placement).

<div figure-id="fig:name-placement" figure-class="flow-subfigures" figure-caption="Placement of Road Name Signs">
  <div figure-id="subfig:name-signs-turn" figure-caption="Turn">
    <img src="name-signs-turn.pdf" style='width:15em;height:auto'/>
  </div>
  <div figure-id="subfig:name-signs-straight" figure-caption="Straight">
    <img src="name-signs-straight.pdf" style='width:15em;height:auto'/>
  </div>
</div>

Street name signs should never be perpendicular to the road - they are too big and obtrusive.

## Traffic Lights {#traffic-light-app-spec status=ready}

The assembly procedure for building traffic lights can be found in [](#traffic-light-assembly-18).

### Placement

The lights must be at a height of 20 cm above the center of the intersection tile.

<!--

The Raspberry Pi should sit on a pole that is based at the corner of the tile outside of the allowable driving region.

-->

The computational stack of the traffic light should be mounted in the appropriate housing outside the allowable driving region. The cabling should be housed in the appropriate structure as detailed in [](#traffic-light-assembly-18). The traffic light pillar stands should be positioned in such a way that the embedded traffic sign stands respect the above specifications for traffic light stands.
