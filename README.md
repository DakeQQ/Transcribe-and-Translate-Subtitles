# Transcribe and Translate Subtitles

## 🚨 Important Note
- **This project is for non-commercial use only!**
- **Every task runs locally without internet, ensuring maximum privacy**

---

## 📋 Setup Instructions

### ✅ Step 1: Install Dependencies
Run the following command in your terminal to install the latest required Python packages:
```bash
pip install -r requirements.txt
```

### 📥 Step 2: Download Necessary Models
1. Download the required models from Google Drive: [Transcribe_and_Translate_Subtitles](https://drive.google.com/drive/folders/1W5yqPm-FYD2r1KR7JrDwJ8jzuFALNr9O?usp=drive_link)
2. After downloading, unzip the file.

### 🤖 Step 3: Download a Preferred LLM Model
1. Choose and download your preferred LLM model. LLM Supports: [ipex-llm](https://github.com/intel-analytics/ipex-llm).  For example: [Qwen2.5-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct)
2. The largest LLM size that can run on a 16GB RAM computer is 7 billion parameters (7B).

### 📂 Step 4: Place the LLM Model in the Correct Directory
Move the downloaded LLM model to the following path:
```
Transcribe_and_Translate_Subtitles/LLM/Qwen/7B
```

### 🖥️ Step 5: Download and Place `run.py`
1. Download the `run.py` script from this repository.
2. Place it in the `Transcribe_and_Translate_Subtitles` folder.

### 📁 Step 6: Place Target Videos in the Media Folder
Place the videos you want to transcribe and translate in the following directory:
```
Transcribe_and_Translate_Subtitles/Media
```
The application will process the videos one by one.

### 🚀 Step 7: Run the Application
1. Open your preferred terminal (PyCharm, CMD, PowerShell, etc.).
2. Execute the following command to start the application:
```bash
python run.py
```
3. Once the application starts, you will see a webpage open in your browser.
   ![screenshot](https://github.com/DakeQQ/Transcribe-and-Translate-Subtitles/blob/main/screen/Screenshot%20from%202025-01-13%2000-47-34.png)

### 🛠️ Step 8: Fix Silero-VAD Error (if encountered)
On the first run, you might encounter a **Silero-VAD error**. Simply restart the application, and it should be resolved.

### 💻 Step 9: Intel and AMD Device Support
This project currently supports both **Intel-CPU-GPU-NPU** and **AMD-CPU** users.

### 🔧 Step 10: Enable Intel-GPU or Intel-NPU (Optional)
The LLM integration is based on the [ipex-llm](https://github.com/intel-analytics/ipex-llm). To use Intel-GPU or Intel-NPU, follow the instructions in the `ipex-llm` repository to enable these devices. Without this setup, the application will not work on GPU/NPU hardware.

---

## 🎉 Enjoy the Application!
```
Transcribe_and_Translate_Subtitles/Results/Subtitles
```
---

## 📌 To-Do List
- [ ] Add support for NVIDIA devices
- [ ] Add support for AMD devices
- [ ] Real-Time Translate & Trascribe Video Player

---
---
---
# 转录和翻译字幕

## 🚨 重要提示  
- **此项目仅限非商业用途！**  
- **所有任务均在本地运行，无需连接互联网，确保最大程度的隐私保护。**

---

## 📋 设置指南

### ✅ 第一步：安装依赖项  
在终端中运行以下命令来安装所需的最新 Python 包：  
```bash
pip install -r requirements.txt
```

### 📥 第二步：下载必要的模型  
1. 从 Google Drive 下载所需模型：[Transcribe_and_Translate_Subtitles](https://drive.google.com/drive/folders/1W5yqPm-FYD2r1KR7JrDwJ8jzuFALNr9O?usp=drive_link)  
2. 下载完成后，解压文件。

### 🤖 第三步：下载你喜欢的 LLM 模型  
1. 选择并下载你偏好的 LLM 模型。LLM支持: [ipex-llm](https://github.com/intel-analytics/ipex-llm)。 例如：[Qwen2.5-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct)
2. 在16GB内存的电脑上可运行的最大LLM模型为70亿参数(7B)。

### 📂 第四步：将 LLM 模型放置到正确的目录  
将下载的 LLM 模型移动到以下路径：  
```
Transcribe_and_Translate_Subtitles/LLM/Qwen/7B
```

### 🖥️ 第五步：下载并放置 `run.py`  
1. 从此项目的仓库下载 `run.py` 脚本。  
2. 将 `run.py` 放置在 `Transcribe_and_Translate_Subtitles` 文件夹中。

### 📁 第六步：将目标视频放入 Media 文件夹  
将你想要转录和翻译的视频放置在以下目录：  
```
Transcribe_and_Translate_Subtitles/Media
```
应用程序将逐个处理这些视频。

### 🚀 第七步：运行应用程序  
1. 打开你喜欢的终端工具（PyCharm、CMD、PowerShell 等）。  
2. 运行以下命令来启动应用程序：  
```bash
python run.py
```
3. 应用程序启动后，你的浏览器将自动打开一个网页。  
   ![screenshot](https://github.com/DakeQQ/Transcribe-and-Translate-Subtitles/blob/main/screen/Screenshot%20from%202025-01-13%2000-53-21.png)

### 🛠️ 第八步：修复 Silero-VAD 错误（如有）  
首次运行时，你可能会遇到 **Silero-VAD 错误**。只需重启应用程序即可解决该问题。

### 💻 第九步：支持 Intel 和 AMD 设备  
此项目目前支持 **Intel-CPU-GPU-NPU** 和 **AMD-CPU** 用户。

### 🔧 第十步：启用 Intel-GPU 或 Intel-NPU（可选）  
此项目的 LLM 集成基于 [ipex-llm](https://github.com/intel-analytics/ipex-llm)。  
若要使用 Intel-GPU 或 Intel-NPU，请按照 `ipex-llm` 仓库中的说明来启用这些设备。  
如果不进行此设置，应用程序将无法在 GPU/NPU 硬件上运行。

---

## 🎉 尽情享受应用程序吧！
```
Transcribe_and_Translate_Subtitles/Results/Subtitles
```
---

## 📌 待办事项  
- [ ] 添加对 NVIDIA 设备的支持  
- [ ] 添加对 AMD 设备的支持  
- [ ] 实现实时视频转录和翻译播放器
---
