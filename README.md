# aurarouter-cuda13

**AuraRouter High-Performance GPU Backend (CUDA 13.1)**

This package is a "sidecar" for **AuraRouter**. It contains the pre-compiled binary payload required to run local LLMs on modern NVIDIA GPUs with maximum performance.

## What's inside?
- `llama-server.exe`: Compiled with CUDA 13.1 support.
- `ggml-cuda.dll`: Optimized kernels for NVIDIA Ada (RTX 40), Blackwell (RTX 50), and Ampere (RTX 30) architectures.
- `cudart64_13.dll` & `cublas64_13.dll`: Required NVIDIA runtime libraries.

## Requirements
- **Hardware**: NVIDIA GPU (RTX 20-series or newer recommended).
- **Drivers**: NVIDIA Driver version **570.86** or higher.
- **AuraRouter**: Must be installed in the same environment.

## Usage
Simply install this package into the same virtual environment as `aurarouter`:

```bash
pip install aurarouter-cuda13
```

AuraRouter's `BinaryManager` will automatically detect this package and prioritize it over CPU-based backends. No configuration change is required.
