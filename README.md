## Overview

A web app that can classify how likely specific mutations in DNA are to cause diseases (variant effect prediction). Using the state-of-the-art Evo2 large language model for prediction the pathogenicity of single nucleotide variants (SNVs). Deployed on FastAPI Python backend on an H100 serverless GPU with Modal for analysis. A web app where users can select a genome assembly, browse its chromosomes or search for specific genes like BRCA1, and view the gene's reference genome sequence. The user can input a mutation in the gene and predict its pathogenicity with AI, but the user can also pick from a list of existing known variations, and compare the Evo2 prediction (pathogenic/benign) against existing ClinVar classifications. The web app is built with Next.js 15, React 19, TypeScript, Tailwind CSS, and Shadcn UI and is based off of the T3 Stack.


[•] This is on-going product expansion of Anamnes.com a Medical data analysis app I'm building...
[•] Gigabite size CSV file analysis with context window more than 1M+ rows and 20+ columns EEG analysis for Kazakova A. from Sullivanov Epilepsy Reasearch Clinic Almaty. (Waiting for Cerebras.ai response to play with LLama 4 Scout 10M context window)
[•] Create new microbiome that cure cancer... 

Features:

- 🧬 Evo2 model for variant effect prediction
- 🧬 Explore gene and variants data (NCBI ClinVar/E-utilities)
- 💻 Python backend deployed with Modal
- 🚀 FastAPI endpoint for variant analysis requests
- ⚡ GPU-accelerated (H100) variant scoring via Modal
- 📱 Responsive Next.js web interface
- 🎨 Modern UI with Tailwind CSS & Shadcn UI

## Evo2 Model

Check out the paper behind the model.

- [Paper](https://www.biorxiv.org/content/10.1101/2025.02.18.638918v1)
- [GitHub Repository](https://github.com/ArcInstitute/evo2)

## Setup

Follow these steps to install and set up the project.

### Clone the Repository

```bash
git clone --recurse-submodules https://github.com/Andreaswt/variant-analysis-evo2.git
```

### Install Python

Download and install Python if not already installed. Use the link below for guidance on installation:
[Python Download](https://www.python.org/downloads/)

Create a virtual environment for each folder, except elevenlabs-clone-frontend, with **Python 3.10**.

### Backend

Navigate to backend folder:

```bash
cd evo2-backend
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Modal setup:

```bash
modal setup
```

Run on Modal:

```bash
modal run main.py
```

Deploy backend:

```bash
modal deploy main.py
```

### Frontend

Install dependencies:

```bash
cd evo2-frontend
npm i
```

Run:

```bash
npm run dev
```
