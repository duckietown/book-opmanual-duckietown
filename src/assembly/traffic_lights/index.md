(traffic-light-assembly)=
# Assembly - Traffic Light

```{needget}
*   Traffic light components ([Duckietown project shop](https://get.duckietown.com/products/smart-traffic-light?variant=32311801413771))

*   An appropriately [configured SD-card](book-opmanual-duckiebot:setup-duckiebot-sd-card).

*   Tools: (strong) wood glue or hot glue gun, tape, double-sided tape.
---
*   An assembled traffic light in configuration `DT21-TL` (latest) or previous legacy versions.
```

This section describes the physical assembly and installation of traffic lights.  

## Overview

Traffic lights are crucial elements of modern cities as city dwellers rely on them to have well-organized traffic. In Duckietown, traffic lights serve the same purpose.

Traffic lights can be used as centralized coordinators of traffic at three or four way intersections in Duckietown, or as elements of a Duckietown Autolab watchtower network. 

```{attention}
For Duckiebots to know traffic lights are governing a certain intersection, appropriate signage must be placed at the intersection (traffic light traffic sign instead of stop sign).
```

* Hardware wise, traffic lights are essentially "Duckiebots without wheels", and a beautiful, different chassis.
* They are composed of two supports connected by an overhanging tube. 
* They are intended to be placed on the diagonal direction of an intersection. 
* One of the supports is equipped with the computational stack and an overseeing camera.

## Hardware Assembly

* For traffic lights of the **latest** configuration, please refer to this for the assembly instructions.
  * [](traffic-light-assembly-21)
* For legacy build, the assembly instructions for configurations prior to `TL21` can be found in
  * [](traffic-light-assembly-18).

(dt-ops-tl-prep)=
### SD-card Image Preparation

Even at software level, traffic lights are essentially Duckiebots without wheels. In initializing the SD-card of your traffic light, follow the instructions [here](book-opmanual-duckiebot:setup-duckiebot-sd-card), with the extra step of using the option `--type traffic_light`. 

Also, Wi-Fi configuration for traffic lights by default is not set. You can add it using the `--wifi` option as specified in the [instructions](book-opmanual-duckiebot:setup-duckiebot-sd-card).

An example flashing command for a Wi-Fi connected traffic light can be:

```shell
dts init_sd_card --hostname watchtower![XX] --country ![COUNTRY] --type traffic_light --configuration TL21
```

```{note}
For Autolab users: since traffic lights will work as watchtowers adopt the convention:

    hostname : `watchtowerXX`

where `XX` are, e.g., increasing numbers.
```

- However, if you just want to use it as a traffic light, use the traffic light setup:
    *   hostname : `trafficlightXX`

- The default username and password are all the same:

    *   Username: `duckie`
    *   Password: `quackquack`

```{warning}
For Autolab users, do not change the username and password.
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