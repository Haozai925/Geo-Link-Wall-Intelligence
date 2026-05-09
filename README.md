# Geo-Link Wall Intelligence (GLWI)

🚧 **Status: Active Development / Private Core Modules**

GLWI is an LLM-driven Multi-Agent framework designed to automate the geotechnical analysis and PLAXIS finite element modeling for ultra-deep diaphragm walls, specifically targeting the pressure hardening mechanism of joint mud skins.

## 📌 Project Background
This project was initiated to optimize the foundation pit stability analysis for mega-infrastructure projects (e.g., Zhangjinggao Yangtze River Bridge south anchorage). Traditional manual parameter tuning in PLAXIS 3D is time-consuming and often fails to accurately map experimental benchmark data (such as Cui Jianfeng's test results) to numerical simulations.

## ⚙️ Core Architecture
GLWI utilizes a multi-agent orchestration approach (powered by OpenClaw/Claude/DeepSeek):
- **DataExtraction Agent:** Processes unstructured geotechnical reports (PDFs) and lab test data (e.g., RJP pile return slurry titration tests) to extract core mechanical indices.
- **Reasoning Agent:** Employs Chain-of-Thought (CoT) to deduce interface reduction factors based on mud skin thickness variations.
- **CodeGeneration Agent:** Translates the reasoned parameters into executable PLAXIS 3D Python API scripts.
- **Validation Agent:** Automatically compares FEM results against empirical benchmark data to form a self-healing iteration loop.

## 📊 Token Usage & Scalability
Due to the necessity of handling long-context geological reports (>100k tokens per run) and multi-turn iterative reasoning, the system operates with high token throughput. We are currently scaling the framework to handle multi-pile interlocking simulations.

---
*Note: The core reasoning prompts and proprietary dataset scripts are currently kept private due to ongoing academic research and project confidentiality. Only the interface API and framework documentation are publicly documented here.*
