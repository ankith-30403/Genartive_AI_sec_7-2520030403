# Next Token Prediction

## What is this experiment?

In this experiment, I tried to understand how a language model guesses
the next word or token in a sentence.

I gave the model an incomplete sentence and checked what it thought
could come next. The program shows the five most likely predictions
along with their probabilities.

For example, in `main.py`, I used this sentence:

`Artificial Intelligence is ruling the`

The model reads the sentence and predicts which token might come next.
It was interesting to see that it can have more than one possible
answer.

## Files used

-   `main.py` -- This file uses GPT-2. It loads the model, gives it a
    sentence, and prints the top five next-token predictions.
-   `huggingface.py` -- This file does a similar experiment, but it
    connects to a model using the Hugging Face API.
-   `.env` -- I use this file to keep the Hugging Face token and model
    ID needed by `huggingface.py`.
-   `requirements.txt` -- This file has the Python libraries that need
    to be installed before running the programs.

## What is needed?

-   Python
-   An internet connection
-   The libraries listed in `requirements.txt`
-   A Hugging Face access token to run `huggingface.py`

## How I ran the programs

First, I opened the project folder in VS Code and opened the terminal.

I created and activated a virtual environment:

``` bash
python -m venv venv
venv\Scripts\activate
```

Then I installed the required libraries:

``` bash
pip install -r requirements.txt
```

To run the GPT-2 program, I used:

``` bash
python main.py
```

To run the Hugging Face API program, I used:

``` bash
python huggingface.py
```

## Hugging Face setup

Before running `huggingface.py`, the `.env` file needs these values:

``` env
HF_TOKEN=your_hugging_face_token
HF_MODEL_ID=your_model_id
```

I need to replace these example values with a valid token and a model ID
that supports the features used in the program. I should keep my real
token private and should not push it to GitHub.

## What I understood

Before doing this experiment, I thought the model simply predicts the
next word. Now I understand that it works with tokens, which can be
whole words or smaller parts of words.

In `main.py`, GPT-2 gives scores for possible next tokens. The program
uses softmax to turn those scores into probabilities and displays the
top five results.

I also understood that Hugging Face lets us connect to a model online
through an API, instead of loading the model directly on our computer.

Overall, this experiment helped me understand the basic idea of
next-token prediction and how Python can be used to try it with GPT-2
and Hugging Face.
