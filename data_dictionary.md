# Data Dictionary — Titanic Survival (Cleaned)

(891 rows, 10 columns — after dropping `PassengerId`, `Name`, `Ticket`, `Cabin`, filling in missing values for `Age`/`Embarked`, and label-encoding `Sex`/`Embarked`)

| Column | Type | Values | Description |
|---|---|---|---|
| `Survived` | int64 (binary) | 0 / 1 | **Target variable.** Whether the passenger survived (1) or did not (0). |
| `Pclass` | int64  | 1 / 2 / 3 | Ticket class: 1st, 2nd, or 3rd.  **Predictor.** |
| `Sex` | str | `female` / `male` | Passenger's sex. |
| `Age` | float64 (continuous) | 0.42–80.0 | Passenger's age in years. 177 missing values filled with the column median. **Predictor.** |
| `SibSp` | int64 (discrete) | 0–8 | Number of siblings/spouses aboard with the passenger. **Predictor.** |
| `Parch` | int64 (discrete) | 0–6 | Number of parents/children aboard with the passenger. **Predictor.** |
| `Fare` | float64 (continuous) | 0.0–512.33 | Ticket fare paid. **Predictor.** |
| `Embarked` | str | `C` / `Q` / `S` | Port of embarkation. 2 missing values filled with the most popular value (`S`). |
| `Sex_number` | int64 (binary) | 0 / 1 | `Sex` label-encoded for the model: 0 = female, 1 = male. **Predictor.** |
| `Embarked_number` | int64 (categorical) | 0 / 1 / 2 | `Embarked` label-encoded for the model: 0 = C, 1 = Q, 2 = S. **Predictor.** |

## Columns dropped during cleaning (and why)

| Column | Reason dropped |
|---|---|
| `PassengerId` | Row index. |
| `Name` | Unique text, 891 unique values (one per passenger) and not usable in raw form. |
| `Ticket` | Text, 681 unique values, no clean structure. |
| `Cabin` | 687 of 891 rows (77%) missing and was too sparse to use directly. |

## Predictors used in the Decision Tree model (`X` / `inputs`)

```
Pclass, Age, SibSp, Parch, Fare, Sex_number, Embarked_number
```

## Target variable (`y` / `target`)

```
Survived
```