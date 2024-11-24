# ComfyUI-MultiGPU


### Allows distributing ComfyUI VRAM requirements across multiple GPUs

This extension adds new nodes for model loading that allow you to specify the GPU to use for each model.
This allows loading larger models across multiple GPUs, but does not allow for splitting a single model across multiple GPUs.
For example, you can load the main diffusion model on GPU 0 and the clip and VAE on GPU 1.

This functionality does not necessarily speed up image generation, it simply allows you to run a larger model than you could on a single GPU.

## Installation

Clone this repository inside `ComfyUI/custom_nodes/`.

## Nodes

The extension adds new loader nodes corresponding to the default ones. The new nodes have the same functionality but add a new `device` parameter that allows you to specify the GPU to use.

- `CLIPLoaderMultiGPU`
- `CheckpointLoaderMultiGPU`
- `ControlNetLoaderMultiGPU`
- `CLIPLoaderMultiGPU`
- `DualCLIPLoaderMultiGPU`
- `TripleCLIPLoaderMultiGPU`
- `VAELoaderMultiGPU`


## Credits

Forked from the original work of [Alexander Dzhoganov](https://github.com/AlexanderDzhoganov)
https://github.com/neuratech-ai/ComfyUI-MultiGPU

