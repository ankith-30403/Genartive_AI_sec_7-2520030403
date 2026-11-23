# Week 2 – Working with Different LLM Providers

## What is this program about?
This program allows the user to choose between two AI providers: Google Gemini and Ollama. After selecting a provider, the user enters a question and the program displays the answer.

The code uses a common `LLMProvider` structure. Gemini and Ollama have their own classes, but both provide a `generate()` method. The `LLMClient` uses the selected provider to get the response.

## What I understood
I understood that we do not need to write completely different application code for every AI model. We can create a common structure and connect different providers to it.

Gemini runs through Google's API, while Ollama can run a model locally on the computer. The program also checks the selected provider and asks for the required input.

I also understood the basic use of unit testing. The test uses a fake provider to check whether the client returns the expected answer without making a real API call.

## Main things I learned
- What an abstract base class is and why it is useful.
- How Gemini and Ollama can be used through one common interface.
- How to separate provider code from the main program.
- How to take input from the user.
- How to write a simple unit test using `unittest`.

## Result
The user can select Gemini or Ollama, enter a prompt, and receive an AI-generated response. The test checks the client using a fake provider.
