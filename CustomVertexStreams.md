---
layout: default
title: Custom Vertex Streams
nav_order: 5
---

## Custom Vertex Streams

Many Particle Effects parameters are controlled via Custom Vertex Streams. Such parameters like Emission Power, Dissolve Progress, Appear and Disappear, Random Offset for Noise Textures, and etc. Check the name of a shader used in the Particle System, find it on this page, and check what each Custom Vertex Stream does. Try to modify, for example, the Dissolve Progress parameter for the "DissolveParticleAdvanced" shader and make particles disappear quicker or slower.

![s17](/assets/images/Screenshot_17.png)

For more information, you can check the official Unity Documentation: [https://docs.unity3d.com/Manual/PartSysVertexStreams.html](https://docs.unity3d.com/Manual/PartSysVertexStreams.html)

### DissolveParticleSimple:

* **Custom1.X / UV0.Z** - Random value for adjusting the offset of Main Texture
* **Custom1.Y / UV0.W** - Random value for adjusting the scale of the Main Texture
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Random value for flipbook frames

### DissolveParticleAdvanced:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Distortion Power Multiplier, used to control texture distortion over a lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over a lifetime
* **Custom2.X / UV1.Z** - Secondary Mask offset, used to multiply opacity by moving this mask texture with Vertex Streams
* **Custom2.Y / UV1.W** - Secondary Mask negate, use this to control how much Second Mask affects the opacity
* **Custom2.Z / UV2.X** - Distortion Mask offset, used to multiply distortion by moving this mask texture with Vertex Streams

Changes in version 2.0
{: .label .label-yellow }
* **Custom2.Z / UV2.X** - UV Offset / Scroll of a Distortion texture, used to imitate heat effects
* **Custom2.W / UV2.Y** - Controls the Gradient Ramp color by offsetting the mask texture, useful to imitate Fire to Smoke transitions

### DissolveParticleDepth:

* **Custom1.X / UV0.Z** - Emission Multiplier, control the emission power over the lifetime
* **Custom1.Y / UV0.W** - Offset and Dissolve Progress, this parameter will affect both the dissolve and offset parameters
* **Size / UV1.X** - Adjusting the scale multiplier depending on particle size (No need to modify this parameter, it is a fix)

### DissolveParticleGroundPacked:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Secondary Mask (Appear/Initialize) progress, use this to make the effect appear
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over a lifetime
* **Custom2.X / UV1.Z** - Lava Appear progress, control the appearance of lava

### FakeTrailAndMeshFireParticles:

* **Custom1.X / UV0.Z** - Control the U gradient mask, used for fade-in and fade-out effects of the fire
* **Custom1.Y / UV0.W** - Custom UV offset animation, moving the whole fire mask texture, used to make moving fire trail look more realistic
* **Custom1.Z / UV1.X** - Random value for each particle, to make them look slightly different

### DissolveParticleMV / DissolveParticleFlipBook:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Distortion Power Multiplier, used to control texture distortion over lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over a lifetime
* **Custom2.X / UV1.Z** - Secondary Mask offset, used to multiply opacity by moving this mask texture with Vertex Streams
* **Custom2.Y / UV1.W** - Secondary Mask negate, use this to control how much Second Mask affects the opacity
* **Custom2.Z / UV2.X** - Distortion Mask offset, used to multiply distortion by moving this mask texture with Vertex Streams
* **Custom2.W / UV2.Y** - Custom frame animation control for a flipbook texture, enable the "MV Particle Frame Control Enabled" parameter in material settings to use this Vertex Stream.

Changes in version 2.0
{: .label .label-yellow }
* **Custom2.Z / UV2.X** - Controls the Gradient Ramp color by offsetting the mask texture, useful to imitate Fire to Smoke transitions

### DissolveParticleWave:
This is a variation of a DissolveParticleAdvanced shader with some tweaks, used to make wave-like effects.

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Distortion Power Multiplier, used to control texture distortion over a lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over a lifetime
* **Custom2.X / UV1.Z** - 
* **Custom2.Y / UV1.W** - Main Mask offset, used to create a moving wave effect
* **Custom2.Z / UV2.X** - Distortion Mask offset, used to multiply distortion by moving this mask texture with Vertex Streams

Changes in version 2.0
{: .label .label-yellow }
* **Custom2.Z / UV2.X** - UV Offset / Scroll of a Distortion texture, used to imitate heat effects
* **Custom2.W / UV2.Y** - Controls the Gradient Ramp color by offsetting the mask texture, useful to imitate Fire to Smoke transitions

### DissolveParticleCloudy:
A new shader was added in version 2.0, useful for small cloud-like explosions.

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Heat Texture Emission Multiplier, control the emission power over a lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - BLANK
* **Custom2.X / UV1.Z** - BLANK
* **Custom2.Y / UV1.W** - Cloud texture scroll/offset over a lifetime, enable the "Smoke Texture Scroll Manual" to see the effect.
* **Custom2.Z / UV2.X** - Controls the Smoke Gradient Ramp color by offsetting the mask texture, useful to imitate Fire to Smoke transitions
* **Custom2.W / UV2.Y** - Controls the Heat Gradient Ramp color by offsetting the mask texture, useful to imitate Fire to Smoke transitions

### CenterCurve:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Emission Multiplier, control the emission power over a lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Second Mask offset progress, used to move the second mask on V coordinate

### Props:

* **Custom1.Z / UV1.X** - Dissolve/Appear Effect progress control. Used to control the dissolve effect of the mesh when it appears or disappears.



### Support email: sinevfx@gmail.com
