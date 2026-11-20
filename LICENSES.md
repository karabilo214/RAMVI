# Лицензии / Licenses

RAMVI распространяется по лицензии MIT. В комплект входят сторонние компоненты, у каждого свои условия. Все тексты лежат в папке [`licenses/`](licenses/) — и в этом репозитории, и внутри архива релиза.

RAMVI is MIT-licensed. The release bundle contains third-party components under their own terms; all texts are in [`licenses/`](licenses/) here and inside the release archive.

## RAMVI

| Компонент | Лицензия | Текст |
|---|---|---|
| RAMVI | MIT | [LICENSE](LICENSE) |

## Двоичные компоненты NVIDIA и Microsoft / NVIDIA and Microsoft binaries

Условия для пользователя (на что распространяются, что запрещено): [THIRD_PARTY_TERMS.txt](licenses/THIRD_PARTY_TERMS.txt). Сводка всех компонентов: [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).

| Компонент | Условия | Где |
|---|---|---|
| NVIDIA CUDA 13.2 (cuBLAS, cuFFT, cuSPARSE, cuSOLVER, cuRAND, NVRTC, nvJitLink, CUPTI, NVTX, libdevice) | [CUDA Toolkit EULA v13.2, приложение A](https://docs.nvidia.com/cuda/archive/13.2.0/eula/index.html) | `runtime/python/Lib/site-packages/torch/lib`, `triton/backends/nvidia` |
| NVIDIA cuDNN 9 | [NVIDIA SDK License + cuDNN Supplement (v. 22.02.2022)](https://docs.nvidia.com/deeplearning/cudnn/latest/reference/eula.html) | `torch/lib/cudnn64_9.dll` |
| Microsoft Visual C++ Runtime 14.44 | [Visual Studio license, Distributable Code](https://visualstudio.microsoft.com/license-terms/) | `runtime/python/*.dll` |
| Python 3.12.10 (embeddable) | PSF-2.0 | [LICENSE.txt](licenses/python/LICENSE.txt) |

## Пакеты Python / Python packages

| Пакет | Лицензия | Тексты |
|---|---|---|
| annotated-doc-0.0.5 | MIT | [LICENSE](licenses/python-packages/annotated-doc-0.0.5/LICENSE) |
| annotated-types-0.8.0 | MIT | [LICENSE](licenses/python-packages/annotated-types-0.8.0/LICENSE) |
| anyio-4.16.0 | MIT | [LICENSE](licenses/python-packages/anyio-4.16.0/LICENSE) |
| apache-tvm-ffi-0.1.16 | Apache 2.0 | [LICENSE](licenses/python-packages/apache-tvm-ffi-0.1.16/LICENSE), [NOTICE](licenses/python-packages/apache-tvm-ffi-0.1.16/NOTICE), [libbacktrace-LICENSE](licenses/python-packages/apache-tvm-ffi-0.1.16/libbacktrace-LICENSE) |
| attrs-26.1.0 | MIT | [LICENSE](licenses/python-packages/attrs-26.1.0/LICENSE) |
| certifi-2026.10.23 | MPL-2.0 | [LICENSE](licenses/python-packages/certifi-2026.10.23/LICENSE) |
| cffi-2.1.1 | MIT-0 | [LICENSE](licenses/python-packages/cffi-2.1.1/LICENSE) |
| charset-normalizer-3.5.2 | MIT | [LICENSE](licenses/python-packages/charset-normalizer-3.5.2/LICENSE) |
| click-8.5.0 | BSD-3-Clause | [LICENSE.txt](licenses/python-packages/click-8.5.0/LICENSE.txt) |
| colorama-0.4.6 | BSD License | [LICENSE.txt](licenses/python-packages/colorama-0.4.6/LICENSE.txt) |
| filelock-4.2.4 | MIT | [LICENSE](licenses/python-packages/filelock-4.2.4/LICENSE) |
| flatbuffers-25.12.19 | Apache-2.0 | [LICENSE-Apache-2.0.txt](licenses/python-packages/flatbuffers-25.12.19/LICENSE-Apache-2.0.txt) |
| fsspec-2026.9.0 | BSD-3-Clause | [LICENSE](licenses/python-packages/fsspec-2026.9.0/LICENSE) |
| h11-0.16.0 | MIT | [LICENSE.txt](licenses/python-packages/h11-0.16.0/LICENSE.txt) |
| hf-xet-1.8.0 | Apache-2.0 | [LICENSE](licenses/python-packages/hf-xet-1.8.0/LICENSE) |
| httpcore2-2.16.0 | BSD-3-Clause | [LICENSE.md](licenses/python-packages/httpcore2-2.16.0/LICENSE.md) |
| httpx2-2.16.0 | BSD-3-Clause | [LICENSE.md](licenses/python-packages/httpx2-2.16.0/LICENSE.md) |
| huggingface_hub-2.4.0 | Apache-2.0 | [LICENSE](licenses/python-packages/huggingface_hub-2.4.0/LICENSE) |
| idna-3.20 | BSD-3-Clause | [LICENSE.md](licenses/python-packages/idna-3.20/LICENSE.md) |
| Jinja2-3.1.6 | BSD License | [LICENSE.txt](licenses/python-packages/Jinja2-3.1.6/LICENSE.txt) |
| jsonschema-4.26.0 | MIT | [COPYING](licenses/python-packages/jsonschema-4.26.0/COPYING) |
| jsonschema-specifications-2025.9.1 | MIT | [COPYING](licenses/python-packages/jsonschema-specifications-2025.9.1/COPYING) |
| llvmlite-0.50.0 | BSD-2-Clause AND Apache-2.0 WITH LLVM-exception | [LICENSE](licenses/python-packages/llvmlite-0.50.0/LICENSE), [LICENSE.thirdparty](licenses/python-packages/llvmlite-0.50.0/LICENSE.thirdparty) |
| markdown-it-py-4.2.0 | MIT License | [LICENSE](licenses/python-packages/markdown-it-py-4.2.0/LICENSE), [LICENSE.markdown-it](licenses/python-packages/markdown-it-py-4.2.0/LICENSE.markdown-it) |
| MarkupSafe-3.0.3 | BSD-3-Clause | [LICENSE.txt](licenses/python-packages/MarkupSafe-3.0.3/LICENSE.txt) |
| mdurl-0.1.2 | MIT License | [LICENSE](licenses/python-packages/mdurl-0.1.2/LICENSE) |
| mpmath-1.3.0 | BSD | [LICENSE](licenses/python-packages/mpmath-1.3.0/LICENSE) |
| networkx-3.7 | BSD-3-Clause | [LICENSE.txt](licenses/python-packages/networkx-3.7/LICENSE.txt) |
| numba-0.68.1 | BSD | [LICENSE](licenses/python-packages/numba-0.68.1/LICENSE), [LICENSES.third-party](licenses/python-packages/numba-0.68.1/LICENSES.third-party) |
| numpy-2.5.4 | BSD-3-Clause AND 0BSD AND MIT AND Zlib AND CC0-1.0 | [COPYING](licenses/python-packages/numpy-2.5.4/COPYING), [LICENSE](licenses/python-packages/numpy-2.5.4/LICENSE), [LICENSE.md](licenses/python-packages/numpy-2.5.4/LICENSE.md), [LICENSE.txt](licenses/python-packages/numpy-2.5.4/LICENSE.txt), [distributions-LICENSE.md](licenses/python-packages/numpy-2.5.4/distributions-LICENSE.md), [dragon4_LICENSE.txt](licenses/python-packages/numpy-2.5.4/dragon4_LICENSE.txt), [lapack_lite-LICENSE.txt](licenses/python-packages/numpy-2.5.4/lapack_lite-LICENSE.txt), [libdivide-LICENSE.txt](licenses/python-packages/numpy-2.5.4/libdivide-LICENSE.txt), [ma-LICENSE](licenses/python-packages/numpy-2.5.4/ma-LICENSE), [mt19937-LICENSE.md](licenses/python-packages/numpy-2.5.4/mt19937-LICENSE.md), [pcg64-LICENSE.md](licenses/python-packages/numpy-2.5.4/pcg64-LICENSE.md), [philox-LICENSE.md](licenses/python-packages/numpy-2.5.4/philox-LICENSE.md), [pocketfft-LICENSE.md](licenses/python-packages/numpy-2.5.4/pocketfft-LICENSE.md), [random-LICENSE.md](licenses/python-packages/numpy-2.5.4/random-LICENSE.md), [random-LICENSE.txt](licenses/python-packages/numpy-2.5.4/random-LICENSE.txt), [sfc64-LICENSE.md](licenses/python-packages/numpy-2.5.4/sfc64-LICENSE.md), [splitmix64-LICENSE.md](licenses/python-packages/numpy-2.5.4/splitmix64-LICENSE.md), [svml-LICENSE](licenses/python-packages/numpy-2.5.4/svml-LICENSE) |
| onnxruntime-1.24.4 | MIT | [LICENSE](licenses/python-packages/onnxruntime-1.24.4/LICENSE), [ThirdPartyNotices.txt](licenses/python-packages/onnxruntime-1.24.4/ThirdPartyNotices.txt) |
| packaging-26.3 | Apache-2.0 OR BSD-2-Clause | [LICENSE](licenses/python-packages/packaging-26.3/LICENSE), [LICENSE.APACHE](licenses/python-packages/packaging-26.3/LICENSE.APACHE), [LICENSE.BSD](licenses/python-packages/packaging-26.3/LICENSE.BSD) |
| platformdirs-4.14.7 | MIT | [LICENSE](licenses/python-packages/platformdirs-4.14.7/LICENSE) |
| protobuf-7.36.2 | BSD-3-Clause | [LICENSE](licenses/python-packages/protobuf-7.36.2/LICENSE) |
| pycparser-3.12 | BSD-3-Clause | [LICENSE](licenses/python-packages/pycparser-3.12/LICENSE) |
| pydantic-2.14.3 | MIT | [LICENSE](licenses/python-packages/pydantic-2.14.3/LICENSE) |
| pydantic_core-2.50.4 | MIT | [LICENSE](licenses/python-packages/pydantic_core-2.50.4/LICENSE) |
| Pygments-2.21.0 | BSD-2-Clause | [AUTHORS](licenses/python-packages/Pygments-2.21.0/AUTHORS), [LICENSE](licenses/python-packages/Pygments-2.21.0/LICENSE) |
| pywhispercpp-1.5.1 | MIT | [LICENSE](licenses/python-packages/pywhispercpp-1.5.1/LICENSE) |
| PyYAML-6.0.3 | MIT | [LICENSE](licenses/python-packages/PyYAML-6.0.3/LICENSE) |
| referencing-0.37.0 | MIT | [COPYING](licenses/python-packages/referencing-0.37.0/COPYING) |
| regex-2026.9.29 | Apache-2.0 AND CNRI-Python | [LICENSE.txt](licenses/python-packages/regex-2026.9.29/LICENSE.txt) |
| requests-2.34.2 | Apache-2.0 | [LICENSE](licenses/python-packages/requests-2.34.2/LICENSE), [NOTICE](licenses/python-packages/requests-2.34.2/NOTICE) |
| rich-15.0.0 | MIT | [LICENSE](licenses/python-packages/rich-15.0.0/LICENSE) |
| rpds-py-2026.9.1 | MIT | [LICENSE](licenses/python-packages/rpds-py-2026.9.1/LICENSE) |
| safetensors-0.8.0 | Apache Software License | [LICENSE](licenses/python-packages/safetensors-0.8.0/LICENSE) |
| setuptools-78.1.0 | MIT License | [LICENSE](licenses/python-packages/setuptools-78.1.0/LICENSE), [LICENSE.APACHE](licenses/python-packages/setuptools-78.1.0/LICENSE.APACHE), [LICENSE.BSD](licenses/python-packages/setuptools-78.1.0/LICENSE.BSD), [LICENSE.txt](licenses/python-packages/setuptools-78.1.0/LICENSE.txt), [NOTICE](licenses/python-packages/setuptools-78.1.0/NOTICE), [_validate_pyproject-NOTICE](licenses/python-packages/setuptools-78.1.0/_validate_pyproject-NOTICE), [autocommand-2.2.2.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/autocommand-2.2.2.dist-info-LICENSE), [backports.tarfile-1.2.0.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/backports.tarfile-1.2.0.dist-info-LICENSE), [importlib_metadata-8.0.0.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/importlib_metadata-8.0.0.dist-info-LICENSE), [inflect-7.3.1.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/inflect-7.3.1.dist-info-LICENSE), [jaraco.collections-5.1.0.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/jaraco.collections-5.1.0.dist-info-LICENSE), [jaraco.context-5.3.0.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/jaraco.context-5.3.0.dist-info-LICENSE), [jaraco.functools-4.0.1.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/jaraco.functools-4.0.1.dist-info-LICENSE), [jaraco.text-3.12.1.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/jaraco.text-3.12.1.dist-info-LICENSE), [licenses-LICENSE](licenses/python-packages/setuptools-78.1.0/licenses-LICENSE), [more_itertools-10.3.0.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/more_itertools-10.3.0.dist-info-LICENSE), [packaging-24.2.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/packaging-24.2.dist-info-LICENSE), [packaging-LICENSE](licenses/python-packages/setuptools-78.1.0/packaging-LICENSE), [packaging-LICENSE.APACHE](licenses/python-packages/setuptools-78.1.0/packaging-LICENSE.APACHE), [packaging-LICENSE.BSD](licenses/python-packages/setuptools-78.1.0/packaging-LICENSE.BSD), [tomli-2.0.1.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/tomli-2.0.1.dist-info-LICENSE), [typeguard-4.3.0.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/typeguard-4.3.0.dist-info-LICENSE), [typing_extensions-4.12.2.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/typing_extensions-4.12.2.dist-info-LICENSE), [zipp-3.19.2.dist-info-LICENSE](licenses/python-packages/setuptools-78.1.0/zipp-3.19.2.dist-info-LICENSE) |
| shellingham-1.5.4 | ISC License | [LICENSE](licenses/python-packages/shellingham-1.5.4/LICENSE) |
| sounddevice-0.5.6 | MIT | [LICENSE](licenses/python-packages/sounddevice-0.5.6/LICENSE) |
| sympy-1.14.0 | BSD | [AUTHORS](licenses/python-packages/sympy-1.14.0/AUTHORS), [LICENSE](licenses/python-packages/sympy-1.14.0/LICENSE), [LICENSE.txt](licenses/python-packages/sympy-1.14.0/LICENSE.txt) |
| tokenizers-0.23.3 | Apache Software License | [LICENSE-Apache-2.0.txt](licenses/python-packages/tokenizers-0.23.3/LICENSE-Apache-2.0.txt) |
| torch-2.15.0+cu132 | Apache-2.0 AND Apache-2.0 WITH LLVM-exception AND BSD-2-Clause AND BSD-3-Clause AND BSL-1.0 AND ISC AND MIT AND Zlib | [FP16-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/FP16-LICENSE), [FXdiv-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/FXdiv-LICENSE), [LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE), [LICENSE-MIT.txt](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE-MIT.txt), [LICENSE-extra](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE-extra), [LICENSE.APACHE](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE.APACHE), [LICENSE.Apache-2.0](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE.Apache-2.0), [LICENSE.BSD](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE.BSD), [LICENSE.MIT](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE.MIT), [LICENSE.md](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE.md), [LICENSE.txt](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE.txt), [LICENSE.uvw](licenses/python-packages/torch-2.15.0%2Bcu132/LICENSE.uvw), [NNPACK-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/NNPACK-LICENSE), [VulkanMemoryAllocator-LICENSE.txt](licenses/python-packages/torch-2.15.0%2Bcu132/VulkanMemoryAllocator-LICENSE.txt), [XNNPACK-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/XNNPACK-LICENSE), [aiter-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/aiter-LICENSE), [asmjit-LICENSE.md](licenses/python-packages/torch-2.15.0%2Bcu132/asmjit-LICENSE.md), [clog-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/clog-LICENSE), [composable_kernel-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/composable_kernel-LICENSE), [cpp-httplib-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/cpp-httplib-LICENSE), [cpuinfo-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/cpuinfo-LICENSE), [cudnn_frontend-LICENSE.txt](licenses/python-packages/torch-2.15.0%2Bcu132/cudnn_frontend-LICENSE.txt), [cute-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/cute-LICENSE), [cutlass-LICENSE.txt](licenses/python-packages/torch-2.15.0%2Bcu132/cutlass-LICENSE.txt), [dynolog_headers-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/dynolog_headers-LICENSE), [fbgemm-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/fbgemm-LICENSE), [flash-attention-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/flash-attention-LICENSE), [flash_attn-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/flash_attn-LICENSE), [flatbuffers-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/flatbuffers-LICENSE), [fmt-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/fmt-LICENSE), [gemmlowp-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/gemmlowp-LICENSE), [gloo-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/gloo-LICENSE), [ideep-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/ideep-LICENSE), [kineto-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/kineto-LICENSE), [libnop-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/libnop-LICENSE), [libuv-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/libuv-LICENSE), [llvm-openmp-LICENSE.txt](licenses/python-packages/torch-2.15.0%2Bcu132/llvm-openmp-LICENSE.txt), [mimalloc-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/mimalloc-LICENSE), [miniz-3.0.2-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/miniz-3.0.2-LICENSE), [mkl-dnn-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/mkl-dnn-LICENSE), [mslk-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/mslk-LICENSE), [onnx-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/onnx-LICENSE), [opencl-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/opencl-LICENSE), [packaging-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/packaging-LICENSE), [packaging-LICENSE.BSD](licenses/python-packages/torch-2.15.0%2Bcu132/packaging-LICENSE.BSD), [perfetto-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/perfetto-LICENSE), [pocketfft-LICENSE.md](licenses/python-packages/torch-2.15.0%2Bcu132/pocketfft-LICENSE.md), [protobuf-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/protobuf-LICENSE), [psimd-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/psimd-LICENSE), [pthreadpool-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/pthreadpool-LICENSE), [pybind11-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/pybind11-LICENSE), [quack-LICENSE](licenses/python-packages/torch-2.15.0%2Bcu132/quack-LICENSE), [sleef-LICENSE.txt](licenses/python-packages/torch-2.15.0%2Bcu132/sleef-LICENSE.txt), [tensorpipe-LICENSE.txt](licenses/python-packages/torch-2.15.0%2Bcu132/tensorpipe-LICENSE.txt) |
| tqdm-4.70.1 | MPL-2.0 AND MIT | [LICENCE](licenses/python-packages/tqdm-4.70.1/LICENCE) |
| transformers-5.22.1 | Apache 2.0 License | [LICENSE](licenses/python-packages/transformers-5.22.1/LICENSE) |
| triton-windows-3.9.0.post30 | MIT | [LICENSE](licenses/python-packages/triton-windows-3.9.0.post30/LICENSE) |
| truststore-0.10.5 | MIT | [LICENSE](licenses/python-packages/truststore-0.10.5/LICENSE) |
| typer-0.27.3 | MIT | [LICENSE](licenses/python-packages/typer-0.27.3/LICENSE), [LICENSE.txt](licenses/python-packages/typer-0.27.3/LICENSE.txt) |
| typing-inspection-0.4.5 | MIT | [LICENSE](licenses/python-packages/typing-inspection-0.4.5/LICENSE) |
| typing_extensions-4.16.0 | PSF-2.0 | [LICENSE](licenses/python-packages/typing_extensions-4.16.0/LICENSE) |
| urllib3-2.8.0 | MIT | [LICENSE.txt](licenses/python-packages/urllib3-2.8.0/LICENSE.txt) |
| xgrammar-0.2.9 | Apache 2.0 | [LICENSE](licenses/python-packages/xgrammar-0.2.9/LICENSE), [NOTICE](licenses/python-packages/xgrammar-0.2.9/NOTICE) |

## Оболочка (.NET, NuGet) / Desktop shell (.NET, NuGet)

| Пакет | Лицензия | Тексты |
|---|---|---|
| Avalonia 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia-12.1.6/LICENSE-MIT.txt) |
| Avalonia.Angle.Windows.Natives 2.1.27548.20260419 | см. текст | [LICENSE](licenses/dotnet/Avalonia.Angle.Windows.Natives-2.1.27548.20260419/LICENSE) |
| Avalonia.Desktop 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.Desktop-12.1.6/LICENSE-MIT.txt) |
| Avalonia.Fonts.Inter 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.Fonts.Inter-12.1.6/LICENSE-MIT.txt) |
| Avalonia.FreeDesktop 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.FreeDesktop-12.1.6/LICENSE-MIT.txt) |
| Avalonia.FreeDesktop.AtSpi 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.FreeDesktop.AtSpi-12.1.6/LICENSE-MIT.txt) |
| Avalonia.HarfBuzz 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.HarfBuzz-12.1.6/LICENSE-MIT.txt) |
| Avalonia.Native 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.Native-12.1.6/LICENSE-MIT.txt) |
| Avalonia.Remote.Protocol 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.Remote.Protocol-12.1.6/LICENSE-MIT.txt) |
| Avalonia.Skia 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.Skia-12.1.6/LICENSE-MIT.txt) |
| Avalonia.Themes.Fluent 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.Themes.Fluent-12.1.6/LICENSE-MIT.txt) |
| Avalonia.Win32 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.Win32-12.1.6/LICENSE-MIT.txt) |
| Avalonia.X11 12.1.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Avalonia.X11-12.1.6/LICENSE-MIT.txt) |
| HarfBuzzSharp 8.3.1.3 | MIT | [LICENSE.txt](licenses/dotnet/HarfBuzzSharp-8.3.1.3/LICENSE.txt) |
| HarfBuzzSharp.NativeAssets.Win32 8.3.1.3 | MIT | [LICENSE.txt](licenses/dotnet/HarfBuzzSharp.NativeAssets.Win32-8.3.1.3/LICENSE.txt), [THIRD-PARTY-NOTICES.txt](licenses/dotnet/HarfBuzzSharp.NativeAssets.Win32-8.3.1.3/THIRD-PARTY-NOTICES.txt) |
| MicroCom.Runtime 0.11.6 | MIT | [LICENSE-MIT.txt](licenses/dotnet/MicroCom.Runtime-0.11.6/LICENSE-MIT.txt) |
| Microsoft.NETCore.App.Runtime.win-x64 10.0.12 | MIT | [LICENSE.TXT](licenses/dotnet/Microsoft.NETCore.App.Runtime.win-x64-10.0.12/LICENSE.TXT), [THIRD-PARTY-NOTICES.TXT](licenses/dotnet/Microsoft.NETCore.App.Runtime.win-x64-10.0.12/THIRD-PARTY-NOTICES.TXT) |
| SkiaSharp 3.119.4 | MIT | [LICENSE.txt](licenses/dotnet/SkiaSharp-3.119.4/LICENSE.txt) |
| SkiaSharp.NativeAssets.Win32 3.119.4 | MIT | [LICENSE.txt](licenses/dotnet/SkiaSharp.NativeAssets.Win32-3.119.4/LICENSE.txt), [THIRD-PARTY-NOTICES.txt](licenses/dotnet/SkiaSharp.NativeAssets.Win32-3.119.4/THIRD-PARTY-NOTICES.txt) |
| Tmds.DBus.Protocol 0.94.1 | MIT | [LICENSE-MIT.txt](licenses/dotnet/Tmds.DBus.Protocol-0.94.1/LICENSE-MIT.txt) |
