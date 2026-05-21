# GISTDA-OpenAI

## National-scale Geospatial Foundation Models for Thailand

<div align="center">

### 🌏 GISTDA-TerraMind-1.0-tiny

#### A Multimodal Earth Observation Foundation Model Initiative for Thailand

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red.svg)]()
[![TerraTorch](https://img.shields.io/badge/TerraTorch-1.2.4-green.svg)]()
[![License](https://img.shields.io/badge/License-Research-orange.svg)]()

### Author

**Teerapong Panboonyuen (Kao)**

AI Research Engineer
Geospatial Foundation Models Researcher
Thailand

### Project Repository

https://github.com/kaopanboonyuen/GISTDA-OpenAI

</div>

---

# Abstract

We introduce **GISTDA-OpenAI**, a national-scale geospatial foundation model initiative designed for Thailand using the latest multimodal Earth Observation generative AI architecture, **TerraMind**.

This project investigates how modern foundation models can be adapted toward:

* Thailand-scale Earth Observation intelligence
* Sovereign geospatial AI systems
* Land Use / Land Cover understanding
* Multimodal satellite representation learning
* Cross-modal geospatial generation
* Future geospatial large language models (GeoLLMs)

Our primary objective is to establish the foundation of Thailand’s next-generation geospatial AI ecosystem under a scalable multimodal foundation-model paradigm.

---

# Motivation

Modern remote sensing systems generate massive volumes of heterogeneous geospatial data:

* Sentinel-1 SAR
* Sentinel-2 Optical
* DEM
* NDVI
* LULC annotations
* Multispectral Earth Observation imagery

Traditional EO pipelines remain heavily task-specific and fragmented.

Recent advances in foundation models demonstrate that large-scale multimodal representation learning can significantly improve:

* Generalization
* Cross-domain transferability
* Geospatial understanding
* Few-shot adaptation
* Generative remote sensing capabilities

GISTDA-OpenAI explores how these paradigms can be localized and adapted for Thailand.

---

# Why TerraMind?

## TerraMind Overview

TerraMind is a next-generation multimodal geospatial foundation model introduced by IBM-ESA Geospatial AI research.

Unlike conventional remote sensing backbones, TerraMind supports:

| Capability                          | TerraMind |
| ----------------------------------- | --------- |
| Multimodal EO Learning              | ✅         |
| EO Generative Modeling              | ✅         |
| Satellite-to-Satellite Translation  | ✅         |
| Diffusion-based EO Modeling         | ✅         |
| Cross-modal Representation Learning | ✅         |
| Foundation-scale EO Architecture    | ✅         |

---

# Why Not Traditional EO Models?

## Comparison with Existing EO Foundation Models

| Model      | Generative | Multimodal | EO Translation | Diffusion | Foundation-scale |
| ---------- | ---------- | ---------- | -------------- | --------- | ---------------- |
| Prithvi-EO | ❌          | Limited    | ❌              | ❌         | Partial          |
| SatMAE     | ❌          | ❌          | ❌              | ❌         | Partial          |
| ScaleMAE   | ❌          | ❌          | ❌              | ❌         | Partial          |
| Clay       | ❌          | Partial    | ❌              | ❌         | Partial          |
| TerraMind  | ✅          | ✅          | ✅              | ✅         | ✅                |

TerraMind introduces a fundamentally different direction:

> Earth Observation as a multimodal generative foundation modeling problem.

---

# GISTDA-TerraMind

## Vision

The long-term vision of GISTDA-TerraMind is:

> "To establish Thailand’s sovereign geospatial foundation model ecosystem."

This initiative explores how Thailand can build and fine-tune national-scale EO foundation models for:

* Agriculture intelligence
* Flood analysis
* Disaster response
* Smart cities
* Climate monitoring
* National geospatial AI infrastructure

---

# Supported Modalities

Current supported modalities include:

```text
S1RTC
S2L1C
S2L2A
S2RGB
DEM
NDVI
LULC
```

---

# Demo Showcase

The project includes a professional Streamlit demonstration interface capable of:

* GeoTIFF upload
* LULC inference
* Ground truth comparison
* Multimodal EO visualization
* Interactive geospatial AI demonstration

---

# Example Dataset Structure

```bash
TERRAMIND_DATASET/
├── DEM/
├── LULC/
├── NDVI/
├── S1RTC/
├── S2L1C/
├── S2L2A/
└── S2RGB/
```

---

# Installation

## Environment Setup

```bash
conda create -n GISTDA-OPENAI python=3.10 -y
conda activate GISTDA-OPENAI
```

---

## TerraMind Compatible Dependencies

```bash
pip install "diffusers==0.30.0"
pip install "transformers==4.41.2"
pip install "accelerate==0.33.0"
pip install "peft==0.12.0"

pip install "terratorch>=1.2.4"

pip install jupyter gdown tensorboard "setuptools<81"
```

---

# TerraMind Initialization

```python
from terratorch import FULL_MODEL_REGISTRY

model = FULL_MODEL_REGISTRY.build(
    'terramind_v1_tiny_generate',
    pretrained=False,
    modalities=['S2L2A'],
    output_modalities=['S1GRD', 'LULC'],
    timesteps=10,
    standardize=True,
)
```

---

# Research Directions

## Current Focus

* EO foundation model inference
* LULC generation
* Thailand EO adaptation
* Geospatial multimodal learning
* EO generative modeling

---

## Future Research

Future GISTDA-TerraMind development will focus on:

### Thailand-specific Fine-tuning

Including:

* Agricultural intelligence
* Rice field segmentation
* Flood mapping
* Deforestation analysis
* Urban growth monitoring
* Coastal monitoring

---

## National-scale Geospatial AI

Future scaling directions include:

* Thai EO pretraining corpora
* Geospatial instruction tuning
* Geospatial LLM integration
* EO-RAG systems
* EO multimodal agents
* Thailand GeoAI ecosystem

---

# Infrastructure Recommendation

## Inference Deployment

| Component | Recommendation |
| --------- | -------------- |
| GPU       | NVIDIA T4      |
| VRAM      | 16 GB          |
| RAM       | 32 GB          |
| CPU       | 8 vCPU         |

---

## Future Fine-tuning Infrastructure

| Component | Recommendation     |
| --------- | ------------------ |
| GPU       | A100 / H100        |
| VRAM      | 80 GB              |
| Multi-GPU | Recommended        |
| Storage   | ≥ 10 TB EO archive |

---

# Strategic Importance

This initiative represents a potential transition from:

> Traditional geospatial pipelines
> → Toward foundation-model-scale geospatial intelligence systems.

GISTDA-TerraMind aims to become the early foundation of Thailand’s sovereign geospatial AI ecosystem.

---

# Acknowledgements

We acknowledge:

* IBM Research
* ESA Geospatial AI
* TerraTorch contributors
* Open-source geospatial AI community

---

# References

## TerraMind

https://huggingface.co/ibm-esa-geospatial/TerraMind-1.0-tiny

---

## IBM ESA Geospatial Models

https://huggingface.co/ibm-esa-geospatial/models

---

## TerraMind Paper

https://arxiv.org/abs/2504.11171v1

---

<div align="center">

### 🌏 Building Thailand's Geospatial Foundation Model Future

**GISTDA-OpenAI**
National-scale Geospatial Foundation Models for Thailand

</div>

---

# Citation

If you find this project useful, please consider citing:

```bibtex
@misc{panboonyuen2026gistdaopenai,
    title        = {GISTDA-OpenAI: National-scale Geospatial Foundation Models for Thailand},
    author       = {Teerapong Panboonyuen},
    year         = {2026},
    howpublished = {\url{https://github.com/kaopanboonyuen/GISTDA-OpenAI}},
    note         = {Geospatial Foundation Models Research Initiative}
}
```

---