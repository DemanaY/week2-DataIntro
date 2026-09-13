# Session 2 — Intro to Data Course

This repository contains the materials for **Session 2** of *Intro to Data Course*.  
- Slides: see [`slides/`](./slides/) folder  
- Notebooks: see [`notebooks/`](./notebooks/) folder 
---
## 📑 What you need to deliver by next session:

Each group should complete the notebook [`notebooks/00_week2_RQ_data_ethics.ipynb`](./notebooks/00_week2_RQ_data_ethics.ipynb) and push the completed notebook back to the group's forked repository.

The TA team will check that every group has returned all three parts: a dataset reference, a research question, and a completed ethics checklist.

### Easiest Way: Submit using GitHub Desktop

1. On GitHub, fork this repository into your own GitHub account. Your group should agree which fork will be the group's shared submission. Introduce your group representative to us.
2. Open GitHub Desktop and select **File → Clone repository**. Choose the **GitHub.com** tab, select your fork, choose a local folder, and click **Clone**.
3. Open the cloned repository in VS Code. Edit `notebooks/00_week2_RQ_data_ethics.ipynb` and replace the placeholders with your group's research question, dataset reference, rationale, and ethics answers.
4. Save the notebook and review it from top to bottom. Make sure all eight ethics questions have an answer, or clearly say `N/A`.
5. Return to GitHub Desktop. Check the changed file, enter a summary such as `Complete group research and ethics check`, and click **Commit to main**.
6. Click **Push origin** to send the commit to your fork on GitHub.
7. Open your fork on GitHub and check that the updated notebook is visible. This is the version the TA team will review next session.


## 📑 Session Outline

1. **Quick Quiz**
   * Check loop 
2. **Group and Research Questions**
   * Groups report back
   * Discussion of the drafted research questions
3. **Data Ethics: The Pipeline View**
   * Ethical problems can enter at every stage: collection → data → analysis → model → decision → impact
   * At each stage, ask: what could go wrong?
   * Legal ≠ ethical: legal but questionable, desirable but restricted, clearly illegal
   * Case source are mostly: David Dao et al., [*Awful AI*](https://github.com/daviddao/awful-ai) — a curated list of problematic AI uses (DOI 10.5281/zenodo.5855972)
4. **Stage 1 — Collection**
   * Clearview AI: "Can we?" vs "Should we?"
   * Publicly accessible ≠ ethically unrestricted
   * Cambridge Analytica: not who provided the data, but what for
   * Consent is not a blank cheque
5. **Stage 2 — Data**
   * Who is represented? The dermatology app and its 3.5%
   * Amazon's recruitment algorithm: learning historical hiring bias
   * Bias enters even before the model: who is included, what was measured, how it was labelled
6. **Stage 3 — Analysis**
   * What can we infer about someone?
   * Sensitive attributes don't need to be in the data to be inferred
   * Predicting what someone never chose to disclose
   * Video: Leo Anthony Celi, *Data Bias is the Waterloo of Health AI*
   * Data can reveal more than it contains
7. **Stage 4 — Model**
   * Accuracy is not the whole story
   * Model A vs Model B: aggregate accuracy vs per-group performance
   * The dermatology case in numbers
   * There may be no single right answer, but the choice must be justified
8. **Stage 5 — Decision**
   * When analysis changes behaviour
   * Who benefits from the optimisation?
   * When does personalisation become manipulation?
   * Video: Tristan Harris, *How a handful of tech companies control billions of minds every day*
9. **Stage 6 — Impact**
   * Who benefits if the prediction works? Who bears the cost if it is wrong?
   * Ownership and credit: the OpenAI Navier–Stokes dispute
   * Technical vs ethical vs legal questions
   * Access ≠ permission ≠ credit
10. **A Data-Ethics Checklist**
    * One question per pipeline stage, as a working tool
11. **Your Project: The Ethics Check**
    * Eight questions applied to your own dataset
    * Provenance, representation, sensitive information, inference, benefit and harm
    * Ethics is not a final checkbox
12. **The Question to Remember**
    * Not only "Can I analyse this data?" but "What happens if I do?" and "Who bears the consequences?"
---
## 🚀 Environment Setup

Before starting, please **fork this repository** and create a fresh Python virtual environment.  
All required libraries are listed in `requirements.txt`.

> ⚠️ If you encounter errors during `pip install`, try removing the version pinning for the failing package(s) in `requirements.txt`.  
> On Apple M1/M2 systems you may also need to install additional system packages (the “M1 shizzle”).

---

### macOS / Linux (bash/zsh)

```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/Scripts/activate

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

You’re now ready to run the session notebooks!

Deactivate the environment when you’re done:
```bash
deactivate
```
