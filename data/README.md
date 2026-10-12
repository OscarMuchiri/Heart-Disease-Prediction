# Dataset Setup

The notebook expects the following local file:

```text
data/heart_disease_uci.csv
```

## Expected schema

The CSV used by the original notebook contains these fields:

```text
id
age
sex
dataset
cp
trestbps
chol
fbs
restecg
thalch
exang
oldpeak
slope
ca
thal
num
```

## Source and attribution

The coursework dataset is based on the **UCI Heart Disease** collections associated with Cleveland, Hungary, Switzerland, and VA Long Beach.

UCI Machine Learning Repository:
https://archive.ics.uci.edu/dataset/45/heart+disease

DOI:
https://doi.org/10.24432/C52P4X

UCI currently lists the underlying dataset under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

The exact assembled CSV used in the original coursework is not redistributed here so that its specific provenance can be preserved and documented accurately before publication.

## Target

The notebook converts the original `num` field into a binary target:

- `0`: no heart disease
- `1`: heart disease present, where the original `num > 0`
