# PyTorch 2.3 (2.3.1) for AMD gfx802 / gfx803 / gfx900 on ROCm 5.7.3 (Python 3.11)

Prebuilt **torch 2.3** wheel for AMD GPUs:
- **gfx802** — *AMD FirePro S7150 x2* (16 GB total = 2×8 GB)
- **gfx803** — *AMD Radeon RX 580* (8 GB)
- **gfx900** — *AMD Radeon RX Vega 64* (8 GB)

**Tested OS:** Debian 12  
**Python:** 3.11  
**ROCm:** 5.7.3

## Prerequisites
- Working **ROCm 5.7.3** stack for the GPUs above  
- Properly configured **OpenCL**, **HIP**, and **Vulkan** environments  
- A functioning **C/C++ toolchain** (*for OpenCL / HIP / Vulkan targets*)

## Install (system Python 3.11 on Debian 12)

```bash
# Remove any previous torch (if present)
sudo pip uninstall -y torch --break-system-packages

# Clone repo 
git clone https://github.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900
cd pytorch2.3-gfx802-gfx803-gfx900/

# Install
sudo pip install --break-system-packages ./torch-2.3.1+git63d5e92-cp311-cp311-linux_x86_64.whl
```

## Quick check
```bash
python3 - << 'PY'
import torch
print("torch:", torch.__version__)
print("cuda available:", torch.cuda.is_available())
print("hip available:", hasattr(torch.version, "hip") and torch.version.hip is not None)
PY
```

---

# PyTorch 2.3 (2.3.1) AMD gfx802 / gfx803 / gfx900 ROCm 5.7.3-hoz (Python 3.11) — Magyar

Előre fordított **torch 2.3** wheel AMD GPU-khoz:
- **gfx802** — *AMD FirePro S7150 x2* (összesen 16 GB = 2×8 GB)
- **gfx803** — *AMD Radeon RX 580* (8 GB)
- **gfx900** — *AMD Radeon RX Vega 64* (8 GB)

**Tesztelt rendszer:** Debian 12  
**Python:** 3.11  
**ROCm:** 5.7.3

## Előfeltételek
- Működő **ROCm 5.7.3** a fenti kártyákhoz  
- Helyesen konfigurált **OpenCL**, **HIP** és **Vulkan** környezet  
- Működő **C/C++ fordítóeszköz-lánc** (*OpenCL / HIP / Vulkan célokra*)

## Telepítés (rendszer Python 3.11 Debian 12-n)

```bash
# Korábbi torch eltávolítása (ha volt)
sudo pip uninstall -y torch --break-system-packages

# Repó letöltése:
git clone https://github.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900
cd pytorch2.3-gfx802-gfx803-gfx900/

# Telepítés
sudo pip install --break-system-packages ./torch-2.3.1+git63d5e92-cp311-cp311-linux_x86_64.whl
```

## Gyors ellenőrzés
```bash
python3 - << 'PY'
import torch
print("torch:", torch.__version__)
print("cuda elérhető:", torch.cuda.is_available())
print("hip elérhető:", hasattr(torch.version, "hip") and torch.version.hip is not None)
PY
```
