# Week 1 – First LLM API Call

## What is this program about?
This program sends a question to Google's Gemini AI model and prints the answer on the screen. In this experiment, the question is about Artificial Intelligence.

The program reads the Gemini API key from a `.env` file. It uses that key to connect to Gemini and send the prompt.

## What I understood
I understood how to connect a Python program with an AI model using an API. I also learned that we have to keep the API key safely in an environment file instead of writing it directly in the program.

When we send a prompt, the model processes it and gives a response. We can then display that response using Python.

## Main things I learned
- How to load values from a `.env` file.
- How to read an API key using `os.getenv()`.
- How to create a Gemini client.
- How to send a prompt using `generate_content()`.
- How to print the AI response.

## Result
The program sends the question to Gemini and displays the generated answer.
