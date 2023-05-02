# source
- https://learn.deeplearning.ai/chatgpt-prompt-eng/lesson/6/transforming

# notes
- Large language models are very good at transforming its input to a different format, such as:
    - translating: inputting a piece of text in one language and transforming it to a different language
    - fixing grammar: taking as input a piece of text that may not be fully grammatical and helping you to fix that up a bit
    - transforming formats: such as inputting HTML and outputting JSON

## Translation
- LLMs are trained on a lot of text from kind of many sources, a lot of which is the internet, in many different languages
    - So this kind of gives the model the ability to do translation
    - LLMs know hundreds of languages to varying degrees of proficiency
- LLM can act as a universal translator
    - Use case:
        - Imagine you are in charge of IT at a large multinational e-commerce company.
        - Users are messaging you with IT issues in all their native languages.
        - Your staff is from all over the world and speaks only their native languages.
        - You need a universal translator! LLM might be a good choice
- Prompts:
    - Translate:
        - Translate the following English text to Spanish: ```Hi, I would like to order a blender```
    - Find out what language is it:
        - Tell me which language this is: ```Combien coûte le lampadaire?```
    - Translate into specific language forms, like in the following example "Pirate English"
        - Prompt: Translate the following text to "English pirate": ```I want to order a basketball```
        - Output: English pirate: Arrr, I be wantin' to order a basketball!
    - Transform the text into formal/informal style:
        - Prompt: Translate the following text to Ukrainian in both the formal and informal forms: 'Would you like to order a pillow?'
        - Output: Formal: Чи бажаєте ви замовити подушку? Informal: Чи хочеш замовити подушку?

## Tone transformation
- Writing can vary based on kind of an intended audience
    - writing an email to a colleague is obviously going to be quite different to the way we text to younger brother
- ChatGPT can help producing different tones = transforming your text into different tone
- Example: informal -> formal
    - Prompt: Translate the following from slang to a business letter: 'Dude, This is Joe, check out this spec on this standing lamp.'
    - Output: Dear Sir/Madam, I am writing to bring to your attention a standing lamp that I believe may be of interest to you. Please find attached the specifications for your review. Thank you for your time and consideration. Sincerely, Joe
- You can create your own unique tone and reuse it with every prompt

## Format transformation
- ChatGPT is very good at translating between different formats such as JSON to HTML, XML, Markdown
- Important: The prompt should describe the input and output formats.
- Example: transform json to html:
    - Prompt: Translate the following python dictionary from JSON to an HTML table with column headers and title: {data_json}

## Spellcheck / Grammar check
- This is a really popular kind of task for ChatGPT
- It's especially useful when you're working in a non-native language
- Example: find out grammatical/spelling errors:
    - Prompt: Proofread and correct the following text and rewrite the corrected version. If you don't find and errors, just say "No errors found". Don't use any punctuation around the text: ``text``
- Example 2: follow the APA style (APA = APA Style is used by writers in many disciplines around the world for concise, powerful, and persuasive scholarly communication)
    - Prompt: proofread and correct this review. Ensure it follows APA style guide and targets an advanced reader.
