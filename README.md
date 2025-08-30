# SHROOM-Guard Hallucination Detection - Final Model

![Macro F1 Score](https://img.shields.io/badge/Final_Macro_F1_Score-0.7410-brightgreen)

This repository contains the final, consolidated code and methodology for our submission to the **SHROOM-Guard Challenge ESYA '25**. The project, developed by Yash Kamra and Aryaman Kapur (Team Ozero), details the creation of a robust, model-agnostic system for detecting AI-generated hallucinations.

The entire workflow—from data loading and feature engineering to model training, evaluation, and visualization—is contained within the main Jupyter Notebook: **`Final_Report.ipynb`**.

Our final system is a **Unified Hybrid Model** that uses a tuned LightGBM classifier. It achieved a **Macro F1 Score of 0.7410** on the official, unseen `test.model-agnostic.json` data.

---

## Final Performance on Test Data

| Metric          | Precision | Recall | F1-Score |
|-----------------|-----------|--------|----------|
| **Hallucination**   | 0.70      | 0.68   | 0.69     |
| **Not Hallucination** | 0.78      | 0.80   | 0.79     |
| **Macro Avg**       | **0.74**      | **0.74**   | **0.74**     |
| **Accuracy**|     |                                |{**0.75**} |

---

## Project Structure


---

### Step 2: Set Up the Conda Environment

Open your terminal or Anaconda Prompt and run the following commands.

```bash
# 1. Create a new Conda environment
conda create -n hallucination_env python=3.9 -y

# 2. Activate the environment
conda activate hallucination_env

# 3. Install all required libraries from the requirements file
pip install -r requirements.txt

# 4. Download necessary NLP models for spaCy and NLTK
python -m spacy download en_core_web_sm
python -c "import nltk; nltk.download('stopwords')"
## How to Reproduce the Final Result (Step-by-Step)

Follow these instructions exactly to set up the environment and run the code.

### Step 1: Create and Populate `requirements.txt`

Create a file named `requirements.txt` in the main project directory and paste the following content into it:

The project is organized around a central notebook and a few helper modules.
