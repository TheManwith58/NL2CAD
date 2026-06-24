#  NL2CAD: Natural Language to Computer-Aided Design

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/[YourUsername]/[YourRepo]/issues)

**NL2CAD** is an AI-powered tool that translates natural language text prompts into functional 3D CAD models. By leveraging Large Language Models (LLMs) and programmatic CAD environments, it allows users to generate, modify, and iterate on mechanical parts and 3D designs using plain English.

---

##  Features

* **Text-to-CAD Generation:** Describe a part (e.g., *"A 50x50mm mounting bracket with 4 corner screw holes"*), and get a valid CAD file.
* **Iterative Design:** Modify existing generated models using follow-up text prompts.
* **Multi-Format Export:** Supports exporting designs as `.[stl/obj/step]` files for 3D printing or further engineering.
* **Programmatic Backend:** Powered by `[OpenSCAD / FreeCAD / CadQuery]` scripts generated via LLMs.

## How It Works

1. **Input:** The user provides a text description.
2. **LLM Processing:** The text is parsed and converted into programmatic CAD code (e.g., Python CadQuery scripts or OpenSCAD modules) using `[OpenAI API / Local LLaMA / Claude]`.
3. **Rendering:** The generated code is compiled by the CAD engine to create a 3D mesh.
4. **Output:** The rendered 3D model is displayed and made available for download.

---

##  Installation

### Prerequisites
* Python 3.8 or higher
* `[OpenSCAD / FreeCAD]` installed on your system (if using a local engine)
* `[OpenAI API Key]` (or equivalent for your LLM backend)

### Setup Instructions

1. **Clone the repository:**
   `git clone https://github.com/[YourUsername]/NL2CAD.git`
   `cd NL2CAD`

2. **Create a virtual environment:**
   `python -m venv venv`
   `source venv/bin/activate`  *(On Windows use `venv\Scripts\activate`)*

3. **Install dependencies:**
   `pip install -r requirements.txt`

4. **Set your environment variables:**
   Create a `.env` file in the root directory and add your API keys:
   `LLM_API_KEY=your_api_key_here`

---

##  Usage

### Running the Web Interface
If you have a frontend (like Streamlit or Gradio), start it by running:
`python app.py`

Then, open your browser and navigate to `http://localhost:8501`.

### Command Line Interface (CLI)
You can also generate models directly from the terminal:
`python generate.py --prompt "A simple coffee mug with a thick handle" --output mug.stl`

---

##  Architecture / Tech Stack

* **Frontend:** `[Streamlit / Gradio / React]`
* **Backend:** `[FastAPI / Flask]`
* **LLM Integration:** `[LangChain / OpenAI / HuggingFace]`
* **CAD Engine:** `[CadQuery / OpenSCAD / Build123d]`

---

## 🛣️ Roadmap

- [x] Basic text-to-script generation.
- [x] Integration with local CAD compiler.
- [ ] Add support for complex assemblies (multi-part generation).
- [ ] Implement visual feedback loop (LLM self-correction based on render).
- [ ] Support for parametric adjustments via sliders.

---

##  Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

---

