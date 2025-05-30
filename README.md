# Text2Video-Text2Video-Audio
**Text2Video &amp; Text2Video+Audio**: This project converts text prompts into dynamic video using the CogVideoX-2b model. It also adds audio narration via gTTS, enabling complete audiovisual storytelling from a single input. Ideal for AI-driven content creation, storytelling, education, and multimedia projects.

# 🎥 CogVideoX Text-to-Video + Audio Narration

This project demonstrates how to generate **realistic videos from text prompts** using the [CogVideoX-2b](https://huggingface.co/THUDM/CogVideoX-2b) model, along with **voice narration** using Google Text-to-Speech (`gTTS`). It is designed to run on **Google Colab**, even with limited GPU memory.

---

## 🔍 Overview

- 🌐 **Text Prompt → Video** using CogVideoX
- 🔊 **Narration** added using `gTTS`
- 🎬 **Final Output**: A narrated video, generated from your input prompt
- 🧠 Works with low VRAM by enabling memory-efficient techniques (slower but compatible)

---

## 🚀 How It Works

1. **Prompt Input**: Provide a descriptive sentence about the scene.
2. **Model Loading**: Load CogVideoX-2b modules: `text_encoder`, `transformer`, and `VAE`.
3. **Video Generation**: Generate a sequence of frames based on the prompt.
4. **Narration**: Convert the prompt into speech using `gTTS`.
5. **Final Composition**: Combine the generated video and audio using `MoviePy`.

---

 ##**Notes
float16 is used instead of bfloat16 due to limited GPU support (Turing architecture).

Sequential CPU offloading allows CogVideoX to run on Colab, but generation may be slow (30–60 minutes per video).

For better speed and quality, use Ampere or newer GPUs.**

📦 Output Example
Prompt:
"A brown dog runs energetically after a gray cat on a grassy path..."

Output:
A generated .mp4 video with synchronized voice narration.

## 🛠️ Setup

Run the project in **Google Colab** with the following dependencies:

```bash
pip install diffusers transformers accelerate moviepy gtts

##📁 Files
| File               | Description                                        |
| ------------------ | -------------------------------------------------- |
| `main.ipynb`       | Colab-compatible notebook to run the full pipeline |
| `final_output.mp4` | Sample generated video (if uploaded)               |
| `narration.mp3`    | Audio generated using gTTS                         |

✨ Future Work
Add GUI/Gradio interface for easier prompt input

Support batch video generation

Explore multi-language narration with gTTS

🙌 Credits
THUDM/CogVideoX
Hugging Face Diffusers
Google TTS (gTTS)
MoviePy

