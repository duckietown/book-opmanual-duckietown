(traffic-light-assembly-18)=
# Assembly - Traffic Light `DT18-TL`

```{needget}
*   `DT18-TL` Traffic light components (can be sourced from the [Duckietown project shop](https://get.duckietown.com/collections/the-duckietown-city/products/smart-traffic-light?variant=32311801413771))

*   An appropriately [configured SD-card](https://docs.duckietown.org/daffy/opmanual_duckiebot/out/setup_duckiebot.html).

*   Tools: wood glue or hot glue gun.
---
*   Traffic light in configuration `DT18-TL`.
```

Traffic lights can be used to coordinate traffic at three or four way intersections in Duckietown. Hardware wise, traffic lights are essentially "Duckiebots without wheels", and a beautiful different chassis.

```{attention}
For traffic lights to be recognized by Duckiebots, appropriate signage must be placed at intersections (traffic light traffic sign instead of stop sign).
```

This section describes the physical assembly and installation of traffic lights.  

## Overview

<!--

Traffic lights are crucial parts in modern cities. We rely on them to have well-organized traffic. While autonomous cars could communicate with each other through so many different kinds of protocols, humans can't. Unless you are a terminator, or a RoboCop, or Neo. In the near future where autonomous cars drive with human drivers, we still need the help of traffic lights.

-->

Traffic lights are composed of two supports connected by an overhanging tube. They are intended to be placed on the diagonal direction of an intersection. One of the supports is equipped with the computational stack and an overseeing camera.

