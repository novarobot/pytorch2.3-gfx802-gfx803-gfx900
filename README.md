# PyTorch 2.3 for AMD gfx802 / gfx803 / gfx900 on ROCm 5.7.3 (Python 3.11)

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
> ⚠️ These are the exact commands. If `wget` from the `blob` URL doesn’t fetch the wheel, use the *raw* link variant shown in the comment.

```bash
# Remove any previous torch (if present)
sudo pip uninstall -y torch --break-system-packages

# Download the wheel from this repo (GitHub may redirect HTML if using 'blob'):
wget "https://github.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900/blob/main/torch-2.3.0a0%2Bgit63d5e92-cp311-cp311-linux_x86_64.whl"
# (If needed, use the raw link instead:)
# wget -O torch-2.3.0a0+git63d5e92-cp311-cp311-linux_x86_64.whl #   "https://raw.githubusercontent.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900/refs/heads/main/torch-2.3.0a0%2Bgit63d5e92-cp311-cp311-linux_x86_64.whl"

# Install
sudo pip install --break-system-packages ./torch-2.3.0a0+git63d5e92-cp311-cp311-linux_x86_64.whl
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

# PyTorch 2.3 AMD gfx802 / gfx803 / gfx900 ROCm 5.7.3-hoz (Python 3.11) — Magyar

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
> ⚠️ Ezek **pontosan** azok a parancsok, amiket kértél. Ha a `blob` URL-ről a `wget` HTML-t tölt le, használd a lenti *raw* linkes megjegyzést.

```bash
# Korábbi torch eltávolítása (ha volt)
sudo pip uninstall -y torch --break-system-packages

# Wheel letöltése a repóból (a 'blob' URL néha HTML-t ad vissza):
wget "https://github.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900/blob/main/torch-2.3.0a0%2Bgit63d5e92-cp311-cp311-linux_x86_64.whl"
# (Szükség esetén használd a raw linket:)
# wget -O torch-2.3.0a0+git63d5e92-cp311-cp311-linux_x86_64.whl #   "https://raw.githubusercontent.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900/refs/heads/main/torch-2.3.0a0%2Bgit63d5e92-cp311-cp311-linux_x86_64.whl"

# Telepítés
sudo pip install --break-system-packages ./torch-2.3.0a0+git63d5e92-cp311-cp311-linux_x86_64.whl
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

---

## How to upload this README via GitHub Web UI

1. Open your repo in the browser: **https://github.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900**
2. Click **Add file** → **Create new file**.
3. Enter the filename: **README.md**.
4. Paste the entire content of this file.
5. At the bottom, add a commit message (e.g., *Add README*), keep branch as **main**, then click **Commit changes**.

### Alternately (upload from Web if you already have the file)
1. Click **Add file** → **Upload files**.
2. Drag-and-drop **README.md** here, or use **choose your files**.
3. Commit to **main**.

---

## Hogyan töltsd fel ezt a README-t a GitHub Web UI-n (magyar)

1. Nyisd meg a repót böngészőben: **https://github.com/novarobot/pytorch2.3-gfx802-gfx803-gfx900**
2. **Add file** → **Create new file**.
3. Fájlnév: **README.md**.
4. Illeszd be a teljes tartalmat.
5. Alul írj egy commit üzenetet (pl. *Add README*), a branch maradjon **main**, majd **Commit changes**.

### Alternatíva (ha a fájl már megvan nálad)
1. **Add file** → **Upload files**.
2. Húzd be a **README.md** fájlt (vagy válaszd ki).
3. Commitold a **main** branchre.
