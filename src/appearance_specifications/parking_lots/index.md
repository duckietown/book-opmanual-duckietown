(specs-layer-parking-lots)=
# Layer - Parking Lots {bdg-warning}`BETA`

```{note}
The tile types described here are experimental. Use at your own risk!
```

A parking lot is a place for Duckiebots to go when they are tired and need a rest.

A parking lot introduces three additional tile types:

1. **Parking lot entry tile**: This is similar to a straight tile except with a red stop in the middle. 
   The parking lot sign ({numref}`subfig:parking`) will be visible from this stop line.
2. **Parking spot tiles**:
3. **Parking spot access tiles**:

```{todo}
the tape on the spot and spot access tiles is currently not yet specified.
```

The following are the rules for a conforming parking lot:

1. One "parking spot" has size one tile.
2. From each parking spot, there is a path to go to the parking lot entry tile that does not intersect 
   any other parking spot. (i.e. when a Duckiebot is parked, nobody will disturb it).
3. From any position in any parking spot, a Duckiebot can see at least two orthogonal lines or a sign with an AprilTag.

```{todo}
this point needs further specification
```
