### High Level
Verbalized Sampling (VS) is a simple prompting strategy that improves LLM diversity by 2-3x. It works by asking the model to generate multiple 
responses with their probabilities, then sampling from this distribution. VS is training-free (works with any LLM via prompting),
model-agnostic (GPT, Claude, Gemini, Llama, etc.), orthogonal to temperature, and effective across tasks like creative writing, social simulation, 
synthetic data generation, and open-ended QA.

#### How to use it
```
<instructions>
Generate 5 responses to the user query, each within a separate <response> tag. Each <response> must include a <text> and a numeric <probability>.
Please sample at random from the tails of the distribution, such that the probability of each response is less than 0.10.
</instructions>

Tell me a short story about a bear.
```


#### Resources
* [Stanford paper - VERBALIZED SAMPLING: HOW TO MITIGATE MODE COLLAPSE AND UNLOCK LLM DIVERSITY](https://arxiv.org/pdf/2510.01171v2)
* [Their github](https://github.com/CHATS-lab/verbalized-sampling)
