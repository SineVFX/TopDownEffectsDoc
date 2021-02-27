---
layout: default
title: Material Parameters
nav_order: 4
---

## Material Parameters

Here is the description of the most tricky material parameters. Most parameters are named according to what they do to the materil, but some requeres a more detailed explanation. Parameters sorted per shader name, you can see it on top of material when selected in the inspector.

### General Material Parameters:

Final parameters are mostly used to adjust the result look of the effect, its emission power, color (if not using Ramp) and opacity

* **Final Color** - Emission color of affected particles
* **Final Power** - Final brightness of the image, you need to lower this value if you using "Gamma Rendering" Mode
* **Final Opacity Power** - Adjust the opacity of the effect without changing its emission power
* **Final Opacity Exp** - Control the smoothness(curve) of opacity mask, higher numbers will lead to more sharp transitions.

Other Ramp parameters just used to further customize the gradient coloring mode

* **Ramp Enabled** - Use ramp gradient texture to colorize particles
* **Ramp** - Gradient texture, located in "VFXTextures" folder
* **Ramp Color Tint** - Multiply ramp texture by this color
* **Ramp Affected By Dynamics** - How much Dynamics (dissolving and appear effects) will affect the ramp texture. So, when the particle is begin to dissolve, the color of dissolve areas will change according to ramp gradient.
* **Ramp Offset Multiply** - Multiply the Ramp position, use it to offset ramp colors
* **Ramp Offset Exp** - Power (Math) the Ramp position, use it to offset ramp colors but in a more smooth way.
* **Ramp Ignore Vertex Color** - Ramp ignore the particle/vertex color

Custom Color mask is used when you need to color your particles with a ramp gradient using a specific mask.

* **Custom Color Mask Channels** - What channels to use from color mask
* **Custom Color Mask Switch** - Enabling and disabling the mask
* **Custom Color Mask Affected By Dynamics** - How much Dynamics (dissolving and appear effects) will affect the mask texture. So, when the particle is begin to dissolve, the color of dissolve areas will change according to mask and ramp gradient.

Second Mask is used mainly for appear effect of Indicator Effects and some othe particles. It is also controlled with Custom Vertex Stream.

* **Second Mask Profile** - Profile gradient mask, utilizing R (emission boost) and G (opacity) channels.
* **Second Mask Negate** - Negating/disabling the second mask
* **Second Mask VS Move** - Moving the second mask UV, driven by Custom Vertex Stream
* **Second Affects Distortion** - Distortion only applies to the R channel of second mask
* **Second Mask Noise 01 Negate** - Noise 01 will be negated in the R channel of second mask
* **Second Mask Affects Ramp** - R channel of second mask will be added to the ramp, adjusting the ramp position as a result
* **Second Mask Boosts Emission** - Boosting emission in the R channel of second mask
* **Second Mask Fract Switch** - Apply fract function to the second mask, making it looks like a saw wave
* **Second Mask Fract Shrink** - Stretching the resulting fract mask

### DissolveParticleSimple:

A simple dissolving particle, used for embers, small stars and simillar particle effects.

* **Custom1.X / UV0.Z** - Random value for adjusting offset of the Main Texture
* **Custom1.Y / UV0.W** - Random value for adjusting scale of the Main Texture
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Random value for flipbook frames

### DissolveParticleAdvanced:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Distortion Power Multiplier, used to control texture distortion over lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over lifetime
* **Custom2.X / UV1.Z** - Secondary Mask offset, used to multiply opacity by moving this mask texture with Vertex Streams
* **Custom2.Y / UV1.W** - Secondary Mask negate, use this to control how much Second Mask affecting opacity
* **ustom2.Z / UV2.X** - Distortion Mask offset, used to multiply distortion by moving this mask texture with Vertex Streams

### DissolveParticleDepth:

* **Custom1.X / UV0.Z** - Emission Multiplier, control the emission power over the lifetime
* **Custom1.Y / UV0.W** - Offset and Dissolve Progress, this parameter will affect both the dissolve and offset parameters
* **Size / UV1.X** - Adjusting the scale multiplier depending on particle size (No need to modify this parameter, it is a fix)

### DissolveParticleGroundPacked:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Secondary Mask (Appear/Initialize) progress, use this to make effect appear
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over lifetime
* **Custom2.X / UV1.Z** - Lava Appear progress, control the appearence of lava

### FakeTrailAndMeshFireParticles:

* **Custom1.X / UV0.Z** - Control the U gradient mask, used for fade in and fade out effects of the fire
* **Custom1.Y / UV0.W** - Custom UV offset animation, moving the whole fire mask texture, used to make moving fire trail look more realistic
* **Custom1.Z / UV1.X** - Random value for each particle, to make them look slightly different

### DissolveParticleMV / DissolveParticleFlipBook:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Distortion Power Multiplier, used to control texture distortion over lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over lifetime
* **Custom2.X / UV1.Z** - Secondary Mask offset, used to multiply opacity by moving this mask texture with Vertex Streams
* **Custom2.Y / UV1.W** - Secondary Mask negate, use this to control how much Second Mask affecting opacity
* **Custom2.Z / UV2.X** - Distortion Mask offset, used to multiply distortion by moving this mask texture with Vertex Streams
* **Custom2.W / UV2.Y** - Custom frame animation control for a flipbook texture, enable "MV Particle Frame Control Enabled" parameter in material settings to use this Vertex Stream.

### CenterCurve:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Emission Multiplier, control the emission power over lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Second Mask offset progress, used to move the second mask on V coordinate

### Props:

* **Custom1.Z / UV1.X** - Dissolve/Appear Effect progress control. Used to control the dissolve effect of the mesh when it appears or disappears.



### Support email: sinevfx@gmail.com
