<div align="center">

## 🎬 视频字幕转录和翻译 / Transcribe and Translate Subtitles

**一个强大的、隐私优先的视频字幕转录和翻译工具**
</br>
**A powerful, privacy-first tool for transcribing and translating video subtitles**

[![Privacy First](https://img.shields.io/badge/Privacy-100%25%20Local-green.svg)](https://github.com/your-repo)
[![ONNX Runtime](https://img.shields.io/badge/Powered%20by-ONNX%20Runtime-blue.svg)](https://onnxruntime.ai/)
[![Multi-Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey.svg)](https://github.com/your-repo)

</div>

---

## 🔒 隐私保证 / Privacy Guarantee

> **🚨 所有处理完全离线运行 / All processing runs completely offline**<br>
> - 无需互联网连接，确保最大程度的隐私和数据安全<br>
> - No internet connection required, ensuring maximum privacy and data security.

---

## 🚀 快速入门 / Quick Start

### 环境准备 / Prerequisites
```bash
# 安装 FFmpeg / Install FFmpeg
conda install ffmpeg

pip install -r requirements.txt

# 安装 Python 依赖 / Install Python dependencies
# 请根据您的硬件平台安装正确的包 / Please according to your hardware platform install the right package
# ----------------------------------------
# For CPU only
# onnxruntime>=1.23.2
# ----------------------------------------
# For Linux + AMD
# 请先按照 URL 设置 ROCm / Please follow the URL to set up the ROCm first before pip install onnxruntime-rocm
# https://rocm.docs.amd.com/projects/radeon/en/latest/docs/install/native_linux/install-onnx.html
# https://onnxruntime.ai/docs/execution-providers/Vitis-AI-ExecutionProvider.html
# onnxruntime>=1.23.2
# onnxruntime-rocm>=1.23.0
# ----------------------------------------
# For Windows + (Intel or AMD)
# onnxruntime>=1.23.2
# onnxruntime-directml>=1.23.0
# ----------------------------------------
# For Intel OpenVINO CPU & GPU & NPU
# onnxruntime>=1.23.2
# onnxruntime-openvino>=1.23.0
# ----------------------------------------
# For NVIDIA-CUDA
# onnxruntime>=1.23.2
# onnxruntime-gpu>=1.23.2
# ----------------------------------------
```

### 设置
1.  **下载模型**: 从 [HuggingFace](https://huggingface.co/H5N1AIDS/Transcribe_and_Translate_Subtitles) 获取所需模型 ，只下载您想要的模型并保持文件夹路径与当前定义相同，无需全部下载。
2.  **下载脚本**: 将 `run.py` 放置在您的 `Transcribe_and_Translate_Subtitles` 文件夹中
3.  **添加媒体**: 将您的音视频放置在 `Transcribe_and_Translate_Subtitles/Media/` 目录下
4.  **运行**: 务必在`Transcribe_and_Translate_Subtitles`目录下执行 `python run.py` 并打开 Web 界面

### Setup
1.  **Download Models**: Get the required models from [HuggingFace](https://huggingface.co/H5N1AIDS/Transcribe_and_Translate_Subtitles). Download only the models you want and keep the folder path the same as currently defined, no need to download all.
2.  **Download Script**: Place `run.py` in your `Transcribe_and_Translate_Subtitles` folder
3.  **Add Media**: Place your audios/videos in `Transcribe_and_Translate_Subtitles/Media/`
4.  **Run**: You must execute `python run.py` in the `Transcribe_and_Translate_Subtitles` folder and open the web interface

### 结果 / Results
在以下位置找到您处理后的字幕 / Find your processed subtitles in:
```
Transcribe_and_Translate_Subtitles/Results/Subtitles/
```
**准备好开始了吗？/ Ready to get started?** 🎉
<br>
<br>
<div align="center">
  
![demo](https://github.com/DakeQQ/Transcribe-and-Translate-Subtitles/blob/main/screen/Screenshot%20from%202025-09-19%2013-22-37.png)

</div>

---

## ✨ 功能特性 / Features

### 🔇 降噪模型 / Noise Reduction Models
- **[DFSMN](https://modelscope.cn/models/iic/speech_dfsmn_ans_psm_48k_causal)**
- **[GTCRN](https://github.com/Xiaobin-Rong/gtcrn)**
- **[ZipEnhancer](https://modelscope.cn/models/iic/speech_zipenhancer_ans_multiloss_16k_base)**
- **[Mel-Band-Roformer](https://github.com/KimberleyJensen/Mel-Band-Roformer-Vocal-Model)**
- **[MossFormerGAN_SE_16K](https://www.modelscope.cn/models/alibabasglab/MossFormerGAN_SE_16K)**
- **[MossFormer2_SE_48K](https://www.modelscope.cn/models/alibabasglab/MossFormer2_SE_48K)**

### 🎤 语音活动检测 (VAD) / Voice Activity Detection (VAD)
- **[Faster-Whisper-Silero](https://github.com/SYSTRAN/faster-whisper/blob/master/faster_whisper/vad.py)**
- **[Official-Silero-v6](https://github.com/snakers4/silero-vad)**
- **[HumAware](https://huggingface.co/CuriousMonkey7/HumAware-VAD)**
- **[NVIDIA-NeMo-VAD-v2.0](https://huggingface.co/nvidia/Frame_VAD_Multilingual_MarbleNet_v2.0)**
- **[TEN-VAD](https://github.com/TEN-framework/ten-vad)**
- **[Pyannote-Segmentation-3.0](https://huggingface.co/pyannote/segmentation-3.0)**
  - *注意：您需要接受 Pyannote 的使用条款并下载 Pyannote 的 `pytorch_model.bin` 文件。将其放置在 `VAD/pyannote_segmentation` 文件夹中*。
  - *Note: You need to accept Pyannote's terms of use and download the Pyannote `pytorch_model.bin` file. Place it in the `VAD/pyannote_segmentation` folder.*

### 🗣️ 语音识别 (ASR) / Speech Recognition (ASR)
#### 多语言模型 / Multilingual Models
- **[Fun-ASR-Nano-2512-Multilingual](https://modelscope.cn/models/FunAudioLLM/Fun-ASR-Nano-2512)**
- **[Fun-ASR-MLT-Nano-2512-Multilingual](https://modelscope.cn/models/FunAudioLLM/Fun-ASR-MLT-Nano-2512)**
- **[SenseVoice-Small-Multilingual](https://modelscope.cn/models/iic/SenseVoiceSmall)**
- **[Dolphin-Small-Asian 亚洲语言](https://github.com/DataoceanAI/Dolphin)**
- **[Paraformer-Large-Chinese 中文](https://modelscope.cn/models/iic/speech_paraformer-large_asr_nat-zh-cn-16k-common-vocab8404-pytorch)**
- **[Paraformer-Large-English 英语](https://modelscope.cn/models/iic/speech_paraformer_asr-en-16k-vocab4199-pytorch)**
- **[FireRedASR-AED-L Chinese 中文](https://github.com/FireRedTeam/FireRedASR)**
- **[Official-Whisper-Large-v3-Multilingual](https://huggingface.co/openai/whisper-large-v3)**
- **[Official-Whisper-Large-v3-Turbo-Multilingual](https://huggingface.co/openai/whisper-large-v3-turbo)**
- **[阿拉伯语 / Arabic](https://huggingface.co/Byne/whisper-large-v3-arabic)**
- **[巴斯克语 / Basque](https://huggingface.co/xezpeleta/whisper-large-v3-eu)**
- **[粤语 / Cantonese-Yue](https://huggingface.co/JackyHoCL/whisper-large-v3-turbo-cantonese-yue-english)**
- **[中文 / Chinese](https://huggingface.co/BELLE-2/Belle-whisper-large-v3-zh-punct)**
- **[台湾客家话 / Chinese-Hakka](https://huggingface.co/formospeech/whisper-large-v3-taiwanese-hakka)**
- **[台湾闽南语 / Chinese-Minnan](https://huggingface.co/TSukiLen/whisper-medium-chinese-tw-minnan)**
- **[台湾华语 / Chinese-Taiwan](https://huggingface.co/JacobLinCool/whisper-large-v3-turbo-common_voice_19_0-zh-TW)**
- **[CrisperWhisper-Multilingual](https://github.com/nyrahealth/CrisperWhisper)**
- **[丹麦语 / Danish](https://huggingface.co/sam8000/whisper-large-v3-turbo-danish-denmark)**
- **[印度英语 / English-Indian](https://huggingface.co/Tejveer12/Indian-Accent-English-Whisper-Finetuned)**
- **[英语 v3.5 / Engish-v3.5](https://huggingface.co/distil-whisper/distil-large-v3.5)**
- **[法语 / French](https://huggingface.co/bofenghuang/whisper-large-v3-french-distil-dec16)**
- **[瑞士德语 / German-Swiss](https://huggingface.co/Flurin17/whisper-large-v3-turbo-swiss-german)**
- **[德语 / German](https://huggingface.co/primeline/whisper-large-v3-turbo-german)**
- **[希腊语 / Greek](https://huggingface.co/sam8000/whisper-large-v3-turbo-greek-greece)**
- **[意大利语 / Italian](https://huggingface.co/bofenghuang/whisper-large-v3-distil-it-v0.2)**
- **[日语-动漫 / Japanese-Anime](https://huggingface.co/efwkjn/whisper-ja-anime-v0.3)**
- **[日语 / Japanese](https://huggingface.co/hhim8826/whisper-large-v3-turbo-ja)**
- **[韩语 / Korean](https://huggingface.co/ghost613/whisper-large-v3-turbo-korean)**
- **[马来语 / Malaysian](https://huggingface.co/mesolitica/Malaysian-whisper-large-v3-turbo-v3)**
- **[波斯语 / Persian](https://huggingface.co/MohammadGholizadeh/whisper-large-v3-persian-common-voice-17)**
- **[波兰语 / Polish](https://huggingface.co/Aspik101/distil-whisper-large-v3-pl)**
- **[葡萄牙语 / Portuguese](https://huggingface.co/freds0/distil-whisper-large-v3-ptbr)**
- **[俄语 / Russian](https://huggingface.co/dvislobokov/whisper-large-v3-turbo-russian)**
- **[塞尔维亚语 / Serbian](https://huggingface.co/Sagicc/whisper-large-v3-sr-combined)**
- **[西班牙语 / Spanish](https://huggingface.co/Berly00/whisper-large-v3-spanish)**
- **[泰语 / Thai](https://huggingface.co/nectec/Pathumma-whisper-th-large-v3)**
- **[土耳其语 / Turkish](https://huggingface.co/selimc/whisper-large-v3-turbo-turkish)**
- **[乌尔都语 / Urdu](https://huggingface.co/urdu-asr/whisper-large-v3-ur)**
- **[越南语 / Vietnamese](https://huggingface.co/suzii/vi-whisper-large-v3-turbo-v1)**

### 🤖 翻译模型 (LLM) / Translation Models (LLM)
- **[Qwen-3-4B-Instruct-2507-Abliterated](https://huggingface.co/huihui-ai/Huihui-Qwen3-4B-Instruct-2507-abliterated)**
- **[Qwen-3-8B-Abliterated](https://huggingface.co/huihui-ai/Huihui-Qwen3-8B-abliterated-v2)**
- **[Hunyuan-MT-1.5-1.8B-Abliterated](https://huggingface.co/huihui-ai/Huihui-HY-MT1.5-1.8B-abliterated)**
- **[Hunyuan-MT-1.5-7B-Abliterated](https://huggingface.co/huihui-ai/Huihui-HY-MT1.5-7B-abliterated)**
- **[Seed-X-PRO-7B](https://www.modelscope.cn/models/ByteDance-Seed/Seed-X-PPO-7B)**

---
  
## 🖥️ 硬件支持 / Hardware Support
<table>
  <tr>
    <td align="center"><strong>💻 中央處理器 (CPU)</strong></td>
    <td align="center"><strong>🎮 圖形處理器 (GPU)</strong></td>
    <td align="center"><strong>🧠 神經網路處理單元 (NPU)</strong></td>
  </tr>
  <tr>
    <td valign="top">
      <ul>
        <li>Apple Silicon</li>
        <li>AMD</li>
        <li>ARM</li>
        <li>Intel</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li>Apple CoreML</li>
        <li>AMD ROCm</li>
        <li>Intel OpenVINO</li>
        <li>NVIDIA CUDA</li>
        <li>Windows DirectML</li>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li>Apple CoreML</li>
        <li>AMD Ryzen-VitisAI</li>
        <li>Intel OpenVINO</li>
      </ul>
    </td>
  </tr>
</table>

---

## 📊 性能基准测试 / Performance Benchmarks

*测试条件 / Test Conditions： Ubuntu 24.04, Intel i3-12300, 7602 秒视频*

| 操作系统 (OS) | 后端 (Backend) | 降噪器 (Denoiser) | VAD | 语音识别 (ASR) | 大语言模型 (LLM) | 实时率<br>(Real-Time Factor) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Ubuntu-24.04 | CPU i3-12300 | - | Silero | SenseVoiceSmall | - | **0.08** |
| Ubuntu-24.04 | CPU i3-12300 | GTCRN | Silero | SenseVoiceSmall | Qwen2.5-7B-Instruct | **0.50** |
| Ubuntu-24.04 | CPU i3-12300 | GTCRN | FSMN | SenseVoiceSmall | - | **0.054** |
| Ubuntu-24.04 | CPU i3-12300 | ZipEnhancer | FSMN | SenseVoiceSmall | - | **0.39** |
| Ubuntu-24.04 | CPU i3-12300 | GTCRN | Silero | Whisper-Large-V3 | - | **0.20** |
| Ubuntu-24.04 | CPU i3-12300 | GTCRN | FSMN | Whisper-Large-V3-Turbo | - | **0.148** |

---

## 🛠️ 问题排查 / Troubleshooting

### 常见问题 / Common Issues
- **Silero VAD 错误 / Silero VAD Error**: 首次运行时只需重启应用程序 / Simply restart the application on first run
- **libc++ 错误 (Linux) / libc++ Error (Linux)**:
  ```bash
  sudo apt update
  sudo apt install libc++1
  ```
- **苹果芯片 / Apple Silicon**: 请避免安装 `onnxruntime-openvino`，因为它会导致错误 / Avoid installing `onnxruntime-openvino` as it will cause errors

---

## 📋 更新历史 / Update History

### 🆕 **2026/1/4** - 更新 / Release
- ✅ **新增 ASR / Added ASR**:
  - FunASR-Nano-2512
  - FunASR-Nano-MLT-2512
- ✅ **更新 LLM / update LLM**:
  - 更新 Hunyuan-MT-1.5-1.8B-Abliterated
  - 更新 Hunyuan-MT-1.5-7B-Abliterated
- ✅ **性能改进 / Performance Improvements**:
  - 改善 SenseVoice & Paraformer 长音频的准确度
  - 改善 Nvidia_VAD, Ten_VAD, HumAware_VAD 音频切割准确度
  - 修复 LLM 在翻译时偶尔输出乱码文字
  - Improve the long audio accuracy of SenseVoice and Paraformer
  - Improve the accuracy of Nvidia_VAD, Ten_VAD, and HumAwareVAD audio segmentation
  - Fix LLM occasionally outputting garbled text during translation
    
### 🆕 **2025/9/19** - 重大更新 / Major Release
- ✅ **新增 ASR / Added ASR**:
  - 28 个地区微调的 Whisper 模型
  - 28 region fine-tuned Whisper models
- ✅ **新增降噪器 / Added Denoiser**: MossFormer2_SE_48K
- ✅ **新增 LLM 模型 / Added LLM Models**:
  - Qwen3-4B-Instruct-2507-abliterated
  - Qwen3-8B-abliterated-v2
  - Hunyuan-MT-7B-abliterated
  - Seed-X-PRO-7B
- ✅ **性能改进 / Performance Improvements**:
  - 为类 Whisper 的 ASR 模型应用了束搜索（Beam Search）和重复惩罚（Repeat Penalty）
  - 应用 ONNX Runtime IOBinding 实现最大加速（比常规 ort_session.run() 快 10%以上）
  - 支持单次推理处理 20 秒的音频片段
  - 改进了多线程性能
  - Applied Beam Search & Repeat Penalty for Whisper-like ASR models
  - Applied ONNX Runtime IOBinding for maximum speed up (10%+ faster than normal ort_session.run())
  - Support for 20 seconds audio segment per single run inference
  - Improved multi-threads performance
- ✅ **硬件支持扩展 / Hardware Support Expansion**:
  - AMD-ROCm 执行提供程序 / Execution Provider
  - AMD-MIGraphX 执行提供程序 / Execution Provider
  - NVIDIA TensorRTX 执行提供程序 / Execution Provider
  - *(必须先配置环境，否则无法工作 / Must config the env first or it will not work)*
- ✅ **准确性改进 / Accuracy Improvements**:
  - SenseVoice
  - Paraformer
  - FireRedASR
  - Dolphin
  - ZipEnhancer
  - MossFormerGAN_SE_16K
  - NVIDIA-NeMo-VAD
- ✅ **速度改进 / Speed Improvements**:
  - MelBandRoformer (通过转换为单声道提升速度 / speed boost by converting to mono channel)
- ❌ **移除的模型 / Removed Models**:
  - FSMN-VAD
  - Qwen3-4B-Official
  - Qwen3-8B-Official
  - Gemma3-4B-it
  - Gemma3-12B-it
  - InternLM3
  - Phi-4-Instruct

### **2025/7/5** - 降噪增强 / Noise Reduction Enhancement
- ✅ **新增降噪模型 / Added noise reduction model**: MossFormerGAN_SE_16K

### **2025/6/11** - VAD 模型扩展 / VAD Models Expansion
- ✅ **新增 VAD 模型 / Added VAD Models**:
  - HumAware-VAD
  - NVIDIA-NeMo-VAD
  - TEN-VAD

### **2025/6/3** - 亚洲语言支持 / Asian Language Support
- ✅ **新增 Dolphin ASR 模型以支持亚洲语言 / Added Dolphin ASR model** to support Asian languages

### **2025/5/13** - GPU 加速 / GPU Acceleration
- ✅ **新增 Float16/32 ASR 模型以支持 CUDA/DirectML GPU / Added Float16/32 ASR models** to support CUDA/DirectML GPU usage
- ✅ **GPU 性能 / GPU Performance**: 这些模型可以实现超过 99% 的 GPU 算子部署 / These models can achieve >99% GPU operator deployment

### **2025/5/9** - 主要功能发布 / Major Feature Release
- ✅ **灵活性改进 / Flexibility Improvements**:
  - 新增不使用 VAD（语音活动检测）的选项 / Added option to **not use** VAD (Voice Activity Detection)
- ✅ **新增模型 / Added Models**:
  - **降噪 / Noise reduction**: MelBandRoformer
  - **ASR**: CrisperWhisper
  - **ASR**: Whisper-Large-v3.5-Distil (英语微调 / English fine-tuned)
  - **ASR**: FireRedASR-AED-L (支持中文及方言 / Chinese + dialects support)
  - **三个日语动漫微调的 Whisper 模型 / Three Japanese anime fine-tuned Whisper models**
- ✅ **性能优化 / Performance Optimizations**:
  - 移除 IPEX-LLM 框架以提升整体性能 / Removed IPEX-LLM framework to enhance overall performance
  - 取消 LLM 量化选项，统一使用 **Q4F32** 格式 / Cancelled LLM quantization options, standardized on **Q4F32** format
  - Whisper 系列推理速度提升 10% 以上 / Improved **Whisper** series inference speed by over 10%
- ✅ **准确性改进 / Accuracy Improvements**:
  - 提升 **FSMN-VAD** 准确率 / Improved **FSMN-VAD** accuracy
  - 提升 **Paraformer** 识别准确率 / Improved **Paraformer** recognition accuracy
  - 提升 **SenseVoice** 识别准确率 / Improved **SenseVoice** recognition accuracy
- ✅ **LLM 支持 ONNX Runtime 100% GPU 算子部署 / LLM Support with ONNX Runtime 100% GPU operator deployment**:
  - Qwen3-4B/8B
  - InternLM3-8B
  - Phi-4-mini-Instruct
  - Gemma3-4B/12B-it
- ✅ **硬件支持扩展 / Hardware Support Expansion**:
  - **Intel OpenVINO**
  - **NVIDIA CUDA GPU**
  - **Windows DirectML GPU** (支持集成显卡和独立显卡 / supports integrated and discrete GPUs)

---

## 🗺️ 路线图 / Roadmap
- [ ] **Beam Search for LLM**
- [ ] 分离说话人 / Speaker separation
- [ ] 声纹识别 / voiceprint recognition
- [ ] **视频超分 / [Video Upscaling](https://github.com/ByteDance-Seed/SeedVR/tree/main)** - 提升分辨率 / Enhance resolution
- [ ] **实时播放器 / Real-time Player** - 实时转录和翻译 / Live transcription and translation
