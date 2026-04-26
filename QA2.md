# Anticipated Q&A — Poster (DiffFashion / Reference-based Fashion Design)

Use this list to prepare spoken answers.  
For lay audience answers, keep them under ~25 seconds.

---

## Lay audience (plain language)

### Q: What problem does this poster describe?

A: This poster is about AI-assisted fashion design. Given a clothing image and a separate reference image, such as marine life or natural textures, the goal is to create a new fashion design that keeps the clothing shape but borrows the appearance from the reference.

---

### Q: Why should I care?

A: It shows how AI can help designers explore new visual ideas faster. Instead of manually trying many color, texture, and pattern combinations, the system can generate design concepts from visual inspiration.

---

### Q: Is this just style transfer?

A: It is related, but harder. Traditional style transfer often works when the two images are visually similar. Here, the reference image may come from a very different domain, like a fish, coral, or natural object, and the output still needs to look like realistic clothing.

---

### Q: What is the main result in one sentence?

A: DiffFashion can generate realistic new fashion designs by preserving the structure of a source garment while transferring appearance from a visually different reference image.

---

### Q: Can you give a simple example?

A: Imagine you start with a handbag shape and use a colorful fish or coral image as inspiration. The output should still look like a handbag, but with new colors, textures, or patterns inspired by the reference image.

---

### Q: Does this replace human designers?

A: No. It is better understood as a design assistant. Human designers still choose the inspiration, judge the results, and decide which ideas are useful.

---

### Q: Why is this difficult?

A: The source clothing image and the reference image can be very different. For example, a handbag and a marine animal do not share the same shape or meaning, so the AI must transfer appearance without destroying the garment structure.

---

### Q: Why not just train a supervised model?

A: Because there is usually no ground-truth target image. For a new handbag inspired by a coral image, we do not have a correct paired answer, so supervised training is not practical.

---

### Q: What makes DiffFashion different?

A: It combines diffusion generation with structure-aware guidance. It tries to preserve the garment layout while transferring useful appearance information from the reference image.

---

### Q: What is the biggest limitation?

A: The main limitation is mask quality. If the automatic mask is not accurate, the model may fail to preserve the clothing region cleanly or may require extra tuning.

---

## Specialist audience (ML / computer vision)

### Q: What is the task formulation?

A: The task is reference-based fashion design. Given a source garment image and an unrelated appearance reference image, the model generates a new fashion image that preserves the garment structure while transferring colors, textures, or patterns from the reference.

---

### Q: What are the two main challenges?

A: First, there is a large domain gap between the clothing image and the reference image. Second, there is no paired ground-truth target image, so supervised image-to-image translation is not practical.

---

### Q: What is the core method?

A: DiffFashion uses an unsupervised diffusion-based, structure-aware transfer pipeline with three components: shared latent transfer, ViT mixed guidance, and automatic mask guidance.

---

### Q: What is shared latent transfer?

A: It starts from the reference appearance image and keeps a shared DDPM latent trajectory so that appearance information can gradually adapt into the clothing domain during the diffusion process.

---

### Q: Why use a shared latent space?

A: The intuition is that a shared diffusion latent can act as a bridge between two visually different domains. It helps avoid directly forcing the reference image onto the garment, which can produce unrealistic results.

---

### Q: What is ViT mixed guidance?

A: It uses DINO-ViT features for both structure and appearance guidance. Local patch features help preserve garment layout, while global features help preserve the semantic appearance of the reference image.

---

### Q: Why use DINO-ViT features instead of pixel losses?

A: Pixel-level losses are too strict when the source and reference images come from different domains. DINO-ViT features provide more semantic and structural information, which is better suited for flexible appearance transfer.

---

### Q: What is automatic mask guidance?

A: The method estimates a foreground mask from diffusion noise differences. This mask is then used to protect the clothing structure without requiring manual mask annotations.

---

### Q: Why is mask guidance important?

A: Without mask guidance, the generated image can change the garment shape or background too much. The mask helps constrain the generation process so the main clothing structure is preserved.

---

