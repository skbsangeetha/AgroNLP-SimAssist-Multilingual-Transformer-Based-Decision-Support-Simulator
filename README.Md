# AgroNLP-SimAssist

Official implementation of

**AgroNLP-SimAssist: A Multilingual Transformer-Based Decision Support Simulator for Precision Agriculture**

## Overview

AgroNLP-SimAssist is a multilingual transformer framework for agricultural question answering that jointly performs

- Disease Classification
- Advisory Recommendation
- Named Entity Recognition

using a shared mBERT encoder.

The framework supports multilingual agricultural queries in

- English
- Hindi
- Kannada

with optional translation only for low-confidence language detection or ambiguous code-mixed inputs.

---

## Repository Structure

```
dataset/
configs/
models/
train.py
evaluate.py
inference.py
requirements.txt
environment.yml
config.yaml
train_validation_test_split.csv
random_seed.txt
```

---

## Dataset

The multilingual corpus contains

- 3,200 annotated agricultural queries
- Disease labels
- Advisory labels
- BIO entity annotations

Due to licensing restrictions, PlantVillage images are not redistributed.

The repository contains

- processed text queries
- train/validation/test split
- annotation format

Dataset construction is described in the manuscript.

---

## Training

```
python train.py --config config.yaml
```

---

## Evaluation

```
python evaluate.py --config config.yaml
```

---

## Inference

```
python inference.py --text "Yellow spots on tomato leaves"
```

---

## Random Seed

All experiments were performed using

```
seed = 42
```

for complete reproducibility.

---

## Citation

If you use this repository, please cite

AgroNLP-SimAssist (BMC Plant Biology, 2026)
