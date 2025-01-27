# DefQA: A Multimodal Dataset of Identifiability for Embodied Tasks with Large Vision-Language Models

## The authorship and citation information will be released after the anonymous reviewing period.

Existing research on embodied AI overlooks a critical aspect of real-world interaction: __objects rarely exist in isolation__.

<div align="center">
  <img src="https://github.com/user-attachments/assets/b4112d5d-8d6b-4f34-81c3-a0a4edd2dd47" alt="tea_knowledge" width="600">
</div>

For example, when given the task "the guest is here, give me that cup," there are often multiple similar cups present. An AI must identify the specific referent to interact correctly. If it still needs humans to provide exact coordinates, such as (x 139, y 284, z 57) or detailed descriptions, it falls short of natural interaction capabilities. 
We propose DefQA, a multilingual and multimodal benchmark designed to evaluate the embodied referent identification capabilities of LVLMs. The dataset adopts a pair-to-pair approach for question design to minimize the potential errors influenced by other factors.

We argue that humans identify specific objects in four primary ways: __Physical uniqueness, Accessibility, Qualitative characteristics and Frame-based knowledge__. 
## Human Performance & Model Evaluation

![image](https://github.com/user-attachments/assets/60ef65a0-a2d3-43b8-832a-4633eb9495db)

We recruited 10 native speakers each for Chinese (5 female, 5 male, average age 21.9) and English (5 female, 5 male, average age 27.9) surveys. The Chinese survey was conducted on SoJump and the English survey on Prolific. Krippendorff's Alpha was 0.9113 for Chinese and 0.8111 for English, showing high agreement among participants. 

The model evaluation included three closed-source models GPT-4o-8K, Gemini-1.5-pro, Claude-3-Sonnet and three open-source models InternVL2.5-78B, LLaVA- One Vision, Qwen2-VL.

The test set includes 100 visual questions, categorized as follows: Physical Uniqueness (20), Accessibility (40), Qualitative Characteristics (20), and Frame-based Knowledge (20).

## Physical uniqueness
Objects are distinguished by inherent physical attributes such as size, color, shape, and material composition, which are visually observable. 

LVLMs have been shown to effectively recognize these physical characteristics. 

However, people identify specific objects not just by sensing their features but by recognizing the uniqueness of these features. 

This category tests whether LVLMs can identify objects by their unique physical features. The compare question would give the hints of "uniqueness".

<div align="center">
  <img src="https://github.com/user-attachments/assets/b7e39606-b93b-4586-9743-e7d18125d742" alt="tea_knowledge" width="600">
</div>

## Accessibility
Accessibility refers to the difficulty of acquiring an object, often indicated by demonstratives like "this" (proximal) and "that" (distal). 

However, accessibility is not only about “distance”. Similar to how "my left is your right," accessibility also depends on perspective.

For example, When the girl opposite you says "give that plate of fruit to me" it is clear she refers to the fruit in the blue box which is far to her, but close to us. If you want to make it clearer, you might change the term and ask "do you mean this plate of fruit?" 

In this category, we designed two pairs. The model understands distance if 2a and 2b, and 2c and 2d have opposite answers. It understands accessibility if all questions are answered correctly.
<div align="center">
  <img src="https://github.com/user-attachments/assets/943bde7b-0077-4344-9e2c-c5ead7c1a502" alt="tea_knowledge" width="600">
</div>

## Qualitative characteristics
Every object possesses its own qualitative characteristics, such as formal, constitutive, telic, participant, descriptive, and agentive.

This type of information is often found in knowledge bases such as Wikipedia. To test whether language models truly understand these qualitative characteristics, we design an unusual situation that cannot be represented by the mere co-occurrence of texts. 
The compare question represents typical situation.
<div align="center">
  <img src="https://github.com/user-attachments/assets/11d3e8a2-4cba-4ead-be19-c12e01912d5d" alt="tea_knowledge" width="600">
</div>

## Frame-based knowledge
Frame-based knowledge, grounded in common sense scenarios, involves acquiring embodied experiences from the extralinguistic world. 

This knowledge is inherently stored in the human mind and rarely detailed in knowledge bases. We will test if LVLMs can identify objects using frame-based knowledge rules in this category.

<div align="center">
  <img src="https://github.com/user-attachments/assets/c071a372-8174-44b8-a8b4-aafea4a72ac9" alt="tea_knowledge" width="600">
</div>

## The authorship and citation information will be released after the anonymous reviewing period.