Traffic lights can double-up as [watchtowers](+opmanual_autolab#watchtower-hardware-assembly-WT18) when upgrading a Duckietown to [Duckietown Autolab](+opmanual_autolab#book). 

## Assembly of the traffic light parts

This section shows how to assemble the components from the laser cut traffic light parts.

```{warning}
The small parts with the hole in the middle, i.e., the ones in the left of {numref}`fig:G-1`, are not all equal. Some have a round hole, others a polygonal hole. Double check you are using the right ones in the process (compare with the pics).
```

All parts should be glued together as showed in the pictures for enhanced structural stability.

### Tube holder with big ground plate  

```{figure} ../_images/assembly/traffic_light_18/G-1.jpg
:width: 80%
:name: fig:G-1

Traffic light parts
```

```{figure} ../_images/assembly/traffic_light_18/G-2.jpg
:width: 50%
:name: fig:G-2
```

```{figure} ../_images/assembly/traffic_light_18/G-3.jpg
:width: 50%
:name: fig:G-3
```

```{figure} ../_images/assembly/traffic_light_18/G-4.jpg
:width: 50%
:name: fig:G-4
```

```{figure} ../_images/assembly/traffic_light_18/G-5.jpg
:width: 50%
:name: fig:G-5
```

```{figure} ../_images/assembly/traffic_light_18/G-6.jpg
:width: 50%
:name: fig:G-6
```

```{figure} ../_images/assembly/traffic_light_18/G-7.jpg
:width: 50%
:name: fig:G-7
```

```{figure} ../_images/assembly/traffic_light_18/G-8.jpg

:width: 80%
:name: fig:G-8
```

### Tube holder with small ground plate
```{figure} ../_images/assembly/traffic_light_18/G2-1.jpg
:width: 80%
:name: fig:G2-1
```

```{figure} ../_images/assembly/traffic_light_18/G2-2.jpg
:width: 50%
:name: fig:G2-2
```

```{figure} ../_images/assembly/traffic_light_18/G2-3.jpg
:width: 50%
:name: fig:G2-3
```

```{figure} ../_images/assembly/traffic_light_18/G2-4.jpg
:width: 50%
:name: fig:G2-4
```

```{figure} ../_images/assembly/traffic_light_18/G2-5.jpg
:width: 50%
:name: fig:G2-5
```

```{figure} ../_images/assembly/traffic_light_18/G2-6.jpg
:width: 50%
:name: fig:G2-6
```

```{figure} ../_images/assembly/traffic_light_18/G2-7.jpg
:width: 50%
:name: fig:G2-7
```


### Traffic light LED housing
```{figure} ../_images/assembly/traffic_light_18/L-1.jpg
:width: 80%
:name: fig:L-1
```

```{figure} ../_images/assembly/traffic_light_18/L-2.jpg
:width: 80%
:name: fig:L-2
```

```{figure} ../_images/assembly/traffic_light_18/L-3.jpg
:width: 80%
:name: fig:L-3
```

```{figure} ../_images/assembly/traffic_light_18/L-4.jpg
:width: 80%
:name: fig:L-4
```

```{figure} ../_images/assembly/traffic_light_18/L-5.jpg
:width: 80%
:name: fig:L-5
```

```{figure} ../_images/assembly/traffic_light_18/L-6.jpg
:width: 80%
:name: fig:L-6
```

### Ground module cover
```{figure} ../_images/assembly/traffic_light_18/C-01.jpg
:width: 50%
:name: fig:C-01
```

```{figure} ../_images/assembly/traffic_light_18/C-02.jpg
:width: 50%
:name: fig:C-02
```

### Joint module
```{figure} ../_images/assembly/traffic_light_18/J-1.jpg
:width: 80%
:name: fig:J-1
```

```{figure} ../_images/assembly/traffic_light_18/J-2.jpg
:width: 80%
:name: fig:J-2
```

```{figure} ../_images/assembly/traffic_light_18/J-3.jpg
:width: 80%
:name: fig:J-3
```

```{figure} ../_images/assembly/traffic_light_18/J-4.jpg
:width: 80%
:name: fig:J-4
```

```{figure} ../_images/assembly/traffic_light_18/J-5.jpg
:width: 80%
:name: fig:J-5
```

```{figure} ../_images/assembly/traffic_light_18/J-6.jpg
:width: 80%
:name: fig:J-6
```

```{figure} ../_images/assembly/traffic_light_18/J-7.jpg
:width: 80%
:name: fig:J-7
```

```{figure} ../_images/assembly/traffic_light_18/J-8.jpg
:width: 80%
:name: fig:J-8
```

(tl-mat)=
## Components of the traffic light

Now that you have assembled the traffic light chassis, you are ready to add the electronics.

```{figure} ../_images/assembly/traffic_light_18/TL-01.jpg
:width: 80%
:name: fig:tl_components

Parts of a traffic light needed to complete these instructions.
```

These components are needed for one traffic light:

* Tube holder with big ground plate
* Tube holder with small ground plate (Duckietown)
* Cable with soldered LED strip
* Joint module (2x)
* Traffic light LED housing
* Raspberry Pi base plate
* Ground module cover (Duckietown)
* Camera mount
* Camera mount cover
* Short tube
* Medium tube (2x)
* Long tube with hole at the side
* Raspberry Pi
* Raspberry Pi shield
* M2.5x10 MF Nylon spacers (8x)
* M2.5x8 Nylon screws (4x)
* SD card with Duckietown software
* USB cable
* Ethernet cable

Additionally, the traffic light structure can host:

* Traffic sign stands (4x)
* Traffic sign stand supports (4x).


## Assembling the Traffic Light



### Put the LEDs into the housing

Bend the LED strip at an angle to reduce the chance that the exposed soldered wires short. The exposed part of the wires should **not** be in contact, **especially** when turning on the power.

```{warning}
the actual traffic light in your hands might vary slightly from the pictures above. In particular, the electrical cables could have different colors or be soldered in different positions. Take note of what each color cable is soldered to, as same will go go with same on the other end.
```

```{figure} ../_images/assembly/traffic_light_18/L-0.png
:width: 80%
:name: fig:L-0

Bent LED strip cable
```

```{figure} ../_images/assembly/traffic_light_18/TL-02.jpg
:width: 80%
:name: fig:TL-02

Cable with soldered LED strip LED housing

```

```{figure} ../_images/assembly/traffic_light_18/TL-03.jpg
:width: 80%
:name: fig:TL-03
```

Carefully push the LEDs into the designated holes.

```{figure} ../_images/assembly/traffic_light_18/TL-05.jpg
:width: 80%
:name: fig:TL-05
```

```{figure} ../_images/assembly/traffic_light_18/TL-04.jpg
:width: 80%
:name: fig:TL-04
```

Fix the LEDs with some tape, don't use glue.

```{figure} ../_images/assembly/traffic_light_18/TL-06.jpg
:width: 80%
:name: fig:TL-06
```

### Connect the tubes

```{figure} ../_images/assembly/traffic_light_18/TL-07.jpg
:width: 80%
:name: fig:TL-07

Medium tubes and LED housing.
```

Stick the tubes into the sides of the LED housing and pull the cable through one side.

```{figure} ../_images/assembly/traffic_light_18/TL-08.jpg
:width: 80%
:name: fig:TL-08
``` 

Add the joint modules on the side of the tube without the cable.  

```{figure} ../_images/assembly/traffic_light_18/TL-09.jpg
:width: 80%
:name: fig:TL-09
```

```{figure} ../_images/assembly/traffic_light_18/TL-10.jpg
:width: 80%
:name: fig:TL-10
```

Mount the other joint module on the long tube, such that it aligns with the hole.

You can add additional tape under the joint modules to prevent them to slip down.

```{figure} ../_images/assembly/traffic_light_18/H-1.png
:width: 80%
:name: fig:H-1

Fully assembled traffic light.
```

```{figure} ../_images/assembly/traffic_light_18/TL-11.jpg
:width: 80%
:name: fig:TL-11
```

```{figure} ../_images/assembly/traffic_light_18/TL-12.jpg
:width: 80%
:name: fig:TL-12
```

```{figure} ../_images/assembly/traffic_light_18/TL-13.jpg
:width: 80%
:name: fig:TL-13
```

Pull the cable through longer tube and stick the tube into the joint module.

```{figure} ../_images/assembly/traffic_light_18/TL-14.jpg
:width: 80%
:name: fig:TL-14
```

```{figure} ../_images/assembly/traffic_light_18/TL-15.jpg
:width: 80%
:name: fig:TL-15
```

Put the tubes into the tube holders.  

```{figure} ../_images/assembly/traffic_light_18/TL-16.jpg
:width: 80%
:name: fig:TL-16
```

```{figure} ../_images/assembly/traffic_light_18/TL-17.jpg
:width: 80%
:name: fig:TL-17
```


### Connect the Raspberry Pi


Use the spacers and the screws to mount the Raspberry Pi on the Raspberry Pi ground plate as shown in {numref}`fig:TL-18`.

```{figure} ../_images/assembly/traffic_light_18/TL-18.jpg
:width: 80%
:name: fig:TL-18

Raspberry Pi mounted on ground plate
```

Plug the shield on top of the Raspberry Pi.  
Insert the SD card.  
Connect the LED cable to the shield.  

```{figure} ../_images/assembly/traffic_light_18/STEP_18_cropped.png
:width: 80%
:name: fig:TL-19
```

Connect the Ethernet cable.  
Connect the USB cable.



If done correctly the LEDs should be on.  

```{figure} ../_images/assembly/traffic_light_18/TL-20.jpg
:width: 80%
:name: fig:TL-20
``` 

Close the ground module with the case.    


```{figure} ../_images/assembly/traffic_light_18/TL-21.jpg
:width: 80%
:name: fig:TL-21
```

```{figure} ../_images/assembly/traffic_light_18/TL-22.jpg
:width: 80%
:name: fig:TL-22
```

### Add traffic sign stands

```{figure} ../_images/assembly/traffic_light_18/TL-23.jpg
:width: 80%
:name: fig:TL-23
```

```{figure} ../_images/assembly/traffic_light_18/TL-24.jpg
:width: 80%
:name: fig:TL-24
```

### Fully assembled traffic light

```{figure} ../_images/assembly/traffic_light_18/TL-25.jpg
:width: 80%
:name: fig:TL-25

Fully assembled traffic light.
```

Place the traffic light at an intersection such that the LEDs are exactly in the middle and are facing each incoming lane perpendicularly.

You can verify the position is correct by verifying that Duckiebots at the red stop lines can see only one light blinking, and no reflections of LEDs facing other directions.

You can finally use the provided double-sided tape pads to fix the traffic light to the tiles.

(dt-ops-tl-prep)=
### SD-card image Preparation

At hardware and software level, traffic lights are Duckiebots without wheels. In initializing the SD-card of your
traffic light, follow the instructions [here](+opmanual_duckiebot#setup-duckiebot), with the extra step of using the
option `--type traffic_light`. Also, WiFi configuration for traffic lights by default is not set. You can add it
using the `--wifi` option as specified int the [instructions](+opmanual_duckiebot#setup-duckiebot).

An example flashing command for a Wi-Fi connected traffic light can be:

```shell
dts init_sd_card --hostname watchtower![XX] --country ![COUNTRY] --type traffic_light --configuration TL19 --wifi duckietown:quackquack
```

- For Autolab users: since traffic lights are coupled to watchtowers, please use the watchtower setup:
        hostname : watchtowerXX

- However, if you just want to use it as a traffic light, use the trafficlight setup:
        hostname : trafficlightXX

- The default username and password are all the same:

    Username: duckie
    Password: quackquack

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

If you need to manually restart the behaviour inside the `duckiebot-interface` container, you can restart the traffic light behaviour by running:

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