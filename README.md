# What Process is Behind the Scenes When You Send a Prompt?

<img src="./assets/prompt.webp" alt="Prompt Processing" width="500">

This is a high-level overview of what happens when you send a prompt to OpenAI's API.

## 1. You Send a Prompt

When you send a prompt (your input, like a question or task) to the OpenAI API, it could be something like, "Explain photosynthesis." This prompt is sent to OpenAI’s servers, which run the language model.

## 2. Tokenization: Breaking the Prompt into Tokens

Before the model can process your prompt, it needs to break it down into smaller pieces called tokens. A token can be:

- A whole word (like “dog” or “run”).
- Part of a word (like “phot” and “osynthesis” from “photosynthesis”).
- Or even punctuation or spaces.

The model doesn’t directly work with words like we do. Instead, it works with these tokens because they allow the model to handle a wide variety of languages, symbols, and sentence structures.

## 3. Embeddings: Converting Tokens to Numbers

Once the prompt is tokenized, each token is converted into a numerical representation called an embedding. These embeddings are vectors (basically lists of numbers) that capture the meaning of the tokens and how they relate to other tokens. This step allows the model to work with mathematical representations of language.

## 4. Attention Mechanism: Understanding the Importance of Tokens

Next, the attention mechanism kicks in. This is one of the most important parts of how transformers work. Instead of looking at each word (token) one at a time, the attention mechanism allows the model to look at all tokens at once and figure out which ones are most important to the meaning of the sentence.

For example, if you asked "How do plants make food through photosynthesis?" the model would pay more attention to "plants," "make food," and "photosynthesis" because these are the core parts of your question.

## 5. Transformer Layers: Processing the Input

The model processes the tokens using its transformer architecture, which consists of many layers. Each layer has two main parts:

- **Self-attention layers**: These layers apply the attention mechanism we talked about to understand the relationships between tokens.
- **Feed-forward layers**: These layers process the information to predict the next step.

Each layer refines the understanding of the prompt, passing its output to the next layer, allowing the model to capture complex patterns in the data.

## 6. Inference: Making Predictions

Now the model does inference, which means it makes predictions based on the prompt. Here’s where the model generates the response to your prompt. It predicts one token at a time. For example, for the prompt "Explain photosynthesis," the model might first predict "Photosynthesis," then predict "is," then "the process," and so on.

This prediction process is based on probabilities. The model calculates which token is most likely to come next, and it repeats this until it has generated a full response.

## 7. The Response Is Sent Back

Once the model has finished predicting the sequence of tokens (one by one), it converts those tokens back into human-readable text and sends the response back to you via the OpenAI API.

---

# Summary with Key Concepts:

1. **Prompt**: You send a prompt to the API.
2. **Tokenization**: The prompt is broken down into smaller pieces (tokens) that are easier for the model to work with. Tokens can be whole words, parts of words, or even punctuation.
3. **Embeddings**: The model converts tokens into numbers (embeddings) that represent their meaning.
4. **Attention**: The model uses attention to figure out which tokens (words/parts) are the most important in the prompt.
5. **Transformer Layers**: The tokens pass through many layers where the model processes their relationships and refines its understanding.
6. **Inference**: The model makes predictions about what comes next by generating one token at a time, based on probabilities.
7. **Response**: The generated tokens are combined into a full response, which is sent back to you.

---

## Key Takeaway:

- **Inference** is the process where the model predicts the response, token by token.
- **Tokens** are not always the same as words—they can be parts of words or symbols, and the model processes them one at a time to generate a response.

[Back to Lesson](https://github.com/jdrichards-pursuit/week-6.1-prompt-engineering-theory/blob/main/lesson.ipynb)

[Test Your Knowledge](./quiz.md)