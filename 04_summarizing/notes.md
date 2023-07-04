# notes
- one of the most exciting applications of large language models is to use it to summarise text
    - example of an use case: summarise articles so one could just kind of read the content of many more articles than one previously could

## summarize
- use case: summarize e-commerce reviews
    - If you're building an e-commerce website and there's just a large volume of reviews, having a tool to summarise the lengthy reviews could give you a way to very quickly glance over more reviews to get a better sense of what all your customers are thinking
    - The prompt for the use case: "Your task is to generate a short summary of a product review from an ecommerce site. Summarize the review below in at most 30 words."
- use case 2: add a focus: summarize e-commerce reviews to give feedback to the shipping department
    - just modify the prompt: add "... to give feedback to the Shipping department"
    - same can be done for any department, like "pricing" department - new answer will reflect and completely rebuild the answers
- use case 3: summarize multiple reviews to make them easier to read
    - idea: if you have a website where you have hundreds of reviews, you can imagine how you might use this to build a dashboard to take huge numbers of reviews, generate short summaries of them so that you or someone else can browse the reviews much more quickly. This can help you efficiently get a better sense of what all of your customers are thinking. 
    - input: kind of long, detailed reviews from our Clients
    - output: summarized, at requested short size, short mini-reviews that are easy to read
    

## extract
- Summarization gives us not only the relevant information as we requested, but also some other information, which you could decide may or may not be helpful.
- So depending on how you want to summarize it, you can also ask it to extract information rather than summarize it.
- Prompt to extract information:
    - Your task is to extract relevant information from a product review from an ecommerce site to give feedback to the Shipping department. From the review below, extract the information relevant to shipping and delivery. Limit to 30 words. 

# additional notes
- e-commerce ChatGPT prompts: https://www.ecommerceprompts.com/
- chatgpt for e-commerce use cases: https://writesonic.com/blog/chatgpt-for-ecommerce/
- writesonic https://writesonic.com/chat
