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

Noise parameters are generally used to customize the mask of the effect. This is the most adjustable part of the effects, you can freely change and scale the noise textures. There are plenty of noise textures in this Asset.

* **Noise, Noise 01 and Noise 02** - Noise textures for creating the final noise mask, you can play with this parameter freely and use your own noise textures
* **Noise Scale** - Scale of the noise texture
* **Noise Negate** - Negating the noise texture, making it full white
* **Noise Exp** - Applying Power (Math) the Noise texture
* **Noise Scroll Speed** - Scroll/Panning speed of the texture
* **Noise Random Min Max** - Min and Max parameter for making a unique noise texture offset for each particle
* **Noise Radial** - Change UV fron regular to radial mapping

Dissolve Texture is used for the dissolve/disappear effect. It has many parameters, controlling the slope of the dissolve, scale, and edges emission.

* **Dissolve Texture Flip Switch** - Flip the dissolve texture colors (one minus dissolve texture colors)
* **Dissolve Texture Scale** - Scale of the dissolve texture
* **Dissolve Texture Min Max** - Min and Max parameter for making a unique dissolve texture offset for each particle
* **Dissolve Texture Radial** - Change UV fron regular to radial mapping
* **Dissolve Texture Exp** - Applying Power (Math) the dissolve texture
* **Dissolve Texture Exp Reversed** - Applying Power (Math) the dissolve texture based on particle lifetime, also in reverse
* **Dissolve Glow** - Set of parameters, controlling the glowind edges when the dissolve is happening
* **Dissolve Mask** - Sets the direction (with a texture mask) along which the dissolve will occur
* **Dissolve Steepness** - Control the steepness/slope of the dissolve mask

Dissolve Texture is used for the dissolve/disappear effect. It has many parameters, controlling the slope of the dissolve, scale, and edges emission.

* **Dissolve Texture Flip Switch** - Flip the dissolve texture colors (one minus dissolve texture colors)
* **Dissolve Texture Scale** - Scale of the dissolve texture
* **Dissolve Texture Min Max** - Min and Max parameter for making a unique dissolve texture offset for each particle
* **Dissolve Texture Radial** - Change UV fron regular to radial mapping
* **Dissolve Texture Exp** - Applying Power (Math) the dissolve texture
* **Dissolve Texture Exp Reversed** - Applying Power (Math) the dissolve texture based on particle lifetime, also in reverse
* **Dissolve Glow** - Set of parameters, controlling the glowind edges when the dissolve is happening
* **Dissolve Mask** - Sets the direction (with a texture mask) along which the dissolve will occur
* **Dissolve Steepness** - Control the steepness/slope of the dissolve mask



### Support email: sinevfx@gmail.com
