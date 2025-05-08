# Transcribe and Translate Subtitles

## 🚨 Important Note
- **This project is not recommended for commercial use.**
- **Every task runs locally without internet, ensuring maximum privacy.**

---

## ✨ Features  
This project is built on ONNX Runtime framework.
- Deoiser Support:
  - [ZipEnhancer](https://modelscope.cn/models/iic/speech_zipenhancer_ans_multiloss_16k_base)
  - [GTCRN](https://github.com/Xiaobin-Rong/gtcrn)
  - [DFSMN](https://modelscope.cn/models/iic/speech_dfsmn_ans_psm_48k_causal)
  - [Mel-Band-Roformer](https://github.com/KimberleyJensen/Mel-Band-Roformer-Vocal-Model)

- VAD Support:
  - [FSMN](https://modelscope.cn/models/iic/speech_fsmn_vad_zh-cn-16k-common-pytorch)
  - [Faster_Whisper - Silero](https://github.com/SYSTRAN/faster-whisper/blob/master/faster_whisper/vad.py)
  - [Official - Silero](https://github.com/snakers4/silero-vad)
  - [Pyannote-Segmentation-3.0](https://huggingface.co/pyannote/segmentation-3.0)
    - You need to download the Pyannote `pytorch_model.bin` file yourself and place it in the `VAD/pyannote_segmentation_3` folder.

- ASR Support:
  - [SenseVoice-Small](https://modelscope.cn/models/iic/SenseVoiceSmall)
  - [Paraformer-Large-Chinese](https://modelscope.cn/models/iic/speech_paraformer-large_asr_nat-zh-cn-16k-common-vocab8404-pytorch)
  - [Paraformer-Large-English](https://modelscope.cn/models/iic/speech_paraformer_asr-en-16k-vocab4199-pytorch)
  - [Paraformer-Small-Chinese](https://modelscope.cn/models/iic/speech_paraformer_asr_nat-zh-cn-16k-common-vocab8358-tensorflow1)
  - [Whisper-Large-V3](https://huggingface.co/openai/whisper-large-v3)
  - [Whisper-Large-V3-Turbo](https://huggingface.co/openai/whisper-large-v3-turbo)
  - [Whisper-Large-V3-Turbo-Japanese](https://huggingface.co/hhim8826/whisper-large-v3-turbo-ja)
  - [Whisper-Large-v3.5-Distil](https://huggingface.co/distil-whisper/distil-large-v3.5)
  - [Whisper-Large-V3-Anime-A](https://huggingface.co/efwkjn/whisper-ja-anime-v0.1)
  - [Whisper-Large-V3-Anime-B](https://huggingface.co/litagin/anime-whisper)
  - [CrisperWhisper](https://github.com/nyrahealth/CrisperWhisper)
  - [FireRedASR-AED-L](https://github.com/FireRedTeam/FireRedASR)

- LLM Supports: 
  - Qwen-3: [4B](https://modelscope.cn/models/Qwen/Qwen3-4B), [8B](https://modelscope.cn/models/Qwen/Qwen3-8B)
  - InternLM-3: [8B](https://huggingface.co/internlm/internlm3-8b-instruct)
  - Gemma-3-it: [4B](https://huggingface.co/google/gemma-3-4b-it), [12B](https://huggingface.co/google/gemma-3-12b-it)  
  - Phi-4-Instruct: [mini](https://huggingface.co/microsoft/Phi-4-mini-instruct)
---

## 📋 Setup Instructions

### ✅ Step 1: Install Dependencies
- Run the following command in your terminal to install the latest required Python packages:
- For Apple Silicon M-series chips, avoid installing `onnxruntime-openvino`, as it will cause errors.
```bash
conda install ffmpeg

pip install -r requirements.txt
```

### 📥 Step 2: Download Necessary Models
- Download the required models from HuggingFace: [Transcribe_and_Translate_Subtitles](https://huggingface.co/H5N1AIDS/Transcribe_and_Translate_Subtitles).


### 🖥️ Step 3: Download and Place `run.py`
- Download the `run.py` script from this repository.
- Place it in the `Transcribe_and_Translate_Subtitles` folder.

### 📁 Step 4: Place Target Videos in the Media Folder
- Place the videos you want to transcribe and translate in the following directory:
```
Transcribe_and_Translate_Subtitles/Media
```
- The application will process the videos one by one.

### 🚀 Step 5: Run the Application
- Open your preferred terminal (PyCharm, CMD, PowerShell, etc.).
- Execute the following command to start the application:
```bash
python run.py
```
- Once the application starts, you will see a webpage open in your browser.
   ![screenshot](https://github.com/DakeQQ/Transcribe-and-Translate-Subtitles/blob/main/screen/Screenshot%20from%202025-05-08%2013-01-17.png)

### 🛠️ Step 6: Fix Silero-VAD Error (if encountered)
- On the first run, you might encounter a **Silero-VAD error**. Simply restart the application, and it should be resolved.

### 💻 Step 7: Device Support
- This project currently supports:
  - **Intel-OpenVINO-CPU-GPU-NPU**
  - **Windows-AMD-GPU**
  - **NVIDIA-GPU**
  - **Apple-CPU**
  - **AMD-CPU**

---

## 🎉 Enjoy the Application!
```
Transcribe_and_Translate_Subtitles/Results/Subtitles
```
---

## 📌 To-Do List
- [ ] Real-Time Translate & Trascribe Video Player

---
### 性能 Performance  
| OS           | Backend           | Denoiser          | VAD                  | ASR                  | LLM | Real-Time Factor<br>test_video.mp4<br>7602 seconds |
|:------------:|:-----------------:|:-----------------:|:--------------------:|:--------------------:|:----------------:|:----------------:|
| Ubuntu-24.04 | CPU <br> i3-12300 | -                 | Silero               | SenseVoiceSmall      |        -      |        0.08      |
| Ubuntu-24.04 | CPU <br> i3-12300 | GTCRN             | Silero               | SenseVoiceSmall      | Qwen2.5-7B-Instruct | 0.50       |
| Ubuntu-24.04 | CPU <br> i3-12300 | GTCRN             | FSMN                 | SenseVoiceSmall      |        -      |       0.054      |
| Ubuntu-24.04 | CPU <br> i3-12300 | ZipEnhancer       | FSMN                 | SenseVoiceSmall      |        -      |        0.39      |
| Ubuntu-24.04 | CPU <br> i3-12300 | GTCRN             | Silero               | Whisper-Large-V3     |        -      |        0.20      |
| Ubuntu-24.04 | CPU <br> i3-12300 | GTCRN             | FSMN                 | Whisper-Large-V3-Turbo |      -      |        0.148     |

---
# 转录和翻译字幕

## 🚨 重要提示  
- **不建议将此项目用于商业用途。**  
- **所有任务均在本地运行，无需连接互联网，确保最大程度的隐私保护。**

---

## ✨ 功能
这个项目基于 ONNX Runtime 框架。
- **去噪器 (Denoiser) 支持**：
  - [ZipEnhancer](https://modelscope.cn/models/iic/speech_zipenhancer_ans_multiloss_16k_base)
  - [GTCRN](https://github.com/Xiaobin-Rong/gtcrn)
  - [DFSMN](https://modelscope.cn/models/iic/speech_dfsmn_ans_psm_48k_causal)
  - [Mel-Band-Roformer](https://github.com/KimberleyJensen/Mel-Band-Roformer-Vocal-Model)
 
- **语音活动检测（VAD）支持**：
  - [FSMN](https://modelscope.cn/models/iic/speech_fsmn_vad_zh-cn-16k-common-pytorch)
  - [Faster_Whisper - Silero](https://github.com/SYSTRAN/faster-whisper/blob/master/faster_whisper/vad.py)
  - [官方 - Silero](https://github.com/snakers4/silero-vad)
  - [Pyannote-Segmentation-3.0](https://huggingface.co/pyannote/segmentation-3.0)
    - 需要自行下载 Pyannote `pytorch_model.bin` 文件，并将其放置在 `VAD/pyannote_segmentation_3` 文件夹中。

- **语音识别（ASR）支持**：
  - [SenseVoice-Small](https://modelscope.cn/models/iic/SenseVoiceSmall)
  - [Paraformer-Large-Chinese](https://modelscope.cn/models/iic/speech_paraformer-large_asr_nat-zh-cn-16k-common-vocab8404-pytorch)
  - [Paraformer-Large-English](https://modelscope.cn/models/iic/speech_paraformer_asr-en-16k-vocab4199-pytorch)
  - [Paraformer-Small-Chinese](https://modelscope.cn/models/iic/speech_paraformer_asr_nat-zh-cn-16k-common-vocab8358-tensorflow1)
  - [Whisper-Large-V3](https://huggingface.co/openai/whisper-large-v3)
  - [Whisper-Large-V3-Turbo](https://huggingface.co/openai/whisper-large-v3-turbo)
  - [Whisper-Large-V3-Turbo-Japanese](https://huggingface.co/hhim8826/whisper-large-v3-turbo-ja)
  - [Whisper-Large-v3.5-Distil](https://huggingface.co/distil-whisper/distil-large-v3.5)
  - [Whisper-Large-V3-Anime-A](https://huggingface.co/efwkjn/whisper-ja-anime-v0.1)
  - [Whisper-Large-V3-Anime-B](https://huggingface.co/litagin/anime-whisper)
  - [CrisperWhisper](https://github.com/nyrahealth/CrisperWhisper)
  - [FireRedASR-AED-L](https://github.com/FireRedTeam/FireRedASR)


- **大语言模型（LLM）支持**：  
  - Qwen-3: [4B](https://modelscope.cn/models/Qwen/Qwen3-4B), [8B](https://modelscope.cn/models/Qwen/Qwen3-8B)
  - InternLM-3: [8B](https://huggingface.co/internlm/internlm3-8b-instruct)
  - Gemma-3-it: [4B](https://huggingface.co/google/gemma-3-4b-it), [12B](https://huggingface.co/google/gemma-3-12b-it)  
  - Phi-4-Instruct: [mini](https://huggingface.co/microsoft/Phi-4-mini-instruct)

---

## 📋 设置指南

### ✅ 第一步：安装依赖项  
- 在终端中运行以下命令来安装所需的最新 Python 包：
- 对于苹果 M 系列芯片，请不要安装 `onnxruntime-openvino`，否则会导致错误。
```bash
conda install ffmpeg

pip install -r requirements.txt
```

### 📥 第二步：下载必要的模型  
- 从 HuggingFace 下载所需模型：[Transcribe_and_Translate_Subtitles](https://huggingface.co/H5N1AIDS/Transcribe_and_Translate_Subtitles)


### 🖥️ 第三步：下载并放置 `run.py`  
- 从此项目的仓库下载 `run.py` 脚本。  
- 将 `run.py` 放置在 `Transcribe_and_Translate_Subtitles` 文件夹中。

### 📁 第四步：将目标视频放入 Media 文件夹  
- 将你想要转录和翻译的视频放置在以下目录：  
```
Transcribe_and_Translate_Subtitles/Media
```
- 应用程序将逐个处理这些视频。

### 🚀 第五步：运行应用程序  
- 打开你喜欢的终端工具（PyCharm、CMD、PowerShell 等）。  
- 运行以下命令来启动应用程序：  
```bash
python run.py
```
- 应用程序启动后，你的浏览器将自动打开一个网页。  
   ![screenshot](https://github.com/DakeQQ/Transcribe-and-Translate-Subtitles/blob/main/screen/Screenshot%20from%202025-05-08%2013-01-17.png)

### 🛠️ 第六步：修复 Silero-VAD 错误（如有）  
- 首次运行时，你可能会遇到 **Silero-VAD 错误**。只需重启应用程序即可解决该问题。

### 💻 第七步：支持设备  
- 此项目目前支持:
  - **Intel-OpenVINO-CPU-GPU-NPU**
  - **Windows-AMD-GPU**
  - **NVIDIA-GPU**
  - **Apple-CPU**
  - **AMD-CPU**

## 🎉 尽情享受应用程序吧！
```
Transcribe_and_Translate_Subtitles/Results/Subtitles
```
---

## 📌 待办事项  
- [ ] 实现实时视频转录和翻译播放器
---
