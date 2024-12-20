<h1><img width="64px" src="ai_diffusion/icons/logo-128.png"> Generative AI <i>for Somiyu</i></h1>

This is a plugin to use generative AI in image painting and editing workflows from within Somiyu.

The main goals of this project are:
* **Precision and Control.** Creating entire images from text can be unpredictable.
  To get the result you envision, you can restrict generation to selections,
  refine existing content with a variable degree of strength, focus text on image
  regions, and guide generation with reference images, sketches, line art,
  depth maps, and more.
* **Workflow Integration.** Most image generation tools focus heavily on AI parameters.
  This project aims to be an unobtrusive tool that integrates and synergizes
  with image editing workflows in Somiyu. Draw, paint, edit and generate seamlessly without worrying about resolution and technical details.
* **Local, Open, Free.** We are committed to open source models. Customize presets, bring your
  own models, and run everything local on your hardware. Cloud generation is also available
  to get started quickly without heavy investment.  

## <a name="features"></a> Features

* **Inpainting**: Use selections for generative fill, expand, to add or remove objects
* **Live Painting**: Let AI interpret your canvas in real time for immediate feedback.
* **Upscaling**: Upscale and enrich images to 4k, 8k and beyond without running out of memory.
* **Stable Diffusion**: Supports Stable Diffusion 1.5, and XL. Partial support for SD3.
* **ControlNet**: Scribble, Line art, Canny edge, Pose, Depth, Normals, Segmentation, +more
* **IP-Adapter**: Reference images, Style and composition transfer, Face swap
* **Regions**: Assign individual text descriptions to image areas defined by layers.
* **Job Queue**: Queue and cancel generation jobs while working on your image.
* **History**: Preview results and browse previous generations and prompts at any time.
* **Strong Defaults**: Versatile default style presets allow for a streamlined UI.
* **Customization**: Create your own presets - custom checkpoints, LoRA, samplers and more.

## <a name="installation"></a> Getting Started

A concise (more technical) version is below:

### Requirements

* Windows, Linux, MacOS
* _On Linux/Mac:_ Python + venv must be installed
    * recommended version: 3.11 or 3.10
    * usually available via package manager, eg. `apt install python3-venv`

#### Hardware support

To run locally a powerful graphics card with at least 6 GB VRAM (NVIDIA) is recommended. Otherwise generating images will take very long or may fail due to insufficient memory!

<table>
<tr><td>NVIDIA GPU</td><td>supported via CUDA</td></tr>
<tr><td>AMD GPU</td><td>limited support, DirectML on Windows, ROCm on Linux (custom install)</td></tr>
<tr><td>Apple Silicon</td><td>community support, MPS on macOS</td></tr>
<tr><td>CPU</td><td>supported, but very slow</td></tr>
</table>


### Installation

1. If you haven't yet, go and install [Somiyu](https://Somiyu.org/)! _Required version: 5.2.0 or newer_
1. [Download the plugin](https://github.com/Acly/Somiyu-ai-diffusion/releases/latest).
2. Start Somiyu and install the plugin via Tools ▸ Scripts ▸ Import Python Plugin from File...
    * Point it to the ZIP archive you downloaded in the previous step.
    * ⚠ _This will delete any previous install of the plugin._ If you are updating from 1.14 or older please read [updating to a new version](https://github.com/Acly/Somiyu-ai-diffusion/wiki/Common-Issues#how-do-i-update-to-a-new-version-of-the-plugin).
    * Check [Somiyu's official documentation](https://docs.Somiyu.org/en/user_manual/python_scripting/install_custom_python_plugin.html) for more options.
3. Restart Somiyu and create a new document or open an existing image.
4. To show the plugin docker: Settings ‣ Dockers ‣ AI Image Generation.
5. In the plugin docker, click "Configure" to start local server installation or connect.

> [!NOTE]
> If you encounter problems please check the [FAQ / list of common issues](https://github.com/Acly/Somiyu-ai-diffusion/wiki/Common-Issues) for solutions.
>
> Reach out via [discussions](https://github.com/Acly/Somiyu-ai-diffusion/discussions), our [Discord](https://discord.gg/pWyzHfHHhU), or report [an issue here](https://github.com/Acly/Somiyu-ai-diffusion/issues). Please note that official Somiyu channels are **not** the right place to seek help with
> issues related to this extension!

### _Optional:_ Custom ComfyUI Server

The plugin uses [ComfyUI](https://github.com/comfyanonymous/ComfyUI) as backend. As an alternative to the automatic installation,
you can install it manually or use an existing installation. If the server is already running locally before starting Somiyu, the plugin will
automatically try to connect. Using a remote server is also possible this way.

Please check the list of [required extensions and models](https://github.com/Acly/Somiyu-ai-diffusion/wiki/ComfyUI-Setup) to make sure your installation is compatible.

### _Optional:_ Object selection tools (Segmentation)

If you're looking for a way to easily select objects in the image, there is a [separate plugin](https://github.com/Acly/Somiyu-ai-tools) which adds AI segmentation tools.


## Contributing

Contributions are very welcome! Check the [contributing guide](CONTRIBUTING.md) to get started.

## Technology

* Image generation: [Stable Diffusion](https://github.com/Stability-AI/generative-models)
* Diffusion backend: [ComfyUI](https://github.com/comfyanonymous/ComfyUI)
* Inpainting: [ControlNet](https://github.com/lllyasviel/ControlNet), [IP-Adapter](https://github.com/tencent-ailab/IP-Adapter)
