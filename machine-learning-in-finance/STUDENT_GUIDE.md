# Student Guide

## How to use this e-class

### 1. Begin with the weekly README

Open the relevant weekly folder from the Course Map. The weekly README is the authoritative navigation page for that session.

### 2. Download or open the lecture material

Use the PPTX when you want an editable presentation file. Use the PDF when you want a stable reading copy. The lecture slides explain the concept, mathematics, algorithm, code, results, and financial interpretation.

### 3. Run the laboratory notebook

Each notebook is designed for Google Colab.

1. Open the notebook file.
2. Select Open in Colab, or upload the notebook to Google Colab.
3. Run the setup cells first.
4. Read the markdown explanation before executing each code block.
5. Record your own observations and results.

### 4. Use the Python script for revision

The supporting .py file contains the main implementation in a form that can be run locally or inspected in an editor such as VS Code.

### 5. Complete the exercise

The exercise extends the laboratory work. Students should keep the notebook organised, explain modelling choices, report relevant metrics, and interpret results in financial terms.

## Recommended local setup

~~~bash
python -m venv .venv
source .venv/bin/activate        # macOS/Linux
.venv\Scripts\activate           # Windows
python -m pip install -r requirements.txt
~~~

The weekly material will identify any additional package needed for that session.

## File naming

Use clear names that preserve the course sequence:

~~~text
week-05-logistic-regression.pptx
week-05-logistic-regression-lab.ipynb
week-05-logistic-regression.py
week-05-exercise.ipynb
~~~

## Reproducibility checklist

Before submitting or sharing work:

- Restart the notebook and run all cells from top to bottom.
- Keep random seeds fixed where appropriate.
- Check that file paths work from a clean environment.
- Explain missing-value, encoding, scaling, and feature decisions.
- Check for target leakage.
- Report the evaluation sample and metric definitions.
- Separate model performance from financial interpretation.
- Cite datasets, publications, and external code.

## Responsible AI use

AI assistants may help students understand an error, improve documentation, or explore an alternative implementation. Students must be able to explain all submitted code and results and must acknowledge external assistance where required by course instructions.

## Support path

If a notebook does not run:

1. Read the error message and identify the failing cell.
2. Confirm that the setup cell ran successfully.
3. Check the Python and package versions.
4. Compare the notebook with the supporting .py file.
5. Raise a focused question with the week, cell, error, and attempted fix.
