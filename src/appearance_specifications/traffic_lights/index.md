(specs-layer-traffic-lights)=
# Layer - Traffic Lights

Duckietown traffic lights are more than just blinking lights: they are static robots. We sometimes refer to traffic lights as "Duckiebots without wheels" because they originally had similar capabilities to the `DB18` Duckiebot models, less that to move.

Traffic lights are urban robots that can sense (e.g., the arrival of a Duckiebot) through a camera, run computation on the onboard Raspberry Pi, and communicate with other agents though the LEDs, and WiFi network.  

```{tip}
(For advanced Duckietowners only) Traffic lights are particular cases of Duckietown Watchtowers, i.e., Watchtowers with LEDs. Watchtowers are the building blocks of Duckietown Autolabs.
```

(specs-layer-traffic-lights-assembly)=
## Assembly
The assembly instructions for traffic lights can be found here:
 
 * [Traffic light assembly instructions](traffic-light-assembly-21),
 * [Legacy traffic light assembly instructions](traffic-light-assembly-18),


## Placement

Traffic lights are typically placed over the diagonal direction of intersection tiles. Any intersection is allowed to have a traffic light.

```{note}
The lights must be at a height of 20 cm above the center of the intersection tile.
```

The computational stack of the traffic light is mounted in the appropriate housing, and placed outside 
the allowable driving region. The cabling is designed to be housed in the appropriate structure as detailed in the [assembly instructions](specs-layer-traffic-lights-assembly). The traffic light pillar stands are positioned so that the embedded traffic signs match their [appearance specifications](traffic-signs-placement). 

```{figure} ../../_images/appearance_specifications/traffic-lights/TrafficLight-DT18-TL.png
    :name: subfig:traffic-light-dt18
    :width: 90%

    traffic light
    ```