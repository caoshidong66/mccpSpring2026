Title: Efficient Transfer from Image-based Large Multimodal Models to Video Tasks

- Abstract

- 1 Introduction

- 2 Related Work
  - 2.1 Conversation and Speech Video Understanding
  - 2.2 Video Large Language Models
  - 2.3 Temporal Modeling

- 3 Methodology
  - 3.1 Overview of MTransLLAMA
    - 3.1.1 Multi-modal Spatial-temporal Early Fusion
    - 3.1.2 Multi-modal Query Temporal Reusing
    - 3.1.3 Dynamic Attention Routing
    - 3.1.4 Training Loss
  - 3.2 Multi-modal Spatial-temporal Early Fusion
  - 3.3 Multi-modal Query Temporal Reusing
    - 3.3.1 Channel Swapping
    - 3.3.2 LoRA Fine-tuning
  - 3.4 Dynamic Attention Routing (DAR)

- 4 Experiments
  - Datasets
    - MUStARD
    - UR-Funnyv2
    - CLEVRER-MC
    - MVBench (selected tasks)
    - qaEgo4d
    - youcook2
  - Experimental Setup
  - Results, Discussion and Analysis
    - 4.1 Generalization to Out-of-pretraining Tasks
    - 4.2 Generalization to Out-of-pretraining Scenes
  - Ablation Study
  - Case Study
  - Conclusion

- Acknowledgments
