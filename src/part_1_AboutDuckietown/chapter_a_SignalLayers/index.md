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


<!--

More information in this regards can be found in the [troubleshooting](#part:dt-ops-troubleshooting) section.

Note: the visual appearance of the area where the Duckietown is created is variable. If you discover that this appearance is causing negative performance, a "wall" of blank tiles constructed vertically can be used to reduce visual clutter.

-->
