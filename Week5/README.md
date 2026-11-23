# Week 5 – LLM Token Usage and Budget Estimation

## What is this program about?
This program estimates the token usage and cost of an AI feature before building or using it. It takes details such as requests per day, average input and output tokens, token prices, request limits, token limits, and daily and monthly budgets.

The program calculates the expected daily and monthly token usage and cost. It also adds a safety margin and checks whether the usage and cost are within the given limits.

## What I understood
I understood that using an AI API can have a cost, and the cost depends on the number of input and output tokens. If an application receives many requests, the total cost can increase.

I learned that we should estimate the usage before building a feature. We should also check request limits, token limits, and the available budget. The safety margin gives some extra room for higher usage than expected.

The program also has unit tests to check the cost calculation and to make sure that limit checks work correctly.

## Main things I learned
- How to read configuration values from a `.env` file.
- How to use a dataclass to store budget details.
- How to calculate daily and monthly token usage.
- How to estimate input and output token costs.
- What RPM and TPM limits mean.
- How to apply a safety margin.
- How to test calculations and limit checks using `unittest`.

## Result
The program displays a token economics report and marks each check as PASS or REVIEW. In the saved output, the RPM, TPM, and daily budget checks pass, but the monthly budget needs review. The four unit tests also pass.
