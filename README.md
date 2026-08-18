# 🧪 Molecular Generation with Generative Models

> **Comparative study of generative approaches for molecular generation using Deep Learning and cheminformatics.**

## 🎯 Overview

This project explores and compares different computational approaches for **generating novel molecular structures**, combining generative deep learning techniques with molecular representation and validation tools.

The study investigates different architectures for molecular generation, including **Generative Adversarial Networks (GANs), Variational Autoencoders (VAEs) and Graph Neural Networks (GNNs)**.

Generated molecules are evaluated using three key metrics commonly used in molecular generation research:

- **Validity** — whether generated structures represent chemically valid molecules
- **Uniqueness** — diversity among generated molecules
- **Novelty** — whether generated molecules differ from those present in the training dataset

This project was originally developed as my **Undergraduate Thesis in Computer Engineering at Universidade Federal de São Carlos (UFSCar)**.

---

## 🧠 Research Problem

Generative models have the potential to explore large chemical spaces and generate new molecular structures computationally.

However, generating molecules involves more than simply producing new samples. A useful generative model should ideally generate molecules that are:

**Chemically Valid → Diverse → Novel**

Different generative architectures may perform differently across these dimensions.

The main goal of this project is therefore to **compare different molecular generation approaches and evaluate their performance using standardized metrics**.

---

## 🤖 Approaches Explored

### 🔵 Generative Adversarial Networks (GANs)

GANs use two competing neural networks:

- **Generator** — creates new candidate molecular representations
- **Discriminator** — attempts to distinguish generated samples from real ones

Through adversarial training, the generator progressively learns to produce samples closer to the training distribution.

---

### 🟣 Variational Autoencoders (VAEs)

VAEs learn a continuous latent representation of molecular structures.

The model consists primarily of:

**Encoder → Latent Space → Decoder**

Once the latent representation has been learned, new points can be sampled from the latent space and decoded into candidate molecules.

---

### 🟢 Graph Neural Networks (GNNs)

Molecules can naturally be represented as graphs:

- **Nodes → atoms**
- **Edges → chemical bonds**

Graph Neural Networks can therefore model molecular topology directly instead of relying exclusively on sequential representations.

This approach allows structural relationships between atoms to become part of the learning process.

---

## 📊 Evaluation Metrics

The generated molecular sets are evaluated using three main metrics:

| Metric | What it measures |
|---|---|
| **Validity** | Percentage of generated structures that correspond to valid molecules |
| **Uniqueness** | Percentage of distinct molecules among valid generated samples |
| **Novelty** | Percentage of generated molecules not present in the training dataset |

Together, these metrics help evaluate whether a model is capable of generating molecules that are not only valid, but also **diverse and previously unseen**.

---

## 🧬 Molecular Representation & Processing

Molecular structures are processed using **RDKit**, an open-source cheminformatics toolkit.

The project explores molecular datasets and representations derived from sources such as:

- ChEMBL
- PubChem
- ZINC

Depending on the experiment, molecular information can be represented through structures such as **SMILES strings or molecular graphs**.

---

## 🛠️ Tech Stack

### Machine Learning

`PyTorch` · `PyTorch Geometric`

### Cheminformatics

`RDKit`

### Data Analysis

`Python` · `Pandas` · `NumPy`

### Visualization

`Matplotlib`

### Development

`Google Colab` · `Jupyter Notebook`

---

## 🔬 Experimental Workflow

The general experimental pipeline follows:

```text
Molecular Dataset
        ↓
Data Preprocessing
        ↓
Molecular Representation
        ↓
Generative Model
        ↓
Molecule Generation
        ↓
Chemical Validation
        ↓
Validity · Uniqueness · Novelty
        ↓
Model Comparison
```

This workflow makes it possible to compare different generative approaches under a common evaluation framework.

---

## 📈 Results

The experiments evaluate the trade-offs between the three main objectives:

### Validity

Measures whether the model is capable of learning the structural constraints necessary to produce valid molecular representations.

### Uniqueness

Measures the diversity of generated molecules and helps identify problems such as repeatedly generating similar structures.

### Novelty

Evaluates whether the model can generate structures that were not already present in the training dataset.

The comparison between these metrics helps highlight an important challenge in generative modeling:

> **Generating valid molecules is not enough — a useful model should also generate diverse and novel structures.**

Detailed experimental results and implementations are available in the project notebooks.

---

## 📁 Repository Structure

```text
molecular-generation-models/
│
├── notebooks / experiments
│   └── Molecular generation experiments
│
├── requirements.txt
│
└── README.md
```

> The repository contains the experimental implementations used to train, generate and evaluate molecular structures across different modeling approaches.

---

## 🚀 Running the Project

Clone the repository:

```bash
git clone https://github.com/felipetorrieri/molecular-generation-models.git
```

Enter the project directory:

```bash
cd molecular-generation-models
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

The experiments can then be executed using **Jupyter Notebook or Google Colab**.

> Some experiments may require additional configuration depending on the PyTorch, CUDA and PyTorch Geometric versions used.

---

## 🎓 Academic Context

This project was originally developed as my **Undergraduate Thesis in Computer Engineering at Universidade Federal de São Carlos (UFSCar)**.

### Thesis

**Análise comparativa de desempenho da geração de conjuntos de moléculas utilizando redes generativas adversárias e outros métodos**

The research investigated and compared computational approaches for molecular generation, focusing on their ability to produce **valid, unique and novel molecular structures**.

---

## 💡 What This Project Demonstrates

This project showcases experience with:

- 🧠 Generative Machine Learning
- 🧪 Molecular data processing
- 🕸️ Graph-based machine learning
- 🔬 Experimental model comparison
- 📊 Model evaluation and performance metrics
- 🐍 Python development
- 🔥 PyTorch
- 🧬 RDKit
- 📓 Reproducible experimentation with Jupyter / Google Colab

It also demonstrates the ability to move from a **research question to implementation, experimentation, evaluation and comparative analysis**.

---

## 👤 Author

**Felipe Torrieri**

Computer Engineering · Business Intelligence · Data Analytics

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/felipetorrieri/)

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/felipetorrieri)
