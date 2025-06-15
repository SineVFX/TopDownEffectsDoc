---
layout: default
title: Quick Start
nav_order: 1
---

## Quick Start

First of all, you need to unpack the right packages for your specific Unity setup. This Asset contains three packages, for **Built-in**, **HDRP**, and **URP** pipelines. Start with the **Step_1_CoreResources** package, it will add all core resources (textures, scripts, and animations) needed for this Asset. After that, pick the right SRP package and unpack it too. It will add all other components like prefabs of complete effects, scenes, materials, and shaders.

### Important Notes

* **(URP)** Make sure you enable HDR, Depth, and Opaque textures in URP Asset settings.

![s19](/assets/images/Screenshot_19.png)

* **(Built-in)** Turn on "HDR" on your Camera, Shaders require it.

![s18](/assets/images/Screenshot_18.png)

* **(All)** This VFX Asset looks much better in "Linear" Color Space, but if you are using "Gamma" Color Space, you need to slightly decrease the Final Power (Emission Power) material parameter of each effect. You can check it in the "Edit > Project Settings > Player" TAB.
* **(All)** Image Effects are necessary in order to make a great-looking game, as well as our assets. Be sure to use "ACES Tone Mapping" and "Bloom".
* **(All)** Your camera must render Depth texture in order for some effects to appear correctly.



### How To Use

* First of all, check all the demo scenes "DemoScene_MainEffects", "DemoScene_MainEffects_v2", "DemoScene_SeparateEffects", "DemoScene_SeparateEffects_v2", and "DemoScene_GridEffects_v2" in the Scenes folder. The Main Effects scene contains complete effects. You can spawn it with a right-click. The second one contains additional effects, some environment design meshes, and example particle systems.
* Drag and Drop prefabs from the "CompleteEffects" folder into your scene, and they will automatically play on awake. You can just instantiate these prefabs in your scripts, or create an object pool system, enabling and disabling an array of effects.
* Most of the effects are driven by Particle Systems utilizing ([Custom Vertex Streams](https://docs.unity3d.com/Manual/PartSysVertexStreams.html)). You can freely scale the whole effect, it will preserve the proportions. Only one single parameter needed to be adjusted, it is "Soft Particles Distance" in materials with a "DissolveParticleAdvances" shader.

Changes in version 2.0 {: .label .label-yellow }
* **In version 2.0**, there are some effects that are not 100% scaled automatically. These effects will have the "AutoScaleMaster" script attached to a prefab. This script will handle the scaling process adjustments after you scale the entire prefab. If you want to scale prefab in the editor and it will not be scaled during gameplay, you can click the button "Auto Adjust Scaling and Rate", and it will work properly.
* **In version 2.0**, you now have the tools to adjust the emission power of multiple materials. Check the Tools/SineVFX/MaterialFinalPowerBatchEditor dropdown.
* **In version 2.0**, you have new DemoScene_GridEffects_v2. These effects use a modified shader intended for use in mesh material slots.

![s20](/assets/images/Screenshot_20.png)

* Some prefabs are driven by a standard animation system in Unity, and you can freely customize these animations.



### Support email: sinevfx@gmail.com
