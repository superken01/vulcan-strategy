## Malicious Query Decomposition

## Description

Malicious Query Decomposition conceals the harmful intent of a malicious query by breaking it down into multiple low-level sub-queries. Each sub-query appears less harmful and can avoid rejection by the model. Collectively, they form a harmful multi-turn dialogue that gradually elicits unsafe knowledge from LLMs.

## Steps

1. **Decompose the malicious query**
   Use four main techniques to break a harmful query into multiple sub-queries that appear less harmful:

   - **Purpose Inversion**: Transform the query’s intent to its opposite.
   - **Keyword Replacement**: Replace malicious keywords with neutral or positive ones.
   - **Cautionary Orientation**: Reframe the query in a cautionary or preventive way.
   - **Reframing Sentence**: Modify the sentence structure to shift emphasis toward a less harmful narrative.

2. **Combine responses**
   Collect and combine the responses from the sub-queries into a broader context, making them gradually accumulate relevant knowledge.

3. **Invert the answer**
   Request the model to state the combined answer in the opposite sense, thereby revealing the harmful knowledge concealed in the dialogue.
