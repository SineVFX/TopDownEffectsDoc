---
layout: default
title: Quick Start
nav_order: 1
---

### Important notes:

1. If you using URP make sure, you enable HDR, Depth and Opaque textures in URP Asset settings
1. Turn on "HDR" on your Camera, Shaders requires it
1. This VFX Asset looks much better in "Linear" Color Space, but if you using "Gamma" Color Space, you need to slightly decrease the Final Power (Emission Power) material parameter of each effect
1. Image Effects are necessary in order to make a great looking game, as well as our asset. Be sure to use "ACES Tone Mapping" and "Bloom"
1. Your camera must render Depth texture in order for some effects to appear correctly



### How to use:

1. First of all, check for Demo Scene in the Scenes folder. Also, there is a Prefabs folder with complete effects.
1. Drag and Drop prefabs from the "Prefabs" folder into your scene.
1. All animated prefabs are driven by standard animation system in Unity, you can freely customize these animations
1. For GoldMeteorites effects, you also need to assign the collision plane inside Particle System settings.



### BASIC ADJUSTMENTS AND CUSTOMIZATION:

1. You can scale, rotate and transform the prefab like you normally do.
1. When you scale the effect, you might also need to adjust the noise scale inside Material settings.
1. Most of the adjustments come from Material parameters.
1. Materials have a lot of settings, just play with them and create your own unique look. Be aware, that in a play mode, some materials will be converted into instances because their values are changing by the Animator component. So if you change material settings in a play mode, the original material won't be affected. This is a great way to just test all the settings.
1. Most of the parameters are described in a "02.MaterialParameters.txt" file.
1. Inside Portal prefabs, there are some disabled effects, this was made for easier customization. You can freely enable or disable them in order to create a unique look.



### Support email: sinevfx@gmail.com
