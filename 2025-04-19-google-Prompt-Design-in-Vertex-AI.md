---
title: "Mastering Generative AI with Vertex AI Studio & Gemini API"
date: 2025-04-19
categories: [blog, ai, vertex-ai, gemini, gcp]
description: A hands-on journey through Google Cloud's Vertex AI Studio and Gemini API exploring prompt engineering, multimodal generation, and AI integration with Python.
---

# 🚀 Mastering Generative AI with Vertex AI Studio & Gemini API

My learning journey through the **“Get Started with Vertex AI Studio”** and **“Getting Started with the Gemini API in Vertex AI”** courses on Google Cloud Skills Boost. These labs introduced me to powerful tools for building **generative AI** applications, leveraging **Gemini models** inside **Vertex AI Studio and Workbench**.

---

## 🔍 What I Learned

- ✅ Designing high-quality prompts
- 🖼️ Using multimodal inputs (text, images, video)
- ⚡ Working with the Gemini 2.0 Flash model
- 🔁 Streaming responses
- 🔐 Analyzing and configuring safety filters
- 💻 Generating code, chat, and creative content dynamically

---

## 🧪 Vertex AI Studio Labs: Prompt Design & Multimodal Generation

**Vertex AI Studio** offers a simple way to test prompt ideas with Gemini models. Here's what I explored:

### ✅ Prompt Engineering
- Generated product **descriptions** and **taglines**
- Tuned tone, audience, and intent
- Exported prompts to Python notebooks

### 🖼️ Multimodal Inputs
- Used product images to generate emotional descriptions
- Customized templates with image + text inputs
- Built a tagline generator with tone control (e.g., *empowering*, *connected*)

### 🧬 Code Export to Notebook
- Exported prompt designs into **Vertex AI Workbench**
- Modified system prompts using Python for fine-tuned control

---

## 🧠 Using Gemini API via Vertex AI SDK

I transitioned from the UI to **Python SDK** inside **Vertex AI Workbench**.

### ⚡ Gemini 2.0 Flash Model
A fast, lightweight model perfect for:
- Natural language tasks
- Code generation
- Chat-based multi-turn conversations

```python
from vertexai.preview.generative_models import GenerativeModel

model = GenerativeModel("gemini-2.0-flash")
response = model.generate_content("Explain quantum computing in simple terms.")
print(response.text)


### 🔁 Streaming Responses
- Enabled real-time output by streaming chunks of generated content:
```python
for chunk in model.generate_content_stream("Write a story about AI and humanity."):
    print(chunk.text, end="")
```

### 🔐 Safety Filters
- Inspected and configured Gemini’s **safety filters**
- Verified content categories (e.g., violence, hate, sexual content)
- Adjusted safety settings depending on use case

---

## 🧩 Multimodal Magic with Gemini: Text, Images, and Video

### 🖼️ Text + Image Prompts
- Uploaded an image of a landscape and asked the model to generate poetic descriptions
- Used **multiple image inputs** for **few-shot prompting**

### 🎬 Text from Video
- Passed video input to generate:
  - Summaries
  - Event detection
  - Scene analysis

### 🌐 Web Media Analysis
- Ran the model on **publicly available media URLs**
- Extracted trends and insights in real time

---

## 🧰 Tech Stack & Tools Used

- **Google Cloud Vertex AI Studio**
- **Gemini 2.0 Flash** Model
- **Vertex AI Python SDK**
- **Jupyter Notebook in Workbench**
- Python 3 Kernel (recommended)

---

## 📚 Key Takeaways

- **Prompt engineering** is essential for quality outputs.
- Gemini 2.0 Flash delivers **speed** and **multimodal capability** with sub-second latency.
- Streaming responses and safety filters offer **customization** and **real-time control**.
- Working with **images and videos** opens creative use cases for marketing, education, and media analytics.

---

## 📁 Repo Tip (If you're adding this blog to a GitHub repo)

Consider structuring your learning like this:

```
/gemini-vertex-ai-course/
│
├── 📓 notebooks/
│   ├── prompt_design.ipynb
│   ├── multimodal_image_analysis.ipynb
│   ├── gemini_api_text_and_video.ipynb
│
├── 🧠 README.md (summary of the project)
├── 📘 blog.md ← (this file)
└── requirements.txt
```

You can add this blog as `blog.md` and reference it from your `README.md` like:

```markdown
📖 [Read the full blog summary](./blog.md)
```

---

## 🙌 Final Thoughts

These labs helped me **build a foundation** in generative AI and prompted me to experiment with Gemini's capabilities far beyond simple text generation.

If you're exploring AI on **Google Cloud**, these modules are a fantastic starting point.

---

**📎 Resources:**
- [Vertex AI Studio Documentation](https://cloud.google.com/vertex-ai/docs/generative-ai/overview)
- [Gemini API Reference](https://cloud.google.com/vertex-ai/docs/generative-ai/model-reference/gemini)
- [Google Cloud Skills Boost Labs](https://www.cloudskillsboost.google)

---
