## Overview

A web app that can classify how likely specific mutations in DNA are to cause diseases (variant effect prediction). Using the state-of-the-art Evo2 large language model for prediction the pathogenicity of single nucleotide variants (SNVs). Deployed on FastAPI Python backend on an H100 serverless GPU with Modal for analysis. A web app where users can select a genome assembly, browse its chromosomes or search for specific genes like BRCA1, and view the gene's reference genome sequence. The user can input a mutation in the gene and predict its pathogenicity with AI, but the user can also pick from a list of existing known variations, and compare the Evo2 prediction (pathogenic/benign) against existing ClinVar classifications. 


### Features:

🧬 Evo2 Genome modeling and design across all domains of life
<br>🔬 Explore gene and variants data (NCBI ClinVar/E-utilities)
<br>🟢 Python backend deployed with Modal
<br>👋 FastAPI endpoint
<br>⚡ GPU-accelerated (H100) variant scoring via Modal
<br> 📱 Responsive Next.js 15, React 19 and is based off of the T3 Stack.
<br> 🎨 Modern UI with Tailwind CSS, and Shadcn UI

### Todo

[🚧] This is on-going project to add for internal use for [Anamnesai.com](https://anamnesai.com) a Medical data analysis app that I'm currently building...<br>
[•] Gigabite size CSV file analysis with context window more than 1M+ rows and 20+ columns EEG analysis for K. Anna from [Epilepsy Reasearch Clinic Almaty](klinikasavinova.kz).(Waiting for proper open source model with 10M+ context window to test 880MB cvs with EEG raw data)<br>
[•] Collabrate with Atyrau biodoc ... 

## Evo2 Model

Check out the paper behind the model.

- [Paper](https://www.biorxiv.org/content/10.1101/2025.02.18.638918v1)
- [GitHub Repository](https://github.com/ArcInstitute/evo2)

## Setup

Follow these steps to install and set up the project.

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
npm install
```

Run:

```bash
npm run dev
```
