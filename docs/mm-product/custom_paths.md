# Custom Paths

TODO: Introduction/description

!!! warning
    This is a **Beta feature**, so there may be some minor bugs & issues.

## Path Definition

A **Path** is comprised of **Segments**.

These segments are stitched together, and run through a simulation process to create a path.

A path can be defined in a json object (read from a file) with two properties:
- `info` - An object containing global information that is consistent throughout the entire path
- `segments` - An **array** of objects, with each array element defining a segment

The keys allowed in the `info` object are as follows:

!!! info
    All angles are measured in degrees, **anticlockwise** from the forwards direction

| Property           | Description                                                           |
|--------------------|-----------------------------------------------------------------------|
| `start_from_idle` Default: `false`       | Defines whether the path will start simulating from idle, with an initial speed of 0               |
| `root_offset`  Default: `0`       | An additional rotation added to the root bone throughout the animation|
| `init_direction` Default: `0`       | The initial direction that the first segment will move in|

Segment objects can contain the following properties:

| Property           | Description                                                           |
|--------------------|-----------------------------------------------------------------------|
| `duration`       | How long (in frames) this segments should last. This property is required. Note: the frame rate is currently locked at 30fps               |
| `turn_angle`  Default: `0`       | The simulator will rotate the velocity of the previous segment by this amount. |
| `speed_index` Default: `1`       | Specifies which speed (of the speeds array) that the segment will use. When using PDC, `0` is idle, `1` is Max Speed and `2` is Min Speed|
| `facing_velocity` Default: `true`       | Dictates whether the character should face the direction they are moving. If set to `false`, they will face the `strafe_face_angle`|
| `strafe_face_angle` Default: `0`       | Angle in **global** space that the character will face when `facing_velocity` is set to `false`|
| `start_angspeed` Default: `0`       | The rotation rate (in degrees per second) that the segment will arc at. Higher values result in tighter arcs|
| `end_angspeed` Default: `==start_angspeed`       | The rotation rate the character should have at the **end** of the segment. If undefined, it will be equal to `start_angspeed`, meaning a constant angular speed. If set, the angular speed will interpolate between these two values across the segment.|
| `accel_multiplier` Default: `1.0`       | Value that this segment will multiply the path builder's acceleration by|
| `decel_multiplier` Default: `1.0`       | Value that this segment will multiply the path builder's deceleration by|
| `post_turn` Default: `0.5`       | Dictates when the character will start their turn for this segment. `0.5` means the turn will start immediately as the segment begins. `0.0` means the turn will **finish** as the segment begins (a 'pre-turn'). `1.0` means the turn will start with a delay after the segment begins (a 'post-turn')|

## Creating Paths

In the root folder of the Blender project, you will need to create a folder called `mo_paths`, if it does not already exist.

Within this folder, any subfolders represent a Dance Card set. They can be selected via the dropdown as you usually would in the PDC menu. Currently, custom path definitions are only compatible with **Custom** mode, and have not yet been implemented into **Simplified** mode.

Then, you may create a `.json` file in this subfolder to define a path for the set. The simplest path is defined as so (as seen in `mo_paths/simple_examples/straight.json`)

!!! info
    For a full reference of example paths, check the `mo_paths` folder for simple and complex examples!

```
{
    "info": {},
    "segments": [
        {
            "duration": 90
        }
    ]
}
```
As you can see, the only property that **must** be defined is `duration`. Each path must have **at least one** segment.