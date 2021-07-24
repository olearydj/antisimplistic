---
toc: false
layout: post
description: "Early access fun with the MetaHuman Creator, a free-to-use web-based tool for creating high-fidelity digital humans, by Epic Games."
categories: [Real-Time Graphics]
title: "Digital Twins of Another Kind"
image: images/mhc-thumb.png
comments: true
---
I was finally able to make some time to join the early access program for Epic Games' amazing new offering, [MetaHuman Creator (MHC)](https://www.unrealengine.com/en-US/metahuman-creator). First previewed at [the 2018 Game Developer Conference](https://www.unrealengine.com/en-US/blog/epic-games-and-3lateral-introduce-digital-andy-serkis), MHC is based on world-leading character creation technology developed by the Serbian company [3Lateral](https://www.3lateral.com/) combined with state-of-the-art computer vision and animation technology from England's [Cubic Motion](https://cubicmotion.com/). Both companies have since been acquired by Epic.

<img src="{{ site.baseurl }}/images/mhc-header-1.png" alt="MetaHuman Line-Up" width="900"/>

Remarkably, the result of this collaboration is both **free** and **web-based**. It was announced in February of this year with this jaw-dropping trailer:

<p align="center">
<iframe width="730" height="432" src="https://www.youtube.com/embed/1tjkSpoa7V8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</p>

After spending a few hours with MetaHuman Creator, I agree with Epic on its unique selling points:

- Simple, responsive controls make it **Easy and Fun** to use, and encourage experimentation. It is easy to make a character in 10 minutes, but fun and rewarding enough to spend hours with.
- Nearly infinite choices allow for the creation of **Hugely Variable** characters, as demonstrated by the images in this post, which vary widely in age, gender, skin tone, etc.
- Real-world scan data and appropriately constrained adjustments are designed to easily produce diverse, **Physically Plausible** results.
- The output is **Real-Time Ready**, including everything Unreal needs to build performant apps for a range of hardware: meshes, full facial and body rig, animation controls, materials, and LODs.

<img src="{{ site.baseurl }}/images/mhc-header-2.png" alt="MetaHuman Line-Up" width="900"/>

MHC uses an innovative approach to character modeling that prioritizes quick, amazing results over complete artistic control. It combines parametric controls for blending features from the given base models and adjusting attributes like freckle density, with modeling tools that allow the user to alter the resulting mesh. The latter fall short of sculpting (the term used in MHC) in that you cannot create new geometric features, only adjust what is present in your blended model.

While new characters can be brought to life at the speed of your imagination, the tradeoff described above makes replicating the look of a real person a bit more challenging. The skin around your eyes, for example, is very complex and nuanced. Trying to duplicate a specific example in the wide range of human eye types is difficult in MHC, which only gives you tools for adjusting the location, size, and overall shape of the eye, along with some control over the relative position of the lids. To some extent this can be overcome by blending features from carefully selected base models.

Despite MHC's constraints and my lack of artistry, I was able to get [better-than-Polar-Express results](http://laurawilkens.com/thoughts/2015/12/14/lets-talk-about-the-polar-express) in no time.

<p align="center">
<b><font size="+1">My Non-Identical Digital Twin, Don</font></b>
<iframe width="730" height="432" src="https://www.youtube.com/embed/Y75QqZYjpCY?start=50" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</p>

To experience all of this in your favorite web browser is downright magical. MHC overcomes the limitations of its web-based delivery through the magic of  [Pixel Streaming](https://docs.unrealengine.com/4.26/en-US/SharingAndReleasing/PixelStreaming/). All the heavy lifting is done in an Unreal application running on a remote server, where the GPU-rendered scene is encoded as a browswer-friendly media stream. This approach eliminates most hardware and software requirements, and ensures that all users have a similarly amazing experience.

MetaHuman Creator is still an "early access" preview of what's to come. It would benefit from a greater variety of hair styles, clothing, and body types, as well as continued development of the parametric controls and modeling tools. Even with the current "limits" it is a remarkably capable tool, and an exciting glimpse into the bright future of real-time graphics. For quickly creating a very diverse range of fantastic looking human characters that are real-time ready, it is hard to imagine a better debut. Yet I'm sure that Epic's world-class team is just getting started, and I look forward to being equally inspired and awe-struck by future releases.

<img src="{{ site.baseurl }}/images/mhc-header-3.png" alt="MetaHuman Line-Up" width="900"/>
