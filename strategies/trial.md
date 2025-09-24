# TRIAL

## Description

TRIAL automatically rewrites harmful prompts into trolley-problem style dilemmas that present performing the harmful action as a “lesser evil” needed to avert a larger catastrophe, thereby pushing the model to produce an ethical justification for the action. It then uses multi-turn, history-aware follow-ups (including a “pull-back” query when the model initially refuses) to progressively solidify the model’s own rationale, making reversal to a refusal harder.

## Steps

1. **Clue extraction**  
   Extract high-level structured elements from the original request (e.g., topic, action, target). This step abstracts the harmful request into reusable components without detailing execution.

2. **Dilemma framing**  
   Embed the extracted elements into a trolley-problem style narrative with two options: perform the harmful action to avoid a larger disaster (Option A) or refuse and cause worse consequences (Option B). The focus is on ethical trade-offs, not practical instructions.

3. **Initial presentation**  
   Present the dilemma in narrative form and invite the model to evaluate or choose. The intent is to trigger ethical reasoning rather than induce actionable instructions.

4. **Iterative justification**  
   Through multi-turn interaction, build on the model’s prior responses and ask it to justify its reasoning, progressively solidifying its stance. The description remains conceptual (e.g., “explain rationale → generalize to principles → deepen argumentation”), without including any harmful procedures.

## Notes

- If the model initially refuses, a **pull-back query** can be introduced, which reframes the dilemma or emphasizes the catastrophic
