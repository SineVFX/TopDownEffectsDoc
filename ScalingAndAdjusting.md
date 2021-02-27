---
layout: default
title: Scaling and adjusting
nav_order: 2
---

## Scaling



### Scaling

1. You can scale, rotate and transform the prefab like you normally do.
1. When you scale one of these effects (StormBeacon, SummonStorm, IonMarker, FusionCore), you might also need to adjust the "Soft Particles Distance" parameter of smoke and clouds-like materials. For example, if you scale your model by 0.01, you need to multiply this parameter byt the same amount. By default it is set to 0.2f and the result value should be 0.002f, but this depends on camera depth, sometimes you need to adjust it by eye.
![s20](/assets/images/Screenshot_20.png)
1. Most of the adjustments come from Material parameters.
1. Materials have a lot of settings, just play with them and create your own unique look. Be aware, that in a play mode, some materials will be converted into instances because their values are changing by the Animator component. So if you change material settings in a play mode, the original material won't be affected. This is a great way to just test all the settings.
1. Most of the parameters are described in a "02.MaterialParameters.txt" file.
1. Inside Portal prefabs, there are some disabled effects, this was made for easier customization. You can freely enable or disable them in order to create a unique look.

### Basic Adjustments

1. (Color)
1. (Noise)
1. (Texture Animation)

### Advanced Adjustments

1. (Vertex Stream)
1. (Vertex Stream)
1. (Vertex Stream)



### Support email: sinevfx@gmail.com
