(dt-ops-city-traffic-signs)=
# Traffic Signs Assembly

```{needget}
The materials to build Duckietown signals.
---
A set of signs to be used for assembling your Duckietown.
```


## Build a Map

Before beginning with sign assembly you should design a map that adheres 
to [the specification](dt-ops-appearance-specifications).

The full set of currently existing signs is available [here](https://github.com/duckietown/signs-and-tags).


(making-new-signage)=
## Making New Signage

If you find that what is available in the database in insufficient for your needs, 
then you will need to add to the existing database.

Clone the [signs-and-tags](https://github.com/duckietown/signs-and-tags) repo:

    git clone git@github.com:duckietown/signs-and-tags

The file `tag36h11.pdf` (`tag36h11.ps`) in the repo contains the tags already generated.
Which tag you should use depends on what type of sign you are trying to add. 
The ranges of tags are specified in [](tab:tag-ranges).

```{list-table} April tag ID ranges
:header-rows: 1
:name: tab:tag-ranges

* - Purpose
  - Size
  - Family
  - ID Range

* - Traffic signs
  - 6.5cm x 6.5cm
  - 36h11
  - 1-199

* - Traffic lights
  - 6.5cm x 6.5cm
  - 36h11
  - 200-299

* - Localization
  - 6.5cm x 6.5cm
  - 36h11
  - 300-399

* - Street Name Signs
  - 6.5cm x 6.5cm
  - 36h11
  - 400-587
```

First, find the last sign of the type that you are trying to make in the `Signs_and_tags_V3.docx`. 
You will use the next available ID after this one.

Construct the new sign by first copying and pasting an existing sign of similar type, 
and then replacing/adding the new AprilTag. To add the new april tag, use a screen capture mathod 
to crop precisely around the tag at the top and sides and include the sign id at the bottom. 
Then paste the tag into your word file under your desired and resize it exactly `6.5cm` (`2.56in`).

If you make a new road name sign, you may need to change the font size of the name so that it appears on one line.

```{attention}
You must also add your new sign to the `apriltagsDB.yaml`.
```

Add a new block like the ones that already exists or modify the one with the appropriate tag id:

```
- tag_id: ![NEW_TAG_ID]
  tag_type: in {TrafficSign, Light, Localization, StreetName}
  street_name: either ![NEW_STREET_NAME] or blank
  vehicle_name: currently not used
  traffic_sign_type: either ![TRAFFIC_SIGN_TYPE] or blank
```

The value of `![NEW_STREET_NAME]` is up to you to decide (have fun with it!). 
The value of `![TRAFFIC_SIGN_TYPE]` should be one of the signs in [](fig:traffic-signs)

When finished, regenerate the PDF version of the Word file, and commit everything 
to the repo (via a pull request of course).

```{note}
It is also possible of course to start you own completely different signs and tags database, 
but make sure that you specify in the `april_tags` code which database to load from.
```


## Traffic Signs Assembly


### Assemble the stands

A traffic sign stand consists of a laser cut structure as is show [](fig:traffic_stand_assembly_1).

```{figure} ../../_images/traffic_sign/trafficsign_kit.png
:width: 50%
:name: fig:traffic_stand_assembly_1

Traffic sign stand kit.
```

Detach the components from the wooden plate and plug them together as in [](fig:traffic_stand_assembly_2). 
Typically, the stands are very rigid, but if the structure seems a bit loose, use wooden glue to increase stability.

```{figure} ../../_images/traffic_sign/trafficsign_stand_assembly.png
:width: 35%
:name: fig:traffic_stand_assembly_2

Traffic sign stand assembled.
```

```{figure} ../../_images/traffic_sign/trafficsign_stand_assembled.png
:width: 35%
:name: fig:traffic_stand_assembly_3

Traffic sign stand assembled with mounted traffic sign.
```


## Placement

For placement of signs see [](traffic-signs-placement).
