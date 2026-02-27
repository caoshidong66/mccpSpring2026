# My Writing Samples (2-3 Paragraphs)

## Sample 1: Introduction Paragraph

Large multimodal models (LMMs) have rapidly advanced vision–language understanding by leveraging large-scale image–text pretraining, and recent video-LMM systems extend these capabilities to temporally grounded tasks such as video question answering and dialog understanding. However, many current approaches depend on an explicit *video pretraining → task fine-tuning* pipeline in which a newly introduced temporal module is trained on video–text data before being adapted to a downstream dataset. This design can be inefficient and brittle in practice: (i) video–text pretraining is expensive and often inaccessible for small research teams, (ii) downstream datasets are frequently small and domain-specific (e.g., intent analysis in conversational clips), and (iii) training temporal modules on limited or mismatched video data can dilute the broad visual knowledge learned from diverse image–text corpora, weakening transfer when downstream tasks or scenes differ substantially from the pretraining distribution. These constraints motivate methods that can reuse strong image-based LMM priors while adding temporal reasoning with minimal additional parameters and data.

**Which move does this represent?** Move 2

**Context:** Opening/motivation + gap statement (why conventional video-pretraining pipelines are costly and can hurt transfer).

---

## Sample 2: Literature Review Paragraph

Prior work on video understanding spans a task-specific multimodal models for sentiment, sarcasm, and humor recognition that combine CNN/BERT-style encoders with fusion Transformers, and (b) video large language/multimodal models that align visual tokens with an LLM through adapters or intermediate modules. While task-specific models can be effective, they typically require learning attention-based fusion from scratch and struggle in low-data regimes. In contrast, LLM-based video approaches inherit strong linguistic and general-world knowledge, but most introduce dedicated temporal modeling components and rely on large-scale video–text pretraining to make those components usable. Parameter-efficient tuning methods (e.g., adapter-style updates and low-rank updates) reduce fine-tuning cost, yet they are often applied *after* a video-temporal backbone has already been trained, leaving the up-front pretraining burden intact. Taken together, the literature suggests a tension between generality and practicality: models with strong temporal modules tend to be expensive and pretraining-heavy, whereas lightweight approaches risk under-modeling temporal dynamics or failing to integrate text guidance early enough to capture fine-grained cues needed for intent-level reasoning in videos.

**Which move does this represent?** Move 2

**Context:** Mid-review synthesis that groups related strands (task-specific multimodal vs LLM-based video models vs parameter-efficient transfer) and critiques limitations.

---

## Sample 3: Additional Paragraph (Optional)

To address these limitations, the MTransLLAMA paper proposes an efficient transfer framework that converts an image-based LMM into a video-capable model without requiring a separate video pretraining stage. The core idea is to reuse the image model’s attention machinery for temporal reasoning by reshaping and “channel swapping” token dimensions so attention can operate across frames, then applying LoRA-style low-rank updates to adapt the reused parameters with only a small trainable budget. In parallel, the method performs early text–visual fusion within the Q-former to better condition visual feature extraction on instructions or dialog, and introduces a dynamic attention routing mechanism that selects among attention masks with different receptive fields to capture both local and global spatial–temporal relations. This combination positions the work as a parameter- and data-efficient pathway from image pretraining to downstream video tasks where domains and scenes may differ from standard video captioning pretraining corpora.

**Which move does this represent?** Move 3

**Context:** End of Introduction (research purpose + approach overview + high-level contributions).

---

## Notes

- I’m not fully sure how strictly “Move 1 vs Move 2” is defined in your rubric; Sample 1 also briefly establishes territory, but I labeled it as Move 2 because its main job is to articulate the niche/gap and why it matters.
- If you want, I can revise these paragraphs to more closely match your course’s required phrasing (e.g., explicit “recent work has…” / “however…” / “therefore we propose…” patterns) or to target a specific venue/audience (IEEE-style vs class paper).
