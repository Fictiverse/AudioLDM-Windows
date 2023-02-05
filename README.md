# Text-to-Audio Generation

[![arXiv](https://img.shields.io/badge/arXiv-2109.13731-brightgreen.svg?style=flat-square)](https://arxiv.org/abs/2301.12503)  [![githubio](https://img.shields.io/badge/GitHub.io-Audio_Samples-blue?logo=Github&style=flat-square)](https://audioldm.github.io/)  [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/haoheliu/audioldm-text-to-audio-generation)  [![Hugging Face Hub](https://img.shields.io/badge/%F0%9F%A4%97-Models%20on%20Hub-yellow)](https://huggingface.co/haoheliu/AudioLDM-S-Full)  [![Replicate](https://replicate.com/jagilley/audio-ldm/badge)](https://replicate.com/jagilley/audio-ldm)

<!-- # [![PyPI version](https://badge.fury.io/py/voicefixer.svg)](https://badge.fury.io/py/voicefixer) -->

Generate speech, sound effects, music and beyond.


## Windows installation
```shell
cd C:\Path\Of\AudioLDM
conda env create --name audioldm --file=environment.yml
conda activate audioldm
pip install -r requirements.txt
python scripts\text2sound.py
```

<hr>


## Web APP
1. Prepare running environment
```shell
conda create -n audioldm python=3.8; conda activate audioldm
pip3 install audioldm==0.0.6
git clone https://github.com/haoheliu/AudioLDM; cd AudioLDM
```
2. Start the web application (powered by Gradio)
```shell
python3 app.py
```
3. A link will be printed out. Click the link to open the browser and play.

## Commandline Usage
1. Prepare running environment
```shell
# Optional
conda create -n audioldm python=3.8; conda activate audioldm
# Install AudioLDM
pip3 install audioldm==0.0.6
```

2. text-to-audio generation
```python
# Test run
audioldm -t "A hammer is hitting a wooden surface"
```

For more options on guidance scale, batchsize, seed, etc, please run
```shell
audioldm -h
```

For the evaluation of audio generative model, please refer to [audioldm_eval](https://github.com/haoheliu/audioldm_eval).

# Web Demo

Integrated into [Hugging Face Spaces 🤗](https://huggingface.co/spaces) using [Gradio](https://github.com/gradio-app/gradio). Try out the Web Demo [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/haoheliu/audioldm-text-to-audio-generation)


# TODO

- [ ] Update the checkpoint with more training steps.
- [ ] Add AudioCaps finetuned AudioLDM-S model
- [x] Build pip installable package for commandline use
- [x] Build Gradio web application
- [ ] Add text-guided style transfer
- [ ] Add audio super-resolution
- [ ] Add audio inpainting

## Cite this work

If you found this tool useful, please consider citing
```bibtex
@article{liu2023audioldm,
  title={AudioLDM: Text-to-Audio Generation with Latent Diffusion Models},
  author={Liu, Haohe and Chen, Zehua and Yuan, Yi and Mei, Xinhao and Liu, Xubo and Mandic, Danilo and Wang, Wenwu and Plumbley, Mark D},
  journal={arXiv preprint arXiv:2301.12503},
  year={2023}
}
```

# Hardware requirement
- GPU with 8GB of dedicated VRAM
- A system with a 64-bit operating system (Windows 7, 8.1 or 10, Ubuntu 16.04 or later, or macOS 10.13 or later) 16GB or more of system RAM

## Reference
Part of the code is borrowed from the following repos. We would like to thank the authors of these repos for their contribution. 

> https://github.com/LAION-AI/CLAP

> https://github.com/CompVis/stable-diffusion

> https://github.com/v-iashin/SpecVQGAN 

> https://github.com/toshas/torch-fidelity


We build the model with data from AudioSet, Freesound and BBC Sound Effect library. We share this demo based on the UK copyright exception of data for academic research. 

<!-- This code repo is strictly for research demo purpose only. For commercial use please contact us. -->
