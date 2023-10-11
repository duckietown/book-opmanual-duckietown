(dt-ops-infrastructure-layer)=
# Layer - Infrastructure

The infrastructure layer is made of:
* [traffic lights](specs-layer-traffic-lights), and 
* watchtowers ([legacy instructions](https://docs-old.duckietown.org/daffy/opmanual_autolab/out/watchtower_hardware.html), [work in progress new instructions](https://docs.duckietown.com/ente/opmanual-autolab/intro.html)).

Infrastructure elements sit on the tilemap (floor) layer, outside the lanes, and interact with the Duckiebots in town.

Traffic lights and watchtowers are proper robots: they have computation, sensing, memory and actuation capabilities. As such, they can be programmed to exhibit behaviors, including communication with other agents.

The most fundamental behavior of a traffic light is to signal (stop and go) to the Duckiebots at intersections.

The most fundamental behavior of watchtowers is to localize Duckiebots and communicate their position to other agents. 

A network of watchtowers is the first step to building a Duckietown Autolab ([legacy operation manual](), [work in progress manual](https://docs.duckietown.com/ente/opmanual-autolab/intro.html)). 

```{tip}
If this is your first read-through you may ignore Watchtowers. If you are planning on upgrading your Duckietown to an Autolab at any point in time, remember that traffic lights can be used as part of the Watchtowers network. 
```