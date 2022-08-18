# Rain Generator Blend

## Description

This Blend file provides a Geo Nodes group which can help you simulate rain using a fluid simulator like the built in one in [Blender](<https://www.blender.org/>) or using the [Flip Fluids Addon](<https://flipfluids.com/>).

## Usage

1. In a new file create a plane, Size this plane to the area you want to rain to fall

2. Add the geometry nodes modifier to the plane

3. Go to File Menu -> Link and select the downloaded blend file, you can also use append if you wish. In the Link / Append menu navigate to node groups and select the \|Rain geo modifier\|.

4. In the geometry nodes modifier on the plane select the linked / appended node group.

5. Play around with the settings to get something you like, view the next section for documentation on what the various settings do.

6. Add the fluid "Inflow" modifier to the plane object, if your using Flip Fluids you must also enable the animated emitter option.

7. Add some initial velocity to the object in the negative z axis. TIP, use a driver to vary the velocity on all three axis to simulate wind, using a force could also work.

8. At this point provided you set up everything else required for your fluid system it should just work.

## Geo Node Group Documentation

- **Density -** Controls the amount of instances spawned

- **Seed -** Random Seed, changing this value allows you to get different results

- **Min Scale -** The minimum scale of instanced objects

- **Max Scale -** The maximum scale of instanced objects

- **Rotation Min -** The minimum rotation of instanced objects

- **Rotation Max -** The maximum rotation of instanced objects

- **Animation -** Enables or disables the built in animation, you can turn this off if you want to animate the seed yourself.

- **Animate Every N Frames -** This controls when the instanced objects will switch to a new position. For example if you enter 5 the objects will switch location every 5 frames.\*\*

- **Move Faraway Inbetween N Frames -** In between every frame that is not a key frame, where new instance positions are set, see above, instances will be moved very far away so they are not within the simulation domain. This option is used instead of the below for the flip fluids addon or other simulator where changing topology or deleting instances in the middle of an animation causes problems.

- **Delete Inbetween N Frames -** Same as the above but deletes the instances instead of moving them. This should be off for Flip Fluids or you will get a changing topology warning when baking the simulation and things may react weird. The built in fluid simulator in Blender seems to handle this option fine.

- **Instance Type -** You have a couple options 0 - Sphere, 1 - Custom Object, or 2 - Custom Collection. A sphere will spawn a sphere for the instance. Custom object will spawn a object you choose, and custom collection will spawn a random object in a collection you choose as an instance.

- **Custom Instance Object -** See Above

- **Custom Instance Collection -** See Above

## Example

Open the blend file directly and select a scene to view an example of how the system is setup using the Flip Fluids Addon or Blender's built in fluid solver

## Issues

Please report issues on the [Github issues page](<https://github.com/NHodgesVFX/RainGeneratorBlend/issues>).

## License

[Rain Generator Blend ](<https://nhodgesvfx.com/Projects/RainGeneratorBlend.html>)© 2022 by [Nathan Hodges ](<https://nhodgesvfx.com/>)is licensed under [CC BY 4.0](<http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1>)

## Download

[Click Here](<https://github.com/NHodgesVFX/RainGeneratorBlend/raw/main/RainGenerator.blend>)
