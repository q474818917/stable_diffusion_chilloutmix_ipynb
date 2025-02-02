# AUTOMATIC1111 Stable Diffusion WebUI 1.5 + ChilloutMix + Kohya's Scripts

[[Web UI] Go To Colab](https://colab.research.google.com/github/wibus-wee/stable_diffusion_chilloutmix_ipynb/blob/main/stable_diffusion_1_5_webui.ipynb) | [[LoRA Train] Go To Colab](https://colab.research.google.com/github/wibus-wee/stable_diffusion_chilloutmix_ipynb/blob/main/lora_train.ipynb) | [[Xformers Build] Go To Colab](https://colab.research.google.com/github/wibus-wee/stable_diffusion_chilloutmix_ipynb/blob/main/xformers_build.ipynb) | [Prompts Collection](/prompts.md)

It does not come with any Loras, you need to type in **CivitAI** to download it yourself, and upload it to the `models/Stable-diffusion` folder. If you enable CiivitAIExtension, you can download it directly from the web UI, but remember to check Save add Additional Network option.

> **Warning**: Please note that there may be legal risks before painting. Please note whether your painting may cause controversy and negative impact on the development of the AI community. Please use it with caution.


## Roadmap

- [x] Paperspace Support
- [x] Support for training LoRA Jupyter Notebook
- [x] Optimize model download speed with aria2
- [x] Internationalization
- [x] Provide xformer support for Paperspace M4000 GPU

Jupyter Notebook's Language is still Chinese, I want to find a way to make it internationalized, but maintaining two versions is a bit troublesome, so I will do it later.

## About Training LoRA

Basic training script based on [Akegarasu/lora-scripts](https://github.com/Akegarasu/lora-scripts) which is based on [kohya-ss/sd-scripts](https://github.com/kohya-ss/sd-scripts), but you can also use [ddPn08/kohya-sd-scripts-webui](https://github.com/ddPn08/kohya-sd-scripts-webui) which provides a GUI, it is more convenient, I also provide the corresponding SD WebUI extension installation method in `stable_diffusion_1_5_webui.ipynb`.

Some models are not compatible with the training script, and the training script will not be able to train them. If you want to train them, you need to use the training script provided by the model author.

> In [kohya-ss/sd-scripts train_network documentaion](https://github.com/kohya-ss/sd-scripts/blob/main/train_network_README-ja.md), it notes that the cloneofsimo's repository and the d8ahazard's Dreambooth Extension for Stable-Diffusion-WebUI are not compatible at the current time. This is because they have extended some features.

## Recommended Loras

- `(x1)` 🌟 St. Louis (Luxurious Wheels) (Azur Lane): https://civitai.com/models/6669/st-louis-luxurious-wheels-azur-lane
- `(x1)` 👍 Girls' Frontline-OTs-14"lightning": https://civitai.com/models/6525/girls-frontline-ots-14lightning
- `(x0.5)` 🌟 @kbr/Korean Doll Likeness: https://civitai.com/models/7448/korean-doll-likeness
- `(x0.5)` 🆒 @kbr/Japanese Doll Likeness: https://civitai.com/models/10135
- `(x0.5)` 🆒 @kbr/Taiwan Doll Likeness  : https://civitai.com/models/7716/taiwan-doll-likeness
- `(x0.5)` 🆒 Yae Miko | Realistic Genshin (Mixed): https://civitai.com/models/8484/yae-miko-or-realistic-genshin
- `(x0.5)` 👍 Gakki | Aragaki Yui | 新垣結衣: https://civitai.com/models/8416/gakki-or-aragaki-yui-or

## Recommended Checkpoints

- [2.5D] ChilloutMix: https://civitai.com/models/6424/chilloutmix
- [2.5D] SunshineMix: https://civitai.com/models/9291/sunshinemix
- [2D] Grapefruit (hentai model): https://civitai.com/models/2583/grapefruit-hentai-model

## Recommended Textual Inversion

- Ulzzang-6500 (Korean doll aesthetic): https://civitai.com/models/8109/ulzzang-6500-korean-doll-aesthetic
- Pure Eros Face: https://civitai.com/models/4514/pure-eros-face

## Recommended Experimental LoRA

Experimental LoRA refers to models that are not yet fully tested by me, and have not yet been determined to be compatible. If you want to use these models, please judge the compatibility with other LoRA by yourself.

- liuyifei: https://civitai.com/models/8453/liuyifei
- Lisa Blackpink: https://civitai.com/models/8605/lisa-blackpink
- Jisoo Blackpink: https://civitai.com/models/8311/jisoo-blackpink
- Rosè Blackpink: https://civitai.com/models/8600/rose-blackpink
- ChilloutMixss: https://civitai.com/models/10850/chilloutmixss

## NoteBook Built-in Extension

WebUI Jupyter Notebook built-in Extension, you can install it directly from the notebook.

- [deforum-art/deforum-for-automatic1111-webui](https://github.com/deforum-art/deforum-for-automatic1111-webui)
- [AlUlkesh/stable-diffusion-webui-images-browser](https://github.com/Akegarasu/stable-diffusion-webui-images-browser)
- [camenduru/stable-diffusion-webui-huggingface](https://github.com/camenduru/stable-diffusion-webui-huggingface)
- [camenduru/sd-civitai-browser](https://github.com/camenduru/sd-civitai-browser)
- [camenduru/openpose-editor](https://github.com/camenduru/openpose-editor)
- [Mikubill/sd-webui-controlnet](https://github.com/Mikubill/sd-webui-controlnet)
- [kohya-ss/sd-webui-additional-networks](https://github.com/kohya-ss/sd-webui-additional-networks)
- [ddpn08/kohya-sd-scripts-webui](https://github.com/ddpn08/kohya-sd-scripts-webui) *(This extension has better install before WebUI Starting, otherwise you need to restart Application instead of just reload the UI.)*
- [d8ahazard/sd_dreambooth_extension](https://github.com/d8ahazard/sd_dreambooth_extension)

## Build xformers from source

If you are using Google Colab, there are many precompiled wheels for you to choose from. If you are using something else or want to build from source, you can use this notebook to build the library.

I have written a [notebook](./xformers_build.ipynb) to build xformers from source. You can use it to build xformers for your own GPU.

## CHANGELOG

### 2023.2.25

- **README.md**
  - Update Experimental Lora List - Add `ChilloutMixss`
  - Optimize CHANGELOG format
  - Internationalize README
  - New "Textual Inversion" section
  - Add "NoteBook Built-in Extension" section
  - Add "Build xformers from source" section
- **lora_train.ipynb**
  - Fix serious errors in LoRA training script
  - Remove unnecessary platform and GPU checks
  - Add `export_model_dir` option to specify the directory where the model is exported
  - Add an extra build installation xformers option for the M4000 GPU
  - Use `ninja` to build xformers much faster ( Followed by Official README)
- **stable_diffusion_1_5_webui.ipynb**
  - Add an extra build installation xFormer option for the M4000 GPU
  - Use `ninja` to build xformers much faster ( Followed by Official README)
- **prompts.md**
  - Internationalize
- **xformers_build.ipynb**
  - New xformers build script
  - Switch xformers source version to 0.0.16
- **workflows**
  - Add `xformers_build.ipynb` to Preview CI
  - Remove `pull_request_target` value to prevent the workflow from running twice
- **Release**
  - Publish xformers precompiled wheels for M4000 GPU

### 2023.2.24

- **workflows**
  - Automatically comment on Preview link when Pull Request ( https://github.com/wibus-wee/stable_diffusion_chilloutmix_ipynb/pull/2 )
- **stable_diffusion_1_5_webui.ipynb**
  - Install controlnet, openpose-editor, Kohya sd-scripts extension with Stable-Diffusion-WebUI
  - Remove the old training model installation scheme and merge it into the installation steps ( created in 2023.2.19 )
- **lora_train.ipynb**
  - New Lora Train Script ( Alpha )

### 2023.2.21

- **stable_diffusion_1_5_webui.ipynb**
  - Better option selection mechanism
  - Fine distinction between Paperspace and Colab platforms rather than relying on a single Free GPU model

### 2023.2.19

- **stable_diffusion_1_5_webui.ipynb**
  - Fix the problem of incorrectly identifying the Quadro M4000 GPU
  - Add **Training Model** Installation Scheme ( Power by [d8ahazard/sd_dreambooth_extension](https://github.com/d8ahazard/sd_dreambooth_extension))
  - Optimize checkpoint selection
  - Fix the problem of not being able to read variables
  - Automatically check whether webUI and training extensions are installed

### 2023.2.18

- **stable_diffusion_1_5_webui.ipynb**
  - Update the latest version of the upstream ChilloutMix
  - Update Prompts Collection
  - Compatible with Paperspace platform (Free GPU)
  - Export all generated images
  - Use `nvidia-smi` to view GPU information
  - Check if GPU supports Xformers
  - Optimize variable passing

### 2023.2.17

- **stable_diffusion_1_5_webui.ipynb**
  - Add SunshineMix Checkpoint as a second choice for 2.5D painting

### 2023.2.16
- **stable_diffusion_1_5_webui.ipynb**
  - Because there may be a sudden exit in the middle, there is another way to restart

---

> Created by [@wibus-wee](https://github.com/wibus-wee)
>
> Reference: [camenduru/stable-diffusion-webui-colab](https://github.com/camenduru/stable-diffusion-webui-colab)
