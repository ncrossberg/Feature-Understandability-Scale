# Feature Understandability Scale (FUS): Scoring Guidance

This document explains how to administer and score the two versions of the Feature Understandability Scale (FUS): one for **numerical** features (8 items) and one for **categorical** features (9 items).

**Contents**

1. [Which version to use](#which-version-to-use)
2. [Items](#items)
3. [Response coding](#response-coding)
4. [Scoring steps](#scoring-steps)
5. [Worked example: numerical scale](#worked-example-numerical-scale)
6. [Worked example: categorical scale](#worked-example-categorical-scale)
7. [Scoring code](#scoring-code)
8. [Citation](#citation)

---

## Which version to use

| Feature type | Scale | Items | Factor 1 items | Factor 2 items |
|---|---|---|---|---|
| Numerical (e.g. Credit Score, BMI) | Numerical FUS | 8 | 1-5 | 6-8 |
| Categorical (e.g. Recruitment Strategy) | Categorical FUS | 9 | 1-6 | 7-9 |

Each respondent rates **one feature at a time**. A respondent can rate several features, using the version that matches each feature's type.

The two factors are:

- **Factor 1: Understanding & Measurement.** Whether the respondent understands the feature itself and how it is measured.
- **Factor 2: Feature-Outcome Relation.** How the respondent views the feature as an input for the model's prediction.

The factor labels are for scoring only. During validation, items were presented to respondents in random order, without factor labels.

---

## Items

### Numerical scale (8 items)

| # | Factor | Item |
|---|---|---|
| 1 | Understanding & Measurement | I can understand the scale (units) of the feature. |
| 2 | Understanding & Measurement | I can easily understand if a given value of the feature is high or low. |
| 3 | Understanding & Measurement | I know what this feature measures. |
| 4 | Understanding & Measurement | I know what this feature represents. |
| 5 | Understanding & Measurement | I think that I can easily access a definition of the feature. |
| 6 | Feature-Outcome Relation | In my opinion, the feature should be used to predict the outcome. |
| 7 | Feature-Outcome Relation | I think that the feature is important for the outcome. |
| 8 | Feature-Outcome Relation | I think it is fair that the feature influences the outcome. |

### Categorical scale (9 items)

| # | Factor | Item |
|---|---|---|
| 1 | Understanding & Measurement | I can easily understand how the categories were assessed. |
| 2 | Understanding & Measurement | I can easily understand the order of categories. |
| 3 | Understanding & Measurement | I think it is feasible for me to verify the specific category of the feature. |
| 4 | Understanding & Measurement | I understand all possible values of the categorical feature. |
| 5 | Understanding & Measurement | I know what this feature represents. |
| 6 | Understanding & Measurement | I require no support to understand the feature. |
| 7 | Feature-Outcome Relation | In my opinion, the feature should be used to predict the outcome. |
| 8 | Feature-Outcome Relation | I think that the feature is important for the outcome. |
| 9 | Feature-Outcome Relation | I think it is fair that the feature influences the outcome. |

---

## Response coding

All items use a 5-point Likert scale. **No items are reverse-coded.**

| Response | Code |
|---|---|
| Strongly Disagree | 1 |
| Disagree | 2 |
| Neutral | 3 |
| Agree | 4 |
| Strongly Agree | 5 |

---

## Scoring steps

For one respondent rating one feature:

1. **Code** each response from 1 to 5 (table above).
2. **Overall understandability score** = the sum of all coded items divided by the number of items (8 for the numerical scale, 9 for the categorical scale).
3. **Factor scores** (optional) = the mean of the items belonging to each factor.
4. **Feature-level score for a user group** = the mean of the overall scores across all respondents in that group who rated the feature.

Scores range from 1 (lowest perceived understandability) to 5 (highest). The scale measures *self-reported* understanding within a given user group, so scores should only be compared across features rated by the same group.

---

## Worked example: numerical scale

> Please rate the feature "Credit Score" using the following questions. The scores of "Credit Score" range from 18.4 to 118.65. The feature is used to predict whether or not a customer's loan application will be approved. While rating the feature, consider if you would understand a loan decision, if it was justified using the feature. E.g. "The model predicted that the customer would not get a loan, with their Credit Score of 56.95 as a contributing feature."

| # | Item | Strongly Disagree (1) | Disagree (2) | Neutral (3) | Agree (4) | Strongly Agree (5) |
|---|---|:---:|:---:|:---:|:---:|:---:|
| 1 | I can understand the scale (units) of the feature. | X | | | | |
| 2 | I can easily understand if a given value of the feature is high or low. | | | | X | |
| 3 | I know what this feature measures. | | | | X | |
| 4 | I know what this feature represents. | | X | | | |
| 5 | I think that I can easily access a definition of the feature. | | | | | X |
| 6 | In my opinion, the feature should be used to predict the outcome. | | | X | | |
| 7 | I think that the feature is important for the outcome. | | | | | X |
| 8 | I think it is fair that the feature influences the outcome. | | | | X | |

**Coded responses:** 1, 4, 4, 2, 5, 3, 5, 4

| Score | Calculation | Result |
|---|---|---|
| Factor 1: Understanding & Measurement | (1 + 4 + 4 + 2 + 5) / 5 = 16 / 5 | **3.2** |
| Factor 2: Feature-Outcome Relation | (3 + 5 + 4) / 3 = 12 / 3 | **4.0** |
| Overall understandability | (16 + 12) / 8 = 28 / 8 | **3.5** |

---

## Worked example: categorical scale

> Please rate the feature "Recruitment Strategy" using the following questions. "Recruitment Strategy" takes one of three categories: "Aggressive", "Moderate" or "Conservative". The feature is used to predict whether or not a candidate will be hired. While rating the feature, consider if you would understand a hiring decision, if it was justified using the feature. E.g. "The model predicted that the candidate would not be hired, with their Recruitment Strategy of Conservative as a contributing feature."

| # | Item | Strongly Disagree (1) | Disagree (2) | Neutral (3) | Agree (4) | Strongly Agree (5) |
|---|---|:---:|:---:|:---:|:---:|:---:|
| 1 | I can easily understand how the categories were assessed. | | | | X | |
| 2 | I can easily understand the order of categories. | | | | X | |
| 3 | I think it is feasible for me to verify the specific category of the feature. | | | X | | |
| 4 | I understand all possible values of the categorical feature. | | | | | X |
| 5 | I know what this feature represents. | | | | X | |
| 6 | I require no support to understand the feature. | | | | X | |
| 7 | In my opinion, the feature should be used to predict the outcome. | | | X | | |
| 8 | I think that the feature is important for the outcome. | | | | X | |
| 9 | I think it is fair that the feature influences the outcome. | | X | | | |

**Coded responses:** 4, 4, 3, 5, 4, 4, 3, 4, 2

| Score | Calculation | Result |
|---|---|---|
| Factor 1: Understanding & Measurement | (4 + 4 + 3 + 5 + 4 + 4) / 6 = 24 / 6 | **4.0** |
| Factor 2: Feature-Outcome Relation | (3 + 4 + 2) / 3 = 9 / 3 | **3.0** |
| Overall understandability | (24 + 9) / 9 = 33 / 9 | **3.67** |

Note that the overall score (3.67) is not the average of the two factor scores (3.5), because Factor 1 has more items than Factor 2.

---

## Scoring code

Responses must be given as a list of 1-5 codes in the item order of the tables above.

```python
FACTORS = {
    "numerical": {
        "Understanding & Measurement": range(0, 5),
        "Feature-Outcome Relation": range(5, 8),
    },
    "categorical": {
        "Understanding & Measurement": range(0, 6),
        "Feature-Outcome Relation": range(6, 9),
    },
}
N_ITEMS = {"numerical": 8, "categorical": 9}


def score_fus(responses, scale):
    """Score one respondent's ratings of one feature.

    responses: list of integer codes (1-5) in item order
    scale: "numerical" or "categorical"
    """
    assert len(responses) == N_ITEMS[scale], "wrong number of items for this scale"
    assert all(1 <= r <= 5 for r in responses), "responses must be coded 1-5"

    scores = {"overall": sum(responses) / N_ITEMS[scale]}
    for name, idx in FACTORS[scale].items():
        values = [responses[i] for i in idx]
        scores[name] = sum(values) / len(values)
    return scores


# Worked examples from above
print(score_fus([1, 4, 4, 2, 5, 3, 5, 4], "numerical"))
# overall 3.5, Understanding & Measurement 3.2, Feature-Outcome Relation 4.0

print(score_fus([4, 4, 3, 5, 4, 4, 3, 4, 2], "categorical"))
# overall 3.67, Understanding & Measurement 4.0, Feature-Outcome Relation 3.0
```

---

## Citation

If you use the FUS, please cite:

Rossberg, N., Kleinberg, B., O'Sullivan, B., Longo, L., & Visentin, A. *The Feature Understandability Scale for Human-Centred Explainable AI: Assessing Tabular Feature Importance.* [add journal and DOI once available]
