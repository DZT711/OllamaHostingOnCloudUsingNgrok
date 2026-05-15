# 🚀 Ollama Colab Manager & Hosting

This project provides a powerful, interactive way to run and host **Ollama** on Google Colab using **Ngrok** for external access. It includes a custom-built Model Manager to easily browse, pull, and delete models from multiple providers.

---

## 🌟 Features

- **One-Click Setup:** Automatically installs Ollama and configures the environment for Google Colab.
- **Ngrok Integration:** Publicly host your Ollama server so you can access it from your local machine or other applications.
- **Interactive Model Manager:** A user-friendly UI inside the notebook to manage your models.
- **Multi-Provider Support:** Fetch models from:
  - **Ollama Library** (Official)
  - **Hugging Face** (GGUF Models)
  - **LM Studio** (Community Publishers)
- **GPU Optimized:** Designed to leverage Google Colab's T4, L4, or A100 GPUs for fast inference.

---

## 📊 Statistics & Model Capacity

The **Advanced Model Manager** provides access to a massive library of AI models. Here is the current capacity:

| Provider | Approx. Models | Download Support | Compatibility |
| :--- | :--- | :--- | :--- |
| **🦙 Ollama Library** | **230+** | 100% | Native / Guaranteed |
| **🧠 LM Studio Publishers** | **2,100+** | Varies | GGUF Verified |
| **🤗 Hugging Face** | **1,000+** | Varies | GGUF / Experimental |
| **TOTAL** | **3,300+** | **Discovery list** | |

*Note: While thousands of models are discoverable, automated download support varies for community-provided models (Hugging Face & LM Studio). The "Compatibility Score" in the manager helps you identify models most likely to run smoothly on your setup.*

---

## 📋 Prerequisites

1.  **Google Account:** To use Google Colab.
2.  **Ngrok Account:** Sign up at [ngrok.com](https://ngrok.com/) to get your free Authtoken.

---

## 🚀 Step-by-Step Guide

### Step 0: Enable GPU in Colab
For the best performance, you **must** use a GPU.
1.  Open the notebook in Google Colab.
2.  Go to **Runtime** > **Change runtime type**.
3.  Under **Hardware accelerator**, select **T4 GPU** (or better).
4.  Click **Save**.

### Step 1: System Setup
Locate the cell labeled **"Step 1: System Setup & Ollama Installation"**.
- Replace `YOUR_NGROK_AUTH_TOKEN` with your actual token from the [Ngrok Dashboard](https://dashboard.ngrok.com/get-started/your-authtoken).
- Run the cell. This will install Ollama, start the server, and provide you with a **Public Ngrok URL**.

### Step 2: Install Python Dependencies
Locate the cell labeled **"Step 2: Install Python Dependencies"**.
- Run this cell to install the necessary libraries for the Model Manager UI.

### Step 3: Choose Your Model Manager
You should only run **one** of the following manager cells depending on your needs:

| Version | Cell Number | Description |
| :--- | :--- | :--- |
| **Advanced (Largest)** | **Step 3** | **Recommended.** Fetches from Ollama, Hugging Face, and LM Studio. Offers the widest variety of models. |
| **Enhanced** | **Step 4** | Focuses on Ollama and Hugging Face GGUF models. |
| **Safe (Stable)** | **Step 5** | **Most Stable.** Only fetches models from the official Ollama library. Guarantees 100% compatibility. |

---

## 🛠️ How to Use the Manager

Once you run your chosen Manager cell, an interactive UI will appear with the following commands:

- **Type a Number (e.g., `1`):** Pulls the model corresponding to that ID in the list.
- **`delete 101`:** Deletes the installed model with ID 101.
- **`info 1`:** Shows detailed information about model ID 1.
- **`page 5`:** Jumps to page 5 of the model list.
- **`refresh`:** Reloads the model lists from all providers.
- **`0`:** Starts the Ngrok tunnel (if not already running).
- **`stop ngrok` / `stop server`:** Controls for the background processes.

---

## 🧠 Understanding Model Providers

### 1. Ollama Library (Official) - *The "Safe" Choice*
- **Pros:** Extremely stable, guaranteed to work, optimized for Ollama.
- **Cons:** Limited selection compared to the broader community.

### 2. Hugging Face (GGUF) - *The "Vast" Choice*
- **Pros:** Access to thousands of community-uploaded models, latest research, and specialized fine-tunes.
- **Cons:** "Unsafe" - Some models might have complex configurations or may not be fully compatible with the automated download script.

### 3. LM Studio Publishers
- **Pros:** High-quality quants from reliable community members like `bartowski` or `TheBloke`.
- **Cons:** Similar to Hugging Face, compatibility can vary.

---

## ⚠️ Important Notes

- **One Version Only:** Do not run Step 3, 4, and 5 simultaneously. Pick the one that fits your needs.
- **Stay Active:** Google Colab will disconnect if the browser tab is closed or if there is no activity for a long time.
- **Disk Space:** Large models (70B+) can quickly fill up Colab's temporary storage. Monitor your disk usage!

---

## 🤝 Contributing
Feel free to fork this project and submit pull requests for any improvements or bug fixes!
