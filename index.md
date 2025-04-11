---
layout: default
title: "Conditional Vocal Timbral Technique Conversion via Embedding-Guided Attribute Modulation"
---

<!-- Link to custom CSS to hide GitHub button and footer -->
<link rel="stylesheet" href="/assets/css/style.css">

1. [Abstract](#abstract)  
2. [Timbral Technique Conversion](#timbral-technique-conversion)  
   2.1 [Model to Falsetto](#model-to-falsetto)  
   2.2 [Model to Whisper](#model-to-whisper)  
   2.3 [Model to Scream](#model-to-scream)  
   2.4 [Model to Modal](#model-to-modal)  
3. [Ablation Study](#ablation-study)  
   3.1 [Without Prosody](#without-prosody)  
   3.2 [Augmentations](#augmentations)  

---

## Abstract

Vocal timbral techniques—such as whisper, falsetto, and vocal fry/false cord scream—uniquely shape the spectral properties of the human voice, adding expressive nuance. Converting one timbral technique to another while preserving the original speaker’s identity remains a complex challenge. Traditional voice conversion methods excel at altering speaker identity or broad timbral qualities but often fail to accurately transform specialized timbral techniques without compromising speaker-specific traits. Similarly, existing style-transfer models, designed to capture emotional expressiveness or broad singing styles, lack the granularity and flexibility required to handle diverse, technique-specific timbral variations such as whisper or scream. To address this, we propose FABYOL, a novel embedding-guided framework for timbral technique conversion built upon a pre-trained, frozen FACodec architecture. FABYOL leverages supervised contrastive learning to generate robust embeddings that precisely encode individual timbral techniques, capturing their distinct spectral and stylistic features. Beyond timbre modulation, we emphasize prosody modulation as critical for achieving authentic conversions, employing adaptive layer normalization to modulate these attributes effectively during the transfer process. This approach enables precise, speaker-consistent transformations with minimal architectural changes. Through experimental evaluation—using tailored objective metrics and a user study—FABYOL demonstrates superior performance compared to state-of-the-art voice conversion models, advancing the fidelity and flexibility of timbral technique manipulation.


---

## Timbral Technique Conversion

### Model to Falsetto

*(Demo or description here)*

### Model to Whisper

*(Demo or description here)*

### Model to Scream

*(Demo or description here)*

### Model to Modal

*(Demo or description here)*

---

## Ablation Study

### Without Prosody

*(Demo or description here)*

### Augmentations

*(Demo or description here)*
