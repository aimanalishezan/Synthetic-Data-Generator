Perfect! Here's the updated `README.md` including a `requirements.txt` and a detailed **Deploy Guide** for both **Colab** and **Hugging Face Spaces**.

---

# 🧠 Synthetic Data Generator

This project is an AI-powered **Synthetic Dataset Generator** built with 🤗 Transformers, BitsAndBytes, and Gradio. It takes business requirements and generates realistic datasets in various formats such as **CSV, JSON, Excel, or Tabular** using a quantized LLM (like LLaMA 3.2 8B).

![demo](https://github.com/yourusername/synthetic-data-generator/assets/demo.gif)

---

## 🚀 Features

- 🏭 Generates realistic datasets for any business domain.
- 🧠 Powered by a 4-bit quantized LLM model (LLaMA 3.2 - 8B).
- 🔥 Supports multiple output formats: CSV, JSON, Excel, Tabular.
- ⚡ Fast & efficient inference with GPU acceleration (if available).
- 🧰 Interactive Gradio UI for quick testing and usage.
- 🌐 Hugging Face token-based secure model loading.

---

## 📦 Installation

Install the necessary dependencies:

```bash
pip install -r requirements.txt
```

**`requirements.txt`:**

```txt
transformers
gradio
bitsandbytes
accelerate
torch
huggingface_hub
```

---

## 🧠 Model & Inference

This project uses a Hugging Face-hosted **quantized model** (e.g., `Llama_3.2-8B`) with 4-bit precision via `bitsandbytes` for low-memory usage.

The generation pipeline:

1. Accepts business details from the user.
2. Creates a structured prompt with required data format & record count.
3. Generates realistic data using the LLM.
4. Displays the result in the Gradio interface.

---

## 🖼️ Example Prompt

```
Business: A retail store selling luxury watches
Data Format: CSV
Records: 5
```

**Output:**
```
Item,Price,Quantity,Brand,Sale Date
Superocean IT,80000$,5,Breitling,2025-04-10
...
```

---

## 💻 Usage

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/synthetic-data-generator.git
cd synthetic-data-generator
```

### 2. Set Hugging Face Credentials

Use `userdata.get()` in Google Colab or replace with `os.environ.get()` in a Python script:

```python
from google.colab import userdata
hf_token = userdata.get("HF_TOKEN")  # Hugging Face token
model = userdata.get("model")        # Your model name (e.g. "meta-llama/Llama-3-8B-Instruct")
```

---
## Project WorkFlow

![synthetic data generator](https://github.com/user-attachments/assets/68b5101d-a439-4295-ac9c-9b2ea2198c9b)


## 🚀 Deployment Guide

### Option 1: Deploy on Google Colab

1. Open the notebook in Colab.
2. Upload your `HF_TOKEN` and `model ID` using the Colab UI or directly via `userdata`.
3. Run all cells.
4. The Gradio interface will launch with a public link.

### Option 2: Deploy on Hugging Face Spaces (Gradio App)

1. Fork this repo or create a new one.
2. Create a new Space on Hugging Face (choose **Gradio** template).
3. Upload your code, including:
   - `app.py` (main script)
   - `requirements.txt`
4. Add your `HF_TOKEN` securely in the **"Secrets"** section of the Space settings.
5. Your app will be deployed automatically and publicly accessible!

📘 **Example Space**: `https://huggingface.co/spaces/yourusername/synthetic-data-generator`

---

## 🛠 Tech Stack

| Tool           | Description                              |
|----------------|------------------------------------------|
| 🤗 Transformers| For model loading and generation         |
| 🧱 BitsAndBytes| 4-bit quantization for fast inference     |
| ⚡ Accelerate  | Model/device handling                     |
| 🔥 Gradio     | Interactive UI                            |
| 🐍 Python      | Backend scripting and logic              |

---

## ✅ TODO

- [ ] Add support for uploading schema/format file.
- [ ] Improve output formatting for Excel.
- [ ] Export dataset to downloadable files.
- [ ] Deploy on Hugging Face Spaces or Streamlit.

---

## 📜 License

MIT License. Feel free to modify and use!

---

## 🙌 Acknowledgements

- [Hugging Face](https://huggingface.co/)
- [Gradio](https://gradio.app/)
- [BitsAndBytes](https://github.com/TimDettmers/bitsandbytes)

---

Let me know if you want me to create the `app.py` file separately for Hugging Face Spaces!
