# Week 4 – Comparing Tokenizers

## What is this program about?
This program compares three tokenizers:
- BPE using GPT-2
- WordPiece using Multilingual BERT
- SentencePiece using XLM-R

It tests the same type of text in English, Telugu, and Hindi. For each tokenizer, the program displays the tokens, token IDs, and total token count.

## What I understood
I understood that AI models do not directly process normal sentences in the same way humans read them. A tokenizer first divides the text into smaller pieces called tokens. These tokens are converted into numbers called token IDs, which the model can process.

Different tokenizers may split the same sentence in different ways. This can also happen when we use different languages. So, the number of tokens for one sentence may change depending on the tokenizer.

## Main things I learned
- What tokenization means.
- The basic idea of BPE, WordPiece, and SentencePiece.
- How to load tokenizers using Hugging Face Transformers.
- How to convert text into tokens and token IDs.
- How to compare token counts for English, Telugu, and Hindi.

## Result
The program prints the tokens, token IDs, and token count for each language using all three tokenizers. This helps us compare how they divide the text.
