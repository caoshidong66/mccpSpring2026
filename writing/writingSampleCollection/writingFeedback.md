# Writing Feedback — CAO Shidong (曹世東)

## Feedback on CAO Shidong's Writing Samples: Introduction and Literature Review

**Student:** CAO Shidong (曹世東)
**Topic:** Efficient Transfer from Image-Based LMMs to Video Understanding (MTransLLAMA)
**Date:** 2 March 2026
**Reviewer:** Simon Wang (with AI-assisted analysis)

**Your samples:** writing/writingSampleCollection/writingSamples.md
**Assessment rubric:** writing/assessment/writing_instructions_formatted.md

---

## Overall Assessment

Your writing samples are well-crafted and demonstrate strong analytical thinking. The three samples — a Move 2 (gap identification), a Move 2 (literature synthesis), and a Move 3 (research purpose) — show genuine engagement with the rhetorical structure of academic writing. Your gap identification (the cost and brittleness of video pretraining pipelines) is sharp and well-motivated, and your literature synthesis effectively groups prior work into two strands (task-specific multimodal vs. LLM-based video models). However, the main areas for improvement are: (1) there is no Move 1 (Establishing Territory) sample, which is a critical component; (2) the samples focus on a single paper (MTransLLAMA) and could benefit from broader engagement with the field; (3) the reflection section is entirely blank, which means I cannot assess your writing process or goals; and (4) citations are missing throughout.

**Estimated current level:** Good (7–8 range) — The analytical quality is strong and the move identification is accurate. Completing the missing components and adding citations will push this higher.

---

## Part 1: Move 2 (Introduction Gap Statement) Feedback

### What Works Well

- The dual motivation (cost + negative transfer) is clearly articulated and compelling
- The sentence structure is sophisticated and reads naturally
- You correctly identify that video pretraining can "dilute the broad visual knowledge learned from diverse image-text corpora" — this is a nuanced insight
- You connect the gap to a specific solution space ("methods that can reuse strong image-based LMM priors")

### Issue 1: No Citations

Your Move 2 sample makes several claims that require citations:
- "Large multimodal models (LMMs) have rapidly advanced vision-language understanding" — cite foundational LMM papers (e.g., LLaVA, InstructBLIP, Qwen-VL)
- "video-LMM systems extend these capabilities to temporally grounded tasks" — cite specific video-LMM papers
- "video-text pretraining is expensive and often inaccessible for small research teams" — cite evidence of computational cost

**Action:** Every factual claim in academic writing needs a citation. As a guide, this paragraph should have 5–8 citations.

### Issue 2: Move 1 Is Missing

Your submission starts with Move 2 (the gap). But readers need Move 1 first — why does video understanding matter? What has been achieved so far? Without establishing the territory, the gap statement lacks context.

**Suggestion for Move 1:** Start with 1–2 sentences establishing the importance of video understanding (applications in surveillance, content analysis, human-computer interaction, etc.), then describe the state-of-the-art (LMMs have achieved strong performance on image-language tasks and are being extended to video).

### Issue 3: The Three Constraints Could Be Strengthened with Evidence

You list three constraints: (i) cost, (ii) small/domain-specific datasets, (iii) negative transfer. These are strong points but would be more persuasive with specific numbers.

**Stronger version:** "(i) video-text pretraining typically requires X GPU-hours on Y samples [citation], making it inaccessible for research groups without industrial-scale compute; (ii) many downstream tasks have fewer than N labeled examples [citation]; (iii) models pretrained on instructional video corpora (e.g., HowTo100M) show X% performance drops when transferred to conversational or surveillance domains [citation]."

---

## Part 2: Literature Review (Move 2 Synthesis) Feedback

### What Works Well

- **Excellent thematic grouping.** Organizing prior work into (a) task-specific multimodal models and (b) LLM-based video approaches is a clear and useful framework
- **The concluding synthesis sentence is outstanding:** "the literature suggests a tension between generality and practicality" — this is exactly the kind of critical insight that elevates a literature review above mere description
- **The analysis of parameter-efficient tuning** is nuanced — noting that it reduces fine-tuning cost but doesn't eliminate pretraining burden

### Issue 4: Add Specific Paper Names and Results

Your synthesis discusses categories of approaches but rarely names specific papers or cites specific results. Academic literature reviews need concrete references.

**Your sentence:** "task-specific multimodal models for sentiment, sarcasm, and humor recognition that combine CNN/BERT-style encoders with fusion Transformers"

**With citations:** "Task-specific multimodal models such as [Author1 et al., Year] for sentiment analysis and [Author2 et al., Year] for sarcasm detection combine CNN/BERT-style encoders with fusion Transformers, achieving X% accuracy on [benchmark]."

### Issue 5: Consider Adding a Comparison Table

For the final draft, consider adding a comparison table that summarizes key approaches along dimensions like: model type, pretraining requirement, temporal modeling, parameters, and downstream performance. This would make the literature review more concrete and useful.

---

## Part 3: Move 3 (Research Purpose) Feedback

### What Works Well

- The technical approach (channel swapping for temporal attention reuse, early text-visual fusion, dynamic attention routing) is clearly described
- You effectively frame MTransLLAMA as a "parameter- and data-efficient pathway"
- The connection between the gap (Move 2) and the solution (Move 3) is logical

### Issue 6: Preview Specific Contributions

Move 3 should preview your contributions in a numbered list so readers know exactly what the paper delivers.

**Suggestion:** "This work makes three contributions: (1) a channel-swapping mechanism that repurposes image attention for temporal reasoning without video pretraining; (2) early text-visual fusion within the Q-former that conditions visual extraction on task instructions; and (3) dynamic attention routing that selects among attention masks with different receptive fields."

---

## Part 4: Missing Components

### Issue 7: No Reflection Submitted

Your reflection file contains only the blank template. The reflection is important for two reasons:
1. It helps me understand your writing challenges and provide targeted advice
2. It demonstrates self-awareness about your writing process

**Action:** Please fill in the reflection template honestly. Key questions to consider: What do you find hardest about academic writing? How do you use AI tools? What specific skills do you want to develop?

### Issue 8: Your Note About Move Labeling

You noted uncertainty about whether your Sample 1 is Move 1 or Move 2. Your instinct was correct — it is primarily Move 2 because "its main job is to articulate the niche/gap." This shows good awareness of the rhetorical function. However, you need a separate, dedicated Move 1 paragraph.

---

## Summary of Priority Actions

| Priority | Action | Impact |
|----------|--------|--------|
| 🔴 High | Add citations throughout all three samples | Makes claims evidence-based |
| 🔴 High | Write a Move 1 paragraph establishing the territory | Completes the Introduction structure |
| 🔴 High | Fill in the reflection template | Enables better feedback and self-development |
| 🟡 Medium | Add specific paper names and results to the literature synthesis | Strengthens evidence base |
| 🟡 Medium | Preview specific contributions in Move 3 with numbered list | Clarifies research value |
| 🟢 Lower | Add quantitative evidence for the three constraints in Move 2 | Makes gap argument more compelling |

---

## Next Steps

1. Read the [full writing instructions](https://github.com/tesolchina/mccpSpring2026/blob/main/writing/assessment/writing_instructions_formatted.md) carefully
2. Write a complete Introduction with Moves 1, 2, and 3
3. Expand the Literature Review into a full section with all four moves
4. Fill in your reflection
5. Submit by **15 March 2026** via Moodle forum and Turnitin
