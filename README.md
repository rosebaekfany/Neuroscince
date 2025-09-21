# Neuroscince

## Analysis of HMAX Model for Object Recognition and Confidence Evaluation

This repository contains the analysis of the **HMAX model**, a biologically inspired vision model, applied to an **object recognition task** (animal vs. non-animal). The project also explores **confidence metrics** for classifier reliability and compares computational models with human psychophysics data.

---

## 📌 Overview

* **Biological Motivation**: Inspired by the human visual cortex’s ventral stream (*“what pathway”*), the HMAX model processes images hierarchically from simple edges (S1) to complex object representations (C2).
* **Research Goals**:

  * Investigate the performance of HMAX features for object recognition.
  * Compare classifiers (**SVM** and **MLP**) trained on HMAX-extracted features.
  * Analyze **confidence metrics** for decision reliability.
  * Benchmark against **human behavioral data** (reaction time, accuracy, and self-reported confidence).

---

## 🧪 Experiments

1. **Behavioral Study**:

   * Human subjects classified **animal vs. non-animal** images.
   * Recorded **performance, reaction time (RT), and confidence**.
   * Tested on normal, noisy, and rotated images.

2. **Computational Models**:

   * Extracted features from the **HMAX model** (C2 layer).
   * Trained two classifiers:

     * **Support Vector Machine (SVM)**
     * **Multi-Layer Perceptron (MLP)**
   * Evaluated performance and **confidence scores**.

3. **Dataset**:

   * 1,200 grayscale images (256×256 px).
   * Balanced classes: **600 animals** (head, near-body, medium, far) and **600 non-animals** (natural/artificial scenes).
   * Split into training and test sets.

---

## 📊 Results

* **Human Participants**:

  * Higher accuracy and confidence for **head/near-body views**.
  * Accuracy dropped with noisy and rotated stimuli.

* **SVM Classifier**:

  * Test accuracy: \~76.5%
  * AUC: 0.84
  * More stable across categories.

* **MLP Classifier**:

  * Test accuracy: \~78.7%
  * AUC: 0.87
  * Better adaptability to noise/rotation, but less stable across distant categories.

* **Confidence Analysis**:

  * **SVM**: Mean confidence ≈ 0.60
  * **MLP**: Mean confidence ≈ 0.82
  * PCA dimensionality reduction preserved AUC but slightly reduced accuracy.

## 📚 References

* Riesenhuber & Poggio (1999). *Hierarchical models of object recognition in cortex*.
* Serre et al. (2007). *Robust object recognition with cortex-like mechanisms*.
* Thorpe & Fabre-Thorpe (2001). *Seeking categories in the brain*.
