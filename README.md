# EECE 5644 Assignment 4

## What this project does
This repository is about the titanic dataset which builds a decision tree model that predicts survival based on certain parameters. 

## Repository contents
| File | Description |
|---|---|
| `titanic.ipynb` | Analysis notebook |
| `titanic.csv` | Raw Titanic dataset |
| `data_dictionary.md` | Column-by-column description of the dataset |
| `findings_summary.md` | Description of machine learning model that predicts survival based on parameters |
| `requirements.txt` | Python library versions needed to reproduce this work |

## Dataset
**Titanic**: a dataset of people, with their attributes (PassengerId, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin,Embarked). The goal is to determine, given a person's attributes, would survive or not. 


## How to run
1. Clone this repository (has `titanic.csv` in it).
2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate    # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Open `titanic.ipynb` in Jupyter or VS Code.
4. Input the specific attributes for the individual
5. Run all cells from top to bottom (**Restart Kernel + Run All**) and the output will be if the individual survived or not based on their specific attributes

## Summary of findings
*(See `findings_summary.md` for the full write-up.)*