# notes
- Inferring: deduce or conclude (something) from evidence and reasoning rather than from explicit statements.
- Inferring tasks: tasks where the model takes a text as input and performs some kind of analysis
    - examples:
        - extracting labels
        - extracting names
        - understanding the sentiment of a text
- LLM advantage #1: you can speed up your development workflow by using LLM instead of building custom ML model:
    - Traditional ML: collect the label data set, train the model, figure out how to deploy the model somewhere in the cloud and make inferences
    - LLM: just write a prompt and have it start generating results pretty much right away
- LLM advantage #2: you can just use one model, one API, to do many different tasks rather than needing to figure out how to train and deploy a lot of different models
- LLM advantage #3: you can do multiple tasks at once = extract all the analytics information at once:
    - Prompt: Identify the following items from the review text: - Sentiment (positive or negative) - Is the reviewer expressing anger? (true or false) - ... - ...
    - Output:   "Sentiment": "positive",  "Anger": false,  "Item": "lamp with additional storage",  "Brand": "Lumina"

## Sentiment analysis
- Prompt to analyze a product review:
    - Prompt: What is the sentiment of the following product review, which is delimited with triple backticks?
    - Output: The sentiment of the product review is positive.
- Modify the output so that LLM answers with more concise responses:
    - Prompt: What is the sentiment of the following product review, which is delimited with triple backticks? Give your answer as a single word, either "positive" or "negative".
    - Output: positive
- Identify types of emotions:
    - Prompt: Identify a list of emotions that the writer of the following review is expressing. Include no more than five items in the list. Format your answer as a list of lower-case words separated by commas.
    - Output: happy, satisfied, grateful, impressed, content
    - Use case: find the reviews where the customer is extremely angered with a product/service

## Extracting data
- Use case #2: Extract product and company name from customer reviews
    - Prompt: Identify the following items from the review text: - Item purchased by reviewer - Company that made the item. If the information isn't present, use "unknown" as the value.
    - Output: "Item": "lamp", "Brand": "Lumina"
    - Use case: use the output data for internal automated analysis tool
    - Use case 2: focus on reviews about specific brands

## Inferring topics
- Inferring topics = Given a long piece of text, identify what is this piece of text about? What are the topics?
- Example:
    - Prompt: Determine five topics that are being discussed in the following text. Make each item one or two words long. Format your response as a list of items separated by commas.
    - Output: 'government survey', ' job satisfaction', ' NASA', ' Social Security Administration', ' employee concerns'
    - Use case: group reviews by automatically extracted topics
- Example 2:
    - Prompt: Determine whether each item in the following list of topics is a topic in the text below. Give your answer as list with 0 or 1 for each topic. List of topics: Text sample: 
    - Output: nasa: 1 local government: 0 engineering: 0 employee satisfaction: 1 federal government: 1
    - Use case: make a new alert when it is about e-commerce, or our business

# additional notes
- Using ChatGPT as a tool for the analysis of text data: https://mande.co.uk/2023/lists/software-lists/using-chatgpt-as-a-tool-for-the-analysis-of-text-data/
- Sentiment Analysis with ChatGPT, OpenAI and Python: https://medium.com/data-and-beyond/sentiment-analysis-with-chatgpt-openai-and-python-use-chatgpt-to-build-a-sentiment-analysis-ai-2b89158a37f6
- Chrome Extention: review analyzer: https://github.com/serpapi/review-analyzer?ref=serpapi.com
