# 📰 Website Brochure Notebook

This repository contains a **Jupyter Notebook** that uses **[Ollama Llama 3.2](https://ollama.ai/)** to generate a brochure-like summary of any website.

Just provide a URL, and the notebook will:

* 📝 Summarize the site’s key information
* 📰 Fetch and display the latest related news
* 🖼️ Extract and show the website’s logo

---

## 🚀 How to Use

1. Clone this repository:

   ```bash
   git clone https://github.com/eGKEL/AI_Brochure_With_Llama
   ```

2. Install the required dependencies:

   ```bash
   !pip install os requests beautifulsoup4 ollama gradio
   ```

3. Make sure you have [Ollama](https://ollama.ai/download) installed and the `llama3.2` model:

   ```bash
   ollama pull llama3.2
   ```

4. Open the notebook:

   ```bash
   jupyter notebook brochure_generator.ipynb
   ```

5. Run all cells and enter a website URL when prompted.

---

## 📂 Files

* `brochure_generator.ipynb` – the main notebook
* `requirements.txt` – Python dependencies

---

## 🧩 Requirements

The notebook requires the following Python packages:

```
os
requests
beautifulsoup4
ollama
gradio
```

---

## 📜 License

This project is licensed under the MIT License.
