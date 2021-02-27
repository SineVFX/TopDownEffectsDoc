---
layout: default
title: Quick Start
nav_order: 1
---

## Quick start

First of all, you need to unpack the right packages for your specific setup of Unity. This Asset contains three packages, for **Standard**, **HDRP**, and **URP** pipelines. Start with **Step_1_CoreResources** package, it will add all core resources (textures, scripts, and animations) needed for this Asset. After that, pick the right SRP package and unpack it too. It will add all other components like prefabs of complete effects, scenes, materials, and shaders. If you using Standard pipeline and already have PostProcessing Stack V2 in your project, you can uncheck it when unpacking the **Standard** package.

### Important notes

1. (URP) Make sure, you enable HDR, Depth and Opaque textures in URP Asset settings.
![s19](/assets/images/Screenshot_19.png)
1. (Standard) Turn on "HDR" on your Camera, Shaders requires it.
![s18](/assets/images/Screenshot_18.png)
1. (All) This VFX Asset looks much better in "Linear" Color Space, but if you using "Gamma" Color Space, you need to slightly decrease the Final Power (Emission Power) material parameter of each effect. You can check it in the "Edit > Project Settings > Player" TAB.
1. (All) Image Effects are necessary in order to make a great looking game, as well as our asset. Be sure to use "ACES Tone Mapping" and "Bloom".
1. (All) Your camera must render Depth texture in order for some effects to appear correctly.



### How to use

1. First of all, check two scenes "DemoScene_MainEffects", and "DemoScene_SeparateEffects" in the Scenes folder. First one contains complete effects, you can spawn it with right click. Second one containts additional effects, some environment design meshes, and example particle systems.
1. Drag and Drop prefabs from the "CompleteEffects" folder into your scene and they will automatically play on awake. You can just instantiate these prefabs in your scripts, or create an object pool system, enabling and disabling array of effects.
1. Most of the effects are driven by Particle Systems utilizing ([Custom Vertex Streams](https://docs.unity3d.com/Manual/PartSysVertexStreams.html)). You can freely scale the whole effect, it will preserve the proportions. Only one single parameter needed to be adjust, it is "Soft Particles Distance" in materials with a "DissolveParticleAdvances" shader.
![s20](/assets/images/Screenshot_20.png)
1. Some prefabs are driven by standard animation system in Unity, you can freely customize these animations.



### Basic adjustments and customization

1. You can scale, rotate and transform the prefab like you normally do.
1. When you scale the effect, you might also need to adjust the noise scale inside Material settings.
1. Most of the adjustments come from Material parameters.
1. Materials have a lot of settings, just play with them and create your own unique look. Be aware, that in a play mode, some materials will be converted into instances because their values are changing by the Animator component. So if you change material settings in a play mode, the original material won't be affected. This is a great way to just test all the settings.
1. Most of the parameters are described in a "02.MaterialParameters.txt" file.
1. Inside Portal prefabs, there are some disabled effects, this was made for easier customization. You can freely enable or disable them in order to create a unique look.



### Support email: sinevfx@gmail.com
