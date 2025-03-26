```{seo}
:description: Learn about the infrastructure layer in Duckietown, featuring traffic lights, traffic signs, and watchtowers for advanced robotics operations and communication.
:keywords: Duckietown, infrastructure layer, traffic lights, watchtowers, robotics, Duckiebots, Autolab, autonomous systems, advanced robotics, localization
```

(dt-ops-infrastructure-layer)=
# Layer - Infrastructure

The infrastructure layer is composed of:
- [Traffic Lights](specs-layer-traffic-lights)
- [Traffic signs](specs-layer-traffic-signs)
- (optional) Watchtowers
<!-- 
([legacy instructions](https://docs-old.duckietown.org/daffy/opmanual_autolab/out/watchtower_hardware.html), [work in progress new instructions](https://docs.duckietown.com/ente/opmanual-autolab/intro.html))
-->
Infrastructure elements are positioned on the tilemap (floor) layer, outside the lanes, and interact directly with Duckiebots within Duckietown.

## Key Components and Behaviors

1. **Traffic Lights**: these function as robots; with computation, sensing, memory, and actuation capabilities. Their primary behavior is to signal (stop and go) at intersections, ensuring smooth navigation and traffic management for Duckiebots. Being equipped with cameras and Wi-Fi capabilities, they can be reprogrammed for vehicle to infrastructure (v2i) applications. 

2. **Traffic Signs**: these are primarily used to characterize intersection, informing Duckiebots about the type (3- or 4-way) of intersection and the direction the Duckiebot is coming from. Other uses can be defined arbitrarily, e.g., as road names or pedestrian crossings.

3. **Watchtowers**: These robotic systems localize Duckiebots and communicate their positions to other agents. Watchtowers form the backbone of a Duckietown Autolab, providing advanced coordination and monitoring. As of April 2025, Autolabs are not actively maintained. To build an Autolab, reach out to Duckietown staff at info@duckietown.com.  

<!--
   - **Legacy Manual**: [Watchtower Hardware - Legacy Instructions](https://docs-old.duckietown.org/daffy/opmanual_autolab/out/watchtower_hardware.html)
   - **Work in Progress**: [Updated Watchtower Manual](https://docs.duckietown.com/ente/opmanual-autolab/intro.html)

-->

A network of watchtowers is an essential step in upgrading Duckietown to an Autolab environment. Traffic lights can be integrated into this network to extend their functionality.

```{tip}
If this is your first time exploring the infrastructure layer, you may ignore Watchtowers. However, if you plan to upgrade your Duckietown to an Autolab, remember that traffic lights can be incorporated into the Watchtower network.
```


