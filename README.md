<img src="./dalle2.png" width="450px"></img>

## DALL-E 2 - Pytorch (wip)

Implementation of <a href="https://openai.com/dall-e-2/">DALL-E 2</a>, OpenAI's updated text-to-image synthesis neural network, in Pytorch. <a href="https://youtu.be/RJwPN4qNi_Y?t=555">Yannic Kilcher summary</a>

The main novelty seems to be an extra layer of indirection with the prior network (whether it is an autoregressive transformer or a diffusion network), which predicts an image embedding based on the text embedding from CLIP. Specifically, this repository will only build out the diffusion prior network, as it is the best performing variant (but which incidentally involves a causal transformer as the denoising network 😂)

This model is SOTA for text-to-image for now.

It may also explore an extension of using <a href="https://huggingface.co/spaces/multimodalart/latentdiffusion">latent diffusion</a> in the decoder from Rombach et al.

Please join <a href="https://discord.gg/xBPBXfcFHd"><img alt="Join us on Discord" src="https://img.shields.io/discord/823813159592001537?color=5865F2&logo=discord&logoColor=white"></a> if you are interested in helping out with the replication

Do let me know if anyone is interested in a Jax version https://github.com/lucidrains/DALLE2-pytorch/discussions/8

## Citations

```bibtex
@misc{ramesh2022,
    title   = {Hierarchical Text-Conditional Image Generation with CLIP Latents}, 
    author  = {Aditya Ramesh et al},
    year    = {2022}
}
```

```bibtex
@misc{crowson2022,
    author  = {Katherine Crowson},
    url     = {https://twitter.com/rivershavewings}
}
```

```bibtex
@misc{rombach2021highresolution,
    title   = {High-Resolution Image Synthesis with Latent Diffusion Models}, 
    author  = {Robin Rombach and Andreas Blattmann and Dominik Lorenz and Patrick Esser and Björn Ommer},
    year    = {2021},
    eprint  = {2112.10752},
    archivePrefix = {arXiv},
    primaryClass = {cs.CV}
}
```
