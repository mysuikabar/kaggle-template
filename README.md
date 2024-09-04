# Kaggle Environment Template

## Setup
GPU + Kaggle Docker Environment

1. Create a GPU instance on GCP
2. Install Docker if it's not already installed
3. Install GPU drivers and CUDA toolkit
   - Confirm GPU is recognized using `nvidia-smi`
   - https://cloud.google.com/compute/docs/gpus/install-drivers-gpu?hl=en#install-script
4. Install NVIDIA Container Toolkit
   - https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#
5. Restart Docker
```bash
sudo systemctl restart docker
```
6. Attach to devcontainer
   - Confirm GPU is accessible from within the container
```python
import torch
torch.cuda.is_available()
```