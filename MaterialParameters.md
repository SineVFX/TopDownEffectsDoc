---
layout: default
title: Material Parameters
nav_order: 4
---

## Material Parameters

Here is the description of the most tricky material parameters. Most parameters are named according to what they do to the material, but some require a more detailed explanation. Parameters sorted per shader name, you can see it on top of the material when selected in the inspector.

### General Material Parameters / DissolveParticleAdvanced:


Final parameters are mostly used to adjust the result look of the effect, its emission power, color (if not using Ramp), and opacity

* **Final Color** - Emission color of affected particles
* **Final Power** - Final brightness of the image, you need to lower this value if you using "Gamma Rendering" Mode
* **Final Opacity Power** - Adjust the opacity of the effect without changing its emission power
* **Final Opacity Exp** - Control the smoothness(curve) of the opacity mask, higher numbers will lead to more sharp transitions.

Changes in version 2.0
{: .label .label-yellow }
* **Final Opacity Double AoL Switch** - Makes Particle Alpha affect the opacity after clamping.


Other Ramp parameters are just used to further customize the gradient coloring mode

* **Ramp Enabled** - Use ramp gradient texture to colorize particles
* **Ramp** - Gradient texture, located in the "VFXTextures" folder
* **Ramp Color Tint** - Multiply ramp texture by this color
* **Ramp Affected By Dynamics** - How much Dynamics (dissolving and appear effects) will affect the ramp texture. So, when the particle begins to dissolve, the color of dissolve areas will change according to the ramp gradient.
* **Ramp Offset Multiply** - Multiply the Ramp position, and use it to offset ramp colors
* **Ramp Offset Exp** - Power (Math) the Ramp position, and use it to offset ramp colors but in a more smooth way.
* **Ramp Ignore Vertex Color** - Ramp ignore the particle/vertex color

Changes in version 2.0
{: .label .label-yellow }
* **Ramp Add** - Add a value to a Ramp Mask, offsetting the gradient.
* **Ramp Add VS Switch** - Add a value from a Vertex Stream to a Ramp Mask, offsetting the gradient.


Custom Color mask is used when you need to color your particles with a ramp gradient using a specific mask.

* **Custom Color Mask Channels** - What channels to use from the color mask
* **Custom Color Mask Switch** - Enabling and disabling the mask
* **Custom Color Mask Affected By Dynamics** - Controls how much Dynamics (dissolving and appear effects) will affect the mask texture. So, when the particle begins to dissolve, the color of dissolve areas will change according to mask and ramp gradient.


The second Mask is used mainly to show the effect of Indicator Effects and some other particles. It is also controlled with Custom Vertex Stream.

* **Second Mask Profile** - Profile gradient mask, utilizing R (emission boost) and G (opacity) channels.
* **Second Mask Negate** - Negating/disabling the second mask
* **Second Mask VS Move** - Moving the second mask UV, driven by Custom Vertex Stream
* **Second Affects Distortion** - Distortion only applies to the R channel of the second mask
* **Second Mask Noise 01 Negate** - Noise 01 will be negated in the R channel of the second mask
* **Second Mask Affects Ramp** - The R channel of the second mask will be added to the ramp, adjusting the ramp position as a result
* **Second Mask Boosts Emission** - Boosting emission in the R channel of the second mask
* **Second Mask Fract Switch** - Apply fract function to the second mask, making it look like a saw wave
* **Second Mask Fract Shrink** - Stretching the resulting fract mask


Noise parameters are generally used to customize the mask of the effect. This is the most adjustable part of the effects, you can freely change and scale the noise textures. There are plenty of noise textures in this Asset.

* **Noise, Noise 01, and Noise 02** - Noise textures for creating the final noise mask, you can play with this parameter freely and use your own noise textures
* **Noise Scale** - Scale of the noise texture
* **Noise Negate** - Negating the noise texture, making it full white
* **Noise Exp** - Applying Power (Math) to the Noise texture
* **Noise Scroll Speed** - Scroll/Panning speed of the texture
* **Noise Random Min Max** - Min and Max parameters for making a unique noise texture offset for each particle
* **Noise Radial** - Change UV from regular to radial mapping


Dissolve Texture is used for the dissolve/disappear effect. It has many parameters, controlling the slope of the dissolve, scale, and edges emission.

