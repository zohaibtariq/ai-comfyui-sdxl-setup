# Setup Comfy UI with Stable Diffusion XL model locally

## [Watch on YouTube](https://www.youtube.com/watch?v=dGx50S4b7_s&t=61s)

### Navigate to the folder where you want to install ComfyUI
```bash
mkdir ComfyUI
```

### Move Inside Created Directory
```bash
cd ComfyUI
```

### Clone ComfyUI repo
```bash
git clone https://github.com/comfyanonymous/ComfyUI .
```

### To install ComfyUI manager go to
```bash
cd custom_nodes
```

### Clone ComfyUI manager repo
```bash
git clone https://github.com/ltdrdata/ComfyUI-Manager
```

### Back to main Folder
```bash
cd ..
````

### Create new virtual environment
```bash
python3 -m venv ai
```

### Activate newly created virtual environment
```bash
source ai/bin/activate
```

### Update pip3
```bash
pip3 install --upgrade pip setuptools
```

### Install pytorch Nightly (Recommended) or take it from https://pytorch.org/
```bash
pip3 install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cpu
```

### Install requirements
```bash
pip3 install -r requirements.txt
```

### Download following files from these link
```bash
https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/tree/main
```

- sd_xl_base_1.0.safetensors (Size: 6.94 GB)

```bash
https://huggingface.co/stabilityai/stable-diffusion-xl-refiner-1.0/tree/main
```
- sd_xl_refiner_1.0.safetensors (Size: 6.08 GB)

```bash
https://huggingface.co/stabilityai/sdxl-vae/tree/main
```
- sdxl_vae.safetensors (Size: 335 MB)

### Move files to proper location (IMPORTANT)
- *sd_xl_base_1.0.safetensors* TO *ComfyUI/models/checkpoints*
- *sd_xl_refiner_1.0.safetensors* TO *ComfyUI/models/checkpoints*
- *sdxl_vae.safetensors* TO *ComfyUI/models/vae*

### Run ComfyUI local server follow terminal link
```bash
python3 main.py --gpu-only
```

```bash
http://127.0.0.1:8188/
```
