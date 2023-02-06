(dt-ops-layers)= 
# Signal layers 

% {#dt-ops-layers status=ready}

<!--
* [](#dt-ops-troubleshooting): What could go wrong, and how to fix it.
-->

% <div class='requirements' markdown="1">

* Requires: Nothing.
* Results: Preliminary knowledge of Duckietown information layers.
* Next Steps: [The Duckietown appearance specifications](dt-ops-appearance-specifications).

% </div>

Functionally, Duckietown cities are an integral part of the robotic ecosystem we call Duckietown.  

Duckietown cities are designed to communicate information to the Duckiebots, so these can operate effectively.

Duckietown cities are *modular*, i.e., they are composed of fundamental building blocks that can be combined to create nearly arbitrary city landscapes. 

% Moreover, many hardware components are the same as those used for the Duckiebots.

Duckietown cities are built in layers. Each layer sends information of increasing complexity to the robots operating in it. The layers are, namely, the: *floor*, *signals*, and *smart infrastructure* layers. "Non-functional" elements compliment the construction of every Duckietown. 


## Signals Layer {#dt-ops-signals-layer status=ready}

The signals layer contains all the [signs](dt-ops-city-traffic-signs) and other functional objects that sit on top of the mats (e.g., traffic lights, watchtowers, etc.). Objects are functional when they enable some behavior for the Duckiebots. For example, traffic signs are functional because they inform Duckiebots at intersections where they are and what should they look out for to know when to drive on.

## Non-functional elements {#dt-ops-non-functional-layer status=ready}

The citizens of Duckietown like their cities to be colorful and fun, and encourage all efforts at adding non-functional components to the city. Non functional objects, e.g., decorative building, can still sit on the floor but make sure they don't interfere with the signals or floor layers!

Moreover, although Duckiebot drivers all have their driving licenses and know to focus on the road, the _background_, i.e., whatever is in the room the Duckietown was assembled, matters too. 



<!--

More information in this regards can be found in the [troubleshooting](#part:dt-ops-troubleshooting) section.

Note: the visual appearance of the area where the Duckietown is created is variable. If you discover that this appearance is causing negative performance, a "wall" of blank tiles constructed vertically can be used to reduce visual clutter.

-->
