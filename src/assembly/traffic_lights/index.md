(traffic-light-assembly)=
# Assembly - Traffic Light

```{needget}
*   Traffic light components (can be sourced from the [Duckietown project shop](https://get.duckietown.com/collections/the-duckietown-city/products/smart-traffic-light?variant=32311801413771))

*   An appropriately [configured SD-card](book-opmanual-duckiebot:setup-duckiebot-sd-card).

*   Tools: (strong) wood glue or hot glue gun, tape, double-sided tape.
---
*   An assembled traffic light in configuration `DT21-TL` (latest) or previous legacy versions.
```

Traffic lights can be used to coordinate traffic at three or four way intersections in Duckietown. 
Hardware wise, traffic lights are essentially "Duckiebots without wheels", and a beautiful different chassis.

```{attention}
For traffic lights to be recognized by Duckiebots, appropriate signage must be placed at intersections 
(traffic light traffic sign instead of stop sign).
```

This section describes the physical assembly and installation of traffic lights.  


## Overview

Traffic lights are crucial parts in modern cities. 
We rely on them to have well-organized traffic. 
In Duckietown, traffic lights serve the same purpose.

They are composed of two supports connected by an overhanging tube. 
They are intended to be placed on the diagonal direction of an intersection. 
One of the supports is equipped with the computational stack and an overseeing camera.

Traffic lights can double-up as 
[watchtowers](book-opmanual-autolab:watchtower-hardware-assembly-WT18) 
when upgrading a Duckietown to [Duckietown Autolab](book-opmanual-autolab:book). 

```{todo}
update intersphinx links above
```

## Hardware Assembly

* For traffic lights of the **latest** configuration, please refer to this for the assembly instructions.
  * [](traffic-light-assembly-21)
* For legacy and repair reasons, the assembly instructions before configuration `TL21` can be found in
  * [](traffic-light-assembly-18).

(dt-ops-tl-prep)=
### SD-card image Preparation

At hardware and software level, traffic lights are Duckiebots without wheels. In initializing the SD-card of your
traffic light, follow the instructions [here](book-opmanual-duckiebot:setup-duckiebot-sd-card), with the extra step of using the
option `--type traffic_light`. Also, WiFi configuration for traffic lights by default is not set. You can add it
using the `--wifi` option as specified int the [instructions](book-opmanual-duckiebot:setup-duckiebot-sd-card).


An example flashing command for a Wi-Fi connected traffic light can be:

```shell
dts init_sd_card --hostname watchtower![XX] --country ![COUNTRY] --type traffic_light --configuration TL21
```

- For Autolab users: since traffic lights are coupled to watchtowers, please use the watchtower setup:
    *   hostname : `watchtowerXX`

- However, if you just want to use it as a traffic light, use the trafficlight setup:
    *   hostname : `trafficlightXX`

- The default username and password are all the same:

    *   Username: `duckie`
    *   Password: `quackquack`

```{warning}
For autolab users, do not change the username and password.
```
<!--

`DB17` instructions

Prepare a Duckiebot image following the instructions on `DB17` Duckiebot initialization and remember to generate the new machine file.


See setup-duckiebot
and this chapter
See rc-control


`DB18` instructions {#dt-ops-tl-init status=draft}
 write detailed instruction, verify functionality with docker infrastructure

-->

(dt-ops-tl-launch)=
### Launch Traffic Lights
By choosing the `robot_type` to be `traffic_light`, the blinking behaviour should happen as soon as you boot your device.

If you need to manually restart the behaviour inside the `duckiebot-interface` container, you can restart the traffic light behaviour by running, inside the container:

```shell
roslaunch duckiebot_interface all_drivers.launch veh:=![NAME] robot_type:=traffic_light
```


<!--

Semantics of LEDS {#LED-semantics status=draft}

headlights: white, constant

Assumption:

- **20 fps** to do LED detection

- 1s to decide

- 3 frequencies to detect

tail lights: red, **6 hz square wave**

traffic light "GO" = green, **1 hz square wave**

traffic light "STOP" = red, **1.5 Hz** square wave**

duckie light on top, state 0 = off

duckie light on top, state 1 = blue, **3 Hz, square wave**

duckie light on top, state 2 = ?, **2.5 Hz square wave**

duckie light on top, state 3 = ?, **2 Hz square wave**

verify if this info is still up to date.

-->