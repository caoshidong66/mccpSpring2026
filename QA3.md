# Anticipated Q&A — DiffFashion 3MT Presentation

Use this list to prepare short spoken answers.  
For a non-specialist audience, keep answers simple and under 25 seconds.

---

## Lay Audience Questions

### Q1: What problem does DiffFashion solve?

**A:**  
DiffFashion helps create a new fashion design from two images. One image gives the clothing shape, and another image gives the style, such as color, texture, or pattern.

---

### Q2: What is the main idea in one sentence?

**A:**  
The main idea is to keep the original clothing shape, but give it a new visual style from a reference image.

---

### Q3: Can you give a simple example?

**A:**  
Yes. Imagine I have a plain T-shirt, but I like the pattern from another image. DiffFashion can keep the T-shirt shape and transfer that pattern onto it.

---

### Q4: Is this the same as normal image editing?

**A:**  
Not exactly. Normal image editing may change the whole image. DiffFashion focuses on fashion design, so it tries to protect the clothing structure while changing the appearance.

---

### Q5: Why is this difficult?

**A:**  
Because the AI must balance two goals. It should change enough to follow the reference style, but not change so much that the clothing loses its shape.

---

### Q6: What is a diffusion model?

**A:**  
A diffusion model is an AI model that starts from noise and slowly creates a clear image. In DiffFashion, this process is guided so the final image keeps the clothing shape and uses the reference style.

---

### Q7: What does “reference-based fashion design” mean?

**A:**  
It means the design is guided by a reference image. The reference image gives visual inspiration, such as a color, texture, pattern, or style.

---

### Q8: What does “structure-aware” mean?

**A:**  
It means the model pays attention to the structure of the clothing, such as the outline, category, sleeves, collar, and overall shape.

---

### Q9: What is mask guidance?

**A:**  
Mask guidance tells the model where the clothing is. This helps the AI focus on the garment area instead of changing the background too much.

---

### Q10: What is ViT guidance?

**A:**  
ViT guidance uses visual features from a vision transformer. In simple words, it helps the model understand important visual information, such as structure and style.

---

### Q11: Does DiffFashion replace human designers?

**A:**  
No. DiffFashion is better understood as a design assistant. It can give designers more visual options, but humans still choose, judge, and refine the final design.

---

### Q12: Why is this useful for fashion designers?

**A:**  
Fashion design often needs many trials. DiffFashion can help designers explore ideas faster and see different style options before making a final choice.

---

### Q13: Why is unsupervised learning useful here?

**A:**  
In real fashion design, it is hard to collect many perfect before-and-after image pairs. An unsupervised method can learn without needing these exact paired examples.

---

### Q14: What is the main contribution of this work?

**A:**  
The main contribution is a diffusion-based method that transfers reference appearance to clothing images while preserving clothing structure.

---

### Q15: What makes this work different from simple style transfer?

**A:**  
Simple style transfer may change the image too freely. DiffFashion is designed for fashion, so it tries to keep the garment shape realistic while transferring the reference appearance.

---

### Q16: What could go wrong if the model is not well controlled?

**A:**  
The clothing may lose its shape, the pattern may look unnatural, or the output may not follow the reference image well.

---

### Q17: What is the real-world impact?

**A:**  
It can support faster fashion ideation, lower the cost of visual exploration, and help designers turn inspiration into design examples more quickly.

---

### Q18: Who can benefit from this research?

**A:**  
Fashion designers, online clothing platforms, design students, and companies that need fast visual design exploration can benefit from this work.

---

### Q19: What should the audience remember?

**A:**  
DiffFashion helps answer a simple design question: how can we give clothing a new style while keeping its original shape?

---

## Slightly More Technical Questions

### Q20: What are the two main inputs?

**A:**  
The first input is the source clothing image, which provides structure. The second input is the reference image, which provides appearance information.

---

### Q21: What is transferred from the reference image?

**A:**  
The model transfers appearance information, such as color, texture, pattern, and general visual style.

---

### Q22: What should be preserved from the source image?

**A:**  
The model should preserve the clothing category, outline, shape, and important structural details.

---

### Q23: Why use diffusion models for this task?

**A:**  
Diffusion models are strong at image generation and image editing. They can gradually refine an image, which makes them useful for controlled visual design.

---

### Q24: What is the role of guidance in the diffusion process?

**A:**  
Guidance helps control the generation process. It tells the model to follow the reference appearance while keeping the clothing structure.

---

### Q25: Why is paired data hard to get?

**A:**  
Because it is difficult to find two images where one is the exact original garment and the other is the same garment redesigned with a target style. Real design data is usually not paired so cleanly.

---

### Q26: How do you explain the method without technical words?

**A:**  
I would say: the AI keeps the “cut” of the clothing and borrows the “fabric feeling” from another image to create a new design.

---

### Q27: What is the biggest challenge in this task?

**A:**  
The biggest challenge is balance. The output must be new enough to follow the reference, but stable enough to keep the original clothing structure.

---

### Q28: How do you know the result is good?

**A:**  
A good result should satisfy three things: it keeps the source clothing shape, follows the reference style, and still looks like realistic clothing.

---

### Q29: Can this method be used outside fashion?

**A:**  
The idea may be useful in other design fields where we want to keep structure but change appearance, such as product design or interior design.

---

### Q30: What is your final takeaway?

**A:**  
DiffFashion shows how generative AI can support creative work. It helps people explore new design ideas while keeping human designers in control.