# Week 3 – LLM Usage Monitoring and Logging

## What is this program about?
This program improves the LLM client by tracking details about each AI request. It supports Gemini and Ollama, and records information such as the provider, model, input tokens, output tokens, response time, estimated cost, and request status.

The `UsageLogger` saves the usage details in a MongoDB database. The client also retries some temporary errors, such as timeouts or service errors, up to three attempts.

## What I understood
I understood that getting an answer from an AI model is not the only important part of an application. We should also know how much time a request takes, how many tokens are used, and what the estimated API cost is.

I learned that Gemini provides token usage information and that the program can use it to estimate the hosted API cost. Ollama is treated as local inference, so the program records its hosted API token charge as zero.

I also understood why logging is useful. If a request succeeds or fails, its details can be recorded so that we can check usage later. The retry feature gives temporary errors another chance before the program reports a failure.

## Main things I learned
- How to store request details in a dataclass.
- How to measure response time.
- How to read input and output token counts.
- How to estimate the Gemini API cost.
- How to save usage records in MongoDB.
- How retry logic can handle temporary errors.
- How to test the client with a fake provider and fake logger.

## Result
The program generates an AI response and prints usage information. The request details are saved in MongoDB when the database connection is available. The included test checks the response and logged token count.
