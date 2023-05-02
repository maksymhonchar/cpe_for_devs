# source
https://learn.deeplearning.ai/chatgpt-prompt-eng/lesson/7/expanding

# notes
- Expanding is the task of taking a short piece of text and having the large language model generate a longer piece of text
    - example of short piece of text: a set of instructions, a list of topics
    - example of longer piece of text: an email or an essay about some topic
- Example:
    - use a large language model as a brainstorming partner
- Note: expanding might be used for bad:
    - there are some problematic use cases of this, such as if someone were to use it, they generate a large amount of spam
    - please use it only in a responsible way and in a way that helps people

## Use LLM to generate a personalized email
- Task:
    - given: a customer review and the sentiment 
    - output: we're going to generate a custom response
- How to achieve decent results:
    - define the role: You are a customer service AI assistant
    - define the task: Your task is to send an email reply to a valued customer
    - define the personalization:
        - ... to a valued customer
        - If the sentiment is positive or neutral, thank them for their review.
        - If the sentiment is negative, apologize and suggest that they can reach out to customer service. 
        - Make sure to use specific details from the review.
    - Sign the email as `AI customer agent` -> acknowledge this is AI, not a Human - be responsible (?..)
- Try modifying the temperature parameter to a higher (than 0) value to make your responses more creative

# additional notes
- 5 Ways to Detect Text Written by ChatGPT and Other AI Tools https://www.pcmag.com/how-to/how-to-detect-chatgpt-written-text
