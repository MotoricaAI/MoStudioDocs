# Custom Paths

The **Import Custom Path Set** feature allows you to define your own path sets for use in our Motion Matching workflow. Here you will find a fill reference on how to define these paths.

!!! warning
    This is a **Beta feature**, so there may be some minor bugs & issues.

## Path Definition

A **Path** is comprised of **Segments**.

These segments are stitched together, and run through a simulation process to create a path.

A path is defined in a json object with two properties:
- `info` - An object containing global information that is consistent throughout the entire path
- `segments` - An **array** of objects, with each array element defining a segment.

## Creating Paths

Each path is defined in an individual json file. The name of the dance card will be the name of the json file. The simplest path is defined as so:

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

!!! tip
    To view examples of more complex paths, download our samples [here](https://drive.google.com/file/d/1Ds5ySjlvcYy-himAtRdaTHwys1MMq6rf/view?usp=sharing)!

## Property Reference

The properties allowed in the `info` object are as follows:

| Property           | Description                                                           |
|--------------------|-----------------------------------------------------------------------|
| `start_from_idle` Default: `false`       | Defines whether the path will start simulating from idle, with an initial speed of 0               |
| `root_offset`  Default: `0`       | An additional rotation added to the root bone throughout the animation|
| `init_direction` Default: `0`       | The initial direction that the first segment will move in|

!!! info
    All angles are measured in degrees, **anticlockwise** from the forwards direction

Segment objects can contain the following properties:

| Property           | Description                                                           |
|--------------------|-----------------------------------------------------------------------|
| `duration`       | How long (in frames) this segments should last. This property is required. Note: the frame rate is currently locked at 30fps               |
| `turn_angle`  Default: `0`       | The simulator will rotate the velocity of the previous segment by this amount. |
| `speed_index` Default: `1`       | Specifies which speed (of the speeds array) that the segment will use. `0` is idle, `1` is Max Speed and `2` is Min Speed|
| `facing_velocity` Default: `true`       | Dictates whether the character should face the direction they are moving. If set to `false`, they will face the `strafe_face_angle`|
| `strafe_face_angle` Default: `0`       | Angle in **global** space that the character will face when `facing_velocity` is set to `false`|
| `start_angspeed` Default: `0`       | The rotation rate (in degrees per second) that the segment will arc at. Higher values result in tighter arcs|
| `end_angspeed` Default: `==start_angspeed`       | The rotation rate the character should have at the **end** of the segment. If undefined, it will be equal to `start_angspeed`, meaning a constant angular speed. If set, the angular speed will interpolate between these two values across the segment.|
| `accel_multiplier` Default: `1.0`       | Value that this segment will multiply the path builder's acceleration by|
| `decel_multiplier` Default: `1.0`       | Value that this segment will multiply the path builder's deceleration by|
| `post_turn` Default: `0.5`       | Dictates when the character will start their turn for this segment. `0.5` means the turn will start immediately as the segment begins. `0.0` means the turn will **finish** as the segment begins (a 'pre-turn'). `1.0` means the turn will start with a delay after the segment begins (a 'post-turn')|
