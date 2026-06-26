# Generalized Zero-Shot Learning (GZSL)

Generalized Zero-Shot Learning (GZSL) is the realistic benchmark setting for zero-shot evaluation. 

### Setting Profile:
Unlike standard ZSL, the search space during the test phase contains both seen ($S$) and unseen ($U$) classes simultaneously. 

### The Projection Bias Challenge:
Because the model has only seen training images from $S$, it develops an extreme bias toward predicting seen classes. Visual features of unseen classes are mapped close to seen class anchors in the semantic space, leading to poor accuracy on unseen classes. This is mitigated using calibration, temperature scaling, or generative synthesis.

## Architectural & Process Diagram

```mermaid
flowchart TD
    Train[Training Phase: Labeled Seen Classes] --> Model[ZSL Model]
    Model --> Test[Test Phase: Evaluation Space]
    Test --> MixedSpace["Seen Classes (S) + Unseen Classes (U)"]
    style MixedSpace fill:#bbf,stroke:#333,stroke-width:2px
```

---

[← Back to Main README](../README.md)
