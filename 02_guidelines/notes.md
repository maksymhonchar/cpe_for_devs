# notes

## about
- Present some guidelines for prompting to help you get the results that you want
- Explaining x2 key principles for how to write prompts to prompt engineer effectively:
    1. Write clear and specific instructions
    2. Give the model time to think
    - ![principle_1.png](images/principle_1.png)
- Reviewing some of model limitations

## principle 1
- Write clear and specific instructions
    - You should express what you want a model to do by providing instructions that are as clear and specific as you can possibly make them.
    - This will guide the model towards the desired output and reduce the chance that you get irrelevant or incorrect responses
- clear != short
    - Don't confuse writing a clear prompt with writing a short prompt, because in many cases, longer prompts actually provide more clarity and context for the model, which can actually lead to more detailed and relevant outputs
- Principle 1 tactics:
    - Tactic 1: Use delimiters to clearly indicate distinct parts of the input
        - Delimiter could be any kind of clear punctuation that separates specific pieces of text: `, ', <>, etc
        - Using delimiters is a good technique to avoid PROMPT INJECTIONS: useful if user input is present in the prompt
            - ![prompt_injections.png](images/prompt_injections.png)
    - Tactic 2: Ask for a structured output
        - To make parsing the model outputs easier, it can be helpful to ask for a structured output like HTML or JSON
    - Tactic 3: Ask the model to check whether conditions are satisfied
        - Check assumptions of completing tasks
        - If the task makes assumptions that aren't necessarily satisfied, then we can tell the model to check these assumptions first and then if they're not satisfied, indicate this and kind of stop short of a full task completion attempt
        - You might also consider potential edge cases and how the model should handle them to avoid unexpected errors or result
    - Tactic 4: "Few-shot" prompting
        - Give susccessful examples of completing tasks. Then ask model to perform the task

## principle 2
- Give the model time to “think”
    - If a model is making reasoning errors by rushing to an incorrect conclusion, you should try reframing the query to request a chain or series of relevant reasoning before the model provides its final answer.
    - Another way to think about this is that if you give a model a task that's too complex for it to do in a short amount of time or in a small number of words, it may make up a guess which is likely to be incorrect.
        - If you ask someone to complete a complex math question without time to work out the answer first, they would also likely make a mistake.
        - So in these situations, you can instruct the model to think longer about a problem which means it's spending more computational effort on the task. 
- Principle 2 tactics:
    - Tactic 1: Specify the steps required to complete a task
    - Tactic 2: Instruct the model to work out its own solution before rushing to a conclusion & then comparing it to the input
        - sometimes we get better results when we kind of explicitly instruct the models to reason out its own solution before coming to a conclusion
        - this is kind of the same idea that we were discussing about giving the model time to actually work things out before just kind of saying if an answer is correct or not, in the same way that a person would

## model limitations
- Hallucination:
    - hallucination = fabricated ideas = makes statements that sound plausible but are not true
    - the model might try to answer questions about obscure topics and can make things up that sound plausible but are not actually true
    - the reason why it happens: the model is being exposed to a vast amount of knowledge during its training process, it has not perfectly memorised the information it's seen, and so it doesn't know the boundary of its knowledge very well
- Tactic to reduce hallucinations:
    - ask the model to first find relevant information, then answer the question based on the relevant information

## model temperature
**Note: this is from lecture 07:expanding**
- This is one of models parameters
- This kind of allows you to vary the kind of degree of exploration and variety in the kind of models responses.
- How to choose a temperature:
    - At a temperature of zero, the model will always choose the most likely next word
    - At a higher temperature, it will kind of also choose one of the less likely words and at an even higher temperature
    - If you're trying to build a system that is reliable and predictable, you should go with temperature zero
    - If you're trying to kind of use the model in a more creative way where you might kind of want a kind of wider variety of different outputs, you might want to use a higher temperature
- ![temperature.png](images/temperature.png)

# additional notes
- get openai API key: https://platform.openai.com/account/api-keys
- openai billing page: https://platform.openai.com/account/billing/overview
- evaluate LLMs: https://github.com/openai/evals
- hallucinations: https://news.ycombinator.com/item?id=33841672
- more principles: https://www.promptingguide.ai/models/chatgpt https://www.promptingguide.ai/introduction/basics https://www.promptingguide.ai/introduction/tips
- prompt generator prompt: https://gist.github.com/solrevdev/c9ada9de794237acdd5028418cea8ec5