* **Dissolve Texture Flip Switch** - Flip the dissolve texture colors (one minus dissolve texture colors)
* **Dissolve Texture Scale** - Scale of the dissolve texture
* **Dissolve Texture Min Max** - Min and Max parameters for making a unique dissolve texture offset for each particle
* **Dissolve Texture Radial** - Change UV from regular to radial mapping
* **Dissolve Texture Exp** - Applying Power (Math) the dissolve texture
* **Dissolve Texture Exp Reversed** - Applying Power (Math) the dissolve texture is based on particle lifetime, also in reverse
* **Dissolve Glow** - Set of parameters, controlling the glowing edges when the dissolve is happening
* **Dissolve Mask** - Sets the direction (with a texture mask) along which the dissolve will occur
* **Dissolve Steepness** - Control the steepness/slope of the dissolve mask


Distortion Texture is used for the UV distortion effect.

* **Distortion Scale** - Scale of the distortion texture
* **Distortion Power** - Amount of UV distortion
* **Distortion Remap Min/Max** - Min and Max parameters for making a unique distortion texture offset for each particle
* **Distortion UV or Spherical** - Vector for distortion
* **Distortion U/V** - Control U and V channels separately
* **Distortion Scroll Speed** - Scroll/Panning speed of the texture
* **Distortion Radial** - Change UV from regular to radial mapping

Changes in version 2.0
{: .label .label-yellow }
* **Distortion Scroll VS Enabled** - Enables the Vertex Stream used for scrolling the distortion texture, useful for heat emitation.
* **Radial Distortion Intensity Switch** - Enabled Radial Mask to control the distortion intensity, lower intensity at the center and higher at the edge.
* **Radial Distortion Exp** - Control the smoothness of the Radial Distortion Mask.
* **Radial Visibility Switch** - Apply the Radial Mask to control the opacity of the wave effect.
* **Radial Visibility Mask Value** - Offsets the Radial Mask.
* **Radial Visibility Mask Exp** -  Control the smoothness of the Radial Opacity Mask.


Soft particles is a common effect, it is making particles less visible when they intersect other geometry.

* **Soft Particles Enabled** - Enable the soft particles effect
* **Soft Particles Enabled** - Distance/Thickness of the effect


### Crystal:

* **Inner Rim** - Glowing inside of a crystal, you can control how much of crystal original normals are influencing this effect. You can also apply a texture mask the the whole effect.
* **Vertical Gradient** - Vertical emission gradient in the local mesh coordinates.
* **Appear Gradient** - Same as Vertical Gradient, but it will stay at the same place when changing the "Appear Vertex Y Offset" parameter to move crystal on the local Y-axis.
* **Parallax Noise** - Noise inside the crystal, try to change the texture and the scale of it.


### CenterCurve:

* **Second Mask** - In this shader, the Second Mask is used differently. It is a projectile texture, scrolled along the UV of the mesh, making the final effect.
* **Fresnel Mask** - Rim Mask, used to hide sharp edges of the effect mesh.


### ShieldICO:

* **Offset Texture** - Texture, used to local vertex offset.
* **Tris Glare** - Making effect triangles to glare randomly, imitating the fake lighting.
* **Vertical Gradient** - Applying the vertical gradient to the shield effect. You can change its form and use a custom profile texture.
* **Inner Rim** - Simple Rim/Fresnel effect
* **Waves** - Generating waves for offset and emission
* **Depth Mask** - Depth Blend effect, similar to the Soft Particles effect, but in this case, it will boost the emission when the mesh intersects other opaque geometry.
* **Appear Gradient** - This section is used mainly for appear/disappear effects. Animate the "Appear Gradient Offset" parameter and see the results.


### Props:

* **Albedo Decal** - Coloring the decal parts of Albedo map
* **Rim Emission** - Simple Rim/Fresnel effect
* **Dissolve** - This section controls the dissolve/appear effect of the mesh, check the complete effects (like HammerStrine or SourceEnergyShield) for the examples.


### MaskedDoubleSidedAdvanced:

Most parameters in this shield/barrier effect shader are self-explanatory. It uses many Noise textures to make the effect, you can tweak all the parameters in real time to see what they do. Check the effects like FireBarrier or WaterBarrier to see this shader in action. The main parameter is "Appear Progress" it is animated with a regular Unity animation system.


### DissolveParticleMV:

* **MV Main Mask** - Main flip book mask
* **MV Main Mask Motion Vectors** - Motion vectors, for the smooth slow-motion animation
* **MV Random Frame** - Start the animation from a random frame when a particle is spawned
* **MV Distortion Frame Offset** - Don't change this parameter, it is used for setting up the right value for smooth Motion Vectors transition technique
* **MV Particle Frame Control Enabled** - Use particle system custom vertex stream instead of "MV Animation Speed" to control the animation of flipbook


