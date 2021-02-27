---
layout: default
title: Scaling and adjusting
nav_order: 2
---

## General info

Most of the adjustments come from Material parameters and [Custom Vertex Streams](https://docs.unity3d.com/Manual/PartSysVertexStreams.html). Such particle animations like dissolve, emission power, and appear progress are driven with Vertex Streams. Some effects using control particles to spawn other particles as SubEmitters. Control Particles are invisible, they have their "Renderer" module turned off completely. But you can control the emitter component as you like. For example, you can increase emitter frequency, to make more rockets/missiles to spawn during the effect lifetime.

Materials have a lot of settings, just play with them and create your own unique look. Be aware, that in a play mode, some materials will be converted into instances because their values are changing by the Animator component. So if you change material settings in a play mode, the original material won't be affected. This is a great way to just test all the settings. Most of the parameters are described in a "02.MaterialParameters.txt" file.

### Scaling

1. You can scale, rotate and transform the prefab like you normally do.
1. When you scale one of these effects (StormBeacon, SummonStorm, IonMarker, FusionCore), you might also need to adjust the "Soft Particles Distance" parameter of smoke and clouds-like materials. For example, if you scale your model by 0.01, you need to multiply this parameter byt the same amount. By default it is set to 0.2f and the result value should be 0.002f, but this depends on camera depth, sometimes you need to adjust it by eye.

![s20](/assets/images/Screenshot_20.png)

### Basic Adjustments

1. (Color) Color is set in the material settings, but it is affecter by particle color too. You can use a single color or a ramp texture. When using ramp gradient texture to color your particles, check the "Ramp Ignore Vertex(Particle) Color" parameter if you want to multiply the result by particle color. There is a "RampGeneratorTDE" script, you can attach it to the effects and generate ramp in runtime, or you can bake it as a texture (keep all ramp textures in Clamp mode).

![s21](/assets/images/Screenshot_21.png)

1. (Noise) Effects have many Noise textures, try to change their scroll speed ans scale parameters. There are plenty of additional noise textures included in this Asset.
1. (Texture Animation) Some effects using flopbooks, you can control the animation speed in the material settings. You also can control the animation manually via vertex stream, enable "MV Particle Frame Control Enabled" parameter to do so.

### Advanced Adjustments

1. (Vertex Stream)
1. (Vertex Stream)
1. (Vertex Stream)



### Support email: sinevfx@gmail.com