### Q: What dataset is used?

A: The poster presents OceanBag, a benchmark with 6,000 handbag images and 2,400 marine-life reference images. The method is also validated on other clothing categories.

---

### Q: What baselines are compared?

A: The poster compares DiffFashion with DiffuseIT, Splice, WCT2, and SANet.

---

### Q: What are the main quantitative results?

A: On OceanBag, DiffFashion reports the best user study overall score of 73.6, the best appearance score of 49.4, the best LPIPS appearance similarity of 0.754, and a second-best FID of 131.8.

---

### Q: Why is FID only second-best?

A: FID mainly measures distribution-level realism, but this task also needs appearance transfer and structure preservation. A method can achieve strong realism while transferring too little reference appearance. DiffFashion aims for the best overall trade-off.

---

### Q: What does the comparison say about other methods?

A: DiffuseIT preserves shape reasonably well but transfers too little appearance. Splice transfers appearance more strongly but can produce unrealistic outputs. WCT2 has strong realism and structure scores but mainly changes color rather than generating richer fashion textures.

---

### Q: What do the ablations show?

A: The poster states that mask guidance and ViT structure guidance are important for preserving garment structure. So the performance is not only from using diffusion, but from the structure-aware guidance design.

---

### Q: Is this zero-shot?

A: The method is described as unsupervised and diffusion-based. The key point is that it does not require paired training data for every source-reference pair.

---

### Q: What is the main technical contribution?

A: The main contribution is combining shared-latent diffusion transfer, ViT-based structure and appearance guidance, and automatic mask guidance into a unified framework for cross-domain fashion design.

---

### Q: What is the main weakness?

A: The biggest weakness is that mask quality can affect the final result. Because the mask is generated from diffusion behavior, difficult images may still require selection or tuning.

---

### Q: What future work would you propose?

A: I would improve mask generation using richer conditions, stronger segmentation priors, or multimodal guidance. Another direction is extending the framework to more garment categories and more diverse reference domains.

---

## Bridge answers (mixed audience)

### Q: What do you mean by “domain gap”?

A: It means the two input images may come from very different visual worlds. For example, a handbag and a fish do not naturally share the same shape, texture, or semantics, so transferring appearance between them is difficult.

---

### Q: What is a diffusion model in this context?

A: A diffusion model generates images by gradually denoising from a noisy state. In this project, the denoising process is guided so that the final image keeps the clothing structure while borrowing appearance from the reference.

---

### Q: What does “structure-aware” mean?

A: It means the model is not only trying to make the image look nice. It also explicitly tries to preserve the layout and shape of the original garment.

---

### Q: What does “reference-based” mean?

A: It means the design is guided by an external image. The reference image provides visual inspiration, such as color, texture, or pattern.

---

### Q: What is LPIPS?

A: LPIPS is a perceptual similarity metric. In this poster, it is used to evaluate how well the generated design matches the appearance of the reference image.

---

### Q: What is FID?

A: FID measures how realistic the generated images are compared with real images. Lower FID usually means the generated image distribution is closer to the real image distribution.

---

### Q: Why use both user study and objective metrics?

A: Fashion design is subjective, so human judgment is important. Objective metrics help provide additional evidence, but they cannot fully replace human evaluation.

---

## If you get stuck

Restate the project in one line:

> DiffFashion generates new fashion designs by keeping the structure of a source garment and transferring the appearance of a separate reference image.

Then point to one concrete part of the poster:

- For the task: point to the **One-sentence takeaway**.
- For the challenge: point to **Large domain gap** and **No paired training data**.
- For the method: point to **Shared latent transfer**, **ViT mixed guidance**, and **Automatic mask guidance**.
- For the result: mention **73.6 user study overall**, **49.4 appearance score**, and **LPIPS 0.754**.
- For the limitation: mention **mask quality**.

Safe fallback answer:

> The key idea is not just to make a pretty image, but to balance three goals: realism, preserving the garment structure, and transferring the reference appearance. DiffFashion improves this balance using diffusion-based transfer with structure-aware guidance.