### DissolveParticleGroundPacked:

* **PackedTex** - Packed ground texture, you can pick from many different ones
* **Height Slope Control** - Msaking slopes smoother
* **Height Boost** - Increase height of PackedTex texture
* **Height Map Negate** - Negating the B channel (baked height) of the PackedTex texture
* **Albedo** - Colorize the ground rocks
* **Opacity Mask** - Main opacity mask, applied to the whole effect
* **Second Mask** - The second mask is used only for appear effect (Also controlled with Custom Vertex Streams)
* **Lava Appear Mask** - This mask is used to make lava appear, respecting the final height parameter of a texture (Also controlled with Custom Vertex Streams)
* **Surface Noise** - Add noise texture to the final height
* **Valleys Emission Boost** - Boosts emission if valleys
* **Cracks** - Applying cracks texture to the albedo (color of non-emissive ground) and height
* **Dissolve Texture** - This section is used for the dissolve/disappear effect (Also controlled with Custom Vertex Streams)


### DissolveParticleDepth:

* **Rim Mask** - Simple Rim/Fresnel effect
* **Offset Noise** - Used for the mesh/particle surface offset (Also controlled with Custom Vertex Streams)
* **Depth Fade** - The depth fade effect (similar to the Soft Particle effect), can be flipped and will boost the emission of intersecting parts instead


### FakeTrailAndMeshFireParticle:

* **Main Mask** - Main texture mask of a trail, set it to Clamp only on V coordinate
* **Squeeze UV** - Squeezing UV towards the start point of fire/trail particle
* **Fake Trail Scroll** - This section is used to control the scrolling animation of a trail (Also controlled with Custom Vertex Streams)


### DissolveParticleFlipBook:

This shader is basically the same as DissolveParticleAdvanced but uses flipbooks for its animation. Used mostly for electric and lightning effects, it also has dissolve/appear effects. Set the rows and columns of the material, rotate the UV as you like and it is mostly done. For other parameters, check the DissolveParticleAdvanced section at the top of this page.


Changes in version 2.0
{: .label .label-yellow }
### DissolveParticleNonLinear:

* **Flow Texture** - Main noise texture used for the effect
* **Flow Curve Exp** - Changing the animation curve of the scrolling Noise texture. Control the density of the noise towards the start or the end of the UV coordinate position.
* **Flow Scale U** - Scaling of the noise texture in one direction
* **Flow Scroll Speed** - Scroll speed of a main noise texture
* **Flow Mask SS11-...-SS22** - SmoothStep parameters to create a smooth fade on both ends of a texture. It is recommended to use values between 0 and 1 to avoid sharp edges.
* **Flow Texture 2** - Second noise texture used to multiply the first noise texture by it
* **Flow Texture 2 Negate** - Negates the influence of a second noise texture
* **Horizontal Mask** - Mask based on the U coordinate
* **Global Mask** - Mask based on a separate texture, you can try using the included Mask textures
* **MANUAL Dissolve Progress** - Control the dissolve from both sides. This parameter is only available in the mesh version of a shader.


### DissolveParticleCloudy_v2:

* **Smoke Lighting and Heat Textures** - Textures used for smoke and emissive heat effects
* **Smoke Texture Scroll** - Control how the scrolling of a smoke texture is processed. If the manual mode is selected, use Vertex Streams for the scrolling
* **Smoke Texture Spherical Distance** - Control the spherical distortion of the smoke texture
* **Border Smooth Amount** - Making the borders of the sprite smoother


### DissolveParticleGroundWaveOffset_v2:

* **Flow Texture Parameters** - Same as in the "DissolveParticleNonLinear" shaders, their parameters are described above.
* **Offset Wave Amount** - Strength of the vertex offset effect


### DissolveParticleMVForExplosions_v2:

* **Explosion Lighting Color 1 and 2** - Color of the smoke fake lighting
* **Emission Vertex Stream Enabled** - Enables the vertex stream to control the emission intensity
* **Explosion Lighting Vector Adjustment** - Adjust the screen-spaced vector for the fake smoke lighting.
* **Dissolve Parameters** - Adding dissolve to the flipbook animation for more artistic control. More info for the dissolve parameters is available at the top of the page.
* **Distortion Parameters** - Unlike in other shaders, distortion is only applied when the dissolve is present. More info for the distortion parameters is available at the top of the page.



### Support email: sinevfx@gmail.com
