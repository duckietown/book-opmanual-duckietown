```{seo}
:description: Step-by-step guide to assembling and customizing traffic signs in Duckietown, including AprilTag ID ranges, new signage creation, and placement rules.
:keywords: Duckietown, traffic signs, AprilTags, robotics, signage assembly, modular cities, new signage creation, traffic signs placement
```


(dt-ops-city-traffic-signs)=
# Assembly - Traffic Signs

```{needget}
The materials to build Duckietown signals ([Duckietown project shop](https://get.duckietown.com/products/additional-traffic-signs))
---
A set of signs to be used for assembling your Duckietown.
```

## Build a Map

Before starting sign assembly, design a tilemap that complies with the [tilemap layer specifications](specs-layer-tilemap).

The full set of currently existing signs is available [here](https://github.com/duckietown/signs-and-tags).

(making-new-signage)=
## Making New Signage

If the available database does not meet your needs, you can add new signage to the existing database.

Clone the [signs-and-tags](https://github.com/duckietown/signs-and-tags) repository:

```bash
git clone git@github.com:duckietown/signs-and-tags
```

The file `tag36h11.pdf` in the repo contains the already-generated tags. The type of sign you are adding determines the tag you should use. Refer to [](tab:tag-ranges) for tag ranges.

```{list-table} AprilTag ID Ranges
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

### Steps to Add a New Sign

1. Identify the last sign of the type you want to make in the `Signs_and_tags_V3.docx` file.
2. Use the next available ID after the last one.
3. Copy and paste an existing sign of a similar type and replace/add the new AprilTag.
4. For the new AprilTag, crop precisely around the tag at the top and sides and include the sign ID at the bottom. Resize the tag to exactly `6.5cm` (`2.56in`) and paste it into the Word file.
5. If creating a new road name sign, adjust the font size so the name fits on one line.

```{attention}
You must add your new sign to the `apriltagsDB.yaml`.
```

Add a new block or modify an existing one with the appropriate tag ID:

```yaml
- tag_id: ![NEW_TAG_ID]
  tag_type: {TrafficSign, Light, Localization, StreetName}
  street_name: ![NEW_STREET_NAME] or blank
  vehicle_name: currently not used
  traffic_sign_type: ![TRAFFIC_SIGN_TYPE] or blank
```

- Set `![NEW_STREET_NAME]` creatively.
- Use one of the types from [](tab:traffic-signs) for `![TRAFFIC_SIGN_TYPE]`.

Finally, regenerate the PDF version of the Word file and commit the changes via a pull request.

```{note}
To use a different signs and tags database, ensure you specify the correct database in the `april_tags` code.
```

## Traffic Signs Assembly

### Assemble the Stands

A traffic sign stand consists of laser-cut components, as shown in {numref}`fig:traffic_stand_assembly_1`.

```{figure} ../../_images/assembly/traffic_signs/trafficsign_kit.png
:width: 50%
:name: fig:traffic_stand_assembly_1

Traffic sign stand kit
```

Detach the wooden components and assemble them as shown in {numref}`fig:traffic_stand_assembly_2`. If the structure seems loose, apply wood glue for added stability.

```{figure} ../../_images/assembly/traffic_signs/trafficsign_stand_assembly.png
:width: 35%
:name: fig:traffic_stand_assembly_2

Traffic sign stand assembled
```

Once assembled, mount the traffic sign as shown in {numref}`fig:traffic_stand_assembly_3`.

```{figure} ../../_images/assembly/traffic_signs/trafficsign_stand_assembled.png
:width: 35%
:name: fig:traffic_stand_assembly_3

Traffic sign stand assembled with mounted traffic sign
```

## Placement

Refer to [](specs-layer-traffic-signs-placement) for guidelines on sign placement.

