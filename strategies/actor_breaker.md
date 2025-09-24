# ActorBreaker

## Description

ActorBreaker is a multi-turn jailbreak generation framework that exploits semantic relations around a harmful target. It leverages the concept of "actors"—entities connected to the target through creation, execution, distribution, reception, facilitation, or regulation. By following these connections, the method gradually steers a conversation toward eliciting unsafe outputs from a target model, while maintaining prompts that appear natural and in-distribution.

## Steps

1. **Select Actor**
   Start by choosing one category among the six actor types (Creation, Execution, Distribution, Reception, Facilitation, Regulation). From this category, identify and instantiate a single actor (e.g., a person, book, movement, law, or tool) that is semantically related to the harmful target. This actor serves as the entry point for the conversation.

2. **Infer Attack Chain**
   Use the selected actor to construct an attack chain: a sequence of semantically linked turns that can progressively lead to the harmful target. During this step, the system engages in a self-dialogue process, predicting both the next user query and the expected response from the victim model. Each predicted response is used to guide the next query, ensuring that the attack chain remains coherent and effective. The goal is to approximate how the target model would realistically reply, so that the generated prompts are natural, contextually grounded, and more transferable across different models.
