# ai-art-101
A series of 101-level articles on AI Art. The main goal of the articles is for a reader who follows the lesson exercises to be able to generate nearly anything by the end of the course, using only relatively simple tools. Even if you are a more advanced user, you should consider skimming through this course to survey the basic techniques, as you may have missed a technique and learning it may improve your abilities.

## Chapter Index
1. Prompting
2. Other Parameters
3. Resources
4. img2img
5. Inpainting
6. Manual Editing
7. Upscaling
8. Working on Large Works
9. Other Techniques

## Introduction
These articles are organized into thematic chapters and individual lessons. Most of the lessons are standard lessons designed to be taken one at a time in order, but some lessons are marked as "Additional" and will assume complete knowledge of the standard lessons. Therefore, the intended order is all standard lessons in order followed by the additional lessons in any order.

The focus here is on local generation using open source tools. Many of the concepts and techniques should be applicable to proprietary software and services, especially chapter 1, but such tools generally do not give sufficient control to make full use of the techniques described in this course.

The course (written in 2026) is designed to be moderately future proof and should be largely applicable to any future models that use the diffusion paradigm. Illustrious and Z-Image are used for the examples and some additional content specific to these models will be included.
* Illustrious is, as of writing in Feb 2026, the best model for anime or cartoon generation due mostly to broad community support (though also thanks to some excellent decisions by the Illustrious team during training, most notably the use of higher 1536x1536 resolution for Illustrious v1.0).
    * NoobAI eps is highly compatible with Illustrious so the use of these models should be essentially identical. NoobAI vpred is incompatible but is still similar as long as the NoobAI vpred resources
    * Note that Illustrious v2.0 and later are largely incompatible with v0.1, v1.0, and v1.1. The community settled on the earlier models, so that's what I'll be using. You should also avoid v0.1 whenever possible due to its poor performance at higher resolutions.
* Z-Image has a bright future in this space because it uses more recent architecture and techniques, and is deliberately designed to be accessible to artists and trainers in the local generation space. I expect the number of trained resources to grow dramatically as 2026 progresses.
    * I will generally use Z-Image Base for reasons that will become obvious as you complete the lessons, but Z-Image Turbo is a useful tool and is much faster.
    * While models like Qwen Image have superior scale, their enormous size makes them less accessible, especially to model trainers.
    * Z-Image performs well for more realistic/photographic subjects and is superior to older systems of comparable scale such as vanilla SDXL.

## Requirements
* You need hardware to generate locally, or to use a cloud GPU renting service that can run the same software as local generation.
* You will need to set up at least one of [forge](https://github.com/lllyasviel/stable-diffusion-webui-forge), [reForge](https://github.com/Panchovix/stable-diffusion-webui-reForge), or [ComfyUI](https://github.com/Comfy-Org/ComfyUI). I recommend [Stability Matrix](https://lykos.ai/) for a non-technical turn-key solution.
    * If you are more technical-minded I would recommend setting these tools up manually instead
    * You may use an alternative tool, but will need to adapt the lessons to your tool
    * The lessons will include examples and workflows for both reForge and ComfyUI
* You will need child-level drawing skills
* You will need basic image editing skills like selecting regions in an image and copy-pasting image content
    * I recommend and will be using [Krita](https://krita.org/en/). Remember that you can use Krita in addition to other image editing tools, though most fully featured image editors should have everything needed.
    * I won't cover basic usage of Krita as their [extensive docs](https://docs.krita.org/en/) already cover this.
    * In some cases I will provide an [ImageMagick](https://imagemagick.org/) command line solution in addition to the manual Krita approach. This is simply a convenience for advanced users.
