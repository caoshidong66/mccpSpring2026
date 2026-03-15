# Outline and script for poster presentation (2-3 minutes)

This script follows the poster flow and is designed for a short academic presentation of about 2 to 3 minutes.

## Presentation outline

1. Opening: title, task, and one-sentence takeaway.
2. Background and problem: why reference-based fashion design is difficult.
3. Method: shared latent transfer, ViT guidance, and mask guidance.
4. Results: key comparisons and one or two numbers.
5. Conclusion: impact and limitation.

## Script (about 2 minutes 30 seconds)

**Opening**  
"Hello, today I will present our work, **DiffFashion: Reference-based Fashion Design with Structure-aware Transfer by Diffusion Models**. The goal is to generate a new clothing design by combining the structure of a source garment with the appearance of a reference image, even when the reference comes from a very different domain, such as marine life or natural objects."

**Background and research problem**  
"This is a challenging task for two reasons. First, there is often a large domain gap between the clothing image and the reference image, so standard style transfer or image translation methods may fail to transfer appearance realistically. Second, for new fashion designs, we do not have paired ground-truth training data, so supervised methods are not practical and structure can easily be lost during generation."

**Method**  
"To solve this, we propose DiffFashion, an unsupervised diffusion-based framework. The first idea is a shared latent transfer strategy. Instead of starting from the clothing image, we start from the reference appearance image and keep a shared DDPM latent, which helps bridge the domain gap and gradually adapt the reference appearance into the clothing domain. The second idea is mixed guidance. We use DINO-ViT features for both structure guidance and appearance guidance, so the generated image keeps the garment layout while remaining semantically similar to the reference. We also generate a foreground mask automatically from diffusion noise differences, which gives structural guidance without requiring manual annotation."

**Results**  
"In experiments, we build a new OceanBag dataset with 6,000 handbag images and 2,400 marine-life reference images, and we also test on other clothing categories. Compared with DiffuseIT, Splice, WCT2, and SANet, DiffFashion achieves the best overall user-study score on OceanBag, with **73.6**, and the best appearance score, **49.4**. It also gives the best LPIPS appearance similarity, while keeping strong structure preservation and competitive realism."

**Conclusion**  
"In summary, DiffFashion makes reference-based fashion design more practical by handling large domain gaps and preserving clothing structure in a zero-shot setting. Its main limitation is that mask quality can still vary, so improving mask generation is an important direction for future work. Thank you."
